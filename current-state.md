# Rahm Current State

last_updated_utc: 2026-05-27T17:10:00+00:00
pipeline_heartbeat_utc: 2026-05-27T17:10:00+00:00
generator: Codex generate_current_state.py
workspace_head: 5952a7f

## Trading Bot Runtime
### gemini
- unit: gemini-bot.service
- active: active/running
- pid: 274693
- nrestarts: 0
- active_enter: Wed 2026-05-27 02:35:26 CDT
- reconciliation:
  - Reconciliation: resolved_pnl=$-18386.46 open_cost=$0.60 open_fees=$0.05 recon_adj=$122.87 expected_cash=$17.26 cash_gap=$+0.00 unrealized=-$0.50 [MATCH]
  - ✓ HARD CHECK PASSED — gap $0.00
  - Reconciliation adjustment: $122.87 (auto-computed from exchange balance)
  - Expected cash: $17.26
  - Actual cash (API): $17.26
- selected env:
  - `BLOCKED_ASSETS=WTI,BTC,ETH,SOL,XRP,ZEC,BRENT,COPPER,NGAS`
  - `BTC_FRI_NO_CONTRARIAN_PILOT_ALLOWED_OUTCOMES=no`
  - `BTC_FRI_NO_CONTRARIAN_PILOT_ALLOWED_UTC_DAYS=Fri`
  - `BTC_FRI_NO_CONTRARIAN_PILOT_DAILY_CB=-5`
  - `BTC_FRI_NO_CONTRARIAN_PILOT_LIFETIME_CB=-10`
  - `BTC_FRI_NO_CONTRARIAN_PILOT_MAX_OPEN=2`
  - `BTC_FRI_NO_CONTRARIAN_PILOT_QTY=10`
  - `BTC_QTY=600`
  - `BTC_SAT_NO_CONTRARIAN_PILOT_ALLOWED_OUTCOMES=no`
  - `BTC_SAT_NO_CONTRARIAN_PILOT_ALLOWED_UTC_DAYS=Sat`
  - `BTC_SAT_NO_CONTRARIAN_PILOT_DAILY_CB=-5`
  - `BTC_SAT_NO_CONTRARIAN_PILOT_LIFETIME_CB=-10`
  - `BTC_SAT_NO_CONTRARIAN_PILOT_MAX_OPEN=2`
  - `BTC_SAT_NO_CONTRARIAN_PILOT_QTY=10`
  - `BTC_SUN_NO_CONTRARIAN_PILOT_ALLOWED_OUTCOMES=no`
  - `BTC_SUN_NO_CONTRARIAN_PILOT_ALLOWED_UTC_DAYS=Sun`
  - `BTC_SUN_NO_CONTRARIAN_PILOT_DAILY_CB=-5`
  - `BTC_SUN_NO_CONTRARIAN_PILOT_LIFETIME_CB=-10`
  - `BTC_SUN_NO_CONTRARIAN_PILOT_MAX_OPEN=2`
  - `BTC_SUN_NO_CONTRARIAN_PILOT_QTY=10`
  - `BTC_THU_NO_CONTRARIAN_PILOT_ALLOWED_OUTCOMES=no`
  - `BTC_THU_NO_CONTRARIAN_PILOT_ALLOWED_UTC_DAYS=Thu`
  - `BTC_THU_NO_CONTRARIAN_PILOT_DAILY_CB=-5`
  - `BTC_THU_NO_CONTRARIAN_PILOT_LIFETIME_CB=-10`
  - `BTC_THU_NO_CONTRARIAN_PILOT_MAX_OPEN=2`
  - `BTC_THU_NO_CONTRARIAN_PILOT_QTY=10`
  - `BTC_TUE_NO_CONTRARIAN_PILOT_ALLOWED_OUTCOMES=no`
  - `BTC_TUE_NO_CONTRARIAN_PILOT_ALLOWED_UTC_DAYS=Tue`
  - `BTC_TUE_NO_CONTRARIAN_PILOT_DAILY_CB=-5`
  - `BTC_TUE_NO_CONTRARIAN_PILOT_LIFETIME_CB=-10`
  - `BTC_TUE_NO_CONTRARIAN_PILOT_MAX_OPEN=2`
  - `BTC_TUE_NO_CONTRARIAN_PILOT_QTY=10`
  - `CONTRARIAN_MAX_EXPOSURE=500`
  - `CONTRARIAN_QTY=100`
  - `CRYPTO_BTC_LATE_HIGH_CUSHION_YES_DS_PILOT_ENABLED=false`
  - `CRYPTO_BTC_LATE_HIGH_CUSHION_YES_DS_PILOT_KILL_SWITCH=/home/kingeric/gemini_prediction_bot/KILL_CRYPTO_BTC_LATE_HIGH_CUSHION_YES_DS_PILOT`
  - `CRYPTO_BTC_LATE_HIGH_CUSHION_YES_DS_PILOT_START=2026-05-23 14:28:00`
  - `CRYPTO_BTC_LOW_MID_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_BTC_LOW_MID_NO_DS_PILOT_KILL_SWITCH=/home/kingeric/gemini_prediction_bot/KILL_CRYPTO_BTC_LOW_MID_NO_DS_PILOT`
  - `CRYPTO_BTC_LOW_MID_NO_DS_PILOT_START=2026-05-23 13:47:43`
  - `CRYPTO_BTC_MID_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_BTC_MID_NO_DS_PILOT_KILL_SWITCH=/home/kingeric/gemini_prediction_bot/KILL_CRYPTO_BTC_MID_NO_DS_PILOT`
  - `CRYPTO_BTC_MID_NO_DS_PILOT_START=2026-05-23 13:38:09`
  - `CRYPTO_BTC_MID_WEEKDAY_YES_DS_PILOT_ENABLED=false`
  - `CRYPTO_BTC_MID_WEEKDAY_YES_DS_PILOT_KILL_SWITCH=/home/kingeric/gemini_prediction_bot/KILL_CRYPTO_BTC_MID_WEEKDAY_YES_DS_PILOT`
  - `CRYPTO_BTC_MID_WEEKDAY_YES_DS_PILOT_START=2026-05-23 13:12:31`
  - `CRYPTO_BTC_UTC12_YES_DS_PILOT_ENABLED=false`
  - `CRYPTO_BTC_UTC12_YES_DS_PILOT_KILL_SWITCH=/home/kingeric/gemini_prediction_bot/KILL_CRYPTO_BTC_UTC12_YES_DS_PILOT`
  - `CRYPTO_BTC_UTC12_YES_DS_PILOT_START=2026-05-23 12:59:58`
  - `CRYPTO_BTC_UTC18_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_BTC_UTC18_NO_DS_PILOT_KILL_SWITCH=/home/kingeric/gemini_prediction_bot/KILL_CRYPTO_BTC_UTC18_NO_DS_PILOT`
  - `CRYPTO_BTC_UTC18_NO_DS_PILOT_START=2026-05-23 12:25:00`
  - `CRYPTO_ETH_LATE_HIGH_CUSHION_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_ETH_LATE_HIGH_CUSHION_NO_DS_PILOT_KILL_SWITCH=/home/kingeric/gemini_prediction_bot/KILL_CRYPTO_ETH_LATE_HIGH_CUSHION_NO_DS_PILOT`
  - `CRYPTO_ETH_LATE_HIGH_CUSHION_NO_DS_PILOT_START=2026-05-23 14:45:00`
  - `CRYPTO_ETH_LATE_HIGH_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_ETH_LATE_HIGH_NO_DS_PILOT_KILL_SWITCH=/home/kingeric/gemini_prediction_bot/KILL_CRYPTO_ETH_LATE_HIGH_NO_DS_PILOT`
  - `CRYPTO_ETH_LATE_HIGH_NO_DS_PILOT_START=2026-05-23 12:40:00`
  - `CRYPTO_ETH_LOWER_LATE_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_ETH_LOWER_LATE_NO_DS_PILOT_KILL_SWITCH=/home/kingeric/gemini_prediction_bot/KILL_CRYPTO_ETH_LOWER_LATE_NO_DS_PILOT`
  - `CRYPTO_ETH_LOWER_LATE_NO_DS_PILOT_START=2026-05-23 14:06:00`
  - `CRYPTO_ETH_LOWER_LATE_YES_DS_PILOT_ENABLED=false`
  - `CRYPTO_ETH_LOWER_LATE_YES_DS_PILOT_KILL_SWITCH=/home/kingeric/gemini_prediction_bot/KILL_CRYPTO_ETH_LOWER_LATE_YES_DS_PILOT`
  - `CRYPTO_ETH_LOWER_LATE_YES_DS_PILOT_START=2026-05-23 14:13:00`
  - `CRYPTO_ETH_MIDDAY_MID_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_ETH_MIDDAY_MID_NO_DS_PILOT_KILL_SWITCH=/home/kingeric/gemini_prediction_bot/KILL_CRYPTO_ETH_MIDDAY_MID_NO_DS_PILOT`
  - `CRYPTO_ETH_MIDDAY_MID_NO_DS_PILOT_START=2026-05-23 14:57:00`
  - `CRYPTO_FINAL_HIGH_PRICE_ETH_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_FINAL_HIGH_PRICE_ETH_NO_DS_PILOT_KILL_SWITCH=/home/kingeric/gemini_prediction_bot/KILL_CRYPTO_FINAL_HIGH_PRICE_ETH_NO_DS_PILOT`
  - `CRYPTO_FINAL_HIGH_PRICE_ETH_NO_DS_PILOT_START=2026-05-23 03:06:00`
  - `CRYPTO_FINAL_LOW_PRICE_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_FINAL_LOW_PRICE_NO_DS_PILOT_KILL_SWITCH=/home/kingeric/gemini_prediction_bot/KILL_CRYPTO_FINAL_LOW_PRICE_NO_DS_PILOT`
  - `CRYPTO_FINAL_LOW_PRICE_NO_DS_PILOT_START=2026-05-23 02:51:17`
  - `CRYPTO_FINAL_MID_PRICE_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_FINAL_MID_PRICE_NO_DS_PILOT_KILL_SWITCH=/home/kingeric/gemini_prediction_bot/KILL_CRYPTO_FINAL_MID_PRICE_NO_DS_PILOT`
  - `CRYPTO_FINAL_MID_PRICE_NO_DS_PILOT_START=2026-05-23 06:03:00`
  - `CRYPTO_FINAL_ULTRA_LOW_BTC_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_FINAL_ULTRA_LOW_BTC_NO_DS_PILOT_KILL_SWITCH=/home/kingeric/gemini_prediction_bot/KILL_CRYPTO_FINAL_ULTRA_LOW_BTC_NO_DS_PILOT`
  - `CRYPTO_FINAL_ULTRA_LOW_BTC_NO_DS_PILOT_START=2026-05-23 06:08:00`
  - `CRYPTO_LATE_LOW_PRICE_NO_DS_PILOT_ENABLED=false`
