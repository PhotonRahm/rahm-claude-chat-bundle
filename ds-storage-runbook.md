# DS Storage Runbook

Last updated: 2026-05-09

## Normal State: GREEN / TARGET

- `ds-storage-pressure-monitor.timer` runs every 15 minutes.
- `ds-shadow-retention-engine.timer` runs every 6 hours in dry-run unless
  explicitly enabled.
- No operator action required.
- Confirm state in full picture under `DATABASE STORAGE HEALTH`.

## WARN: YELLOW

Meaning: disk usage crossed `DS_STORAGE_WARN_DISK_PCT` or active DB is above
its target envelope.

Expected automation:
- retention engine uses the WARN disabled-unresolved threshold;
- pressure monitor starts the retention engine when the last retention run is
  at least 1 hour old;
- full picture shows a TOP RISKS storage item;
- trading bots are not touched.

Operator action:
- review `data/storage_pressure_status.json`;
- review `data/retention_engine_status.json`;
- review new non-DS disk anomalies from `data/disk_hygiene_audit.json`.

## CRITICAL: ORANGE

Meaning: disk usage crossed `DS_STORAGE_CRITICAL_DISK_PCT`.

Expected automation:
- disabled unresolved archival becomes more aggressive;
- pressure monitor starts the retention engine when the last retention run is
  at least 15 minutes old;
- `TIER_E_DISPOSABLE` prune stays autonomous;
- sealed archive compression runs on every retention cycle while pressure
  remains elevated;
- full picture reports ORANGE.

Operator action:
- review surfaced TIER_C/D classification questions if compression and TIER_E
  prune cannot bound growth;
- verify compression ratios and archive envelope state;
- avoid touching live trading bots unless reconciliation separately fails.

## HARD_LIMIT: RED / PROTECT_TRADING

Meaning: disk usage crossed `DS_STORAGE_HARD_LIMIT_DISK_PCT`.

Expected automation:
- `PROTECT_TRADING` marker is written under workspace data;
- non-trading shadow writes are blocked;
- `ds-shadow-expansion-scanner.service` and `sports-ds-forward-scanner.service`
  are stopped;
- Gemini, Kalshi, and IBKR live trading bots remain running.

Exit:
- system auto-exits when disk usage drops below HARD_LIMIT;
- operator can remove the marker only after confirming pressure has dropped.

## First-Time Prune Approval

Routine `TIER_E_DISPOSABLE` pruning no longer requires operator approval.
The 2026-05-09 autonomous prune dispatch is standing approval for rows that
pass the explicit TIER_E classification and guardrails. TIER_A/B/C/D pruning
still requires an operator classification decision and is not automated.

## Recovery Utility

Hot archives are queried by archive-aware readers directly. Warm/cold zstd
archives are transparently decompressed to temporary files by
`ds_shadow_archive_reader.py` for report/research queries. For manual recovery,
use:

```bash
cd ~/.openclaw/workspace
python3 scripts/ds_archive_recover.py 2026-05
```

Recovered SQLite files are for ad hoc analysis; the live active DB remains the
only write target.

## WAL Checkpointing

- SQLite `wal_autocheckpoint` is expected to be 1000 pages (~4 MiB).
- If `data/ds_shadow_expansion.db-wal` exceeds 50 MiB outside an active bulk
  archive run, run:

```bash
sqlite3 ~/.openclaw/workspace/data/ds_shadow_expansion.db \
  "PRAGMA busy_timeout=60000; PRAGMA wal_checkpoint(TRUNCATE);"
```

## Kalshi Sports Classification

- Broad `kalshi:sports` rows in `ds_shadow_expansion_signals` are classified
  `TIER_C_RESEARCH` as of 2026-05-09 (after the evening audit reconciliation).
- The earlier intent during the autonomous prune dispatch was
  `TIER_E_DISPOSABLE`. The 90-day actionable-signal guardrail in the retention
  engine detected recent actionable rows in the `kalshi:sports` stream and
  triggered a safety-direction reclassification to `TIER_C_RESEARCH`. The
  guardrail functioning as designed is the reason the classification changed;
  this is not an error.
