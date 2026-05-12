# Rahm Current State

last_updated_utc: 2026-05-12T11:10:03+00:00
generator: Codex generate_current_state.py
workspace_head: 503446d

## Trading Bot Runtime
### gemini
- unit: gemini-bot.service
- active: active/running
- pid: 3089149
- nrestarts: 0
- active_enter: Mon 2026-05-11 18:17:04 CDT
- reconciliation:
  - Reconciliation: resolved_pnl=$-10976.08 open_cost=$7072.57 open_fees=$89.81 recon_adj=$131.35 expected_cash=$274.39 cash_gap=$+0.00 unrealized=-$2,285.93 [MATCH]
  - ✓ HARD CHECK PASSED — gap $0.00
  - Reconciliation adjustment: $131.35 (auto-computed from exchange balance)
  - Expected cash: $274.39
  - Actual cash (API): $274.39
- selected env:
  - `BLOCKED_ASSETS=WTI,BTC,ETH,SOL,XRP,ZEC,BRENT,COPPER,NGAS`
  - `BTC_QTY=600`
  - `CONTRARIAN_MAX_EXPOSURE=500`
  - `CONTRARIAN_QTY=100`
  - `DEFAULT_QTY=600`
  - `DETERMINISTIC_SETTLEMENT_ALLOWED_ASSETS=ETH`
  - `DETERMINISTIC_SETTLEMENT_COHORT_START=2026-05-11 23:16:00`
  - `DETERMINISTIC_SETTLEMENT_DAILY_CB=-20`
  - `DETERMINISTIC_SETTLEMENT_DAILY_RESET_AT=2026-05-11 23:16:00`
  - `DETERMINISTIC_SETTLEMENT_ENABLED=true`
  - `DETERMINISTIC_SETTLEMENT_HIGH_CUSHION_START=2026-05-11 23:16:00`
  - `DETERMINISTIC_SETTLEMENT_LIFETIME_CB=-60`
  - `DETERMINISTIC_SETTLEMENT_MAX_OPEN=3`
  - `DETERMINISTIC_SETTLEMENT_MIN_CUSHION=0.0040`
  - `DETERMINISTIC_SETTLEMENT_MIN_DEPTH=0`
  - `DETERMINISTIC_SETTLEMENT_MIN_NET_EDGE=0.0`
  - `DETERMINISTIC_SETTLEMENT_MIN_PRICE=0.95`
  - `DETERMINISTIC_SETTLEMENT_PER_TRADE_DOLLAR_CAP=10`
  - `DETERMINISTIC_SETTLEMENT_PILOT_START=2026-05-06 16:28:46`
  - `DETERMINISTIC_SETTLEMENT_PREVIOUS_PILOT_START=2026-05-05 18:12:00`
  - `DETERMINISTIC_SETTLEMENT_QTY=10`
  - `DETERMINISTIC_SETTLEMENT_QTY_10_ETH_ROLLBACK_START=2026-05-10 15:20:00`
  - `DETERMINISTIC_SETTLEMENT_QTY_50_ETH_START=2026-05-09 14:01:37`
  - `DETERMINISTIC_SETTLEMENT_THRESHOLD_PCT=0.0007`
  - `DETERMINISTIC_SETTLEMENT_WINDOW_MINUTES=30`
  - `ENABLE_SPREAD_CAPTURE=false`
  - `ETH_QTY=600`
  - `FAV_QTY=200`
  - `GEMINI_MR_KELLY_MULTIPLIER=0.75`
  - `KELLY_HIGH_PROB_SOFTCAP=0.7`
  - `KELLY_MULTIPLIER=0.75`
  - `KELLY_PER_ASSET_CONCENTRATION_CAP=0.50`
  - `KELLY_SIZING_ENABLED=true`
  - `MAX_EXPOSURE=10000`
  - `MEAN_REVERSION_BLOCKED_ASSETS=WTI,ZEC,BRENT,XRP`
  - `MEAN_REVERSION_MAX_EXPOSURE=999999`
  - `MEAN_REVERSION_QTY=400`
  - `MEAN_REVERSION_QTY_UNVALIDATED=100`
  - `MR_WEEKEND_BLOCKED_ASSETS=`
  - `POSITION_CAP=600`
  - `SPREAD_QTY=15`
  - `VALUE_QTY=10`
- strategy/cohort excerpts:
  - Lifetime P&L: +$6,458.89 across 266 resolved trades
  - 24h P&L: +$818.92 (8W-0L resolved, 25 placed)
  - Today's P&L: +$0.00
  - Record: 236W-30L (89%) | P&L: +$6,458.89
  - Today's P&L: +$0.00
  - Today's raw P&L: +$0.00
  - 24h: 25 placed | 8W-0L resolved | P&L +$818.92
  - 24h resolved by time: morning 0-14 UTC 0W-0L +$0.00 | evening 15-23 UTC 4W-0L +$453.81
  - By expiry: 0-8h: 58W-12L (82.9%) +$797.87 | 16-24h: 124W-12L (91.2%) +$4,419.56 | 8-16h: 54W-6L (90.0%) +$1,537.25
  - Trades in rolling 24h: 17
  - Actual P&L (flat QTY baseline): $0.00
  - Kelly P&L (if Kelly was used): $0.00
  - Config: QTY 10 | Max open 3 | Per-trade $10 | Daily CB $-20 | Lifetime CB $-60 | Min depth 0
  - Active cohort start: 2026-05-11 23:16:00 | CB ledgers scoped to active cohort
  - Daily CB reset at: 2026-05-11 23:16:00 | effective daily ledger uses latest of reset/cohort
  - Today: 48 attempted (37 filled, 0 cancelled, 11 unfilled) | 37 resolved (36W-1L) | +$0.18 P&L
  - Active cohort lifetime (since 2026-05-11 23:16:00): 3 filled | 3 resolved (3W-0L) | +$0.36 P&L
  - (See daily/full-picture report for DB-wide DS lifetime including all prior cohorts.)
  - Cohort lifetime CB ledger: +$0.36 / -$60.00 [SAFE]
  - GEMINI DS COHORT TRACKER

### ibkr
- unit: ibkr-scan-loop.service
- active: active/running
- pid: 2459276
- nrestarts: 0
- active_enter: Sat 2026-05-09 17:47:55 CDT
- reconciliation:
  - Formula: expected cash/NLV uses broker_ledger realized P&L + latest Flex statement snapshot
  - ✓ HARD CHECK PASSED — cash gap $0.00
  - Expected cash = deposits + realized + market data fees + incentive income - cost = $1163.09
  - Actual cash (API): $1163.09
  - Raw cash gap before live delta adjustment: $0.00
  - Cash gap: $0.00
- selected env:
  - `DETERMINISTIC_SETTLEMENT_WEATHER_ENABLED=true`
  - `DETERMINISTIC_SETTLEMENT_WEATHER_KILL_SWITCH=/home/kingeric/.openclaw/workspace/ibkr_forecast_bot/KILL_DETERMINISTIC_SETTLEMENT_WEATHER`
  - `MAX_EXPOSURE=2000`
  - `QTY_PER_POSITION=60`
- strategy/cohort excerpts:
  - Lifetime P&L: -$74.71 across 634 resolved trades
  - 24h P&L: -$11.20 (7W-8L resolved, 6 placed)
  - SELF-MANAGED ACTIVITY (last 24h):
  - Pilots: Weather DS cohort since 2026-05-08 15:20:00: 13 placed, 8 resolved, 5 open, $20.25 open cost, latest=2026-05-12 00:26:26.
  - Cohort gates: Weather DS needs 22 more resolved rows before n>=30 evaluation; no pass/fail scaling action due.
  - Post-qty-increase tracking: 27 placed | 18 resolved (18W-0L) | P&L +$63.00 | avg/resolved +$3.50 | underliers JPUSD=7, USEUR=6, USGBP=6, USCAD=5, USGP=3
  - Entry: categories ECONOMICS, FX | proven underliers 10 | bid $0.85-$0.95 | min expiry 24h | max spread $0.10 | order LIMIT at ASK
  - P&L since deploy: $40.79
  - Live record (all bot resolutions): 57W-3L (95.0%) | P&L +$64.21 | avg +$1.07
  - Filters: bid >= $0.80 | ask <= $0.95 | spread >= $0.04 | expiry 12-48h | lifetime 2h
  - Historical: 6071 entries | 398 resolved | 199W-199L (50.0%) | P&L: -$121.68
  - Final avg P&L/trade: -$0.31 | accumulation disabled; data preserved in shadow_nws_trades
  - 0-24h: 75 collected, 60 resolved (90.0% WR)
  - 0-24h: 0 eligible, 0 resolved (0.0% WR)
  - FX 0-24h: 45 collected, 43 resolved (95.3% WR)
  - ECONOMICS 0-24h: 17 collected, 5 resolved (100.0% WR)
  - FX 0-24h: 0 eligible, 0 resolved (0.0% WR)
  - ECONOMICS 0-24h: 0 eligible, 0 resolved (0.0% WR)
  - PLACEMENT CONVERSION (last 24h):
  - Last 24h: 4544 evaluated | 1 live-eligible (0.0%) | 6 placed (600.0%); top rejects: category_blocked(OTHER) 34%, category_blocked(RATES) 27%, ask_too_expensive(0.98>0.97) 6%

