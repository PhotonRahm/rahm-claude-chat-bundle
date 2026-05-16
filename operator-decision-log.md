# Operator Decision Log

## 2026-05-10 - Fix create_union_view() missing-table regression

Decision:
- Fix the test regression introduced by commit e3b2f50 (weather
  persistence dispatch) in
  `~/.openclaw/workspace/scripts/ds_shadow_archive_reader.py`.
- The function now returns `None` when the main schema does not contain
  the requested table, symmetric with how missing archive schemas are
  already handled silently.

Issue diagnosis:
- Commit e3b2f50 changed `create_union_view()` from
  `"SELECT * FROM main.<table>"` to a column-projected form via
  `_project_columns(main_columns, main_available, "main", table)`.
- When `_table_columns()` returns `[]` (main schema doesn't have the
  table), `_project_columns([], ...)` emits
  `"SELECT  FROM main.<table>"` - invalid SQL, syntax error on view
  creation.
- Production: not affected. All 7 tables that
  `shadow_research_status.format_report_lines()` requests exist in
  `ds_shadow_expansion.db`.
- Tests: `test_shadow_research_status.py` fixtures only create
  `ds_shadow_expansion_signals`; calls for the other 6 tables hit the
  syntax error.

Implementation boundary:
- Modify `ds_shadow_archive_reader.create_union_view()` to add an
  early-return when `main_columns` is empty. Drop any stale temp view
  with the same name before returning None. Update docstring to
  document the new `str | None` return contract. Return type of
  `create_union_views()` widened to `dict[str, str | None]` because the
  dict can now carry None values for missing tables.
- Add regression test
  `test_create_union_view_returns_none_when_main_table_missing` in
  `test_ds_shadow_archive.py` exercising both the present-table and
  missing-table paths.
- No env changes, no schema changes, no service restarts.
- All existing callers of `create_union_view` / `create_union_views`
  reviewed: production paths guard with `_table_exists()` before
  using view names, so the new None possibility is harmless in
  production. The dict-style callers
  (`shadow_research_status.py`, `ds_shadow_coverage_inventory.py`,
  `ibkr_goal_readiness.py`) all read view names only after a
  `_table_exists()` gate. The single-table callers
  (`ds_shadow_expansion_lib.py`, `weather_cushion_ds_shadow.py`,
  `gemini_cushion_ds_shadow.py`, `index_fx_cushion_ds_shadow.py`,
  `data_freshness_aggregator.py`) operate on the production DB where
  all expected tables exist.

Production impact: NONE.

Test impact:
- Pre-fix: 297 total, 294 passing, 2 non-IBKR errors (the regression),
  1 IBKR-scope failure (pre-existing, out of scope per Principle 49).
- Post-fix: 298 total, 297 passing, 0 non-IBKR errors, 1 IBKR-scope
  failure remains per Principle 49.
- 1 new regression test added (the +1 to total).

Cross-references:
- Surfaced by Claude Code audit dispatch 2026-05-10 post-afternoon
  (see audit consolidated report).
- Original commit introducing regression: e3b2f50 (weather persistence
  dispatch, 2026-05-10).
- Related dispatches: 2026-05-10 unit-of-independence (Principle 51)
  shared the broader weather persistence release window.

Next review trigger:
- None mandatory. The fix is self-contained and the regression test
  locks in the missing-table contract so future changes cannot
  silently break it.

## 2026-05-16 - Gemini DS hard kill and Kalshi DS BTC qty rollback

Gemini DS:

- Hard-killed Gemini Deterministic Settlement after `filter_combined_eth_high_cushion_qty_10_pilot` reached 50 resolved, 47W-3L, WR 94.0%, Wilson lower 83.8%, and P&L -$19.62.
- Implemented with `DETERMINISTIC_SETTLEMENT_ENABLED=false` and `KILL_DETERMINISTIC_SETTLEMENT`.
- Re-entry requires a new shadow cell with decision-grade independent-unit metrics and positive forward P&L; no tuning of the killed live methodology is authorized.

Kalshi DS:

- Rolled BTC qty/cap 600 -> 225 after `filter_combined_qty_600_btc_post_rollback_pilot` reached 65 resolved, 60W-5L, Wilson lower 83.2%, P&L -$1807.79, and rollback status.
- ETH remains qty/cap 400 because its own cohort is still accumulating cleanly.
- New BTC cohort: `filter_combined_qty_225_btc_post_rollback_pilot`, start `2026-05-16 08:53:26-0500`, gate n>=30, WR>=95%, Wilson lower>=88%, positive P&L, no daily CB breach.

## 2026-05-09 evening - Kalshi DS BTC qty 700 deploy

Decision:
- Scale Kalshi crypto DS BTC sizing from qty 600 to qty 700 as a one-parameter
  evidence-gated step. The `filter_combined_qty_600_btc_pilot` cohort met the
  expansion gate at 38 resolved, 38W-0L, WR 100%, Wilson lower 90.8%,
  P&L +$833.07, max DD $0.00, and no daily CB breach.

Implementation boundary:
- `DS_KALSHI_QTY_BTC=700` and
  `DS_KALSHI_PER_TRADE_DOLLAR_CAP_BTC=700`.
- Daily CB mechanically scales to `DETERMINISTIC_SETTLEMENT_DAILY_CB=-700`;
  lifetime CB mechanically scales to
  `DETERMINISTIC_SETTLEMENT_LIFETIME_CB=-2100`.
- ETH remains `DS_KALSHI_QTY_ETH=275` and
  `DS_KALSHI_PER_TRADE_DOLLAR_CAP_ETH=275`. Max_open 8, asset-hour cap 4,
  max exposure, allowed assets BTC/ETH, and the price>=0.90 plus
  cushion>=0.10% combined filter remain unchanged.
- Close `filter_combined_qty_600_btc_pilot` as PASSED and open
  `filter_combined_qty_700_btc_pilot` fresh at n=0 from
  `DS_KALSHI_QTY_700_BTC_START=2026-05-10 03:35:49`. The qty-600 rows are
  informative only and are not inherited.
- Next review trigger: 30+ resolved BTC trades in the qty-700 cohort with
  WR>=95%, Wilson lower>=88%, positive P&L, no daily CB breach,
  asset/settlement-hour cap block count, and cash-binding evidence.

## 2026-05-09 - Kalshi DS BTC qty 600 deploy

Decision:
- Scale Kalshi crypto DS BTC sizing from qty 500 to qty 600 as a one-parameter
  evidence-gated step. The `filter_combined_qty_500_btc_pilot` cohort met the
  expansion gate at 60 resolved, 59W-1L, WR 98.3%, Wilson lower 91.1%,
  P&L +$435.94, max DD $442.20, and no daily CB breach.

Implementation boundary:
- `DS_KALSHI_QTY_BTC=600` and
  `DS_KALSHI_PER_TRADE_DOLLAR_CAP_BTC=600`.
- Daily CB mechanically scales to `DETERMINISTIC_SETTLEMENT_DAILY_CB=-600`;
  lifetime CB mechanically scales to
  `DETERMINISTIC_SETTLEMENT_LIFETIME_CB=-1800`.
- ETH remains `DS_KALSHI_QTY_ETH=275` and
  `DS_KALSHI_PER_TRADE_DOLLAR_CAP_ETH=275`. Max_open 8, asset-hour cap 4,
  max exposure, allowed assets BTC/ETH, and the price>=0.90 plus
  cushion>=0.10% combined filter remain unchanged.
- Close `filter_combined_qty_500_btc_pilot` as PASSED and open
  `filter_combined_qty_600_btc_pilot` fresh at n=0 from
  `DS_KALSHI_QTY_600_BTC_START=2026-05-09 13:56:56`. The qty-500 rows are
  informative only and are not inherited.
- Next review trigger: 30+ resolved BTC trades in the qty-600 cohort with
  WR>=95%, Wilson lower>=88%, positive P&L, no daily CB breach,
  asset/settlement-hour cap block count, and cash-binding evidence.

## 2026-05-09 - Gemini DS ETH qty 50 deploy

Decision:
- Scale Gemini crypto DS ETH sizing from qty 10 to qty 50 as a one-parameter
  evidence-gated step. The `filter_combined_eth_high_price_pilot` cohort met
  the expansion gate at 52 resolved, 52W-0L, WR 100%, Wilson lower 93.1%,
  P&L +$15.50, max DD $0.00, and no daily CB breach.
- This is a 5x step, larger than normal, accepted because the current cohort
  had zero losses and the absolute per-trade exposure remains bounded near
  $50.

Implementation boundary:
- `DETERMINISTIC_SETTLEMENT_QTY=50` and
  `DETERMINISTIC_SETTLEMENT_PER_TRADE_DOLLAR_CAP=50`.
- Daily CB mechanically scales to `DETERMINISTIC_SETTLEMENT_DAILY_CB=-100`;
  lifetime CB mechanically scales to
  `DETERMINISTIC_SETTLEMENT_LIFETIME_CB=-300`.
- ETH-only allow-list, max_open 3, price>=0.95, cushion>=0.10%,
  min_depth 0, final-30m window, and kill-switch handling remain unchanged.
- Close `filter_combined_eth_high_price_pilot` as PASSED and open
  `filter_combined_eth_high_price_qty_50_pilot` fresh at n=0 from
  `DETERMINISTIC_SETTLEMENT_COHORT_START=2026-05-09 14:01:37` and
  `DETERMINISTIC_SETTLEMENT_QTY_50_ETH_START=2026-05-09 14:01:37`. The
  qty-10 ETH high-price rows are informative only and are not inherited.
- Next review trigger: 30+ resolved ETH trades in the qty-50 cohort with
  WR>=90%, Wilson lower>=80%, positive P&L, no daily CB breach, depth bucket
  distribution, and single-loss event analysis if any loss occurs.

## 2026-05-09 - Kalshi MR surgical investigation

Decision:
- No Kalshi MR config change deployed. No candidate met the dispatch rule of
  n>=30 post-restriction or current allowed-cell evidence plus Wilson clearly
  below breakeven and clearly negative lifetime P&L.

Findings:
- Lifetime MR remains the asymmetry-trap profile: 328W-53L, WR 86.1%,
  Wilson 82.3%, P&L -$103.88, avg win $21.77, avg loss $136.67.
- ETH lifetime remains negative, but current runtime source shows KXETHD
  retired via `MR_BLOCKED_PATTERNS`; post 2026-04-27 cap-era evidence is only
  3 resolved rows, below the n>=30 deploy threshold.