- `kalshi:entertainment` rows in `ds_shadow_external_observations` were
  reclassified to `TIER_C_RESEARCH` on the same basis.
- The only stream currently classified `TIER_E_DISPOSABLE` is
  `ds_shadow_expansion_signals|sports_data|sports`, where the guardrails
  found zero recent actionable signal and zero resolved live-trade reference.
- This applies only to historical broad/heuristic/favorite-tracking sports
  rows. Productive sports research remains in `sports_ds_forward_detections`,
  `sports_ds_forward_quotes`, and `sports_ds_contract_links`.
- `DS_SHADOW_SPORTS_BROAD_BACKFILL_ENABLED=false` remains the scanner guard;
  retention archives old unresolved `kalshi:sports` broad rows under pressure.

## Growth Rate Alarm

- If disk usage grows by more than 5 percentage points over a 24-hour lookback,
  the pressure monitor emits a TOP_RISK growth-rate alarm in addition to normal
  pressure-tier actions.

## TIER_E Autonomous Prune

TIER_E means disposable. Once a stream is explicitly classified
`TIER_E_DISPOSABLE`, the retention engine may delete rows without further
operator approval.

Policy:
- operator approval is not required for routine TIER_E pruning;
- unclassified streams default to `TIER_C_RESEARCH`, not TIER_E;
- TIER_A_LIVE_DECISION, TIER_B_METHODOLOGY, TIER_C_RESEARCH, and TIER_D_AUDIT
  are never pruned by the TIER_E phase;
- normal/WARN prune floor is 30 days;
- CRITICAL disk pressure compresses the floor to 14 days for that run;
- HARD_LIMIT compresses the floor to 7 days for that run while
  PROTECT_TRADING blocks non-trading shadow writes.

Guardrails:
- a stream must be explicitly listed as `TIER_E_DISPOSABLE` in
  `ds-storage-value-tiers.json`;
- any recent actionable signal in the trailing 90 days blocks TIER_E pruning
  for that platform/category;
- any resolved live-trade symbol reference blocks TIER_E pruning for that
  stream.

If a category should be preserved indefinitely, classify it
`TIER_C_RESEARCH` or higher. TIER_E means rows older than the active pressure
floor can be deleted without further notice.

## Autonomous Archive Compression

The retention engine has a compression phase after the existing archive and
TIER_E phases. It uses the existing archive tier-rotation verifier to compress
sealed monthly DS shadow archive DBs with `zstd -19`, then deletes the source
SQLite file only after all checks pass.

Policy:
- compression applies only to `ds_shadow_expansion` monthly archive files;
- active write-path DBs, live trading DBs, and the currently-open monthly
  archive are never compressed;
- a monthly archive is eligible only after the calendar month closes and the
  seal grace has elapsed;
- normal seal grace is 7 days, WARN uses at most 3 days, CRITICAL uses at
  most 1 day, and HARD_LIMIT uses 0 days;
- archives under 100 MiB or modified in the last 24 hours are skipped;
- compression is idempotent when a `.zst` companion or warm/cold compressed
  archive already exists.

Verification before source deletion:
- source SQLite `quick_check` must return `ok`;
- zstd compression and `zstd --test` must succeed;
- decompressed temp copy must pass SQLite `quick_check`;
- row counts for known archive tables must match;
- failures are logged and the source file is preserved.

Archive-aware readers transparently handle compressed archives. `scripts/
ds_shadow_archive_reader.py` prefers an uncompressed `.db` if present, otherwise
decompresses `.zst` archives into `data/.archive_cache/` using a cache key based
on compressed-file mtime and size. Cache entries older than 7 days or beyond
the 20 GiB cache cap are evicted automatically.

## Archive Size Envelope

The pressure monitor tracks `archive_total_bytes` separately from active DB
size and total disk pressure.

Envelope:
- TARGET: under 30 GiB;
- WARN: 50 GiB or more;
- CRITICAL: 80 GiB or more;
- HARD_LIMIT: 120 GiB or more.