- strategy/cohort excerpts:
  - Live/tracked resolved P&L: +$0.02 across 6 resolved trades
  - Full broker-resolved P&L (all historical strategies): -$18,386.46 across 2001 resolved trades
  - 24h P&L: +$0.14 (0W-0L resolved, 8 placed)
  - Today's P&L: +$0.14
  - ✓ Weekday Crypto MR: +$0.02 | 0W-0L | open: 0 | armed; cohort start 2026-05-24T01:26:32Z; early exits 3
  - Permanently killed strategies (3):
  - ✗ [Gemini] Mean Reversion: KILLED 2026-05-21 | -$913.55 | 251W-45L | lifetime breaker breached; Kelly 0.625x rollback failed; no revival authorized
  - ✗ [Gemini] Crypto DS micro-pilots: KILLED 2026-05-23 | -$14.03 | 1W-2L | source-blocked after GRR-KAIKO vs Gemini spot mismatch; no open positions
  - ✗ [Gemini] Contrarian cell micro-pilots: KILLED 2026-05-24 | -$3.95 | 0W-4L | paused after executable evidence failed; spillover positions resolved
  - Next decision gate: 2026-05-27T18:30:00+00:00 - direct-index DS next resolution (151 rows/6 events unresolved | current qty5: 100 rows/6 events unresolved | micro qty1: 51 rows/6 events unresolved) resolution checks; no live expansion before event-collapsed results
  - Status: ⚠ Warnings: mean reversion lifetime breaker tripped | deterministic settlement killed | crypto DS micro-pilots source-blocked | contrarian pilots killed
  - [2.1] Mean Reversion (YES-only)  |  Status: PERMANENT_KILL 2026-05-21 (lifetime breaker breached; Kelly 0.625x rollback failed; no revival authorized)
  - Record: 251W-45L (85%) | P&L: -$913.55
  - Today's P&L: +$0.00
  - Lifetime breaker ledger (reset_at 2026-05-13 19:39:42-0500): -$4,454.27 / -$3,000.00 limit | ❌ BREACHED
  - Blocked candidates today: 0 | lifetime: 0 | shadow resolved: 0 | hypothetical P&L +$0.00
  - Captured rows today: 0 | lifetime: 0 | resolved: 0 | blocked-wins: 0 | blocked-losses: 0
  - Hypothetical block P&L: +$0.00 (positive = guard would have helped) | activation review at n>=30 independent events
  - Multiplier: 0.625 | start 2026-05-13 19:39:42-0500 | cohort gemini_mr_kelly_0.625x_rollback_pilot
  - Resolved post-deploy: 16/50 | 5W-11L (31.2%) | P&L -$4,454.27 | ACCUMULATING

### ibkr
- unit: ibkr-scan-loop.service
- active: active/running
- pid: 357609
- nrestarts: 0
- active_enter: Wed 2026-05-27 06:00:44 CDT
- reconciliation:
  - Formula: expected cash/NLV uses broker_ledger realized P&L + latest Flex statement snapshot
  - ✓ HARD CHECK PASSED — cash gap $0.00
  - Expected cash = deposits + realized + market data fees + incentive income - cost = $1863.15
  - Actual cash (API): $1863.15
  - Raw cash gap before live delta adjustment: $0.00
  - Cash gap: $0.00
- selected env:
  - `DETERMINISTIC_SETTLEMENT_WEATHER_ENABLED=true`
  - `DETERMINISTIC_SETTLEMENT_WEATHER_KILL_SWITCH=/home/kingeric/.openclaw/workspace/ibkr_forecast_bot/KILL_DETERMINISTIC_SETTLEMENT_WEATHER`
  - `FX_CONTRARIAN_LOW_PRICE_DAILY_CB=-25.00`
  - `FX_CONTRARIAN_LOW_PRICE_LIFETIME_CB=-75.00`
  - `FX_CONTRARIAN_LOW_PRICE_MAX_OPEN=1`
  - `FX_CONTRARIAN_LOW_PRICE_QTY=5`
  - `LIVE_QTY30_LONG_FX_COHORT_ENABLED=true`
  - `LIVE_QTY30_LONG_FX_DAILY_CB=-50`
  - `LIVE_QTY30_LONG_FX_LIFETIME_CB=-150`
  - `LIVE_QTY30_LONG_FX_MAX_EXPIRY_HOURS=168`
  - `LIVE_QTY30_LONG_FX_MAX_OPEN=10`
  - `LIVE_QTY30_LONG_FX_MIN_EXPIRY_HOURS=48`
  - `LIVE_QTY30_LONG_FX_PER_POSITION=30`
  - `LIVE_QTY30_LONG_FX_UNDERLIERS=JPUSD,USEUR,USGBP,USCAD`
  - `MAX_EXPOSURE=2000`
  - `MAX_PER_UNDERLIER_DOLLAR_CAP=900`
  - `QTY_PER_POSITION=150`
  - `SHORT_FX_DAILY_CB=-300`
  - `SHORT_FX_QTY150_COHORT_START=2026-05-22T22:45:49Z`
- strategy/cohort excerpts:
  - Lifetime P&L: +$8.95 across 764 resolved trades
  - 24h P&L: +$0.00 (0W-0L resolved, 0 placed)
  - SELF-MANAGED ACTIVITY (last 24h):
  - Decisions: Weather DS post-fix pilot is active for UHBNA lt2/UHBNA 2-5/UHPHX 2-5/UHSFO 5-8/UHSFO ge8 under qty 10 and pre-committed rollback gates; FX Contrarian Low Price is paused to new entries in source after live and blocked-shadow losses; existing open rows resolve naturally; Spread Capture buy-only pilot is paused to new entries after 1h lifetime evidence for WEATHER/10-20c/<50c/buy_only turned negative; existing filled rows resolve naturally; no autonomous scaling decision has met evidence gate.
  - Pilots: Weather DS cohort since 2026-05-16 20:55:30: 4 placed, 4 resolved, 0 open, $0.00 open cost, latest=2026-05-19 22:34:11.
  - Cohort gates: Weather DS scale review needs each of 5 live cells at n>=15 forward resolved; aggregate resolved 4, aggregate remaining at least 71; no scale action due.
  - [2.1] BOT STRATEGY FAMILY — split by cohort:
  - Aggregate bot_strategy since 2026-05-03: 47 placed | 47 resolved (47W-0L) | P&L +$136.19 | avg/resolved +$2.90 | underliers USGBP=13, JPUSD=12, USEUR=12, USCAD=5, USGP=5
  - [bot_strategy_short_fx_qty150] Short-FX qty-150 cohort: 0 placed | 0 resolved (0W-0L) | P&L +$0.00 | open 0 | avg qty 0.0 | avg cost $0.00 | daily CB +$0.00 / $-300.00 | rollback ARMED
  - Qty-150 rollback gates: 2L/10=0/2 | 3L/30=0/3 | daily_pre_n20=+$0.00/-$300.00 (n=0) | lifetime=+$0.00/-$200.00 | max_single_loss=+$0.00/-$130.00 | breaches=none
  - [bot_strategy_short_fx_qty100] Short-FX cohort: 4 placed | 4 resolved (4W-0L) | P&L +$18.39 | open 0 | avg qty 66.8 | avg cost $62.15 | cap-limited 2 | daily CB +$0.00 / $-300.00
  - Qty-100 blocked shadow: 465 rows | 78 symbols | 7 resolved (7W-0L) | P&L +$13.22 | avg qty 127.4 | latest 2026-05-27 12:01:59
  - Sizing blocked shadow: 12 rows | 12 symbols | 0 resolved (0W-0L) | P&L +$0.00 | avg qty 100.0 | latest 2026-05-18 18:50:13
  - [bot_strategy_long_fx_qty30] Long-FX cohort: status PAUSED_EMPTY_SURFACE (paused_empty_surface_ec_2026_05_22) | 0 placed | 0 resolved (0W-0L) | P&L +$0.00 | open 0 | avg qty 0.0 | avg cost $0.00 | daily CB +$0.00 / $-50.00 | lifetime CB +$0.00 / $-150.00
  - [bot_strategy_legacy_qty60] Legacy pre-split cohort: 88 placed | 85 resolved (82W-3L) | P&L +$119.01 | preserved for history, not a current expansion signal
  - Entry: categories FX only | cells JPUSD/NO 24-60h, USCAD/YES 24-60h, USEUR/YES 24-60h, USGBP/YES 48-60h | bid $0.85-$0.95 | min expiry 24h | max expiry 60h | max spread $0.10 | order LIMIT at ASK
  - Qty-150 cohort: START 2026-05-22T22:45:49Z | active qty 150 | rollback-to-100 flag absent | pre-committed gates 2L/10, 3L/30, daily CB -$300 before n=20, lifetime CB -$200, single loss > $130
  - Qty-100 cohort: START 2026-05-17T18:48:00-05:00 | preserved as prior sizing measurement | prior qty-60 rows preserved
  - Qty-30 long-FX cohort: PAUSED (paused_empty_surface_ec_2026_05_22) | START 2026-05-22T09:33:00-05:00 | underliers JPUSD/USCAD/USEUR/USGBP | expiry 48-168h | qty 30 | max open 10 | CB daily $-50 lifetime $-150 | reactivation requires fresh venue contracts plus operator decision | USCAD/NO excluded
  - [bot_strategy_ibkr_econ_pilot] ECONOMICS pilot: 0 placed | 0 resolved (0W-0L) | P&L +$0.00 | open 0 | open exposure $0.00/$50.00 | lifetime exposure tracked $0.00 / cap UNLIMITED | kill switch absent | breaches none

### kalshi
- unit: kalshi-bot.service
- active: active/running
- pid: 4070930
- nrestarts: 0
- active_enter: Tue 2026-05-26 09:35:46 CDT
- reconciliation:
  - Reconciliation: resolved_pnl=$-1793.78 open_cost=$0.00 open_fees=$0.00 recon_adj=$240.06 expected_cash=$1036.83 cash_gap=$+0.00 unrealized=$+90.55 [MATCH]
  - ✓ HARD CHECK PASSED — gap $0.00
  - Reconciliation adjustment: $240.06 (auto-computed from exchange balance)
  - Expected cash: $1036.83
  - Actual cash (API): $1036.83
- selected env:
  - `BTC_DS_PRICE_CEILING_H5_THRESHOLD=0.97`
  - `BTC_DS_PRICE_CEILING_H6_THRESHOLD=0.95`
  - `BTC_DS_PRICE_CEILING_SHADOW_ENABLED=true`
  - `BTC_DS_PRICE_CEILING_SHADOW_START=2026-05-16 10:12:30-0500`
  - `DETERMINISTIC_SETTLEMENT_ALLOWED_ASSETS=ETH`
  - `DETERMINISTIC_SETTLEMENT_BTC_KILL_SWITCH=/home/kingeric/kalshi_favorites_bot/KILL_DETERMINISTIC_SETTLEMENT_BTC`
  - `DETERMINISTIC_SETTLEMENT_DAILY_CB=-600`
  - `DETERMINISTIC_SETTLEMENT_DAILY_RESET_AT=2026-05-13 12:52:04-05:00`
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
  - `DETERMINISTIC_SETTLEMENT_LIFETIME_CB=-1800`
  - `DETERMINISTIC_SETTLEMENT_LIFETIME_RESET_AT=2026-05-16 11:42:22-0500`
  - `DETERMINISTIC_SETTLEMENT_MAX_ASSET_HOUR_OPEN=4`
  - `DETERMINISTIC_SETTLEMENT_MAX_EXPOSURE=999999`
  - `DETERMINISTIC_SETTLEMENT_MAX_OPEN=8`
  - `DETERMINISTIC_SETTLEMENT_MIN_NET_EDGE=0.0`
  - `DETERMINISTIC_SETTLEMENT_PER_TRADE_DOLLAR_CAP=225`
  - `DETERMINISTIC_SETTLEMENT_QTY=225`
  - `DETERMINISTIC_SETTLEMENT_THRESHOLD_PCT=0.0007`
  - `DETERMINISTIC_SETTLEMENT_WINDOW_MINUTES=30`
  - `DS_KALSHI_CLUSTER_CAP_START=2026-05-13 13:29:46-05:00`
  - `DS_KALSHI_CONTRACT_HOUR_MAX=3`
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
  - `DS_KALSHI_PER_TRADE_DOLLAR_CAP_BTC=0`
  - `DS_KALSHI_PER_TRADE_DOLLAR_CAP_ETH=400`
  - `DS_KALSHI_QTY_225_BTC_POST_ROLLBACK_START=2026-05-16 08:53:26-0500`
  - `DS_KALSHI_QTY_275_ETH_START=2026-05-08 14:35:34`
  - `DS_KALSHI_QTY_300_ETH_START=2026-05-11 17:55:04`
  - `DS_KALSHI_QTY_400_BTC_CVAR_START=2026-05-11 00:52:09`
  - `DS_KALSHI_QTY_400_ETH_PILOT_START=2026-05-13 21:41:21-0500`
  - `DS_KALSHI_QTY_400_ETH_POST_ROLLBACK_START=2026-05-21T18:00:00+00:00`
  - `DS_KALSHI_QTY_500_BTC_REDEPLOY_START=2026-05-11 17:55:04`
  - `DS_KALSHI_QTY_500_BTC_START=2026-05-07 13:35:31`
  - `DS_KALSHI_QTY_500_ETH_PILOT_START=2026-05-20 13:25:29-0500`
  - `DS_KALSHI_QTY_600_BTC_POST_ROLLBACK_START=2026-05-13 12:52:04-05:00`
  - `DS_KALSHI_QTY_600_BTC_REDEPLOY_START=2026-05-12 15:19:03`
  - `DS_KALSHI_QTY_600_BTC_ROLLBACK_START=2026-05-10 19:06:00`
  - `DS_KALSHI_QTY_600_BTC_START=2026-05-09 13:56:56`
  - `DS_KALSHI_QTY_700_BTC_REDEPLOY_START=2026-05-13 10:19:42-05:00`
  - `DS_KALSHI_QTY_700_BTC_START=2026-05-10 03:35:49`
  - `DS_KALSHI_QTY_BTC=0`
  - `DS_KALSHI_QTY_ETH=400`
  - `FAV_QTY=100`
  - `KALSHI_MR_ALLOWED_CELLS_START=2026-05-07 20:20:23`
  - `KALSHI_MR_INDEX_SETTLEMENT_HOUR_CAP=4`
  - `KALSHI_MR_INDEX_UNDERLIER_EVENT_CAP=2`
  - `KALSHI_MR_WEATHER_LOW_YES_CAP_START=2026-05-05 19:23:46`
  - `KALSHI_MR_WEATHER_LOW_YES_COST_CAP=0`