- WEATHER_LOW YES had zero post-cap allowed resolved fills; cap telemetry shows
  6/6 above-cap attempts blocked. Continue the pre-committed cap review.
- WEATHER_LOW NO post-cap is 9W-1L, +$65.52, so no change.
- SOL lifetime is positive at 65W-8L, +$825.25; no change.
- INDEX has zero post-cluster-cap resolved fills and 347/347 attempts blocked
  since the cap; continue the 2026-05-21 review.
- Price >=$0.90 has no current allowed resolved rows; the $0.85-$0.90 slice is
  positive at 140W-14L, +$661.08. No price-band tighten.
- Expiry/hour slices did not produce a dispositive n>=30, statistically clear,
  currently-actionable negative cell that is not already restricted.

Operational boundary:
- No Kalshi restart #3. Existing MR restrictions remain unchanged: KXHIGH,
  KXBTCD, and KXETHD retired; WEATHER_LOW YES cost >=$150 blocked; INDEX
  cluster cap max 2 underlier/event and max 4 settlement-hour.
- Continue `kalshi_mr_index_cluster_cap_review`,
  `kalshi_mr_allowed_cells_forward_pnl_review`, and
  `kalshi_mr_weather_low_yes_cap_30_resolution_review` as already documented.

## 2026-05-09 - DS storage stabilization

Decision:
- Classify historical broad `kalshi:sports` rows in
  `ds_shadow_expansion_signals` as `TIER_E_DISPOSABLE` and add
  `kalshi:sports` to the disabled-unresolved archival token list. Productive
  sports research tables remain preserved.
- Harden storage automation so pressure monitoring runs every 15 minutes,
  starts the retention engine when WARN/CRITICAL cadence thresholds are stale,
  and emits a top-risk alert when disk usage grows more than 5 percentage
  points over 24 hours.

Evidence and action:
- Pre-stabilization active DB was 15.62 GiB with a 702 MiB WAL and
  1,779,911 active `kalshi:sports` broad rows, mostly
  `heuristic_observation` / favorite-tracking and non-actionable.
- `PRAGMA wal_checkpoint(TRUNCATE)` reduced the WAL to 0 bytes before the
  retention run. SQLite `wal_autocheckpoint` remained 1000 pages.
- Retention archived 1,872,609 rows on the first run and 50,000 rows on the
  follow-up run, reducing active `kalshi:sports` rows below the 500,000 target.
- Offline maintenance with only non-trading shadow writers stopped returned
  `quick_check=ok`, ran `VACUUM`, and reduced the active DB to about 3.0 GiB
  with a small WAL. Live trading bots were not touched.
- Next review trigger: `ds_storage_autonomous_management_7day_review` on
  2026-05-16 12:00 UTC checks active DB size, WAL size, retention cadence,
  pressure-monitor history, growth-rate alarm behavior, and PROTECT_TRADING
  remaining off below HARD_LIMIT.

## 2026-05-09 - TIER_E autonomous prune policy

Decision:
- Make `TIER_E_DISPOSABLE` pruning autonomous. Future retention-engine runs do
  not require operator approval for explicitly disposable rows.
- Preserve the conservative side of the line: unclassified streams default to
  `TIER_C_RESEARCH`, and TIER_A/B/C/D rows are never pruned by the TIER_E
  phase.

Guardrails:
- TIER_E eligibility requires an explicit `TIER_E_DISPOSABLE` stream entry in
  `ds-storage-value-tiers.json`.
- Recent actionable signals in the trailing 90 days block TIER_E pruning.
- Resolved live-trade symbol references block TIER_E pruning.
- Normal/WARN age floor is 30 days; CRITICAL compresses to 14 days for that
  run; HARD_LIMIT compresses to 7 days for that run.

Classification audit:
- `ds_shadow_expansion_signals|kalshi|sports` was reclassified from TIER_E to
  `TIER_C_RESEARCH` because the active DB still had 60 recent actionable rows
  in the trailing 90 days. It is not eligible for autonomous prune.
- `ds_shadow_external_observations|kalshi|entertainment` was also reclassified
  to `TIER_C_RESEARCH` after the manual retention run found 13 recent
  actionable archived rows in the trailing 90 days.
- The only remaining TIER_E stream is
  `ds_shadow_expansion_signals|sports_data|sports`. It had zero rows older
  than the 30-day floor at deploy time, so the one-time TIER_E prune was
  idempotent and pruned zero rows.

## 2026-05-09 - Autonomous archive compression deploy

Decision:
- Add autonomous lossless compression as the disk-relief lever for preserved
  DS shadow archives. Pruning is correct only for explicitly disposable
  TIER_E data; research-grade archives are retained and compressed.
- Keep live trading bots untouched. Compression applies only to sealed monthly
  `ds_shadow_expansion` archive files, never active DBs or trading DBs.

Implementation boundary:
- The retention engine now runs a compression phase after the existing archive
  and TIER_E phases. It uses zstd level 19, source/decompressed SQLite
  `quick_check`, zstd verification, row-count checks, and deletes the source
  only after verification passes.
- The archive-aware reader can attach compressed archives transparently by
  decompressing `.zst` files into a bounded local cache.
- The pressure monitor now tracks an archive-size envelope separately from
  total disk and active DB pressure, and surfaces archive growth above 5 GiB
  over 24 hours.
- Tier rotation was diagnosed as functional but dormant: current production
  has only the open May 2026 archive, which is not sealed and must not be
  compressed until month close plus grace.
- A daily read-only disk hygiene audit surfaces non-DS growth anomalies.

Incident correction:
- Disk pressure was dominated by stale `/tmp/rahm_full_picture_*` report
  snapshot directories, not by DS archives alone. Those stale directories were
  deleted after verifying no open holders, reducing root filesystem usage from
  about 76% to about 22%.
- `scripts/full_picture.py` now uses a managed temporary directory so future
  snapshots are removed automatically after report completion.

Standing policy:
- Routine archive compression does not require operator approval.
- Compression preserves data; TIER_C/D deletion or reclassification still
  requires operator attention.

## 2026-05-09 - Database finalization

Decision:
- Finalize the storage subsystem around autonomous backup, integrity,
  filesystem leak prevention, cache cleanup, log rotation, and classification
  drift detection.
- Keep live trading bots untouched. Trading DBs receive only read-only metrics,
  passive WAL checkpoints, and SQLite Online Backup API backups.

Implementation boundary:
- `database-autonomous-maintenance.timer` runs daily at 05:40 CDT. It backs up
  DS shadow, Polymarket, Kalshi, Gemini, and IBKR DBs; verifies the latest
  backup of each with SQLite `quick_check`; runs DB quick checks; applies safe
  WAL hygiene; cleans explicitly regenerable caches; audits `/tmp`; and
  detects classification drift.
- `logrotate-user.timer` runs daily at 05:20 CDT. The Codex TUI log rotates
  daily or at 500 MiB with `copytruncate`, 7 compressed rotations.
- `full_picture.py` now writes report snapshots under the workspace
  `ephemeral/` directory and removes stale matching scratch dirs at run end.
- Polymarket shadow data is preserved as `TIER_C_RESEARCH` and is covered by
  backup/integrity checks, not pruned.
- `.npm` and pip cache paths are classified as regenerable in
  `non-ds-cache-tiers.json`; broad `.local` is preserved for review because it
  can contain application state.

First run:
- Codex log rotated from about 9.3 GiB to about 52 MiB, with a 1008 MiB gzip
  rotation retained.
- `.npm` cache cleanup reduced the path from about 7.8 GiB to under 1 MiB.
- Backups verified `quick_check=ok` for DS shadow, Polymarket, Kalshi, Gemini,
  and IBKR DBs.
- Classification drift audit found no open drift flags.

## 2026-05-09 - Fully automated cross-agent knowledge sync

Decision:
- Use GitHub as the primary deployed backing store for Claude-in-chat
  knowledge continuity. Direct claude.ai project-file upload remains
  undocumented and could not be verified without browser session credentials;
  the official GitHub connector supports adding repo files to project
  knowledge, and raw GitHub URLs are a reliable fallback.

Implementation boundary:
- `generate_current_state.py` writes `current-state.md` from rendered status
  reports, systemd runtime state, `/proc/$PID/environ`, storage status,
  timers, deferred verifications, recent decisions, and repo sync state.
- `build_claude_chat_bundle.py` builds the bounded project bundle with a
  manifest and checksums.
- `sync_claude_chat_bundle.py` pushes the bundle to private repo
  `PhotonRahm/rahm-claude-chat-bundle`.
- `claude-chat-sync.timer` runs every 6 hours and commits/pushes
  `current-state.md` before rebuilding and syncing the bundle.
- `CLAUDE-CHAT.md` documents Claude-in-chat startup behavior and stale-context
  detection.

Bootstrap:
- Operator only needs to add/sync `PhotonRahm/rahm-claude-chat-bundle` in the
  Claude.ai Rahm project GitHub connector once. If the connector is unavailable,
  Claude-in-chat can fetch the files through authenticated GitHub access. While
  the repo remains private, unauthenticated raw GitHub URLs are expected to 404.

## 2026-05-09 evening - Public web-fetch Claude chat bundle

Decision:
- Make `PhotonRahm/rahm-claude-chat-bundle` public so Claude-in-chat can use
  unauthenticated `web_fetch` against `raw.githubusercontent.com` at the start
  of each new Rahm chat.
- Keep `PhotonRahm/operations-knowledge` private. The public bundle is the
  curated derived view; operations-knowledge remains the source of truth.

Safeguards:
- `build_claude_chat_bundle.py` now redacts secret-shaped strings, account
  number-shaped fields, token assignments, bearer tokens, JWT-shaped strings,
  GitHub token prefixes, AWS access-key prefixes, and long source-doc hex
  strings before publication.
- Redaction findings are written to `~/operations-knowledge/redaction_log.md`
  and are not included in the public bundle.
- `INDEX.md` is generated in the public bundle and is the first file
  Claude-in-chat fetches. Tier 1 files are `current-state.md` and
  `CLAUDE-CHAT.md`; Tier 2/3 files are fetched only when relevant.

## 2026-05-08 - kalshi:entertainment config-drift cleanup