### kalshi
- unit: kalshi-bot.service
- active: active/running
- pid: 3084990
- nrestarts: 0
- active_enter: Mon 2026-05-11 18:04:59 CDT
- reconciliation:
  - Reconciliation: resolved_pnl=$1044.48 open_cost=$1262.23 open_fees=$4.47 recon_adj=$151.82 expected_cash=$2520.15 cash_gap=$+0.00 unrealized=$-324.89 [MATCH]
  - ✓ HARD CHECK PASSED — gap $0.00
  - Reconciliation adjustment: $151.82 (auto-computed from exchange balance)
  - Expected cash: $2520.15
  - Actual cash (API): $2520.15
- selected env:
  - `DETERMINISTIC_SETTLEMENT_ALLOWED_ASSETS=BTC,ETH`
  - `DETERMINISTIC_SETTLEMENT_DAILY_CB=-500`
  - `DETERMINISTIC_SETTLEMENT_DAILY_RESET_AT=2026-05-11 17:55:04-05:00`
  - `DETERMINISTIC_SETTLEMENT_ENABLED=true`
  - `DETERMINISTIC_SETTLEMENT_FX_ALLOWED_SERIES=KXEURUSD,KXUSDJPY`
  - `DETERMINISTIC_SETTLEMENT_FX_DAILY_CB=-150`
  - `DETERMINISTIC_SETTLEMENT_FX_EDGE_THRESHOLD=0.60`
  - `DETERMINISTIC_SETTLEMENT_FX_ENABLED=false`
  - `DETERMINISTIC_SETTLEMENT_FX_KILL_SWITCH=/home/kingeric/kalshi_favorites_bot/KILL_DETERMINISTIC_SETTLEMENT_FX`
  - `DETERMINISTIC_SETTLEMENT_FX_LIFETIME_CB=-400`
  - `DETERMINISTIC_SETTLEMENT_FX_MAX_OPEN=4`
  - `DETERMINISTIC_SETTLEMENT_FX_PER_TRADE_MAX=50`
  - `DETERMINISTIC_SETTLEMENT_FX_QTY=50`
  - `DETERMINISTIC_SETTLEMENT_INDEX_ALLOWED_SERIES=KXINX,KXNASDAQ100`
  - `DETERMINISTIC_SETTLEMENT_INDEX_DAILY_CB=-200`
  - `DETERMINISTIC_SETTLEMENT_INDEX_EDGE_THRESHOLD=0.60`
  - `DETERMINISTIC_SETTLEMENT_INDEX_ENABLED=false`
  - `DETERMINISTIC_SETTLEMENT_INDEX_KILL_SWITCH=/home/kingeric/kalshi_favorites_bot/KILL_DETERMINISTIC_SETTLEMENT_INDEX`
  - `DETERMINISTIC_SETTLEMENT_INDEX_LIFETIME_CB=-500`
  - `DETERMINISTIC_SETTLEMENT_INDEX_MAX_OPEN=4`
  - `DETERMINISTIC_SETTLEMENT_INDEX_PER_TRADE_MAX=50`
  - `DETERMINISTIC_SETTLEMENT_INDEX_QTY=50`
  - `DETERMINISTIC_SETTLEMENT_LIFETIME_CB=-1500`
  - `DETERMINISTIC_SETTLEMENT_LIFETIME_RESET_AT=2026-05-11 17:55:04-05:00`
  - `DETERMINISTIC_SETTLEMENT_MAX_ASSET_HOUR_OPEN=4`
  - `DETERMINISTIC_SETTLEMENT_MAX_EXPOSURE=999999`
  - `DETERMINISTIC_SETTLEMENT_MAX_OPEN=8`
  - `DETERMINISTIC_SETTLEMENT_MIN_NET_EDGE=0.0`
  - `DETERMINISTIC_SETTLEMENT_PER_TRADE_DOLLAR_CAP=500`
  - `DETERMINISTIC_SETTLEMENT_QTY=500`
  - `DETERMINISTIC_SETTLEMENT_THRESHOLD_PCT=0.0007`
  - `DETERMINISTIC_SETTLEMENT_WINDOW_MINUTES=30`
  - `DS_KALSHI_FILTER_COMBINED_START=2026-05-05 15:57:01`
  - `DS_KALSHI_LOW_PRICE_NO_ALLOWED_ASSETS=BTC,ETH,SOL`
  - `DS_KALSHI_LOW_PRICE_NO_COHORT_START=2026-05-05 20:19:08`
  - `DS_KALSHI_LOW_PRICE_NO_DAILY_CB=-20`
  - `DS_KALSHI_LOW_PRICE_NO_ENABLED=false`
  - `DS_KALSHI_LOW_PRICE_NO_KILL_SWITCH=/home/kingeric/kalshi_favorites_bot/KILL_DS_LOW_PRICE_NO_PILOT`
  - `DS_KALSHI_LOW_PRICE_NO_LIFETIME_CB=-60`
  - `DS_KALSHI_LOW_PRICE_NO_MAX_OPEN=3`
  - `DS_KALSHI_LOW_PRICE_NO_MAX_PRICE=0.80`
  - `DS_KALSHI_LOW_PRICE_NO_MIN_DEPTH=10`
  - `DS_KALSHI_LOW_PRICE_NO_PER_TRADE_MAX=20`
  - `DS_KALSHI_LOW_PRICE_NO_QTY=10`
  - `DS_KALSHI_MIN_CUSHION=0.0010`
  - `DS_KALSHI_MIN_PRICE=0.93`
  - `DS_KALSHI_MIN_PRICE_0_93_START=2026-05-10 20:56:50`
  - `DS_KALSHI_PER_ASSET_ROLLBACK_START=2026-05-06 16:28:46`
  - `DS_KALSHI_PER_TRADE_DOLLAR_CAP_BTC=500`
  - `DS_KALSHI_PER_TRADE_DOLLAR_CAP_ETH=300`
  - `DS_KALSHI_QTY_275_ETH_START=2026-05-08 14:35:34`
  - `DS_KALSHI_QTY_300_ETH_START=2026-05-11 17:55:04`
  - `DS_KALSHI_QTY_400_BTC_CVAR_START=2026-05-11 00:52:09`
  - `DS_KALSHI_QTY_500_BTC_REDEPLOY_START=2026-05-11 17:55:04`
  - `DS_KALSHI_QTY_500_BTC_START=2026-05-07 13:35:31`
  - `DS_KALSHI_QTY_600_BTC_ROLLBACK_START=2026-05-10 19:06:00`
  - `DS_KALSHI_QTY_600_BTC_START=2026-05-09 13:56:56`
  - `DS_KALSHI_QTY_700_BTC_START=2026-05-10 03:35:49`
  - `DS_KALSHI_QTY_BTC=500`
  - `DS_KALSHI_QTY_ETH=300`
  - `FAV_QTY=100`
  - `KALSHI_MR_ALLOWED_CELLS_START=2026-05-07 20:20:23`
  - `KALSHI_MR_INDEX_SETTLEMENT_HOUR_CAP=4`
  - `KALSHI_MR_INDEX_UNDERLIER_EVENT_CAP=2`
  - `KALSHI_MR_WEATHER_LOW_YES_CAP_START=2026-05-05 19:23:46`
  - `KALSHI_MR_WEATHER_LOW_YES_COST_CAP=0`
  - `KELLY_HIGH_PROB_SOFTCAP=0.7`
  - `LONGSHOT_FADING_MAX_EXPOSURE=300`
  - `LONGSHOT_FADING_QTY=100`
  - `MAX_EXPOSURE=2500`
  - `MEAN_REVERSION_BLOCKED_HOURS=`
  - `MEAN_REVERSION_BLOCKED_WEATHER_NO_LIST=CHI_LOW,ATL_HIGH,PHIL_HIGH`
  - `MEAN_REVERSION_MAKER_PILOT_MAX_EXPOSURE=100`
  - `MEAN_REVERSION_MAKER_PILOT_MAX_OPEN_ORDERS=3`
  - `MEAN_REVERSION_MAKER_PILOT_QTY=15`
  - `MEAN_REVERSION_MAX_EXPOSURE=999999`
  - `MEAN_REVERSION_QTY=500`
  - `MEAN_REVERSION_QTY_UNVALIDATED=100`
  - `MODERATE_FAVORITES_ALLOWED_ASSETS=BTC,ETH,SOL,WEATHER_LOW,WEATHER_HIGH`
  - `MODERATE_FAVORITES_DAILY_LOSS_CB=-300`