- strategy/cohort excerpts:
  - Lifetime P&L: -$1,793.78 across 3110 resolved trades
  - 24h P&L: +$41.97 (23W-3L resolved, 28 placed)
  - Status: ⚠ Warnings: deterministic settlement btc kill switch | deterministic settlement fx kill switch | deterministic settlement index kill switch | ds low price no pilot kill switch | kalshi ds btc moderate yes kill switch | ladder coherence sniper kill switch | ladder sniper v2 kill switch | ladder sniper v2.dt t3 archive 1779388145 kill switch | ladder sniper v2.dv archive 1779424356 kill switch | longshot kill switch | longshot fading kill switch | maker kill switch | mean reversion kill switch | moderate favorites kill switch
  - Record: 358W-58L (86%) | P&L: -$744.35
  - Status: KILLED 2026-05-17 (KILL_MEAN_REVERSION)
  - Kill reason: post-cutoff allowed cohort -$730.69; 84.2% nonzero WR vs 91.0% breakeven
  - ✓ Weather-high blocked (80% WR, -$930 lifetime)
  - ✓ BTC blocked (53 resolved, -$173 lifetime; tail-loss asymmetry)
  - ✓ ETH fully blocked from MR (16W-2L, -$258 lifetime; tail-loss asymmetry)
  - ✓ WEATHER_LOW fully blocked from MR (29W-4L, -$678.44 lifetime; loss-asymmetry on both sides)
  - ✓ SOL fully blocked from MR (30W-6L, -$109.04 lifetime; tail-loss asymmetry)
  - 24h: 0 placed | 0W-0L resolved | P&L +$0.00
  - Forward allowed-cell tracker: start 2026-05-07 20:20:23 UTC | 33W-6L (84.6%) | P&L $-668.39 | open 0 ($0.00 cost)
  - WEATHER_LOW YES cap pilot: 0W-0L (0%) | P&L +$0.00 | open 0 ($0.00) | blocks 6/6 attempts | review 0/30 resolved
  - 24h resolved by hour: morning 0-10 CDT 0W-0L (+$0.00) | afternoon 15-20 CDT 0W-0L (+$0.00)
  - Eligible in 4-8h band (would be blocked): observed 13 | resolved 11 | WR 81.8% | P&L without block -$6.26
  - Eligible outside 4-8h band (would still place): observed 23 | resolved 23 | WR 87.0% | P&L +$67.37
  - Verdict: keep current behavior; blocking 4-8h candidates would have hurt P&L
  - In preferred range ($0.75-$0.85): observed 20 | resolved 18 | WR 77.8% | P&L -$26.71
  - Outside preferred range (current live band): observed 16 | resolved 16 | WR 93.8% | P&L +$87.82
  - [2.3D] Ladder Coherence Sniper Micro-Pilot
  - [2.3E] Kalshi Ladder Sniper V2 (Redesigned Execution)
  - Cohort start: 2026-05-17 16:34:42+0000 | Strategy identity: ladder_sniper_v2
  - [2.3G] Kalshi Ladder Sniper V3 (Maker-Side Dry-Run Candidate)
  - BTC MODERATE-FAVORITE YES DS PILOT (FK_2026_05_26, LIVE):
  - Strategy: bot_strategy_kalshi_ds_btc_moderate_favorite_yes_pilot

## Storage State
- DATABASE STORAGE HEALTH
-   Overall status: GREEN / TARGET
-   Disk: 412.19 GiB used / 936.79 GiB total (44.0%), 476.94 GiB free
-   Envelope: TARGET 50.0%, WARN 65.0%, CRITICAL 75.0%, HARD_LIMIT 85.0%
-   DS storage: active 0.87 GiB (state TARGET), hot 27.98 GiB, warm 1.04 GiB, cold 0.00 GiB, archive_state TARGET, total 29.92 GiB (3.2% of disk)
-   Archive sidecars: OK
-   Retention engine: last=2026-05-27T12:17:00+00:00 status=OK dry_run=False rows_selected=0 rows_archived=0 rows_pruned=0
-   Archive compression: status=OK actions=0 warm_days=7 min_file_mb=100
-   Tier rotation: last=2026-05-27T12:17:00+00:00 status=OK actions=0
-   Autonomous maintenance: last=2026-05-25T20:49:44+00:00 status=OK backups=5/5 integrity_failures=0 drift_flags=0
-   PROTECT_TRADING mode: NO
-   TOP_RISK: disk_used_pct grew 10.9pp over 24h

