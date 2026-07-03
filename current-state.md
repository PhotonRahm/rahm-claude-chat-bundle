# Rahm Current State

last_updated_utc: 2026-07-03T23:03:54+00:00
pipeline_heartbeat_utc: 2026-07-03T23:03:54+00:00
generator: Codex generate_current_state.py
workspace_head: 0710930

## Chat Startup Critical Summary
- Generated for Claude-in-chat startup at 2026-07-03T18:03:54-05:00; missing artifacts render UNAVAILABLE instead of breaking sync.
- Full-picture artifact: FULL PICTURE - 2026-07-03 06:00 PM

### Reconciliation and Cash
- Gemini: Cash balance: $22.74
- Gemini reconciliation: Reconciliation: resolved_pnl=$-12871.29 open_cost=$0.80 open_fees=$0.07 recon_adj=$-2139.97 expected_cash=$22.74 cash_gap=$+0.00 unrealized=-$0.80 [MATCH]
- Kalshi: Cash balance: $1,188.83
- Kalshi reconciliation: Reconciliation: resolved_pnl=$-1500.51 open_cost=$0.47 open_fees=$0.03 recon_adj=$189.84 expected_cash=$1188.83 cash_gap=$+0.00 unrealized=$-0.44 [MATCH]
- IBKR: NLV: $1,949.48
- IBKR state: Status: ⚠️ Flex sync 217h stale | ❌ Gateway DOWN | ❌ KILL switch active
- IBKR reconciliation caveat: Cash gap: UNAVAILABLE

### Killed / Non-Revival Roster
- Standard deterministic settlement: global/broad DS is not revived; Kalshi status shows standard DS kill switches, DS low-price NO killed, BTC moderate YES killed, and crypto NO <10c pilot kill switches.
- Sports DS: MLB spread conservative gap pilot is KILLED.
- Mean reversion: Kalshi MR KILLED; Gemini MR KILLED with no revival authorized.
- Favorites: Moderate Favorites KILLED; favorites taker/maker rows are historical buckets, not an active revival.
- Longshot / longshot fading: index longshot fade, FX longshot fade, and longshot fading are KILLED.
- Maker surfaces: KILL_MAKER present; high-price maker/cancel and broad maker surfaces remain evidence-gated or negative/toxic; no broad maker revival.
- Gemini crypto DS / contrarian: Gemini DS and contrarian-style micro-pilots are killed/source-blocked; Gemini live status remains reward-quote only when armed.

### Active / Open Pilot State
- Gemini reward quote pilot: ✓ Reward Quote Pilot: -$0.30 | 0W-3L | open: 7 | live reward quote pilot armed; governed by readiness and quote-manager gates; state from latest manager action
- Claude weather locked pilot v1 and resolution-lag clarity add-on remain bounded micro-pilot state from the 2026-07-01 research files; do not alter open rows or pilot caps from chat.
- Claude crossing-NO v3/v3.2: 4b. Market type: strike_type == "between" ONLY (floor AND cap present) — the exact; no resting orders; halt on any settled YES or cumulative realized drawdown >= $50 per charter.
- Codex locked-MVE passive-maker pilot: Continued the whole-universe Kalshi strategy search after launching the locked-MVE passive-maker pilot. This pass closed out the live MVE order with no fill, refreshed native/maker/source-free gates, and investigated a new non-sports structural surface: monotone corporate-announcement date thresholds in `KXLUCEDELIVERY-27`.
- Codex Netflix views NO pilot: One small live pilot was launched: qty `1` NO on `KXNETFLIXTOPVIEWSMOVIE-26JUL06-25` at `0.05`. This is a predictive live-data pilot using Netflix's official historical Top 10 views TSV; it is not a source-locked result-lag trade because the target chart week ending `2026-07-05` has not published yet.
- Codex Kalshi live-pilot slot: Launched one small live pilot after the fresh native quote, current-price subcell evidence, Coinbase spot cushion, duplicate checks, and live-pilot exposure caps all cleared.
- Goal loops, pilot charters, kill files, and live positions are read-only context for Claude-in-chat.

### IBKR Blockers
- IBKR live trading is killed (KILL_LIVE_TRADING present); Gateway/API are down in current status; open exposure is $0.00.
- Flex Query 1479083 recent-date availability remains pending operator/support action; recent Flex data is stale, so cash gap can be unavailable while live-vs-statement NLV drift is stable.
- TOTP/auth: IBKR says authenticator is already active, so TOTP re-enrollment is pending support. TOTP secret values, paths, and generated codes must never be published.
- FX shadow / deterministic FX POC: current report shows shadow_candidates not initialized and Gateway/API down; no poc-service-specific source was found in current files, so that exact blocker is UNAVAILABLE.

### FX-AK Frontier Verdict
- No Kalshi weather/NWS live pilot is justified.
- Summary: no Kalshi weather/NWS live pilot was justified by FX-AK; direct NWS edge was stale/negative after correction and forecast-accuracy slices were underpowered against Wilson/breakeven requirements.

### Cost / Runway
- • MTD (through 2026-07-03): **$29.14**
- • Projected monthly total: **$301.15/mo**
- • API-realized net after external costs: **$-17087.80**
- • Gemini open positions: 8 trades, $9.50 at cost, $0.04 at mark
- • Combined true P&L: **$-16331.90**
- • True lifetime P&L (bots − one-time − recurring): **$-19195.63**
- External fixed burn is the recurring subscription runway driver; broker fees already embedded in venue/account P&L must not be double-counted.

## Trading Bot Runtime
### gemini
- unit: gemini-bot.service
- active: active/running
- pid: 9238
- nrestarts: 0
- active_enter: Fri 2026-07-03 09:09:17 CDT
- reconciliation:
  - • [Gemini] API Settlement/Cashout Reconciliation Adjustment: -$104.68 | 0W-1L | realized rows: 0 | fees: $0.00 | Gemini settled-positions API netProfit plus cashOuts wins over reconstructed DB sell/cost-basis P&L.
  - Reconciliation: resolved_pnl=$-12871.29 open_cost=$0.80 open_fees=$0.07 recon_adj=$-2139.97 expected_cash=$22.74 cash_gap=$+0.00 unrealized=-$0.80 [MATCH]
  - ✓ HARD CHECK PASSED — gap $0.00
  - Reconciliation adjustment: $-2139.97 (auto-computed from exchange balance)
  - Expected cash: $22.74
  - Actual cash (API): $22.74
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
  - `CRYPTO_BTC_LATE_HIGH_CUSHION_YES_DS_PILOT_KILL_SWITCH=/home/eric-king/gemini_prediction_bot/KILL_CRYPTO_BTC_LATE_HIGH_CUSHION_YES_DS_PILOT`
  - `CRYPTO_BTC_LATE_HIGH_CUSHION_YES_DS_PILOT_START=2026-05-23 14:28:00`
  - `CRYPTO_BTC_LOW_MID_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_BTC_LOW_MID_NO_DS_PILOT_KILL_SWITCH=/home/eric-king/gemini_prediction_bot/KILL_CRYPTO_BTC_LOW_MID_NO_DS_PILOT`
  - `CRYPTO_BTC_LOW_MID_NO_DS_PILOT_START=2026-05-23 13:47:43`
  - `CRYPTO_BTC_MID_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_BTC_MID_NO_DS_PILOT_KILL_SWITCH=/home/eric-king/gemini_prediction_bot/KILL_CRYPTO_BTC_MID_NO_DS_PILOT`
  - `CRYPTO_BTC_MID_NO_DS_PILOT_START=2026-05-23 13:38:09`
  - `CRYPTO_BTC_MID_WEEKDAY_YES_DS_PILOT_ENABLED=false`
  - `CRYPTO_BTC_MID_WEEKDAY_YES_DS_PILOT_KILL_SWITCH=/home/eric-king/gemini_prediction_bot/KILL_CRYPTO_BTC_MID_WEEKDAY_YES_DS_PILOT`
  - `CRYPTO_BTC_MID_WEEKDAY_YES_DS_PILOT_START=2026-05-23 13:12:31`
  - `CRYPTO_BTC_UTC12_YES_DS_PILOT_ENABLED=false`
  - `CRYPTO_BTC_UTC12_YES_DS_PILOT_KILL_SWITCH=/home/eric-king/gemini_prediction_bot/KILL_CRYPTO_BTC_UTC12_YES_DS_PILOT`
  - `CRYPTO_BTC_UTC12_YES_DS_PILOT_START=2026-05-23 12:59:58`
  - `CRYPTO_BTC_UTC18_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_BTC_UTC18_NO_DS_PILOT_KILL_SWITCH=/home/eric-king/gemini_prediction_bot/KILL_CRYPTO_BTC_UTC18_NO_DS_PILOT`
  - `CRYPTO_BTC_UTC18_NO_DS_PILOT_START=2026-05-23 12:25:00`
  - `CRYPTO_ETH_LATE_HIGH_CUSHION_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_ETH_LATE_HIGH_CUSHION_NO_DS_PILOT_KILL_SWITCH=/home/eric-king/gemini_prediction_bot/KILL_CRYPTO_ETH_LATE_HIGH_CUSHION_NO_DS_PILOT`
  - `CRYPTO_ETH_LATE_HIGH_CUSHION_NO_DS_PILOT_START=2026-05-23 14:45:00`
  - `CRYPTO_ETH_LATE_HIGH_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_ETH_LATE_HIGH_NO_DS_PILOT_KILL_SWITCH=/home/eric-king/gemini_prediction_bot/KILL_CRYPTO_ETH_LATE_HIGH_NO_DS_PILOT`
  - `CRYPTO_ETH_LATE_HIGH_NO_DS_PILOT_START=2026-05-23 12:40:00`
  - `CRYPTO_ETH_LOWER_LATE_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_ETH_LOWER_LATE_NO_DS_PILOT_KILL_SWITCH=/home/eric-king/gemini_prediction_bot/KILL_CRYPTO_ETH_LOWER_LATE_NO_DS_PILOT`
  - `CRYPTO_ETH_LOWER_LATE_NO_DS_PILOT_START=2026-05-23 14:06:00`
  - `CRYPTO_ETH_LOWER_LATE_YES_DS_PILOT_ENABLED=false`
  - `CRYPTO_ETH_LOWER_LATE_YES_DS_PILOT_KILL_SWITCH=/home/eric-king/gemini_prediction_bot/KILL_CRYPTO_ETH_LOWER_LATE_YES_DS_PILOT`
  - `CRYPTO_ETH_LOWER_LATE_YES_DS_PILOT_START=2026-05-23 14:13:00`
  - `CRYPTO_ETH_MIDDAY_MID_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_ETH_MIDDAY_MID_NO_DS_PILOT_KILL_SWITCH=/home/eric-king/gemini_prediction_bot/KILL_CRYPTO_ETH_MIDDAY_MID_NO_DS_PILOT`
  - `CRYPTO_ETH_MIDDAY_MID_NO_DS_PILOT_START=2026-05-23 14:57:00`
  - `CRYPTO_FINAL_HIGH_PRICE_ETH_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_FINAL_HIGH_PRICE_ETH_NO_DS_PILOT_KILL_SWITCH=/home/eric-king/gemini_prediction_bot/KILL_CRYPTO_FINAL_HIGH_PRICE_ETH_NO_DS_PILOT`
  - `CRYPTO_FINAL_HIGH_PRICE_ETH_NO_DS_PILOT_START=2026-05-23 03:06:00`
  - `CRYPTO_FINAL_LOW_PRICE_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_FINAL_LOW_PRICE_NO_DS_PILOT_KILL_SWITCH=/home/eric-king/gemini_prediction_bot/KILL_CRYPTO_FINAL_LOW_PRICE_NO_DS_PILOT`
  - `CRYPTO_FINAL_LOW_PRICE_NO_DS_PILOT_START=2026-05-23 02:51:17`
  - `CRYPTO_FINAL_MID_PRICE_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_FINAL_MID_PRICE_NO_DS_PILOT_KILL_SWITCH=/home/eric-king/gemini_prediction_bot/KILL_CRYPTO_FINAL_MID_PRICE_NO_DS_PILOT`
  - `CRYPTO_FINAL_MID_PRICE_NO_DS_PILOT_START=2026-05-23 06:03:00`
  - `CRYPTO_FINAL_ULTRA_LOW_BTC_NO_DS_PILOT_ENABLED=false`
  - `CRYPTO_FINAL_ULTRA_LOW_BTC_NO_DS_PILOT_KILL_SWITCH=/home/eric-king/gemini_prediction_bot/KILL_CRYPTO_FINAL_ULTRA_LOW_BTC_NO_DS_PILOT`
  - `CRYPTO_FINAL_ULTRA_LOW_BTC_NO_DS_PILOT_START=2026-05-23 06:08:00`
  - `CRYPTO_LATE_LOW_PRICE_NO_DS_PILOT_ENABLED=false`
- strategy/cohort excerpts:
  - Live/tracked resolved P&L: -$0.30 across 3 resolved trades
  - API-verified full P&L (all historical strategies): -$12,975.97 across 2354 DB resolved rows (DB reconstruction -$12,871.29)
  - 24h P&L: -$0.10 (0W-1L resolved, 2 placed)
  - Today's P&L: -$0.10
  - Permanently killed strategies (3):
  - ✗ [Gemini] Mean Reversion: KILLED 2026-05-21 | +$488.51 | 168W-30L | lifetime breaker breached; Kelly 0.625x rollback failed; no revival authorized
  - ✗ [Gemini] Crypto DS micro-pilots: KILLED 2026-05-23 | +$0.00 | 0W-0L | source-blocked after GRR-KAIKO vs Gemini spot mismatch; no open positions
  - ✗ [Gemini] Contrarian cell micro-pilots: KILLED 2026-05-24 | +$0.00 | 0W-0L | paused after executable evidence failed; spillover positions resolved
  - Historical realized buckets (8; sum must equal lifetime):
  - • [Gemini] API Settlement/Cashout Reconciliation Adjustment: -$104.68 | 0W-1L | realized rows: 0 | fees: $0.00 | Gemini settled-positions API netProfit plus cashOuts wins over reconstructed DB sell/cost-basis P&L.
  - ✓ Gemini: lifetime -$12,975.97 / 2354 realized rows; bucket sum -$12,975.97 / 2354 rows
  - Next decision gate: 2026-07-04T00:30:00+00:00 - direct-index DS next resolution (52 rows/5 events unresolved | current qty5: 35 rows/5 events unresolved | micro qty1: 17 rows/5 events unresolved) resolution checks; no live expansion before event-collapsed results
  - Status: ⚠ Warnings: deterministic settlement killed | crypto DS micro-pilots source-blocked | contrarian pilots killed | non-strategy legacy/manual open position present
  - [2.1] Mean Reversion (YES-only)  |  Status: PERMANENT_KILL 2026-05-21 (lifetime breaker breached; Kelly 0.625x rollback failed; no revival authorized)
  - Record: 168W-30L (85%) | P&L: +$488.51
  - Today's P&L: +$0.00
  - Lifetime breaker ledger (reset_at 2026-05-13 19:39:42-0500): +$0.00 / -$3,000.00 limit | ✓ SAFE
  - Blocked candidates today: 0 | lifetime: 0 | shadow resolved: 0 | hypothetical P&L +$0.00
  - Captured rows today: 0 | lifetime: 0 | resolved: 0 | blocked-wins: 0 | blocked-losses: 0
  - Hypothetical block P&L: +$0.00 (positive = guard would have helped) | activation review at n>=30 independent events

### ibkr
- unit: ibkr-scan-loop.service
- active: inactive/dead
- pid: 0
- nrestarts: 0
- active_enter: n/a
- reconciliation:
  - Formula: expected cash/NLV uses broker_ledger realized P&L + latest Flex statement snapshot
  - ⚠️ HARD CHECK FAILED — cash gap $UNAVAILABLE
  - Expected cash = deposits + realized + market data fees + incentive income - cost = $1949.51
  - Cash gap: UNAVAILABLE
- selected env:
- strategy/cohort excerpts:
  - MODE: LIVE — KILLED (KILL_LIVE_TRADING present)
  - Lifetime P&L: -$5.55 across 773 resolved trades
  - 24h P&L: +$0.00 (0W-0L resolved, 0 placed)
  - SELF-MANAGED ACTIVITY (last 24h):
  - Decisions: Weather DS post-fix pilot is active for UHBNA lt2/UHBNA 2-5/UHPHX 2-5/UHSFO 5-8/UHSFO ge8 under qty 10 and pre-committed rollback gates; Spread Capture buy-only pilot is paused to new entries after 1h lifetime evidence for WEATHER/10-20c/<50c/buy_only turned negative; existing filled rows resolve naturally; no autonomous scaling decision has met evidence gate.
  - Pilots: Weather DS cohort since 2026-05-16 20:55:30: 0 placed, 0 resolved, 0 open, $0.00 open cost, latest=none.
  - Cohort gates: Weather DS scale review needs each of 5 live cells at n>=15 forward resolved; aggregate resolved 0, aggregate remaining at least 75; no scale action due.
  - [2.1] BOT STRATEGY FAMILY — split by cohort:
  - Mode: KILLED — /home/eric-king/.openclaw/workspace/ibkr_forecast_bot/KILL_LIVE_TRADING
  - Aggregate bot_strategy since 2026-05-03: 0 placed | 0 resolved (0W-0L) | P&L +$0.00 | avg/resolved +$0.00 | underliers collecting
  - [bot_strategy_short_fx_qty150] Short-FX qty-150 cohort: 0 placed | 0 resolved (0W-0L) | P&L +$0.00 | open 0 | avg qty 0.0 | avg cost $0.00 | daily CB +$0.00 / $-200.00 | rollback ARMED
  - Qty-150 rollback gates: 2L/10=0/2 | 3L/30=0/3 | daily_pre_n20=+$0.00/-$300.00 (n=0) | lifetime=+$0.00/-$200.00 | max_single_loss=+$0.00/-$130.00 | breaches=none
  - [bot_strategy_short_fx_qty100] Short-FX cohort: 0 placed | 0 resolved (0W-0L) | P&L +$0.00 | open 0 | avg qty 0.0 | avg cost $0.00 | cap-limited 0 | daily CB +$0.00 / $-200.00
  - [bot_strategy_long_fx_qty30] Long-FX cohort: status PAUSED_EMPTY_SURFACE (paused_empty_surface_ec_2026_05_22) | 0 placed | 0 resolved (0W-0L) | P&L +$0.00 | open 0 | avg qty 0.0 | avg cost $0.00 | daily CB +$0.00 / $-50.00 | lifetime CB +$0.00 / $-150.00
  - [bot_strategy_legacy_qty60] Legacy pre-split cohort: 0 placed | 0 resolved (0W-0L) | P&L +$0.00 | preserved for history, not a current expansion signal
  - Entry: categories FX only | cells JPUSD/NO 24-60h, USCAD/YES 24-60h, USEUR/YES 24-60h, USGBP/YES 48-60h | bid $0.85-$0.95 | min expiry 24h | max expiry 60h | max spread $0.10 | order LIMIT at ASK
  - Qty-150 cohort: START not_set | active qty 60 | rollback-to-100 flag absent | pre-committed gates 2L/10, 3L/30, daily CB -$300 before n=20, lifetime CB -$200, single loss > $130
  - Qty-100 cohort: START 2026-05-17T18:48:00-05:00 | preserved as prior sizing measurement | prior qty-60 rows preserved
  - Qty-30 long-FX cohort: PAUSED (paused_empty_surface_ec_2026_05_22) | START 2026-05-22T09:33:00-05:00 | underliers JPUSD/USCAD/USEUR/USGBP | expiry 48-168h | qty 30 | max open 10 | CB daily $-50 lifetime $-150 | reactivation requires fresh venue contracts plus operator decision | USCAD/NO excluded
  - [bot_strategy_ibkr_econ_pilot] ECONOMICS pilot: 0 placed | 0 resolved (0W-0L) | P&L +$0.00 | open 0 | open exposure $0.00/$50.00 | lifetime exposure tracked $0.00 / cap UNLIMITED | kill switch absent | breaches none

### kalshi
- unit: kalshi-bot.service
- active: active/running
- pid: 9240
- nrestarts: 0
- active_enter: Fri 2026-07-03 09:09:17 CDT
- reconciliation:
  - Reconciliation: resolved_pnl=$-1500.51 open_cost=$0.47 open_fees=$0.03 recon_adj=$189.84 expected_cash=$1188.83 cash_gap=$+0.00 unrealized=$-0.44 [MATCH]
  - ✓ HARD CHECK PASSED — gap $0.00
  - Reconciliation adjustment: $189.84 (auto-computed from exchange balance)
  - Expected cash: $1188.83
  - Actual cash (API): $1188.83