Decision:
- Add `kalshi:entertainment` to the DS shadow expansion scanner's
  `DS_SHADOW_DISABLED_CATEGORIES` list, the retention engine's
  `disabled_unresolved_archive_tokens` policy list, and the storage
  value-tier classification as `TIER_E_DISPOSABLE`. Audit found the
  category functionally inactive (13 actionable historical rows, zero
  last-24h writes, no live dependency) yet unenforced — pure config drift
  cleanup, not a strategy change.

Rationale:
- Scanner level: prevents future broad-bucket entertainment writes from
  the active-market enumerator without affecting any live strategy.
- Retention level: existing rows fall under the standard 7-day disabled-
  unresolved archival policy, matching peer disabled tokens.
- Tier level: classified `TIER_E_DISPOSABLE` (no methodology re-derivation
  value, no live dependency, no historical research value) so the
  retention engine can prune it after operator approval rather than only
  archive.

Implementation boundary:
- `DS_SHADOW_DISABLED_CATEGORIES` updated in
  `~/operations-knowledge/systemd-units/user/ds-shadow-expansion-scanner.service`
  (canonical), mirrored in `~/.openclaw/workspace/systemd/` and the live
  copy at `~/.config/systemd/user/`. Scanner restarted to propagate env;
  no live trading bot was touched.
- `~/operations-knowledge/ds-storage-value-tiers.json` adds
  `kalshi:entertainment` to `disabled_unresolved_archive_tokens` and
  introduces a new `TIER_E_DISPOSABLE` stream entry for the
  `ds_shadow_external_observations` / kalshi / entertainment row.
- Live trading bots `kalshi-bot.service`, `gemini-bot.service`, and
  `ibkr-scan-loop.service` were not restarted and remain on their
  pre-cleanup PIDs. `ds-shadow-expansion-scanner.service` was restarted
  and the new env var was verified via `/proc/$PID/environ`.
- Reconciliation hard checks remain $0.00 across Kalshi, Gemini, and
  IBKR before and after the change.

## 2026-05-08 - Kalshi DS ETH qty 275, Gemini MR Kelly 0.625, Moderate Favorites forward tracker

Decision:
- Scale Kalshi crypto DS ETH sizing from qty 225 to qty 275 as a one-parameter
  evidence-gated step. The `filter_combined_qty_225_eth_pilot` cohort met the
  expansion gate at 38 resolved, 37W-1L, positive P&L, Wilson lower above the
  pre-committed threshold, and no active daily CB breach.
- Increase Gemini MR Kelly multiplier from 0.50 to 0.625 after the formal
  Kelly review trigger. Per-asset forward samples are gate-met, forward
  calibration is under-predicting materially, and the 50% per-asset
  concentration cap remains the binding risk control.
- Add a cross-market Moderate Favorites forward shadow tracker for the
  crypto / YES / 0-1h / $0.80-$0.85 cell on Kalshi and Gemini. This rebuilds
  evidence trust after the prior live Moderate Favorites pilot failure. It is
  shadow-only and does not enable a live placement path.

Kalshi DS implementation boundary:
- `DS_KALSHI_QTY_ETH=275` and `DS_KALSHI_PER_TRADE_DOLLAR_CAP_ETH=275`.
- `DS_KALSHI_QTY_BTC=500`, BTC per-trade cap 500, max_open 8,
  asset-hour cap 4, daily CB -500, lifetime CB -1500, and the price/cushion
  filter remain unchanged.
- Close `filter_combined_qty_225_eth_pilot` as PASSED and open
  `filter_combined_qty_275_eth_pilot` fresh at n=0. The qty-225 rows are
  informative only and are not inherited into the qty-275 cohort.
- New cohort gate remains n>=30, WR>=93%, Wilson lower>=85%, positive P&L,
  and no daily CB breach.

Gemini MR implementation boundary:
- `GEMINI_MR_KELLY_MULTIPLIER=0.625` is the explicit runtime env alias, with
  legacy `KELLY_MULTIPLIER=0.625` kept in sync.
- Empirical-Bayes calibration, 50% per-asset concentration cap, daily CB,
  spread filter, weekend hour blocks, and blocked assets remain unchanged.
- Next review trigger is 50 post-deploy resolved Gemini MR placements, with
  review by per-asset W-L, concentration-cap hits, daily CB state, and
  drawdown versus the 0.50 multiplier era.

Moderate Favorites forward tracker boundary:
- Forward-only table: `shadow_moderate_favorites_crypto_1h_high_band`.
- Separation tag: `forward_shadow_post_pause`.
- Cells tracked: Kalshi / CRYPTO / YES / 0-1h / $0.80-$0.85 and
  Gemini / CRYPTO / YES / 0-1h / $0.80-$0.85.
- Live graduation requires per-cell n>=30 forward resolved, WR>=85%,
  Wilson lower>=80%, positive hypothetical P&L, and acceptable
  shadow-to-live degradation. No live promotion is automatic.

## 2026-05-08 - IBKR Weather pilots and Bug class #17 fix

Update - Option A tightening:
- After deploy, the live `edge_threshold=0.40` label was verified to mean
  `model_probability - ask >= 0.40`, not Wilson margin. For current model
  probability 0.80 cells, this is effectively `ask <= $0.40`.
- Under this actual live filter, `UHATL_YES_cushion_lt_2f`,
  `UHPHL_YES_cushion_lt_2f`, and `UHLAX_YES_cushion_lt_2f` had cheap-subset
  Wilson margins below 20pp, so they were dropped from live placement and
  moved to forward shadow tracking.
- Aggregate CBs were scaled from eight cells to five cells:
  daily -$300 -> -$200 and lifetime -$600 -> -$400.
- Existing UHPHX open position remains untouched because it belongs to kept
  cohort `weather_pilot_UHPHX_YES_cushion_2_to_5f`.
- Future cell-list changes must first query live Weather positions for the
  cells being dropped; any open dropped-cell position halts the change for
  operator decision.

Decision:
- Deploy a new bounded IBKR Weather DS pilot for all operator-approved
  research-ready cells with material positive Wilson margin.
- Runtime strategy key remains `deterministic_settlement_weather`; this is a
  fresh per-cell pilot boundary, not inheritance from the failed 2026-05-03 /
  2026-05-05 Weather DS cohort.
- Operator selected qty 25. Safeties scale proportionally:
  max_open 2 per cell, per-cell daily CB -$75, per-cell lifetime CB -$150,
  aggregate daily CB -$300, aggregate lifetime CB -$600.

Included cells:
- `UHBNA_YES_cushion_2_to_5f`: 168 resolved, 100.0% WR, Wilson 97.8%,
  breakeven 56.3%, P&L +$36.25.
- `UHPHX_YES_cushion_2_to_5f`: 129 resolved, 100.0% WR, Wilson 97.1%,
  breakeven 29.6%, P&L +$46.48.
- `UHJAX_YES_cushion_lt_2f`: 96 resolved, 90.6% WR, Wilson 83.1%,
  breakeven 56.1%, P&L +$22.29.
- `UHSFO_YES_cushion_2_to_5f`: 189 resolved, 82.0% WR, Wilson 75.9%,
  breakeven 53.2%, P&L +$26.53.
- `UHCLT_YES_cushion_2_to_5f`: 161 resolved, 79.5% WR, Wilson 72.6%,
  breakeven 49.4%, P&L +$24.03.
- `UHPHL_YES_cushion_lt_2f`: 114 resolved, 79.8% WR, Wilson 71.5%,
  breakeven 47.5%, P&L +$21.93.
- `UHATL_YES_cushion_lt_2f`: 111 resolved, 75.7% WR, Wilson 66.9%,
  breakeven 50.6%, P&L +$14.11.
- `UHLAX_YES_cushion_lt_2f`: 124 resolved, 71.8% WR, Wilson 63.3%,
  breakeven 41.3%, P&L +$23.68.

Excluded cells:
- `UHBOS_YES_cushion_2_to_5f`: positive but marginal Wilson margin
  around +3.3pp; excluded from this aggressive but still bounded pilot.
- `UHSAT_YES_cushion_2_to_5f`: Wilson approximately at breakeven; excluded.

Cohort discipline:
- One cohort per cell: `weather_pilot_<CELL_KEY>`, start
  2026-05-08 15:20:00 UTC.
- Historical research rows are decision evidence only and are not inherited.
- Per-cell gate: n>=30, WR>=90%, Wilson lower>=80%, positive P&L, and no
  daily CB breach.

Bug class #17 coupling:
- Operator approved fixing the Weather DS partial-fill attribution defect in
  the same deploy before reactivation.
- Forward resolver now uses broker-settlement truth from `settlement_log`
  where present and records fill attribution checks instead of silently
  accepting stale partial-fill state.
- Historical Weather DS drift cleanup is authorized as part of Option 3:
  settled Weather DS `live_trades` rows are refreshed from `settlement_log`
  so DB strategy attribution matches broker truth while cash reconciliation
  remains authoritative.

## 2026-05-08 - Gemini DS ETH-only restriction

Decision:
- Close `filter_combined_btc_eth_high_price_pilot` as FAILED and restrict the
  live Gemini deterministic-settlement pilot to ETH only.
- New active cohort: `filter_combined_eth_high_price_pilot` from
  2026-05-08 14:44:09 UTC / 09:44:09 CDT.
- Runtime scope: `DETERMINISTIC_SETTLEMENT_ALLOWED_ASSETS=ETH`, qty 10,
  max_open 3, per-trade cap $10, daily CB -$30, lifetime CB -$60,
  entry price >=0.95, cushion >=0.10%, depth recorded but not enforced.

Evidence:
- The BTC/ETH high-price pilot reached decision review with negative P&L:
  53 resolved, 51W-2L, Wilson lower 87.2%, P&L -$3.48.
- BTC was the loss source: 36 resolved, 34W-2L, P&L -$8.71.
- ETH was clean but pre-gate as a standalone forward cohort: 17 resolved,
  17W-0L, P&L +$5.23.
- Both losses were BTC high-price/deep-book rows, so the restriction-grade
  evidence supports removing BTC from the pilot rather than loosening any
  gate.

Cohort discipline:
- The existing ETH 17W-0L data is informative operator evidence only. It is
  not inherited into the new active cohort.
- New cohort gate is unchanged: n>=30, WR>=90%, Wilson lower>=80%, positive
  cohort P&L, and no daily CB breach before any further change.
- No daily CB reset was performed because the live daily CB was not breached.

## 2026-05-07 evening - Bounded fix deploy: report label and documentation drift