When archive state is WARN or higher, the pressure monitor can start the
retention engine even if total disk pressure is temporarily normal. Archive
growth above 5 GiB over 24 hours emits a TOP_RISK alert.

## Tier Rotation Diagnosis

The tier-rotation framework is functional but dormant in the current archive
shape. It produced `actions=0` because the only large archive file is the open
`2026-05` monthly archive; by policy, the active month is not sealed and is
not compressed. The framework remains the verified compression mechanism for
closed monthly archives. Expected first production action is after May 2026
closes and the pressure-adjusted seal grace elapses.

## Non-DS Disk Hygiene

`disk-hygiene-audit.timer` runs daily and writes
`data/disk_hygiene_audit.json`. It is read-only: it reports the top disk
consumers under `/home/kingeric`, files over 5 GiB, and directory growth over
1 GiB/day. It does not delete non-DS data.

`database-autonomous-maintenance.timer` runs daily at 05:40 CDT and performs
the maintenance actions that are explicitly safe and re-runnable:
- SQLite Online Backup API backups for DS shadow, Polymarket, Kalshi, Gemini,
  and IBKR DBs;
- zstd compression for those backups at a bounded daily-backup level;
- backup retention: last 7 daily, last 4 Sunday weekly, last 12 first-of-month
  monthly;
- latest-backup decompression plus SQLite `quick_check`;
- quick_check for known DBs;
- passive WAL checkpoints for trading DBs and truncate checkpoints for
  non-trading DBs;
- classification drift audit with only safe-direction auto-change
  (`TIER_E_DISPOSABLE` to `TIER_C_RESEARCH`);
- regeneration-only cache cleanup for paths listed in
  `non-ds-cache-tiers.json`;
- `/tmp` and `ephemeral/` TTL cleanup.

Daily backup restore pattern:

```bash
zstd -d ~/.openclaw/workspace/backups/<db>/<db>_YYYYMMDD.db.zst -o /tmp/<db>.db
sqlite3 /tmp/<db>.db 'PRAGMA quick_check;'
```

Trading DB hygiene invariant:
- allowed: read-only metrics, SQLite Online Backup API, `PRAGMA
  wal_checkpoint(PASSIVE)`;
- blocked: VACUUM, exclusive-lock maintenance, pruning, schema rewrites, or
  delete operations while the trading bot is running.

The 2026-05-09 disk incident was primarily a `/tmp` leak from full-picture
SQLite report snapshots. `scripts/full_picture.py` now uses a managed temporary
directory under `~/.openclaw/workspace/ephemeral/` so report snapshots are
removed after the report completes. Existing `/tmp/rahm_full_picture_*`
directories were deleted after confirming no open file holders.

Ephemeral output pattern:
- scratch outputs go under `~/.openclaw/workspace/ephemeral/`;
- tools should use `tempfile.TemporaryDirectory(dir=EPHEMERAL_DIR)` or a
  try/finally cleanup;
- the daily maintenance run deletes entries older than 7 days.

User log rotation:
- `logrotate-user.timer` runs daily at 05:20 CDT;
- current policy rotates `/home/kingeric/.codex/log/*.log` daily or at 500 MiB,
  keeps 7 compressed rotations, and uses `copytruncate` so active Codex file
  handles remain valid.

Polymarket:
- `polymarket.db` is classified as research-grade shadow data, not disposable
  cache. It is covered by daily backup and integrity checks. No prune is
  deployed until per-table downstream value is separated.

## Automatic vs Operator Attention

Automatic:
- TIER_E prune after explicit classification and guardrails;
- sealed monthly archive compression;
- pressure-triggered retention cadence;
- disk and archive growth alarms;
- read-only non-DS disk anomaly reporting;
- daily DB backups and backup verification;
- weekly-style quick integrity checks through the daily maintenance status;
- safe-direction classification drift correction;
- regenerable cache cleanup;
- user log rotation.

Operator attention:
- TIER_C/D reclassification or deletion decisions;
- non-DS large-file cleanup beyond obvious report-snapshot temp files;
- trading DB growth;
- HARD_LIMIT events if compression and TIER_E prune cannot restore headroom.