- selected env:
  - `BTC_DS_PRICE_CEILING_H5_THRESHOLD=0.97`
  - `BTC_DS_PRICE_CEILING_H6_THRESHOLD=0.95`
  - `BTC_DS_PRICE_CEILING_SHADOW_ENABLED=true`
  - `BTC_DS_PRICE_CEILING_SHADOW_START=2026-05-16 10:12:30-0500`
  - `DETERMINISTIC_SETTLEMENT_ALLOWED_ASSETS=ETH`
  - `DETERMINISTIC_SETTLEMENT_BTC_KILL_SWITCH=/home/eric-king/kalshi_favorites_bot/KILL_DETERMINISTIC_SETTLEMENT_BTC`
  - `DETERMINISTIC_SETTLEMENT_DAILY_CB=-600`
  - `DETERMINISTIC_SETTLEMENT_DAILY_RESET_AT=2026-05-13 12:52:04-05:00`
  - `DETERMINISTIC_SETTLEMENT_ENABLED=true`
  - `DETERMINISTIC_SETTLEMENT_FX_ALLOWED_SERIES=KXEURUSD,KXUSDJPY`
  - `DETERMINISTIC_SETTLEMENT_FX_DAILY_CB=-150`
  - `DETERMINISTIC_SETTLEMENT_FX_EDGE_THRESHOLD=0.60`
  - `DETERMINISTIC_SETTLEMENT_FX_ENABLED=false`
  - `DETERMINISTIC_SETTLEMENT_FX_KILL_SWITCH=/home/eric-king/kalshi_favorites_bot/KILL_DETERMINISTIC_SETTLEMENT_FX`
  - `DETERMINISTIC_SETTLEMENT_FX_LIFETIME_CB=-400`
  - `DETERMINISTIC_SETTLEMENT_FX_MAX_OPEN=4`
  - `DETERMINISTIC_SETTLEMENT_FX_PER_TRADE_MAX=50`
  - `DETERMINISTIC_SETTLEMENT_FX_QTY=50`
  - `DETERMINISTIC_SETTLEMENT_INDEX_ALLOWED_SERIES=KXINX,KXNASDAQ100`
  - `DETERMINISTIC_SETTLEMENT_INDEX_DAILY_CB=-200`
  - `DETERMINISTIC_SETTLEMENT_INDEX_EDGE_THRESHOLD=0.60`
  - `DETERMINISTIC_SETTLEMENT_INDEX_ENABLED=false`
  - `DETERMINISTIC_SETTLEMENT_INDEX_KILL_SWITCH=/home/eric-king/kalshi_favorites_bot/KILL_DETERMINISTIC_SETTLEMENT_INDEX`
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
  - `DS_KALSHI_LOW_PRICE_NO_KILL_SWITCH=/home/eric-king/kalshi_favorites_bot/KILL_DS_LOW_PRICE_NO_PILOT`
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
  - Lifetime P&L: -$1,242.55 across 3211 resolved trades
  - 24h P&L: -$1.62 (1W-2L resolved, 3 placed)
  - Historical realized buckets (16; sum must equal lifetime):
  - • [Kalshi] Kalshi Live Pilot Crypto Last Hour Btc Moderate 80 90 No V1: -$0.81 | 0W-1L | realized rows: 1 | fees: $0.01
  - ✓ Kalshi: lifetime -$1,242.55 / 3211 realized rows; bucket sum -$1,242.55 / 3211 rows
  - Status: ⚠ Warnings: deterministic settlement kill switch | deterministic settlement btc kill switch | deterministic settlement fx kill switch | deterministic settlement index kill switch | ds low price no pilot kill switch | kalshi crypto no lt10c first eligible pilot kill switch | kalshi crypto no lt10c non04z first eligible pilot kill switch | kalshi ds btc moderate yes kill switch | ladder coherence sniper kill switch | ladder sniper v2 kill switch | ladder sniper v2.dt t3 archive 1779388145 kill switch | ladder sniper v2.dv archive 1779424356 kill switch | longshot kill switch | longshot fading kill switch | maker kill switch | mean reversion kill switch | moderate favorites kill switch | sports ds mlb pilot kill switch
  - Record: 251W-38L (87%) | P&L: -$107.67
  - Status: KILLED 2026-05-17 (KILL_MEAN_REVERSION)
  - Kill reason: post-cutoff allowed cohort -$730.69; 84.2% nonzero WR vs 91.0% breakeven
  - ✓ Weather-high blocked (80% WR, -$930 lifetime)
  - ✓ BTC blocked (53 resolved, -$173 lifetime; tail-loss asymmetry)
  - ✓ ETH fully blocked from MR (16W-2L, -$258 lifetime; tail-loss asymmetry)
  - ✓ WEATHER_LOW fully blocked from MR (29W-4L, -$678.44 lifetime; loss-asymmetry on both sides)
  - ✓ SOL fully blocked from MR (30W-6L, -$109.04 lifetime; tail-loss asymmetry)
  - 24h: 0 placed | 0W-0L resolved | P&L +$0.00
  - Forward allowed-cell tracker: start 2026-05-07 20:20:23 UTC | 0W-0L (0.0%) | P&L $+0.00 | open 0 ($0.00 cost)
  - WEATHER_LOW YES cap pilot: 0W-0L (0%) | P&L +$0.00 | open 0 ($0.00) | blocks 0/0 attempts | review 0/30 resolved
  - 24h resolved by hour: morning 0-10 CDT 0W-0L (+$0.00) | afternoon 15-20 CDT 0W-0L (+$0.00)
  - Eligible in 4-8h band (would be blocked): observed 13 | resolved 11 | WR 81.8% | P&L without block -$6.26
  - Eligible outside 4-8h band (would still place): observed 23 | resolved 23 | WR 87.0% | P&L +$67.37
  - [2.3D] Ladder Coherence Sniper Micro-Pilot
  - [2.3E] Kalshi Ladder Sniper V2 (Redesigned Execution)
  - Cohort start: 2026-05-17 16:34:42+0000 | Strategy identity: ladder_sniper_v2
  - [2.3G] Kalshi Ladder Sniper V3 (Maker-Side Dry-Run Candidate)
  - BTC MODERATE-FAVORITE YES DS PILOT (FK_2026_05_26, LIVE):
  - Strategy: bot_strategy_kalshi_ds_btc_moderate_favorite_yes_pilot
  - BTC MODERATE V2 FS SHADOW:
  - SHADOW: Longshot Fading (research-backed)
  - Live-matched v2 (full filter stack): 348W-13L (96.4%) | maker +$1,317.00  -> taker +$574.04
  - Live-matched v2 first-ticker: 229W-13L (94.6%) | taker -$116.93 | Wilson 91.0% vs BE 95.1% | 7d -$353.17 | gate=NOT_LIVE_DEPLOYABLE
  - v1→v2 drops: tier=4981, volume=2791, excluded=1149, category=173, spread=56, nws=52, hours=36
  - [2.5] Moderate Favorites Pilot ($0.80-$0.85 only)
  - Validation vs shadow: shadow WR 83.0% / -$108.00 (spread<=0.05 + allowed assets, matches pilot) | live WR 82.8% | shadow P&L negative; no revival
  - No-revival audit: late-settled live rows do not override the permanent kill; the matching shadow bucket remains loss-asymmetric after fees and repeated observations.
  - Scale-up criteria: disabled while KILL_MODERATE_FAVORITES is present; any revival requires a new forward-only strategy identity and explicit operator approval.
  - Mean reversion shadow freshness: last_row=2026-04-22T03:02:54Z age=72.8d live_match_last=2026-04-21T02:43:31Z post_kill_shadow_rows=0 post_kill_live_placements=0 | gate=STALE_NO_FORWARD_EVIDENCE
  - Forecast accuracy (live-matched 0.85-0.90): 182W-23L (88.8%) | -$613.59
  - Forecast accuracy first-ticker live-match: 178W-21L (89.4%) | -$327.91 | Wilson 84.4% vs BE 90.3% | gate=CONTINUE_SHADOW
  - Forecast accuracy YES 90-93 above-live-threshold: event-first 118W-2L n=120 | +$1,514.16 avg_ask=0.915 | Wilson 94.1% vs BE 92.6% margin=+1.6pp | recent 38W-1L n=39 Wilson 86.8% vs BE 92.7% | pending=3 stale_pending=0 | gate=THIN_MARGIN_RECENT_UNDERPOWERED_FORWARD_ONLY | next_pending=KXLOWTPHIL-26JUL03-B82.5 city=PHIL due=2026-07-04T04:59:59.757304+00:00 ask=0.92 reason=ask_above_max(0.92>0.90)
  - Forecast accuracy high-ask NO event-first: ask>=0.98 all 949W-5L n=954 | +$1,559.40 avg_ask=0.986 | Wilson 98.8% vs BE 98.8%
  - Forecast accuracy high-ask NO ex-LAX: 871W-2L n=873 | +$1,941.78 avg_ask=0.986 | Wilson 99.2% vs BE 98.8% | unresolved_live_est_events=41 | gate=FORWARD_WATCH_ONLY
  - Forecast accuracy high-ask NO native preflight: rows=48990 events=196 actionable_qty1=862 latest=2026-07-03T23:00:25+00:00 | reasons: missing_native_no_ask=43382, nonpositive_qty1_win:0.0000=3250, actionable_qty1_fee_positive=862, native_no_ask_out_of_band:0.9700=274 | latest_run=2026-07-03T23:00:25+00:00 candidates=20 checked=20 actionable=0 run_reasons={"missing_native_no_ask": 18, "native_no_ask_out_of_band:0.0100": 1, "native_no_ask_out_of_band:0.9300": 1}
  - Forecast accuracy high-ask NO latest actionables: captured=2026-07-03T23:00:25+00:00 events=20 actionable_events=0 top_reason=missing_native_no_ask
  - Forecast accuracy high-ask NO native gate: native_events=48 resolved=45 pending=3 43W-2L native_pnl=-$1.55 Wilson 85.2% vs BE 99.0% next_pending=KXLOWTNYC-26JUL03-T77 city=NYC event=KXLOWTNYC-26JUL03 due=2026-07-04T19:00:00+00:00 ttl=37.4h no_ask=0.98 depth=100.00 win1=+$0.01 loss1=-$0.99
  - Forecast accuracy NO candidate-cell preflight: rows=32914 cohorts=2 events=76 actionable_qty1=9030 latest=2026-07-03T23:03:40+00:00 | latest_run=2026-07-03T23:03:40+00:00 candidates=16 checked=16 actionable=4 run_reasons={"no_90_95_min_probe_v1:native_no_ask_out_of_band:0.9700": 1, "no_90_95_min_probe_v1:native_no_ask_out_of_band:0.9800": 1, "no_95_98_zero_loss_cities_v1:actionable_qty1_fee_positive": 4, "no_95_98_zero_loss_cities_v1:missing_native_no_ask": 6, "no_95_98_zero_loss_cities_v1:native_no_ask_out_of_band:0.7700": 1, "no_95_98_zero_loss_cities_v1:native_no_ask_out_of_band:0.9900": 3}
  - Forecast accuracy NO candidate-cell cohorts: no_95_98_zero_loss_cities_v1 rows=29745 events=75 actionable=8229; no_90_95_min_probe_v1 rows=3169 events=10 actionable=801
  - Forecast accuracy NO candidate-cell latest cohort actionables: no_90_95_min_probe_v1 captured=2026-07-03T23:03:40+00:00 events=2 actionable_events=0 top_reason=native_no_ask_out_of_band:0.9800; no_95_98_zero_loss_cities_v1 captured=2026-07-03T23:03:40+00:00 events=14 actionable_events=4 best=KXLOWTMIA-26JUL04-B74.5 city=MIA event=KXLOWTMIA-26JUL04 due=2026-07-05T19:00:00+00:00 no_ask=0.96 depth=1.36 win1=+$0.03 loss1=-$0.97
  - Forecast accuracy NO candidate-cell historical control: all-city 95-98 905W-25L n=930 Wilson 96.1% vs BE 96.7%; selected-cities 310W-2L n=312 Wilson 97.7% vs BE 96.8%; weakest_city=AUS 40W-1L n=41 Wilson 87.4% vs BE 96.8% | selected-city filter is in-sample; no live order
  - Forecast accuracy NO candidate-cell forward gate: no_90_95_min_probe_v1 native_events=10 resolved=8 pending=2 7W-1L native_pnl=-$0.58 Wilson 52.9% vs BE 94.6% next_pending=KXHIGHTMIN-26JUL03-B87.5 city=MIN event=KXHIGHTMIN-26JUL03 due=2026-07-04T19:00:00+00:00 ttl=37.7h no_ask=0.91 depth=1.00 win1=+$0.08 loss1=-$0.92; no_95_98_zero_loss_cities_v1 native_events=71 resolved=58 pending=13 56W-2L native_pnl=-$0.56 Wilson 88.3% vs BE 97.5% next_pending=KXHIGHMIA-26JUL03-B88.5 city=MIA event=KXHIGHMIA-26JUL03 due=2026-07-04T14:00:00+00:00 ttl=32.7h no_ask=0.96 depth=25.96 win1=+$0.03 loss1=-$0.97
  - Legacy untapped FX/Index NO shadow: bid=0.85-0.90 12-24h first-ticker-side 483W-33L n=516 | +$3,334.03 | avg_bid=0.865 | Wilson 91.2% vs modeled BE 87.1% margin=+4.1pp | pending=0 | gate=LEGACY_MAKER_FORWARD_REQUIRED
  - Legacy untapped FX/Index NO recency: since_2026-06-17 157W-8L n=165 +$1,287.11 pending=0 Wilson 90.7% vs modeled BE 87.2% | forward_since_2026-06-25T09:25Z resolved=80 pending=0 | KXEURUSD 25W-2L pending=0, KXINX 26W-2L pending=0, KXNASDAQ100 16W-0L pending=0, KXUSDJPY 27W-1L pending=0 | next_pending=none | bid-side/maker-priced shadow, not taker-executable
  - Legacy untapped FX/Index NO event collapse: event-side 94W-5L n=99 +$725.55 pending=0 Wilson 88.7% vs modeled BE 87.6% margin=+1.2pp | recent_event_side 36W-2L n=38 Wilson 82.7% vs BE 87.5% | forward_event_side resolved=17 pending=0 | gate=RECENT_EVENT_UNDERPOWERED_MAKER_FORWARD_REQUIRED
  - Legacy untapped FX/Index NO maker/cancel proxy: v2 side_bid=0.85-0.90 candidates=210 markets=30 fills=24 pending_fills=0 resolved_indep=24/50 22W-2L pnl=+$2.78 Wilson 74.2% vs modeled BE 90.4% | cancels=186 late_cross_ttl=6 open=0 | gate=MAKER_FILL_FORWARD_REQUIRED
  - Legacy weather-city NO shadow: bid>=0.88 first-ticker-side 5446W-260L n=5706 | +$10,365.36 | avg_bid=0.932 | Wilson 94.9% vs modeled BE 93.6% margin=+1.2pp | pending=215 | gate=LEGACY_MAKER_FORWARD_REQUIRED
  - Legacy weather-city NO recency: since_2026-06-17 2034W-81L n=2115 +$4,049.69 pending=213 Wilson 95.3% vs modeled BE 94.3% | forward_since_2026-06-25T09:35Z resolved=972 pending=213 | blocked 1562W-86L +$1,981.40, unblocked 3884W-174L +$8,383.96 | best=KXLOWTNYC 224W-5L +$1,073.43; worst=KXLOWTDEN 225W-19L -$364.54 | next_pending=KXHIGHPHIL-26JUL03-B101.5 city=PHIL due_est=2026-07-04T04:58:59.039229+00:00 ttl_at_capture=14.0h bid=0.90 overdue_pending=2 | bid-side/maker-priced shadow, not taker-executable
  - Legacy weather-city NO event collapse: event-side 1086W-18L n=1104 +$3,804.55 pending=48 Wilson 97.4% vs modeled BE 94.9% margin=+2.5pp | recent_event_side 399W-9L n=408 Wilson 95.9% vs BE 95.5% | forward_event_side resolved=192 pending=48 | gate=EVENT_MAKER_FORWARD_REQUIRED
  - Legacy weather-city NO maker/cancel proxy: v2 side_bid>=0.88 candidates=115 markets=57 fills=36 pending_fills=6 resolved_indep=30/50 30W-0L pnl=+$19.74 Wilson 88.6% vs modeled BE 93.4% | cancels=79 late_cross_ttl=16 open=0 | gate=MAKER_FILL_FORWARD_REQUIRED
  - Crypto price-range bid-side shadow: side-aware ticker+side first rows 598W-0L n=598 | +$3,690.02 | Wilson 99.4% vs modeled BE 93.8% | pending=0 | gate=MAKER_FILL_FORWARD_REQUIRED
  - Crypto price-range bid-side recency: since_2026-06-17 120W-0L n=120 +$725.58 pending=0 | forward_since_2026-06-25T07:30Z resolved=73 pending=0 | YES 59W-0L pending=0, NO 44W-0L pending=0 | bid-side shadow, not taker-executable
  - Crypto price-range bid-side event collapse: event-side 103W-0L n=103 +$627.56 pending=0 Wilson 96.4% vs BE 93.9% margin=+2.5pp | event_only 70W-0L n=70 Wilson 94.8% vs BE 93.9% margin=+0.9pp | recent_event_side 31W-0L n=31 Wilson 89.0% vs BE 93.9% | forward_event_side resolved=19 pending=0 | gate=RECENT_EVENT_UNDERPOWERED_MAKER_FORWARD_REQUIRED
  - Crypto long-expiry bid-side shadow: 24-72h bid=0.90-0.95 event-side 64W-1L n=65 | +$376.86 | avg_bid=0.921 | Wilson 91.8% vs modeled BE 92.7% margin=-0.9pp | pending=11 | gate=NO_GO_EVENT_ONLY_COLLAPSE
  - Crypto long-expiry bid-side collapse: event_only 36W-0L n=36 +$255.21 Wilson 90.4% vs BE 92.9% | ticker-side_raw 407W-5L n=412 +$2,660.24 pending=93 | YES 35W-0L pending=5, NO 29W-1L pending=6
  - Crypto long-expiry bid-side recency: since_2026-06-17 event-side 19W-1L n=20 +$42.11 pending=7 Wilson 76.4% vs modeled BE 92.9% | forward_since_2026-06-25T09:50Z resolved=5 pending=3 | next_pending=KXETHD-26JUL0417-T1979.99 side=NO due_est=2026-07-04T20:59:59.389264+00:00 ttl_at_capture=24.2h bid=0.94 overdue_pending=10 | bid-side/maker-priced shadow, not taker-executable
  - Crypto long-expiry maker/cancel proxy: v2 crypto side_bid=0.90-0.95 candidates=496 markets=270 fills=110 pending_fills=7 resolved_indep=103/50 95W-8L pnl=-$14.13 Wilson 85.4% vs modeled BE 93.6% | 24hplus_candidates=108 24hplus_fills=14 24hplus_pending_fills=5 | cancels=362 late_cross_ttl=42 open=24 | gate=MAKER_FILL_FORWARD_REQUIRED
  - Crypto price-range maker/cancel shadow: v2 side_bid=0.92-0.94 candidates=264 markets=156 fills=61 filled_units=61 pending_fills=3 resolved_indep=58/50 54W-4L pnl=-$6.17 Wilson 83.6% vs modeled BE 94.2% | cancels=190 late_cross_ttl=23 open=13 | gate=MAKER_FILL_FORWARD_REQUIRED
  - Crypto price-range maker/cancel sides: NO rows=140 markets=76 fills=26 pending=3 resolved_rows=23; YES rows=124 markets=80 fills=35 pending=0 resolved_rows=35 | source=kalshi_high_price_maker_cancel_shadow | no live orders
  - Crypto legacy taker NO shadow: ask=0.90-0.95 12-24h first-ticker-side 244W-15L n=259 | +$565.16 | avg_ask=0.915 | Wilson 90.7% vs modeled BE 92.0% margin=-1.4pp | pending=0 | gate=NO_GO
  - Crypto favorite taker native preflight: rows=9974 cohorts=2 contracts=55 actionable_obs=1975 latest=2026-07-03T23:03:40+00:00 | latest_run=2026-07-03T23:03:40+00:00 candidates=1 checked=1 actionable=0 reasons={"crypto_near_certain_95_99_12_24h:nonpositive_qty1_win:0.0000": 1} | no order path
  - Crypto favorite taker native cohorts: crypto_near_certain_95_99_12_24h rows=7809 contracts=43 actionable_obs=1566; crypto_favorite_no_90_95_12_24h rows=2165 contracts=12 actionable_obs=409
  - Crypto favorite taker latest cohort actionables: crypto_favorite_no_90_95_12_24h captured=2026-07-03T20:58:01+00:00 contracts=2 actionable_contracts=0; crypto_near_certain_95_99_12_24h captured=2026-07-03T23:03:40+00:00 contracts=1 actionable_contracts=0
  - Crypto favorite taker native gate: crypto_favorite_no_90_95_12_24h first_actionable_contracts=10 resolved=10 pending=0 8W-2L native_pnl=-$1.21 Wilson 49.0% vs BE 92.1% gate=NATIVE_FORWARD_ACCUMULATING; crypto_near_certain_95_99_12_24h first_actionable_contracts=40 resolved=39 pending=1 38W-1L native_pnl=-$0.08 Wilson 86.8% vs BE 97.7% next_pending=KXBTCD-26JUL0417-T64499.99 side=NO asset=BTC event=KXBTCD-26JUL0417 due=2026-07-04T20:59:59.946773+00:00 ask=0.97 depth=14.00 win1=+$0.02 loss1=-$0.98 gate=NATIVE_FORWARD_ACCUMULATING
  - Crypto contrarian NO underdog shadow: ask=0.20-0.25 18-24h event-first 21W-41L n=62 +$601.04 avg_ask=0.229 Wilson 23.3% vs modeled BE 24.2% pending=1 active_pending=0 stale_pending=1 old_live_match_events=5/63 | gate=ALL_PERIOD_BELOW_BREAKEVEN_POSTHOC
  - Crypto contrarian NO recency: since_2026-06-17 13W-14L n=27 +$638.16 pending=0 Wilson 30.7% vs modeled BE 24.5% | forward_since_2026-06-25T10:40Z resolved=9 pending=0 | 2026-04 8W-27L -$37.12, 2026-06 13W-11L +$711.92 | BTC 8W-18L +$167.58 pending=0, ETH 9W-9L +$477.11 pending=0, SOL 4W-14L -$43.65 pending=1 | next_pending=KXSOLD-26APR2417-T83.9999 event=KXSOLD-26APR2417 due_est=2026-04-24T20:59:59.002927+00:00 ttl=-1682.1h ask=0.22 spread=0.09 active_pending=0 stale_pending=1 unknown_pending=0 | exploratory ask-priced shadow; no live orders
  - Crypto last-hour longshot NO shadow: event-first 1200W-78L n=1278 | +$6,308.33 avg_ask=0.883 | Wilson 92.4% vs modeled BE 89.0% | recent 779W-64L +$2,474.51 | gate=LIQUIDITY_PROXY_FAIL_FORWARD_ONLY
  - Crypto last-hour longshot liquidity: volume=0 603W-9L +$6,825.14; volume>=500/spread<=5c 390W-42L -$192.33 Wilson 87.1% vs BE 90.7%; 80-85c volume-backed 39W-5L +$210.06 Wilson 76.0% vs BE 83.9%; 90-95c volume-backed 258W-21L -$99.49 Wilson 88.8% vs BE 92.8%; 95-99c volume-backed 587W-23L -$550.52 Wilson 94.4% vs BE 97.1%; forward_since_2026-06-25T11:20Z 403W-40L +$488.73 Wilson 87.9% vs BE 89.9% resolved=443 pending=0 | no live orders
  - Crypto last-hour longshot native preflight: rows=5731 events=442 actionable_qty1=1544 latest=2026-07-03T22:55:26+00:00 | latest_run=2026-07-03T23:03:40+00:00 candidates=0 checked=0 actionable=0 reasons={} | no order path
  - Crypto last-hour longshot latest actionables: captured=2026-07-03T22:55:26+00:00 events=3 contracts=3 actionable_contracts=0 top_reason=missing_native_no_ask
  - Crypto last-hour longshot native gate: native_events=332 resolved=332 pending=0 active_pending=0 stale_pending=0 unknown_pending=0 298W-34L native_pnl=-$3.44 Wilson 86.0% vs BE 90.8% | gate=NATIVE_FORWARD_ACCUMULATING
  - SOL vol model executable shadow: would_place_live row 47W-38L resolved=86 -$1,824.00 flat=1 pending=5 | first-ticker 35W-11L resolved=46 +$157.00 pending=2 | first-event 7W-4L resolved=11 -$108.00 pending=1 avg_ask=0.685 Wilson 35.4% | gate=EVENT_FORWARD_RECENCY_FAIL
  - SOL vol model recency: since_2026-06-17 first-event 2W-3L resolved=5 -$186.00 Wilson 11.8% | last_candidate=2026-06-29 02:15:07 | live_placements=0 open=0 | stored taker-fee P&L; no new live orders
  - Weather near-expiry favorite shadow: 1-4h ask>=0.90 event-first 47W-0L n=47 +$265.00 avg_ask=0.944 Wilson 92.4% vs modeled BE 94.7% pending=0 overdue_pending=0 | gate=UNDERPOWERED_BELOW_BREAKEVEN
  - Weather near-expiry favorite recency: since_2026-06-17 32W-0L n=32 +$189.00 pending=0 Wilson 89.3% vs modeled BE 94.5% | best_event_price_cell=2-4h/p90_95 28W-0L n=28 +$212.00 pending=0 | next_pending=none | ask-priced near-expiry shadow; no live orders
  - Commodity WTI high-bid blocked shadow: NO first-market 174W-5L n=179 +$854.40; event-side 22W-1L n=23 +$60.78 Wilson 79.0% vs BE 93.0% | YES first-market 113W-6L n=119 +$259.33; event-side 22W-3L n=25 -$116.69 Wilson 70.0% vs BE 92.7% | gate=EVENT_FORWARD_N50_REQUIRED
  - Commodity WTI blocked recency: since_2026-06-17 event-side NO 6W-0L n=6 +$35.48 pending=0, YES 4W-1L n=5 -$66.35 pending=0 | blocked-category diagnostic; no live orders
  - Commodity WTI contrarian NO longshot: event-side 5W-15L n=20 +$201.06 Wilson 11.2% vs BE 14.9% pending_events=0 | first-market 12W-57L n=69 +$391.09 | gate=EVENT_FORWARD_N50_REQUIRED
  - Commodity WTI contrarian recency: since_2026-06-17 event-side 2W-8L n=10 +$49.45 pending=0 | ask-priced live_match; high-variance longshot; no live orders
  - [2.3I] High-Price Maker/Cancel Shadow
  - Cohort: fx_aq_high_price_maker_cancel_shadow_600s_2026_06_24 | scanner=v2_high_price_maker_cancel_ttl_precedence_600s
  - Protocol: discovery cadence target 300s | quote TTL 600s | series fetch delay 2.0s | TTL checked before fill simulation.
  - Summary: rows=7431 open=199 fills=1903 markets=1720 cancels=5329 late_cross_ttl=464 resolved=1392 markets=1290 pnl=-3040.11 last=2026-07-03T23:00:11+00:00
  - Pending fills: unresolved=511 markets=430 next=KXMLBSPREAD-26JUN301905DETNYY-DET3 sports NO close=2026-07-03T23:05:00+00:00 expiration=2026-07-03T23:05:00+00:00 | units=511 active=511 stale=0 unknown=0
  - Overall independent fills: resolved=1392 915W-477L pnl=-3040.11 wilson_low=63.2% breakeven=87.6% toxic=477 status=NO_GO_REVIEW
  - Review progress: best_cell=sports NO resolved_independent=408/50 indep=316W-92L pnl=-410.30 wilson_low=73.2% breakeven=87.5% toxic=92 pending_markets=298 filled_markets=706 next_close=2026-07-03T23:05:00+00:00 status=NO_GO_REVIEW
  - Cell scan: resolved_cells=7 edge_positive_cells=0 leader=sports NO resolved_indep=408 best_edge_positive=none best_alternate=crypto YES resolved_indep=320 176W-144L pnl=-1002.41 wilson_low=49.5% breakeven=86.3% toxic=144 status=NO_GO_REVIEW
  - KALSHI CRYPTO LOW-PRICE NO CELL AUDIT
  - Status: SHADOW_ONLY | broad low-price NO kill=present | standard DS kill=present
  - NO <10c first-market: n=6 4W-2L wr=66.7% wilson_low=30.0% breakeven=5.0% pnl=+3.72 avg=+0.6200
  - NO <10c first-eligible: n=6 4W-2L wr=66.7% wilson_low=30.0% breakeven=5.0% pnl=+3.72 avg=+0.6200
  - NO <10c concentration: underliers=2 top=BTC n=5 share=83.3% pnl=+2.82 worst=SOL n=1 pnl=+0.90
  - NO <10c day stability: days=1 positive=1 losing=0 worst=2026-06-27 n=6 pnl=+3.72
  - NO <10c UTC-hour stability: hours=2 positive=2 losing=0 worst=12Z n=4 pnl=+1.79
  - Post-kill NO <10c first-market: n=6 4W-2L wr=66.7% wilson_low=30.0% breakeven=5.0% pnl=+3.72 avg=+0.6200
  - Post-kill NO <10c first-eligible: n=6 4W-2L wr=66.7% wilson_low=30.0% breakeven=5.0% pnl=+3.72 avg=+0.6200
  - Review: post-kill NO <10c first-eligible progress 6/50 status=ACCUMULATING reason=native taker NO ask <10c evidence absent
  - Post-kill NO <10c first-eligible concentration: underliers=2 top=BTC n=5 share=83.3% pnl=+2.82 worst=SOL n=1 pnl=+0.90
  - Post-kill NO <10c first-eligible day stability: days=1 positive=1 losing=0 worst=2026-06-27 n=6 pnl=+3.72
  - Post-kill NO <10c first-eligible UTC-hour stability: hours=2 positive=2 losing=0 worst=12Z n=4 pnl=+1.79
  - Post-kill NO <10c first-eligible loss cluster: losses=2 loss_hours=1 top_hour=12Z top_hour_losses=2/2 share=100.0% top_underlier=BTC 2/2 | excluding_top_loss_hour=POST_HOC_FORWARD_ONLY n=2 2W-0L pnl=+1.93 Wilson 34.2% vs modeled BE 3.7%
  - Post-kill NO <10c first-eligible source provenance: rows=6 sources=1 top=kalshi.shadow_deterministic_settlement n=6 distinct_source_row_ids=6 missing_source_row_ids=0
  - Post-kill NO <10c first-eligible native source check: source_ids=6 checked=5 native_taker_ask_lt10c=0/5 min=0.7300 avg=0.9360 max=0.9900
  - Fresh non-04Z NO <10c first-eligible: n=6 4W-2L wr=66.7% wilson_low=30.0% breakeven=5.0% pnl=+3.72 avg=+0.6200
  - Forward gate: fresh non-04Z NO <10c first-eligible start=2026-06-25T08:30:00+00:00 excluded_hour=04Z progress 6/50 pending_markets=0 status=ACCUMULATING reason=resolved 6/50; needs 44 new markets after pending; native taker NO ask <10c evidence absent
  - Fresh non-04Z NO <10c first-eligible pending horizon: resolved=6/50 pending_markets=0 max_if_all_pending_resolve=6/50 need_new_after_pending=44 next_due=unknown last_due=unknown next_backfill_after=unknown last_backfill_after=unknown
  - Fresh 04Z excluded-control NO <10c first-eligible: no resolved rows
  - Fresh non-04Z NO <10c first-eligible source provenance: rows=6 sources=1 top=kalshi.shadow_deterministic_settlement n=6 distinct_source_row_ids=6 missing_source_row_ids=0
  - Fresh non-04Z NO <10c first-eligible native source check: source_ids=6 checked=5 native_taker_ask_lt10c=0/5 min=0.7300 avg=0.9360 max=0.9900
  - Fresh non-04Z NO <10c first-eligible concentration: underliers=2 top=BTC n=5 share=83.3% pnl=+2.82 worst=SOL n=1 pnl=+0.90
  - Fresh non-04Z NO <10c first-eligible day stability: days=1 positive=1 losing=0 worst=2026-06-27 n=6 pnl=+3.72
  - Fresh non-04Z NO <10c first-eligible UTC-hour stability: hours=2 positive=2 losing=0 worst=12Z n=4 pnl=+1.79
  - Post-kill pending NO: rows=0 markets=0 actionable=0 qty50=0 avg_price=n/a first=none last=none
  - Post-kill pending NO <10c first-eligible: rows=0 markets=0 actionable=0 qty50=0 avg_price=n/a first=none last=none
  - Post-kill NO <10c first-eligible pending horizon: resolved=6/50 pending_markets=0 max_if_all_pending_resolve=6/50 need_new_after_pending=44 next_due=unknown last_due=unknown next_backfill_after=unknown last_backfill_after=unknown
  - Post-kill NO <10c first-eligible live pending preview: pending_first_eligible=0 live_actionable=0 settlement_pending_or_ineligible=0 now=2026-07-03T23:04:10+00:00 | no order path
  - Pilot readiness: NOT_READY | proposed_strategy=kalshi_crypto_no_lt10c_first_eligible_pilot | new identity required; do not revive ds_low_price_no | reason=resolved 6/50; needs 44 new markets after pending; native taker NO ask <10c evidence absent
  - DS CONTRACT-HOUR CLUSTER CAP TRACKER:
  - Shadow blocked candidates: 138 total | 50 resolved (50W-0L) | qty-backed causal 0/50 resolved | P&L unavailable: resolved rows have candidate_qty=0/non-causal; stored +$0.00 is not economic
  - Review note: blocked rows are win-heavy but non-causal/zero-qty; max3 cap has no qty-backed forward proof
  - Gate: qty-backed blocked rows n>=50, positive hypothetical P&L, loss rate compatible with ~2.26% projection, no daily CB breach
  - KALSHI DS MAKER-SHADOW TRACKER:
  - Captured rows: 71 (68 resolved) | maker fill rate: 11.8%
  - Actual taker P&L: +$39.58 | hypothetical maker filled-only P&L: -$654.29 | net delta: -$693.87 | fee savings if filled: -$32.14
  - Per-asset breakdown:
  - ETH: 71 captured (68 resolved), maker fill 11.8%, maker -$654.29, aggressive -$291.63, net delta -$693.87
  - Review: ETH 68/100 NEGATIVE_INTERIM_TAKER_NECESSARY fill=11.8% delta=-$693.87
  - Gate: n>=100 resolved per asset | no maker conversion unless maker P&L beats taker with >=80% fill
  - FX first-symbol: 9W-134L n=143 | P&L -$1,167.06 | Wilson 3.3% vs BE 23.6% | native_NO 100.0% | side_match 100.0% | live YES/NO 136/7
  - INDEX first-symbol: 22W-369L n=391 | P&L -$498.56 | Wilson 3.7% vs BE 8.3% | native_NO 100.0% | side_match 100.0% | live YES/NO 391/0
  - Raw predicate: 43W-9L n=52 | P&L -$52.70 | Wilson 70.3% vs BE 86.7%
  - First-symbol: 39W-8L n=47 | P&L -$43.68 | Wilson 69.9% vs BE 86.7%
  - Pending predicate rows: 0
  - Review: first-30 progress 52/30 status=FAILED
  - KALSHI INDEX/FX SIDE-EQUIVALENCE FS SHADOW
  - Status: REJECTED_NATIVE_CONTROL | no live pilot
  - Pending native-actionable rows: FX=3157
  - Gate: failed; native executable rows disprove Index/FX favorite-tracking salvage

## Storage State
- DATABASE STORAGE HEALTH
-   Overall status: GREEN / TARGET
-   Disk: 165.45 GiB used / 936.79 GiB total (17.7%), 723.68 GiB free
-   Envelope: TARGET 50.0%, WARN 65.0%, CRITICAL 75.0%, HARD_LIMIT 85.0%
-   DS storage: active 1.09 GiB (state TARGET), hot 27.90 GiB, warm 0.03 GiB, cold 0.00 GiB, archive_state TARGET, total 30.09 GiB (3.2% of disk)
-   Archive sidecars: OK
-   Retention engine: last=2026-07-01T18:17:00+00:00 status=OK dry_run=False rows_selected=1 rows_archived=1 rows_pruned=0
-   Archive compression: status=OK actions=0 warm_days=7 min_file_mb=100
-   Tier rotation: last=2026-07-03T18:20:36+00:00 status=DRY_RUN actions=2, compression_ratio_avg=0.005
-   Autonomous maintenance: last=2026-07-03T10:47:39+00:00 status=OK backups=4/5 integrity_failures=1 drift_flags=0
-   PROTECT_TRADING mode: NO
-   TOP_RISK: database integrity issue polymarket_shadow status=MISSING

## Kalshi Same-Strike Complementarity
- source: daily-reports/same-strike-rollup-2026-07-01.md
- Date: 2026-07-01 UTC
- Scanner uptime: 23.7% (260 observed scan timestamps)
- Total: 22565
- Crypto: 15591
- Weather: 5198
- FX: 1040
- Index: 736
- descriptive: 0
- fresh_simultaneous: 21229
- execution_ready: 1336
- All tiers: 0 (best edge $-0.0100 on KXBTCD-26JUL0117-T63999.99)
- Fresh simultaneous: 0 (best edge $-0.0100 on KXBTCD-26JUL0117-T63999.99)
- Execution ready: 0 (best edge $-0.0100 on KXHIGHLAX-26JUL01-T72)
- Independent opportunities (deduplicated by market_ticker): 0
- Empirical edge frequency: always tight
- Pilot-decision criteria status: deferred; no strategy attached; broker YES+NO simultaneous holding unverified

## Kalshi Post-Expiration Active Scan
- command: `python3 scripts/kalshi_post_expiration_active_scanner.py --limit 1000 --max-pages 100 --pause-seconds 0.08 --min-age-minutes 1 --max-ask 0.25 --max-spread 0.20 --min-depth 1 --max-candidates 20 --record --json`
- latest_run: id=30 captured_at=2026-07-03T20:17:56+00:00 | markets_seen=100000 post_expiration_open_unresolved=21 candidate_count=0 | direct_market_recheck=True pages=100 page_cap=True rate_limited=False | trigger_fields={"expected_expiration_time": 21} | top_series=KXMVESPORTSMULTIGAMEEXTENDED=19, KXMVECROSSCATEGORY=2

## Kalshi Duplicate Proposition Scan
- command: `python3 scripts/kalshi_duplicate_proposition_scanner.py --series-title-regex '.' --max-series 100 --max-pages-per-series 1 --pause-seconds 0.05 --min-ask-gap 0.10 --min-bid-edge 0.05 --max-cheap-ask 0.75 --min-depth 1 --max-candidates 20 --record --json`
- latest_run: id=32 captured_at=2026-07-03T20:28:04+00:00 | mode=global_open_cursor markets_seen=60000 grouped_markets=59969 duplicate_groups=613 candidate_count=0 | pages=60 page_cap=true rate_limited=false | top_series=KXMVESPORTSMULTIGAMEEXTENDED=49600, KXMVECROSSCATEGORY=9747, KXMLBTB=197, KXMLBHRR=173, KXMLBHIT=148

## Kalshi Binary Complement Scan
- command: `python3 scripts/kalshi_binary_complement_scanner.py --series-title-regex '.' --max-series 100 --max-pages-per-series 1 --pause-seconds 0.05 --min-net-edge 0.005 --min-depth 1 --record --json`
- latest_run: id=29 captured_at=2026-07-03T20:29:24+00:00 | mode=global_open_cursor markets=60000 parsed=0 groups=0 relations=0 candidates=0 | pages=60 page_cap=true rate_limited=false | top_series=KXMVESPORTSMULTIGAMEEXTENDED=49650, KXMVECROSSCATEGORY=9732, KXMLBTB=197, KXMLBHRR=173, KXMLBHIT=148 | parse_rejects=not_strict_binary_labels=60000

## Kalshi Date-Threshold Ladder Scan
- command: `python3 scripts/kalshi_date_threshold_ladder_scanner.py --limit 1000 --max-pages 120 --pause-seconds 0.05 --record --json`
- latest_run: captured_at=2026-07-03T04:40:33+00:00 | mode=whole_universe markets_seen=40000 parsed_markets=0 parsed_events=0 groups=0 orderbooks=0 candidates=0 best_edge=none | pages=40 page_cap=true rate_limited=false | top_series=KXMVESPORTSMULTIGAMEEXTENDED=33943, KXMVECROSSCATEGORY=6047, KXWCGOAL=4, KXITFMATCH=4, KXWCTEAMFIRSTGOAL=2

## Kalshi Series Ladder Dominance Scan
- command: `python3 scripts/kalshi_series_ladder_dominance_scanner.py --series-title-regex '<scalar ladder terms>' --max-series 50 --max-pages-per-series 1 --pause-seconds 0.05 --record`
- latest_run: id=48 captured_at=2026-07-03T20:34:23+00:00 | mode=whole_universe markets=80000 parsed=951 families=506 multi_row=177 relations=459 candidates=0 top_net=-8.0pp | pages=80 page_cap=true rate_limited=false
- nearest_relations: KXMLBTB KXMLBTB-26JUL031910BALCIN at_least loose=KXMLBTB-26JUL031910BALCIN-CINEARROYO56-4(4.0)@0.07 strict=KXMLBTB-26JUL031910BALCIN-CINEARROYO56-5(5.0)@0.99 net=-8.0pp ; KXMLBTB KXMLBTB-26JUL031915NYMATL at_least loose=KXMLBTB-26JUL031915NYMATL-ATLMYASTRZEMSKI18-4(4.0)@0.11 strict=KXMLBTB-26JUL031915NYMATL-ATLMYASTRZEMSKI18-5(5.0)@0.99 net=-12.0pp ; KXMLBHIT KXMLBHIT-26JUL031915NYMATL at_least loose=KXMLBHIT-26JUL031915NYMATL-ATLJMATEO2-2(2.0)@0.11 strict=KXMLBHIT-26JUL031915NYMATL-ATLJMATEO2-3(3.0)@0.99 net=-12.0pp ; KXMLBTB KXMLBTB-26JUL031915NYMATL at_least loose=KXMLBTB-26JUL031915NYMATL-ATLMDUBN14-4(4.0)@0.14 strict=KXMLBTB-26JUL031915NYMATL-ATLMDUBN14-5(5.0)@0.99 net=-15.0pp ; KXMLBTB KXMLBTB-26JUL031910BALCIN at_least loose=KXMLBTB-26JUL031910BALCIN-CINEARROYO56-3(3.0)@0.14 strict=KXMLBTB-26JUL031910BALCIN-CINEARROYO56-5(5.0)@0.99 net=-15.0pp

## Kalshi Interval Partition Scan
- command: `python3 scripts/kalshi_interval_partition_scanner.py --series-title-regex '<numeric/interval terms>' --max-series 50 --max-pages-per-series 1 --pause-seconds 0.05 --record`
- latest_run: id=32 captured_at=2026-07-03T20:31:26+00:00 | mode=global_open_cursor markets=60000 parsed=33721 groups=30923 partitions=0/1880 candidates=0 | pages=60 page_cap=true rate_limited=false | top_series=KXMVESPORTSMULTIGAMEEXTENDED=49670, KXMVECROSSCATEGORY=9755, KXMLBTB=197, KXMLBHRR=173, KXMLBHIT=148 | non_partition=missing_lower_tail=1880

## Kalshi Interval Relation Scan
- command: `python3 scripts/kalshi_interval_relation_scanner.py --series-title-regex '<numeric/interval terms>' --max-series 50 --max-pages-per-series 1 --pause-seconds 0.05 --record`
- latest_run: id=35 captured_at=2026-07-03T20:32:36+00:00 | mode=global_open_cursor markets=60000 parsed=33584 groups=30781 relations=0 candidates=0 | pages=60 page_cap=true rate_limited=false | top_series=KXMVESPORTSMULTIGAMEEXTENDED=49714, KXMVECROSSCATEGORY=9752, KXMLBTB=197, KXMLBHRR=173, KXMLBHIT=147 | parse_rejects=not_interval_title=26416

## Kalshi Threshold Complement Scan
- command: `python3 scripts/kalshi_threshold_complement_scanner.py --series-title-regex '<numeric/interval terms>' --max-series 50 --max-pages-per-series 1 --pause-seconds 0.05 --record`
- latest_run: id=35 captured_at=2026-07-03T20:30:04+00:00 | mode=global_open_cursor markets=60000 parsed=9665 groups=9287 relations=0 candidates=0 | pages=60 page_cap=true rate_limited=false | top_series=KXMVESPORTSMULTIGAMEEXTENDED=49675, KXMVECROSSCATEGORY=9737, KXMLBTB=197, KXMLBHRR=173, KXMLBHIT=148 | parse_rejects=not_single_threshold_title=50335

## Kalshi Post-Close Active Scan
- command: `python3 scripts/kalshi_post_close_active_scanner.py --limit 1000 --max-pages 100 --pause-seconds 0.05 --min-age-minutes 1 --max-ask 0.25 --max-spread 0.15 --min-depth 1 --max-candidates 20 --record`
- latest_run: id=27 captured_at=2026-07-03T20:17:56+00:00 | markets_seen=100000 post_close_open_unresolved=0 candidates=0 min_age_min=1.00 max_ask=0.30 max_spread=0.15 min_depth=1 | pages=100 page_cap=true rate_limited=false | categories=none | top_series=unknown

## Kalshi Public Result Active Scan
- command: `python3 scripts/kalshi_public_result_active_scanner.py --limit 1000 --max-pages 100 --pause-seconds 0.05 --max-ask 0.25 --max-spread 0.15 --min-depth 1 --max-candidates 20 --record`
- latest_run: id=33 captured_at=2026-07-03T21:17:51+00:00 | markets_seen=30000 public_result_active=0 candidates=0 max_ask=0.30 max_spread=0.15 min_depth=1 | pages=30 page_cap=true rate_limited=false | results=none | categories=none | top_series=unknown

## Kalshi Event Result Propagation Scan
- command: `python3 scripts/kalshi_event_result_propagation_scanner.py --limit 200 --max-pages 35 --max-details 1000 --pause-seconds 0.03 --max-ask 0.25 --min-depth 1 --print-limit 20`
- latest_run: id=21 captured_at=2026-07-03T22:14:15+00:00 | version=event_result_propagation_v1 events_seen=7006 events_examined=5109 mutex_events=2001 details=2000/2000 detail_cap=true markets=24389 locked=0 actionable_qty1=0 max_ask=0.25 min_depth=1 | pages=36 page_cap=false rate_limited=false | reasons=event_not_mutually_exclusive_summary=3108, no_exhaustive_proof=2000, detail_cap_reached=1

## Kalshi Event Mutex Bundle Scan
- command: `python3 scripts/kalshi_event_mutex_bundle_scanner.py --event-limit 200 --max-event-pages 80 --max-details 1000 --pause-seconds 0.03 --detail-pause-seconds 0.03 --min-net-edge 0.01 --record`
- latest_run: id=23 captured_at=2026-07-03T21:18:47+00:00 | events_seen=1200 mutex_events=160 details=80/80 markets=648 tradable_no=521 candidates=0 top_net=-3.3pp | pages=6 page_cap=true rate_limited=false | categories=Elections=104, Politics=22, Entertainment=13, Economics=7, Financials=6, Sports=4 | detail_errors=none
- nearest_no_bundles: KXNEXTUKPM-30 KXNEXTUKPM k=2 floor=1.00 cost=1.01 fees=0.02 net=-3.3pp tickers=KXNEXTUKPM-30-ABUR,KXNEXTUKPM-30-ACAR ; GOVPARTYMO-28 GOVPARTYMO k=2 floor=1.00 cost=1.01 fees=0.02 net=-3.4pp tickers=GOVPARTYMO-28-R,GOVPARTYMO-28-D ; KXNEXTUKPM-30 KXNEXTUKPM k=3 floor=2.00 cost=2.01 fees=0.03 net=-4.1pp tickers=KXNEXTUKPM-30-ABUR,KXNEXTUKPM-30-ACAR,KXNEXTUKPM-30-SMAH ; KXG7LEADEROUT-45JAN01 KXG7LEADEROUT k=2 floor=1.00 cost=1.02 fees=0.02 net=-4.2pp tickers=KXG7LEADEROUT-45JAN01-KSTA,KXG7LEADEROUT-45JAN01-EMAC ; KXG7LEADEROUT-45JAN01 KXG7LEADEROUT k=3 floor=2.00 cost=2.02 fees=0.03 net=-4.8pp tickers=KXG7LEADEROUT-45JAN01-KSTA,KXG7LEADEROUT-45JAN01-EMAC,KXG7LEADEROUT-45JAN01-FMER
- unsafe_all_yes_positive_requires_exhaustive_validation: count=4 best_net=+72.8pp

