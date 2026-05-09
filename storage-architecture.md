# Storage Architecture

Last updated: 2026-05-09

Rahm storage is managed by four autonomous layers:

1. DS active lifecycle: `ds-shadow-retention-engine.timer` archives
   resolver-safe rows, prunes only explicit `TIER_E_DISPOSABLE` rows, and
   compresses sealed monthly archives.
2. Pressure control: `ds-storage-pressure-monitor.timer` tracks raw disk,
   active DB, archive envelope, growth alarms, and PROTECT_TRADING for
   non-trading shadow writes only.
3. Database maintenance: `database-autonomous-maintenance.timer` performs
   online backups, backup verification, integrity checks, safe WAL hygiene,
   classification drift detection, cache cleanup, and `/tmp` hygiene.
4. Log/cache hygiene: `logrotate-user.timer` bounds user-owned logs; cache
   cleanup is limited to explicit regenerable paths in
   `non-ds-cache-tiers.json`.

Trading databases are protected by a whitelist: read-only metrics, passive WAL
checkpoint, and SQLite Online Backup API. No autonomous phase vacuums, prunes,
or schema-rewrites trading DBs while bots are running.