## Timers
```
NEXT                            LEFT LAST                              PASSED UNIT                                                               ACTIVATES
Wed 2026-05-27 12:11:30 CDT    473ms Wed 2026-05-27 12:11:00 CDT      29s ago gemini-cushion-ds-scanner.timer                                    gemini-cushion-ds-scanner.service
Wed 2026-05-27 12:11:30 CDT    525ms Wed 2026-05-27 12:10:30 CDT      59s ago gemini-ds-index-parity.timer                                       gemini-ds-index-parity.service
Wed 2026-05-27 12:11:42 CDT      12s Wed 2026-05-27 11:56:42 CDT    14min ago gemini-ds-source-parity.timer                                      gemini-ds-source-parity.service
Wed 2026-05-27 12:11:49 CDT      20s Wed 2026-05-27 12:10:49 CDT      39s ago gemini-liquidity-rewards-scanner.timer                             gemini-liquidity-rewards-scanner.service
Wed 2026-05-27 12:11:51 CDT      21s Wed 2026-05-27 12:10:51 CDT      38s ago gemini-two-leg-scanner.timer                                       gemini-two-leg-scanner.service
Wed 2026-05-27 12:11:51 CDT      21s Wed 2026-05-27 12:10:51 CDT      38s ago ibkr-scan-loop-watchdog.timer                                      ibkr-scan-loop-watchdog.service
Wed 2026-05-27 12:12:00 CDT      30s Wed 2026-05-27 12:11:00 CDT      29s ago cushion-ds-multi-series-scanner.timer                              cushion-ds-multi-series-scanner.service
Wed 2026-05-27 12:12:08 CDT      39s Wed 2026-05-27 12:02:06 CDT     9min ago ds-shadow-continuous-archive.timer                                 ds-shadow-continuous-archive.service
Wed 2026-05-27 12:12:49 CDT 1min 20s Wed 2026-05-27 12:07:49 CDT 3min 39s ago gemini-maker-fill-simulator.timer                                  gemini-maker-fill-simulator.service
Wed 2026-05-27 12:12:55 CDT 1min 26s Wed 2026-05-27 12:07:55 CDT 3min 33s ago gemini-categorical-scanner.timer                                   gemini-categorical-scanner.service
Wed 2026-05-27 12:12:55 CDT 1min 26s Wed 2026-05-27 12:07:55 CDT 3min 33s ago gemini-fp-orderbook-capture.timer                                  gemini-fp-orderbook-capture.service
Wed 2026-05-27 12:14:16 CDT 2min 46s Wed 2026-05-27 12:07:56 CDT 3min 33s ago gemini-reward-post-only-safety.timer                               gemini-reward-post-only-safety.service
Wed 2026-05-27 12:15:00 CDT 3min 30s Wed 2026-05-27 12:00:00 CDT    11min ago cushion-ds-multi-series-resolver.timer                             cushion-ds-multi-series-resolver.service
Wed 2026-05-27 12:15:00 CDT 3min 30s Wed 2026-05-27 11:15:00 CDT    56min ago gemini-btc-lowband-mr-first-resolution-verifier.timer              gemini-btc-lowband-mr-first-resolution-verifier.service
Wed 2026-05-27 12:15:00 CDT 3min 30s Wed 2026-05-27 12:00:00 CDT    11min ago gemini-cushion-ds-resolver.timer                                   gemini-cushion-ds-resolver.service
Wed 2026-05-27 12:19:06 CDT     7min Wed 2026-05-27 11:18:57 CDT    52min ago macro-release-resolver.timer                                       macro-release-resolver.service
Wed 2026-05-27 12:19:22 CDT     7min Wed 2026-05-27 12:04:22 CDT     7min ago ds-storage-pressure-monitor.timer                                  ds-storage-pressure-monitor.service
Wed 2026-05-27 12:20:00 CDT     8min Wed 2026-05-27 11:20:00 CDT    51min ago gemini-zec-legacy-favorites-active-window-verifier.timer           gemini-zec-legacy-favorites-active-window-verifier.service
Wed 2026-05-27 12:20:00 CDT     8min Wed 2026-05-27 11:20:00 CDT    51min ago gemini-zec-thursday-high-price-active-window-verifier.timer        gemini-zec-thursday-high-price-active-window-verifier.service
Wed 2026-05-27 12:21:08 CDT     9min Wed 2026-05-27 12:11:08 CDT      21s ago ibkr-yes-no-complementarity-scanner.timer                          ibkr-yes-no-complementarity-scanner.service
Wed 2026-05-27 12:22:12 CDT    10min Wed 2026-05-27 11:52:12 CDT    19min ago ds-storage-monitor.timer                                           ds-storage-monitor.service
Wed 2026-05-27 12:25:00 CDT    13min Wed 2026-05-27 12:10:00 CDT 1min 29s ago gemini-categorical-resolver.timer                                  gemini-categorical-resolver.service
Wed 2026-05-27 12:26:19 CDT    14min Wed 2026-05-27 11:24:59 CDT    46min ago consensus-tracking-resolver.timer                                  consensus-tracking-resolver.service
Wed 2026-05-27 12:30:00 CDT    18min Wed 2026-05-27 11:30:00 CDT    41min ago gemini-direct-index-ds-first-resolution-verifier.timer             gemini-direct-index-ds-first-resolution-verifier.service
Wed 2026-05-27 12:30:00 CDT    18min Wed 2026-05-27 11:30:00 CDT    41min ago gemini-sol-weekend-mr-first-resolution-verifier.timer              gemini-sol-weekend-mr-first-resolution-verifier.service
Wed 2026-05-27 12:34:18 CDT    22min Wed 2026-05-27 11:33:02 CDT    38min ago moderate-favorites-unr-resolver.timer                              moderate-favorites-unr-resolver.service
Wed 2026-05-27 12:35:00 CDT    23min Wed 2026-05-27 11:35:00 CDT    36min ago gemini-mr-profit-watchlist-first-resolution-verifier.timer         gemini-mr-profit-watchlist-first-resolution-verifier.service
Wed 2026-05-27 12:35:00 CDT    23min Wed 2026-05-27 11:35:00 CDT    36min ago gemini-weekday-mr-breakeven-margin-first-resolution-verifier.timer gemini-weekday-mr-breakeven-margin-first-resolution-verifier.service
Wed 2026-05-27 12:35:00 CDT    23min Wed 2026-05-27 11:35:00 CDT    36min ago gemini-weekday-mr-excluded-asset-first-resolution-verifier.timer   gemini-weekday-mr-excluded-asset-first-resolution-verifier.service
Wed 2026-05-27 12:35:00 CDT    23min Wed 2026-05-27 11:35:00 CDT    36min ago gemini-weekday-mr-near-miss-first-resolution-verifier.timer        gemini-weekday-mr-near-miss-first-resolution-verifier.service
Wed 2026-05-27 12:38:37 CDT    27min Wed 2026-05-27 11:37:56 CDT    33min ago moderate-favorites-weather-resolver.timer                          moderate-favorites-weather-resolver.service
Wed 2026-05-27 12:38:58 CDT    27min Wed 2026-05-27 11:38:24 CDT    33min ago ladder-coherence-two-leg-resolver.timer                            ladder-coherence-two-leg-resolver.service
Wed 2026-05-27 12:46:52 CDT    35min Wed 2026-05-27 11:45:03 CDT    26min ago moderate-favorites-finance-resolver.timer                          moderate-favorites-finance-resolver.service
Wed 2026-05-27 12:51:18 CDT    39min Wed 2026-05-27 11:49:46 CDT    21min ago spread-capture-weather-resolver.timer                              spread-capture-weather-resolver.service
Wed 2026-05-27 12:58:02 CDT    46min Wed 2026-05-27 11:56:37 CDT    14min ago ladder-coherence-resolver.timer                                    ladder-coherence-resolver.service
Wed 2026-05-27 13:03:24 CDT    51min Wed 2026-05-27 12:02:23 CDT     9min ago moderate-favorites-economics-resolver.timer                        moderate-favorites-economics-resolver.service
Wed 2026-05-27 13:05:00 CDT    53min Wed 2026-05-27 12:05:00 CDT     6min ago gemini-mr-profit-watchlist-first-target-verifier.timer             gemini-mr-profit-watchlist-first-target-verifier.service
Wed 2026-05-27 13:10:00 CDT    58min Wed 2026-05-27 12:10:00 CDT 1min 29s ago gemini-mr-profit-watchlist-btc-1-4h-target-verifier.timer          gemini-mr-profit-watchlist-btc-1-4h-target-verifier.service
Wed 2026-05-27 13:11:23 CDT    59min Wed 2026-05-27 12:09:49 CDT 1min 40s ago spread-capture-resolver.timer                                      spread-capture-resolver.service
Wed 2026-05-27 13:17:00 CDT  1h 5min Wed 2026-05-27 07:17:00 CDT 4h 54min ago ds-shadow-retention-engine.timer                                   ds-shadow-retention-engine.service
Wed 2026-05-27 14:11:29 CDT 1h 59min Wed 2026-05-27 10:11:29 CDT  2h 0min ago deal-scout.timer                                                   deal-scout.service
Wed 2026-05-27 14:17:00 CDT  2h 5min Wed 2026-05-27 08:17:00 CDT 3h 54min ago ds-contract-universe-refresh.timer                                 ds-contract-universe-refresh.service
Wed 2026-05-27 14:40:11 CDT 2h 28min Wed 2026-05-27 11:40:11 CDT    31min ago db-auto-vacuum.timer                                               db-auto-vacuum.service
Wed 2026-05-27 15:00:00 CDT 2h 48min Wed 2026-05-27 12:00:00 CDT    11min ago snap.firmware-updater.firmware-notifier.timer                      snap.firmware-updater.firmware-notifier.service
Wed 2026-05-27 15:24:20 CDT 3h 12min Wed 2026-05-27 09:24:20 CDT 2h 47min ago ds-shadow-archive.timer                                            ds-shadow-archive.service
Wed 2026-05-27 16:27:25 CDT 4h 15min Wed 2026-05-27 10:27:25 CDT 1h 44min ago gemini-db-retention.timer                                          gemini-db-retention.service
Wed 2026-05-27 17:35:09 CDT 5h 23min Wed 2026-05-27 11:35:09 CDT    36min ago ds-shadow-db-maintenance.timer                                     ds-shadow-db-maintenance.service
Wed 2026-05-27 17:57:22 CDT 5h 45min Tue 2026-05-26 17:57:22 CDT      18h ago gemini-fp-retention.timer                                          gemini-fp-retention.service
Thu 2026-05-28 04:30:00 CDT      16h Wed 2026-05-27 04:30:03 CDT       7h ago tax-ledger-ingest.timer                                            tax-ledger-ingest.service
Thu 2026-05-28 04:39:35 CDT      16h Wed 2026-05-27 04:40:11 CDT       7h ago ds-archive-tier-rotation.timer                                     ds-archive-tier-rotation.service
Thu 2026-05-28 05:20:00 CDT      17h Wed 2026-05-27 05:20:06 CDT       6h ago logrotate-user.timer                                               logrotate-user.service
Thu 2026-05-28 05:30:00 CDT      17h Wed 2026-05-27 05:30:00 CDT       6h ago disk-hygiene-audit.timer                                           disk-hygiene-audit.service
Thu 2026-05-28 06:40:00 CDT      18h Wed 2026-05-27 08:05:00 CDT  4h 6min ago ibkr-deterministic-fx-poc.timer                                    ibkr-deterministic-fx-poc.service
Thu 2026-05-28 07:20:00 CDT      19h Wed 2026-05-27 07:20:00 CDT 4h 51min ago ibkr-release-monitor-auto.timer                                    ibkr-release-monitor-auto.service
Thu 2026-05-28 08:00:00 CDT      19h Wed 2026-05-27 08:00:00 CDT 4h 11min ago deal-scout-daily.timer                                             deal-scout-daily.service
Thu 2026-05-28 09:16:08 CDT      21h Wed 2026-05-27 09:16:08 CDT 2h 55min ago launchpadlib-cache-clean.timer                                     launchpadlib-cache-clean.service
-                                  - Wed 2026-05-27 12:10:00 CDT 1min 29s ago claude-chat-sync.timer                                             claude-chat-sync.service
-                                  - Wed 2026-05-27 05:40:00 CDT       6h ago database-autonomous-maintenance.timer                              database-autonomous-maintenance.service
-                                  - Wed 2026-05-27 12:11:15 CDT      14s ago gemini-ds-index-micro-parity.timer                                 gemini-ds-index-micro-parity.service
-                                  - Wed 2026-05-27 12:10:00 CDT 1min 29s ago gemini-reward-account-monitor.timer                                gemini-reward-account-monitor.service
-                                  - Wed 2026-05-27 12:10:00 CDT 1min 29s ago gemini-reward-live-readiness.timer                                 gemini-reward-live-readiness.service
-                                  - Wed 2026-05-27 12:09:56 CDT 1min 32s ago gemini-reward-quote-pilot.timer                                    gemini-reward-quote-pilot.service
-                                  - Wed 2026-05-27 12:10:44 CDT      45s ago gemini-trade-print-capture.timer                                   gemini-trade-print-capture.service
-                                  - Sun 2026-05-24 23:59:06 CDT   2 days ago gemini-weekday-mr-final-preopen-verifier.timer                     gemini-weekday-mr-final-preopen-verifier.service
-                                  - Mon 2026-05-25 00:30:01 CDT   2 days ago gemini-weekday-mr-first-cycle-verifier.timer                       gemini-weekday-mr-first-cycle-verifier.service
-                                  - Sun 2026-05-24 23:50:05 CDT   2 days ago gemini-weekday-mr-preopen-verifier.timer                           gemini-weekday-mr-preopen-verifier.service

66 timers listed.
```

## Repo State
- gemini: head=f13a613 branch=master in_sync=true remote=https://github.com/PhotonRahm/gemini_prediction_bot.git dirty=no
- ibkr: head=3a580e4 branch=master in_sync=true remote=https://github.com/PhotonRahm/ibkr_forecast_bot.git dirty=no
- kalshi: head=30e521b branch=master in_sync=true remote=https://github.com/PhotonRahm/kalshi_favorites_bot.git dirty=yes
- operations-knowledge: head=cc9da22 branch=master in_sync=true remote=https://github.com/PhotonRahm/operations-knowledge.git dirty=no
- workspace: head=5952a7f branch=master in_sync=false remote=https://github.com/PhotonRahm/rahm-workspace.git dirty=yes

## Active User Services
```
at-spi-dbus-bus.service
cross-venue-dislocation-scanner.service
dbus.service
dconf.service
ds-shadow-expansion-scanner.service
evolution-addressbook-factory.service
evolution-calendar-factory.service
evolution-source-registry.service
filter-chain.service
gcr-ssh-agent.service
gemini-bot.service
gemini-price-feed.service
gnome-keyring-daemon.service
gnome-session-manager@ubuntu.service
gnome-session-monitor.service
gnome-terminal-server.service
gvfs-afc-volume-monitor.service
gvfs-daemon.service
gvfs-goa-volume-monitor.service
gvfs-gphoto2-volume-monitor.service
gvfs-metadata.service
gvfs-mtp-volume-monitor.service
gvfs-udisks2-volume-monitor.service
ibkr-bot-stack.service
ibkr-gateway-monitor.service
ibkr-scan-loop.service
kalshi-bot.service
kalshi-ladder-sniper-v2.service
kalshi-ladder-sniper-v3.service
kalshi-same-strike-complementarity-scanner.service
ladder-coherence-scanner.service
ladder-coherence-two-leg-scanner.service
ollama.service
openclaw-gateway.service
org.freedesktop.IBus.session.GNOME.service
org.gnome.SettingsDaemon.A11ySettings.service
org.gnome.SettingsDaemon.Color.service
org.gnome.SettingsDaemon.Datetime.service
org.gnome.SettingsDaemon.Housekeeping.service
org.gnome.SettingsDaemon.Keyboard.service
org.gnome.SettingsDaemon.MediaKeys.service
org.gnome.SettingsDaemon.Power.service
org.gnome.SettingsDaemon.PrintNotifications.service
org.gnome.SettingsDaemon.Rfkill.service
org.gnome.SettingsDaemon.ScreensaverProxy.service
org.gnome.SettingsDaemon.Sharing.service
org.gnome.SettingsDaemon.Smartcard.service
org.gnome.SettingsDaemon.Sound.service
org.gnome.SettingsDaemon.Wacom.service
org.gnome.Shell@wayland.service
pipewire-pulse.service
pipewire.service
polymarket-shadow.service
rahm-phone.service
speech-dispatcher.service
sports-ds-forward-scanner.service
tracker-miner-fs-3.service
wireplumber.service
xdg-desktop-portal-gnome.service
xdg-desktop-portal-gtk.service
xdg-desktop-portal.service
xdg-document-portal.service
xdg-permission-store.service
```

## Today's Research Files (2026-05-27 UTC)
- research/2026-05-27-fq-ws1-btc-moderate-pilot-state-verification.md
- research/2026-05-27-fq-ws2-kalshi-favorites-tracking-methodology-audit.md
- research/2026-05-27-fq-ws3-favorites-tracking-pilot-proposals.md
- research/2026-05-27-fq-ws4-gemini-db-automated-retention.md
- research/2026-05-27-fq-ws5-kalshi-auto-vacuum-verification.md