## Kalshi Exhaustive YES Basket Audit
- command: `PYTHONPATH=scripts python3 scripts/kalshi_event_exhaustive_yes_audit.py --event-limit 300 --max-event-pages 6 --pause-seconds 0.08 --detail-pause-seconds 0.08 --min-net-edge 0.005 --print-limit 20 --record`
- latest_run: id=17 captured_at=2026-07-03T21:19:14+00:00 | version=event_exhaustive_yes_v2_esports events_seen=206 event_details=206 baskets_checked=150 actionable_qty1=0 min_net_edge=0.000 | series=14 page_limits=[200] | counts=KXATPCHALLENGERMATCH=3, KXITFMATCH=18, KXITFWMATCH=20, KXLOLGAME=12, KXLOLMAP=24, KXMLBGAME=44, KXNBAGAME=0, KXNHLGAME=0 | reasons=exhaustive_basket_checked=150, two_way_sports_shape_mismatch=52, event_not_mutually_exclusive=2, not_all_active_yes_tradable=1, two_way_no_tie_match_shape_mismatch=1
- nearest_baskets: KXLOLGAME-26JUL031900DOHGL two_way_no_tie_sports_match contracts=2 sum_asks=0.990 fees=0.040 net=-0.030 depth=5 actionable=0 ; KXVALORANTGAME-26JUL040700RRQEDG two_way_no_tie_sports_match contracts=2 sum_asks=0.990 fees=0.040 net=-0.030 depth=100 actionable=0 ; KXITFWMATCH-26JUL03AROEWI two_way_no_tie_sports_match contracts=2 sum_asks=1.010 fees=0.020 net=-0.030 depth=5589 actionable=0 ; KXITFWMATCH-26JUL03PODJOR two_way_no_tie_sports_match contracts=2 sum_asks=1.000 fees=0.040 net=-0.040 depth=50 actionable=0 ; KXWTAMATCH-26JUL05MUCKRE two_way_no_tie_sports_match contracts=2 sum_asks=1.000 fees=0.040 net=-0.040 depth=1498 actionable=0

## Kalshi Crypto NO <10c Gate Check
- command: `python3 scripts/kalshi_crypto_no_lt10c_gate_check.py --json`
- status: NOT_READY | ready=false
- broad_pilot_note: old_strategy=kalshi_crypto_no_lt10c_first_eligible_pilot kill=present | active_live_path=kalshi_crypto_no_lt10c_non04z_first_eligible_forward_pilot kill=present
- reasons: resolved 6/50; wilson 30.0% < 90.0%; open_filled_trades=5; source reconciliation checked 189/6; source reconciliation mismatches 40; native taker NO ask <10c evidence absent
- resolved: 6/50 | 4W-2L | pnl=+3.72 | wilson=30.0%
- pending: 0 markets | max_if_pending=6/50 | need_new_after_pending=44
- risk: open_filled=5 | sports_open=0 | live_maker_open_like=0
- source_reconciliation: checked=189/189 | mismatches=40 | native_taker_ask_lt10c=0/184
- candidate_preview: available=false | pending_first_eligible=0 | shadow_live_actionable=0 | native_taker_actionable=0 | native_taker_blocked=0 | settlement_pending_or_ineligible=0 | expired_unresolved=0 | reason=no unresolved first-eligible <10c candidate remains before settlement
- fresh_non04z_review: status=NOT_READY | ready=false | reason=fresh gate status ACCUMULATING; resolved 6/50; wilson 30.0% < 90.0%; open_filled_trades=5; source reconciliation checked 177/6; source reconciliation mismatches 40; native taker NO ask <10c evidence absent | resolved=6/50 | 4W-2L | pnl=+3.72 | wilson=30.0% | pending=0 | shadow_live_actionable=0 | native_taker_actionable=0 | native_taker_blocked=0 | expired_unresolved=0 | next_backfill_after=unknown | source_reconciliation=177/177 mismatches=40 | native_taker_ask_lt10c=0/172
- pilot_launcher: script=scripts/kalshi_crypto_no_lt10c_pilot.py | strategy=kalshi_crypto_no_lt10c_first_eligible_pilot | tracking_rows=0 | live_placed_rows=0 | pilot_kill=present | first_live_review_ack=absent | execute_blocked_rows=0 | dry_run_ready_rows=0 | latest=none
- first_live_verifier: status=WAITING_FOR_FIRST_LIVE_ROW | ok=true | placed_tracking_rows=0 | errors=none
- non04z_pilot_launcher: script=scripts/kalshi_crypto_no_lt10c_non04z_pilot.py | strategy=kalshi_crypto_no_lt10c_non04z_first_eligible_forward_pilot | tracking_rows=1 | live_placed_rows=0 | pilot_kill=present | first_live_review_ack=absent | execute_blocked_rows=1 | dry_run_ready_rows=0 | latest=2026-06-25 17:34:38 KXBTCD-26JUN2514-T60199.99 dry_run=0 status=BLOCKED
- non04z_first_live_verifier: status=WAITING_FOR_FIRST_LIVE_ROW | ok=true | placed_tracking_rows=0 | errors=none

## Kalshi Native Forward Gate Leaderboard
- command: `python3 scripts/kalshi_native_forward_leaderboard.py --json`
- status: NO_LIVE_READY | ready=false | cells=9 | ready_cells=0 | min_resolved=30 | edge_buffer=+2.0pp | pending=22 active=22 stale=0 unknown=0 | next_pending=weather_no_candidate:no_95_98_zero_loss_cities_v1:KXHIGHMIA-26JUL03-B88.5 status=active due=2026-07-04T14:00:00+00:00
- best: crypto_last_hour_longshot_no | gate=NATIVE_FORWARD_ACCUMULATING | native_events=332 resolved=332 pending=0 active=0 stale=0 unknown=0 | 298W-34L | pnl=-3.44 | Wilson 86.0% vs BE 90.8% | gap=-4.8pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=320
- rank 1: crypto_last_hour_longshot_no | gate=NATIVE_FORWARD_ACCUMULATING | native_events=332 resolved=332 pending=0 active=0 stale=0 unknown=0 | 298W-34L | pnl=-3.44 | Wilson 86.0% vs BE 90.8% | gap=-4.8pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=320
- rank 2: weather_no_candidate:no_95_98_zero_loss_cities_v1 | gate=NATIVE_FORWARD_ACCUMULATING | native_events=71 resolved=58 pending=13 active=13 stale=0 unknown=0 | 56W-2L | pnl=-0.56 | Wilson 88.3% vs BE 97.5% | gap=-9.3pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=1557 | next_pending=KXHIGHMIA-26JUL03-B88.5 status=active due=2026-07-04T14:00:00+00:00 ask=0.96
- rank 3: crypto_favorite_taker:crypto_near_certain_95_99_12_24h | gate=NATIVE_FORWARD_ACCUMULATING | native_events=40 resolved=39 pending=1 active=1 stale=0 unknown=0 | 38W-1L | pnl=-0.08 | Wilson 86.8% vs BE 97.7% | gap=-10.8pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=1576 | next_pending=KXBTCD-26JUL0417-T64499.99 status=active due=2026-07-04T20:59:59.946773+00:00 ask=0.97
- rank 4: weather_high_ask_no | gate=NATIVE_FORWARD_ACCUMULATING | native_events=48 resolved=45 pending=3 active=3 stale=0 unknown=0 | 43W-2L | pnl=-1.55 | Wilson 85.2% vs BE 99.0% | gap=-13.8pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=>5000_or_target_impossible | next_pending=KXLOWTNYC-26JUL03-T77 status=active due=2026-07-04T19:00:00+00:00 ask=0.98
- rank 5: weather_yes_90_93:yes_90_93_above_live_threshold_v1 | gate=NATIVE_FORWARD_ACCUMULATING | native_events=22 resolved=19 pending=3 active=3 stale=0 unknown=0 | 18W-1L | pnl=+0.42 | Wilson 75.4% vs BE 92.6% | gap=-17.2pp | blockers=resolved<30; wilson<BE+2pp | perfect_wins_needed=82 | next_pending=KXHIGHPHIL-26JUL03-B101.5 status=active due=2026-07-04T14:00:00+00:00 ask=0.92
- rank 6: other_longshot_no_80_90:other_weak_no_80_90_4_24h_v1 | gate=NATIVE_FORWARD_ACCUMULATING | native_events=6 resolved=6 pending=0 active=0 stale=0 unknown=0 | 6W-0L | pnl=+0.77 | Wilson 61.0% vs BE 87.2% | gap=-26.2pp | blockers=resolved<30; wilson<BE+2pp | perfect_wins_needed=26

## Kalshi Native Preflight Cut Miner
- command: `python3 scripts/kalshi_native_preflight_cut_miner.py --limit 8`
- status: NATIVE_CUT_FORWARD_REQUIRED | ready=false | observations=14994 | cuts=2296 | display_cuts=506 | candidate_cuts=1 | ready_cuts=0 | min_resolved=30 | min_display_resolved=10 | edge_buffer=+2.0pp | scope=posthoc_native_executable_cut_discovery_requires_predeclared_forward_gate
- best: crypto_last_hour_longshot_no|minutes_to_expiry_band=20-40m|native_ask_band=80-85 | gate=NATIVE_CUT_FORWARD_REQUIRED | type=pair | observations=59 resolved=59 pending=0 active=0 stale=0 unknown=0 | 56W-3L | pnl=+$6.53 | Wilson 86.1% vs target 85.8% (BE 83.8%) | gap=+0.2pp | blockers=none | promotion_blockers=posthoc_cut_requires_predeclared_forward_gate
- rank 1: crypto_last_hour_longshot_no|minutes_to_expiry_band=20-40m|native_ask_band=80-85 | gate=NATIVE_CUT_FORWARD_REQUIRED | type=pair | observations=59 resolved=59 pending=0 active=0 stale=0 unknown=0 | 56W-3L | pnl=+$6.53 | Wilson 86.1% vs target 85.8% (BE 83.8%) | gap=+0.2pp | blockers=none | promotion_blockers=posthoc_cut_requires_predeclared_forward_gate
- rank 2: crypto_last_hour_longshot_no|captured_weekday=Tue | gate=NATIVE_CUT_ACCUMULATING | type=single | observations=52 resolved=52 pending=0 active=0 stale=0 unknown=0 | 52W-0L | pnl=+$4.54 | Wilson 93.1% vs target 93.3% (BE 91.3%) | gap=-0.1pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=2
- rank 3: crypto_last_hour_longshot_no|signal_tier=moderate|native_ask_band=90-95 | gate=NATIVE_CUT_ACCUMULATING | type=pair | observations=76 resolved=76 pending=0 active=0 stale=0 unknown=0 | 75W-1L | pnl=+$4.46 | Wilson 92.9% vs target 94.8% (BE 92.8%) | gap=-1.9pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=30
- rank 4: crypto_last_hour_longshot_no|shadow_entry_band=80-85 | gate=NATIVE_CUT_ACCUMULATING | type=single | observations=47 resolved=47 pending=0 active=0 stale=0 unknown=0 | 45W-2L | pnl=+$4.34 | Wilson 85.8% vs target 88.5% (BE 86.5%) | gap=-2.8pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=13
- rank 5: crypto_last_hour_longshot_no|native_ask_band=85-90 | gate=NATIVE_CUT_ACCUMULATING | type=single | observations=187 resolved=187 pending=0 active=0 stale=0 unknown=0 | 169W-18L | pnl=+$3.85 | Wilson 85.3% vs target 90.3% (BE 88.3%) | gap=-5.0pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=101
- rank 6: crypto_last_hour_longshot_no|shadow_spread_band=<=1c | gate=NATIVE_CUT_ACCUMULATING | type=single | observations=233 resolved=233 pending=0 active=0 stale=0 unknown=0 | 215W-18L | pnl=+$1.96 | Wilson 88.1% vs target 93.4% (BE 91.4%) | gap=-5.3pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=194
- rank 7: crypto_last_hour_longshot_no|asset=BTC|native_ask_band=90-95 | gate=NATIVE_CUT_ACCUMULATING | type=pair | observations=134 resolved=134 pending=0 active=0 stale=0 unknown=0 | 127W-7L | pnl=+$2.23 | Wilson 89.6% vs target 95.1% (BE 93.1%) | gap=-5.5pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=157
- rank 8: crypto_last_hour_longshot_no|native_spread_band=<=1c | gate=NATIVE_CUT_ACCUMULATING | type=single | observations=288 resolved=288 pending=0 active=0 stale=0 unknown=0 | 263W-25L | pnl=+$0.51 | Wilson 87.5% vs target 93.1% (BE 91.1%) | gap=-5.6pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=244

## Kalshi Native Forward Watchlist
- command: `python3 scripts/kalshi_native_forward_watchlist.py --limit 8`
- status: NO_FORWARD_WATCH_READY | ready=false | watches=8 | ready_watches=0 | min_resolved=30 | edge_buffer=+2.0pp | scope=predeclared_forward_only_after_posthoc_cut_discovery
- best: native_watch|crypto_spread_le1_depth_100_999 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-07-01T11:00:00+00:00 | observations=65 resolved=65 pending=0 active=0 stale=0 unknown=0 | 55W-10L | pnl=$-4.18 | Wilson 73.9% vs target 93.0% (BE 91.0%) | gap=-19.1pp | blockers=pnl<=0;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=195 | excluded_post_start_actionables=298 (native_spread_band=<=5c=99, native_spread_band=<=2c=78, native_depth_band=1000+=69, native_depth_band=10-99=38) | excluded_sample=KXBTCD-26JUL0108-T58799.99 native_depth_band=10-99 ask=0.85 | target_window_misses=147 (not_actionable=147) | target_window_sample=KXBTCD-26JUL0108-T58799.99 not_actionable ask=0.99
- rank 1: native_watch|crypto_spread_le1_depth_100_999 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-07-01T11:00:00+00:00 | observations=65 resolved=65 pending=0 active=0 stale=0 unknown=0 | 55W-10L | pnl=$-4.18 | Wilson 73.9% vs target 93.0% (BE 91.0%) | gap=-19.1pp | blockers=pnl<=0;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=195 | excluded_post_start_actionables=298 (native_spread_band=<=5c=99, native_spread_band=<=2c=78, native_depth_band=1000+=69, native_depth_band=10-99=38) | excluded_sample=KXBTCD-26JUL0108-T58799.99 native_depth_band=10-99 ask=0.85 | target_window_misses=147 (not_actionable=147) | target_window_sample=KXBTCD-26JUL0108-T58799.99 not_actionable ask=0.99
- rank 2: native_watch|crypto_strong_no_90_95 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-07-01T11:00:00+00:00 | observations=45 resolved=45 pending=0 active=0 stale=0 unknown=0 | 37W-8L | pnl=$-5.00 | Wilson 68.7% vs target 95.3% (BE 93.3%) | gap=-26.7pp | blockers=pnl<=0;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=289 | excluded_post_start_actionables=332 (signal_tier=weak=156, signal_tier=moderate=87, native_ask_band=85-90=44, native_ask_band=95-98=29) | excluded_sample=KXBTCD-26JUL0108-T58799.99 native_ask_band=85-90 ask=0.89 | target_window_misses=612 (not_actionable_native_ask_band=missing=170, not_actionable_native_ask_band=<80=102, not_actionable_native_ask_band=95-98=93, not_actionable_native_ask_band=98-99=80) | target_window_sample=KXBTCD-26JUL0108-T58799.99 native_ask_band=85-90 ask=0.89
- rank 3: native_watch|crypto_20_40m_no_80_85 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-06-29T11:05:00+00:00 | observations=29 resolved=29 pending=0 active=0 stale=0 unknown=0 | 27W-2L | pnl=$+2.65 | Wilson 78.0% vs target 86.0% (BE 84.0%) | gap=-7.9pp | blockers=resolved<30;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=19 | excluded_post_start_actionables=866 (minutes_band=40-60m=483, native_ask_band=90-95=144, native_ask_band=85-90=89, minutes_band=10-20m=77) | excluded_sample=KXBTCD-26JUN2908-T60299.99 minutes_band=40-60m ask=0.95 | target_window_misses=1162 (not_actionable_native_ask_band=98-99=209, not_actionable_native_ask_band=missing=201, not_actionable_native_ask_band=99+=176, not_actionable_native_ask_band=95-98=159) | target_window_sample=KXBTCD-26JUN2908-T60299.99 not_actionable_native_ask_band=98-99 ask=0.98
- rank 4: native_watch|crypto_btc_no_85_90 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-06-30T07:13:19+00:00 | observations=29 resolved=29 pending=0 active=0 stale=0 unknown=0 | 22W-7L | pnl=$-3.64 | Wilson 57.9% vs target 90.4% (BE 88.4%) | gap=-32.5pp | blockers=resolved<30;pnl<=0;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=117 | excluded_post_start_actionables=640 (asset=SOL=235, asset=ETH=190, native_ask_band=90-95=145, native_ask_band=95-98=47) | excluded_sample=KXBTCD-26JUN3005-T59699.99 native_ask_band=90-95 ask=0.94 | target_window_misses=1030 (not_actionable_native_ask_band=missing=385, native_ask_band=90-95=145, not_actionable_native_ask_band=98-99=130, not_actionable_native_ask_band=95-98=111) | target_window_sample=KXBTCD-26JUN3004-T59799.99 not_actionable_native_ask_band=98-99 ask=0.98
- rank 5: native_watch|crypto_spread_le1_depth_10_99 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-07-01T07:10:00+00:00 | observations=28 resolved=28 pending=0 active=0 stale=0 unknown=0 | 23W-5L | pnl=$-2.33 | Wilson 64.4% vs target 92.5% (BE 90.5%) | gap=-28.1pp | blockers=resolved<30;pnl<=0;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=123 | excluded_post_start_actionables=436 (native_depth_band=100-999=171, native_spread_band=<=5c=101, native_spread_band=<=2c=80, native_depth_band=1000+=70) | excluded_sample=KXBTCD-26JUL0104-T58899.99 native_depth_band=100-999 ask=0.93 | target_window_misses=44 (not_actionable=44) | target_window_sample=KXSOLD-26JUL0107-T75.9999 not_actionable ask=0.99
- rank 6: native_watch|crypto_sol_no_85_90 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-07-01T13:00:00+00:00 | observations=19 resolved=19 pending=0 active=0 stale=0 unknown=0 | 17W-2L | pnl=$+0.19 | Wilson 68.6% vs target 90.5% (BE 88.5%) | gap=-21.9pp | blockers=resolved<30;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=54 | excluded_post_start_actionables=381 (asset=BTC=184, asset=ETH=103, native_ask_band=90-95=62, native_ask_band=80-85=21) | excluded_sample=KXBTCD-26JUL0110-T59199.99 asset=BTC ask=0.93 | target_window_misses=338 (not_actionable_native_ask_band=missing=72, native_ask_band=90-95=62, not_actionable_native_ask_band=99+=53, not_actionable_native_ask_band=<80=48) | target_window_sample=KXSOLD-26JUL0111-T79.9999 not_actionable_native_ask_band=missing
- rank 7: native_watch|crypto_btc_strong_no_90_95_spread_le1_depth_100_999 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-07-01T14:00:00+00:00 | observations=14 resolved=14 pending=0 active=0 stale=0 unknown=0 | 13W-1L | pnl=$-0.12 | Wilson 68.5% vs target 95.7% (BE 93.7%) | gap=-27.2pp | blockers=resolved<30;pnl<=0;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=115 | excluded_post_start_actionables=385 (asset=SOL=142, asset=ETH=103, native_depth_band=1000+=46, signal_tier=weak=30) | excluded_sample=KXETHD-26JUL0111-T1609.99 asset=ETH ask=0.90 | target_window_misses=81 (not_actionable_native_ask_band=95-98=23, not_actionable_native_ask_band=99+=16, native_ask_band=85-90=12, not_actionable_native_ask_band=<80=10) | target_window_sample=KXBTCD-26JUL0112-T60099.99 native_ask_band=85-90 ask=0.89
- rank 8: native_watch|crypto_tue_no_any_ask | gate=FORWARD_WATCH_WAITING | start=2026-07-01T07:10:00+00:00 | observations=0 resolved=0 pending=0 active=0 stale=0 unknown=0 | 0W-0L | pnl=$+0.00 | Wilson 0.0% vs target 2.0% (BE 0.0%) | gap=-2.0pp | blockers=no_forward_observations;resolved<30;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=>5000_or_target_impossible | excluded_post_start_actionables=475 (captured_weekday=Fri=177, captured_weekday=Thu=165, captured_weekday=Wed=133) | excluded_sample=KXBTCD-26JUL0104-T58899.99 captured_weekday=Wed ask=0.93

## Kalshi Native Preflight Walk-Forward Validation
- command: `python3 scripts/kalshi_native_preflight_walkforward.py --limit 8`
- status: NO_WALKFORWARD_NATIVE_CUT | ready=false | observations=14994 | cuts=2296 | display_cuts=225 | validated_cuts=0 | ready_cuts=0 | split_cutoff=2026-06-29T23:56:08+00:00 | min_train=30 | min_validation=15 | edge_buffer=+2.0pp | scope=posthoc_walkforward_native_cut_validation_requires_predeclared_forward_gate
- best: crypto_last_hour_longshot_no|captured_weekday=Tue | gate=WALKFORWARD_REJECT | type=single | train=0 resolved 0W-0L +$0.00 Wilson 0.0% vs target 2.0% gap=-2.0pp | validation=52 resolved 52W-0L +$4.54 Wilson 93.1% vs target 93.3% gap=-0.1pp | blockers=train_resolved<30;train_pnl<=0;train_wilson<BE+buffer;validation_wilson<BE+buffer | promotion_blockers=none
- rank 1: crypto_last_hour_longshot_no|captured_weekday=Tue | gate=WALKFORWARD_REJECT | type=single | train=0 resolved 0W-0L +$0.00 Wilson 0.0% vs target 2.0% gap=-2.0pp | validation=52 resolved 52W-0L +$4.54 Wilson 93.1% vs target 93.3% gap=-0.1pp | blockers=train_resolved<30;train_pnl<=0;train_wilson<BE+buffer;validation_wilson<BE+buffer | promotion_blockers=none
- rank 2: crypto_last_hour_longshot_no|shadow_entry_band=80-85 | gate=WALKFORWARD_REJECT | type=single | train=21 resolved 19W-2L +$0.73 Wilson 71.1% vs target 89.0% gap=-17.9pp | validation=26 resolved 26W-0L +$3.61 Wilson 87.1% vs target 88.1% gap=-1.0pp | blockers=train_resolved<30;train_wilson<BE+buffer;validation_wilson<BE+buffer | promotion_blockers=none
- rank 3: crypto_last_hour_longshot_no|captured_weekday=Sun | gate=WALKFORWARD_REJECT | type=single | train=37 resolved 35W-2L +$2.09 Wilson 82.3% vs target 90.9% gap=-8.7pp | validation=0 resolved 0W-0L +$0.00 Wilson 0.0% vs target 2.0% gap=-2.0pp | blockers=train_wilson<BE+buffer;validation_resolved<15;validation_pnl<=0;validation_wilson<BE+buffer | promotion_blockers=none
- rank 4: crypto_last_hour_longshot_no|captured_weekday=Mon | gate=WALKFORWARD_REJECT | type=single | train=52 resolved 48W-4L +$0.54 Wilson 81.8% vs target 93.3% gap=-11.4pp | validation=0 resolved 0W-0L +$0.00 Wilson 0.0% vs target 2.0% gap=-2.0pp | blockers=train_wilson<BE+buffer;validation_resolved<15;validation_pnl<=0;validation_wilson<BE+buffer | promotion_blockers=none
- rank 5: crypto_last_hour_longshot_no|captured_weekday=Sat | gate=WALKFORWARD_REJECT | type=single | train=27 resolved 24W-3L -$0.68 Wilson 71.9% vs target 93.4% gap=-21.5pp | validation=0 resolved 0W-0L +$0.00 Wilson 0.0% vs target 2.0% gap=-2.0pp | blockers=train_resolved<30;train_pnl<=0;train_wilson<BE+buffer;validation_resolved<15;validation_pnl<=0;validation_wilson<BE+buffer | promotion_blockers=none
- rank 6: weather_no_candidate:no_95_98_zero_loss_cities_v1|captured_weekday=Mon | gate=WALKFORWARD_REJECT | type=single | train=15 resolved 14W-1L -$0.66 Wilson 70.2% vs target 99.7% gap=-29.6pp | validation=0 resolved 0W-0L +$0.00 Wilson 0.0% vs target 2.0% gap=-2.0pp | blockers=train_resolved<30;train_pnl<=0;train_wilson<BE+buffer;validation_resolved<15;validation_pnl<=0;validation_wilson<BE+buffer | promotion_blockers=none
- rank 7: crypto_last_hour_longshot_no|signal_tier=moderate|native_ask_band=90-95 | gate=WALKFORWARD_REJECT | type=pair | train=41 resolved 40W-1L +$1.91 Wilson 87.4% vs target 94.9% gap=-7.5pp | validation=35 resolved 35W-0L +$2.55 Wilson 90.1% vs target 94.7% gap=-4.6pp | blockers=train_wilson<BE+buffer;validation_wilson<BE+buffer | promotion_blockers=none
- rank 8: crypto_last_hour_longshot_no|signal_tier=moderate | gate=WALKFORWARD_REJECT | type=single | train=51 resolved 46W-5L +$0.40 Wilson 79.0% vs target 91.4% gap=-12.4pp | validation=42 resolved 40W-2L +$2.29 Wilson 84.2% vs target 91.8% gap=-7.6pp | blockers=train_wilson<BE+buffer;validation_wilson<BE+buffer | promotion_blockers=none

## Kalshi Crypto Last-Hour Native Subcell Audit
- command: `python3 scripts/kalshi_crypto_last_hour_subcell_audit.py --json`
- status: NO_NATIVE_SUBCELL_READY | ready=false | cells=6 | ready_cells=0 | mapped_shadow_candidate_cells=3 | min_resolved=30 | edge_buffer=+2.0pp | scope=first native-actionable event per crypto hour split by shadow tier/entry band
- best: crypto_last_hour_native_subcell:moderate:80-90 | gate=NATIVE_FORWARD_ACCUMULATING | mapped_shadow_candidate=true | native_events=60 resolved=60 pending=0 active=0 stale=0 unknown=0 | 57W-3L | pnl=+3.75 | Wilson 86.3% vs BE 88.8% | gap=-2.5pp | blockers=wilson<BE+2pp | perfect_wins_needed=31
- rank 1: crypto_last_hour_native_subcell:moderate:80-90 | gate=NATIVE_FORWARD_ACCUMULATING | mapped_shadow_candidate=true | native_events=60 resolved=60 pending=0 active=0 stale=0 unknown=0 | 57W-3L | pnl=+3.75 | Wilson 86.3% vs BE 88.8% | gap=-2.5pp | blockers=wilson<BE+2pp | perfect_wins_needed=31
- rank 2: crypto_last_hour_native_subcell:strong:90-95 | gate=NATIVE_FORWARD_ACCUMULATING | mapped_shadow_candidate=true | native_events=160 resolved=160 pending=0 active=0 stale=0 unknown=0 | 145W-15L | pnl=-4.10 | Wilson 85.1% vs BE 93.2% | gap=-8.1pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=349
- rank 3: crypto_last_hour_native_subcell:weak:80-90 | gate=NATIVE_FORWARD_ACCUMULATING | mapped_shadow_candidate=true | native_events=79 resolved=79 pending=0 active=0 stale=0 unknown=0 | 67W-12L | pnl=-2.03 | Wilson 75.3% vs BE 87.4% | gap=-12.1pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=113
- rank 4: crypto_last_hour_native_subcell:native_ask:80-90 | gate=NATIVE_FORWARD_ACCUMULATING | mapped_shadow_candidate=false | native_events=145 resolved=145 pending=0 active=0 stale=0 unknown=0 | 126W-19L | pnl=+0.06 | Wilson 80.4% vs BE 86.9% | gap=-6.4pp | blockers=wilson<BE+2pp | perfect_wins_needed=115
- rank 5: crypto_last_hour_native_subcell:native_ask:90-95 | gate=NATIVE_FORWARD_ACCUMULATING | mapped_shadow_candidate=false | native_events=143 resolved=143 pending=0 active=0 stale=0 unknown=0 | 132W-11L | pnl=-1.26 | Wilson 86.8% vs BE 93.2% | gap=-6.4pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=261
- rank 6: crypto_last_hour_native_subcell:moderate:90-95 | gate=NATIVE_FORWARD_ACCUMULATING | mapped_shadow_candidate=false | native_events=33 resolved=33 pending=0 active=0 stale=0 unknown=0 | 29W-4L | pnl=-1.06 | Wilson 72.7% vs BE 91.1% | gap=-18.4pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=112

## Kalshi Crypto Last-Hour Entry Timing Audit
- command: `python3 scripts/kalshi_crypto_last_hour_entry_timing_audit.py --limit 8`
- status: NO_ENTRY_TIMING_CANDIDATE | ready=false | posthoc_candidates=0 | source_actionable_rows=1544 | selected_observations=834 | cuts=375 | min_resolved=30 | edge_buffer=+2.0pp
- best: crypto_last_hour_entry_timing:latest_actionable|native_ask_band=90-95 | gate=ENTRY_TIMING_ACCUMULATING | observations=175 resolved=175 pending=0 | 168W-7L | pnl=+$4.23 | Wilson 92.0% vs target 95.6% (BE 93.6%) | gap=-3.6pp | blockers=wilson<BE+2pp
- rank 1: crypto_last_hour_entry_timing:latest_actionable|native_ask_band=90-95 | gate=ENTRY_TIMING_ACCUMULATING | observations=175 resolved=175 pending=0 | 168W-7L | pnl=+$4.23 | Wilson 92.0% vs target 95.6% (BE 93.6%) | gap=-3.6pp | blockers=wilson<BE+2pp
- rank 2: crypto_last_hour_entry_timing:first_actionable|native_spread_band=<=1c | gate=ENTRY_TIMING_ACCUMULATING | observations=231 resolved=231 pending=0 | 213W-18L | pnl=+$2.20 | Wilson 88.0% vs target 93.3% (BE 91.3%) | gap=-5.2pp | blockers=wilson<BE+2pp
- rank 3: crypto_last_hour_entry_timing:latest_actionable|signal_tier=moderate|native_ask_band=90-95 | gate=ENTRY_TIMING_ACCUMULATING | observations=53 resolved=53 pending=0 | 52W-1L | pnl=+$2.52 | Wilson 90.1% vs target 95.4% (BE 93.4%) | gap=-5.3pp | blockers=wilson<BE+2pp
- rank 4: crypto_last_hour_entry_timing:first_actionable|native_depth_band=1000+ | gate=ENTRY_TIMING_ACCUMULATING | observations=84 resolved=84 pending=0 | 80W-4L | pnl=+$2.78 | Wilson 88.4% vs target 93.9% (BE 91.9%) | gap=-5.5pp | blockers=wilson<BE+2pp
- rank 5: crypto_last_hour_entry_timing:latest_actionable|asset=BTC|native_ask_band=95-98 | gate=ENTRY_TIMING_ACCUMULATING | observations=46 resolved=46 pending=0 | 46W-0L | pnl=+$1.84 | Wilson 92.3% vs target 98.0% (BE 96.0%) | gap=-5.7pp | blockers=wilson<BE+2pp
- rank 6: crypto_last_hour_entry_timing:latest_actionable|asset=BTC|native_ask_band=90-95 | gate=ENTRY_TIMING_ACCUMULATING | observations=79 resolved=79 pending=0 | 76W-3L | pnl=+$1.98 | Wilson 89.4% vs target 95.7% (BE 93.7%) | gap=-6.3pp | blockers=wilson<BE+2pp
- rank 7: crypto_last_hour_entry_timing:first_actionable|signal_tier=moderate | gate=ENTRY_TIMING_ACCUMULATING | observations=93 resolved=93 pending=0 | 86W-7L | pnl=+$2.69 | Wilson 85.3% vs target 91.6% (BE 89.6%) | gap=-6.3pp | blockers=wilson<BE+2pp
- rank 8: crypto_last_hour_entry_timing:first_actionable|signal_tier=weak|native_ask_band=85-90 | gate=ENTRY_TIMING_ACCUMULATING | observations=39 resolved=39 pending=0 | 37W-2L | pnl=+$2.78 | Wilson 83.1% vs target 89.7% (BE 87.7%) | gap=-6.6pp | blockers=wilson<BE+2pp

## Kalshi Crypto Ladder Dislocation Preflight
- command: `python3 scripts/kalshi_crypto_ladder_dislocation_preflight.py --json`
- latest_run: captured_at=2026-07-03T23:04:53+00:00 | lookahead=75m | events=5 rows_per_event=40 | candidates=99 checked=99 dislocation_qty1=0 | min_source_edge=0.03 max_source_age=300s | top_reasons=missing_native_no_ask=98, nonpositive_qty1_win:0.0000=1
- latest_rows: KXSOLD-26JUL0320-T82.9999 SOL/extreme source_no=0.97 native_no_ask=0.99 edge=-0.02 age=44s spread=0.02 depth=4462 win=0.00 due=2026-07-04T00:00:00.000997+00:00 reason=nonpositive_qty1_win:0.0000 ; KXETHD-26JUL0320-T1779.99 ETH/extreme source_no=0.99 native_no_ask=missing edge=missing age=45s spread=missing depth=0 win=missing due=2026-07-03T23:59:59.471392+00:00 reason=missing_native_no_ask ; KXETHD-26JUL0320-T1799.99 ETH/extreme source_no=0.99 native_no_ask=missing edge=missing age=45s spread=missing depth=0 win=missing due=2026-07-03T23:59:59.476140+00:00 reason=missing_native_no_ask ; KXETHD-26JUL0320-T1819.99 ETH/extreme source_no=0.99 native_no_ask=missing edge=missing age=45s spread=missing depth=0 win=missing due=2026-07-03T23:59:59.481151+00:00 reason=missing_native_no_ask ; KXETHD-26JUL0320-T1839.99 ETH/extreme source_no=0.99 native_no_ask=missing edge=missing age=45s spread=missing depth=0 win=missing due=2026-07-03T23:59:59.486831+00:00 reason=missing_native_no_ask ; KXETHD-26JUL0320-T1859.99 ETH/extreme source_no=0.99 native_no_ask=missing edge=missing age=45s spread=missing depth=0 win=missing due=2026-07-03T23:59:59.491651+00:00 reason=missing_native_no_ask