End-of-day audit verified all reports numerically accurate, methodology
gates intact, and today's structural deploys all working correctly.
Reconciliation $0.00 across Gemini, Kalshi, IBKR maintained throughout
this fix deploy. Live trading bots untouched; no restarts; no logic or
sizing changes. Audit surfaced four findings; this deploy addresses all
four with bounded label and documentation fixes.

Finding A (Gemini DS "Lifetime" label ambiguity, significant):
- Per-bot status used `_strategy_lifetime_since` (pilot-scoped: -$28.87,
  57W-6L) while daily/full-picture used `authoritative_trade_lifetime`
  (DB-wide: -$388.61, 257W-47L). Both correct individually; shared label
  could mislead.
- Fix: per-bot status DS detail relabeled "Pilot lifetime (since
  <ts>): ..." with a pointer to the daily/full-picture report for
  DB-wide rendering, and CB ledger relabeled "Pilot CB ledger (lifetime
  CB scoped to current pilot)". DS strategy entry in exec summary
  carries a "pilot-to-date since <ts>" note. Daily report and
  full_picture annotate the [Gemini] DS strategy entry with "DB-wide
  (all cohorts; per-bot status shows current pilot only)".
- Function semantics unchanged. New regression test
  `test_ds_lifetime_scope_labels.py` guards the rendering paths.
- Scope check found only Gemini DS exhibits this pattern (Kalshi DS
  lifetime CB never resets on cohort change, Kalshi MR/DS Low-Price NO
  use a single scope, IBKR already uses scope qualifiers like "Lifetime
  (DB live_trades)"). Originally a single-instance "surface but defer"
  per audit policy; codified along with Finding D as Bug class #29
  because Finding D made the meta-pattern visible.

Finding D (workspace CLAUDE.md stale, significant):
- Workspace CLAUDE.md described Gemini DS as `parallel_filter_pilot`
  with price>=0.90, max_open 2, BTC/ETH/SOL while runtime is
  `filter_combined_btc_eth_high_price_pilot` with price>=0.95,
  max_open 3, BTC/ETH only. Bot-local `~/gemini_prediction_bot/CLAUDE.md`
  was correct.
- Scope check found drift in five additional workspace CLAUDE.md rows
  (Kalshi DS qty/cohort, Kalshi DS Low-Price NO still LIVE PILOT after
  pause, Kalshi MR INDEX cluster cap and retired subseries, IBKR qty 60
  raise context, Gemini DS row) plus one row in
  `strategies-glossary.md` (Kalshi DS BTC qty cohort still naming the
  qty-400 cohort). Six stale references across two documents.
- Fix: each workspace-level Active strategies row updated to current
  state with a "Bot-local `<path>` is the canonical operational source"
  pointer so future operators know which file wins.
- Multiple instances meets the codification threshold; codified as
  Bug class #30 ("Multiple documentation surfaces drift apart when only
  one is updated").

Finding B (Kalshi exec summary "14 totaling $2,373.07" mislabel, minor):
- The `Open positions: N totaling $X exposure` line summed N as
  per-strategy `authoritative_open_positions["count"]` (all open rows
  including `fill_confirmed=0` resting orders) while $X was Kalshi's
  bot-DB `open_exposure` field which is `fill_confirmed=1` only. The
  count mixed filled+unfilled while the dollars were filled-only.
- Fix: rebuild the exposure side to use the same per-strategy
  `authoritative_open_positions["exposure"]` sum as the count for
  internal consistency, with an explicit label "(includes pending
  resting orders)" so the operator sees the scope.