- strategy/cohort excerpts:
  - Lifetime P&L: +$1,044.48 across 2568 resolved trades
  - 24h P&L: +$718.65 (96W-2L resolved, 136 placed)
  - Record: 332W-54L (86%) | P&L: -$268.87
  - ✓ Weather-high blocked (80% WR, -$930 lifetime)
  - ✓ BTC blocked (53 resolved, -$173 lifetime; tail-loss asymmetry)
  - ✓ ETH fully blocked from MR (16W-2L, -$258 lifetime; tail-loss asymmetry)
  - ✓ WEATHER_LOW YES fully blocked (25W-3L, -$206.99 lifetime; NO side unaffected)
  - 24h: 13 placed | 4W-1L resolved | P&L -$164.99
  - Forward allowed-cell tracker: start 2026-05-07 20:20:23 UTC | 7W-2L (77.8%) | P&L $-192.91 | open 8 ($1262.23 cost)
  - WEATHER_LOW YES cap pilot: 0W-0L (0%) | P&L +$0.00 | open 0 ($0.00) | blocks 6/6 attempts | review 0/30 resolved
  - 24h resolved by hour: morning 0-10 CDT 2W-1L (-$248.69) | afternoon 15-20 CDT 0W-0L (+$0.00)
  - Eligible in 4-8h band (would be blocked): observed 13 | resolved 11 | WR 81.8% | P&L without block -$6.26
  - Eligible outside 4-8h band (would still place): observed 23 | resolved 23 | WR 87.0% | P&L +$67.37
  - Verdict: keep current behavior; blocking 4-8h candidates would have hurt P&L
  - In preferred range ($0.75-$0.85): observed 20 | resolved 18 | WR 77.8% | P&L -$26.71
  - Outside preferred range (current live band): observed 16 | resolved 16 | WR 93.8% | P&L +$87.82
  - Decision trigger: at 30+ resolved in each slice, pilot only if preferred-range WR/P&L is materially better
  - Record: 22W-3L (88.0%) | P&L: $-205.31
  - NWS FILTER BEHAVIOR (last 24h):
  - 297645 entries | 290029 resolved | 288854W-1175L (99.6%) | P&L: +$402,085.20

## Storage State
- DATABASE STORAGE HEALTH
-   Overall status: GREEN / TARGET
-   Disk: 194.67 GiB used / 936.79 GiB total (20.8%), 694.46 GiB free
-   Envelope: TARGET 50.0%, WARN 65.0%, CRITICAL 75.0%, HARD_LIMIT 85.0%
-   DS storage: active 4.28 GiB (state TARGET), hot 99.85 GiB, warm 0.00 GiB, cold 0.00 GiB, archive_state CRITICAL, total 104.15 GiB (11.1% of disk)
-   Retention engine: last=2026-05-12T10:55:06+00:00 status=OK dry_run=False rows_selected=0 rows_archived=0 rows_pruned=0
-   Archive compression: status=OK actions=0 warm_days=7 min_file_mb=100
-   Tier rotation: last=2026-05-12T10:55:06+00:00 status=OK actions=0
-   Autonomous maintenance: last=2026-05-12T10:43:53+00:00 status=OK backups=5/5 integrity_failures=0 drift_flags=0
-   PROTECT_TRADING mode: NO

## Timers
```
NEXT                            LEFT LAST                              PASSED UNIT                                          ACTIVATES
Tue 2026-05-12 06:10:30 CDT       7s Tue 2026-05-12 06:10:03 CDT      19s ago gemini-cushion-ds-scanner.timer               gemini-cushion-ds-scanner.service
Tue 2026-05-12 06:11:00 CDT      37s Tue 2026-05-12 06:10:03 CDT      19s ago cushion-ds-multi-series-scanner.timer         cushion-ds-multi-series-scanner.service
Tue 2026-05-12 06:11:10 CDT      48s Tue 2026-05-12 06:10:10 CDT      11s ago ibkr-scan-loop-watchdog.timer                 ibkr-scan-loop-watchdog.service
Tue 2026-05-12 06:14:37 CDT 4min 14s Tue 2026-05-12 06:04:36 CDT     5min ago ds-shadow-continuous-archive.timer            ds-shadow-continuous-archive.service
Tue 2026-05-12 06:15:00 CDT 4min 37s Tue 2026-05-12 06:00:01 CDT    10min ago cushion-ds-multi-series-resolver.timer        cushion-ds-multi-series-resolver.service
Tue 2026-05-12 06:15:00 CDT 4min 37s Tue 2026-05-12 06:00:01 CDT    10min ago gemini-cushion-ds-resolver.timer              gemini-cushion-ds-resolver.service
Tue 2026-05-12 06:21:57 CDT    11min Tue 2026-05-12 05:20:03 CDT    50min ago consensus-tracking-resolver.timer             consensus-tracking-resolver.service
Tue 2026-05-12 06:25:06 CDT    14min Tue 2026-05-12 06:10:06 CDT      16s ago ds-storage-pressure-monitor.timer             ds-storage-pressure-monitor.service
Tue 2026-05-12 06:26:24 CDT    16min Tue 2026-05-12 05:25:06 CDT    45min ago moderate-favorites-unr-resolver.timer         moderate-favorites-unr-resolver.service
Tue 2026-05-12 06:39:39 CDT    29min Tue 2026-05-12 05:38:06 CDT    32min ago moderate-favorites-finance-resolver.timer     moderate-favorites-finance-resolver.service
Tue 2026-05-12 06:41:52 CDT    31min Tue 2026-05-12 05:41:24 CDT    28min ago moderate-favorites-weather-resolver.timer     moderate-favorites-weather-resolver.service
Tue 2026-05-12 06:50:19 CDT    39min Tue 2026-05-12 05:50:03 CDT    20min ago moderate-favorites-economics-resolver.timer   moderate-favorites-economics-resolver.service
Tue 2026-05-12 06:58:26 CDT    48min Tue 2026-05-12 05:56:31 CDT    13min ago ladder-coherence-resolver.timer               ladder-coherence-resolver.service
Tue 2026-05-12 07:05:25 CDT    55min Tue 2026-05-12 06:03:39 CDT     6min ago macro-release-resolver.timer                  macro-release-resolver.service
Tue 2026-05-12 07:07:37 CDT    57min Tue 2026-05-12 06:05:40 CDT 4min 41s ago spread-capture-resolver.timer                 spread-capture-resolver.service
Tue 2026-05-12 07:17:00 CDT  1h 6min Tue 2026-05-12 01:17:06 CDT 4h 53min ago ds-shadow-retention-engine.timer              ds-shadow-retention-engine.service
Tue 2026-05-12 09:00:00 CDT 2h 49min Tue 2026-05-12 06:00:01 CDT    10min ago snap.firmware-updater.firmware-notifier.timer snap.firmware-updater.firmware-notifier.service
Tue 2026-05-12 09:14:28 CDT  3h 4min Mon 2026-05-11 09:14:28 CDT      20h ago launchpadlib-cache-clean.timer                launchpadlib-cache-clean.service
Tue 2026-05-12 09:24:00 CDT 3h 13min Tue 2026-05-12 03:24:06 CDT 2h 46min ago ds-shadow-archive.timer                       ds-shadow-archive.service
Tue 2026-05-12 09:40:00 CDT 3h 29min Tue 2026-05-12 03:40:00 CDT 2h 30min ago ds-storage-monitor.timer                      ds-storage-monitor.service
Tue 2026-05-12 11:31:16 CDT 5h 20min Tue 2026-05-12 05:31:16 CDT    39min ago ds-shadow-db-maintenance.timer                ds-shadow-db-maintenance.service
Tue 2026-05-12 23:35:00 CDT      17h Mon 2026-05-11 23:55:01 CDT       6h ago ibkr-deterministic-fx-poc.timer               ibkr-deterministic-fx-poc.service
Wed 2026-05-13 04:30:00 CDT      22h Tue 2026-05-12 04:30:03 CDT 1h 40min ago tax-ledger-ingest.timer                       tax-ledger-ingest.service
Wed 2026-05-13 04:44:58 CDT      22h Tue 2026-05-12 04:49:06 CDT 1h 21min ago ds-archive-tier-rotation.timer                ds-archive-tier-rotation.service
Wed 2026-05-13 05:20:00 CDT      23h Tue 2026-05-12 05:20:03 CDT    50min ago logrotate-user.timer                          logrotate-user.service
Wed 2026-05-13 05:30:00 CDT      23h Tue 2026-05-12 05:30:04 CDT    40min ago disk-hygiene-audit.timer                      disk-hygiene-audit.service
Wed 2026-05-13 05:40:00 CDT      23h Tue 2026-05-12 05:40:04 CDT    30min ago database-autonomous-maintenance.timer         database-autonomous-maintenance.service
-                                  - Tue 2026-05-12 06:10:03 CDT      19s ago claude-chat-sync.timer                        claude-chat-sync.service

28 timers listed.
```