## Kalshi Crypto Ladder Dislocation Forward Audit
- command: `python3 scripts/kalshi_crypto_ladder_dislocation_audit.py --limit 8`
- status: NO_LIVE_READY | ready=false | cells=6 | ready_cells=0 | observations=96 | min_resolved=30 | edge_buffer=+2.0pp | scope=source-vs-native ladder gaps only; not riskless structural arbitrage
- best: event_first | gate=LADDER_DISLOCATION_ACCUMULATING | observations=61 resolved=61 pending=0 active=0 stale=0 | 42W-19L pnl_qty1=-$7.90 | Wilson 56.4% vs target 83.8% gap=-27.4pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=116
- rank 1: event_first | gate=LADDER_DISLOCATION_ACCUMULATING | observations=61 resolved=61 pending=0 active=0 stale=0 | 42W-19L pnl_qty1=-$7.90 | Wilson 56.4% vs target 83.8% gap=-27.4pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=116
- rank 2: ticker_first | gate=LADDER_DISLOCATION_ACCUMULATING | observations=64 resolved=64 pending=0 active=0 stale=0 | 44W-20L pnl_qty1=-$8.73 | Wilson 56.6% vs target 84.4% gap=-27.8pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=128
- rank 3: all_rows | gate=LADDER_DISLOCATION_ACCUMULATING | observations=96 resolved=96 pending=0 active=0 stale=0 | 62W-34L pnl_qty1=-$13.99 | Wilson 54.6% vs target 81.2% gap=-26.5pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=148
- rank 4: asset_btc | gate=LADDER_DISLOCATION_ACCUMULATING | observations=7 resolved=7 pending=0 active=0 stale=0 | 4W-3L pnl_qty1=-$2.32 | Wilson 25.0% vs target 92.3% gap=-67.2pp | blockers=resolved<30; pnl<=0; wilson<BE+2pp | perfect_wins_needed=103
- rank 5: asset_eth | gate=LADDER_DISLOCATION_ACCUMULATING | observations=42 resolved=42 pending=0 active=0 stale=0 | 26W-16L pnl_qty1=-$7.07 | Wilson 46.8% vs target 80.7% gap=-33.9pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=87
- rank 6: asset_sol | gate=LADDER_DISLOCATION_ACCUMULATING | observations=47 resolved=47 pending=0 active=0 stale=0 | 32W-15L pnl_qty1=-$4.60 | Wilson 53.8% vs target 79.9% gap=-26.0pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=70

## Kalshi Hourly Temperature State Audit
- command: `python3 scripts/kalshi_hourly_temp_state_audit.py --max-pages-per-series 2 --limit 1000 --max-dates 4 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T22:19:48+00:00 | markets_checked=24 parsed=24 source_observations=67 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXTEMPNYCH dates=2026-07-03 | state_keys=19 observations_raw=67 source=weathercom_kalshi_metar_primary source_errors=0 | counts=KXTEMPNYCH=24 | reasons=hourly_temp_observation_missing_or_future=24

## Kalshi Direct MLB Player Prop State Audit
- command: `python3 scripts/kalshi_mlb_player_prop_state_audit.py --max-pages-per-series 6 --limit 1000 --max-dates 6 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T22:19:48+00:00 | markets_checked=2656 parsed=2656 espn_games=13 locked_rows=65 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXMLBKS,KXMLBOUTS,KXMLBHIT,KXMLBHRR,KXMLBHR,KXMLBTB,KXMLBRBI,KXMLBSB dates=2026-07-03 | state_games=13 | reasons=mlb_boxscore_not_current=2394, player_stat_waiting_for_threshold_or_final=126, player_stat_missing_after_final=69, mlb_player_stat_already_reached=65, player_stat_missing_before_final=2
- locked_rows: KXMLBHIT-26JUL031605STLCHC-CHCABREGMAN3-1 YES ask=1.00 depth=0 bid=0.99 win=0.00 stat=hits:1/1 game=STL@CHC 16-0 STATUS_IN_PROGRESS reason=mlb_player_stat_already_reached actionable=0 ; KXMLBHIT-26JUL031605STLCHC-CHCCKELLY15-1 YES ask=1.00 depth=0 bid=0.99 win=0.00 stat=hits:1/1 game=STL@CHC 16-0 STATUS_IN_PROGRESS reason=mlb_player_stat_already_reached actionable=0 ; KXMLBHIT-26JUL031605STLCHC-CHCMBUSCH29-1 YES ask=1.00 depth=0 bid=0.99 win=0.00 stat=hits:1/1 game=STL@CHC 16-0 STATUS_IN_PROGRESS reason=mlb_player_stat_already_reached actionable=0 ; KXMLBHIT-26JUL031605STLCHC-CHCPCROWARMSTRONG4-1 YES ask=1.00 depth=0 bid=0.99 win=0.00 stat=hits:1/1 game=STL@CHC 16-0 STATUS_IN_PROGRESS reason=mlb_player_stat_already_reached actionable=0 ; KXMLBHIT-26JUL031605STLCHC-STLABURLESON41-1 YES ask=1.00 depth=0 bid=0.99 win=0.00 stat=hits:2/1 game=STL@CHC 16-0 STATUS_IN_PROGRESS reason=mlb_player_stat_already_reached actionable=0 ; KXMLBHIT-26JUL031605STLCHC-STLABURLESON41-2 YES ask=1.00 depth=0 bid=0.99 win=0.00 stat=hits:2/2 game=STL@CHC 16-0 STATUS_IN_PROGRESS reason=mlb_player_stat_already_reached actionable=0 ; KXMLBHIT-26JUL031605STLCHC-STLBJORDAN33-1 YES ask=1.00 depth=0 bid=0.99 win=0.00 stat=hits:3/1 game=STL@CHC 16-0 STATUS_IN_PROGRESS reason=mlb_player_stat_already_reached actionable=0 ; KXMLBHIT-26JUL031605STLCHC-STLBJORDAN33-2 YES ask=1.00 depth=0 bid=0.99 win=0.00 stat=hits:3/2 game=STL@CHC 16-0 STATUS_IN_PROGRESS reason=mlb_player_stat_already_reached actionable=0

## Kalshi MVE Component Result Audit
- command: `python3 scripts/kalshi_mve_component_result_audit.py --series KXMVESPORTSMULTIGAMEEXTENDED,KXMVECROSSCATEGORY --limit 1000 --max-pages 20 --max-component-events 250 --pause-seconds 0.3 --max-target-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T05:27:07+00:00 | markets_checked=32000 with_legs=32000 component_events=340/340 fetched=340 component_markets=2993 resolved=85 locked_rows=242 actionable_qty1=0 | max_target_ask=0.30 min_depth=1 | series=KXMVESPORTSMULTIGAMEEXTENDED,KXMVECROSSCATEGORY counts=KXMVECROSSCATEGORY=20000, KXMVESPORTSMULTIGAMEEXTENDED=12000 | page_cap=KXMVECROSSCATEGORY rate_limited=KXMVESPORTSMULTIGAMEEXTENDED component_cap=false component_rate_limited=false | reasons=not_locked_by_component_results=31758, component_false_locks_mve_no=224, component_market_resolved=85, all_components_true_locks_mve_yes=18
- latest_rows: KXMVECROSSCATEGORY-S2026021E78221C6-3DDD6D8C44F YES ask=0.00 depth=0 bid=0.00 win=1.00 series=KXMVECROSSCATEGORY legs=3/3 decisive=KXXRP15M-26JUL030100-00:NO->NO reason=all_components_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S20260F0CFD4310F-58841A07B67 YES ask=0.00 depth=0 bid=0.00 win=1.00 series=KXMVECROSSCATEGORY legs=3/3 decisive=KXSOL15M-26JUL030115-15:YES->YES reason=all_components_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S20264AD77054F0F-399B463A30A YES ask=0.00 depth=0 bid=0.00 win=1.00 series=KXMVECROSSCATEGORY legs=2/2 decisive=KXDOGE15M-26JUL030115-15:YES->YES reason=all_components_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S20264EBAC1FAF98-0F53D228989 YES ask=0.00 depth=0 bid=0.00 win=1.00 series=KXMVECROSSCATEGORY legs=3/3 decisive=KXETH15M-26JUL030115-15:YES->YES reason=all_components_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S2026591ECC256AB-A1F0579A698 YES ask=0.00 depth=0 bid=0.00 win=1.00 series=KXMVECROSSCATEGORY legs=4/4 decisive=KXXRP15M-26JUL030115-15:YES->YES reason=all_components_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S20266A995B65A66-681118F31B9 YES ask=0.00 depth=0 bid=0.00 win=1.00 series=KXMVECROSSCATEGORY legs=2/2 decisive=KXXRP15M-26JUL030115-15:YES->YES reason=all_components_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S202676362E3BD21-8AEECC6042F YES ask=0.00 depth=0 bid=0.00 win=1.00 series=KXMVECROSSCATEGORY legs=2/2 decisive=KXXRP15M-26JUL030115-15:YES->YES reason=all_components_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S20267BFC2BFA368-3552E675DD2 YES ask=0.00 depth=0 bid=0.00 win=1.00 series=KXMVECROSSCATEGORY legs=4/4 decisive=KXSOL15M-26JUL030100-00:NO->NO reason=all_components_true_locks_mve_yes actionable=0

## Kalshi MVE Locked Passive Maker Pilot
- strategy: kalshi_live_pilot_mve_locked_passive_maker_v1
- monitor_command: `python3 scripts/kalshi_mve_locked_passive_maker_pilot.py --monitor`
- status: live_rows=1 dry_runs=1 live_today=0 open_orders=0 open_risk=$0.00 rows_with_fills=0 filled_unresolved=0 filled_unresolved_cost=$0.00 realized_pnl=+0.00
- tracking_status_counts: CANCELLED=1
- live_maker_orders: open_like=0 status_counts=CANCELLED=1
- latest_orders: id=2 live=true status=CANCELLED ticker=KXMVECROSSCATEGORY-S20261CA825626CE-B9A808D19A4 side=YES qty=1 limit=0.01 filled=0 fee=$0.00 order=b13030ab source_run=6 legs=3/3 lock=all_components_true_locks_mve_yes decisive=KXWTAMATCH-26JUL02RAKSAK-SAK placed_at=2026-07-02T18:04:56+00:00 expires_at=2026-07-02T18:34:56+00:00 resolution=unresolved realized_pnl=unknown reason=order_accepted ; id=1 live=false status=DRY_RUN_READY ticker=KXMVECROSSCATEGORY-S20261CA825626CE-B9A808D19A4 side=YES qty=1 limit=0.01 filled=0 fee=$0.01 order=none source_run=6 legs=3/3 lock=all_components_true_locks_mve_yes decisive=KXWTAMATCH-26JUL02RAKSAK-SAK placed_at=None expires_at=None resolution=unresolved realized_pnl=unknown reason=dry_run_ready

## Kalshi Crypto Last-Hour NO Pilot
- strategy: kalshi_live_pilot_crypto_last_hour_btc_moderate_80_90_no_v1
- check_command: `python3 scripts/kalshi_crypto_last_hour_longshot_no_pilot.py --record-dry-run`
- status: live_rows=1 dry_runs=4 filled_rows=0 cancelled_rows=0 | strategy_open=0 strategy_open_cost=$0.00 | all_live_pilot_open=5 all_live_pilot_cost=$0.50
- latest_rows: id=5 live=false status=DRY_RUN ticker=KXBTCD-26JUL0302-T61599.99 side=NO qty=1 limit=0.00 bid=unknown ask=unknown depth=unknown spread=unknown trade_id=none order=none fill_confirmed=0 cost=$unknown fee=$unknown spot=61907.04 threshold=61599.99 cushion=$-307.06 subcell=57W-3L wilson=0.86 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=missing_native_no_ask ; id=4 live=true status=RESOLVED_LOSS ticker=KXBTCD-26JUL0302-T61599.99 side=NO qty=1 limit=0.80 bid=0.79 ask=0.80 depth=747 spread=0.01 trade_id=7108 order=12692f14 fill_confirmed=1 cost=$0.80 fee=$0.01 spot=61464.29 threshold=61599.99 cushion=$135.69 subcell=57W-2L wilson=0.88 pred_p=0.97 edge=0.15 resolution=LOSS pnl=-0.81 reason=none ; id=3 live=false status=DRY_RUN ticker=KXBTCD-26JUL0302-T61599.99 side=NO qty=1 limit=0.81 bid=0.80 ask=0.81 depth=698 spread=0.01 trade_id=none order=none fill_confirmed=0 cost=$unknown fee=$unknown spot=61467.47 threshold=61599.99 cushion=$132.51 subcell=57W-2L wilson=0.88 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=dry_run_quote_ok ; id=2 live=false status=DRY_RUN ticker=KXBTCD-26JUL0302-T61599.99 side=NO qty=1 limit=0.83 bid=0.82 ask=0.83 depth=750 spread=0.01 trade_id=none order=none fill_confirmed=0 cost=$unknown fee=$unknown spot=61441.51 threshold=61599.99 cushion=$158.47 subcell=57W-2L wilson=0.88 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=native_no_ask_out_of_guard:0.8300 ; id=1 live=false status=DRY_RUN ticker=KXBTCD-26JUL0302-T61599.99 side=NO qty=1 limit=0.79 bid=0.78 ask=0.79 depth=50 spread=0.01 trade_id=none order=none fill_confirmed=0 cost=$unknown fee=$unknown spot=61460.68 threshold=61599.99 cushion=$139.31 subcell=57W-2L wilson=0.88 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=native_no_ask_out_of_guard:0.7900

## Kalshi Weather Chicago Low 77-78 YES Pilot
- strategy: kalshi_live_pilot_weather_chi_low_77_78_yes_v1
- check_command: `python3 scripts/kalshi_weather_chi_low_77_78_yes_pilot.py`
- status: live_rows=1 dry_runs=0 filled_rows=0 cancelled_rows=0 | strategy_open=0 strategy_open_cost=$0.00 | all_live_pilot_open=5 all_live_pilot_cost=$0.50
- latest_rows: id=1 live=true status=RESOLVED_LOSS ticker=KXLOWTCHI-26JUL02-B77.5 side=YES qty=1 limit=0.81 bid=0.80 ask=0.81 depth=205 spread=0.01 trade_id=7105 order=059f7bf4 fill_confirmed=1 cost=$0.81 fee=$0.01 observed_min_f=78.08 forecast_min_f=83.00 resolution=LOSS pnl=-0.82 reason=none

## Kalshi Netflix Top Views NO Pilot
- strategy: kalshi_live_pilot_netflix_top_views_movie_25m_no_v1
- check_command: `python3 scripts/kalshi_netflix_top_views_no_pilot.py`
- status: live_rows=1 dry_runs=5 filled_rows=0 cancelled_rows=0 | strategy_open=0 strategy_open_cost=$0.00 | all_live_pilot_open=5 all_live_pilot_cost=$0.50
- latest_rows: id=6 live=false status=DRY_RUN ticker=KXNETFLIXTOPVIEWSMOVIE-26JUL06-25 side=NO qty=1 limit=0.13 bid=0.05 ask=0.13 depth=23 spread=0.08 trade_id=none order=none fill_confirmed=0 cost=$unknown fee=$unknown target_week=2026-07-05 latest_week=2026-06-28 latest_views_m=31.00 primary_no=13/23 primary_wilson=0.37 recent_no=5/15 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=native_no_ask_out_of_guard:0.1300 ; id=5 live=false status=DRY_RUN ticker=KXNETFLIXTOPVIEWSMOVIE-26JUL06-25 side=NO qty=1 limit=0.14 bid=0.05 ask=0.14 depth=10 spread=0.09 trade_id=none order=none fill_confirmed=0 cost=$unknown fee=$unknown target_week=2026-07-05 latest_week=2026-06-28 latest_views_m=31.00 primary_no=13/23 primary_wilson=0.37 recent_no=5/15 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=native_no_ask_out_of_guard:0.1400 ; id=4 live=false status=DRY_RUN ticker=KXNETFLIXTOPVIEWSMOVIE-26JUL06-25 side=NO qty=1 limit=0.14 bid=0.07 ask=0.14 depth=20 spread=0.07 trade_id=none order=none fill_confirmed=0 cost=$unknown fee=$unknown target_week=2026-07-05 latest_week=2026-06-28 latest_views_m=31.00 primary_no=13/23 primary_wilson=0.37 recent_no=5/15 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=native_no_ask_out_of_guard:0.1400 ; id=3 live=false status=DRY_RUN ticker=KXNETFLIXTOPVIEWSMOVIE-26JUL06-25 side=NO qty=1 limit=0.16 bid=0.06 ask=0.16 depth=15 spread=0.10 trade_id=none order=none fill_confirmed=0 cost=$unknown fee=$unknown target_week=2026-07-05 latest_week=2026-06-28 latest_views_m=31.00 primary_no=13/23 primary_wilson=0.37 recent_no=5/15 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=native_no_ask_out_of_guard:0.1600 ; id=2 live=false status=DRY_RUN ticker=KXNETFLIXTOPVIEWSMOVIE-26JUL06-25 side=NO qty=1 limit=0.06 bid=0.05 ask=0.06 depth=11 spread=0.01 trade_id=none order=none fill_confirmed=0 cost=$unknown fee=$unknown target_week=2026-07-05 latest_week=2026-06-28 latest_views_m=31.00 primary_no=13/23 primary_wilson=0.37 recent_no=5/15 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=static_preflight_failed

## Kalshi Netflix Top10 Rank Audit
- command: `python3 scripts/kalshi_netflix_top10_rank_audit.py --series KXNETFLIXRANKSHOWRUNNERUP,KXNETFLIXRANKSHOWGLOBAL,KXNETFLIXRANKMOVIEGLOBAL --limit 1000 --max-pages-per-series 2 --pause-seconds 0.05 --max-ask 0.25 --min-depth 1 --record --json`
- latest_run: captured_at=2026-07-03T21:21:49+00:00 | kalshi_markets=31 events=3 netflix_rows=30 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXNETFLIXRANKSHOWRUNNERUP,KXNETFLIXRANKSHOWGLOBAL,KXNETFLIXRANKMOVIEGLOBAL counts=KXNETFLIXRANKMOVIEGLOBAL=10, KXNETFLIXRANKSHOWGLOBAL=10, KXNETFLIXRANKSHOWRUNNERUP=11 | source_week_end=2026-06-28 | charts=KXNETFLIXRANKMOVIEGLOBAL:week=2026-06-28 range=Global | 6/22/26 - 6/28/26 rank1=Voicemails for Isabelle ; KXNETFLIXRANKSHOWGLOBAL:week=2026-06-28 range=Global | 6/22/26 - 6/28/26 rank1=I Will Find You: Limited Series ; KXNETFLIXRANKSHOWRUNNERUP:week=2026-06-28 range=United States | 6/22/26 - 6/28/26 rank2=Avatar: The Last Airbender: Season 2 | page_cap=none rate_limited=none | reasons=source_week_not_target=31

## Kalshi X Post Count Audit
- command: `python3 scripts/kalshi_x_post_count_audit.py --series KXIMFTWEETS,KXWEFTWEETS --limit 1000 --max-pages-per-series 2 --pause-seconds 0.05 --max-ask 0.25 --min-depth 1 --record --json`
- latest_run: captured_at=2026-07-03T21:21:48+00:00 | markets_checked=12 events=2 timelines=2 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXIMFTWEETS,KXWEFTWEETS counts=KXIMFTWEETS=6, KXWEFTWEETS=6 | events_summary=KXIMFTWEETS-26JUL09:handle=IMFNews visible=3 complete=true after_close=false window=2026-07-02T16:00:00+00:00->2026-07-09T16:00:00+00:00 ; KXWEFTWEETS-26JUL09:handle=wef visible=1 complete=true after_close=false window=2026-07-02T16:00:00+00:00->2026-07-09T16:00:00+00:00 | reasons=range_not_irreversible=8, over_not_irreversible=2, under_not_irreversible=2

## Kalshi MVE MLB Player State Audit
- command: `python3 scripts/kalshi_mve_mlb_player_state_audit.py --limit 0 --max-components 500 --max-dates 6 --pause-seconds 0.02 --max-target-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-02T17:47:16+00:00 | markets_checked=17223 supported_markets=17223 supported_legs=82795 espn_games=10 locked_rows=95 actionable_qty1=0 | max_target_ask=0.15 min_depth=1 | component_titles=400 component_failures=0 state_games=10 index_rows=160000 | reasons=supported_mlb_player_legs_not_locked=10749, some_supported_mlb_player_legs_true_but_mve_not_locked=6379, mlb_player_state_false_selected_leg_locks_mve_no=89, all_supported_mlb_player_state_legs_true_locks_mve_yes=6
- locked_rows: KXMVECROSSCATEGORY-S20264C28382C2C2-4D0DC50D4AD YES ask=0.00 depth=0 bid=0.00 win=1.00 legs=2/2/2 decisive=KXMLBKS-26JUL021235PITPHI-PHIARANGEL57-2:YES reason=mlb_player_stat_already_reached lock=all_supported_mlb_player_state_legs_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S20264C28382C2C2-7B1B02C9C52 YES ask=0.00 depth=0 bid=0.00 win=1.00 legs=2/2/2 decisive=KXMLBKS-26JUL021235PITPHI-PITJJONES17-3:YES reason=mlb_player_stat_already_reached lock=all_supported_mlb_player_state_legs_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S20264C9FA442D9A-248EC4FF99D YES ask=0.00 depth=0 bid=0.00 win=1.00 legs=2/2/2 decisive=KXMLBKS-26JUL021235PITPHI-PITJJONES17-4:YES reason=mlb_player_stat_already_reached lock=all_supported_mlb_player_state_legs_true_locks_mve_yes actionable=0 ; KXMVESPORTSMULTIGAMEEXTENDED-S20268E062B5C7B7-84848751D61 YES ask=0.00 depth=0 bid=0.00 win=1.00 legs=3/3/3 decisive=KXMLBKS-26JUL021235PITPHI-PITJJONES17-3:YES reason=mlb_player_stat_already_reached lock=all_supported_mlb_player_state_legs_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S2026124A15CA8AC-26F0C5EDAE4 NO ask=1.00 depth=0 bid=0.00 win=0.00 legs=2/2/2 decisive=KXMLBHIT-26JUL021235PITPHI-PHIBHARPER3-1:NO reason=mlb_player_stat_already_reached lock=mlb_player_state_false_selected_leg_locks_mve_no actionable=0 ; KXMVECROSSCATEGORY-S2026124A15CA8AC-3C6A3231625 NO ask=1.00 depth=0 bid=1.00 win=0.00 legs=2/2/2 decisive=KXMLBHIT-26JUL021235PITPHI-PHIBHARPER3-1:NO reason=mlb_player_stat_already_reached lock=mlb_player_state_false_selected_leg_locks_mve_no actionable=0 ; KXMVECROSSCATEGORY-S2026124A15CA8AC-6BC9157AD5D NO ask=1.00 depth=0 bid=0.00 win=0.00 legs=2/2/2 decisive=KXMLBHRR-26JUL021235PITPHI-PHIBHARPER3-2:NO reason=mlb_player_stat_already_reached lock=mlb_player_state_false_selected_leg_locks_mve_no actionable=0 ; KXMVECROSSCATEGORY-S2026124A15CA8AC-786A21AE056 NO ask=1.00 depth=0 bid=1.00 win=0.00 legs=1/2/2 decisive=KXMLBHRR-26JUL021235PITPHI-PHIBHARPER3-1:NO reason=mlb_player_stat_already_reached lock=mlb_player_state_false_selected_leg_locks_mve_no actionable=0

## Kalshi MLB Partial-Game State Audit
- command: `python3 scripts/kalshi_mlb_partial_game_state_audit.py --max-pages-per-series 6 --limit 1000 --max-dates 8 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T22:19:48+00:00 | markets_checked=920 parsed=920 espn_games=44 locked_rows=7 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXMLBRFI,KXMLBF3,KXMLBF5,KXMLBF5SPREAD,KXMLBF5TOTAL,KXMLBF7,KXMLBTEAMTOTAL,KXMLBEXTRAS dates=2026-07-03,2026-07-04,2026-07-05,2026-07-06 | state_games=44 | counts=KXMLBEXTRAS=44, KXMLBF3=72, KXMLBF5=72, KXMLBF5SPREAD=96, KXMLBF5TOTAL=168, KXMLBF7=75, KXMLBRFI=43, KXMLBTEAMTOTAL=350 | reasons=mlb_teamtotal_game_not_final=343, mlb_f5total_window_not_complete=168, mlb_f5spread_window_not_complete=96, mlb_f7_window_not_complete=75, mlb_f3_window_not_complete=72, mlb_f5_window_not_complete=72, mlb_extras_game_not_final=44, mlb_rfi_first_inning_not_complete=43
- locked_rows: KXMLBTEAMTOTAL-26JUL031605STLCHC-STL2 YES ask=1.00 depth=0 bid=0.99 win=0.00 type=teamtotal window=None target=STL threshold=1.50 margin=missing total=None game=STL@CHC 16-0 STATUS_IN_PROGRESS reason=mlb_teamtotal_over_already_exceeded actionable=0 ; KXMLBTEAMTOTAL-26JUL031605STLCHC-STL3 YES ask=1.00 depth=0 bid=0.99 win=0.00 type=teamtotal window=None target=STL threshold=2.50 margin=missing total=None game=STL@CHC 16-0 STATUS_IN_PROGRESS reason=mlb_teamtotal_over_already_exceeded actionable=0 ; KXMLBTEAMTOTAL-26JUL031605STLCHC-STL4 YES ask=1.00 depth=0 bid=0.99 win=0.00 type=teamtotal window=None target=STL threshold=3.50 margin=missing total=None game=STL@CHC 16-0 STATUS_IN_PROGRESS reason=mlb_teamtotal_over_already_exceeded actionable=0 ; KXMLBTEAMTOTAL-26JUL031605STLCHC-STL5 YES ask=1.00 depth=0 bid=0.99 win=0.00 type=teamtotal window=None target=STL threshold=4.50 margin=missing total=None game=STL@CHC 16-0 STATUS_IN_PROGRESS reason=mlb_teamtotal_over_already_exceeded actionable=0 ; KXMLBTEAMTOTAL-26JUL031605STLCHC-STL6 YES ask=1.00 depth=0 bid=0.99 win=0.00 type=teamtotal window=None target=STL threshold=5.50 margin=missing total=None game=STL@CHC 16-0 STATUS_IN_PROGRESS reason=mlb_teamtotal_over_already_exceeded actionable=0 ; KXMLBTEAMTOTAL-26JUL031605STLCHC-STL7 YES ask=1.00 depth=0 bid=0.99 win=0.00 type=teamtotal window=None target=STL threshold=6.50 margin=missing total=None game=STL@CHC 16-0 STATUS_IN_PROGRESS reason=mlb_teamtotal_over_already_exceeded actionable=0 ; KXMLBTEAMTOTAL-26JUL031605STLCHC-STL8 YES ask=1.00 depth=0 bid=0.99 win=0.00 type=teamtotal window=None target=STL threshold=7.50 margin=missing total=None game=STL@CHC 16-0 STATUS_IN_PROGRESS reason=mlb_teamtotal_over_already_exceeded actionable=0

## Kalshi WNBA Game State Audit
- command: `python3 scripts/kalshi_wnba_game_state_audit.py --max-pages-per-series 5 --limit 1000 --max-dates 8 --pause-seconds 1.0 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T22:19:48+00:00 | markets_checked=276 parsed=255 espn_games=4 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXWNBAGAME,KXWNBASPREAD,KXWNBATOTAL,KXWNBAOT,KXWNBA1QWINNER,KXWNBA2QWINNER,KXWNBA3QWINNER,KXWNBA4QWINNER,KXWNBA1HWINNER,KXWNBA2HWINNER,KXWNBA1QSPREAD,KXWNBA2QSPREAD,KXWNBA3QSPREAD,KXWNBA4QSPREAD,KXWNBA1HSPREAD,KXWNBA2HSPREAD,KXWNBA1QTOTAL,KXWNBA2QTOTAL,KXWNBA3QTOTAL,KXWNBA4QTOTAL,KXWNBA1HTOTAL,KXWNBA2HTOTAL dates=2026-07-03,2026-07-04,2026-07-05 | state_games=4 | counts=KXWNBA1HSPREAD=6, KXWNBA1HTOTAL=2, KXWNBA1HWINNER=6, KXWNBA1QSPREAD=14, KXWNBA1QTOTAL=14, KXWNBA1QWINNER=6, KXWNBA2HSPREAD=15, KXWNBA2HTOTAL=14, KXWNBA2HWINNER=6, KXWNBA2QSPREAD=14, KXWNBA2QTOTAL=14, KXWNBA2QWINNER=6, KXWNBA3QSPREAD=14, KXWNBA3QTOTAL=14, KXWNBA3QWINNER=6, KXWNBA4QSPREAD=14, KXWNBA4QTOTAL=14, KXWNBA4QWINNER=6, KXWNBAGAME=10, KXWNBAOT=5, KXWNBASPREAD=40, KXWNBATOTAL=36 | reasons=wnba_spread_game_not_final=31, wnba_total_game_not_final=27, wnba_2h_spread_not_complete=15, wnba_1q_spread_not_complete=14, wnba_1q_total_not_complete=14, wnba_2h_total_not_complete=14, wnba_2q_spread_not_complete=14, wnba_2q_total_not_complete=14

## Kalshi WNBA Player Prop State Audit
- command: `python3 scripts/kalshi_wnba_player_prop_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T22:19:12+00:00 | markets_checked=130 parsed=130 espn_games=2 locked_rows=0 actionable_qty1=0 | max_ask=0.98 min_depth=1 | series=KXWNBAPTS,KXWNBAREB,KXWNBAAST,KXWNBA3PT dates=2026-07-03 | state_games=2 titles=130 title_failures=0 summary_fetches=2 | counts=KXWNBA3PT=28, KXWNBAAST=11, KXWNBAPTS=49, KXWNBAREB=42 | reasons=wnba_player_boxscore_not_current=130

## Kalshi WNBA Player Prop Live Pilot
- strategy: kalshi_live_pilot_wnba_player_prop_boxscore_lock_v1
- check_command: `python3 scripts/kalshi_wnba_player_prop_live_pilot.py`
- status: live_rows=1 dry_runs=0 filled_rows=1 cancelled_rows=0 | strategy_open=0 strategy_open_cost=$0.00 | all_live_pilot_open=5 all_live_pilot_cost=$0.50
- latest_rows: id=1 live=true status=PLACED_FILLED ticker=KXWNBAREB-26JUL02ATLWSH-ATLAGRAY15-2 side=YES qty=1 limit=0.98 bid=0.97 ask=0.98 depth=10 modeled_fee=$0.01 win_pnl=$0.01 trade_id=7107 order=face9810 fill_confirmed=1 cost=$0.98 ledger_fee=$0.00 player=Allisha Gray stat=rebounds 2/2 clock=2:44 period=1 pred_p=1.00 edge=0.02 resolution=WIN pnl=+0.01 reason=wnba_player_stat_already_reached

## Kalshi AFL Game State Audit
- command: `python3 scripts/kalshi_afl_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 10 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T20:43:30+00:00 | markets_checked=14 parsed=14 espn_games=7 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXAFLGAME dates=2026-07-03,2026-07-04,2026-07-05,2026-07-06,2026-07-09 | state_games=7 | counts=KXAFLGAME=14 | reasons=afl_game_not_final=14

## Kalshi CFL Game State Audit
- command: `python3 scripts/kalshi_cfl_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T20:42:50+00:00 | markets_checked=8 parsed=8 official_games=93 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXCFLGAME dates=2026-07-03,2026-07-04,2026-07-05,2026-07-09 | state_games=4 rounds_raw=27 tournaments_raw=93 supported_games=93 | counts=KXCFLGAME=8 | source_errors=0 | reasons=cfl_game_not_final=8

## Kalshi BIG3 Game State Audit
- command: `python3 scripts/kalshi_big3_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T20:42:50+00:00 | markets_checked=8 parsed=8 official_games=32 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXBIG3GAME dates=2026-07-05 | state_games=4 events_raw=32 supported_games=32 | counts=KXBIG3GAME=8 | source_errors=0 | reasons=big3_game_not_final=8

## Kalshi Asia Baseball Game State Audit
- command: `python3 scripts/kalshi_asia_baseball_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 12 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T20:43:30+00:00 | markets_checked=44 parsed=44 official_games=22 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXKBOGAME,KXNPBGAME dates=2026-07-04,2026-07-05 | state_games=22 | counts=KXKBOGAME=20, KXNPBGAME=24 | source_errors=0 | reasons=npb_game_not_final=24, kbo_game_not_final=20

## Kalshi LMB Game State Audit
- command: `python3 scripts/kalshi_lmb_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 10 --pause-seconds 0.5 --max-ask 0.25 --min-depth 1 --tolerance-minutes 180`
- latest_run: captured_at=2026-07-03T19:25:13+00:00 | markets_checked=68 parsed=66 official_games=40 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXLMBGAME dates=2026-07-03,2026-07-02,2026-07-04,2026-07-05 | state_games=33 schedule_games=40 teams=20 | counts=KXLMBGAME=68 | source_errors=0 | reasons=lmb_game_not_final=50, no_matching_official_lmb_game_state=10, lmb_game_postponed_or_canceled=6

## Kalshi R6 Game State Audit
- command: `python3 scripts/kalshi_r6_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.5 --max-ask 0.25 --min-depth 1 --tolerance-minutes 180`
- latest_run: captured_at=2026-07-03T20:43:12+00:00 | markets_checked=20 parsed=20 official_games=44 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXR6GAME dates=2026-07-03,2026-07-04,2026-07-06 | state_games=20 calendar=2026-7 matches_raw=92 supported_games=44 | counts=KXR6GAME=20 | source_errors=0 | reasons=r6_game_not_final=20

## Kalshi VALORANT Game State Audit
- command: `python3 scripts/kalshi_valorant_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.5 --max-ask 0.25 --min-depth 1 --tolerance-minutes 180`
- latest_run: captured_at=2026-07-03T22:21:46+00:00 | markets_checked=32 parsed=32 official_games=80 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXVALORANTGAME dates=2026-07-03,2026-07-04,2026-07-05 | state_games=37 events_raw=80 supported_games=80 | counts=KXVALORANTGAME=32 | source_errors=0 | reasons=valorant_game_not_final=26, no_matching_official_valorant_game_state=6

## Kalshi LoL Game State Audit
- command: `python3 scripts/kalshi_lol_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.5 --max-ask 0.25 --min-depth 1 --tolerance-minutes 180`
- latest_run: captured_at=2026-07-03T22:21:46+00:00 | markets_checked=23 parsed=23 official_games=80 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXLOLGAME dates=2026-07-03,2026-07-02,2026-07-04,2026-07-05 | state_games=28 events_raw=80 supported_games=80 | counts=KXLOLGAME=23 | source_errors=0 | reasons=lol_game_not_final=18, lol_game_final_no_unique_winner=2, no_matching_official_lol_game_state=2, lol_game_target_not_in_game=1

## Kalshi CS2 Game State Audit
- command: `python3 scripts/kalshi_cs2_game_state_audit.py --max-pages-per-series 2 --limit 1000 --hltv-offsets 2 --hltv-pause-seconds 0.2 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T22:21:37+00:00 | markets_checked=40 groups=20 hltv_results=146 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXCS2GAME counts=KXCS2GAME=40 | hltv_index_pairs=135 fetches=2 raw_results=146 | reasons=no_hltv_match_pair=20