## Deferred And Pending Items
```
specific trigger condition. Once the trigger is in the past, the item is due and
should be handled in the next operational review.
## Pending
| Key | Verification | Why deferred | Trigger | Due |
| `ibkr_weather_ds_uhsfo_5_to_8f_first_live_placement` | UHSFO 5-to-8F first live Weather DS placement verification | FD WS2 promoted `UHSFO_YES_cushion_5_to_8f` from shadow-only to the live Weather DS pilot under `SHADOW_APPROVAL_BOUNDARY_LIFTED_BY_OPERATOR_2026_05_24`. First-placement proof depends on venue supply and edge conditions, so it cannot be forced at deploy time. | On first `live_trades` row for `cell_key='UHSFO_YES_cushion_5_to_8f'` or strategy key `weather_pilot_UHSFO_YES_cushion_5_to_8f`, verify cohort tracker updates, CB ledger initializes, rollback evaluator includes the cell, and reconciliation remains $0.00. | Trigger-based |
| `fq_gemini_trades_auto_vacuum_after_open_positions_clear` | Gemini trades.db post-retention auto-VACUUM verification | FQ WS4 archived 99,704 rows from active Gemini `trades.db` into monthly SQLite archives, but safe auto-VACUUM deferred because four `gemini_reward_quote_pilot` positions were still open. VACUUM must not run while open-position gate is nonzero. | When Gemini `SELECT COUNT(*) FROM trades WHERE placed_at > datetime('now','-7 days') AND (resolution IS NULL OR resolution='PENDING')` returns 0, run `cd ~/.openclaw/workspace/scripts && python3 db_auto_vacuum.py --execute --only gemini_trades`, verify backup, `integrity_check=ok`, active DB size reduction, retention report rendering, and Gemini reconciliation remains $0.00. | Trigger-based |
| `fq_kalshi_auto_vacuum_pause_ack_remediation` | Kalshi auto-VACUUM pause acknowledgement remediation | FQ WS5 verified the FL open-position query fix: dry-run returned READY with 0 relevant open positions. Execution aborted before VACUUM on `pause_ack_timeout`; no DB mutation occurred. The pause/ack timing path must be remediated before claiming Kalshi auto-VACUUM is functioning end to end. | On next Kalshi maintenance pass, verify `KALSHI_BOT_PAUSE_FLAG` path matches `db_auto_vacuum_config.json`, inspect bot cycle latency around `_maintenance_pause_active()`, adjust timeout or ack location if needed, then run `python3 db_auto_vacuum.py --execute --only kalshi_trades` and verify backup, `integrity_check=ok`, and reconciliation $0.00. | Trigger-based |
| `kalshi_btc_moderate_yes_ds_first_10_review` | BTC moderate-favorite YES DS pilot first-10 resolved review | FK deployed a new live Kalshi BTC moderate-favorite YES DS pilot at qty 25 with a 2L/10 auto-kill gate. The review depends on natural settlement of the first cohort and cannot be forced at deploy time. | When `btc_moderate_pilot_cohort` reaches 10 resolved rows, verify loss count is below 2, CB ledger matches realized P&L, kill switch state matches gate result, status/daily/full-picture reports render the cohort, and Kalshi reconciliation remains $0.00. | Trigger-based |
| `kalshi_btc_moderate_yes_ds_first_30_review` | BTC moderate-favorite YES DS pilot first-30 resolved review | FK deployed a new live Kalshi BTC moderate-favorite YES DS pilot at qty 25 with a 3L/30 auto-kill gate and recent-30 P&L review trigger. The review depends on forward settlement. | When `btc_moderate_pilot_cohort` reaches 30 resolved rows, verify loss count is below 3, recent-30 P&L is nonnegative or explicitly reviewed, CB ledger matches realized P&L, kill switch state matches gate result, and Kalshi reconciliation remains $0.00. | Trigger-based |
| `kalshi_btc_moderate_yes_ds_n50_decision_review` | BTC moderate-favorite YES DS pilot n=50 decision review | FK authorized only the initial qty-25 live pilot. Scale/continue/kill decision needs realized forward evidence with corrected breakeven math and independent event review. | When `btc_moderate_pilot_cohort` reaches 50 resolved rows, compute realized average win/loss corrected breakeven, Wilson lower, P&L, settlement-hour/loss clustering, and surface a continue/kill/scale-proposal recommendation. No scale-up without separate operator authorization. | Trigger-based |
| `ibkr_weather_ds_historical_drift_cleanup_decision` | Weather DS historical drift cleanup decision | FD WS3 fixed the Weather DS settlement attribution path forward-only. The four historical BUG_CLASSES #17 drift rows remain intentionally unmodified under the no-DB-cleanup constraint. | Operator decision: either authorize controlled historical cleanup against `settlement_log` broker truth or accept the documented $0.40 historical attribution drift permanently. | Trigger-based |
| `tax_ledger_gemini_q1_2026_reconciliation_resolution` | Resolve Gemini Q1 known tax-ledger gap | Operator overrode the 2026-05-11 halt and completed source-of-truth remediation with the Gemini Q1 legacy FIFO-vs-direct gap documented as OPEN. | Before 2026-06-08 if practical, decompose the $3,946.52 gap into line items, update Decision 1 or Decision 9 if needed, re-ingest Gemini under corrected methodology, verify reconciliation within $5, and mark the known gap RESOLVED. | 2026-06-08 |
| `tax_ledger_q2_2026_estimated_payment_prep_review` | Q2 2026 estimated-payment prep | The source-of-truth tax ledger now generates Q2 partial planning reports, but the Gemini Q1 known gap remains open under Decision 9. | On 2026-06-08, run Q2 estimated-tax planning report, review open CPA flags, and decide whether the Gemini Q1 gap is resolved or carried into payment planning. | 2026-06-08 |
| `tax_ledger_q3_2026_estimated_payment_prep_review` | Q3 2026 estimated-payment prep | Quarterly payment prep should use the autonomous source-of-truth ledger and review open CPA flags. | Run Q3 planning report and review methodology flags. | 2026-09-08 |
| `tax_ledger_q4_2026_estimated_payment_prep_review` | Q4 2026 estimated-payment prep | Quarterly payment prep should use the autonomous source-of-truth ledger and review open CPA flags. | Run Q4 planning report and review methodology flags. | 2026-12-08 |
| `tax_ledger_2026_annual_filing_prep_review` | 2026 annual filing prep | CPA review is recommended before filing, especially for event-contract tax posture and the Gemini Q1 known gap. | On 2027-02-01, engage CPA/review methodology decisions, resolve open CPA flags, generate annual report, and freeze filing methodology. | 2027-02-01 |
| `kalshi_ds_eth_utc08_shadow_100_resolved_review` | Kalshi ETH DS UTC08 shadow filter forward review | ED loss-pattern forensic found UTC hour 08 loss concentration significant (p=0.0317), but the candidate failed live-deploy breakeven-margin proof after correcting breakeven to average win/loss size. It is shadow-only; live ETH DS placements remain unchanged. | When forward UTC08 current-filter ETH DS placements reach 100 resolved after 2026-05-23 13:34:00 UTC, evaluate Wilson lower versus corrected breakeven and compare to forward non-UTC08 over the same window. If UTC08 Wilson lower is below breakeven +2pp, scope a live UTC08 filter dispatch for operator approval; if above breakeven +2pp, retire the shadow as sample artifact. | Trigger-based |
| `kalshi_ds_eth_kill_condition_monitoring` | ETH DS kill condition forward monitoring | EE 2026-05-23 codified the operator framework "strategy works or it does not" into automated report-visible kill conditions. These thresholds replace ad hoc rollback recommendations for the operator-fixed qty 400 ETH cohort. | Continuously evaluate: lifetime CB breach at -$1,800, rolling 50-trade loss rate >8%, and n=50 cohort Wilson lower <90%. Any trigger surfaces as TOP RISK and requires operator decision on strategy continuation. | Trigger-based |
| `gemini_proper_cushion_shadow_decision_gate` | Gemini full-universe proper cushion DS live/retire decision gate | Scope 3 scanner starts a clean forward cohort in `shadow_gemini_cushion_ds`; decision-grade promotion or retirement requires per-asset independent contract-settlement evidence rather than favorite-tracking aggregates or repeated row observations. Updated 2026-05-10 per AGENTS.md Principle 51. | Once `shadow_gemini_cushion_ds` reaches n>=30 independent executable contract-settlement events per asset with Wilson lower above breakeven and positive collapsed P&L, evaluate per-asset live pilot, scale, or retire decision. Row-level metrics remain descriptive only. | Trigger-based, estimated 2-4 weeks after deploy |
| `gemini_weekday_crypto_mr_first_weekday_cycle_verification` | Gemini Weekday Crypto MR first weekday cycle verification | CLOSED VERIFIED 2026-05-25: `gemini-weekday-mr-first-cycle-verifier.service` exited 0/PASS at 00:30 CDT. It verified the intended env, 22 bot cycles after open, 30 price-feed heartbeats after open, no log errors, no DB locks, placement auth OK, DB write health OK, `STANDBY_WEEKEND` absent, telemetry advanced by 374 rows, no weekend standby after open, no stranded intent, no submit failures, no IOC unfilled, no low-cash blocks, and open positions remained 0. | CLOSED. Live Weekday Crypto MR stayed armed/funded but did not place because precise non-weekend blockers dominated; no live predicate change was authorized. | Completed 2026-05-25 |
| `gemini_mr_profit_watchlist_fast_target_coverage` | Gemini MR profit-watchlist fast-cadence target coverage | The 2026-05-25 fast-cadence fix makes shadow sweeps add target contracts from the full event universe before applying per-shadow caps. Immediate post-restart logs showed `source=target_augmented` behavior could be deployed, but the missed BTC `dow=1 1-4h` window had already moved under the 1h target boundary before the fix went live. | During the next active BTC `1-4h` watchlist window after commit `a4d71dd`, verify `MR_WATCHLIST_FAST_SHADOW ... source=target_augmented` appears, `mr_regime_shadow` records rows for cohort `mr_profit_watchlist_forward_shadow_2026_05_24` with `asset='BTC'` and `hours_to_expiry BETWEEN 1 AND 4`, and `GEMINI MR PROFIT WATCHLIST FORWARD SHADOW` renders nonzero flow for the active BTC `1-4h` target. The tracked guard is `gemini-mr-profit-watchlist-btc-1-4h-target-verifier.timer` / `scripts/verify_mr_profit_watchlist_btc_1_4h_target.py`; it fails if venue BTC 1-4h contracts exist while rows remain zero, or if the fast shadow sample cap saturates. If flow is still zero while venue contracts exist, reopen fast-cadence coverage. | Trigger-based, next BTC 1-4h target window |
| `gemini_zec_thursday_high_price_first_active_window` | Gemini ZEC Thursday high-price forward shadow first active-window verification | The 2026-05-25 ZEC high-price forward shadow is active in the fast-cadence MR watchlist path and reports as zero-flow before the Thursday UTC target window. First coverage proof depends on venue ZEC contract supply in the 4-24h window, so it cannot be forced at deploy time. | During the next UTC Thursday ZEC 4-24h target window after 2026-05-25, verify `MR_WATCHLIST_FAST_SHADOW` reports nonzero `zec_thursday_high_price_checked` when eligible ZEC contracts exist, `mr_regime_shadow` records cohort `zec_thursday_high_price_forward_shadow_2026_05_25` rows with `placement_rejected_reason` covering ask/depth blockers or `zec_thursday_high_price_forward_shadow_observation_only`, `GEMINI ZEC THURSDAY HIGH-PRICE FORWARD SHADOW` renders nonzero rows/events, and live MR remains blocked for ZEC unless a later independent event-collapsed gate and operator approval clear. If venue ZEC 4-24h contracts exist but rows remain zero, reopen fast-cadence target coverage. | Trigger-based, next UTC Thursday ZEC 4-24h target window |
| `gemini_zec_legacy_favorites_first_active_window` | Gemini ZEC legacy favorites forward shadow first active-window verification | The 2026-05-25 ZEC legacy-favorites forward shadow converts legacy short-expiry and lowprob ZEC cells into forward-only equivalence evidence, but current report flow is zero before the Thursday UTC 4-24h target. First proof depends on venue ZEC contract supply in that window. | During the next UTC Thursday ZEC 4-24h target window after 2026-05-25, verify `MR_WATCHLIST_FAST_SHADOW` reports nonzero `zec_legacy_favorites_checked` when eligible ZEC contracts exist, `mr_regime_shadow` records cohort `zec_legacy_favorites_forward_shadow_2026_05_25` rows with `zec_legacy_short_expiry_forward_shadow_observation_only` and/or `zec_legacy_lowprob_forward_shadow_observation_only` when predicates match, `GEMINI ZEC LEGACY FAVORITES FORWARD SHADOW` renders nonzero flow, and the legacy surfaces remain methodology-gated until n>=30 independent resolved event units with Wilson margin, positive P&L, predicate equivalence, and operator approval. If venue ZEC 4-24h contracts exist but rows remain zero, reopen target coverage. | Trigger-based, next UTC Thursday ZEC 4-24h target window |
| `gemini_weekday_crypto_mr_preopen_readiness_verification` | Gemini Weekday Crypto MR pre-open readiness verification | CLOSED VERIFIED 2026-05-25: both `gemini-weekday-mr-preopen-verifier.service` at 23:50 CDT and `gemini-weekday-mr-final-preopen-verifier.service` at 23:59 CDT exited 0/PASS. They verified bot/price-feed active with NRestarts=0, kill switch absent, broad MR kill present, expected ETH-only qty-5 env, open exposure 0, recent bot cycles, no recent log errors or DB locks, fresh price-feed heartbeats, auth OK, DB write OK, capital runway funded, and report still in weekend standby before open. | CLOSED. No pre-open deployment change required. | Completed 2026-05-25 |
| `gemini_sol_weekend_mr_first_resolution_verification` | Gemini SOL weekend MR first shadow resolution verification | CLOSED VERIFIED 2026-05-25: `gemini-sol-weekend-mr-first-resolution-verifier.service` exited 0/PASS. It verified the shadow enabled/cohort identity, intent rows present, and first-expiry rows resolved. Current DB/report evidence: 185 first-expiry intent rows, 1 independent event, 185 resolved, row W-L 59-126, row P&L -$971.85; decision-grade collapsed event is 0W-1L, P&L -$7.93, Wilson lower 0.0%, and due unresolved intent is 0. | CLOSED. Resolver/report path works, but SOL weekend MR first event is negative and not a live expansion candidate. | Completed 2026-05-25 |
| `gemini_weekday_mr_excluded_asset_first_resolution_verification` | Gemini Weekday MR excluded-asset first shadow resolution verification | CLOSED VERIFIED 2026-05-25: `gemini-weekday-mr-excluded-asset-first-resolution-verifier.service` exited 0/PASS. It verified the shadow enabled/cohort identity, intent rows present, and first-expiry rows resolved. Current DB/report evidence: 398 first-expiry intent rows across 2 independent events, 398 resolved, row W-L 306-92, row P&L -$167.04; report collapses BTC to 1W-0L +$0.61 with Wilson margin -66.3pp and SOL to 0W-1L -$4.25 with Wilson margin -84.0pp; due unresolved intent is 0. | CLOSED. Resolver/report path works, but excluded-asset re-entry remains non-decision-grade and does not justify expanding live Weekday Crypto MR beyond ETH. | Completed 2026-05-25 |
| `weather_cushion_ds_contract_date_gate` | Weather cushion DS unit-of-independence and time-window gate | Weather cushion-DS rows are repeated observations of daily weather contracts. The 2026-05-10 Gemini weather forensic showed row-level LIVE_PILOT_CANDIDATE labels collapsed to only 4-7 independent executable contract-date groups. Dispatch-conventions now also pre-commits an actionable time-window rule for future weather live pilot consideration. Updated 2026-05-10 per AGENTS.md Principle 51. | Once `weather_cushion_ds_shadow` per-cell time-windowed contract-date-collapsed metrics reach n>=30 independent executable contract-date groups with Wilson lower above breakeven and positive collapsed P&L within the actionable window, evaluate per-cell live pilot or retire decision. Row-level and full-lifetime collapsed metrics remain descriptive/contextual for pilot promotion. | Trigger-based |
| `index_fx_salvage_methodology_review` | Kalshi Index/FX Longshot Fade salvage methodology review | CLOSED SUPERSEDED 2026-05-13: Index and FX Longshot Fade were permanently killed after final live state 0W-12L combined, -$26.60. | CLOSED. No revival authorized from this live strategy key. Proper Index/FX cushion DS remains a separate shadow-only gate. | Completed 2026-05-13 |
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
| `kalshi_ds_qty_500_btc_redeploy_30_resolution_review` | Kalshi DS BTC qty 500 redeploy cohort review | CLOSED PASSED 2026-05-12: `filter_combined_qty_500_btc_redeploy_pilot` reached 44 resolved, 44W-0L, Wilson lower 92.0%, P&L +$956.89, and no daily CB breach. Operator elected scale-up to qty 600 with hard stop at qty 600 and asymmetric rollback pre-committed. | CLOSED. Forward BTC review now tracked under `kalshi_ds_qty_600_btc_redeploy_30_resolution_review`. | Completed 2026-05-12 |
| `kalshi_ds_qty_600_btc_redeploy_30_resolution_review` | Kalshi DS BTC qty 600 redeploy cohort review | CLOSED PASSED 2026-05-13: `filter_combined_qty_600_btc_redeploy_pilot` reached 42 resolved, 42W-0L, WR 100.0%, Wilson lower 91.6%, P&L +$770.93, and no daily CB breach. Operator elected scale-up to qty 700 with hard ceiling and tighter rollback. | CLOSED. Forward BTC review now tracked under `kalshi_ds_qty_700_btc_redeploy_30_resolution_review`. | Completed 2026-05-13 |
| `kalshi_ds_qty_700_btc_redeploy_30_resolution_review` | Kalshi DS BTC qty 700 redeploy cohort review | COMPLETED ROLLBACK_TRIGGERED 2026-05-13: `filter_combined_qty_700_btc_redeploy_pilot` resolved 2 trades, 0W-2L, Wilson lower 0.0%, P&L -$1,354.30, and daily CB breach before n=20. All three pre-committed rollback conditions fired. | CLOSED. Evidence preserved in `ds_qty_cohort_tracker`; qty-700 rows are informative only and are not inherited into the post-rollback qty-600 cohort. | Completed 2026-05-13 |
| `kalshi_ds_qty_600_btc_post_rollback_30_resolution_review` | Kalshi DS BTC qty 600 post-rollback cohort review | BTC rolled back from qty 700 to qty 600 on 2026-05-13 after the qty-700 redeploy attempt triggered rollback. New cohort `filter_combined_qty_600_btc_post_rollback_pilot` starts at `DS_KALSHI_QTY_600_BTC_POST_ROLLBACK_START`. | Once `filter_combined_qty_600_btc_post_rollback_pilot` reaches 30+ resolved BTC trades, evaluate WR>=95%, Wilson lower>=88%, positive P&L, and no daily CB breach. If gate clears, continue at qty 600 indefinitely unless operator elects a fresh scale review. If gate fails, choose rollback to qty 500, kill DS BTC, or alternative methodology by separate operator decision. | Trigger-based |
| `kalshi_ds_qty_700_btc_future_re_evaluation` | Future Kalshi DS BTC qty 700+ re-evaluation | Today's rollback is not a permanent prohibition on qty 700 or higher. It closes the 2026-05-13 qty-700 attempt as failed for this attempt only. | Operator-elected only. Requires documented reasoning for why the next attempt differs from the 2026-05-13 0W-2L failure, fresh CVaR at then-current Kalshi cash, tighter asymmetric rollback discipline, and stable qty-600 post-rollback cohort at n>=50 with Wilson lower >=90%. | Trigger-based |
| `kalshi_ds_contract_hour_max3_50_resolution_review` | Kalshi DS contract-hour max-3 cluster-cap forward review | Deployed 2026-05-13 after full-history loss forensic found the sequential max-3 contract-hour cap statistically supported: blocks 189/1,209 historical trades, 18/44 losses, projected +$1,535.39 P&L improvement, Fisher p=3.47e-05 and Bonferroni p x 8=0.00028. Contract-hour is symbol prefix before `-T`; cap applies uniformly to BTC and ETH. | Once `kalshi_ds_contract_hour_max3_forward_pilot` reaches 50+ resolved DS trades, evaluate observed loss rate versus ~2.26% historical unblocked projection, cumulative P&L, daily CB breaches, and `ds_cluster_cap_shadow` blocked-candidate outcomes. If blocked candidates would have lost more than won and allowed cohort stays positive, continue. If shadow shows wins blocked > losses prevented, operator-elected removal or threshold relaxation to max 4. If inconclusive, continue to n=100. | Trigger-based |
| `kalshi_ds_cb_reset_at_clean_window_2026-05-13` | Kalshi DS CB reset after qty-700 deploy | COMPLETED 2026-05-13: initial deploy preserved the prior reset timestamps, then the natural clean window was observed with DS open positions at 0. Reset timestamps were updated to `2026-05-13 10:25:36-05:00`, Kalshi restarted, `/proc/<pid>/environ` verified, and cash_gap remained $0.00. | CLOSED. Daily and lifetime CB ledgers now start fresh for the qty-700 era against -700/-2100 limits. | Completed 2026-05-13 |
| `kalshi_ds_qty_300_eth_30_resolution_review` | Kalshi DS ETH qty 300 cohort review | Operator scaled ETH qty/cap 275 -> 300 on 2026-05-11 17:55:04 CDT after the qty-275 ETH cohort and $0.93 filter cohort cleared gates. | Once `ds_qty_cohort_tracker` `filter_combined_qty_300_eth_pilot` reaches 30+ resolved ETH trades, evaluate WR>=93%, Wilson lower>=85%, positive P&L, and no daily CB breach. No automatic further scale-up regardless of result. If qty-300 cohort fails P&L or CB at n=30, roll back to qty 275 per separate operator decision. | Trigger-based |
| `filter_combined_qty_400_eth_pilot_30_resolution_review` | Kalshi DS ETH qty 400 cohort review | CLOSED PASSED 2026-05-20: `filter_combined_qty_400_eth_pilot` reached 44 resolved, 43W-1L, Wilson lower 88.2%, P&L +$214.33, max DD $369.59, and no hard rollback trigger. Operator honored EXPANSION_CANDIDATE with qty/cap 500. | CLOSED. Forward ETH review now tracked under `filter_combined_qty_500_eth_pilot_30_resolution_review`. | Completed 2026-05-20 |
| `filter_combined_qty_500_eth_pilot_30_resolution_review` | Kalshi DS ETH qty 500 cohort review | CLOSED ROLLBACK_TRIGGERED 2026-05-21: qty-500 ETH cohort resolved 2 trades, 1W-1L, P&L -$486.04, with a single trade loss worse than -$100. Operator honored the pre-committed asymmetric rollback and returned ETH qty/cap to 400. | CLOSED. Forward ETH review now tracked under `filter_combined_qty_400_eth_post_rollback_pilot_30_resolution_review`. | Completed 2026-05-21 |
| `kalshi_ds_eth_qty_500_first_trade_alarm` | Kalshi DS ETH qty 500 first-trade alarm | RESOLVED 2026-05-21: first resolved qty-500 ETH trades included one WIN and one LOSS; the loss triggered the single-trade-loss rollback guard. | CLOSED. Evidence preserved in `filter_combined_qty_500_eth_pilot`. | Completed 2026-05-21 |
| `filter_combined_qty_400_eth_post_rollback_pilot_30_resolution_review` | Kalshi DS ETH qty 400 post-rollback cohort review | ETH qty 500 cohort hit asymmetric rollback at n=2 after a single loss worse than -$100. New post-rollback cohort starts at `DS_KALSHI_QTY_400_ETH_POST_ROLLBACK_START=2026-05-21T18:00:00+00:00` with qty/cap 400. | Once `filter_combined_qty_400_eth_post_rollback_pilot` reaches 30+ resolved ETH trades, evaluate WR>=93%, Wilson lower>=85%, positive P&L, and no daily CB breach. Asymmetric rollback remains armed: 2 losses in first 10, 3 losses in first 30, daily CB breach before n=20, or any single trade loss worse than -$80 -> rollback to qty 300. | Trigger-based |
| `filter_combined_qty_500_eth_pilot_residual_resolution` | ETH qty 500 cohort residual position resolution | Qty-500 cohort was closed at rollback time with 2 resolved trades. Any pre-rollback open qty-500 ETH positions should settle naturally and then final cohort P&L should be logged. Current T1 snapshot found zero unresolved DS rows in `trades`, so this is a guard item in case broker/platform state reveals delayed settlement rows outside local open state. | On any later resolution of pre-rollback qty-500 ETH rows, update the closed cohort final P&L and confirm no live placement path still uses qty/cap 500. | Trigger-based |
| `kalshi_ladder_sniper_v2_kill_log_monitoring` | V2 kill-log monitoring | DV established `ladder_sniper_v2_kill_log` and the surface-in-reports requirement. Forward monitoring depends on this table being populated only when expected gates fire. | Any new row in `ladder_sniper_v2_kill_log` requires operator review within 24h. If a kill fires with a gate name not in the documented inventory, escalate to forensic dispatch. | Trigger-based |
| `sports_ds_mlb_pilot_first_resolved_trade` | Sports DS MLB pilot first resolved trade | Pilot deployed 2026-05-21 for `mlb_spread_conservative_gap_5plus` after current recheck showed 165 independent games, 148W-17L, Wilson 84.1%, BE 64.5%, and P&L +$2.64. No fresh active candidates existed at deploy verification, so first placement/resolution depends on future fresh scanner rows. | On first resolved `sports_ds_mlb_pilot_trades` row, verify settlement, P&L, CB ledger update, and asymmetric rollback evaluation. | Trigger-based |
| `sports_ds_mlb_pilot_50_resolution_review` | Sports DS MLB pilot 50-resolution review | Sports DS MLB pilot started as a bounded live-information pilot with separate strategy key `sports_ds_mlb_spread_conservative_gap5plus`, qty 10, max open 1, daily CB -25, lifetime CB -75, and kill switch `KILL_SPORTS_DS_MLB_PILOT`. | Once `sports_ds_mlb_pilot_trades` reaches 50+ resolved, evaluate WR, Wilson lower vs breakeven, P&L, CB state, and whether game-collapsed live evidence still supports continuation. | Trigger-based |
| `kalshi_ds_qty_225_eth_30_resolution_review` | Kalshi DS ETH qty 225 rollback cohort review | Completed 2026-05-08: `filter_combined_qty_225_eth_pilot` reached 38 resolved at 37W-1L, Wilson lower 86.5%, +$117.74, and the operator honored EXPANSION_CANDIDATE by scaling ETH to qty 275. | CLOSED. Forward ETH review now tracked under `kalshi_ds_qty_275_eth_30_resolution_review`. | Completed 2026-05-08 |
| `kalshi_ds_max_open_5_to_8_utilization_review` | Kalshi DS max_open 5->8 utilization review | Max_open was restored from 5 to 8 after BTC qty 400 / ETH qty 225 per-asset split made ETH-heavy windows underutilize capital. The DS dollar exposure cap was effectively disabled on 2026-05-10 with `DETERMINISTIC_SETTLEMENT_MAX_EXPOSURE=999999`, so platform cash is now the binding dollar constraint. This is a capital-throughput monitor, not a new per-trade strategy gate. | Review the `5->8` cap era after 30+ resolved trades or two active trading days, whichever comes first. Check active-window capital utilization target 60-90%, daily P&L trend, no daily CB breach, asset-hour cap block count, and whether max_open or platform cash is binding. Rollback/review if daily CB breaches on 2 consecutive days or cap-era quality materially deteriorates versus the historical 6->8 cohort. | Trigger-based |
| `kalshi_ds_cluster_cap_postfix_30_resolution_review` | Kalshi DS post-cluster-cap review | Qty-400 loss investigation found no filter or resolver bug, but did find funded-slot selection drift and correlated same asset/hour exposure. Max open was reduced to 5 and max asset/settlement-hour open positions capped at 4 on 2026-05-06. | Once 30 post-fix `strategy='deterministic_settlement'` rows have resolved, evaluate WR>=95%, Wilson lower>=88%, positive P&L, no daily CB breach, asset/hour cap block count, and whether qty 400 should continue, roll back, or pause. | Trigger-based |
| `gemini_mr_kelly_075_50_resolution_review` | Gemini MR Kelly 0.75x forward review | RESOLVED SUPERSEDED 2026-05-21: Gemini MR is permanently killed after lifetime breaker breach and failed 0.625x rollback cohort. Evidence: `research/2026-05-21-dt-gemini-mr-permanent-kill-forensics.md`. | CLOSED. No revival authorized from the `mean_reversion` strategy identity. | Completed 2026-05-21 |
| `gemini_mr_kelly_0.625x_rollback_pilot_50_resolution_review` | Gemini MR Kelly 0.625x rollback pilot review | RESOLVED FAILED 2026-05-21: post-rollback cohort had 16 resolved, 5W-11L, 31.2% WR, -$4,454.27 P&L versus 85.6% breakeven. Evidence: `research/2026-05-21-dt-gemini-mr-permanent-kill-forensics.md`. | CLOSED. No revival authorized from the `mean_reversion` strategy identity. | Completed 2026-05-21 |
| `gemini_mr_sol_eb_guard_30_resolved_shadow_review` | Gemini MR SOL EB guard blocked-candidate review | Dispatch N enabled a SOL-only EB overconfidence guard at live sizing probability >=0.97 and records blocked candidates to `sol_eb_overconfidence_guard_shadow`. | Once `sol_eb_overconfidence_guard_shadow` has 30+ resolved blocked candidates with `eventual_resolution` and `hypothetical_pnl` populated, evaluate blocked-candidate hypothetical P&L, W-L, and average per-candidate impact. If blocked net negative, continue guard. If blocked net positive, operator review to loosen/remove guard. If neutral, continue to n=50. | Trigger-based |
| `gemini_mr_eb_kelly_50_trade_review` | Gemini MR empirical-Bayes half-Kelly review | RESOLVED SUPERSEDED 2026-05-21: Gemini MR is permanently killed after the failed rollback cohort. | CLOSED. EB/maker/regime telemetry remains research-only for any future redesigned strategy identity. | Completed 2026-05-21 |
| `kalshi_proper_index_fx_cushion_shadow_decision_gate` | Proper Index/FX cushion DS promotion gate | Existing large Index/FX shadow evidence is favorite-tracking/longshot methodology, while the proper final-30m cushion DS table now accumulates from the separate `cushion-ds-multi-series-scanner.timer` deployed 2026-05-10. Sports is intentionally separate because it lacks a numeric spot/strike cushion. The legacy live Index/FX longshot keys remain killed. Updated 2026-05-10 per AGENTS.md Principle 51. | Once `shadow_index_fx_cushion_ds` reaches n>=30 independent executable contract-settlement events per series with Wilson lower above breakeven and positive collapsed P&L, evaluate per-series live pilot deployment. Row-level metrics remain descriptive only. | Trigger-based, estimated 2-4 weeks after deploy depending on per-series accumulation rate |
| `gemini_ds_parallel_filter_30_resolution_review` | Gemini DS parallel-filter pilot review | Completed 2026-05-06: parallel filter reached 36 resolved, 33W-3L, Wilson lower 78.2%, P&L -$14.48. All three losses were SOL; operator approved removing SOL and continuing BTC/ETH only. | CLOSED. Evidence preserved in `gemini_ds_cohort_tracker` as closed `parallel_filter_pilot`; no further action on BTC/ETH/SOL cohort. | Completed 2026-05-06 |
| `gemini_ds_parallel_filter_btc_eth_30_resolution_review` | Gemini DS BTC/ETH parallel-filter refinement review | Completed 2026-05-07: `parallel_filter_btc_eth_pilot` failed at 42 resolved, 37W-5L, Wilson lower 75.0%, P&L -$24.63, and daily CB breach. Loss-pattern review found all five losses below entry price 0.95. | CLOSED. Evidence preserved in `gemini_ds_cohort_tracker` as closed `parallel_filter_btc_eth_pilot`; no further action on the price>=0.90 BTC/ETH cohort. | Completed 2026-05-07 |
| `gemini_ds_eth_high_price_30_resolution_review` | Gemini DS ETH-only high-price refinement review | Completed 2026-05-09: `filter_combined_eth_high_price_pilot` reached 52 resolved, 52W-0L, WR 100%, Wilson lower 93.1%, P&L +$15.50, max DD $0.00, and no daily CB breach. Operator honored EXPANSION_CANDIDATE with qty 50. | CLOSED. Forward ETH review now tracked under `gemini_ds_eth_qty_50_30_resolution_review`. | Completed 2026-05-09 |
| `gemini_ds_eth_qty_50_30_resolution_review` | Gemini DS ETH qty 50 high-price review | CLOSED FAILED 2026-05-10: `filter_combined_eth_high_price_qty_50_pilot` reached 39 resolved, 37W-2L, WR 94.9%, Wilson lower 83.1%, P&L -$35.79, max DD $79.52. Operator honored ROLLBACK_RECOMMENDED and rolled ETH back to qty 10. | CLOSED. Evidence preserved in `gemini_ds_cohort_tracker`; qty-50 rows are informative only and not inherited into the rollback cohort. | Completed 2026-05-10 |
| `gemini_ds_high_cushion_30_resolution_review` | Gemini DS ETH high-cushion qty 10 review | The qty-10 rollback cohort failed positive-P&L at 78 resolved (73W-5L, Wilson 85.9%, P&L -$22.77). The surgical refinement tightens live Gemini DS to price>=0.95 and cushion>=0.40%, preserving qty 10 and all CBs. New cohort `filter_combined_eth_high_cushion_qty_10_pilot` starts 2026-05-11 23:16:00 UTC / 18:16:00 CDT. | Once `gemini_ds_cohort_tracker` `filter_combined_eth_high_cushion_qty_10_pilot` reaches 30+ resolved ETH trades, evaluate WR>=96%, Wilson lower>=88%, positive cohort P&L, and no daily CB breach. No automatic scale-up. If P&L is negative at n>=30 or daily CB breaches earlier, kill or pause Gemini DS per separate operator decision. | Trigger-based |
| `kalshi_moderate_favorites_crypto_yes_0_1h_80_85_resurrection_review` | Kalshi Moderate Favorites resurrection review | CLOSED SUPERSEDED 2026-05-13: Moderate Favorites was permanently killed. Final live state 204 resolved, 154W-50L, WR 75.5%, P&L -$209.49; 2026-05-11 forensic returned Verdict B and no resurrection was authorized. | CLOSED. No revival authorized from this live strategy key. | Completed 2026-05-13 |
| `whelan_weather_0_5_1h_independent_contract_review` | Whelan near-expiry weather independent-contract review | 2026-05-11 forensic returned Verdict B: row-level weather/0.5-1h was 37W-0L, +$275, but collapsed to only 11 independent contract symbols, 11W-0L, Wilson 74.1%, +$77. Non-crypto/0.5-1h flipped from +$149 row-level to -$49 collapsed, proving row count is not decision-grade. | Once `shadow_near_expiry_favorites` weather/0.5-1h reaches 30+ independent resolved contract symbols after collapse-by-symbol, evaluate collapsed W-L/P&L using first eligible row per symbol, Wilson lower above breakeven, positive P&L in both temporal halves, and explicit exclusion of adjacent weather 1-2h and 2-4h bands. If all pass, write a separate bounded live-pilot deployment dispatch; do not auto-deploy from row-level counts. | Trigger-based |
| `kalshi_mr_index_cluster_cap_review` | Kalshi MR INDEX cluster cap review | Path B deployed max 2 open MR INDEX positions per underlier/event and max 4 total open MR INDEX positions per settlement hour after loss-pattern analysis found same-settlement clustering as the highest-evidence unmitigated INDEX risk. Existing open INDEX rows at deploy are grandfathered. | Once post-deploy INDEX MR rows have 30+ resolved trades or on 2026-05-21, whichever comes first, evaluate INDEX P&L, block counts, max same-event/hour exposure, and whether the max 2/max 4 cap should stay, tighten, loosen, or retire INDEX. | 2026-05-21 20:20 UTC |
| `kalshi_mr_allowed_cells_forward_pnl_review` | Kalshi MR currently-allowed cell forward P&L review | REPLACED 2026-05-11 by `kalshi_mr_post_surgical_blocks_30_resolution_review` after ETH and WEATHER_LOW YES were promoted from capped/partial controls to full surgical blocks. | CLOSED. Evidence before replacement remains visible in Kalshi status as the pre-block allowed-cell tracker. | Completed 2026-05-11 |
| `gemini_ds_realized_volatility_first_live_rows` | Gemini DS realized-volatility instrumentation first live rows | Gemini DS `realized_volatility_at_entry` returned NULL because `bot.py` referenced `sqlite3.Row` without importing `sqlite3`; fix applies forward only and historical rows are not backfilled. | On the first Gemini DS trade after the parallel-filter deploy, verify `time_to_settlement_seconds` and `realized_volatility_at_entry` are populated, or realized volatility is explicitly NULL only with an insufficient-history warning. | Trigger-based |
| `ds_entry_instrumentation_first_live_rows` | DS entry instrumentation first-row verification | `time_to_settlement_seconds` and `realized_volatility_at_entry` schema, placement code, and tests are deployed, but no post-deploy Kalshi/Gemini DS placement occurred during restart verification windows. | On the first Kalshi DS trade after `DS_KALSHI_FILTER_COMBINED_START` and first Gemini DS trade after `DETERMINISTIC_SETTLEMENT_PILOT_START`, verify both new fields are populated or explicitly NULL only when insufficient spot history exists; confirm price/cushion/depth filters on the same rows. | Trigger-based |
| `kalshi_mr_weather_low_yes_cap_30_resolution_review` | Kalshi MR WEATHER_LOW YES permanent-cap review | SUPERSEDED 2026-05-11 by full WEATHER_LOW YES block. The prior cap remains documented but is no longer the active policy. | CLOSED. Forward review now tracked under `kalshi_mr_post_surgical_blocks_30_resolution_review`. | Completed 2026-05-11 |
| `kalshi_mr_post_surgical_blocks_30_resolution_review` | Kalshi MR post-surgical-block review | REPLACED 2026-05-12 by `kalshi_mr_post_full_weather_low_block_30_resolution_review` after WEATHER_LOW NO was added to the block list. The 2026-05-11 surgical block left WEATHER_LOW NO eligible, and that side bled materially before replacement. | CLOSED. Forward review now tracks the post-full-WEATHER_LOW residual universe. | Completed 2026-05-12 |
| `kalshi_mr_post_full_weather_low_block_30_resolution_review` | Kalshi MR post-full-WEATHER_LOW-block review | REPLACED 2026-05-13 by `kalshi_mr_minimal_sizing_post_sol_block_30_resolution_review` after SOL tail-loss flipped negative and MR moved to qty-10 data-collection sizing with `MR_MIN_SPREAD=0.02`. | CLOSED. Forward review now tracks the post-SOL-block minimal-sizing cohort. | Completed 2026-05-13 |
| `kalshi_mr_minimal_sizing_post_sol_block_30_resolution_review` | Kalshi MR minimal-sizing post-SOL-block review | On 2026-05-13 Kalshi MR moved to qty 10, `MR_MIN_SPREAD=0.02`, `MEAN_REVERSION_MAX_PER_TRADE=20`, and SOL full block after SOL moved to 30W-6L, -$109.04 with observed WR below breakeven. Effective residual live universe is OTHER/INDEX subject to existing weather/BTC/ETH/SOL blocks and spread 2-5c. | Once Kalshi MR placements after `KALSHI_MR_MINIMAL_SIZING_START=2026-05-13 10:19:42-05:00` reach 30+ resolved, evaluate cumulative P&L sign, Wilson lower versus breakeven, and OTHER/INDEX breakdown. If positive P&L and Wilson lower above breakeven, operator may evaluate larger sizing. If negative P&L at n>=30, HARD KILL PERMANENTLY, not pause. If marginal, operator decision. | Trigger-based |
| `kalshi_mr_instrumentation_first_live_rows` | Kalshi MR first live instrumentation rows | MR placement path now writes `time_to_settlement_seconds` and quote-path `realized_volatility_at_entry` forward-only; historical MR rows remain NULL. | On the first Kalshi MR placement after the deploy, verify both fields are populated, or realized volatility is explicitly NULL only with an insufficient-history warning in logs. | Trigger-based |
| `kalshi_ds_low_price_no_30_resolution_review` | Kalshi DS low-price NO pilot review | Completed 2026-05-06: pilot was 15W-6L at 21 resolved and mathematically could not reach the 90% WR gate by 30 resolved. Paused early as equivalent gate failure and BUG_CLASSES #24 subset-overfitting lesson preserved. | CLOSED. Existing open positions settle naturally; do not re-enable without a fresh operator-approved methodology and cohort boundary. | Completed 2026-05-06 |
| `kalshi_ds_low_price_no_first_live_rows` | Kalshi DS low-price NO first-placement instrumentation | Pilot instrumentation is forward-only and no historical rows are backfilled. | On first `strategy='ds_low_price_no'` filled row, verify side=NO, price < $0.80, asset in BTC/ETH/SOL, qty=10, `time_to_settlement_seconds`, `realized_volatility_at_entry`, `cushion_at_entry`, and depth fields are populated or explicitly explain any NULL. | Trigger-based |
```