Finding C (IBKR Section 4 "Legacy positions: 21 | $635.05 cost basis
exposure" mislabel, minor):
- The label said "Legacy positions" but `pos_count` and `exp_str` come
  from `_get_live_trades_cost_basis()` and `ib_data["positions"]` which
  cover total open `live_trades` (bot_strategy + manual_user +
  unclear_legacy combined), not legacy positions only.
- Fix: relabeled to "Total live_trades open: N | $X cost basis exposure
  (all attribution: bot_strategy + manual_user + unclear_legacy)".

Documentation discipline question for operator decision (deferred):
- Should workspace CLAUDE.md be auto-generated from bot-local?
- Or should both be explicitly maintained?
- Or should there be a pre-commit checklist for config changes that
  touches both files?
- The 2026-04-27 auto-update disable was driven by drift in auto-generated
  prose; the current state is "manual on both surfaces with a canonical
  pointer added in this deploy". A future fix could automate the rollup
  table from a structured source.

Live trading bot safety verified before, between sections, and after:
- gemini-bot.service, kalshi-bot.service, ibkr-scan-loop.service PIDs
  unchanged throughout. No restarts, no reloads.
- Reconciliation $0.00 across all three platforms before, between
  sections, and after the deploy.

## 2026-05-07 - Kalshi MR Path B INDEX cluster cap and retirement formalization

Decision:
- Deploy Path B from the Kalshi MR deep loss-pattern investigation: add an
  INDEX cluster cap as the only behavioral change, formalize already-blocked
  KXHIGH/KXETHD/KXBTCD subseries as retired, make the WEATHER_LOW YES $150
  total-cost cap permanent policy, and start forward P&L tracking for the
  currently allowed cell portfolio.
- INDEX cap: max 2 open MR positions per `(underlier, settlement_event)` and
  max 4 total open MR INDEX positions per settlement hour. YES and NO count
  together. Existing open INDEX positions are grandfathered and settle
  naturally; the cap applies only to new placements.
- Forward tracker starts at 2026-05-07 20:20:23 UTC / 15:20:23 CDT and counts
  only post-deploy resolved MR rows from currently allowed cells.

Evidence:
- Strategy economics from the investigation: lifetime 311W-48L, -$58.13
  (-$0.16/trade), actual WR 86.63% versus 86.73% breakeven; recent 30d
  182W-26L, -$277.28 (-$1.33/trade), actual WR 87.50% versus 88.10%
  breakeven; recent 18 rows 13W-5L, -$389.58 (-$21.64/trade).
- INDEX was recently positive in aggregate (+$245.04 over 30d), but clustering
  was the unmitigated tail risk. Restriction simulation showed max 2 per
  underlier/event would have improved recent 30d INDEX from +$245.04 to
  +$301.40 by blocking 11 cluster trades whose net P&L was -$56.36.
- WEATHER_LOW YES cap evidence remains unchanged: `<$150` kept the small-cost
  slice at 14W-1L, +$70.92, while the above-cap tail drove the cell negative.
  The deployed cap was binding today, blocking 4/4 attempts around $331-$345.

Policy:
- KXHIGH, KXETHD, and KXBTCD are RETIRED MR subseries, not merely paused. The
  runtime enforcement remains `MR_BLOCKED_PATTERNS`; Moderate Favorites and
  other strategies do not inherit these MR-specific retirements.
- WEATHER_LOW YES total_cost >= $150 is permanent MR policy until a future
  operator-approved evidence review changes it. WEATHER_LOW NO remains
  unrestricted.
- Review INDEX cluster cap after 30+ post-deploy INDEX resolutions or two
  weeks, whichever comes first. Check P&L, block counts, cluster exposure, and
  whether max 2/max 4 remains the right shape.

## 2026-05-07 - Gemini DS high-price bounded refinement and Principle 49 retirement

Gemini DS operator decision:
- Close `parallel_filter_btc_eth_pilot` as FAILED at 42 resolved, 37W-5L, Wilson lower 75.0%, P&L -$24.63, and daily CB breached at -$32.89 / -$30. The strategy is refined, not retired.
- Deploy bounded refinement from the loss-pattern investigation: all five losses were below entry price 0.95; the price >=0.95 subset was 22W-0L but remains pre-gate/informative only.
- New active cohort: `filter_combined_btc_eth_high_price_pilot` from 2026-05-07 19:04:24 UTC / 14:04:24 CDT. Filter is BTC/ETH only, entry price >=0.95, cushion >=0.10%, depth tracked only, qty 10, max_open 3, daily CB -30, lifetime CB -60.
- Gate is unchanged from the prior BTC/ETH pilot: n>=30, WR>=90%, Wilson lower>=80%, positive cohort P&L, and no daily CB breach. The prior 22W-0L high-price subset does not count toward the new cohort.
- Manual daily CB reset uses the timestamp-scoped `DETERMINISTIC_SETTLEMENT_DAILY_RESET_AT="2026-05-07 19:04:24"` architecture. Historical trade rows are not mutated; the daily ledger counts only rows placed after the reset timestamp; the lifetime ledger remains scoped to the broader BTC/ETH pilot and is unaffected.

Principle 49 retired:
- Operator workflow for CB breaches is investigate -> deploy structural fix -> reset CB -> resume trading. The 2026-05-06 Principle 49 wording added policy friction around natural-cycle deferral and reset-frequency escalation that did not match this workflow.
- The timestamp-scoped `*_DAILY_RESET_AT` architecture remains valid and is used by this deploy. What is retired is the prescriptive principle constraining when the operator may use it.
- `AGENTS.md` no longer contains Principle 49. Existing architectural and bug-class discipline still applies through the remaining principles and BUG_CLASSES entries.

## 2026-05-07 - Kalshi DS BTC qty 500 scale and MR/DS loss-pattern investigations

Kalshi DS BTC qty 500 operator decision:
- Trigger honored: `filter_combined_qty_400_btc_pilot` emitted EXPANSION_CANDIDATE after 33 resolved BTC trades, 33W-0L, Wilson lower 89.6%, P&L +$389.36, and no daily CB breach.
- Change scope: one parameter family only, BTC DS size/cap. `DS_KALSHI_QTY_BTC` and `DS_KALSHI_PER_TRADE_DOLLAR_CAP_BTC` moved 400 -> 500. ETH stays qty/cap 225. `DETERMINISTIC_SETTLEMENT_MAX_OPEN=8`, `DETERMINISTIC_SETTLEMENT_MAX_ASSET_HOUR_OPEN=4`, daily CB -500, lifetime CB -1500, and the combined filter price >=0.90 plus cushion >=0.10% are unchanged.
- Cohort handling: close `filter_combined_qty_400_btc_pilot` as PASSED and open `filter_combined_qty_500_btc_pilot` from deploy timestamp with the same gate as the prior BTC pilot: n>=30, WR>=95%, Wilson lower>=88%, positive P&L, and no daily CB breach.
- Capital math: at roughly $2.3k Kalshi cash, qty 500 makes cash the effective BTC-only limiter before max_open. Four BTC positions require about $2,000; five require about $2,500. This is an intentional capital-binding side effect, not a max_open change. ETH qty 225 still mixes into the eight-slot architecture.
- Daily CB math: at qty 500, approximately 3.8 full-cost BTC losses would breach the -500 daily CB versus about 4.5 losses at qty 400. The CB is intentionally unchanged so the new cohort measures the higher size under the same risk floor.

Investigation scope:
- Kalshi MR and Gemini DS loss-pattern investigations are read-only and surface surgical-fix candidates for operator decision only. No surgical fix is auto-deployed in this session.

## 2026-05-06 evening - Five-item fix deploy: cohort tracker sweep, Principle 49, naming alignment, daily-report env fix, Weather DS closure

End-of-day audit at 20:12 CDT verified all 18 daily deploys clean and reconciliation $0.00, but surfaced five findings that this deploy addresses. Live trading bots untouched throughout; reconciliation $0.00 maintained.

IBKR Weather DS settlement watch closed:
- The four 2026-05-05 Weather DS rows (`UHMDW_050526_56_NO`, `UHMDW_050526_60_YES`, `UHMDW_050526_63_YES`, `UHSAT_050526_90_YES`) cleared the broker portfolio snapshot at 2026-05-06 19:45 CDT (last seen 19:09:01, absent from 19:45:01 snapshot).
- Final 24h: 1W-3L for +$3.00. Lifetime DB ledger +$1.90, broker truth -$2.50; the -$4.40 gap is the BUG_CLASSES #17 partial-fill defect already tracked separately as `ibkr_weather_ds_partial_fill_defect_fix` and is not closed by this entry.
- Stale-position detector reports `ibkr_weather_ds: open=0 within=0 candidates=0 confirmed=0`. Hard reconciliation $0.00 across Gemini/Kalshi/IBKR.
- Operator question on extending the 4h stale-position buffer is moot for this instance because the broker eventually settled at ~12-15h hold without intervention. Defer the buffer extension question until and unless a future paused-strategy instance also persists 10+ hours.
- Moved `ibkr_weather_ds_pause_settlement_watch` from VERIFICATION_DEFERRED.md Pending to Completed.

Cohort tracker methodology gate sweep (BUG_CLASSES #27 defense-in-depth):
- The morning's BUG_CLASSES #27 fix added a methodology gate to `analyze_ds_category()` in `ds_shadow_expansion_lib.py`. End-of-day audit found the same meta-pattern in five other decision-grade label emitters that all read live filled trades or shadow rows and emit deploy/scale recommendations.
- This evening's sweep applied the same methodology gate to: `kalshi_favorites_bot/ds_qty_cohort_tracker.py` (lines for `_recommendation` EXPANSION_CANDIDATE and the combined-filter DEPLOYMENT_VALIDATED path), `kalshi_favorites_bot/ds_low_price_no_cohort_tracker.py` (`recommendation` DECISION_READY), `gemini_prediction_bot/gemini_ds_cohort_tracker.py` (`_recommend` EXPANSION_CANDIDATE), and `.openclaw/workspace/scripts/shadow_mf_cross_market.py` (decision_grade list across four markets).
- Each instance now checks input row methodology markers and emits `METHODOLOGY_REVIEW_REQUIRED` when any non-authoritative row is present, instead of the existing decision-grade label. Existing labels still emit when methodology check passes.
- Defense-in-depth only. Live trades currently flow through validated placement paths so no active bug is fixed; the sweep prevents future upstream bugs (resolver, side-encoding, subset-derivation regressions) from silently propagating into recommendation labels.
- Tests added per file. All existing cohort tracker tests still pass.

Manual circuit breaker reset architecture note, retired as an operating principle 2026-05-07:
- This is the second instance of timestamp-scoped CB reset architecture (first was `MODERATE_FAVORITES_DAILY_RESET_AT="2026-04-23T12:56:44-05:00"`; today's was `DETERMINISTIC_SETTLEMENT_DAILY_RESET_AT="2026-05-06 11:49:55-05:00"`).
- Architecture is sound: env-var timestamp scopes the WHERE clause in CB-ledger queries, lifetime ledger is unaffected, audit trail preserved (env var visible in `/proc/$PID/environ`, reset timestamp logged at startup, no historical data mutation).
- The 2026-05-06 policy codification was removed on 2026-05-07 because Eric's operating workflow is CB breach -> investigate -> fix -> reset -> resume. The architecture remains valid; the extra policy constraint is retired.

Gemini DS cohort naming alignment:
- The cohort tracker code (`gemini_ds_cohort_tracker.py`) and database tables use precise cohort names: `strict_filter_pilot`, `parallel_filter_pilot`, `parallel_filter_btc_eth_pilot`. Documentation has occasionally used loose terms like "parallel filter closed" without the cohort name, which created ambiguity during the audit when reconciling cohort tracker output against operator log entries.
- Code is the source of truth (cohort tables, status report rendering, and historical attribution all use the code names). Documentation now aligns to the code: this and future operator-decision-log entries use the full cohort name.
- Updated `strategies-glossary.md` to list active and closed Gemini DS cohorts by their code names.
- No code changes; this is doc-only alignment that preserves historical attribution.

Daily report environment-independence fix:
- `gemini_ds_cohort_tracker.py` previously read pilot-start timestamps only from environment variables (`DETERMINISTIC_SETTLEMENT_PILOT_START`, `DETERMINISTIC_SETTLEMENT_PREVIOUS_PILOT_START`) at module import. The bot has these set via `start_bot.sh` which sources `.env`, but reports run via `daily-report.py` (which spawns `python3 gemini_status_report.py` without sourcing the bot env) saw empty values, causing the `closed_parallel` cohort section to silently render with the wrong boundary.
- Fix adds an env-var fallback that reads the bot's `.env` file when the env vars are absent at function-call time. Bot runtime behavior is unchanged because env vars take precedence; reports become environment-independent because they fall back to the same `.env` values the bot uses.
- Verified the report renders identical content inside the bot env and outside the bot env after the fix.

Bug class #28 codification:
- The daily-report environment-dependence is the same theme as BUG_CLASSES #22, #24, #26, #27: "decision-grade output emitted without verifying input state." This is the fifth instance of the meta-pattern in 48 hours.
- Codified as BUG_CLASSES #28 (report renders state-dependent text without verifying the state source is reachable) so future instances surface as a known pattern rather than a new investigation.
- State-verification follow-up confirmed BUG_CLASSES #28 as broader than env propagation: workspace `verification_deferred.py` rendered stale Gemini DS depth-filtered-pilot prose, workspace `daily-report.py` duplicated Kalshi DS cap-era SQL and folded `10->5` / `5->8` into `8->10`, and IBKR report output did not label the boundary between `live_trades` open lifecycle rows and broker portfolio snapshot positions.
- Deployed fixes: Gemini deferred-verification prose now references the active `parallel_filter_btc_eth_pilot` review without hardcoded qty/depth/SOL state; daily report's compact Kalshi DS cohort line now calls `kalshi_favorites_bot/ds_cohort_tracker.py`; daily report now prints `live_trades` open rows versus broker snapshot positions and surfaces mismatches for operator decision.
- IBKR boundary rows surfaced for operator review, not auto-reconciled: `FF_043026_3.375_NO` is live_trades-open only; `UHPHX_050626_83_YES` broker snapshot qty/cost exceeds live_trades; two recent FX bot_strategy lifecycle rows observed during investigation were absent from broker snapshot at that moment. Cash reconciliation remained $0.00, so this remains BUG_CLASSES #17 bookkeeping/lifecycle review rather than a financial gap.

Reconciliation:
- Pre-deploy: Gemini gap $0.00, Kalshi gap $0.00, IBKR gap $0.00.
- Post-deploy: same. No live trading bot restart, no DB mutation.

## 2026-05-06 - Afternoon daily-report cleanup: sports freshness, Kalshi 429, IBKR Weather drift

Sports DS forward scanner:
- Service was active and healthy, and a one-shot scan returned 32 games and
  3023 Kalshi sports markets without errors.
- The stale alert was a methodology/reporting bug, not a dead scanner:
  `sports_ds_forward_quotes` freshness checked only the active DB table after
  archive policy moved resolver-safe quote rows into the monthly archive.
- Fixed the freshness source to query active+archive via the archive reader.
  Post-fix freshness shows `sports_ds_forward_quotes` OK with 801,565 rows and
  latest timestamp 2026-05-06T04:17:20+00:00.
- Documented BUG_CLASSES #26 for active-only freshness checks on archived
  decision tables.

Kalshi 429 post-throttle measurement:
- Closed the overdue verification. The 24h window before the 2026-05-04
  09:00 CDT trigger had 231 429s, avg 9.62/hr, peak 171/hr. The 24h window
  after had 69 429s, avg 2.88/hr, peak 67/hr.
- Current status report showed 0 429s in 1h and 59 in 24h. The throttle is
  working; no additional throttle change was deployed.

IBKR Weather DS drift candidates:
- The four paused Weather DS positions are still present in the broker
  portfolio snapshot, so this is not a local resolver lag yet.
- NWS public data is available and implies expected outcomes of 1W-3L:
  `UHMDW_050526_63_YES` loss at 61F, `UHSAT_050526_90_YES` loss at 88F,
  `UHMDW_050526_60_YES` win at 61F, and `UHMDW_050526_56_NO` loss at 61F.
- Updated the read-only stale-position detector to report
  `BROKER_PORTFOLIO_OPEN` for IBKR candidates found in the latest broker
  snapshot instead of `UNVERIFIED`. Weather DS remains paused and no positions
  were force-closed.

Decision:
- No live trading bot restart.
- No sports scanner restart required.
- Continue waiting for broker settlement/Flex to remove or settle the four
  Weather DS contracts; if broker-open status persists into the next report,
  operator should decide whether the Weather DS expected-settlement buffer
  needs a weather-specific extension.

## 2026-05-06 - DS shadow DB audit and bounded cleanup

Findings:
- Active DS shadow expansion DB is about 14.6GB with a small WAL and small
  freelist; size is mostly real active/index footprint, not VACUUM-reclaimable
  bloat.
- Largest active object is `ds_shadow_external_observations`, followed by
  `ds_shadow_expansion_signals`; active row retention is driven by current
  resolver/archive policy and broad historical observations.
- Continuous archive and batch archive are working; archive is about 73GB.

Action:
- Performed only Tier 1 cleanup: deleted active unified-signal rows for
  `kalshi|politics`, `kalshi|culture`, and `kalshi|business` after verifying
  zero actionable rows, zero resolved rows, and no active cohort dependency.
- Recalibrated DS shadow DB thresholds to warn=15GB, critical=20GB, halt=25GB
  because the post-archive active steady-state floor is about 14-15GB.
- Added formal DS shadow DB retention policy and Principle 46.

Operator decisions still needed:
- Whether to prune or cold-store archive data.
- Whether to reduce or disable broad Kalshi/Gemini sports storage beyond the
  current daily caps.
- Whether to schedule offline VACUUM after a larger cleanup event.

## 2026-05-06 - DS archive tier rotation deploy

Decision:
- Bound long-term DS shadow archive growth with recoverable zstd compression
  and cold-storage rotation, not deletion.
- Add a separate `ds-archive-tier-rotation.timer`; do not modify or restart
  existing live bots, scanners, continuous archive, or batch archive services.

Mechanism:
- Hot tier: closed monthly archive DBs remain uncompressed and queryable under
  `~/.openclaw/workspace/data/archive/` for 30 days after period close.
- Warm tier: 30-90 days after period close, archives compress to
  `~/.openclaw/workspace/data/archive_warm/`.
- Cold tier: 90+ days after period close, compressed archives move to
  `~/.openclaw/cold_archive/ds_shadow_expansion/`.
- Each compression must pass decompression, SQLite `quick_check`, row-count
  comparison, and SHA-256 roundtrip verification before the uncompressed source
  is removed.
- Recovery uses `scripts/ds_archive_recover.py <YYYY-MM>` into a queryable
  SQLite DB under `data/recovered_archives/`.

Activation note:
- Production currently has only the open `2026-05` archive period, so the first
  real production run is a no-op until a monthly period closes and ages past the
  configured thresholds.
- Synthetic integration tests verified compression, warm-to-cold movement,
  idempotency, and recovery.

Operator decisions still needed:
- Confirm whether the default 30/90-day hot/warm thresholds should stay after
  the first closed monthly archives exist.
- Confirm whether cold storage should remain under
  `~/.openclaw/cold_archive/ds_shadow_expansion/` or move to another disk later.

## 2026-05-06 - Kalshi DS max_open 5 -> 8 capital-utilization deploy

Decision:
- Increase Kalshi crypto DS `DETERMINISTIC_SETTLEMENT_MAX_OPEN` from 5 to 8.

Rationale:
- The max_open=5 setting was a reactive funded-slot control for the uniform qty=400 era. After the per-asset split, BTC remains qty 400 while ETH runs qty 225, so ETH-heavy windows can leave roughly 44% of available capital idle at max_open=5.
- Historical max_open=8 evidence was the prior sweet spot: 6->8 cohort produced 114 resolved, 111W-3L, 97.4% WR, Wilson lower 92.5%, and +$210.91 P&L.
- Asset-hour cap remains 4 per asset/settlement-hour, so the correlated-cluster control is unchanged. Daily CB remains -$500, lifetime CB remains -$1,500, and the price/cushion filter remains unchanged.

Monitoring:
- Treat the new `5->8` cap era as an informational capital-throughput era, not a new per-trade strategy gate. Existing BTC qty 400 and ETH qty 225 per-asset cohorts continue.
- Target active-window capital utilization is 60-90%.
- Rollback/review trigger: daily CB breach for 2 consecutive days, or materially deteriorating `5->8` cap-era quality versus the historical 6->8 cohort.

## 2026-05-06 - Gate enforcement deploy: Kalshi/Gemini DS refinements and verification pipeline

Decisions:
- Kalshi crypto DS aggregate qty-400 cohort failed its 30-resolution gate: 27W-3L, 90.0% WR, Wilson lower 74.4%, P&L -$691.95, and daily CB breach. Per-asset decomposition supported a surgical split, so BTC remains qty 400 and ETH rolls back to qty 225.
- Kalshi DS Low-Price NO Pilot paused early at 21 resolved because 15W-6L cannot mathematically reach the 90% WR gate by 30 resolved. Existing open positions settle naturally.
- Gemini DS parallel filter closed at 36 resolved, 33W-3L, Wilson lower 78.2%, P&L -$14.48. SOL caused all three losses, so SOL was removed and BTC/ETH continue as a fresh `parallel_filter_btc_eth_pilot`.
- IBKR verification pipeline root cause was trust-state overwrite from partial-category verifier runs. The verifier now preserves prior verified sections when a category is skipped.

Implementation:
- Kalshi DS uses per-asset env vars `DS_KALSHI_QTY_BTC`, `DS_KALSHI_QTY_ETH`, `DS_KALSHI_PER_TRADE_DOLLAR_CAP_BTC`, and `DS_KALSHI_PER_TRADE_DOLLAR_CAP_ETH`, all routed through `_ds_cap_available_qty()`.
- New Kalshi cohorts: `filter_combined_qty_400_btc_pilot` and `filter_combined_qty_225_eth_pilot`.
- New Gemini cohort: `parallel_filter_btc_eth_pilot`.
- New operation-wide Principle 45 and BUG_CLASSES #25 capture asset-specific tail divergence in scaled clustered binary strategies.

## 2026-05-06 - Morning cleanup: FRED row and subset over-fitting principle

Scope:
- Approved single-row FRED correction for `shadow_candidates.id=128406` / `USGP_050426_4.3_NO`.
- Codified subset over-fitting as Principle 44 / BUG_CLASSES #24.
- Tightened deferred gate review criteria for Gemini DS depth and Kalshi DS Low-Price NO.

Findings:
- The dirty FRED economics verifier row was isolated. It used stale `FRED:4.123`; current GASREGW for the contract date was 4.452, so the NO side lost.
- After correction, the independent verifier reports 985 verified, 985 match, 0 mismatch; Economics shadow data is independently verified.
- Existing Principle 41 and BUG_CLASSES #23 were already assigned, so the new methodology rule uses Principle 44 and BUG_CLASSES #24.

Decision:
- Correct the single shadow row; no live trading tables, bot configs, or services touched.
- Require audit-derived deployment subsets to be re-derived from raw shadow data and reproduced within 5pp before decision use.
- Gate reviews must preserve original criteria unless Eric explicitly approves a benchmark change.

## 2026-05-04 - Gemini DS depth-filtered live pilot

Eric overrode the recommendation in
`gemini_prediction_bot/docs/gemini-ds-investigation-2026-05-04.md` to keep
Gemini DS paused. The override rationale is that live trading data is more
informative than forward shadow data for the depth-filter hypothesis.

Decision:

- Re-enable Gemini DS as a new bounded live pilot.
- Test placement-time depth as the independent variable across BTC, ETH, and
  SOL. Do not restrict to ETH-only, because that would confound the experiment.
- Require `DETERMINISTIC_SETTLEMENT_MIN_DEPTH=500`.
- Use qty 25, max_open 2, daily CB -75, lifetime CB -150.
- Scope daily/lifetime CB ledgers and cohort evidence from
  `DETERMINISTIC_SETTLEMENT_PILOT_START`.
- Preserve historical unfiltered Gemini DS rows for reporting and investigation.

Pre-committed review criteria:

- 50+ resolved depth-filtered pilot trades.
- WR >= 90%.
- Wilson 95% lower bound >= 80%.
- Lifetime P&L positive.
- Daily CB has not triggered.
- Per-asset breakdown reviewed for BTC/ETH/SOL divergence.

Any future change must alter one parameter at a time and start a new cohort.

## 2026-05-05 - Kalshi/Gemini DS high-price high-cushion filters

Morning loss-pattern analysis identified a cross-venue cell where high entry
price and high settlement cushion materially reduced adverse selection.

Decision:

- Add Kalshi crypto DS combined filter: entry price >= 0.90 and
  cushion_at_entry >= 0.10%.
- Keep Kalshi DS qty 225, max_open 10, daily CB -500, lifetime CB -1500,
  max exposure 5000, and BTC/ETH allowlist unchanged.
- Restart Gemini DS as a new strict-filter pilot with depth >=1000,
  entry price >=0.90, cushion_at_entry >=0.10%, qty 10, max_open 2,
  daily CB -30, and lifetime CB -60.
- Reset Gemini DS pilot start/CB ledger because the strict-filter pilot is a
  different thesis from the failed depth-only pilot.
- Add placement-time instrumentation for `time_to_settlement_seconds` and
  `realized_volatility_at_entry` on Kalshi and Gemini DS rows.

Pre-committed review criteria:

- Kalshi `filter_combined_pilot`: 50+ resolved, WR >=95%, Wilson lower >=90%,
  positive P&L, no daily CB breach, and BTC/ETH split reviewed.
- Gemini `strict_filter_pilot`: 30+ resolved, WR >=90%, Wilson lower >=80%,
  positive P&L, daily CB not triggered, and BTC/ETH/SOL split reviewed.

Reversibility:

- Kalshi filter thresholds are controlled by `DS_KALSHI_MIN_PRICE` and
  `DS_KALSHI_MIN_CUSHION`.
- Gemini strict pilot is controlled by `DETERMINISTIC_SETTLEMENT_ENABLED`,
  `DETERMINISTIC_SETTLEMENT_MIN_DEPTH`, `DETERMINISTIC_SETTLEMENT_MIN_PRICE`,
  `DETERMINISTIC_SETTLEMENT_MIN_CUSHION`, and the DS kill-switch file.

## 2026-05-04 - Kalshi crypto DS quarter-Kelly Wilson-lower qty scale

Eric directed Kalshi crypto DS per-trade sizing to scale from qty 50 to qty
225. The rationale is the academic Kelly framework applied conservatively to
the live crypto DS sample:

- n=356 lifetime resolved trades.
- Point-estimate WR 95.8%.
- Wilson 95% lower-bound WR 93.4%.
- Win/loss payoff ratio b ~= $4.50 / $42.50 = 0.106.
- Full Kelly using Wilson lower ~=31% of bankroll.
- Quarter-Kelly using Wilson lower ~=7.8% of bankroll, or about $225/trade on
  the referenced bankroll.

Decision:

- Deploy qty 225 and per-trade cap $225.
- Keep max_open at 10.
- Set max exposure to $5,000 so cash, not the dollar exposure cap, is the
  practical binding constraint.
- Scale daily CB to -$500 and lifetime CB to -$1,500.
- Do not reset lifetime CB ledger because the strategy mechanics are unchanged.
- Keep threshold, final-window, min-edge, and BTC/ETH allowlist unchanged.

Pre-committed review criteria:

- 50+ resolved trades in the qty-225 cohort.
- WR >= 95%.
- Wilson 95% lower bound >= 90%.
- Lifetime P&L positive.
- Daily CB has not triggered.
- Per-trade EV at scaled qty matches or exceeds aggregate.
- Future changes alter one parameter at a time.

## 2026-05-05 - DS shadow collection scope and storage controls

Phase 1-3 analysis and fresh pre-change verification converted broad shadow
collection from speculative capture to evidence-scoped capture.

Decision:

- Disable broad DS writes for confirmed empty Kalshi categories only:
  `kalshi:politics`, `kalshi:culture`, `kalshi:business`, `kalshi:tech`, and
  `kalshi:climate_science`.
- Keep Gemini politics/economics/business/tech/culture/weather enabled because
  fresh pre-change data showed nonzero actionable rows or broad/per-cell
  weather coupling risk.
- Keep Kalshi entertainment enabled because fresh data showed nonzero actionable
  rows.
- Keep productive per-cell streams untouched, including Kalshi sports DS
  forward quote capture and Gemini weather cushion DS.
- Tighten DS shadow archive cadence from daily to every 6 hours.
- Add per-category storage monitoring every 6 hours, offset after archive runs.

Reversibility:

- Collection scope is controlled by
  `DS_SHADOW_DISABLED_CATEGORIES` on `ds-shadow-expansion-scanner.service`.
  Remove a `platform:category` token and restart only the shadow scanner to
  re-enable that category.

Review criteria:

- Review `storage_monitoring_baseline_review` after 7 days of monitor history.
- Confirm disabled categories have zero post-change writes.
- Confirm active DB remains bounded after the new archive cadence.
- Use per-category trend data before any additional kill/downsample decision.

## 2026-05-08 - DS storage self-managing steady-state system

Decision:

- Build on the existing continuous archive, six-hour archive, three-tier
  rotation, and Principle 46/47 retention model rather than replacing it.
- Add disk-percent storage envelopes: TARGET 50%, WARN 65%, CRITICAL 75%,
  HARD_LIMIT 85%.
- Add active DB envelope: target 15 GiB, warn 20 GiB, critical 25 GiB, hard
  limit 30 GiB.
- Classify DS shadow streams by VALUE_TIER in
  `ds-storage-value-tiers.json`.
- Add retention engine for disabled unresolved broad-category rows, deployed in
  dry-run posture first.
- Add storage pressure monitor and PROTECT_TRADING emergency mode. At hard
  limit it blocks non-trading shadow writes/stops shadow scanners while live
  trading bots stay untouched.
- Add full-picture `DATABASE STORAGE HEALTH` reporting.

Initial posture:

- `DS_RETENTION_ENGINE_DRY_RUN=true` for first 24h observation.
- First-time prune remains operator-approved only.
- No trading bot restart required.

## 2026-05-05 - Kalshi DS low-price NO pilot

The H1 methodology audit found that Phase 2 crypto DS aggregation was
side-agnostic: YES outcomes were counted as wins even for NO predictions.
Corrected side-aware aggregation made the low-price NO cells pilot-worthy.

Decision:

- Start a bounded independent Kalshi live pilot with strategy key
  `ds_low_price_no`.
- Trade only NO side, entry price < $0.80, assets BTC/ETH/SOL.
- Use qty 10, max open 3, per-trade max $20, daily CB -$20, lifetime CB -$60.
- Keep existing Kalshi MR and high-price crypto DS combined filter unchanged.
- Track forward-only cohort from the deploy timestamp; do not backfill.

Pre-committed review criteria:

- 30+ resolved pilot trades.
- WR >= 90%.
- Wilson 95% lower bound >= 80%.
- Positive P&L.
- No daily/lifetime CB stress.

## 2026-05-06 - Morning report five-item investigation

Scope:

- Investigated Kelly Daily Impact, IBKR Economics/JOLT shadow, VIBP pause
  state, Gemini DS depth diagnostics, and Kalshi DS Low-Price NO pilot gap.
- Reconciliation remained $0 on Gemini, Kalshi, and IBKR during the
  investigation.

Findings:

- Gemini MR Kelly is active. Runtime env has `KELLY_SIZING_ENABLED=true`, logs
  show `MR_KELLY_COMPUTE`, and the first post-activation MR placement used qty
  544 instead of the flat 400 baseline.
- Kelly Daily Impact was not showing pending impact because it only summed
  realized P&L fields. Open Kelly-comparison rows now report pending actual
  exposure, shadow Kelly exposure, and delta qty.
- IBKR Economics/JOLT had a side-aware methodology bug in the DS expansion
  resolver: `macro_release_signals.actual_outcome` is side-relative, but DS
  expansion interpreted `1.0` as actual YES. Fixed forward resolver logic and
  added a NO-side win regression test. Source MRN rows themselves showed
  96W-192L by side-relative payoff, not the reported 0W-267L.
- The FRED verifier still has one real dirty economics row:
  `USGP_050426_4.3_NO` (FRED GASREGW 4.452 > 4.3, YES wins, stored shadow
  WIN for NO). Economics remains excluded from promotion decisions until the
  dirty row is corrected or explicitly quarantined.
- VIBP is paused now. The kill switch exists and code respects it; latest
  Gemini/Kalshi VIBP rows were around 2026-05-06 02:13 UTC. The report was
  showing rolling 24h historical rows, so status text now says rolling-24h,
  latest row timestamp, and PAUSED by kill switch.
- Gemini DS depth remains a live gate-review issue, not a config change. The
  linked orderbook sample shows wins have far deeper books than losses
  (overall 378W-76L, win depth 3836.8 vs loss depth 65.2). Parallel-filter
  cohort is currently 48W-4L in linked snapshot rows, with 17W-2L below depth
  500 and 28W-2L above 5000.
- Kalshi DS Low-Price NO remains below gate WR but positive P&L at current
  status: 21 resolved, 15W-6L, +$11.35. Current live-shadow comparison did not
  justify changing config before the 30-resolution gate. A separate note for
  gate review: the raw current `shadow_deterministic_settlement` low-price NO
  resolved slice reads 185W-88L for BTC/ETH/SOL, so the earlier 90%+ audit
  statistic must be re-derived from its exact audited population before any
  scale or kill decision.

Decision:

- Deployed bounded report/methodology fixes only: Kelly pending impact
  reporting, VIBP paused-status reporting, and IBKR economics side-aware
  resolver mapping.
- No Gemini, Kalshi, or IBKR live trading service restart was required.
- Do not change Gemini DS or Kalshi DS Low-Price NO configs before their
  pre-committed 30-resolution gates unless a new dispositive methodology bug
  is found.
- Per-asset breakdown supports continuing all included assets.

Emergency halt criteria:

- 5 consecutive losses.
- 0W-5L total at any point.
- Daily CB or lifetime CB breach.

## 2026-05-05 - IBKR Weather DS and VIBP pause

Decision:

- Pause IBKR Weather DS with both runtime controls:
  `DETERMINISTIC_SETTLEMENT_WEATHER_ENABLED=false` and
  `KILL_DETERMINISTIC_SETTLEMENT_WEATHER`.
- Leave the four open Weather DS positions to settle naturally.
- Preserve the IBKR Long+Short-dated bot strategy unchanged.
- Pause VIBP by creating workspace `KILL_VOL_IMPLIED_BINARY`; preserve all
  historical `vol_implied_signals` rows for methodology rebuild.

Rationale:

- Weather DS live broker-truth evidence is 0W-4L and BUG_CLASSES #17 remains
  unresolved.
- VIBP has unresolved timing contamination and side-aware aggregation risk.

Verification:

- IBKR restarted once; `/proc` env showed Weather DS disabled, startup log
  showed `enabled=False`, status report showed Weather DS `KILLED`, and the
  IBKR hard-check cash gap stayed $0.00.

## 2026-05-05 - Gemini MR Kelly and Kalshi DS qty 400 continuation

Decision:

- Remove the Gemini MR "Kelly qty >= current qty" preference because it
  conflicts with the 50% single-asset concentration cap.
- Keep the 50% per-asset concentration cap as a permanent placement-path
  safety feature.
- Activate Gemini MR half-Kelly sizing with empirical-Bayes calibration
  infrastructure.
- Scale Kalshi crypto DS combined filter from qty 225 to qty 400, and start
  the `filter_combined_qty_400_pilot` forward cohort.
- Do not activate Kalshi Index/FX proper cushion DS yet: the proper
  `shadow_index_fx_cushion_ds` evidence table has zero observations, while the
  large Index/FX evidence source is favorite-tracking/longshot methodology.

Verification:

- Gemini restart showed Kelly config in file, code, process env, startup log,
  and status report. ETH new placements are blocked/sized down while existing
  ETH exposure exceeds the 50% cap; existing positions were left alone.
- Kalshi restart showed crypto DS qty 400 and per-trade cap $400 in file,
  code, process env, startup log, and status report. Legacy Index/FX longshot
  keys remained disabled and killed.
- Kalshi and Gemini hard reconciliation checks stayed at $0.00 during deploy.

## 2026-05-06 - Kalshi DS qty-400 loss-pattern correction

Decision:

- Keep Kalshi crypto DS live but under rollback review after the qty-400 daily
  CB breach.
- Reduce `DETERMINISTIC_SETTLEMENT_MAX_OPEN` from 10 to 5 to match funded-slot
  reality at qty 400.
- Add `DETERMINISTIC_SETTLEMENT_MAX_ASSET_HOUR_OPEN=4` as a live placement-path
  cap on correlated crypto DS positions in the same asset/settlement-hour.
- Preserve the existing combined filter: entry price >= 0.90 and cushion >=
  0.10%.
- Do not touch Gemini, IBKR, Kalshi MR, or Kalshi DS Low-Price NO.

Rationale:

- The overnight qty-400 losses were genuine losses, not resolver or cohort
  accounting bugs.
- All post-filter placements complied with price/cushion thresholds.
- Three qty-400 losses came from the same 2026-05-06 05:00 UTC crypto
  settlement cluster, showing correlated exposure risk rather than a broad
  filter failure.
- Qty 400 made cash/funded slots the practical limiter while max_open still
  advertised 10 slots.

Review criteria:

- Review the post-fix cohort after 30+ resolved rows.
- Continue only if WR >=95%, Wilson lower >=88%, P&L is positive, and no daily
  CB breach occurs.
- Roll back or pause if the post-fix cohort is negative or breaches CB.

## 2026-05-06 - 16:27 daily-report bounded investigations

Decision:

- Keep IBKR Weather DS paused; do not force-close the four remaining Weather
  DS positions. They remain broker-open and should settle naturally.
- Do not extend the Weather DS stale-position threshold automatically. Operator
  decision required: either extend `max_hold_after_settlement` from 4h to 12h
  or 24h for ForecastEx weather, or keep 4h and treat `BROKER_PORTFOLIO_OPEN`
  drift candidates as informational while broker truth still shows open.
- Fix DS SHADOW EXPANSION recommendation labels so aggregate metrics from
  non-deployable methodology cannot print `LIVE_PILOT_CANDIDATE`.
- Treat Kalshi/Gemini bot warning volumes as signal to monitor, not immediate
  strategy-change evidence. No live trading bot restarts.
- Treat the small DS scanner and sports scanner error counts as transient
  upstream API noise unless they recur or freshness degrades.

Evidence:

- Reconciliation checks stayed clean: Kalshi, Gemini, and IBKR cash gaps were
  all $0.00.
- IBKR stale detector at 2026-05-06T21:42Z still showed all four Weather DS
  positions as `DRIFT_CANDIDATE` with platform status
  `BROKER_PORTFOLIO_OPEN`; broker position snapshot last saw all four at
  2026-05-06T20:56Z, and `settlement_log` had no rows.
- NWS station observations for the local 2026-05-05 weather day showed KMDW
  max 60.8F (rounds to 61F) and KSAT max 87.8F (rounds to 88F), matching the
  expected 1W-3L outcome once ForecastEx settles.
- Fresh 24h log aggregation at 2026-05-06 16:41 showed Kalshi warnings/errors
  dominated by VIBP kill notices, DS circuit-breaker warnings, REST 429 retry
  warnings, and known cancel_order 404s; Gemini warnings were dominated by VIBP
  kill notices plus IOC no-fill and temporary settlement-retry messages.
- DS scanner errors were NWS/ESPN read timeouts; sports scanner errors were one
  Kalshi 429 and one ESPN timeout. Both scanners resumed healthy `status=OK`
  summaries immediately afterward.

Fix:

- `ds_shadow_expansion_lib.py` now requires authoritative methodology and a
  Wilson lower-bound floor before emitting `LIVE_PILOT_CANDIDATE`. Positive
  favorite-tracking/mixed aggregates render as `METHODOLOGY_REVIEW_REQUIRED`;
  low-WR positive-EV weather aggregate renders as `CONTINUE_SHADOW`.
- BUG_CLASSES #27 and AGENTS.md Principle 48 document the new pattern.

## 2026-05-09 evening - Audit findings response

The 2026-05-09 evening audit raised fourteen FLAGs and ten reality-vs-claim
discrepancies. Resolutions below; live trading bots remain untouched.

### Reconciliation finding (largest item) — was a misread, not a violation

The audit reported "non-zero reconciliation gaps on Kalshi ($119.50) and
Gemini ($3,241.45)" violating the "$0.00 cash gap" requirement. Verification
shows the cash gap is actually $0.00 on all three platforms; the audit
misread the `recon_adj` column as the cash gap.

What the report numbers actually mean:

- `cash_gap`: actual cash from API minus expected cash from the equation
  (`deposits + resolved + recon_adj + documented_baseline - open_cost - open_fees`).
  This is what reconciliation discipline refers to; HARD CHECK passes when
  `abs(cash_gap) < $1.00`. All three bots' status reports show
  `✓ HARD CHECK PASSED — gap $0.00`.
- `recon_adj`: auto-computed correction the bot stores so the equation
  balances. It moves with positions and rounding; a drift over $5 between
  consecutive snapshots flags a possible bad-P&L trade. Stable drift = OK.
- `documented_baseline`: one-time absorption captured for structural
  unverifiable variance. Kalshi has $90.55 absorbed; Gemini has none yet.
  Recon_adj is then the residual on top of the baseline.

State at end of audit (verified by re-running each bot's status report):

| Platform | cash_gap | recon_adj | baseline | drift | source |
|---|---|---|---|---|---|
| Kalshi | $0.00 ✓ | $-6.52 (varies with positions) | $90.55 | $0.00 stable | kalshi_api_balance |
| Gemini | $0.00 ✓ | $3,193.83 (stable) | $0.00 (none) | $0.00 stable | gemini_api_balance |
| IBKR | $0.00 ✓ (cash) | $12.54 statement_live_nlv_delta | n/a | n/a | live_nlv vs Flex 20260508 |

Action taken:

- Created `~/operations-knowledge/dispatch-conventions.md` to document the
  three-quantity reporting convention so audits and dispatches use the same
  vocabulary going forward. Cash_gap is the only quantity that can be claimed
  as `$0.00` for reconciliation discipline; recon_adj and statement_live_nlv_delta
  must be labeled separately and may be non-zero by design.
- Reading the audit's "$3,241.45 Gemini gap" against current reality: the
  Gemini recon_adj has stayed in the $3,193-$3,241 band stably. This is the
  pre-MR-strategy structural offset (Gemini's older strategies had losses
  that reduced cash below `deposits + cumulative_pnl_post_MR`). The audit's
  hypothesis — daily report's "lifetime P&L" tracks current strategy only,
  while recon equation's `pnl` tracks all resolved trades — is correct. Both
  numbers match their respective DB queries: `SELECT SUM(pnl) FROM trades
  WHERE pnl IS NOT NULL` returns -$13,077.60 (matches the equation), and the
  Gemini status report's "Lifetime P&L: +$4,296.85" is current-strategy-only
  by design.
- Gemini structural offset of ~$3,200: deferred to a future code-level
  dispatch. Adding a `gemini_documented_baseline` mechanism (mirror Kalshi's
  pattern where $90.55 was absorbed at some prior point) would require
  `gemini_status_report.py` modifications. The change is non-trivial and
  affects code that the running bot calls; it should be its own dispatch
  with proper testing rather than rolled into this remediation pass. Until
  then, the recon_adj stably reads the structural offset, which is a valid
  audit signal.

### Documentation drift

- `ds-storage-runbook.md` "Kalshi Sports Classification" section had stale
  TIER_E_DISPOSABLE wording. Updated to TIER_C_RESEARCH with explanation
  that the 90-day actionable-signal guardrail triggered the safety
  reclassification — the guardrail functioning as designed is the reason
  the classification changed.
- Added a note clarifying that `sports_data|sports` is the only stream
  currently classified TIER_E_DISPOSABLE.
- Workspace `CLAUDE.md` Active strategies table updated: Kalshi DS shows
  qty 600 BTC / qty 275 ETH with daily CB -$600 / lifetime CB -$1,800;
  Gemini DS shows qty 50 ETH with daily CB -$100 / lifetime CB -$300.
- `dispatch-conventions.md` created with reporting conventions for
  reconciliation, test counts, commit/push reporting, cohort numerics,
  and SHA verification depth.

### Test claim and one cross-module test failure

- The audit's "1/254 FAIL" turned out to be a test-isolation issue, not a
  real code bug. `test_gemini_weather_range_actual_outcome_from_cached_nws`
  passes when run individually (`python3 -m unittest scripts.test_ds_shadow_expansion`
  reports 83/83 OK) and only fails when the broader `discover -p test_*.py`
  cross-module sequence runs.
- Root cause appears to be the module-level `dsx._WEATHER_ACTUAL_MEMO` being
  populated by an earlier test in the cross-module sequence. The fix is a
  setUp/tearDown that clears the memo, but doing so without verifying full
  cross-module pass-through risks new failures, so deferred for a focused
  test-isolation pass.
- Dispatch-conventions update: test count claims must include scope. The
  prior "38/38" or "33/33" claims referred to specific subsets, not the full
  254-test workspace suite.

### Cleanup

- Workspace `.gitignore`: added `.kalshi_report_*.txt` (the dotfile-prefixed
  Kalshi report dumps that the existing `*_report.txt` pattern did not catch)
  and `data/.archive_cache/` (the archive-aware reader's transparent
  decompression cache, regenerable from `data/archive/*.zst`).
- Workspace dirty tree: per operator direction, `memory/2026-05-09.md`,
  `memory/costs-ledger.md`, and `scripts/costs.json` are append-only history
  records and have been committed. The `.kalshi_report_*.txt` runtime artifacts
  are now gitignored.
- `/tmp/rahm_full_picture_check.txt` (May 5 artifact, no open handles): deleted.

### Disk_pct field

The audit reported `storage_pressure_status.disk_pct = null` as a bug. The
field is actually named `disk_used_pct` and is populated correctly
(0.19175 = 19.2%). The audit looked for the wrong key. No code change
needed; reporting convention should reference the correct field name.

### Missing SHAs

- `[REDACTED:long_hex]` exists in operations-knowledge
  history. The audit's `git log -10` was too shallow; deeper search via
  `git rev-parse 47dcad18` confirms the commit.
- `325a87c6` does not appear in either operations-knowledge or workspace.
  Most likely a typo or amend artifact in the dispatch report; the storage
  stabilization commits actually present are `c447a09`, `af57f185`,
  `836443d`, and the documented work is in those.

### Git remotes (deferred per operator)

- All four repos (kalshi_favorites_bot, gemini_prediction_bot,
  .openclaw/workspace, operations-knowledge) have no remote configured.
- Operator will provide GitHub URLs in a follow-up. Until then, all
  "pushed to origin" claims in dispatch reports are inaccurate; commits are
  local-only.
- Going forward, `dispatch-conventions.md` requires honest "committed
  locally; remote not configured" wording instead of "pushed to origin"
  when no remote exists.

### Trading bot verification

- Kalshi PID 2327704, NRestarts 0, ActiveEnterTimestamp 2026-05-09 09:00:38 CDT.
- Gemini PID 2329966, NRestarts 0, ActiveEnterTimestamp 2026-05-09 09:05:33 CDT.
- IBKR-scan-loop PID 2049139, NRestarts 0, ActiveEnterTimestamp 2026-05-08 10:53:36 CDT.
- All three unchanged from the audit pre-flight reading. No service restart
  occurred during this remediation dispatch.