## Kalshi CS2 Total Maps State Audit
- command: `python3 scripts/kalshi_cs2_total_maps_state_audit.py --max-pages-per-series 2 --limit 1000 --hltv-offsets 2 --hltv-pause-seconds 0.2 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T19:23:01+00:00 | markets_checked=17 parsed=17 hltv_results=144 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXCS2TOTALMAPS counts=KXCS2TOTALMAPS=17 | hltv_index_pairs=133 fetches=2 raw_results=144 | reasons=no_hltv_match_pair=17

## Kalshi Tennis Final-State Audit
- command: `python3 scripts/kalshi_tennis_final_state_audit.py --series KXATPMATCH,KXWTAMATCH,KXATPDOUBLES,KXWTADOUBLES --limit 1000 --max-pages-per-series 2 --espn-event-limit 700 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T22:19:38+00:00 | kalshi_markets=100 groups=50 espn_matches=602 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXATPMATCH,KXWTAMATCH,KXATPDOUBLES,KXWTADOUBLES counts=KXATPDOUBLES=20, KXATPMATCH=24, KXWTADOUBLES=32, KXWTAMATCH=24 | espn_events=atp=1, wta=1 competitions=atp=304, wta=298 status_fetches=602 | reasons=espn_match_not_unique_completed=42, no_espn_match_pair=8

## Kalshi ITF Flashscore Match Audit
- command: `python3 scripts/kalshi_itf_flashscore_match_audit.py --series KXITFMATCH,KXITFWMATCH --limit 1000 --max-pages-per-series 2 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T21:22:44+00:00 | kalshi_markets=76 groups=38 flashscore_tournaments=20 flashscore_matches=591 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXITFMATCH,KXITFWMATCH counts=KXITFMATCH=36, KXITFWMATCH=40 | category_tournaments=KXITFMATCH=17, KXITFWMATCH=13 matched_tournaments=20 tournament_match_failures=0 | reasons=flashscore_match_not_unique_completed=34, no_flashscore_match_pair=4

## Kalshi Tennis Set-Score State Audit
- command: `python3 scripts/kalshi_tennis_set_score_audit.py --series KXATPSETWINNER,KXWTASETWINNER,KXATPEXACTMATCH,KXWTAEXACTMATCH --limit 1000 --max-pages-per-series 2 --espn-event-limit 700 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T22:21:24+00:00 | kalshi_markets=192 groups=72 espn_matches=602 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXATPSETWINNER,KXWTASETWINNER,KXATPEXACTMATCH,KXWTAEXACTMATCH counts=KXATPEXACTMATCH=72, KXATPSETWINNER=72, KXWTAEXACTMATCH=0, KXWTASETWINNER=48 | espn_events=atp=1, wta=1 competitions=atp=304, wta=298 status_fetches=602 linescore_fetches=1204 | reasons=espn_match_not_unique_completed=72

## Kalshi Esports Map Sweep Audit
- command: `python3 scripts/kalshi_esports_map_sweep_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.5 --max-ask 0.25 --min-depth 1 --tolerance-minutes 180`
- latest_run: captured_at=2026-07-03T22:21:46+00:00 | markets_checked=114 parsed=114 official_games=160 locked_rows=4 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXVALORANTMAP,KXLOLMAP dates=2026-07-03,2026-07-04,2026-07-05 | state_games=54 events_raw=160 supported_games=160 | counts=KXLOLMAP=46, KXVALORANTMAP=68 | source_errors=0 | proof=completed_clean_sweep_only | reasons=valorant_match_not_final=56, lol_match_not_final=40, no_matching_official_valorant_map_sweep_state=10, no_matching_official_lol_map_sweep_state=4, lol_map_clean_sweep_final=2, valorant_map_clean_sweep_final=2
- locked_rows: KXLOLMAP-26JUL031600MGVTC-2-MG NO ask=0.99 depth=0 bid=0.73 win=0.00 type=map2 target=Malvinas Gaming winner=Volticons game=Volticons vs Malvinas Gaming 2-0 completed source=lol_esports_official_schedule reason=lol_map_clean_sweep_final actionable=0 ; KXLOLMAP-26JUL031600MGVTC-2-VTC YES ask=0.99 depth=1 bid=0.61 win=0.00 type=map2 target=Volticons winner=Volticons game=Volticons vs Malvinas Gaming 2-0 completed source=lol_esports_official_schedule reason=lol_map_clean_sweep_final actionable=0 ; KXVALORANTMAP-26JUL031500UWKRSPARK-1-KRSPARK YES ask=1.00 depth=0 bid=0.76 win=0.00 type=map1 target=KRÜ SPARK winner=KRÜ SPARK game=University War vs KRÜ SPARK 0-2 completed source=valorant_esports_official_schedule reason=valorant_map_clean_sweep_final actionable=0 ; KXVALORANTMAP-26JUL031500UWKRSPARK-1-UW NO ask=1.00 depth=0 bid=0.30 win=0.00 type=map1 target=University War winner=KRÜ SPARK game=University War vs KRÜ SPARK 0-2 completed source=valorant_esports_official_schedule reason=valorant_map_clean_sweep_final actionable=0

## Kalshi FIBA Game State Audit
- command: `python3 scripts/kalshi_fiba_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1 --match-window-minutes 90`
- latest_run: captured_at=2026-07-03T20:42:50+00:00 | markets_checked=100 parsed=66 official_games=29 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXFIBAGAME dates=2026-06-30,2026-07-02,2026-07-03,2026-07-04,2026-07-05 | state_games=58 matched_markets=58 raw_games=180 supported_games=68 | counts=KXFIBAGAME=100 | source_errors=0 | reasons=fiba_game_not_final=58, no_matching_official_fiba_game_state=8

## Kalshi NZNBL Game State Audit
- command: `python3 scripts/kalshi_nznbl_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T20:43:30+00:00 | markets_checked=6 parsed=6 official_games=26 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXNZNBLGAME dates=2026-07-04,2026-07-05 | state_games=3 widget_rows=52 supported_games=26 | counts=KXNZNBLGAME=6 | source_errors=0 | reasons=nznbl_game_not_final=6

## Kalshi VBA Game State Audit
- command: `python3 scripts/kalshi_vba_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T19:25:13+00:00 | markets_checked=4 parsed=4 official_games=16 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXVBAGAME dates=2026-07-04,2026-07-05 | state_games=2 widget_rows=16 supported_games=16 | counts=KXVBAGAME=4 | source_errors=0 | reasons=vba_game_not_final=4

## Kalshi NBA Summer Game State Audit
- command: `python3 scripts/kalshi_nba_summer_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 10 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T20:42:50+00:00 | markets_checked=20 parsed=20 espn_games=10 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXNBASUMMERGAME dates=2026-07-03,2026-07-04,2026-07-05 | state_games=10 | counts=KXNBASUMMERGAME=20 | leagues=nba-summer-california=8, nba-summer-utah=2 | reasons=nba_summer_game_not_final=20

## Kalshi World Cup Corner State Audit
- command: `python3 scripts/kalshi_worldcup_corner_state_audit.py --max-pages-per-series 2 --limit 1000 --max-dates 8 --pause-seconds 0.25 --espn-pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T22:21:46+00:00 | markets_checked=77 parsed=77 espn_games=7 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXWCCORNERS,KXWCTCORNERS dates=2026-07-03,2026-07-04,2026-07-05,2026-07-06 | state_games=7 needed_events=7 | counts=KXWCCORNERS=35, KXWCTCORNERS=42 | reasons=team_corner_state_unknown=36, corner_state_unknown=30, team_corners_waiting_for_threshold_or_final=6, total_corners_waiting_for_threshold_or_final=5

## Kalshi World Cup Player Contribution State Audit
- command: `python3 scripts/kalshi_worldcup_player_contribution_state_audit.py --max-pages-per-series 2 --limit 1000 --max-dates 8 --pause-seconds 0.25 --espn-pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T19:25:59+00:00 | markets_checked=382 parsed=378 espn_games=9 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXWCGOAL,KXWCAST,KXWCSOA dates=2026-07-03,2026-07-04,2026-07-05,2026-07-06 | state_games=9 needed_events=9 | counts=KXWCAST=128, KXWCGOAL=163, KXWCSOA=91 | reasons=wc_player_goal_waiting_for_threshold_or_final=161, wc_player_assist_waiting_for_threshold_or_final=127, wc_player_score_or_assist_waiting_for_threshold_or_final=90, unparsed_market=4

## Kalshi World Cup Starting Lineup State Audit
- command: `python3 scripts/kalshi_worldcup_starting_lineup_state_audit.py --max-pages-per-series 2 --limit 1000 --max-dates 8 --pause-seconds 0.25 --espn-pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T19:26:28+00:00 | markets_checked=104 parsed=104 espn_games=2 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXWCSTART dates=2026-07-03,2026-07-06 | state_games=2 needed_events=2 | counts=KXWCSTART=104 | reasons=wc_start_lineup_not_available=104