## Recent Decisions
## 2026-05-17 - CK IBKR complementarity scanner simultaneity fix

Decision:
- Add quote simultaneity fields and evidence tiers to the IBKR YES/NO
  complementarity scanner.
- Use execution-ready fresh-simultaneous rows, not raw gross-positive rows, for
  the 30-observation evidence gate.

Reason:
- CG found raw gross-positive BV rows were latest-pair artifacts: quote
  timestamp deltas ranged from 3,330s to 6,125s, with zero fresh-simultaneous
  positives.
- After CK backfill, gross-positive fresh-simultaneous rows remain 0.

Scope:
- Scanner/reporting fix only.
- No trading logic enabled.
- Existing rows preserved and classified rather than deleted.

## 2026-05-17 - CL IBKR Release Monitor USTM wrong-source block

Decision:
- Disable Release Monitor collection for USTM through the FRED/DGS10 path.
- Mark historical Release Monitor USTM rows as wrong-source methodology-review
  evidence in readiness and status reporting.

Reason:
- USTM resolves from NCEI temperature, not Treasury DGS10.
- Existing Release Monitor USTM/DGS10 rows showed positive-looking cells, but
  they are structurally non-deployable because the source identity is wrong.

Scope:
- Collector/schedule/reporting fix only.
- No live placement, sizing, broker, or DB mutation.
- Existing rows are preserved and blocked from promotion.