## Repo State
- gemini: head=8c79e88 branch=master in_sync=true remote=https://github.com/PhotonRahm/gemini_prediction_bot.git dirty=no
- ibkr: head=e1a8d8b branch=master in_sync=true remote=https://github.com/PhotonRahm/ibkr_forecast_bot.git dirty=no
- kalshi: head=6604517 branch=master in_sync=true remote=https://github.com/PhotonRahm/kalshi_favorites_bot.git dirty=no
- operations-knowledge: head=45a765e branch=master in_sync=true remote=https://github.com/PhotonRahm/operations-knowledge.git dirty=no
- workspace: head=503446d branch=master in_sync=true remote=https://github.com/PhotonRahm/rahm-workspace.git dirty=no

## Deferred And Pending Items
```
specific trigger condition. Once the trigger is in the past, the item is due and
should be handled in the next operational review.
## Pending
| Key | Verification | Why deferred | Trigger | Due |
| `tax_ledger_gemini_q1_2026_reconciliation_resolution` | Resolve Gemini Q1 known tax-ledger gap | Operator overrode the 2026-05-11 halt and completed source-of-truth remediation with the Gemini Q1 legacy FIFO-vs-direct gap documented as OPEN. | Before 2026-06-08 if practical, decompose the $3,946.52 gap into line items, update Decision 1 or Decision 9 if needed, re-ingest Gemini under corrected methodology, verify reconciliation within $5, and mark the known gap RESOLVED. | 2026-06-08 |
| `tax_ledger_q2_2026_estimated_payment_prep_review` | Q2 2026 estimated-payment prep | The source-of-truth tax ledger now generates Q2 partial planning reports, but the Gemini Q1 known gap remains open under Decision 9. | On 2026-06-08, run Q2 estimated-tax planning report, review open CPA flags, and decide whether the Gemini Q1 gap is resolved or carried into payment planning. | 2026-06-08 |
| `tax_ledger_q3_2026_estimated_payment_prep_review` | Q3 2026 estimated-payment prep | Quarterly payment prep should use the autonomous source-of-truth ledger and review open CPA flags. | Run Q3 planning report and review methodology flags. | 2026-09-08 |
| `tax_ledger_q4_2026_estimated_payment_prep_review` | Q4 2026 estimated-payment prep | Quarterly payment prep should use the autonomous source-of-truth ledger and review open CPA flags. | Run Q4 planning report and review methodology flags. | 2026-12-08 |
| `tax_ledger_2026_annual_filing_prep_review` | 2026 annual filing prep | CPA review is recommended before filing, especially for event-contract tax posture and the Gemini Q1 known gap. | On 2027-02-01, engage CPA/review methodology decisions, resolve open CPA flags, generate annual report, and freeze filing methodology. | 2027-02-01 |
| `ds_shadow_archive_batch_next_timer_review` | DS shadow batch archive service verification | The shared archive schema drift defect was fixed and the bounded continuous archive path succeeded, but the heavier `ds-shadow-archive.service` batch path was not manually forced during live operations. | After the next scheduled `ds-shadow-archive.timer` run, verify the service exits successfully and no longer fails with `sqlite3.OperationalError: no such column: cohort_start`. | Next scheduled timer run |
| `gemini_proper_cushion_shadow_decision_gate` | Gemini full-universe proper cushion DS live/retire decision gate | Scope 3 scanner starts a clean forward cohort in `shadow_gemini_cushion_ds`; decision-grade promotion or retirement requires per-asset independent contract-settlement evidence rather than favorite-tracking aggregates or repeated row observations. Updated 2026-05-10 per AGENTS.md Principle 51. | Once `shadow_gemini_cushion_ds` reaches n>=30 independent executable contract-settlement events per asset with Wilson lower above breakeven and positive collapsed P&L, evaluate per-asset live pilot, scale, or retire decision. Row-level metrics remain descriptive only. | Trigger-based, estimated 2-4 weeks after deploy |
| `weather_cushion_ds_contract_date_gate` | Weather cushion DS unit-of-independence and time-window gate | Weather cushion-DS rows are repeated observations of daily weather contracts. The 2026-05-10 Gemini weather forensic showed row-level LIVE_PILOT_CANDIDATE labels collapsed to only 4-7 independent executable contract-date groups. Dispatch-conventions now also pre-commits an actionable time-window rule for future weather live pilot consideration. Updated 2026-05-10 per AGENTS.md Principle 51. | Once `weather_cushion_ds_shadow` per-cell time-windowed contract-date-collapsed metrics reach n>=30 independent executable contract-date groups with Wilson lower above breakeven and positive collapsed P&L within the actionable window, evaluate per-cell live pilot or retire decision. Row-level and full-lifetime collapsed metrics remain descriptive/contextual for pilot promotion. | Trigger-based |
| `shadow_coverage_inventory_review` | Comprehensive DS coverage map review | Phase 2b closed Gemini weather and depth, and mapped the only current Gemini sports single-game subset; review accumulation after first resolutions. | Review `SHADOW COVERAGE INVENTORY` after 7 days of accumulation and prioritize any newly listed marginal cells. | 2026-05-10 12:00 UTC |
| `index_fx_salvage_methodology_review` | Kalshi Index/FX Longshot Fade salvage methodology review | First live taker-side cohorts resolved 0W-8L combined, dispositive against the promoted shadow hypothesis. | Opportunistic only: review a new forward-shadow methodology such as liquidity/depth filter or maker variant before any re-enable proposal. | Trigger-based |
| `kalshi_ds_qty_225_cohort_50_resolution_review` | Kalshi DS qty 225 cohort review | Kalshi crypto DS operates per-asset: BTC qty 700 (cohort `filter_combined_qty_700_btc_pilot`, accumulating), ETH qty 275 since 2026-05-08 14:35:34 (cohort `filter_combined_qty_275_eth_pilot`, accumulating). Initial quarter-Kelly Wilson-lower qty=225 cohort closed PASSED at 38 resolved (37W-1L, +$117.74). | CLOSED at the qty-225 layer; forward review now tracked separately by per-asset cohort rows (`kalshi_ds_qty_700_btc_30_resolution_review` and `kalshi_ds_qty_275_eth_30_resolution_review`). | Completed 2026-05-08 |
| `kalshi_ds_qty_275_eth_30_resolution_review` | Kalshi DS ETH qty 275 cohort review | CLOSED PASSED 2026-05-11: `filter_combined_qty_275_eth_pilot` reached 53 resolved, 52W-1L, WR 98.1%, Wilson lower 90.1%, P&L +$127.06, and no daily CB breach. Operator honored EXPANSION_CANDIDATE with qty 300. | CLOSED. Forward ETH review now tracked under `kalshi_ds_qty_300_eth_30_resolution_review`. | Completed 2026-05-11 |
| `kalshi_ds_combined_filter_50_resolution_review` | Kalshi DS combined-filter review | Loss-pattern investigation found price >=0.90 and cushion >=0.10% cell materially outperformed the broader crypto DS set; filter deployed without changing qty/max_open/CBs. | Once `ds_qty_cohort_tracker` `filter_combined_pilot` reaches 50+ resolved post-filter trades, evaluate WR>=95%, Wilson lower>=90%, positive P&L, no daily CB breach, and per-asset BTC/ETH breakdown. | Trigger-based, expected ~12-24h depending on filter pass rate |
| `kalshi_ds_qty_400_30_resolution_review` | Kalshi DS qty 400 cohort review | Completed 2026-05-06: aggregate qty-400 cohort failed its gate at 30 resolved, 27W-3L, Wilson lower 74.4%, P&L -$691.95, and daily CB breach. Operator approved per-asset rollback: BTC stays qty 400, ETH returns to qty 225. | CLOSED. Evidence preserved in `ds_qty_cohort_tracker` as `filter_combined_qty_400_pilot`; no further action on aggregate cohort. | Completed 2026-05-06 |
| `kalshi_ds_qty_500_btc_30_resolution_review` | Kalshi DS BTC qty 500 per-asset cohort review | Completed 2026-05-09: `filter_combined_qty_500_btc_pilot` reached 60 resolved, 59W-1L, WR 98.3%, Wilson lower 91.1%, P&L +$435.94, max DD $442.20, and no daily CB breach. Operator honored EXPANSION_CANDIDATE with qty 600. | CLOSED. Forward BTC review now tracked under `kalshi_ds_qty_600_btc_30_resolution_review`. | Completed 2026-05-09 |
| `kalshi_ds_qty_600_btc_30_resolution_review` | Kalshi DS BTC qty 600 per-asset cohort review | Completed 2026-05-09 evening: `filter_combined_qty_600_btc_pilot` reached 38 resolved, 38W-0L, WR 100%, Wilson lower 90.8%, P&L +$833.07, max DD $0.00, and no daily CB breach. Operator honored EXPANSION_CANDIDATE with qty 700. | CLOSED. Forward BTC review now tracked under `kalshi_ds_qty_700_btc_30_resolution_review`. | Completed 2026-05-09 |
| `kalshi_ds_qty_700_btc_30_resolution_review` | Kalshi DS BTC qty 700 per-asset cohort review | CLOSED FAILED 2026-05-10: `filter_combined_qty_700_btc_pilot` reached 26 resolved at 24W-2L, Wilson lower 75.9% (below 88% gate), P&L -$751.17, and daily CB breach. Operator honored ROLLBACK_RECOMMENDED by rolling BTC back to qty 600. | CLOSED. Evidence preserved in `ds_qty_cohort_tracker`; qty-700 rows are informative only and are not inherited into the rollback cohort. | Completed 2026-05-10 |
| `kalshi_ds_qty_600_btc_rollback_30_resolution_review` | Kalshi DS BTC qty 600 rollback cohort review | SUPERSEDED 2026-05-10. The qty-600 rollback cohort was closed at 10 resolved, 9W-1L, WR 90.0%, Wilson lower 59.6%, P&L -$325.54, max DD $559.63, and CB intact per CVaR-driven interim reduction. Operator chose to reduce qty proactively rather than wait for formal gate failure. | CLOSED. New cohort `filter_combined_qty_400_btc_cvar_pilot` opens 2026-05-11 00:52:09 UTC; see `kalshi_ds_qty_400_btc_cvar_30_resolution_review`. | Completed 2026-05-10 |
| `kalshi_ds_qty_400_btc_cvar_30_resolution_review` | Kalshi DS BTC qty 400 CVaR interim cohort review | CLOSED PASSED 2026-05-11: `filter_combined_qty_400_btc_cvar_pilot` reached 50 resolved, 49W-1L, WR 98.0%, Wilson lower 89.5%, P&L +$236.71, and no daily CB breach. Operator elected scale-up to qty 500 with explicit beyond-CVaR-aggressive acknowledgment. | CLOSED. Forward BTC review now tracked under `kalshi_ds_qty_500_btc_redeploy_30_resolution_review`. | Completed 2026-05-11 |
| `kalshi_ds_min_price_0_93_30_resolution_review` | Kalshi DS min-price $0.93 filter cohort review | CLOSED PASSED 2026-05-11: `filter_min_price_0_93_pilot` reached 111 resolved, 110W-1L, WR 99.1%, Wilson lower 95.1%, P&L +$488.56. Filter validated and remains active. | CLOSED. Continued monitoring occurs inside the new qty cohorts; the filter itself stays active with no automatic scale-up authority. | Completed 2026-05-11 |
| `kalshi_ds_qty_500_btc_redeploy_30_resolution_review` | Kalshi DS BTC qty 500 redeploy cohort review | Operator scaled BTC qty/cap 400 -> 500 on 2026-05-11 17:55:04 CDT after the qty-400 CVaR cohort and $0.93 filter cohort cleared gates. This is a fresh redeploy cohort because the original `filter_combined_qty_500_btc_pilot` already exists as a closed historical cohort. | Once `ds_qty_cohort_tracker` `filter_combined_qty_500_btc_redeploy_pilot` reaches 30+ resolved BTC trades, evaluate WR>=95%, Wilson lower>=88%, positive P&L, and no daily CB breach. No automatic further scale-up regardless of result; any further qty change requires explicit operator approval and fresh dispatch. If qty-500 cohort fails P&L or CB at n=30, roll back to qty 400 per separate operator decision. | Trigger-based |
| `kalshi_ds_qty_300_eth_30_resolution_review` | Kalshi DS ETH qty 300 cohort review | Operator scaled ETH qty/cap 275 -> 300 on 2026-05-11 17:55:04 CDT after the qty-275 ETH cohort and $0.93 filter cohort cleared gates. | Once `ds_qty_cohort_tracker` `filter_combined_qty_300_eth_pilot` reaches 30+ resolved ETH trades, evaluate WR>=93%, Wilson lower>=85%, positive P&L, and no daily CB breach. No automatic further scale-up regardless of result. If qty-300 cohort fails P&L or CB at n=30, roll back to qty 275 per separate operator decision. | Trigger-based |
| `kalshi_ds_qty_225_eth_30_resolution_review` | Kalshi DS ETH qty 225 rollback cohort review | Completed 2026-05-08: `filter_combined_qty_225_eth_pilot` reached 38 resolved at 37W-1L, Wilson lower 86.5%, +$117.74, and the operator honored EXPANSION_CANDIDATE by scaling ETH to qty 275. | CLOSED. Forward ETH review now tracked under `kalshi_ds_qty_275_eth_30_resolution_review`. | Completed 2026-05-08 |
| `kalshi_ds_max_open_5_to_8_utilization_review` | Kalshi DS max_open 5->8 utilization review | Max_open was restored from 5 to 8 after BTC qty 400 / ETH qty 225 per-asset split made ETH-heavy windows underutilize capital. The DS dollar exposure cap was effectively disabled on 2026-05-10 with `DETERMINISTIC_SETTLEMENT_MAX_EXPOSURE=999999`, so platform cash is now the binding dollar constraint. This is a capital-throughput monitor, not a new per-trade strategy gate. | Review the `5->8` cap era after 30+ resolved trades or two active trading days, whichever comes first. Check active-window capital utilization target 60-90%, daily P&L trend, no daily CB breach, asset-hour cap block count, and whether max_open or platform cash is binding. Rollback/review if daily CB breaches on 2 consecutive days or cap-era quality materially deteriorates versus the historical 6->8 cohort. | Trigger-based |
| `kalshi_ds_cluster_cap_postfix_30_resolution_review` | Kalshi DS post-cluster-cap review | Qty-400 loss investigation found no filter or resolver bug, but did find funded-slot selection drift and correlated same asset/hour exposure. Max open was reduced to 5 and max asset/settlement-hour open positions capped at 4 on 2026-05-06. | Once 30 post-fix `strategy='deterministic_settlement'` rows have resolved, evaluate WR>=95%, Wilson lower>=88%, positive P&L, no daily CB breach, asset/hour cap block count, and whether qty 400 should continue, roll back, or pause. | Trigger-based |
| `gemini_mr_kelly_075_50_resolution_review` | Gemini MR Kelly 0.75x forward review | Operator scaled Kelly multiplier from 0.625 to 0.75 on 2026-05-10 based on EB posteriors exceeding predicted probabilities across BTC/ETH/SOL cells. The 50% per-asset concentration cap remains the binding correlated-blowup control. Source: operator decision log 2026-05-10. | Once gemini-bot post-deploy resolved MR placements reach n>=50, compare per-asset W-L and P&L to the 0.625x era, evaluate drawdown profile, concentration-cap hit rate, daily CB consumption, and Kelly shadow delta. If daily CB breaches or max DD materially exceeds 0.625x cohort, roll back Kelly to 0.625. Success does not authorize further Kelly increase without explicit operator approval and a fresh 100-resolution review. | Trigger-based |
| `gemini_mr_eb_kelly_50_trade_review` | Gemini MR empirical-Bayes half-Kelly review | Gemini MR now uses half-Kelly sizing with empirical-Bayes calibration and a permanent 50% per-asset concentration cap. Initial EB cells are mostly accumulating because per-asset n<30. | Once 50 post-deploy Gemini MR placements have resolved, compare raw vs calibrated probability, final qty, concentration-cap hits, per-asset W-L/P&L, and reconciliation state. | Trigger-based |
| `kalshi_proper_index_fx_cushion_shadow_decision_gate` | Proper Index/FX cushion DS promotion gate | Existing large Index/FX shadow evidence is favorite-tracking/longshot methodology, while the proper final-30m cushion DS table now accumulates from the separate `cushion-ds-multi-series-scanner.timer` deployed 2026-05-10. Sports is intentionally separate because it lacks a numeric spot/strike cushion. The legacy live Index/FX longshot keys remain killed. Updated 2026-05-10 per AGENTS.md Principle 51. | Once `shadow_index_fx_cushion_ds` reaches n>=30 independent executable contract-settlement events per series with Wilson lower above breakeven and positive collapsed P&L, evaluate per-series live pilot deployment. Row-level metrics remain descriptive only. | Trigger-based, estimated 2-4 weeks after deploy depending on per-series accumulation rate |
| `gemini_ds_parallel_filter_30_resolution_review` | Gemini DS parallel-filter pilot review | Completed 2026-05-06: parallel filter reached 36 resolved, 33W-3L, Wilson lower 78.2%, P&L -$14.48. All three losses were SOL; operator approved removing SOL and continuing BTC/ETH only. | CLOSED. Evidence preserved in `gemini_ds_cohort_tracker` as closed `parallel_filter_pilot`; no further action on BTC/ETH/SOL cohort. | Completed 2026-05-06 |
| `gemini_ds_parallel_filter_btc_eth_30_resolution_review` | Gemini DS BTC/ETH parallel-filter refinement review | Completed 2026-05-07: `parallel_filter_btc_eth_pilot` failed at 42 resolved, 37W-5L, Wilson lower 75.0%, P&L -$24.63, and daily CB breach. Loss-pattern review found all five losses below entry price 0.95. | CLOSED. Evidence preserved in `gemini_ds_cohort_tracker` as closed `parallel_filter_btc_eth_pilot`; no further action on the price>=0.90 BTC/ETH cohort. | Completed 2026-05-07 |
| `gemini_ds_eth_high_price_30_resolution_review` | Gemini DS ETH-only high-price refinement review | Completed 2026-05-09: `filter_combined_eth_high_price_pilot` reached 52 resolved, 52W-0L, WR 100%, Wilson lower 93.1%, P&L +$15.50, max DD $0.00, and no daily CB breach. Operator honored EXPANSION_CANDIDATE with qty 50. | CLOSED. Forward ETH review now tracked under `gemini_ds_eth_qty_50_30_resolution_review`. | Completed 2026-05-09 |
| `gemini_ds_eth_qty_50_30_resolution_review` | Gemini DS ETH qty 50 high-price review | CLOSED FAILED 2026-05-10: `filter_combined_eth_high_price_qty_50_pilot` reached 39 resolved, 37W-2L, WR 94.9%, Wilson lower 83.1%, P&L -$35.79, max DD $79.52. Operator honored ROLLBACK_RECOMMENDED and rolled ETH back to qty 10. | CLOSED. Evidence preserved in `gemini_ds_cohort_tracker`; qty-50 rows are informative only and not inherited into the rollback cohort. | Completed 2026-05-10 |
| `gemini_ds_high_cushion_30_resolution_review` | Gemini DS ETH high-cushion qty 10 review | The qty-10 rollback cohort failed positive-P&L at 78 resolved (73W-5L, Wilson 85.9%, P&L -$22.77). The surgical refinement tightens live Gemini DS to price>=0.95 and cushion>=0.40%, preserving qty 10 and all CBs. New cohort `filter_combined_eth_high_cushion_qty_10_pilot` starts 2026-05-11 23:16:00 UTC / 18:16:00 CDT. | Once `gemini_ds_cohort_tracker` `filter_combined_eth_high_cushion_qty_10_pilot` reaches 30+ resolved ETH trades, evaluate WR>=96%, Wilson lower>=88%, positive cohort P&L, and no daily CB breach. No automatic scale-up. If P&L is negative at n>=30 or daily CB breaches earlier, kill or pause Gemini DS per separate operator decision. | Trigger-based |
| `kalshi_moderate_favorites_crypto_yes_0_1h_80_85_resurrection_review` | Kalshi Moderate Favorites resurrection review | 2026-05-11 forensic returned Verdict B: forward Kalshi crypto/YES/0-1h/$0.80-$0.85 was positive at 69 resolved, 59W-10L, Wilson 75.3%, +$175, but first 70% temporal split was negative (-$180), historical live matched rows were only 28 resolved, and BTC-only forward Wilson was 74.7%. | Re-evaluate once post-pause forward tracker reaches either all-crypto n>=100 with WR>=85%, Wilson>=78%, positive P&L, and positive P&L in both temporal halves, or BTC-only n>=75 with WR>=85%, Wilson>=75%, positive P&L, and positive P&L in both temporal halves. If cleared, write a separate live-pilot deployment dispatch; do not auto-enable from shadow data. | Trigger-based |
| `whelan_weather_0_5_1h_independent_contract_review` | Whelan near-expiry weather independent-contract review | 2026-05-11 forensic returned Verdict B: row-level weather/0.5-1h was 37W-0L, +$275, but collapsed to only 11 independent contract symbols, 11W-0L, Wilson 74.1%, +$77. Non-crypto/0.5-1h flipped from +$149 row-level to -$49 collapsed, proving row count is not decision-grade. | Once `shadow_near_expiry_favorites` weather/0.5-1h reaches 30+ independent resolved contract symbols after collapse-by-symbol, evaluate collapsed W-L/P&L using first eligible row per symbol, Wilson lower above breakeven, positive P&L in both temporal halves, and explicit exclusion of adjacent weather 1-2h and 2-4h bands. If all pass, write a separate bounded live-pilot deployment dispatch; do not auto-deploy from row-level counts. | Trigger-based |
| `order_book_imbalance_correlation_analysis` | Kalshi/Gemini DS order-book imbalance correlation analysis | Forward-only order-book imbalance instrumentation was added to Kalshi DS and Gemini DS live trade rows on 2026-05-10. Historical rows remain NULL. Metrics include top-of-book imbalance, level-5 imbalance, within-3%-of-mid imbalance, microprice, microprice-vs-mid, total top-5 depth, and relative spread. The fields are observation-only and do not affect placement decisions. | Once Kalshi DS and Gemini DS each have 100+ resolved deterministic-settlement trades with `bid_ask_imbalance_top IS NOT NULL`, analyze correlation between imbalance metrics at placement and trade outcomes. If WR by imbalance quartile differs by >5pp with Fisher p<0.05 after Bonferroni correction across tested metrics, a candidate surgical-filter dispatch may follow. If no correlation, close the imbalance hypothesis false. | Trigger-based |
| `kalshi_mr_index_cluster_cap_review` | Kalshi MR INDEX cluster cap review | Path B deployed max 2 open MR INDEX positions per underlier/event and max 4 total open MR INDEX positions per settlement hour after loss-pattern analysis found same-settlement clustering as the highest-evidence unmitigated INDEX risk. Existing open INDEX rows at deploy are grandfathered. | Once post-deploy INDEX MR rows have 30+ resolved trades or on 2026-05-21, whichever comes first, evaluate INDEX P&L, block counts, max same-event/hour exposure, and whether the max 2/max 4 cap should stay, tighten, loosen, or retire INDEX. | 2026-05-21 20:20 UTC |
| `kalshi_mr_allowed_cells_forward_pnl_review` | Kalshi MR currently-allowed cell forward P&L review | REPLACED 2026-05-11 by `kalshi_mr_post_surgical_blocks_30_resolution_review` after ETH and WEATHER_LOW YES were promoted from capped/partial controls to full surgical blocks. | CLOSED. Evidence before replacement remains visible in Kalshi status as the pre-block allowed-cell tracker. | Completed 2026-05-11 |
| `gemini_ds_realized_volatility_first_live_rows` | Gemini DS realized-volatility instrumentation first live rows | Gemini DS `realized_volatility_at_entry` returned NULL because `bot.py` referenced `sqlite3.Row` without importing `sqlite3`; fix applies forward only and historical rows are not backfilled. | On the first Gemini DS trade after the parallel-filter deploy, verify `time_to_settlement_seconds` and `realized_volatility_at_entry` are populated, or realized volatility is explicitly NULL only with an insufficient-history warning. | Trigger-based |
| `ds_entry_instrumentation_first_live_rows` | DS entry instrumentation first-row verification | `time_to_settlement_seconds` and `realized_volatility_at_entry` schema, placement code, and tests are deployed, but no post-deploy Kalshi/Gemini DS placement occurred during restart verification windows. | On the first Kalshi DS trade after `DS_KALSHI_FILTER_COMBINED_START` and first Gemini DS trade after `DETERMINISTIC_SETTLEMENT_PILOT_START`, verify both new fields are populated or explicitly NULL only when insufficient spot history exists; confirm price/cushion/depth filters on the same rows. | Trigger-based |
| `kalshi_mr_weather_low_yes_cap_30_resolution_review` | Kalshi MR WEATHER_LOW YES permanent-cap review | SUPERSEDED 2026-05-11 by full WEATHER_LOW YES block. The prior cap remains documented but is no longer the active policy. | CLOSED. Forward review now tracked under `kalshi_mr_post_surgical_blocks_30_resolution_review`. | Completed 2026-05-11 |
| `kalshi_mr_post_surgical_blocks_30_resolution_review` | Kalshi MR post-surgical-block review | On 2026-05-11 Kalshi MR added full ETH and WEATHER_LOW YES blocks after both cells showed high-WR/negative-P&L asymmetry. Pre-block lifetime MR P&L was -$288.74; open pre-block MR rows continue resolving naturally. | Once Kalshi MR placements after `KALSHI_MR_SURGICAL_BLOCKS_START=2026-05-11 18:01:00` reach 30+ resolved, evaluate residual cell-by-cell P&L, residual YES vs NO aggregate P&L, daily CB breach count, and lifetime MR P&L delta from -$288.74. If residual MR forward P&L is still negative at n=30, evaluate blanket YES block, further surgical blocks, or full strategy pause/retire per separate operator decision. If positive, continue current config and accumulate to n=50. | Trigger-based |
| `kalshi_mr_instrumentation_first_live_rows` | Kalshi MR first live instrumentation rows | MR placement path now writes `time_to_settlement_seconds` and quote-path `realized_volatility_at_entry` forward-only; historical MR rows remain NULL. | On the first Kalshi MR placement after the deploy, verify both fields are populated, or realized volatility is explicitly NULL only with an insufficient-history warning in logs. | Trigger-based |
| `kalshi_ds_low_price_no_30_resolution_review` | Kalshi DS low-price NO pilot review | Completed 2026-05-06: pilot was 15W-6L at 21 resolved and mathematically could not reach the 90% WR gate by 30 resolved. Paused early as equivalent gate failure and BUG_CLASSES #24 subset-overfitting lesson preserved. | CLOSED. Existing open positions settle naturally; do not re-enable without a fresh operator-approved methodology and cohort boundary. | Completed 2026-05-06 |
| `kalshi_ds_low_price_no_first_live_rows` | Kalshi DS low-price NO first-placement instrumentation | Pilot instrumentation is forward-only and no historical rows are backfilled. | On first `strategy='ds_low_price_no'` filled row, verify side=NO, price < $0.80, asset in BTC/ETH/SOL, qty=10, `time_to_settlement_seconds`, `realized_volatility_at_entry`, `cushion_at_entry`, and depth fields are populated or explicitly explain any NULL. | Trigger-based |
| `ibkr_weather_ds_kaus_uh_removed_evidence_check` | IBKR Weather DS post-KAUS removal evidence check | Workspace `analysis/phase3/SYNTHESIS.md` classified `ibkr|UHAUS|HIGH|cushion_2_to_5f` as a validated kill (n=101, 45W-56L, Wilson upper 54.3% vs 73.2% breakeven, P&L -$6.03), and live Weather DS had two corroborating KAUS_UH/UHAUS losses. `KAUS_UH` was removed from the active Weather DS cell list on 2026-05-05. | Once post-removal `deterministic_settlement_weather` has >=20 broker-truth resolved rows, compare overall Weather DS WR, broker-truth P&L, CB consumption, and per-cell mix against the prior 4-trade baseline and verify no new UHAUS placements occurred after the code deploy. | Trigger-based |
| `ibkr_economics_mrn_sideaware_next_resolution` | IBKR economics MRN side-aware resolver verification | 2026-05-06 audit fixed DS expansion mapping for `macro_release_signals.actual_outcome`, which is side-relative rather than actual YES/NO. Current DS expansion economics rows do not overlap the already resolved source rows, so the fixed path needs a forward resolved source row to prove report output. | Once `macro_release_signals` has a newly resolved row after the fix and the DS expansion scanner has inserted the corresponding economics observation, verify a NO-side win resolves to `actual_outcome='NO'`, W-L uses `realized_pnl > 0`, and economics is not promoted while FRED remains dirty. | Trigger-based |
| `ibkr_consensus_tracking_first_forward_resolution` | IBKR Consensus Tracking first forward-tagged resolution | First forward-tagged row is verified, but the initial row (`UNR_0426_4_YES`, release `20260508`) is not mature yet; resolver dry-run checks 0 rows until after expiry. The resolver timer now runs `--category ALL`, so this ECONOMICS row is covered when it matures. | After `shadow_consensus_tracking.favorite_symbol IS NOT NULL` rows mature past `release_date`, run/observe `consensus-tracking-resolver.timer`, verify `resolved=1`, `favorites_won` is side-aware, `resolution_source` is populated, and no live trades/broker/position tables changed. | Trigger-based |
| `storage_monitoring_baseline_review` | DS per-category storage monitoring 7-day baseline review | `db_category_storage_monitor.py` was deployed on 2026-05-05 with a 6-hour timer and first baseline. Need a full week of historical snapshots before using trend deltas for additional kill/downsample decisions. | After 7 days of `data/storage_monitor_history.jsonl` entries, compare top daily-growth categories, zero-actionable 7d candidates, disabled-category post-change writes, and active+archive size trajectory. | 2026-05-12 12:00 UTC |
| `ds_storage_autonomous_management_7day_review` | DS storage autonomous-management 7-day review | 2026-05-09 stabilization classified historical broad `kalshi:sports` as `TIER_E_DISPOSABLE`, archived rows to reduce active residence, shortened pressure monitoring to 15 minutes, added pressure-triggered retention starts, and added a >5pp/24h disk-growth alarm. | On 2026-05-16, verify active DB remains within target, WAL stays below 50 MiB outside bulk archive runs, retention and pressure-monitor timers fire at expected cadence, growth-rate alarms surface when applicable, PROTECT_TRADING stays off below HARD_LIMIT, and archive-aware reports still render. | 2026-05-16 12:00 UTC |
| `ds_shadow_continuous_archive_24h_review` | DS continuous archive 24h bounded-state review | Continuous micro-archive reduces between-sweep growth pressure, but the first full day is needed to verify active DB peak, rows moved per tick, lock contention, and 6-hour compaction interaction under normal scanner load. | After 24h of `ds-shadow-continuous-archive.timer`, confirm all ticks are success or lock-busy skips during batch sweep only, active DB stays below warning between compactions, storage monitor direct stats match file stats, and archive-aware reports still render. | 2026-05-06 20:00 UTC |
| `ds_shadow_db_steady_state_review` | DS shadow final DB fix 7-day steady-state review | Broad sports backfill and validated-empty Gemini broad categories were disabled, daily category caps were added, and per-table retention became env-configurable. Main SQLite file bytes may lag row reductions until scheduled compaction. | After 7 days, verify disabled broad paths have zero post-deploy writes, productive per-cell streams still write, daily caps did not block productive paths, active DB direct stat remains below the warning threshold after compaction cycles, and archive-aware reports still reproduce cohort/state metrics. | 2026-05-12 22:00 UTC |
| 2026-05-11 | Spot-age instrumentation diagnostic review | CLOSED with verdict B/no filter. Kalshi crossed the n>=100 trigger with 104 resolved instrumented W/L rows; Gemini had 59 resolved W/L rows and was analyzed in parallel for cross-platform direction. No spot-age bucket survived Bonferroni p<0.003125 or BH FDR; cross-platform direction was inconsistent; no filter deployment recommended. Research: `research/2026-05-11-kalshi-gemini-ds-spot-age-correlation-analysis.md`. Continue passive accumulation; re-run at n>=200 resolved W/L rows per platform or >=10 losses per platform. |
| 2026-05-11 | Gemini DS ETH qty 10 rollback review | CLOSED FAILED. `filter_combined_eth_high_price_qty_10_rollback_pilot` reached 78 resolved, 73W-5L, WR 93.6%, Wilson lower 85.9%, and P&L -$22.77. Loss asymmetry kept breakeven around 96.5%-97.2%. Surgical refinement deployed `DETERMINISTIC_SETTLEMENT_MIN_CUSHION=0.0040` and opened `filter_combined_eth_high_cushion_qty_10_pilot`; no scale-up authorized. Research: `research/2026-05-11-gemini-ds-surgical-or-kill-investigation.md`. |
| 2026-05-11 | Tax ledger adapter and daily ingestion remediation | COMPLETED VIA OPERATOR OVERRIDE. Source-of-truth event layer `v1.0-2026-05-11-override` ingested Kalshi, Gemini, and IBKR 2026 direct source rows; daily `tax-ledger-ingest.timer` enabled; reports generated. Gemini Q1 legacy FIFO-vs-direct gap remains OPEN under `tax_ledger_gemini_q1_2026_reconciliation_resolution`. |
| 2026-05-08 | Gemini DS BTC/ETH high-price 30-resolution review | CLOSED FAILED. `filter_combined_btc_eth_high_price_pilot` reached review at 53 resolved, 51W-2L, Wilson lower 87.2%, and P&L -$3.48. BTC was 34W-2L for -$8.71 while ETH was 17W-0L for +$5.23. Operator approved ETH-only restriction and opened `filter_combined_eth_high_price_pilot`; prior ETH rows are informative only, not inherited. |
| 2026-05-07 | IBKR Release Monitor USTM 2026-05-07 run verification | Closed after the 30-minute post-release window. `shadow_release_monitor` inserted 18 fresh rows for `release_date='2026-05-07'` at 2026-05-07 22:25:01 UTC, actual USTM value 44.1, detection delay 0.09s, 0 mispriced rows, and total theoretical profit $0.00. Readiness reflected the new event, kept USTM cells `METHODOLOGY_REVIEW_REQUIRED_SOURCE_TIMING`, and stayed `live-pilot-ready=0`. A stale auto lock was found and fixed at the source in IBKR commit `1fc7aa5`; the stale runtime lock was removed and readiness now reports `Release Monitor runtime: no_active_auto_runner`. Full-picture reconciliation rendered Gemini OK, Kalshi OK, and IBKR OK with Gemini cash gap $0.00, Kalshi cash gap $0.00, and IBKR hard cash gap $0.00; IBKR DB `quick_check` returned `ok`. |
| 2026-05-07 | Kalshi DS BTC qty 400 per-asset cohort review | CLOSED PASSED. `filter_combined_qty_400_btc_pilot`: 33 resolved, 33W-0L, Wilson lower 89.6%, P&L +$389.36, no daily CB breach. Operator honored EXPANSION_CANDIDATE with the one-parameter BTC qty/cap 400->500 scale. |
| 2026-05-05 | Gemini DS depth-filtered pilot 50-resolution review superseded | Depth-filtered pilot was paused early after dispositive failure: 30 resolved, 16W-14L, BTC 5W-12L, `P(X<=16 | n=30, p=0.90)=3.051e-07`. The pending 50-resolution trigger is no longer applicable unless Eric approves a new bounded redeploy cohort. |
| 2026-05-05 | Gemini DS strict-filter pilot 30-resolution review superseded | Strict filter pilot was closed early at operator direction to start the cleaner Gemini/Kalshi parallel-filter comparison. Final pre-close state by fresh DB query was 4W-0L, +$0.72, n=4 resolved plus 4 IOC-unfilled attempts; any already-open strict-filter positions continue resolving by placement timestamp into the closed cohort. |
| 2026-05-06 | Kalshi 429 post-throttle 24h measurement | Closed overdue verification. Baseline 24h before 2026-05-04 09:00 CDT: 231 429s, avg 9.62/hr, peak 171/hr in one burst. First 24h after trigger: 69 429s, avg 2.88/hr, peak 67/hr in one burst. Current status report: 0 in 1h, 59 in 24h. Throttle is working; no further throttle change warranted. |
| 2026-05-06 | DS expansion DB daily policy archive review superseded | Superseded by the DS archive tier-rotation deployment. Continuous and batch archive health now surface through `ds_shadow_expansion_archives`, `ds_shadow_continuous_archive_24h_review`, and the tier-rotation runbook rather than the old one-off daily policy review. |
| 2026-05-06 | IBKR Weather DS paused-position settlement watch | Closed at 2026-05-06 19:45 CDT when the four 2026-05-05 Weather DS rows (`UHMDW_050526_56_NO`, `UHMDW_050526_60_YES`, `UHMDW_050526_63_YES`, `UHSAT_050526_90_YES`) cleared the broker portfolio snapshot (last seen 19:09:01 CDT, absent from 19:45:01 snapshot). Settled 1W-3L for +$3.00 24h; lifetime DB ledger now +$1.90, broker-truth -$2.50 (gap is BUG_CLASSES #17 partial-fill defect, tracked separately as `ibkr_weather_ds_partial_fill_defect_fix`). Stale-position detector reports `open=0 within=0 candidates=0 confirmed=0` for `ibkr_weather_ds`. Hard reconciliation $0.00 across Gemini/Kalshi/IBKR. Operator question on extending the 4h stale-position buffer is moot for this instance — broker eventually settled at ~12-15h hold without intervention; defer the buffer extension question until and unless a future Weather DS or other paused-strategy instance also persists 10+ hours. |
| Verification | Why deferred | Trigger | Expected action | Status |
| Kalshi MR shadow Kelly statistical comparison | New uncertainty/drawdown-aware Kelly runs as shadow only and needs forward rows before evaluation. | `kalshi_mr_kelly_shadow_comparison` reaches 100+ rows. | Compare actual sizing EV vs shadow Kelly EV; activation only if materially better with no drawdown/CB stress and operator approval. | PENDING |
| Kalshi DS 10->12 cohort decision | The 8->10 cohort must accumulate enough resolved trades after the cap raise. | 8->10 cohort reaches 50 resolved trades. | Use DS cohort tracker to decide ready/still accumulating/revert; no automatic cap change. Estimated 24-48h at current placement rate. | PENDING |
| IBKR Long+Short Kelly activation review | Live sample is below the n>=100 activation gate. | bot_strategy resolved live trades reach 100. | Review inactive Kelly shadow output; activation requires Wilson lower above breakeven, no CB stress, and operator approval. | PENDING |
```

## Recent Decisions
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

---
sha256_without_checksum: [REDACTED:long_hex]