## Kalshi Soccer Game State Audit
- command: `python3 scripts/kalshi_soccer_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 1.0 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T22:21:46+00:00 | markets_checked=60 parsed=54 espn_games=18 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXCHNSLGAME,KXALLSVENSKANGAME,KXBRASILEIROBGAME,KXBRASILEIROCGAME,KXUSLGAME,KXECULPGAME dates=2026-07-03,2026-07-02,2026-07-04,2026-07-01,2026-07-05,2026-07-06,2026-07-07,2026-07-08 | state_games=18 | counts=KXALLSVENSKANGAME=0, KXBRASILEIROBGAME=15, KXBRASILEIROCGAME=21, KXCHNSLGAME=0, KXECULPGAME=21, KXUSLGAME=3 | reasons=soccer_game_not_final=54

## Kalshi Broad Event-First Shadow Audit
- command: `python3 scripts/kalshi_shadow_event_first_audit.py --json`
- status: SHADOW_EVENT_FIRST_CANDIDATES | ready=false | eligible_cells=167 | candidate_cells=4 | ready_cells=0 | min_events=30 | edge_buffer=+2.0pp | scope=event-first shadow only; native execution still requires a separate forward gate
- best: shadow_longshot_fading:other:NO:weak:80-90:4-24h | gate=SHADOW_EVENT_FIRST_CANDIDATE | events=55 | 54W-1L | pnl=+771.83 | Wilson 90.4% vs target 85.3% (avg_price 83.3%) | target_gap=+5.1pp | blockers=none
- rank 1: shadow_longshot_fading:other:NO:weak:80-90:4-24h | gate=SHADOW_EVENT_FIRST_CANDIDATE | events=55 | 54W-1L | pnl=+771.83 | Wilson 90.4% vs target 85.3% (avg_price 83.3%) | target_gap=+5.1pp | blockers=none
- rank 2: shadow_longshot_fading:crypto:NO:moderate:80-90:<1h | gate=SHADOW_EVENT_FIRST_CANDIDATE | events=599 | 554W-45L | pnl=+2501.87 | Wilson 90.1% vs target 89.5% (avg_price 87.5%) | target_gap=+0.5pp | blockers=none
- rank 3: shadow_deterministic_settlement:ETH:YES:50-80:<1h | gate=SHADOW_EVENT_FIRST_CANDIDATE | events=83 | 67W-16L | pnl=+995.78 | Wilson 71.0% vs target 70.7% (avg_price 68.7%) | target_gap=+0.2pp | blockers=none
- rank 4: shadow_longshot_fading:crypto:NO:weak:80-90:<1h | gate=SHADOW_EVENT_FIRST_CANDIDATE | events=848 | 741W-107L | pnl=+3025.97 | Wilson 85.0% vs target 84.8% (avg_price 82.8%) | target_gap=+0.2pp | blockers=none

## Kalshi Shadow Longshot Stability Audit
- command: `python3 scripts/kalshi_shadow_longshot_stability_audit.py --limit 8`
- status: NO_SHADOW_STABILITY_CANDIDATES | ready=false | event_rows=7036 | eligible_cells=25 | base_candidate_cells=3 | stable_candidate_cells=0 | ready_cells=0 | min_events=30 | min_train=30 | min_validation=15 | min_slice=20 | edge_buffer=+2.0pp
- 1. shadow_longshot_fading:crypto:NO:moderate:80-90:<1h | gate=SHADOW_STABILITY_REJECT | aggregate=599ev 554W-45L +2501.87 Wilson 90.1% vs target 89.5% gap +0.5pp | train=419ev 388W-31L +1779.15 Wilson 89.7% vs target 89.6% gap +0.1pp | validation=180ev 166W-14L +722.72 Wilson 87.4% vs target 89.4% gap -2.1pp | worst_asset=KXSOLD 112ev 104W-8L +511.92 Wilson 86.5% vs target 89.5% gap -3.0pp | worst_hour=15Z 23ev 18W-5L -231.64 Wilson 58.1% vs target 89.6% gap -31.5pp | blockers=validation_wilson<avg_price+buffer;asset_slice_wilson<avg_price:KXSOLD;utc_hour_slice_pnl<=0:15Z;utc_hour_slice_wilson<avg_price:15Z
- 2. shadow_longshot_fading:other:NO:weak:80-90:4-24h | gate=SHADOW_STABILITY_REJECT | aggregate=55ev 54W-1L +771.83 Wilson 90.4% vs target 85.3% gap +5.1pp | train=38ev 37W-1L +487.74 Wilson 86.5% vs target 85.7% gap +0.8pp | validation=17ev 17W-0L +284.09 Wilson 81.6% vs target 84.4% gap -2.8pp | worst_asset=none>=min_slice | worst_hour=none>=min_slice | blockers=validation_wilson<avg_price+buffer
- 3. shadow_longshot_fading:crypto:NO:weak:80-90:<1h | gate=SHADOW_STABILITY_REJECT | aggregate=848ev 741W-107L +3025.97 Wilson 85.0% vs target 84.8% gap +0.2pp | train=593ev 529W-64L +3328.60 Wilson 86.5% vs target 84.6% gap +1.9pp | validation=255ev 212W-43L -302.63 Wilson 78.1% vs target 85.3% gap -7.3pp | worst_asset=KXBTCD 449ev 383W-66L +711.91 Wilson 81.7% vs target 84.7% gap -3.0pp | worst_hour=13Z 35ev 25W-10L -449.18 Wilson 54.9% vs target 85.3% gap -30.3pp | blockers=validation_pnl<=0;validation_wilson<avg_price+buffer;asset_slice_wilson<avg_price:KXBTCD;utc_hour_slice_pnl<=0:13Z;utc_hour_slice_wilson<avg_price:13Z

## Kalshi Shadow Longshot Filtered Stability Audit
- command: `python3 scripts/kalshi_shadow_longshot_filtered_stability_audit.py --limit 8`
- status: NO_FILTERED_SHADOW_STABILITY_CANDIDATES | ready=false | event_rows=7036 | base_candidate_cells=3 | filtered_cells=74 | filtered_candidate_cells=0 | ready_cells=0 | min_events=30 | min_train=30 | min_validation=15 | min_slice=20 | edge_buffer=+2.0pp
- 1. shadow_longshot_fading:crypto:NO:moderate:80-90:<1h|exclude_hour=02Z | gate=FILTERED_SHADOW_STABILITY_REJECT | filter=exclude_hour=02Z | excluded=34 | aggregate=565ev 525W-40L +2586.94 Wilson 90.5% vs target 89.6% gap +0.9pp | train=395ev 366W-29L +1684.36 Wilson 89.7% vs target 89.6% gap +0.0pp | validation=170ev 159W-11L +902.58 Wilson 88.8% vs target 89.4% gap -0.7pp | worst_asset=KXSOLD 103ev 96W-7L +497.35 Wilson 86.6% vs target 89.6% gap -3.0pp | worst_hour=15Z 23ev 18W-5L -231.64 Wilson 58.1% vs target 89.6% gap -31.5pp | blockers=validation_wilson<avg_price+buffer;asset_slice_wilson<avg_price:KXSOLD;utc_hour_slice_pnl<=0:15Z;utc_hour_slice_wilson<avg_price:15Z
- 2. shadow_longshot_fading:crypto:NO:moderate:80-90:<1h|exclude_hour=01Z | gate=FILTERED_SHADOW_STABILITY_REJECT | filter=exclude_hour=01Z | excluded=38 | aggregate=561ev 519W-42L +2367.50 Wilson 90.0% vs target 89.5% gap +0.5pp | train=392ev 362W-30L +1573.33 Wilson 89.3% vs target 89.6% gap -0.3pp | validation=169ev 157W-12L +794.17 Wilson 88.0% vs target 89.4% gap -1.4pp | worst_asset=KXSOLD 102ev 94W-8L +398.41 Wilson 85.3% vs target 89.5% gap -4.2pp | worst_hour=15Z 23ev 18W-5L -231.64 Wilson 58.1% vs target 89.6% gap -31.5pp | blockers=train_wilson<avg_price+buffer;validation_wilson<avg_price+buffer;asset_slice_wilson<avg_price:KXSOLD;utc_hour_slice_pnl<=0:15Z;utc_hour_slice_wilson<avg_price:15Z
- 3. shadow_longshot_fading:crypto:NO:moderate:80-90:<1h|exclude_hour=13Z | gate=FILTERED_SHADOW_STABILITY_REJECT | filter=exclude_hour=13Z | excluded=22 | aggregate=577ev 536W-41L +2644.74 Wilson 90.5% vs target 89.5% gap +1.0pp | train=403ev 375W-28L +1889.57 Wilson 90.1% vs target 89.6% gap +0.5pp | validation=174ev 161W-13L +755.17 Wilson 87.6% vs target 89.4% gap -1.8pp | worst_asset=KXETHD 93ev 87W-6L +503.57 Wilson 86.6% vs target 89.4% gap -2.7pp | worst_hour=15Z 23ev 18W-5L -231.64 Wilson 58.1% vs target 89.6% gap -31.5pp | blockers=validation_wilson<avg_price+buffer;asset_slice_wilson<avg_price:KXETHD;utc_hour_slice_pnl<=0:15Z;utc_hour_slice_wilson<avg_price:15Z
- 4. shadow_longshot_fading:crypto:NO:moderate:80-90:<1h|exclude_hour=09Z | gate=FILTERED_SHADOW_STABILITY_REJECT | filter=exclude_hour=09Z | excluded=22 | aggregate=577ev 533W-44L +2345.71 Wilson 89.9% vs target 89.5% gap +0.4pp | train=403ev 372W-31L +1593.37 Wilson 89.3% vs target 89.6% gap -0.3pp | validation=174ev 161W-13L +752.34 Wilson 87.6% vs target 89.4% gap -1.8pp | worst_asset=KXSOLD 109ev 101W-8L +476.25 Wilson 86.2% vs target 89.5% gap -3.3pp | worst_hour=15Z 23ev 18W-5L -231.64 Wilson 58.1% vs target 89.6% gap -31.5pp | blockers=train_wilson<avg_price+buffer;validation_wilson<avg_price+buffer;asset_slice_wilson<avg_price:KXSOLD;utc_hour_slice_pnl<=0:15Z;utc_hour_slice_wilson<avg_price:15Z
- 5. shadow_longshot_fading:crypto:NO:moderate:80-90:<1h|exclude_hour=15Z | gate=FILTERED_SHADOW_STABILITY_REJECT | filter=exclude_hour=15Z | excluded=23 | aggregate=576ev 536W-40L +2733.51 Wilson 90.7% vs target 89.5% gap +1.1pp | train=403ev 376W-27L +1993.37 Wilson 90.4% vs target 89.6% gap +0.8pp | validation=173ev 160W-13L +740.14 Wilson 87.6% vs target 89.4% gap -1.9pp | worst_asset=KXETHD 91ev 85W-6L +483.89 Wilson 86.4% vs target 89.3% gap -3.0pp | worst_hour=13Z 22ev 18W-4L -142.87 Wilson 61.5% vs target 89.5% gap -28.1pp | blockers=validation_wilson<avg_price+buffer;asset_slice_wilson<avg_price:KXETHD;utc_hour_slice_pnl<=0:13Z;utc_hour_slice_wilson<avg_price:13Z
- 6. shadow_longshot_fading:crypto:NO:moderate:80-90:<1h|exclude_asset=KXETHD | gate=FILTERED_SHADOW_STABILITY_REJECT | filter=exclude_asset=KXETHD | excluded=94 | aggregate=505ev 466W-39L +1985.15 Wilson 89.6% vs target 89.6% gap +0.0pp | train=353ev 325W-28L +1295.62 Wilson 88.8% vs target 89.6% gap -0.9pp | validation=152ev 141W-11L +689.53 Wilson 87.5% vs target 89.5% gap -1.9pp | worst_asset=KXSOLD 112ev 104W-8L +511.92 Wilson 86.5% vs target 89.5% gap -3.0pp | worst_hour=15Z 20ev 15W-5L -264.47 Wilson 53.1% vs target 89.5% gap -36.3pp | blockers=train_wilson<avg_price+buffer;validation_wilson<avg_price+buffer;asset_slice_wilson<avg_price:KXSOLD;utc_hour_slice_pnl<=0:15Z;utc_hour_slice_wilson<avg_price:15Z
- 7. shadow_longshot_fading:crypto:NO:moderate:80-90:<1h|exclude_hour=12Z | gate=FILTERED_SHADOW_STABILITY_REJECT | filter=exclude_hour=12Z | excluded=27 | aggregate=572ev 530W-42L +2477.11 Wilson 90.2% vs target 89.6% gap +0.7pp | train=400ev 371W-29L +1755.80 Wilson 89.8% vs target 89.6% gap +0.2pp | validation=172ev 159W-13L +721.31 Wilson 87.5% vs target 89.5% gap -2.0pp | worst_asset=KXSOLD 106ev 98W-8L +436.80 Wilson 85.8% vs target 89.6% gap -3.8pp | worst_hour=15Z 23ev 18W-5L -231.64 Wilson 58.1% vs target 89.6% gap -31.5pp | blockers=validation_wilson<avg_price+buffer;asset_slice_wilson<avg_price:KXSOLD;utc_hour_slice_pnl<=0:15Z;utc_hour_slice_wilson<avg_price:15Z
- 8. shadow_longshot_fading:crypto:NO:moderate:80-90:<1h|exclude_hour=03Z | gate=FILTERED_SHADOW_STABILITY_REJECT | filter=exclude_hour=03Z | excluded=34 | aggregate=565ev 523W-42L +2409.66 Wilson 90.1% vs target 89.5% gap +0.6pp | train=395ev 366W-29L +1708.02 Wilson 89.7% vs target 89.6% gap +0.1pp | validation=170ev 157W-13L +701.64 Wilson 87.4% vs target 89.5% gap -2.1pp | worst_asset=KXETHD 89ev 83W-6L +455.70 Wilson 86.1% vs target 89.4% gap -3.3pp | worst_hour=15Z 23ev 18W-5L -231.64 Wilson 58.1% vs target 89.6% gap -31.5pp | blockers=validation_wilson<avg_price+buffer;asset_slice_wilson<avg_price:KXETHD;utc_hour_slice_pnl<=0:15Z;utc_hour_slice_wilson<avg_price:15Z

## Kalshi Legacy Shadow Surface Audit
- command: `python3 scripts/kalshi_legacy_shadow_surface_audit.py --limit 8`
- status: LEGACY_SHADOW_FORWARD_REQUIRED | ready=false | eligible_cells=139 | candidate_cells=1 | ready_cells=0 | min_events=30 | edge_buffer=+2.0pp | scope=legacy_shadow_only_requires_native_or_maker_forward_gate
- best: moderate_favorites:CRYPTO:ETH:YES:80-90:0-1H:liq1:spread1 | gate=LEGACY_SHADOW_FORWARD_REQUIRED | execution=legacy_taker_like_shadow | events=67 | 64W-3L | pnl=+$851.00 | Wilson 87.6% vs target 84.7% (BE 82.7%, avg_price 82.8%) | gap=+3.0pp | blockers=none | promotion_blockers=requires_native_or_maker_forward_gate
- rank 1: moderate_favorites:CRYPTO:ETH:YES:80-90:0-1H:liq1:spread1 | gate=LEGACY_SHADOW_FORWARD_REQUIRED | execution=legacy_taker_like_shadow | events=67 | 64W-3L | pnl=+$851.00 | Wilson 87.6% vs target 84.7% (BE 82.7%, avg_price 82.8%) | gap=+3.0pp | blockers=none | promotion_blockers=requires_native_or_maker_forward_gate
- rank 2: untapped_bid_side:FX:NO:90-95:4-24h | gate=LEGACY_SHADOW_REJECT | execution=legacy_bid_side_maker | events=47 | 47W-0L | pnl=+$324.36 | Wilson 92.4% vs target 95.1% (BE 93.1%, avg_price 92.6%) | gap=-2.6pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=28
- rank 3: weather_city_bid_side:KXHIGHTSEA:NO:90-95:unblocked | gate=LEGACY_SHADOW_REJECT | execution=legacy_bid_side_maker | events=45 | 45W-0L | pnl=+$323.50 | Wilson 92.1% vs target 94.8% (BE 92.8%, avg_price 92.3%) | gap=-2.6pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=25
- rank 4: weather_city_bid_side:KXHIGHTPHX:NO:90-95:unblocked | gate=LEGACY_SHADOW_REJECT | execution=legacy_bid_side_maker | events=43 | 43W-0L | pnl=+$319.84 | Wilson 91.8% vs target 94.5% (BE 92.5%, avg_price 92.0%) | gap=-2.7pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=24
- rank 5: weather_city_bid_side:KXHIGHTMIN:NO:90-95:unblocked | gate=LEGACY_SHADOW_REJECT | execution=legacy_bid_side_maker | events=44 | 44W-0L | pnl=+$306.60 | Wilson 92.0% vs target 95.0% (BE 93.0%, avg_price 92.5%) | gap=-3.0pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=29
- rank 6: untapped_bid_side:FX:NO:80-90:4-24h | gate=LEGACY_SHADOW_REJECT | execution=legacy_bid_side_maker | events=61 | 58W-3L | pnl=+$432.10 | Wilson 86.5% vs target 90.0% (BE 88.0%, avg_price 87.2%) | gap=-3.5pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=23
- rank 7: sell_inverse:WEATHER:NO:95+:4-24h | gate=LEGACY_SHADOW_REJECT | execution=legacy_inverse_shadow | events=709 | 6W-703L | pnl=-$701.15 | Wilson 0.4% vs target 3.9% (BE 1.9%, avg_price 98.3%) | gap=-3.5pp | blockers=pnl<=0;wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=33
- rank 8: weather_city_bid_side:KXHIGHTHOU:NO:90-95:unblocked | gate=LEGACY_SHADOW_REJECT | execution=legacy_bid_side_maker | events=41 | 41W-0L | pnl=+$286.98 | Wilson 91.4% vs target 95.0% (BE 93.0%, avg_price 92.5%) | gap=-3.5pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=32

## Kalshi Moderate Favorites ETH YES Native Preflight
- command: `python3 scripts/kalshi_moderate_favorites_eth_yes_preflight.py --json --fetch-delay-seconds 0`
- latest_run: captured_at=2026-07-03T23:01:41+00:00 | cohort=moderate_favorites_eth_yes_80_90_0_1h_v1 | start=2026-07-03T16:50:00+00:00 | include_pre_cutoff_live=false | candidates=0 checked=0 actionable_qty1=0 | top_reasons=none

## Kalshi Weather YES 90-93 Native Preflight
- command: `python3 scripts/kalshi_weather_yes_90_93_preflight.py --json --fetch-delay-seconds 0`
- latest_run: captured_at=2026-07-03T23:05:34+00:00 | cohort=yes_90_93_above_live_threshold_v1 | start=2026-06-25T11:45:00+00:00 | include_pre_cutoff_live=true | candidates=3 checked=3 actionable_qty1=1 | top_reasons=yes_90_93_above_live_threshold_v1:actionable_qty1_fee_positive=1, yes_90_93_above_live_threshold_v1:native_yes_ask_below_band_watch:0.8800=1, yes_90_93_above_live_threshold_v1:native_yes_ask_out_of_band:0.9700=1
- latest_rows: KXHIGHPHIL-26JUL03-B101.5 city=PHIL yes_ask=0.90 no_depth=33 reason=actionable_qty1_fee_positive ; KXLOWTMIA-26JUL03-B78.5 city=MIA yes_ask=0.88 no_depth=6 reason=native_yes_ask_below_band_watch:0.8800 ; KXLOWTPHIL-26JUL03-B82.5 city=PHIL yes_ask=0.97 no_depth=5 reason=native_yes_ask_out_of_band:0.9700

## Kalshi Weather NO Candidate Native Preflight
- command: `python3 scripts/kalshi_weather_no_candidate_preflight.py --json --fetch-delay-seconds 0`
- latest_run: captured_at=2026-07-03T23:03:40+00:00 | start=2026-06-25T07:05:00+00:00 | include_pre_cutoff_live=false | candidates=16 checked=16 actionable_qty1=4 | top_reasons=no_95_98_zero_loss_cities_v1:missing_native_no_ask=6, no_95_98_zero_loss_cities_v1:actionable_qty1_fee_positive=4, no_95_98_zero_loss_cities_v1:native_no_ask_out_of_band:0.9900=3, no_90_95_min_probe_v1:native_no_ask_out_of_band:0.9700=1, no_90_95_min_probe_v1:native_no_ask_out_of_band:0.9800=1, no_95_98_zero_loss_cities_v1:native_no_ask_out_of_band:0.7700=1
- latest_rows: KXLOWTMIA-26JUL04-B74.5 cohort=no_95_98_zero_loss_cities_v1 city=MIA no_ask=0.96 no_ask_depth=1 qty1=+0.03/-0.97 reason=actionable_qty1_fee_positive due=2026-07-05T19:00:00+00:00 ; KXHIGHTMIN-26JUL03-B87.5 cohort=no_95_98_zero_loss_cities_v1 city=MIN no_ask=0.97 no_ask_depth=10 qty1=+0.02/-0.98 reason=actionable_qty1_fee_positive due=2026-07-04T19:00:00+00:00 ; KXHIGHTOKC-26JUL04-B104.5 cohort=no_95_98_zero_loss_cities_v1 city=OKC no_ask=0.97 no_ask_depth=169 qty1=+0.02/-0.98 reason=actionable_qty1_fee_positive due=2026-07-05T19:00:00+00:00 ; KXHIGHTSEA-26JUL04-B78.5 cohort=no_95_98_zero_loss_cities_v1 city=SEA no_ask=0.97 no_ask_depth=127 qty1=+0.02/-0.98 reason=actionable_qty1_fee_positive due=2026-07-05T19:00:00+00:00 ; KXHIGHTMIN-26JUL03-B87.5 cohort=no_90_95_min_probe_v1 city=MIN no_ask=0.97 no_ask_depth=10 qty1=+0.02/-0.98 reason=native_no_ask_out_of_band:0.9700 due=2026-07-04T19:00:00+00:00 ; KXHIGHTMIN-26JUL04-T78 cohort=no_90_95_min_probe_v1 city=MIN no_ask=0.98 no_ask_depth=53 qty1=+0.01/-0.99 reason=native_no_ask_out_of_band:0.9800 due=2026-07-05T19:00:00+00:00 ; KXLOWTAUS-26JUL03-B70.5 cohort=no_95_98_zero_loss_cities_v1 city=AUS no_ask=missing no_ask_depth=0 qty1=n/a/n/a reason=missing_native_no_ask due=2026-07-04T19:00:00+00:00 ; KXLOWTAUS-26JUL04-B72.5 cohort=no_95_98_zero_loss_cities_v1 city=AUS no_ask=0.77 no_ask_depth=4 qty1=+0.21/-0.79 reason=native_no_ask_out_of_band:0.7700 due=2026-07-05T19:00:00+00:00

## Kalshi Other Longshot NO Native Preflight
- command: `python3 scripts/kalshi_other_longshot_no_80_90_preflight.py --json --fetch-delay-seconds 0`
- latest_run: captured_at=2026-07-03T23:05:25+00:00 | cohort=all | start=2026-06-25T20:00:00+00:00 | include_pre_cutoff_live=true | candidates=0 checked=0 actionable_qty1=0 | top_reasons=none

## Kalshi Index/FX Low-Price NO Favtrack Native Preflight
- command: `python3 scripts/kalshi_index_fx_low_price_no_favorite_tracking_preflight.py --json --fetch-delay-seconds 0`
- methodology_status: non-live favorite_tracking source; native-forward evidence only
- latest_run: captured_at=2026-07-03T19:11:41+00:00 | start=2026-06-26T17:10:00+00:00 | include_pre_cutoff_live=false | candidates=0 checked=0 actionable_qty1=0 | top_reasons=none

## Kalshi Maker Forward Proxy Leaderboard
- command: `python3 scripts/kalshi_maker_forward_leaderboard.py --json`
- status: NO_LIVE_READY | ready=false | cells=15 | ready_cells=0 | review_min=50 | fills=1904 pending_units=504 active=504 stale=0 unknown=0 overall_resolved_indep=1400 toxic=481 | next_pending=cell_sports_no:KXMLBSPREAD-26JUN301907NYMTOR-NYM4 status=active close=2026-07-03T23:07:00+00:00
- best: cell_sports_no | gate=NO_GO_REVIEW | resolved_indep=413/50 max_if_pending_resolve=706 new_needed_after_pending=0 | 318W-95L | pnl=-435.44 | Wilson 72.7% vs BE 87.5% | gap=-14.8pp | fills=706/2476 fill_rate=28.5% pending_units=293 active=293 stale=0 unknown=0 toxic=95 | blockers=pnl<=0; wilson<=BE; toxic>0 | perfect_benign_wins_needed=blocked_or_>5000 | next_pending=KXMLBSPREAD-26JUN301907NYMTOR-NYM4 status=active close=2026-07-03T23:07:00+00:00 price=0.93
- rank 1: cell_sports_no | gate=NO_GO_REVIEW | resolved_indep=413/50 max_if_pending_resolve=706 new_needed_after_pending=0 | 318W-95L | pnl=-435.44 | Wilson 72.7% vs BE 87.5% | gap=-14.8pp | fills=706/2476 fill_rate=28.5% pending_units=293 active=293 stale=0 unknown=0 toxic=95 | blockers=pnl<=0; wilson<=BE; toxic>0 | perfect_benign_wins_needed=blocked_or_>5000 | next_pending=KXMLBSPREAD-26JUN301907NYMTOR-NYM4 status=active close=2026-07-03T23:07:00+00:00 price=0.93
- rank 2: cell_crypto_yes | gate=NO_GO_REVIEW | resolved_indep=320/50 max_if_pending_resolve=345 new_needed_after_pending=0 | 176W-144L | pnl=-1002.41 | Wilson 49.5% vs BE 86.3% | gap=-36.8pp | fills=345/1188 fill_rate=29.0% pending_units=25 active=25 stale=0 unknown=0 toxic=144 | blockers=pnl<=0; wilson<=BE; toxic>0 | perfect_benign_wins_needed=blocked_or_>5000 | next_pending=KXBTCD-26JUL0417-T61749.99 status=active close=2026-07-04T21:00:00+00:00 price=0.87
- rank 3: cell_crypto_no | gate=NO_GO_REVIEW | resolved_indep=294/50 max_if_pending_resolve=318 new_needed_after_pending=0 | 162W-132L | pnl=-936.22 | Wilson 49.4% vs BE 86.9% | gap=-37.6pp | fills=318/1051 fill_rate=30.3% pending_units=24 active=24 stale=0 unknown=0 toxic=132 | blockers=pnl<=0; wilson<=BE; toxic>0 | perfect_benign_wins_needed=blocked_or_>5000 | next_pending=KXBTCD-26JUL0417-T59749.99 status=active close=2026-07-04T21:00:00+00:00 price=0.79
- rank 4: cell_sports_yes | gate=NO_GO_REVIEW | resolved_indep=124/50 max_if_pending_resolve=256 new_needed_after_pending=0 | 49W-75L | pnl=-588.58 | Wilson 31.4% vs BE 87.0% | gap=-55.6pp | fills=256/416 fill_rate=61.5% pending_units=132 active=132 stale=0 unknown=0 toxic=75 | blockers=pnl<=0; wilson<=BE; toxic>0 | perfect_benign_wins_needed=blocked_or_>5000 | next_pending=KXMLBSPREAD-26JUN301910WSHBOS-WSH6 status=active close=2026-07-03T23:10:00+00:00 price=0.84
- rank 5: cell_index_no | gate=NO_GO_REVIEW | resolved_indep=113/50 max_if_pending_resolve=113 new_needed_after_pending=0 | 101W-12L | pnl=-29.57 | Wilson 82.4% vs BE 91.9% | gap=-9.6pp | fills=113/1944 fill_rate=5.8% pending_units=0 active=0 stale=0 unknown=0 toxic=12 | blockers=pnl<=0; wilson<=BE; toxic>0 | perfect_benign_wins_needed=blocked_or_>5000
- rank 6: cell_weather_no | gate=NO_GO_REVIEW | resolved_indep=110/50 max_if_pending_resolve=137 new_needed_after_pending=0 | 90W-20L | pnl=-87.20 | Wilson 73.6% vs BE 89.7% | gap=-16.2pp | fills=137/293 fill_rate=46.8% pending_units=27 active=27 stale=0 unknown=0 toxic=20 | blockers=pnl<=0; wilson<=BE; toxic>0 | perfect_benign_wins_needed=blocked_or_>5000 | next_pending=KXHIGHMIA-26JUL03-B88.5 status=active close=2026-07-04T04:59:00+00:00 price=0.94
- rank 7: watch_crypto_bid_90_95 | gate=NO_GO_REVIEW | resolved_indep=103/50 max_if_pending_resolve=110 new_needed_after_pending=0 | 95W-8L | pnl=-14.13 | Wilson 85.4% vs BE 93.6% | gap=-8.2pp | fills=110/496 fill_rate=22.2% pending_units=7 active=7 stale=0 unknown=0 toxic=8 | blockers=pnl<=0; wilson<=BE; toxic>0 | perfect_benign_wins_needed=blocked_or_>5000 | next_pending=KXBTCD-26JUL0417-T63249.99 status=active close=2026-07-04T21:00:00+00:00 price=0.94
- rank 8: watch_crypto_bid_92_94 | gate=NO_GO_REVIEW | resolved_indep=58/50 max_if_pending_resolve=61 new_needed_after_pending=0 | 54W-4L | pnl=-6.17 | Wilson 83.6% vs BE 94.2% | gap=-10.6pp | fills=61/264 fill_rate=23.1% pending_units=3 active=3 stale=0 unknown=0 toxic=4 | blockers=pnl<=0; wilson<=BE; toxic>0 | perfect_benign_wins_needed=blocked_or_>5000 | next_pending=KXBTCD-26JUL0417-T63249.99 status=active close=2026-07-04T21:00:00+00:00 price=0.94

## Kalshi Maker Price-Band Cut Audit
- query: `kalshi_high_price_maker_cancel_shadow` grouped by category/side/maker_price_band
- scope: discovery-only subcell audit; live trading still requires the main maker gate and toxic=0
- status: NO_MAKER_CUT_READY | ready=false | cells=24 | display_cells=19 | ready_cells=0 | positive_cells=5 | review_min=50
- best: index NO maker_band=85-90 | gate=ACCUMULATING | resolved_indep=15/50 | 14W-1L | pnl=+8.38 | Wilson 70.2% vs BE 87.7% | gap=-17.5pp | candidates=181 fills=15 fill_rate=8.3% pending_units=0 toxic=1 | blockers=resolved<50; wilson<=BE; toxic>0
- rank 1: index NO maker_band=85-90 | gate=ACCUMULATING | resolved_indep=15/50 | 14W-1L | pnl=+8.38 | Wilson 70.2% vs BE 87.7% | gap=-17.5pp | candidates=181 fills=15 fill_rate=8.3% pending_units=0 toxic=1 | blockers=resolved<50; wilson<=BE; toxic>0
- rank 2: weather YES maker_band=<85 | gate=ACCUMULATING | resolved_indep=14/50 | 12W-2L | pnl=+4.93 | Wilson 60.1% vs BE 82.2% | gap=-22.1pp | candidates=27 fills=15 fill_rate=55.6% pending_units=1 toxic=2 | blockers=resolved<50; wilson<=BE; toxic>0
- rank 3: weather YES maker_band=85-90 | gate=ACCUMULATING | resolved_indep=9/50 | 8W-1L | pnl=+0.48 | Wilson 56.5% vs BE 88.4% | gap=-31.9pp | candidates=18 fills=11 fill_rate=61.1% pending_units=2 toxic=1 | blockers=resolved<50; wilson<=BE; toxic>0
- rank 4: crypto YES maker_band=90-95 | gate=NO_GO_REVIEW | resolved_indep=95/50 | 85W-10L | pnl=-34.58 | Wilson 81.7% vs BE 93.1% | gap=-11.4pp | candidates=379 fills=99 fill_rate=26.1% pending_units=4 toxic=10 | blockers=pnl<=0; wilson<=BE; toxic>0
- rank 5: index NO maker_band=90-95 | gate=NO_GO_REVIEW | resolved_indep=94/50 | 83W-11L | pnl=-44.59 | Wilson 80.2% vs BE 93.0% | gap=-12.7pp | candidates=1709 fills=94 fill_rate=5.5% pending_units=0 toxic=11 | blockers=pnl<=0; wilson<=BE; toxic>0
- rank 6: sports NO maker_band=85-90 | gate=NO_GO_REVIEW | resolved_indep=104/50 | 85W-19L | pnl=-63.36 | Wilson 73.2% vs BE 87.8% | gap=-14.6pp | candidates=645 fills=201 fill_rate=31.2% pending_units=97 toxic=19 | blockers=pnl<=0; wilson<=BE; toxic>0
- rank 7: weather NO maker_band=90-95 | gate=NO_GO_REVIEW | resolved_indep=60/50 | 53W-7L | pnl=-30.73 | Wilson 77.8% vs BE 93.5% | gap=-15.6pp | candidates=167 fills=68 fill_rate=40.7% pending_units=8 toxic=7 | blockers=pnl<=0; wilson<=BE; toxic>0
- rank 8: sports NO maker_band=<85 | gate=NO_GO_REVIEW | resolved_indep=157/50 | 115W-42L | pnl=-143.82 | Wilson 65.8% vs BE 82.4% | gap=-16.6pp | candidates=1300 fills=268 fill_rate=20.6% pending_units=111 toxic=42 | blockers=pnl<=0; wilson<=BE; toxic>0

## Kalshi Maker Walk-Forward Validation
- command: `python3 scripts/kalshi_maker_walkforward.py --limit 8`
- status: NO_MAKER_WALKFORWARD_CUT | ready=false | observations=1904 | cuts=187 | display_cuts=122 | validated_cuts=0 | ready_cuts=0 | split_cutoff=2026-06-28T18:17:15+00:00 | min_train=30 | min_validation=15 | edge_buffer=+2.0pp | scope=posthoc_maker_cut_walkforward_requires_predeclared_live_spec
- best: maker_all_fills|category=crypto|side_bid_band=90-92 | gate=MAKER_WALKFORWARD_REJECT | type=pair | train=17 resolved 13W-4L -$27.83 toxic=4 Wilson 52.7% vs target 94.8% gap=-42.1pp | validation=28 resolved 28W-0L +$19.87 toxic=0 Wilson 87.9% vs target 94.9% gap=-7.0pp | blockers=train_resolved<30;train_pnl<=0;train_toxic>0;train_wilson<BE+buffer;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXETHD-26JUL0417-T1779.99 status=active due=2026-07-04T21:00:00+00:00 price=0.92
- rank 1: maker_all_fills|category=crypto|side_bid_band=90-92 | gate=MAKER_WALKFORWARD_REJECT | type=pair | train=17 resolved 13W-4L -$27.83 toxic=4 Wilson 52.7% vs target 94.8% gap=-42.1pp | validation=28 resolved 28W-0L +$19.87 toxic=0 Wilson 87.9% vs target 94.9% gap=-7.0pp | blockers=train_resolved<30;train_pnl<=0;train_toxic>0;train_wilson<BE+buffer;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXETHD-26JUL0417-T1779.99 status=active due=2026-07-04T21:00:00+00:00 price=0.92
- rank 2: maker_all_fills|category=crypto|spread_band=<=2c | gate=MAKER_WALKFORWARD_REJECT | type=pair | train=57 resolved 50W-7L -$4.41 toxic=7 Wilson 76.8% vs target 90.5% gap=-13.7pp | validation=102 resolved 93W-9L +$21.06 toxic=9 Wilson 84.1% vs target 91.1% gap=-7.0pp | blockers=train_pnl<=0;train_toxic>0;train_wilson<BE+buffer;validation_toxic>0;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXBTCD-26JUL0417-T61749.99 status=active due=2026-07-04T21:00:00+00:00 price=0.87
- rank 3: maker_all_fills|spread_band=<=2c | gate=MAKER_WALKFORWARD_REJECT | type=single | train=175 resolved 146W-29L -$88.26 toxic=29 Wilson 77.2% vs target 90.5% gap=-13.3pp | validation=163 resolved 146W-17L +$6.64 toxic=17 Wilson 83.9% vs target 91.1% gap=-7.2pp | blockers=train_pnl<=0;train_toxic>0;train_wilson<BE+buffer;validation_toxic>0;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXMLBSPREAD-26JUN301940CINMIL-MIL5 status=active due=2026-07-03T23:40:00+00:00 price=0.81
- rank 4: maker_all_fills|side_bid_band=90-92 | gate=MAKER_WALKFORWARD_REJECT | type=single | train=41 resolved 36W-5L -$20.97 toxic=5 Wilson 74.5% vs target 94.9% gap=-20.4pp | validation=49 resolved 46W-3L +$5.15 toxic=3 Wilson 83.5% vs target 94.8% gap=-11.3pp | blockers=train_pnl<=0;train_toxic>0;train_wilson<BE+buffer;validation_toxic>0;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXMLBSPREAD-26JUN302010MINHOU-HOU6 status=active due=2026-07-04T00:10:00+00:00 price=0.94
- rank 5: maker_all_fills|side_ask_band=90-92 | gate=MAKER_WALKFORWARD_REJECT | type=single | train=81 resolved 56W-25L -$170.66 toxic=25 Wilson 58.4% vs target 92.2% gap=-33.8pp | validation=54 resolved 49W-5L +$3.08 toxic=5 Wilson 80.1% vs target 92.1% gap=-12.1pp | blockers=train_pnl<=0;train_toxic>0;train_wilson<BE+buffer;validation_toxic>0;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXMLBSPREAD-26JUN301940TBKC-TB9 status=active due=2026-07-03T23:40:00+00:00 price=0.90
- rank 6: maker_all_fills|due_hour=18Z | gate=MAKER_WALKFORWARD_REJECT | type=single | train=28 resolved 16W-12L -$90.27 toxic=12 Wilson 39.1% vs target 91.4% gap=-52.3pp | validation=21 resolved 20W-1L +$16.06 toxic=1 Wilson 77.3% vs target 89.6% gap=-12.3pp | blockers=train_resolved<30;train_pnl<=0;train_toxic>0;train_wilson<BE+buffer;validation_toxic>0;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXMLBSPREAD-26JUL011420SDCHC-CHC10 status=active due=2026-07-04T18:20:00+00:00 price=0.84
- rank 7: maker_all_fills|side_bid_band=80-85 | gate=MAKER_WALKFORWARD_REJECT | type=single | train=106 resolved 85W-21L -$61.33 toxic=21 Wilson 71.6% vs target 88.0% gap=-16.4pp | validation=106 resolved 89W-17L -$27.48 toxic=17 Wilson 75.8% vs target 88.5% gap=-12.7pp | blockers=train_pnl<=0;train_toxic>0;train_wilson<BE+buffer;validation_pnl<=0;validation_toxic>0;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXMLBSPREAD-26JUN301940CINMIL-CIN4 status=active due=2026-07-03T23:40:00+00:00 price=0.87
- rank 8: maker_all_fills|side=YES|side_bid_band=80-85 | gate=MAKER_WALKFORWARD_REJECT | type=pair | train=29 resolved 26W-3L +$11.41 toxic=3 Wilson 73.6% vs target 87.7% gap=-14.1pp | validation=41 resolved 36W-5L +$10.10 toxic=5 Wilson 74.5% vs target 87.3% gap=-12.9pp | blockers=train_resolved<30;train_toxic>0;train_wilson<BE+buffer;validation_toxic>0;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXMLBSPREAD-26JUN301940TBKC-TB5 status=active due=2026-07-03T23:40:00+00:00 price=0.86

## Kalshi Bid-Side Maker Shadow
- command: `python3 scripts/kalshi_bid_side_maker_shadow.py --report`
- Kalshi legacy bid-side maker shadow
-   Cohort: legacy_bid_side_maker_shadow_bid_plus_1_600s_2026_06_28
-   Mode: observation_only bid+1 maker simulation; no live orders
-   Status: ACCUMULATING | candidates=335 fills=15 cancels=280 open=40 pending_fills=15 independent_resolved=0/50 0W-0L pnl=+0.00 wilson=0.0% breakeven=100.0% toxic=0
-   Cell index KXNASDAQ100 NO: candidates=71 fills=4 pending=4 resolved=0 0W-0L pnl=+0.00 wilson=0.0% breakeven=100.0% toxic=0 gate=ACCUMULATING next_close=2026-06-29T20:00:00+00:00
-   Cell fx KXEURUSD NO: candidates=56 fills=0 pending=0 resolved=0 0W-0L pnl=+0.00 wilson=0.0% breakeven=100.0% toxic=0 gate=ACCUMULATING next_close=none
-   Cell fx KXUSDJPY NO: candidates=34 fills=0 pending=0 resolved=0 0W-0L pnl=+0.00 wilson=0.0% breakeven=100.0% toxic=0 gate=ACCUMULATING next_close=none
-   Cell index KXINX NO: candidates=34 fills=2 pending=2 resolved=0 0W-0L pnl=+0.00 wilson=0.0% breakeven=100.0% toxic=0 gate=ACCUMULATING next_close=2026-06-29T20:00:00+00:00
-   Cell weather KXLOWTAUS NO: candidates=13 fills=0 pending=0 resolved=0 0W-0L pnl=+0.00 wilson=0.0% breakeven=100.0% toxic=0 gate=ACCUMULATING next_close=none
-   Cell weather KXLOWTPHIL NO: candidates=13 fills=0 pending=0 resolved=0 0W-0L pnl=+0.00 wilson=0.0% breakeven=100.0% toxic=0 gate=ACCUMULATING next_close=none
-   Cell weather KXHIGHTDAL NO: candidates=12 fills=1 pending=1 resolved=0 0W-0L pnl=+0.00 wilson=0.0% breakeven=100.0% toxic=0 gate=ACCUMULATING next_close=2026-06-30T06:00:00+00:00
-   Cell weather KXHIGHTHOU NO: candidates=12 fills=0 pending=0 resolved=0 0W-0L pnl=+0.00 wilson=0.0% breakeven=100.0% toxic=0 gate=ACCUMULATING next_close=none

## Kalshi Forward Pending Maturity Queue
- command: `python3 scripts/kalshi_native_forward_leaderboard.py --json` + `python3 scripts/kalshi_maker_forward_leaderboard.py --json`
- status: native=NO_LIVE_READY pending=22 active=22 stale=0 unknown=0 | maker=NO_LIVE_READY pending_units=504 active=504 stale=0 unknown=0 | queued=17
- 1. maker:cell_sports_no | ticker=KXMLBSPREAD-26JUN301907NYMTOR-NYM4 | status=active | time=2026-07-03T23:07:00+00:00 | resolved_indep=413 pending_units=293
- 2. maker:cell_sports_yes | ticker=KXMLBSPREAD-26JUN301910WSHBOS-WSH6 | status=active | time=2026-07-03T23:10:00+00:00 | resolved_indep=124 pending_units=132
- 3. maker:cell_weather_no | ticker=KXHIGHMIA-26JUL03-B88.5 | status=active | time=2026-07-04T04:59:00+00:00 | resolved_indep=110 pending_units=27
- 4. maker:cell_weather_yes | ticker=KXHIGHMIA-26JUL03-B90.5 | status=active | time=2026-07-04T04:59:00+00:00 | resolved_indep=26 pending_units=3
- 5. maker:watch_weather_no_ge88 | ticker=KXHIGHMIA-26JUL03-B88.5 | status=active | time=2026-07-04T04:59:00+00:00 | resolved_indep=30 pending_units=6
- 6. native:weather_no_candidate:no_95_98_zero_loss_cities_v1 | ticker=KXHIGHMIA-26JUL03-B88.5 | status=active | time=2026-07-04T14:00:00+00:00 | resolved=58 pending=13
- 7. native:weather_yes_90_93:yes_90_93_above_live_threshold_v1 | ticker=KXHIGHPHIL-26JUL03-B101.5 | status=active | time=2026-07-04T14:00:00+00:00 | resolved=19 pending=3
- 8. native:weather_high_ask_no | ticker=KXLOWTNYC-26JUL03-T77 | status=active | time=2026-07-04T19:00:00+00:00 | resolved=45 pending=3
- 9. native:weather_no_candidate:no_90_95_min_probe_v1 | ticker=KXHIGHTMIN-26JUL03-B87.5 | status=active | time=2026-07-04T19:00:00+00:00 | resolved=8 pending=2
- 10. native:crypto_favorite_taker:crypto_near_certain_95_99_12_24h | ticker=KXBTCD-26JUL0417-T64499.99 | status=active | time=2026-07-04T20:59:59.946773+00:00 | resolved=39 pending=1

## Kalshi Academic-Prior Aligned Queue
- command: `python3 scripts/kalshi_academic_prior_queue.py --report --per-family 2`
- KALSHI ACADEMIC-PRIOR ALIGNED QUEUE
- generated_at=2026-07-03T23:05:41.950912+00:00 db=/home/eric-king/kalshi_favorites_bot/trades.db
- Lower rank_score means closer to review, not approval.
- 1. high_price_native_taker:crypto_last_hour_longshot_no | status=NATIVE_FORWARD_ACCUMULATING rank=0.0677 | 332 resolved 298W-34L -$3.44 | Wilson 86.0% vs target 92.8% | blockers=pnl<=0, wilson<BE+2pp | next=wait for native-actionable forward rows to resolve; no live order until target clears
- 2. high_price_native_taker:weather_no_candidate:no_95_98_zero_loss_cities_v1 | status=NATIVE_FORWARD_ACCUMULATING rank=0.1128 | 58 resolved 56W-2L -$0.56 | Wilson 88.3% vs target 99.5% | next=KXHIGHMIA-26JUL03-B88.5 active due=2026-07-04T14:00:00+00:00 | blockers=pnl<=0, wilson<BE+2pp | next=wait for native-actionable forward rows to resolve; no live order until target clears
- 3. source_shadow_requires_native:shadow_longshot_fading:crypto:NO:moderate:80-90:<1h | status=SHADOW_STABILITY_REJECT rank=0.2500 | 599 events 554W-45L +$2501.87 | Wilson 90.1% vs target 89.5% | stability_validation=180ev 166W-14L +$722.72 Wilson 87.4% vs target 89.4% | blockers=source_only_requires_native_forward_gate, shadow_stability_reject, validation_wilson<avg_price+buffer, asset_slice_wilson<avg_price:KXSOLD, utc_hour_slice_pnl<=0:15Z, utc_hour_slice_wilson<avg_price:15Z | next=only promote if a matching native first-actionable gate clears after fees and depth
- 4. source_shadow_requires_native:shadow_longshot_fading:other:NO:weak:80-90:4-24h | status=SHADOW_STABILITY_REJECT rank=0.2500 | 55 events 54W-1L +$771.83 | Wilson 90.4% vs target 85.3% | stability_validation=17ev 17W-0L +$284.09 Wilson 81.6% vs target 84.4% | blockers=source_only_requires_native_forward_gate, shadow_stability_reject, validation_wilson<avg_price+buffer | next=only promote if a matching native first-actionable gate clears after fees and depth
- 5. maker_adverse_selection:cell_sports_no | status=NO_GO_REVIEW rank=0.6484 | 413 independent resolved 318W-95L -$435.44 | Wilson 72.7% vs BE 87.5% | toxic=95 fill_rate=28.5% | blockers=pnl<=0, wilson<=BE, toxic>0 | next=continue shadow fill/toxicity measurement; no maker pilot with toxic or Wilson blockers
- 6. maker_adverse_selection:cell_crypto_yes | status=NO_GO_REVIEW rank=0.8680 | 320 independent resolved 176W-144L -$1002.41 | Wilson 49.5% vs BE 86.3% | toxic=144 fill_rate=29.0% | blockers=pnl<=0, wilson<=BE, toxic>0 | next=continue shadow fill/toxicity measurement; no maker pilot with toxic or Wilson blockers
- 7. structural_arbitrage:same_strike_last_24h | status=WATCH_ONLY rank=1.0000 | 43693 observations | fresh_pairs=43355 execution_ready_tier=5337 gross_positive=1 execution_ready_gross_positive=0 qty10_positive=1 execution_ready_qty10_positive=0 best_gross_edge=0.01 | blockers=no_execution_ready_gross_positive, no_execution_ready_fee_net_qty10_positive | next=continue simultaneous quote scans; only trade fee-net positive executable dislocations

## Kalshi Shadow Longshot Fading Resolver
- timer: kalshi-shadow-longshot-fading-backfill.timer active/enabled | service=kalshi-shadow-longshot-fading-backfill.service
- recent_36h_backlog: unresolved=219 | expired_after_60s_grace=4 | oldest_expired=2026-07-02 13:59:59 | oldest_expected=2026-07-02 13:59:59
- recent_36h_crypto_backlog: unresolved=126 | expired_after_60s_grace=0 | oldest_expired=none | oldest_expected=2026-07-03 23:59:59
- native_gate_stale_unresolved=0
- resolved_last_30m=128
- all_expired_backlog: unresolved=6526 | crypto=6171 | other=352 | weather=3 | oldest_expired=2026-04-15 21:59:59 | newest_expired=2026-07-02 16:59:59
- legacy_pre36h_expired_backlog: unresolved=6522 | crypto=6171 | other=348 | weather=3 | oldest_expired=2026-04-15 21:59:59 | newest_expired=2026-07-02 16:59:59
- scope: evidence-only resolver; no order placement path; timer category=crypto lookback=36h; prioritizes stale native-gate rows

## Kalshi Shadow Forecast Accuracy Resolver
- timer: kalshi-shadow-forecast-accuracy-backfill.timer active/enabled | service=kalshi-shadow-forecast-accuracy-backfill.service
- recent_72h_backlog: unresolved=320 | expired_after_60s_grace=0 | oldest_expired=none | oldest_expected=2026-07-04 04:58:59
- native_weather_gate_stale_unresolved=0 | next_due=2026-07-04T14:00:00+00:00
- scope: evidence-only resolver; no order placement path; lookback=72h; resolves binary/scalar public Kalshi outcomes

## Broad Favorite-Longshot Maker Edge
- command: `python3 scripts/favorite_longshot_maker_edge.py --report`
- FAVORITE-LONGSHOT MAKER EDGE
-   Cohort: fx_y_forward_only_2026_06_23 | start=2026-06-23T03:11:18+00:00 | source=gemini_maker_fp_only | mode=SHADOW_ONLY_NO_PLACEMENT
-   Verdict: NO-GO_EXECUTABLE_EDGE | all observed bands have fill rate <5%; toxic fills dominate 9/9 mature bands; no live capital.
-   5-10c: candidates=62525 fill=0.2% resolved=31 benign/toxic=9/22 net=$-13.96 benign=$+7.48 Wilson=70.1% BE=0.0% margin=+70.1pp | NO-GO_FILL_RATE+TOXIC_DOMINANT+NONPOSITIVE_NET_PNL
-   10-20c: candidates=58574 fill=0.4% resolved=47 benign/toxic=15/32 net=$-16.67 benign=$+44.57 Wilson=79.6% BE=0.0% margin=+79.6pp | NO-GO_FILL_RATE+TOXIC_DOMINANT+NONPOSITIVE_NET_PNL
-   20-35c: candidates=58854 fill=0.6% resolved=59 benign/toxic=21/38 net=$-17.84 benign=$+64.14 Wilson=84.5% BE=0.0% margin=+84.5pp | NO-GO_FILL_RATE+TOXIC_DOMINANT+NONPOSITIVE_NET_PNL
-   35-50c: candidates=36159 fill=0.6% resolved=41 benign/toxic=15/26 net=$+22.03 benign=$+65.98 Wilson=79.6% BE=0.0% margin=+79.6pp | NO-GO_FILL_RATE+TOXIC_DOMINANT
-   50-65c: candidates=35930 fill=0.8% resolved=41 benign/toxic=12/29 net=$-42.10 benign=$+50.56 Wilson=75.7% BE=0.0% margin=+75.7pp | NO-GO_FILL_RATE+TOXIC_DOMINANT+NONPOSITIVE_NET_PNL
-   65-80c: candidates=30974 fill=0.7% resolved=51 benign/toxic=15/36 net=$-6.55 benign=$+68.80 Wilson=79.6% BE=0.0% margin=+79.6pp | NO-GO_FILL_RATE+TOXIC_DOMINANT+NONPOSITIVE_NET_PNL
-   80-90c: candidates=29147 fill=0.7% resolved=58 benign/toxic=15/43 net=$+13.69 benign=$+35.81 Wilson=79.6% BE=0.0% margin=+79.6pp | NO-GO_FILL_RATE+TOXIC_DOMINANT
-   90-95c: candidates=17208 fill=0.5% resolved=36 benign/toxic=11/25 net=$-16.37 benign=$+10.53 Wilson=74.1% BE=0.0% margin=+74.1pp | NO-GO_FILL_RATE+TOXIC_DOMINANT+NONPOSITIVE_NET_PNL
-   95-99c: candidates=35736 fill=0.2% resolved=40 benign/toxic=7/33 net=$+0.30 benign=$+2.55 Wilson=64.6% BE=0.0% margin=+64.6pp | NO-GO_FILL_RATE+TOXIC_DOMINANT

## Timers
```
NEXT                                  LEFT LAST                              PASSED UNIT                                                   ACTIVATES
Fri 2026-07-03 18:06:00 CDT            15s Fri 2026-07-03 18:05:00 CDT      44s ago cushion-ds-multi-series-scanner.timer                  cushion-ds-multi-series-scanner.service
Fri 2026-07-03 18:06:00 CDT            15s Fri 2026-07-03 18:05:30 CDT      14s ago gemini-cushion-ds-scanner.timer                        gemini-cushion-ds-scanner.service
Fri 2026-07-03 18:06:02 CDT            17s Fri 2026-07-03 18:00:55 CDT 4min 48s ago kalshi-shadow-longshot-fading-backfill.timer           kalshi-shadow-longshot-fading-backfill.service
Fri 2026-07-03 18:06:06 CDT            21s Fri 2026-07-03 18:01:06 CDT 4min 38s ago kalshi-shadow-forecast-accuracy-backfill.timer         kalshi-shadow-forecast-accuracy-backfill.service
Fri 2026-07-03 18:06:06 CDT            22s Fri 2026-07-03 18:05:33 CDT      11s ago kalshi-worldcup-score-state-live-pilot.timer           kalshi-worldcup-score-state-live-pilot.service
Fri 2026-07-03 18:06:14 CDT            30s Fri 2026-07-03 18:05:14 CDT      29s ago gateway-watchdog.timer                                 gateway-watchdog.service
Fri 2026-07-03 18:06:14 CDT            30s Fri 2026-07-03 18:05:14 CDT      29s ago goal-loop-watchdog.timer                               goal-loop-watchdog.service
Fri 2026-07-03 18:06:19 CDT            34s Fri 2026-07-03 17:56:18 CDT     9min ago ds-shadow-continuous-archive.timer                     ds-shadow-continuous-archive.service
Fri 2026-07-03 18:06:20 CDT            35s Fri 2026-07-03 18:05:20 CDT      24s ago gemini-ds-index-parity.timer                           gemini-ds-index-parity.service
Fri 2026-07-03 18:06:20 CDT            36s Fri 2026-07-03 18:05:16 CDT      28s ago kalshi-worldcup-final-state-live-pilot.timer           kalshi-worldcup-final-state-live-pilot.service
Fri 2026-07-03 18:06:32 CDT            47s Fri 2026-07-03 18:01:32 CDT 4min 12s ago kalshi-side-equivalence-scanner.timer                  kalshi-side-equivalence-scanner.service
Fri 2026-07-03 18:06:32 CDT            47s Fri 2026-07-03 18:01:32 CDT 4min 12s ago kalshi-weather-no-candidate-preflight.timer            kalshi-weather-no-candidate-preflight.service
Fri 2026-07-03 18:06:49 CDT        1min 5s Fri 2026-07-03 18:01:41 CDT  4min 3s ago kalshi-moderate-favorites-eth-yes-preflight.timer      kalshi-moderate-favorites-eth-yes-preflight.service
Fri 2026-07-03 18:07:00 CDT       1min 15s Fri 2026-07-03 18:02:00 CDT 3min 44s ago claude-crossing-no-v3.timer                            claude-crossing-no-v3.service
Fri 2026-07-03 18:07:08 CDT       1min 24s Fri 2026-07-03 18:03:52 CDT 1min 52s ago kalshi-sports-final-state-live-pilot.timer             kalshi-sports-final-state-live-pilot.service
Fri 2026-07-03 18:07:36 CDT       1min 51s Fri 2026-07-03 18:02:36 CDT  3min 8s ago btc-moderate-v2-shadow-scanner.timer                   btc-moderate-v2-shadow-scanner.service
Fri 2026-07-03 18:07:36 CDT       1min 51s Fri 2026-07-03 18:02:36 CDT  3min 8s ago gemini-fp-orderbook-capture.timer                      gemini-fp-orderbook-capture.service
Fri 2026-07-03 18:07:36 CDT       1min 51s Fri 2026-07-03 18:02:36 CDT  3min 8s ago gemini-reward-post-only-safety.timer                   gemini-reward-post-only-safety.service
Fri 2026-07-03 18:08:28 CDT       2min 44s Fri 2026-07-03 18:03:25 CDT 2min 19s ago kalshi-shadow-deterministic-settlement-backfill.timer  kalshi-shadow-deterministic-settlement-backfill.service
Fri 2026-07-03 18:08:34 CDT       2min 50s Fri 2026-07-03 18:03:25 CDT 2min 18s ago gemini-reward-live-readiness.timer                     gemini-reward-live-readiness.service
Fri 2026-07-03 18:08:35 CDT       2min 50s Fri 2026-07-03 18:03:35 CDT  2min 9s ago gemini-maker-fill-simulator.timer                      gemini-maker-fill-simulator.service
Fri 2026-07-03 18:09:55 CDT       4min 11s Fri 2026-07-03 18:04:53 CDT      51s ago kalshi-crypto-ladder-dislocation-preflight.timer       kalshi-crypto-ladder-dislocation-preflight.service
Fri 2026-07-03 18:10:00 CDT       4min 15s Fri 2026-07-03 12:10:00 CDT 5h 55min ago claude-chat-sync.timer                                 claude-chat-sync.service
Fri 2026-07-03 18:10:00 CDT       4min 15s Fri 2026-07-03 18:00:00 CDT     5min ago full-picture-latest-refresh.timer                      full-picture-latest-refresh.service
Fri 2026-07-03 18:10:11 CDT       4min 27s Fri 2026-07-03 18:05:09 CDT      34s ago kalshi-crypto-favorite-taker-preflight.timer           kalshi-crypto-favorite-taker-preflight.service
Fri 2026-07-03 18:10:32 CDT       4min 48s Fri 2026-07-03 18:05:25 CDT      19s ago kalshi-other-longshot-no-80-90-preflight.timer         kalshi-other-longshot-no-80-90-preflight.service
Fri 2026-07-03 18:10:33 CDT       4min 48s Fri 2026-07-03 18:05:29 CDT      14s ago kalshi-weather-high-ask-no-preflight.timer             kalshi-weather-high-ask-no-preflight.service
Fri 2026-07-03 18:10:36 CDT       4min 52s Fri 2026-07-03 18:05:34 CDT      10s ago kalshi-weather-yes-90-93-preflight.timer               kalshi-weather-yes-90-93-preflight.service
Fri 2026-07-03 18:10:46 CDT           5min Fri 2026-07-03 18:05:41 CDT       3s ago kalshi-crypto-last-hour-longshot-no-preflight.timer    kalshi-crypto-last-hour-longshot-no-preflight.service
Fri 2026-07-03 18:11:08 CDT           5min Fri 2026-07-03 17:56:08 CDT     9min ago gemini-ds-source-parity.timer                          gemini-ds-source-parity.service
Fri 2026-07-03 18:12:08 CDT           6min Fri 2026-07-03 17:57:08 CDT     8min ago ds-storage-pressure-monitor.timer                      ds-storage-pressure-monitor.service
Fri 2026-07-03 18:13:10 CDT           7min Fri 2026-07-03 17:58:10 CDT     7min ago kalshi-side-equivalence-resolver.timer                 kalshi-side-equivalence-resolver.service
Fri 2026-07-03 18:14:02 CDT           8min Fri 2026-07-03 17:44:02 CDT    21min ago ds-storage-monitor.timer                               ds-storage-monitor.service
Fri 2026-07-03 18:14:08 CDT           8min Fri 2026-07-03 17:59:08 CDT     6min ago btc-moderate-v2-shadow-resolver.timer                  btc-moderate-v2-shadow-resolver.service
Fri 2026-07-03 18:14:08 CDT           8min Fri 2026-07-03 17:59:08 CDT     6min ago gemini-categorical-scanner.timer                       gemini-categorical-scanner.service
Fri 2026-07-03 18:15:00 CDT           9min Fri 2026-07-03 18:00:00 CDT     5min ago cushion-ds-multi-series-resolver.timer                 cushion-ds-multi-series-resolver.service
Fri 2026-07-03 18:15:00 CDT           9min Fri 2026-07-03 18:00:00 CDT     5min ago gemini-cushion-ds-resolver.timer                       gemini-cushion-ds-resolver.service
Fri 2026-07-03 18:18:58 CDT          13min Fri 2026-07-03 15:18:58 CDT 2h 46min ago db-auto-vacuum.timer                                   db-auto-vacuum.service
Fri 2026-07-03 18:18:58 CDT          13min Fri 2026-07-03 17:18:58 CDT    46min ago gemini-db-retention.timer                              gemini-db-retention.service
Fri 2026-07-03 18:19:03 CDT          13min Fri 2026-07-03 17:49:03 CDT    16min ago eth-ds-fg-filter-blocks-resolver.timer                 eth-ds-fg-filter-blocks-resolver.service
Fri 2026-07-03 18:19:10 CDT          13min Fri 2026-07-03 18:04:10 CDT 1min 34s ago gemini-categorical-resolver.timer                      gemini-categorical-resolver.service
Fri 2026-07-03 18:24:00 CDT          18min Fri 2026-07-03 17:54:00 CDT    11min ago gemini-db-size-monitor.timer                           gemini-db-size-monitor.service
Fri 2026-07-03 18:29:39 CDT          23min Fri 2026-07-03 17:29:09 CDT    36min ago ladder-coherence-two-leg-resolver.timer                ladder-coherence-two-leg-resolver.service
Fri 2026-07-03 18:30:00 CDT          24min Fri 2026-07-03 17:30:00 CDT    35min ago gemini-direct-index-ds-first-resolution-verifier.timer gemini-direct-index-ds-first-resolution-verifier.service
Fri 2026-07-03 18:34:58 CDT          29min Fri 2026-07-03 17:34:00 CDT    31min ago macro-release-resolver.timer                           macro-release-resolver.service
Fri 2026-07-03 19:17:00 CDT       1h 11min Fri 2026-07-03 13:17:00 CDT 4h 48min ago ds-shadow-retention-engine.timer                       ds-shadow-retention-engine.service
Fri 2026-07-03 21:18:56 CDT       3h 13min Fri 2026-07-03 15:18:56 CDT 2h 46min ago ds-shadow-db-maintenance.timer                         ds-shadow-db-maintenance.service
Fri 2026-07-03 21:24:20 CDT       3h 18min Fri 2026-07-03 15:24:20 CDT 2h 41min ago ds-shadow-archive.timer                                ds-shadow-archive.service
Sat 2026-07-04 03:15:00 CDT             9h Fri 2026-07-03 03:15:00 CDT            - shadow-verification.timer                              shadow-verification.service
Sat 2026-07-04 03:30:00 CDT             9h Fri 2026-07-03 03:30:00 CDT            - ibkr-independent-verification.timer                    ibkr-independent-verification.service
Sat 2026-07-04 04:13:00 CDT            10h Fri 2026-07-03 16:13:00 CDT 1h 52min ago claude-calibration-logger.timer                        claude-calibration-logger.service
Sat 2026-07-04 04:30:00 CDT            10h Fri 2026-07-03 04:30:00 CDT            - tax-ledger-ingest.timer                                tax-ledger-ingest.service
Sat 2026-07-04 04:46:58 CDT            10h Fri 2026-07-03 04:46:50 CDT            - ds-archive-tier-rotation.timer                         ds-archive-tier-rotation.service
Sat 2026-07-04 05:20:00 CDT            11h Fri 2026-07-03 05:20:01 CDT            - logrotate-user.timer                                   logrotate-user.service
Sat 2026-07-04 05:30:00 CDT            11h Fri 2026-07-03 05:30:01 CDT            - disk-hygiene-audit.timer                               disk-hygiene-audit.service
Sat 2026-07-04 05:30:00 CDT            11h Fri 2026-07-03 05:30:01 CDT            - full-picture-daily-save.timer                          full-picture-daily-save.service
Sat 2026-07-04 05:40:00 CDT            11h Fri 2026-07-03 05:40:00 CDT            - database-autonomous-maintenance.timer                  database-autonomous-maintenance.service
Sat 2026-07-04 06:40:00 CDT            12h -                                      - ibkr-deterministic-fx-poc.timer                        ibkr-deterministic-fx-poc.service
Sat 2026-07-04 09:14:12 CDT            15h Fri 2026-07-03 09:14:12 CDT       8h ago launchpadlib-cache-clean.timer                         launchpadlib-cache-clean.service
Sat 2026-07-04 09:18:56 CDT            15h Fri 2026-07-03 09:18:56 CDT       8h ago gemini-fp-retention.timer                              gemini-fp-retention.service
Sun 2026-07-05 02:00:00 CDT       1 day 7h Sun 2026-06-28 02:00:00 CDT            - gemini-archive-compression.timer                       gemini-archive-compression.service
Fri 2026-07-10 09:16:55 CDT         6 days Fri 2026-07-03 09:16:55 CDT       8h ago ubuntu-insights-upload.timer                           ubuntu-insights-upload.service
Sun 2026-08-02 19:43:55 CDT 4 weeks 2 days Fri 2026-07-03 09:13:55 CDT       8h ago ubuntu-insights-collect.timer                          ubuntu-insights-collect.service
-                                        - Fri 2026-07-03 18:05:36 CDT       8s ago gemini-ds-index-micro-parity.timer                     gemini-ds-index-micro-parity.service
-                                        - Fri 2026-07-03 18:05:35 CDT       9s ago gemini-liquidity-rewards-scanner.timer                 gemini-liquidity-rewards-scanner.service
-                                        - Fri 2026-07-03 18:04:30 CDT 1min 14s ago gemini-reward-account-monitor.timer                    gemini-reward-account-monitor.service
-                                        - Fri 2026-07-03 18:02:32 CDT 3min 11s ago gemini-reward-inventory-exit.timer                     gemini-reward-inventory-exit.service
-                                        - Fri 2026-07-03 18:01:46 CDT 3min 58s ago gemini-reward-quote-pilot.timer                        gemini-reward-quote-pilot.service
-                                        - Fri 2026-07-03 18:05:36 CDT       8s ago gemini-trade-print-capture.timer                       gemini-trade-print-capture.service
-                                        - Fri 2026-07-03 18:05:37 CDT       7s ago kalshi-mve-component-result-live-pilot.timer           kalshi-mve-component-result-live-pilot.service
-                                        - Fri 2026-07-03 15:00:00 CDT  3h 5min ago snap.firmware-updater.firmware-notifier.timer          snap.firmware-updater.firmware-notifier.service