## 2026-05-17 - CM DS status archive attach-limit fix

Decision:
- Bound the DS Shadow Expansion platform-status archive window so IBKR status
  reports do not fail with SQLite's attached-database limit.

Reason:
- The report tried to attach every DS shadow archive and rendered
  `UNAVAILABLE: too many attached databases - max 10`.
- A bounded recent archive window preserves the operational status surface
  without hiding the section.

Scope:
- Reporting fix only.
- No live placement, sizing, broker, or DB mutation.

## 2026-05-17 - CN IBKR Long+Short USGP/NO side block

Decision:
- Block new live Long+Short placements for `USGP/NO`.
- Keep `USGP/YES` live-eligible under the existing gates.

Reason:
- Live bot USGP is 7W-1L but -$4.62 because the single NO loss cost -$9.50
  while YES wins are small.
- Shadow USGP/NO is 81W-22L with -$353.80 P&L; shadow USGP/YES remains
  positive.
- This is the asymmetry-trap bug class and should be handled as a
  side-specific block, not a broad USGP underlier block.

Scope:
- Future placement gate only.
- Existing open positions are not mutated.

## 2026-05-17 - CO IBKR Maker weather UHHOU-only live gate

Decision:
- Restrict new live Weather Maker placements to `UHHOU`.
- Keep the broader Weather Maker city set in shadow collection.

Reason:
- Mid-price replay showed only `UHHOU` positive.
- `UHBNA`, `UHDFW`, `UHCLT`, `UHLAX`, `UHLGA`, and `UHMDW` were negative at
  the live midpoint style and should not keep taking live risk.

Scope:
- Future maker placement gate only.
- Shadow evidence collection continues for the broader city set.
- Existing maker order history is not mutated.

## 2026-05-17 - CP IBKR FRER freight source correction

Decision:
- Map `FRERC` and `FRERI` public shadow resolution to FRED/BTS rail freight
  carloads and rail freight intermodal traffic.
- Correct the status label from rent index to freight.

Reason:
- CFTC/ForecastEx references show `FRERI` is total freight traffic from
  intermodal traffic and `FRERC` is total freight traffic from carloads.
- FRED exposes the corresponding BTS series as `RAILFRTINTERMODAL` and
  `RAILFRTCARLOADS`.

Scope:
- Shadow resolver/reporting correction only.
- Exact monthly observation matching is required.
- Neither underlier is live-allowlisted by this change.

## 2026-05-17 - CQ IBKR Weather DS UHSFO 5-to-8 shadow tracking

Decision:
- Add `UHSFO_YES_cushion_5_to_8f` to Weather DS shadow-only signal tracking.
- Do not add it to the live pilot allowlist.

Reason:
- Readiness shows this cell as approval-bound and separate from the excluded
  `UHSFO_YES_cushion_2_to_5f` cell.
- Forward signal rows are needed before any later graduation review.

Scope:
- Shadow collection only.
- No live placement, sizing, broker, or existing position mutation.

## 2026-05-17 - CN IBKR repo hygiene round 2

Decision:
- Commit the remaining IBKR dirty state as report-only maker-shadow wording
  hygiene.

Reason:
- The actual dirty file was `ibkr_status_report.py`; the expected Release
  Monitor dirty files were already clean.
- The change prevents fill-rate-only maker-shadow output from saying a level
  "looks promising" when net P&L is negative.
- This matches the BS maker-shadow lesson that filled-price improvement,
  non-fill avoidance, and filled-P&L must be distinguished before promotion
  wording.

Scope:
- Report-only change.
- No service restart.

## 2026-05-17 - CO Rahm workspace repo hygiene

Decision:
- Commit the remaining workspace dirty state as identity/memory hygiene.

Reason:
- The expected `ibkr_goal_readiness` files were already clean.
- `USER.md` added Eric's confirmed Discord identity for future owner request
  recognition.
- `memory/2026-05-17.md` followed the existing daily memory backup pattern.

Scope:
- Workspace documentation/memory only.
- No running service changes.

## 2026-05-17 - CX Kill Kalshi Mean Reversion

Decision:
- Kill Kalshi Mean Reversion via `KILL_MEAN_REVERSION`.

Reason:
- CW found the post-filter allowed-cell cohort was materially negative and below
  breakeven: about 84% observed nonzero WR versus about 91% breakeven WR, with
  P&L around -$730 on the current allowed cohort.
- No sufficiently powered currently live subset validated out-of-sample.
- Open MR positions at kill were zero.

Scope:
- Kill-switch enforcement only.
- No position closes.
- Other Kalshi strategies unchanged.

## 2026-05-17 - CY Scale IBKR Long+Short to qty 100 short FX

Decision:
- Scale IBKR Long+Short from qty 60 to qty 100 by operator override.
- Restrict the scaled cohort to short-dated FX on `JPUSD`, `USEUR`, and
  `USGBP` only.

Reason:
- CW showed edge concentration in FX and better capital efficiency in the
  short-dated sleeve.
- Operator explicitly overrode the 50-resolution post-raise trigger while
  narrowing scope as risk mitigation.

Scope:
- New qty-100 cohort starts at `2026-05-17T18:48:00-05:00`.
- Existing qty-60 positions resolve naturally.
- Economics, USCAD, and >48h contracts are excluded from the scaled cohort.

## 2026-05-22 - CZ Operator override IBKR FX route expansion pilot

Decision:
- Treat the pending IBKR Long+Short live-route expansion as an explicit
  operator-overridden pilot despite the evidence gap.
- Add `USCAD/YES 24-60h` to the qty-100 short-FX cohort.
- Add a separate qty-30 long-FX pilot across `JPUSD`, `USEUR`, `USGBP`, and
  `USCAD` for 48-168h contracts.

Reason:
- Operator selected the override path on 2026-05-22 after Codex reported that
  the route did not meet normal evidence gates.
- Pre-override evidence was deliberately below the standard decision-grade
  threshold: `USCAD/YES 24-60h` had only 18 resolved shadow samples
  (`17W-1L`, +$4.60), and 60-168h FX cells had tiny per-cell samples.
- The purpose is bounded live execution data, not a statistical scale claim.

Scope:
- New qty-30 long-FX cohort starts at `2026-05-22T09:33:00-05:00`.
- Qty-30 route is capped at 30 contracts per position, max 10 open, daily CB
  -$50, lifetime CB -$150, and review/exit at 30 resolved or any CB breach.
- `USCAD/NO` remains hard-excluded. Economics and Weather are not added to
  this route. Existing positions resolve naturally.

---
sha256_without_checksum: [REDACTED:long_hex]