71 timers listed.
```

## Repo State
- gemini: head=fd8d19d branch=master in_sync=true remote=https://github.com/PhotonRahm/gemini_prediction_bot.git dirty=yes
- ibkr: head=3a580e4 branch=master in_sync=true remote=https://github.com/PhotonRahm/ibkr_forecast_bot.git dirty=yes
- kalshi: head=99546b4 branch=master in_sync=true remote=https://github.com/PhotonRahm/kalshi_favorites_bot.git dirty=yes
- operations-knowledge: head=eba3a6a branch=master in_sync=true remote=https://github.com/PhotonRahm/operations-knowledge.git dirty=yes
- workspace: head=0710930 branch=master in_sync=true remote=https://github.com/PhotonRahm/rahm-workspace.git dirty=yes

## Active User Services
```
at-spi-dbus-bus.service
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
gvfs-afc-volume-monitor.service
gvfs-daemon.service
gvfs-goa-volume-monitor.service
gvfs-gphoto2-volume-monitor.service
gvfs-metadata.service
gvfs-mtp-volume-monitor.service
gvfs-udisks2-volume-monitor.service
kalshi-bot.service
kalshi-high-price-maker-cancel-shadow.service
kalshi-same-strike-complementarity-scanner.service
ladder-coherence-two-leg-scanner.service
localsearch-3.service
mpris-proxy.service
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
org.gnome.SettingsDaemon.UsbProtection.service
org.gnome.SettingsDaemon.Wwan.service
org.gnome.SettingsDaemon.XSettings.service
org.gnome.Shell@ubuntu.service
pipewire-pulse.service
pipewire.service
sports-ds-forward-scanner.service
ssh-agent.service
wireplumber.service
xdg-desktop-portal-gnome.service
xdg-desktop-portal-gtk.service
xdg-desktop-portal.service
xdg-document-portal.service
xdg-permission-store.service
```

## Today's Research Files (2026-07-03 America/Chicago)
- research/2026-07-03-claude-crossing-no-v3-day1-zero-fills-v33-latency-amendment.md
- research/2026-07-03-fx-ka-kalshi-live-slot-whole-universe-source-refresh-no-go.md
- research/2026-07-03-fx-kb-kalshi-btc-last-hour-live-pilot.md
- research/2026-07-03-fx-kc-kalshi-btc-monitor-universe-no-go.md
- research/2026-07-03-fx-kd-kalshi-btc-loss-post-expiration-no-go.md
- research/2026-07-03-fx-ke-kalshi-live-wrapper-cap-alignment.md
- research/2026-07-03-fx-kf-kalshi-sports-final-state-index-backed-wrapper.md
- research/2026-07-03-fx-kg-kalshi-worldcup-score-state-timeout-hardening.md
- research/2026-07-03-fx-kh-kalshi-worldcup-score-state-market-cache-fallback.md
- research/2026-07-03-fx-ki-kalshi-mve-component-event-cache-and-source-refresh.md
- research/2026-07-03-fx-kj-kalshi-mve-refresh-timeout-hardening.md
- research/2026-07-03-fx-kk-kalshi-crypto-pilot-stale-candidate-guard.md
- research/2026-07-03-fx-kl-kalshi-weather-chi-resolution-and-no-go-refresh.md
- research/2026-07-03-fx-km-kalshi-post-weather-loss-broad-refresh-no-go.md
- research/2026-07-03-fx-kn-kalshi-structural-scanner-sweep-no-go.md
- research/2026-07-03-fx-ko-kalshi-eth-yes-native-preflight-and-crypto-backfill-no-go.md
- research/2026-07-03-fx-kp-kalshi-source-state-refresh-and-corner-cache-hardening.md
- research/2026-07-03-fx-kq-kalshi-quote-structure-and-tennis-lock-refresh-no-go.md
- research/2026-07-03-fx-kr-kalshi-resolution-lag-and-crypto-boundary-no-go.md
- research/2026-07-03-fx-ks-kalshi-source-native-crypto-boundary-and-db-lock-hardening.md
- research/2026-07-03-fx-kt-kalshi-live-source-structural-crypto-boundary-no-go.md
- research/2026-07-03-fx-ku-kalshi-live-source-structural-crypto-21z-boundary-no-go.md
- research/2026-07-03-fx-kv-kalshi-post-22z-crypto-boundary-and-source-refresh-no-go.md

## Deferred And Pending Items
```
specific trigger condition. Once the trigger is in the past, the item is due and
should be handled in the next operational review.
## Pending
`89.0%` vs BE `93.0%`). No live pilot is justified; maker-forward reviews
remain trigger-based only. Evidence:
| Key | Verification | Why deferred | Trigger | Due |
| `fx_cs_kalshi_crypto_no_lt10c_non04z_review_ready_followup` | Kalshi crypto NO `<10c` non-04Z review-ready follow-up | CLOSED NO-GO 2026-06-25 18:15Z: follow-up found the statistical gate was not taker-executable. `shadow_deterministic_settlement.market_ask`/`market_bid` are side-specific to `predicted_side`, so the apparent DS `0.02` NO price came from the transform `1 - market_bid` on high-side NO rows, not from a source/native NO ask below `10c`. Reconciled native/source NO ask evidence is `0/174` broad and `0/116` fresh non-04Z below `10c`; both gates now render `NOT_READY` with reason `native taker NO ask <10c evidence absent`. The 18:00Z candidate `KXBTCD-26JUN2514-T60199.99` was not traded; tracking has one `BLOCKED` row, placed/cancelled live rows `0`, main strategy trades `0`. Wrote `KILL_KALSHI_CRYPTO_NO_LT10C_NON04Z_FIRST_ELIGIBLE_PILOT`, disabled the non-04Z pilot timer and first-live verifier timer, and verified manual `--execute` blocks on `fresh_non04z_gate_not_ready`, `fresh_non04z_status=NOT_READY`, `pilot_kill_switch_present`, and `no_live_candidate`. | CLOSED. Do not place under `kalshi_crypto_no_lt10c_non04z_first_eligible_forward_pilot`; do not revive the old broad identity. Future work in this family requires a separate native-taker forward gate built from actual source/native NO asks below `0.10`, not bid-inverted shadow prices. Keep `kalshi-shadow-deterministic-settlement-backfill.timer` only for no-order source/report hygiene. Evidence: `research/2026-06-25-fx-cs-kalshi-crypto-no-lt10c-non04z-review-ready.md`. | Completed 2026-06-25 |
| `fs_kalshi_index_fx_side_equivalence_first_30_native_resolved` | Kalshi Index/FX side-equivalence harness first-30 native-actionable resolved review | CLOSED FAILED 2026-06-24: trigger reached and failed decisively. Native-actionable first-symbol collapse: FX `3W-32L`, `-$204.41`, Wilson `3.0%` vs corrected BE `20.6%`; Index `6W-89L`, `-$143.01`, Wilson `2.9%` vs corrected BE `9.4%`. Raw native-actionable rows were also negative: FX `63W-1591L`, `-$11,305.82`; Index `659W-8531L`, `-$7,908.26`. Native NO availability and native-vs-reconstructed side-match were `100%`, so this is not a synthetic-NO artifact; it disproves the Index/FX favorite-tracking salvage idea under native executable quotes. | CLOSED. No pilot; do not revive old Index/FX DS or longshot labels from this evidence. The Kalshi status report now renders `KALSHI INDEX/FX SIDE-EQUIVALENCE FS SHADOW` as `REJECTED_NATIVE_CONTROL`. Evidence: `research/2026-06-24-fx-be-kalshi-index-fx-side-equivalence-gate.md`. | Completed 2026-06-24 |
| `fs_btc_moderate_v2_first_30_resolved` | BTC moderate v2 shadow first-30 resolved review | CLOSED FAILED 2026-06-28 10:25Z: trigger crossed and failed. Raw predicate is `31` resolved, `26W-5L`, `-$22.51`, avg win `$3.29`, avg loss `$21.61`, Wilson `67.4%` vs corrected BE `86.8%`; first-symbol is `22W-4L`, `-$13.49`, Wilson `66.5%` vs BE `86.7%`; first settlement-hour is `17W-4L`, `-$29.46`, Wilson `60.0%` vs BE `86.6%`. The old live BTC moderate pilot remains killed and this v2 shadow has no live authorization. | CLOSED. No live pilot, no revival of `bot_strategy_kalshi_ds_btc_moderate_favorite_yes_pilot`, and no new BTC moderate identity from this evidence. Evidence: `research/2026-06-24-fx-bf-kalshi-btc-moderate-v2-shadow-visibility.md`. | Completed 2026-06-28 |
| `fx_av_kalshi_crypto_no_lt10c_post_kill_50_resolved` | Kalshi crypto low-price NO `<10c` post-kill first-eligible review | CLOSED REVERSED 2026-06-25: the initial `50W-0L` review-ready state was invalidated when the remaining one-hour pending markets settled. Current post-kill first-eligible sample is `58` resolved, `52W-6L`, `+$49.50`, Wilson lower `79.2%`, below the `90.0%` gate; source reconciliation still checked `58/58` with `0` mismatches, so these are true losses rather than source defects. No live pilot row was placed. Wrote `/home/eric-king/kalshi_favorites_bot/KILL_KALSHI_CRYPTO_NO_LT10C_FIRST_ELIGIBLE_PILOT`. | CLOSED. Do not place under `kalshi_crypto_no_lt10c_first_eligible_pilot` or revive `ds_low_price_no` from this evidence. Any future crypto `<10c` NO work requires a fresh review and explicit unkill/new-identity decision. Evidence: `research/2026-06-25-fx-bq-kalshi-crypto-no-lt10c-gate-reversal.md`. | Completed 2026-06-25 |
| `fx_bk_kalshi_crypto_no_lt10c_first_live_row_verification` | Kalshi crypto NO `<10c` first live row verification | CLOSED NO_ROW 2026-06-25: no first live row ever existed (`tracking_rows=0`, `live_placed_rows=0`, main strategy trade rows `0`). After pending losses invalidated the gate, the pilot kill switch was written and the launcher preflight now blocks on `pilot_kill_switch_present` plus `gate_not_ready`. The verifier remains harmless but has no placed row to validate. | CLOSED. If this family is ever reconsidered, open a new verification item with a fresh strategy/review boundary rather than reusing this first-live-row trigger. | Completed 2026-06-25 |
| `fx_aw_kalshi_high_price_maker_cancel_first_50_resolved_cell` | Kalshi high-price maker/cancel first-50 independent resolved cell review | CLOSED NO-GO 2026-06-26 15:03Z: the first formal 50-independent-fill cell reached review and failed. Crypto NO is `50/50`, `32W-18L`, `-$122.28`, Wilson `50.1%` vs BE `88.5%`, toxic `19`, status `NO_GO_REVIEW`; aggregate maker/cancel is `185` independent resolved, `122W-63L`, `-$407.25`, Wilson `58.9%` vs BE `88.0%`, toxic `64`, status `NO_LIVE_READY`. Crypto YES is also negative at `45/50`, `27W-18L`, `-$125.52`; sports NO remains negative at `46/50`, `28W-18L`, `-$117.13`; watch `92-94c` is only `8W-0L`, `+$4.66`, Wilson `67.6%` vs BE `94.2%`. Evidence: `research/2026-06-25-fx-dc-kalshi-maker-cancel-subcell-sweep.md` and current-state `2026-06-26T15:04Z`. | CLOSED. No live maker pilot; do not auto-deploy this broad high-price maker/cancel hypothesis. Future maker work requires a materially different cell or separate existing verification item, with the same first-resolved independent-fill, fee-net P&L, Wilson-vs-breakeven, toxicity, fill/cancel, and TTL-late-cross review discipline. | Completed 2026-06-26 |
| `fx_cv_kalshi_broad_event_first_shadow_candidate_audit` | Kalshi broad event-first shadow candidate audit | FX-CV added `scripts/kalshi_shadow_event_first_audit.py` and a current-state section to scan favorites, forecast accuracy, longshot fading, deterministic settlement, and legacy taker-style surfaces (`shadow_taker`, `shadow_contrarian`, `shadow_mean_reversion`, `shadow_near_expiry_favorites`) with event-first collapse. Current expanded output after the 08:04Z refresh has `155` eligible cells and `4` shadow-only candidates: crypto last-hour weak `<1h` is `527W-64L`, Wilson `86.4%` vs target `84.6%`; crypto moderate `<1h` is `378W-29L`, Wilson `90.0%` vs target `89.6%`; `other` weak `4-24h` is `36W-1L`, Wilson `86.2%` vs target `85.8%`; and the old contrarian crypto fragment remains `19W-32L`. The controlling native crypto gate improved at 08:00Z but is still not live-ready: `28` resolved, `25W-3L`, `-$0.29`, Wilson `72.8%` vs BE `90.3%`, about `83` perfect wins from review. The `other` preflight logs both `other_weak_no_80_90_4_24h_v1` and watch-only `other_strong_no_90_95_4_24h_v1`; a 07:33Z stress test shows the weak candidate's all-period gap is only `+0.4pp`, while INDEX and FX splits fail independently. The 08:15Z fee-audit refresh found two actionable strong index rows, while the subsequent 08:19Z generated refresh had one actionable weak index row and strong rows out of band at native NO ask `0.99`; the native `other` gates remain pending-only with `0` resolved rows. | Treat `SHADOW_EVENT_FIRST_CANDIDATES` as a source-discovery signal only. When `other_longshot_no_80_90:other_weak_no_80_90_4_24h_v1`, `other_longshot_no_80_90:other_strong_no_90_95_4_24h_v1`, or any shadow candidate cell has >=30 fresh forward native-actionable resolved rows in the same execution regime, evaluate native fee-net W-L/P&L, Wilson lower vs native breakeven plus `2pp`, row/event independence, volume/depth/source hygiene, and concentration. Any pilot requires a new strategy identity, qty `1`, max-open `1`, current native ask/depth and fee-net economics; do not auto-deploy from shadow-only candidates. Evidence: `research/2026-06-25-fx-cv-kalshi-broad-event-first-shadow-audit.md` and `research/2026-06-25-fx-de-kalshi-other-longshot-strong-watch-and-04z-refresh.md`. | Trigger-based |
| `fx_cx_kalshi_weather_moderate_yes_50_60_forward_review` | Kalshi weather moderate YES 50-60 forward review | FX-CX audited the fresh `shadow_moderate_favorites` Weather HIGH YES 50-60c 4-24h cell under event-first collapse. All rows are barely positive after a `2pp` buffer (`85` resolved, `60W-25L`, `+$1,230.00`, avg entry `0.561`, Wilson `60.2%` vs target `58.1%`), and the stricter liquidity/spread-filtered slice is `62` resolved, `44W-18L`, `+$925.00`, avg entry `0.560`, Wilson `58.7%` vs target `58.0%`. Fresh-window evidence fails: since `2026-06-17`, the liquidity-filtered slice is `39W-18L`, Wilson `55.5%` vs target `58.0%`; since `2026-06-20`, it is `25W-13L`, Wilson `49.9%`. A one-off native recheck of `12` pending first-event rows at about `2026-06-26T00:40Z` found `0` still actionable in the original `0.50-0.60` YES band. This does not revive the permanently killed `moderate_favorites` strategy. | Starting at `2026-06-25T00:00:00Z`, when `shadow_moderate_favorites` has >=50 fresh resolved event-first rows with `category='WEATHER'`, `asset='WEATHER_HIGH'`, `hyp_side='YES'`, `0.50 <= entry_price < 0.60`, `expiry_band='4-24h'`, `passed_liquidity_filter=1`, and `spread_acceptable=1`, evaluate fee-net W-L/P&L, avg entry and modeled breakeven including fees, Wilson lower margin >=`2pp`, day/city/series concentration, current native YES ask/depth availability in the same `0.50-0.60` regime, and whether pending rows preserved the original entry regime. Any live pilot requires a new strategy identity, qty `1`, max-open `1`, current native YES ask/depth preflight, fee-net qty-1 economics, and first-live-row review before any second placement; do not revive `moderate_favorites`. Evidence: `research/2026-06-25-fx-cx-kalshi-weather-moderate-yes-50-60-forward-watch.md`. | Trigger-based |
| `fx_bp_kalshi_weather_high_ask_event_first_50_forward` | Kalshi weather high-ask event-first forward review | FX-BP found an exploratory ask-priced weather candidate in `shadow_forecast_accuracy`: event-collapsed `0.97 <= ask_price < 1.00` rows were `816W-5L`, `+$1,766.17`, Wilson `98.6%` vs corrected BE `97.3%`; June resolved rows were `164W-0L`. This is not live-deployable yet because the margin is thin, the predicate is exploratory, May has a data gap, and current candidates have not been mechanically checked against native orderbook depth. | Starting at `2026-06-25T06:15:00Z`, when `shadow_forecast_accuracy` has >=50 forward resolved event-first rows with `0.97 <= ask_price < 1.00`, collapse to one earliest eligible row per `series-date` event key and evaluate W-L, fee-net `pnl_at_ask`, corrected breakeven, Wilson lower, temporal stability, city/date loss concentration, and current native orderbook availability. Any live pilot requires a new strategy identity, qty `1`, max-open `1`, native ask/depth preflight, and first-live-row review before any second placement; do not auto-deploy from this backtest. | Trigger-based |
| `fx_br_kalshi_weather_no_high_ask_ex_lax_50_forward` | Kalshi weather high-ask NO ex-LAX forward review | FX-BR refined the FX-BP weather idea to the stronger ask-priced cell: event-first `side='no'`, `0.98 <= ask_price < 1.00`, excluding historical loss-concentrated `city='LAX'`, is now `721W-0L`, `+$1,887.94`, avg ask `0.986`, Wilson `99.5%` vs modeled ask/fee BE `98.8%` (thin margin). This remains shadow-only because the LAX exclusion is discovered in-sample, May has a data gap, and native taker availability is sparse. 2026-06-26 11:05Z refresh: first native outcomes scored as `3W-0L`, `+$0.03`, Wilson `43.8%` vs native BE `99.0%`; latest preflight checked `20` markets and found `0` latest actionable events; next pending first-actionable row is `KXLOWTCHI-26JUN25-B56.5`, NO ask `0.98`, qty-1 `+$0.01`/`-$0.99`, due `2026-06-26T19:00:00Z`. The native gate is still only `9` events, `3` resolved, `6` pending, far below the `50` resolved trigger; no live order placed. | Starting at `2026-06-25T06:30:00Z`, when `kalshi_weather_high_ask_no_preflight` has >=50 forward resolved event-first rows with `actionable_qty1=1` and `yes_depth >= qty`, join to `shadow_forecast_accuracy` by `source_shadow_id` and evaluate W-L, native fee-net P&L, corrected breakeven, Wilson lower margin >=`1pp`, month/day/city concentration, latest-actionability versus first-actionable gate evidence, and current native orderbook availability. Any live pilot requires a new strategy identity, qty `1`, max-open `1`, current native NO ask/depth preflight, fee-net qty-1 win > `$0` (normally native NO ask `<=0.98`), and first-live-row review before any second placement; do not auto-deploy from this backtest. Evidence: `research/2026-06-25-fx-br-kalshi-weather-high-ask-no-ex-lax-audit.md`. | Trigger-based |
| `fx_bs_kalshi_weather_no_candidate_cell_30_forward_native` | Kalshi weather NO candidate-cell native-actionable forward review | FX-BS found a lower-ask extension of the weather favorite/longshot idea where fee-net upside remains positive: `no_95_98_zero_loss_cities_v1` (`side='no'`, `0.95 <= ask_price < 0.98`, cities `AUS,DAL,LV,MIA,MIN,OKC,SEA`) is now event-first `258W-1L`, Wilson `97.8%` vs modeled BE `96.8%`; `no_90_95_min_probe_v1` (`MIN`, `0.90 <= ask_price < 0.95`) remains an underpowered probe. These remain in-sample city filters with the same May data gap: the broad all-city `0.95-0.98` NO control is only `750W-22L`, Wilson `95.7%` vs modeled BE `96.7%`, and the weakest selected city is `AUS 33W-1L`, Wilson `85.1%` vs BE `96.8%`. 2026-06-26 11:05Z refresh: the `no_95_98_zero_loss_cities_v1` native gate has `13` events, `6` resolved, `7` pending, `5W-1L`, `-$0.87`, Wilson `43.6%` vs native BE `97.6%`; `no_90_95_min_probe_v1` has `2` events, `1` resolved, `1` pending, `1W-0L`, `+$0.04`, Wilson `20.7%` vs BE `96.0%`. Latest preflight checked `8` markets and found `1` latest actionable OKC row at NO ask `0.98`; no live order placed. | Starting at `2026-06-25T07:05:00Z`, when any cohort in `kalshi_weather_no_candidate_preflight` has >=30 forward resolved native-actionable event-first rows with `actionable_qty1=1` and `yes_depth >= qty`, join to `shadow_forecast_accuracy` by `source_shadow_id` and evaluate actual native-entry W-L, fee-net P&L, corrected breakeven, Wilson lower margin >=`2pp`, and city/day/settlement-hour concentration. Any live pilot requires a new strategy identity, qty `1`, max-open `1`, current native NO ask/depth preflight, fee-net qty-1 win > `$0`, and first-live-row review before any second placement; do not auto-deploy from this backtest. Evidence: `research/2026-06-25-fx-bs-kalshi-weather-no-candidate-cell-preflight.md`. | Trigger-based |
| `fx_cm_kalshi_weather_yes_90_93_forward_review` | Kalshi weather YES 90-93 above-live-threshold forward review | FX-CM audited the only pass-ish all-period holdout from a broad ask-priced/event-first scan: `shadow_forecast_accuracy`, `side='yes'`, `0.90 <= ask_price < 0.93`, `COALESCE(live_match,0)=0`, collapsed first by weather event. Historical event-first evidence is now `97W-1L`, `+$1,368.03`, avg ask `0.914`, Wilson `94.4%` vs modeled BE `92.5%`, margin only `+1.9pp`; since `2026-06-17`, it is still underpowered at `17W-0L`, Wilson `81.6%` vs modeled BE `92.7%`. The single resolved loss is PHIL at ask `0.92` for `-$185.04`, and adjacent `93-95c` widening failed. 2026-06-26 11:05Z refresh: the native-forward cell has `2` events, `1` resolved, `1` pending, `1W-0L`, `+$0.07`, Wilson `20.7%` vs native BE `92.5%`; latest preflight checked `1` row and found `0` actionable because the remaining PHIL row moved out of band at native YES ask `0.98`. No live order placed. | Starting at `2026-06-25T11:45:00Z`, when `shadow_forecast_accuracy` has >=50 fresh resolved event-first rows with `side='yes'`, `0.90 <= ask_price < 0.93`, and `COALESCE(live_match,0)=0`, evaluate fee-net W-L/P&L, modeled breakeven from ask plus fees, Wilson lower margin >=`2pp` in both all-forward and recent slices, city/date concentration, pending hygiene, and native YES ask/depth availability from `kalshi_weather_yes_90_93_preflight`. Any pilot requires a new strategy identity, qty `1`, max-open `1`, current native YES ask/depth preflight, fee-net qty-1 economics, and first-live-row review before any second placement; do not widen to `93-95c` without fresh evidence clearing the same buffer. Evidence: `research/2026-06-25-fx-cm-kalshi-weather-yes-90-93-above-live-threshold.md` and `research/2026-06-26-fx-df-kalshi-weather-yes-93-95-adjacent-no-go.md`. | Trigger-based |
| `fx_bt_kalshi_crypto_price_range_bid_side_50_forward_maker_review` | Kalshi crypto price-range bid-side maker-fill review | FX-BT audited `shadow_price_range` after the side-aware resolver fix. Side-aware `category='CRYPTO'`, `side IN ('yes','no')`, `0.92 <= price <= 0.94` rows collapse to ticker+side first rows at `523W-0L`, `+$3,234.30`, Wilson `99.3%` vs modeled bid-price breakeven `93.8%`, with `4` unresolved. Since `2026-06-17`, the same predicate is `45W-0L`, `+$269.86`, with `4` pending. This is only prior evidence because the table records the side bid seen during scanning, not a native taker ask; legacy `side IS NULL` rows from before side-aware instrumentation were negative and are explicitly excluded. The active v2 high-price maker/cancel harness is already collecting the executable proxy for this band: current `category='crypto'`, `0.92 <= side_bid <= 0.94` rows show `29` quote candidates across `11` markets, `4` simulated fills, `4` pending fills, `0` resolved independent fills, `24` cancels, and `7` TTL-late-cross cancels. | Starting at `2026-06-25T07:30:00Z`, when the status line `Crypto price-range maker/cancel shadow` has >=50 forward resolved independent simulated maker fills, collapsed first by `market_ticker, side`, evaluate W-L, fee-net P&L, modeled breakeven from maker price plus fee, Wilson lower margin >=`2pp`, asset/day/hour concentration, side-specific YES/NO breakdown, fill rate, cancel reasons, TTL-late-crosses, and adverse-selection/toxicity labels. Any live pilot requires a separate maker-fill feasibility spec: new strategy identity, qty `1`, max-open `1`, post-only or quote/cancel semantics, explicit quote lifetime, fill/cancel/adverse-selection telemetry, first-fill review before any second fill, and no assumption that bid-side shadow rows are taker-executable. Evidence: `research/2026-06-25-fx-bt-kalshi-crypto-price-range-bid-side-shadow-audit.md`. | Trigger-based |
| `fx_bu_kalshi_crypto_favorite_no_taker_50_forward` | Kalshi crypto favorite NO taker forward review | FX-BU found an ask-priced, native-taker analog to the favorite-side prior in `shadow_favorites`: first eligible live-match rows with `category='CRYPTO'`, `side='no'`, `price_band='strong_fav_90-95'`, and `expiry_band='12-24h'` are `73W-1L`, `+$425.85`, with `2` unresolved pending rows. Corrected FX-BY model-breakeven rendering: avg ask `0.920`, Wilson `92.7%` versus modeled ask/fee breakeven `92.5%`, margin only `+0.2pp`; since `2026-06-17`, it is `23W-0L`, `+$177.77`, Wilson `85.7%` versus modeled BE `92.3%`, with `2` pending. Pending-clock refresh: next pending is `KXSOLD-26JUN2517-T70.9999` NO, due estimate `2026-06-25T20:59:59.022735+00:00`, ask `0.92`. This is more executable than the bid-side `shadow_price_range` prior because entry is the side ask and `live_match=1` requires ask `0.90-0.97`, `2-24h`, and spread `<=0.05`; it is still not live-deployable because the all-period margin is thin, recent Wilson is below modeled breakeven, the one loss is real, and the predicate is exploratory. | Starting at `2026-06-25T07:45:00Z`, when `shadow_favorites` has >=50 forward resolved first rows by `ticker, side` with `category='CRYPTO'`, `side='no'`, `price_band='strong_fav_90-95'`, `expiry_band='12-24h'`, and `live_match=1`, evaluate W-L, fee-net P&L, modeled breakeven from ask plus fee, Wilson lower margin >=`2pp`, asset/day/hour concentration, current pending outcomes, and native orderbook availability. Any live pilot requires a new strategy identity, qty `1`, max-open `1`, current native NO ask/depth preflight, fee-net qty-1 win > `$0`, and first-live-row review before any second placement; do not auto-deploy from this backtest. Evidence: `research/2026-06-25-fx-bu-kalshi-crypto-favorite-no-taker-shadow.md`. | Trigger-based |
| `fx_bx_kalshi_crypto_near_certain_taker_50_forward` | Kalshi crypto near-certain taker forward review | FX-BX surfaced a higher-price ask-side crypto favorite cell in `shadow_favorites`: `category='CRYPTO'`, `side IN ('yes','no')`, `price_band='near_certain_95+'`, `expiry_band='12-24h'`, `live_match=1`, collapsed first by `ticker, side`. All-period evidence is `188W-1L`, `+$528.92`, Wilson `97.1%` versus modeled ask/fee breakeven `96.5%`, margin only `+0.6pp`, with `11` pending. Since `2026-06-17`, it is `58W-1L`, `+$109.60`, Wilson `91.0%` versus modeled breakeven `96.4%`, so it is not live-deployable now. Native preflight is forward-only: the current native preflight refresh had `1` latest actionable near-certain contract, `KXETHD-26JUN2517-T1489.99` YES at native ask `0.95`, depth `10.00`, qty-1 `+$0.04`/`-$0.96`; the first-actionable native gate is still `9` pending, `0` resolved, Wilson `0.0%` vs BE `97.7%`. No live order placed. | Starting at `2026-06-25T08:10:00Z`, when `shadow_favorites` has >=50 forward resolved first rows by `ticker, side` with `category='CRYPTO'`, `side IN ('yes','no')`, `price_band='near_certain_95+'`, `expiry_band='12-24h'`, and `live_match=1`, and/or the native preflight gate has >=30 resolved first-actionable contracts in a single cohort, evaluate W-L, fee-net P&L, modeled breakeven from current ask plus fee, Wilson lower margin >=`2pp`, asset/side/day/hour concentration, pending outcomes, and native orderbook availability. Any live pilot requires a new strategy identity, qty `1`, max-open `1`, native ask/depth preflight, modeled qty-1 win/loss check, and first-live-row review before any second placement; do not auto-deploy from this backtest. Evidence: `research/2026-06-25-fx-bx-kalshi-crypto-near-certain-taker-shadow.md` and `research/2026-06-25-fx-cq-kalshi-crypto-favorite-taker-native-preflight.md`. | Trigger-based |
| `fx_cl_kalshi_crypto_last_hour_longshot_no_forward_liquidity` | Kalshi crypto last-hour longshot NO liquidity-backed forward review | FX-CL audited the fresh positive `shadow_longshot_fading` crypto cell: `category='crypto'`, `entry_side='NO'`, taker entry `0.80 <= COALESCE(entry_price_taker, entry_price) < 0.95`, `hours_to_expiry < 1`, collapsed first by crypto hourly event. Shadow event-first fragments remain source-discovery candidates, but execution controls still dominate: profit is historically concentrated in reported `volume=0` rows, while the executable proxy `volume>=500` and `spread<=0.05` remains below breakeven in the exact-BE report. 2026-06-26 12:04Z native-forward evidence is visible but still not sufficient: aggregate `crypto_last_hour_longshot_no` is now `32` resolved, `29W-3L`, `+$0.00`, Wilson `75.8%` vs native BE `90.6%`. The best mapped native subcell `strong:90-95` remains negative at `19` resolved, `17W-2L`, `-$0.56`, Wilson `68.6%` vs BE `92.4%`. The cleaner native ask `90-95c` fragment is perfect but underpowered at `16W-0L`, `+$1.09`, Wilson `80.6%` vs BE `93.2%`; native ask `80-90c` remains negative at `12W-2L`, `-$0.17`, Wilson `60.1%` vs BE `86.9%`. Current longshot live config excludes crypto, requires `4-72h`, and is killed; no live order placed. | Starting at `2026-06-25T11:20:00Z`, when `shadow_longshot_fading` has >=50 fresh resolved first-event rows with `category='crypto'`, `entry_side='NO'`, `0.80 <= COALESCE(entry_price_taker, entry_price) < 0.95`, `hours_to_expiry < 1`, and independently verified executable liquidity (`volume>=500` plus spread `<=0.05`, or native `actionable_qty1=1` rows in `kalshi_crypto_last_hour_longshot_no_preflight` proving qty-1 NO ask depth and positive fee-net win), evaluate aggregate and native subcell W-L, fee-net P&L, modeled breakeven from taker ask plus fees, Wilson lower margin >=`2pp`, volume-zero control behavior, native ask-band behavior, latest-actionability versus first-actionable gate evidence, asset/tier/hour concentration, and comparison against the stricter crypto favorite/near-certain taker gates. Any live pilot requires a new strategy identity, qty `1`, max-open `1`, current native NO ask/depth preflight, fee-net qty-1 win/loss check, and first-live-row review before any second placement; do not revive the killed longshot path or deploy from the historical volume-zero sample. Evidence: `research/2026-06-25-fx-cl-kalshi-crypto-last-hour-longshot-no-liquidity-audit.md`, `research/2026-06-25-fx-cw-kalshi-crypto-last-hour-native-subcell-audit.md`, and `research/2026-06-25-fx-de-kalshi-other-longshot-strong-watch-and-04z-refresh.md`. | Trigger-based |
| `fx_ck_kalshi_crypto_contrarian_no_underdog_forward` | Kalshi crypto contrarian NO underdog forward review | FX-CK audited the positive-looking residual `shadow_contrarian` crypto cell: `category='CRYPTO'`, `side='no'`, `price_band='underdog_20-40'`, `hours_band='18-24h'`, collapsed first by crypto event key. The original all-period event-first review was positive P&L but below decision threshold (`18W-33L`, `+$578.09`, avg ask `0.227`, Wilson `23.6%` vs modeled BE `24.0%`) and the stale April row is finalized YES on Kalshi. 2026-06-28 11:10Z refresh: exact event-first `20-40c` NO ask / `18-24h` evidence is `60` resolved events, `19W-41L`, `+$430.87`, avg ask `0.232`, Wilson `21.3%` vs target `25.2%`; since `2026-06-17` is `11W-7L`, `+$658.42`, but the predeclared forward window since `2026-06-25T10:40Z` is only `0W-2L`, `-$48.49`. The one active exact-regime shadow row is `KXBTCD-26JUN2817-T55999.99`, but a public Kalshi market/orderbook fetch returned empty YES and NO bid ladders, so there is no current native NO ask/depth to trade. The no-pilot conclusion is unchanged: April was negative, the predicate is post-hoc, fresh forward evidence is negative, and current native executability is absent. | Starting at `2026-06-25T10:40:00Z`, when `shadow_contrarian` has >=50 fresh forward resolved first-event rows with `category='CRYPTO'`, `side='no'`, `price_band='underdog_20-40'`, `hours_band='18-24h'`, and native-actionable NO ask/depth in the same price/execution regime, evaluate event W-L, fee-net `pnl_if_bought_no`, modeled breakeven from native `no_ask` plus fee, Wilson lower margin >=`2pp`, April/June and forward temporal stability, asset concentration, current native NO ask/depth availability, and comparison against the stricter crypto favorite/near-certain taker gates. Any live pilot requires a new strategy identity, qty `1`, max-open `1`, current native NO ask/depth preflight, fee-net qty-1 win/loss check, and first-live-row review before any second placement; do not auto-deploy from the post-hoc historical cell. Evidence: `research/2026-06-25-fx-ck-kalshi-crypto-contrarian-no-underdog.md`, `research/2026-06-25-fx-cv-kalshi-broad-event-first-shadow-audit.md`, and `research/2026-06-27-fx-ek-kalshi-crypto-contrarian-underdog-forward-check.md`. | Trigger-based |
| `fx_cc_kalshi_crypto_legacy_taker_no_50_forward` | Kalshi crypto legacy taker NO forward review | FX-CC audited the older `shadow_taker` ask-priced crypto NO favorite cell: `category='CRYPTO'`, `side='no'`, `0.90 <= ask_price < 0.95`, `12 <= hours_left < 24`, collapsed first by `ticker, side`. All-period fee-net evidence is `206W-8L`, `+$908.82`, avg ask `0.915`, Wilson `92.8%` versus modeled BE `92.0%`, margin `+0.8pp`, with `8` pending. Since `2026-06-17`, it is `23W-1L`, `+$93.62`, Wilson `79.8%` versus modeled BE `91.9%`, so the report marks `gate=RECENT_BELOW_BREAKEVEN`. The legacy scanner only records crypto asks around `0.91-0.92` inside 24h and lacks the newer `shadow_favorites live_match` spread gate. Next pending is `KXSOLD-26JUN2517-T70.9999` NO, due estimate `2026-06-25T20:59:59.022735+00:00`, ask `0.92`. | Starting at `2026-06-25T09:10:00Z`, when `shadow_taker` has >=50 fresh resolved first rows by `ticker, side` with `category='CRYPTO'`, `side='no'`, `0.90 <= ask_price < 0.95`, and `12 <= hours_left < 24`, evaluate W-L, fee-net P&L, modeled breakeven from ask plus fees, Wilson lower margin >=`2pp`, recent-window stability, underlier/day/hour concentration, pending outcomes, and comparison against the stricter `shadow_favorites live_match` crypto NO taker gate. Any live pilot requires a new strategy identity, qty `1`, max-open `1`, current native NO ask/depth preflight, fee-net qty-1 win > `$0`, and first-live-row review before any second placement; do not auto-deploy from the legacy backtest. Evidence: `research/2026-06-25-fx-cc-kalshi-crypto-legacy-taker-no-shadow.md`. | Trigger-based |
| `fx_cd_kalshi_legacy_untapped_index_fx_no_maker_50_forward` | Kalshi legacy untapped Index/FX NO maker-fill review | FX-CD audited the older `shadow_untapped_categories` high-bid NO surface: `category IN ('FX','INDEX')`, `side='no'`, `0.85 <= bid < 0.90`, `12 <= hours_left < 24`, collapsed first by `ticker, side`. All-period bid-side evidence is `391W-28L`, `+$2,606.35`, avg bid `0.864`, Wilson `90.5%` vs modeled BE `87.1%`, margin `+3.4pp`, with `17` pending. Since `2026-06-17`, it is `65W-3L`, `+$559.43`, Wilson `87.8%` vs modeled BE `87.4%`, margin only `+0.4pp`. The next pending legacy row has bid `0.88` and ask `1.00`, proving this is maker-priced and not taker-executable. The active maker/cancel proxy for Index NO `0.85 <= side_bid < 0.90` has `50` candidates, `9` simulated fills, `9` pending fills, and `0/50` resolved independent fills. | Starting at `2026-06-25T09:25:00Z`, when the active high-price maker/cancel harness has >=50 forward resolved independent simulated maker fills for `category IN ('fx','index')`, `side='NO'`, and `0.85 <= side_bid < 0.90`, collapsed first by `market_ticker, side`, evaluate W-L, fee-net realized P&L, modeled breakeven from maker price plus fee, Wilson lower margin >=`2pp`, fill/cancel rate, TTL-late-crosses, adverse-selection labels, and separate FX vs Index behavior. Any live pilot requires a new maker strategy identity, qty `1`, max-open `1`, explicit post-only/quote-cancel semantics, bounded quote lifetime, first-fill review before any second fill, and no assumption that legacy bid-side rows are taker-executable. Evidence: `research/2026-06-25-fx-cd-kalshi-legacy-untapped-index-fx-no-bid-side.md`. | Trigger-based |
| `fx_ce_kalshi_legacy_weather_city_no_maker_50_forward` | Kalshi legacy weather-city NO maker-fill review | FX-CE audited the older `shadow_weather_cities` high-bid NO surface: `side='no'`, `price >= 0.88`, collapsed first by `ticker, side`. All-period bid-side evidence is `4367W-207L`, `+$8,493.37`, avg bid `0.932`, Wilson `94.8%` vs modeled BE `93.6%`, margin `+1.2pp`, with `224` pending. Since `2026-06-17`, it is `955W-28L`, `+$2,177.70`, Wilson `95.9%` vs modeled BE `94.9%`, margin `+1.0pp`. A 2026-06-26 event-side subcell stress test found the aggregate still positive all-period (`899W-13L`, `+$3,296.89`, Wilson `97.58%` vs modeled BE `94.96%`) but recent event-side below breakeven (`212W-4L`, Wilson `95.34%` vs BE `96.17%`), with no simple price/hour/high-low/blocked slice and no city slice clearing both all-period and recent robustness gates. The active maker/cancel proxy for weather NO `side_bid >= 0.88` remains pending-only with no resolved independent fills. | Starting at `2026-06-25T09:35:00Z`, when the active high-price maker/cancel harness has >=50 forward resolved independent simulated maker fills for `category='weather'`, `side='NO'`, and `side_bid >= 0.88`, collapsed first by `market_ticker, side`, evaluate W-L, fee-net realized P&L, modeled breakeven from maker price plus fee, Wilson lower margin >=`2pp`, city/series and blocked/unblocked concentration, fill/cancel rate, TTL-late-crosses, adverse-selection labels, and stale pending-row hygiene. Do not add a narrower legacy weather-city NO logger unless fresh forward evidence clears the same event-side recent robustness check. Any live pilot requires a new maker strategy identity, qty `1`, max-open `1`, explicit post-only/quote-cancel semantics, bounded quote lifetime, first-fill review before any second fill, and no assumption that legacy bid-side rows are taker-executable. Evidence: `research/2026-06-25-fx-ce-kalshi-legacy-weather-city-no-bid-side.md`. | Trigger-based |
| `fx_cf_kalshi_crypto_long_expiry_bid_side_maker_50_forward` | Kalshi crypto long-expiry high-bid maker-fill review | FX-CF audited `shadow_long_expiry`: `category='CRYPTO'`, `side IN ('yes','no')`, `0.90 <= price < 0.95`, `24 <= hours_left <= 72`. Raw ticker-side evidence is `356W-0L`, `+$2,768.56`, but event-side collapse is only `56W-0L`, `+$416.10`, Wilson `93.6%` vs modeled BE `92.6%`, margin `+1.0pp`, with `12` event-side pending; event-only collapse is `31W-0L`, Wilson `89.0%` vs BE `93.0%`. Since `2026-06-17`, event-side is `11W-0L`, Wilson `74.1%` vs BE `92.6%`, so the report marks `RECENT_EVENT_UNDERPOWERED_MAKER_FORWARD_REQUIRED`. The same audit rejected `shadow_sell` crypto inverse rows: all-period profit was dominated by zero-cent inverse artifacts, while nonzero inverse bands were negative recently. The active maker/cancel proxy for crypto `0.90 <= side_bid < 0.95` has `45` candidates, `6` simulated fills, `6` pending fills, `0/50` resolved independent fills; only `2` candidates and `1` pending fill are 24h+. | Starting at `2026-06-25T09:50:00Z`, when the active high-price maker/cancel harness has >=50 forward resolved independent simulated maker fills for `category='crypto'`, `side_bid >= 0.90`, `side_bid < 0.95`, preferably with `hours_to_close >= 24`, collapsed first by `market_ticker, side`, evaluate W-L, fee-net realized P&L, modeled breakeven from maker price plus fee, Wilson lower margin >=`2pp`, asset/side/event concentration, fill/cancel rate, TTL-late-crosses, adverse-selection labels, and separate 24h+ versus <24h behavior. Any live pilot requires a new maker strategy identity, qty `1`, max-open `1`, explicit post-only/quote-cancel semantics, bounded quote lifetime, first-fill review before any second fill, and no assumption that bid-side rows are taker-executable. Evidence: `research/2026-06-25-fx-cf-kalshi-crypto-long-expiry-bid-side-and-sell-artifact.md`. | Trigger-based |
| `fx_cg_kalshi_commodity_wti_event_forward_review` | Kalshi commodity WTI event-collapsed shadow review | FX-CG audited the remaining fresh commodity surfaces. `shadow_blocked` WTI high-bid favorites were attractive at first-market level but failed event collapse: NO first-event `20W-1L`, `+$48.64`, Wilson `77.3%` vs modeled BE `92.9%`; YES first-event `20W-3L`, `-$133.54`, Wilson `67.9%` vs modeled BE `92.8%`. Recent since `2026-06-17` is only NO `4W-0L` with `1` pending and YES `2W-1L` with `1` pending. `shadow_contrarian` WTI NO longshot is ask-priced/live_match but high-variance and underpowered: first-event `5W-9L`, `+$294.32`, Wilson `16.3%` vs modeled BE `14.7%`, with only `2W-2L` recent and `2` pending. NWS direct weather was stale (`last=2026-04-23`) and sports maker had `0` resolved rows. | Starting at `2026-06-25T10:05:00Z`, when either WTI surface has >=50 forward resolved first-event observations, review event W-L, fee-net P&L, modeled breakeven from entry price plus fee, Wilson lower margin >=`2pp`, day/event/strike-side concentration, current native orderbook availability, and whether blocked-category status still applies. Eligible surfaces are `shadow_contrarian` with `category='COMMODITY'`, `live_match=1`, `price_band='longshot_0-20'`, `hours_band='36-48h'`, collapsed first by WTI event key, and `shadow_blocked` with `category='COMMODITY'`, `side IN ('no','yes')`, `0.90 <= price <= 0.94`, collapsed first by WTI event key and side. Any live pilot requires a new strategy identity, qty `1`, max-open `1`, current native ask/depth preflight, fee-net qty-1 win/loss check, and first-live-row review before any second placement. Evidence: `research/2026-06-25-fx-cg-kalshi-commodity-wti-shadow-event-collapse.md`. | Trigger-based |
| `fx_ch_kalshi_weather_near_expiry_favorite_50_forward` | Kalshi weather near-expiry favorite first-event review | FX-CH refreshed the Whelan-style `shadow_near_expiry_favorites` table and found a promising but underpowered weather favorite predicate: `category='weather'`, `entry_price >= 0.90`, `expiry_band IN ('1-2h','2-4h')`, collapsed first by weather event key. 2026-06-28 11:15Z refresh finalized the stale rows: row-level backfill updated `70` weather rows, all YES, for `+$429.00`; decision collapse is now `38W-0L`, `+$226.00`, avg ask `0.9405`, Wilson `90.8%` vs target about `96.1%`, with `0` pending. Since `2026-06-17`, it is `23W-0L`, `+$150.00`, Wilson `85.7%` vs target about `95.5%`; best `2-4h/p90_95` is `25W-0L`, `+$191.00`, Wilson `86.7%` vs target about `94.4%`. Still below decision N and fee-adjusted Wilson; native weather gates also fail. | Starting at `2026-06-25T10:15:00Z`, when `shadow_near_expiry_favorites` has >=50 forward resolved first-event rows with `category='weather'`, `entry_price >= 0.90`, and `expiry_band IN ('1-2h','2-4h')`, evaluate event W-L, fee-net P&L, modeled breakeven from ask plus fee, Wilson lower margin >=`2pp`, spread distribution, city/series/date concentration, pending-row freshness, and comparison against native weather NO preflight gates. Any live pilot requires a new strategy identity, qty `1`, max-open `1`, current native ask/depth preflight, fee-net qty-1 win/loss check, and first-live-row review before any second placement. Evidence: `research/2026-06-25-fx-ch-kalshi-weather-near-expiry-favorite-refresh.md`. | Trigger-based |
| `fx_ci_kalshi_sol_vol_model_event_forward_review` | Kalshi SOL vol-model executable-shadow event review | FX-CI audited `shadow_vol_model` rows with `asset='SOL'` and `would_place_live=1`. Raw executable rows are negative under the table's stored taker-fee P&L (`39W-36L`, `76` resolved, `-$1,794.00`, `1` flat, `5` pending). First-ticker collapse is only `32W-10L`, `+$181.00`, and first-event collapse fails outright at `5W-3L`, `-$68.00`, Wilson `30.6%`, with `1` pending event. Since `2026-06-17`, first-event evidence is `0W-2L`, `-$146.00`; the last executable shadow candidate was `2026-06-17 11:44:24`, and live `sol_vol_model` placements remain `0`. | Starting at `2026-06-25T10:25:00Z`, when `shadow_vol_model` has >=50 forward resolved first-event rows with `asset='SOL'` and `would_place_live=1`, evaluate event W-L, stored and corrected fee-net P&L, Wilson lower, ask/edge/hour distribution, repeated strike-ladder concentration, model calibration versus settlement side, current native orderbook availability, and whether the existing SOL vol live path is still disabled/dormant. Do not treat row-level or first-ticker strike ladders as independent evidence. Any live pilot requires explicit operator authorization, qty `1`, max-open `1`, current native ask/depth preflight, fee-net qty-1 win/loss check, and first-live-row review before any second placement. Evidence: `research/2026-06-25-fx-ci-kalshi-sol-vol-model-event-collapse.md`. | Trigger-based |
| `fx_bz_kalshi_crypto_no_lt10c_non_04z_forward_review` | Kalshi crypto NO `<10c` non-04Z forward review | CLOSED/SUPERSEDED 2026-06-25: the initial fresh non-04Z statistical trigger was later invalidated by source/native taker reconciliation. The report-side gate now renders `NOT_READY` because native/source NO asks below `10c` are absent (`0/116` fresh non-04Z, `0/174` broad), so the apparent low prices were bid-inverted shadow artifacts, not executable taker asks. No live order placed. | CLOSED into `fx_cs_kalshi_crypto_no_lt10c_non04z_review_ready_followup`; future work in this family requires a native-taker forward gate built from actual source/native NO asks below `0.10`. Evidence: `research/2026-06-25-fx-bz-kalshi-crypto-no-lt10c-04z-loss-cluster.md` and `research/2026-06-25-fx-cs-kalshi-crypto-no-lt10c-non04z-review-ready.md`. | Completed 2026-06-25 |
| `ibkr_weather_ds_uhsfo_5_to_8f_first_live_placement` | UHSFO 5-to-8F first live Weather DS placement verification | FD WS2 promoted `UHSFO_YES_cushion_5_to_8f` from shadow-only to the live Weather DS pilot under `SHADOW_APPROVAL_BOUNDARY_LIFTED_BY_OPERATOR_2026_05_24`. First-placement proof depends on venue supply and edge conditions, so it cannot be forced at deploy time. | On first `live_trades` row for `cell_key='UHSFO_YES_cushion_5_to_8f'` or strategy key `weather_pilot_UHSFO_YES_cushion_5_to_8f`, verify cohort tracker updates, CB ledger initializes, rollback evaluator includes the cell, and reconciliation remains $0.00. | Trigger-based |
| `fq_gemini_trades_auto_vacuum_after_open_positions_clear` | Gemini trades.db post-retention auto-VACUUM verification | FQ WS4 archived 99,704 rows from active Gemini `trades.db` into monthly SQLite archives, but safe auto-VACUUM deferred because four `gemini_reward_quote_pilot` positions were still open. VACUUM must not run while open-position gate is nonzero. | When Gemini `SELECT COUNT(*) FROM trades WHERE placed_at > datetime('now','-7 days') AND (resolution IS NULL OR resolution='PENDING')` returns 0, run `cd ~/.openclaw/workspace/scripts && python3 db_auto_vacuum.py --execute --only gemini_trades`, verify backup, `integrity_check=ok`, active DB size reduction, retention report rendering, and Gemini reconciliation remains $0.00. | Trigger-based |
| `fq_kalshi_auto_vacuum_pause_ack_remediation` | Kalshi auto-VACUUM pause acknowledgement remediation | FR WS3 fixed the Kalshi pause ACK path by checking the maintenance pause flag during one-second sleep increments and before balance/headroom API calls. Manual ACK verified within 10s. The subsequent end-to-end VACUUM attempt was interrupted after ~35m because other long-running processes held `trades.db`; `quick_check` and `integrity_check` both returned `ok`. `db_auto_vacuum.py` now defers when non-self DB handles are active instead of entering VACUUM. | During a true maintenance window, stop or quiesce non-live Kalshi DB readers/writers shown by `db_handles_active(...)`, then run `cd ~/.openclaw/workspace/scripts && python3 db_auto_vacuum.py --execute --only kalshi_trades`; verify backup, `integrity_check=ok`, active DB/WAL size result, pause files removed, Kalshi bot active, and reconciliation $0.00. | Trigger-based |
| `kalshi_btc_moderate_yes_ds_first_10_review` | BTC moderate-favorite YES DS pilot first-10 resolved review | CLOSED RESOLVED_BY_KILL 2026-05-27 (FW WS3): cohort died at n=5 (3W-2L, -$35.48) before reaching n=10. The 2L/30 asymmetric rollback gate fired earlier at 2L/5; kill switch `~/kalshi_favorites_bot/KILL_KALSHI_DS_BTC_MODERATE_YES` written 2026-05-27 08:05 (FQ WS1). | CLOSED. Trigger condition n=10 unreachable because strategy was killed at n=5. Evidence in research/2026-05-27-fq-ws1-btc-moderate-pilot-state-verification.md and FV WS1b. | Completed 2026-05-27 |
| `kalshi_btc_moderate_yes_ds_first_30_review` | BTC moderate-favorite YES DS pilot first-30 resolved review | CLOSED RESOLVED_BY_KILL 2026-05-27 (FW WS3): cohort died at n=5; trigger condition n=30 unreachable. See first-10 entry above. | CLOSED. Strategy killed; no n=30 cohort exists. | Completed 2026-05-27 |
| `kalshi_btc_moderate_yes_ds_n50_decision_review` | BTC moderate-favorite YES DS pilot n=50 decision review | CLOSED RESOLVED_BY_KILL 2026-05-27 (FW WS3): cohort died at n=5; trigger condition n=50 unreachable. | CLOSED. No n=50 cohort exists; revival requires fresh operator authorization with new strategy identity per CLAUDE.md "no revival authorized" discipline. | Completed 2026-05-27 |
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
| `kalshi_ds_contract_hour_max3_50_resolution_review` | Kalshi DS contract-hour max-3 cluster-cap forward review | CLOSED FAILED/INAPPLICABLE 2026-06-24; causal refresh 2026-06-25. Trigger reached with `68` resolved allowed post-cap DS rows, `66W-2L`, `+$39.58`, loss rate `2.9%` (Wilson `0.8%-10.1%`, compatible with the old `~2.26%` projection), but the blocked-candidate shadow was `50W-0L` on resolved rows. All resolved blocked rows had `candidate_qty=0`; current report renders `qty-backed causal 0/50 resolved`, so stored hypothetical P&L `+$0.00` is not economic and the rows are non-causal while global/independent caps were already binding. Standard DS is globally killed, so no live cap relaxation was made. | CLOSED. Do not carry max3 forward as validated evidence into any future DS identity. Any future DS redesign must re-test contract-hour concentration with fresh `candidate_qty>0` blocked rows and operator authorization. Evidence: `research/2026-06-24-fx-bd-kalshi-ds-contract-hour-cap-review.md`. | Completed 2026-06-24 |
| `kalshi_ds_cb_reset_at_clean_window_2026-05-13` | Kalshi DS CB reset after qty-700 deploy | COMPLETED 2026-05-13: initial deploy preserved the prior reset timestamps, then the natural clean window was observed with DS open positions at 0. Reset timestamps were updated to `2026-05-13 10:25:36-05:00`, Kalshi restarted, `/proc/<pid>/environ` verified, and cash_gap remained $0.00. | CLOSED. Daily and lifetime CB ledgers now start fresh for the qty-700 era against -700/-2100 limits. | Completed 2026-05-13 |
| `kalshi_ds_qty_300_eth_30_resolution_review` | Kalshi DS ETH qty 300 cohort review | Operator scaled ETH qty/cap 275 -> 300 on 2026-05-11 17:55:04 CDT after the qty-275 ETH cohort and $0.93 filter cohort cleared gates. | Once `ds_qty_cohort_tracker` `filter_combined_qty_300_eth_pilot` reaches 30+ resolved ETH trades, evaluate WR>=93%, Wilson lower>=85%, positive P&L, and no daily CB breach. No automatic further scale-up regardless of result. If qty-300 cohort fails P&L or CB at n=30, roll back to qty 275 per separate operator decision. | Trigger-based |
| `filter_combined_qty_400_eth_pilot_30_resolution_review` | Kalshi DS ETH qty 400 cohort review | CLOSED PASSED 2026-05-20: `filter_combined_qty_400_eth_pilot` reached 44 resolved, 43W-1L, Wilson lower 88.2%, P&L +$214.33, max DD $369.59, and no hard rollback trigger. Operator honored EXPANSION_CANDIDATE with qty/cap 500. | CLOSED. Forward ETH review now tracked under `filter_combined_qty_500_eth_pilot_30_resolution_review`. | Completed 2026-05-20 |
| `filter_combined_qty_500_eth_pilot_30_resolution_review` | Kalshi DS ETH qty 500 cohort review | CLOSED ROLLBACK_TRIGGERED 2026-05-21: qty-500 ETH cohort resolved 2 trades, 1W-1L, P&L -$486.04, with a single trade loss worse than -$100. Operator honored the pre-committed asymmetric rollback and returned ETH qty/cap to 400. | CLOSED. Forward ETH review now tracked under `filter_combined_qty_400_eth_post_rollback_pilot_30_resolution_review`. | Completed 2026-05-21 |
| `kalshi_ds_eth_qty_500_first_trade_alarm` | Kalshi DS ETH qty 500 first-trade alarm | RESOLVED 2026-05-21: first resolved qty-500 ETH trades included one WIN and one LOSS; the loss triggered the single-trade-loss rollback guard. | CLOSED. Evidence preserved in `filter_combined_qty_500_eth_pilot`. | Completed 2026-05-21 |
| `filter_combined_qty_400_eth_post_rollback_pilot_30_resolution_review` | Kalshi DS ETH qty 400 post-rollback cohort review | ETH qty 500 cohort hit asymmetric rollback at n=2 after a single loss worse than -$100. New post-rollback cohort starts at `DS_KALSHI_QTY_400_ETH_POST_ROLLBACK_START=2026-05-21T18:00:00+00:00` with qty/cap 400. | Once `filter_combined_qty_400_eth_post_rollback_pilot` reaches 30+ resolved ETH trades, evaluate WR>=93%, Wilson lower>=85%, positive P&L, and no daily CB breach. Asymmetric rollback remains armed: 2 losses in first 10, 3 losses in first 30, daily CB breach before n=20, or any single trade loss worse than -$80 -> rollback to qty 300. | Trigger-based |
| `filter_combined_qty_500_eth_pilot_residual_resolution` | ETH qty 500 cohort residual position resolution | Qty-500 cohort was closed at rollback time with 2 resolved trades. Any pre-rollback open qty-500 ETH positions should settle naturally and then final cohort P&L should be logged. Current T1 snapshot found zero unresolved DS rows in `trades`, so this is a guard item in case broker/platform state reveals delayed settlement rows outside local open state. | On any later resolution of pre-rollback qty-500 ETH rows, update the closed cohort final P&L and confirm no live placement path still uses qty/cap 500. | Trigger-based |
| `kalshi_ladder_sniper_v2_kill_log_monitoring` | V2 kill-log monitoring | DV established `ladder_sniper_v2_kill_log` and the surface-in-reports requirement. Forward monitoring depends on this table being populated only when expected gates fire. | Any new row in `ladder_sniper_v2_kill_log` requires operator review within 24h. If a kill fires with a gate name not in the documented inventory, escalate to forensic dispatch. | Trigger-based |
| `sports_ds_mlb_pilot_first_resolved_trade` | Sports DS MLB pilot first resolved trade | CLOSED VERIFIED 2026-06-24: first resolved pilot row was `sports_ds_mlb_pilot_trades.id=1` / `trade_id=7019`, `KXMLBSPREAD-26JUN162140LAAAZ-LAA6`, YES qty 10 @ `$0.89`, resolved WIN at 2026-06-17 04:17:54 for `+$1.03`. Source signal `id=4` was `PLACED`, main `trades.id=7019` matched strategy `sports_ds_mlb_spread_conservative_gap5plus`, and CB ledger row `id=1` recorded daily/lifetime running P&L `+$1.03` with no breach. Final follow-up state: 10 resolved, 8W-2L, `-$13.94`, open positions `0`; trade `7095` (`KXMLBSPREAD-26JUN241945AZSTL-AZ6`, YES qty 10 @ `$0.92`) resolved LOSS for `-$9.26`; rollback counters are first10 losses `2/2` and first30 losses `2/3`; daily/lifetime CB not breached, reconciliation gap `$0.00`. Risk-control update: `KILL_SPORTS_DS_MLB_PILOT` present as of 2026-06-24 and now justified by the fired first-10 rollback. | CLOSED. First-resolution instrumentation, rollback accounting, and final first-10 settlement verified. The pilot is killed; no scale-up or further placements under this identity. | Completed 2026-06-24 |
| `sports_ds_mlb_pilot_open_trade_7095_final_settlement` | Sports DS MLB killed-pilot final open-row settlement | CLOSED VERIFIED 2026-06-24: trade `7095`, `KXMLBSPREAD-26JUN241945AZSTL-AZ6`, YES qty 10 @ `$0.92`, resolved `LOSS` for `-$9.26` at `2026-06-25 02:49:13` UTC. Ran `sports_ds_mlb_pilot.resolve_ledger()`: unresolved pilot rows `1 -> 0`, first-10 cohort `8W-2L`, `-$13.94`, open Sports rows `0`, first10 losses `2/2`. Discord material updates posted as pause `1519534167933583440` and final settlement `1519535339314876427`. | CLOSED. Keep `KILL_SPORTS_DS_MLB_PILOT` present and verify future status reports continue to show no open Sports DS rows and no placements after the kill timestamp. Any revival requires a separate postmortem and operator-authorized new strategy identity. | Completed 2026-06-24 |
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
