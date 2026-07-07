# Rahm Current State

last_updated_utc: 2026-07-07T12:18:57+00:00
pipeline_heartbeat_utc: 2026-07-07T12:18:56+00:00
generator: Codex generate_current_state.py
workspace_head: 0710930

## Chat Startup Critical Summary
- Generated for Claude-in-chat startup at 2026-07-07T07:18:57-05:00; missing artifacts render UNAVAILABLE instead of breaking sync.
- Full-picture artifact: FULL PICTURE - 2026-07-07 07:10 AM

### Reconciliation and Cash
- Gemini: Cash balance: $22.74
- Gemini reconciliation: UNAVAILABLE
- Kalshi: Cash balance: $1,188.96
- Kalshi reconciliation: Reconciliation: resolved_pnl=$-1500.38 open_cost=$0.47 open_fees=$0.03 recon_adj=$189.84 expected_cash=$1188.96 cash_gap=$+0.00 unrealized=$-0.43 [MATCH]
- IBKR: NLV: $1,949.48
- IBKR state: Status: ⚠️ Flex sync 302h stale | ❌ Gateway DOWN | ❌ KILL switch active
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
- Gemini reward quote pilot: • [Gemini] Gemini Reward Quote Pilot: -$0.30 | 0W-3L | realized rows: 3 | fees: $0.00
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
- • MTD (through 2026-07-07): **$68.00**
- • Projected monthly total: **$301.15/mo**
- • API-realized net after external costs: **$-17126.66**
- • Gemini open positions: 8 trades, $9.50 at cost, $0.05 at mark
- • Combined true P&L: **$-16328.18**
- • True lifetime P&L (bots − one-time − recurring): **$-19230.77**
- External fixed burn is the recurring subscription runway driver; broker fees already embedded in venue/account P&L must not be double-counted.

## Trading Bot Runtime
### gemini
- unit: gemini-bot.service
- active: active/running
- pid: 9238
- nrestarts: 0
- active_enter: Fri 2026-07-03 09:09:17 CDT
- reconciliation:
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
  - Contrarian: 9026 entries | 9026 resolved | 894W-8132L (10%) | Hyp P&L: $+26,511.00
  - BRENT aggressive: 229 entries | 148 resolved | 122W-26L (82%) | Hyp P&L: $-1,582.00
  - Moderate favorites shadow: 7 entries | 2 resolved | 1W-1L (50%) | Hyp P&L: $-57.00
  - Vol model ask-side trade P&L: REVIEW_ONLY - stored model-direction accuracy is not trade P&L; BUY_NO_SYNTH assumes NO ask = 1 - YES bid and needs native quote verification.
  - SOL BUY_YES 4-24h <20c: n=35 | 6W-29L | P&L +$2.39 | Wilson 8.1% vs avg entry 10.3% | margin -2.2pp | status REVIEW_ONLY_DEDUPED_SHADOW
  - SOL BUY_NO_SYNTH 4-24h 80c+: n=30 | 30W-0L | P&L +$2.11 | Wilson 88.6% vs avg entry 93.0% | margin -4.3pp | status REVIEW_ONLY_SYNTHETIC_NO
  - ETH BUY_YES 0-4h 20-50c: n=157 | 56W-101L | P&L +$1.42 | Wilson 28.6% vs avg entry 34.8% | margin -6.2pp | status REVIEW_ONLY_DEDUPED_SHADOW
  - BTC BUY_YES 4-24h 20-50c: n=122 | 45W-77L | P&L +$0.92 | Wilson 28.8% vs avg entry 36.1% | margin -7.3pp | status REVIEW_ONLY_DEDUPED_SHADOW
  - BTC BUY_YES 0-4h 80c+: n=31 | 30W-1L | P&L +$0.72 | Wilson 83.8% vs avg entry 94.5% | margin -10.6pp | status REVIEW_ONLY_DEDUPED_SHADOW
  - Short expiry (0-16h): 847 entries | 736 resolved | 615W-121L (84%) | Hyp P&L: $-6,570.00
  - Lowprob (0.88-0.90): 924 entries | 527 resolved | 414W-113L (79%) | Hyp P&L: $-4,977.00
  - Lowband (0.75-0.89): 2524 entries | 1382 resolved | 930W-452L (67%) | Hyp P&L: $-17,746.00
  - Low cushion (2-3%): 674 entries | 482 resolved | 411W-71L (85%) | Hyp P&L: $-2,592.00
  - Expiry filter: 2212 entries | 311 resolved | 143W-168L (46%) | Hyp P&L: $-2,401.00

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
  - Reconciliation: resolved_pnl=$-1500.38 open_cost=$0.47 open_fees=$0.03 recon_adj=$189.84 expected_cash=$1188.96 cash_gap=$+0.00 unrealized=$-0.43 [MATCH]
  - ✓ HARD CHECK PASSED — gap $0.00
  - Reconciliation adjustment: $189.84 (auto-computed from exchange balance)
  - Expected cash: $1188.96
  - Actual cash (API): $1188.96
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
  - Lifetime P&L: -$1,242.55 across 3213 resolved trades
  - 24h P&L: +$0.13 (1W-1L resolved, 0 placed)
  - Historical realized buckets (17; sum must equal lifetime):
  - • [Kalshi] Kalshi Live Pilot Crypto Last Hour Btc Moderate 80 90 No V1: -$0.81 | 0W-1L | realized rows: 1 | fees: $0.01
  - ✓ Kalshi: lifetime -$1,242.55 / 3213 realized rows; bucket sum -$1,242.55 / 3213 rows
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
  - Live-matched v2 (full filter stack): 377W-15L (96.2%) | maker +$1,342.00  -> taker +$538.38
  - Live-matched v2 first-ticker: 257W-15L (94.5%) | taker -$159.13 | Wilson 91.1% vs BE 95.1% | 7d -$36.41 | gate=NOT_LIVE_DEPLOYABLE
  - v1→v2 drops: tier=5097, volume=2824, excluded=1159, category=185, spread=58, nws=52, hours=37
  - [2.5] Moderate Favorites Pilot ($0.80-$0.85 only)
  - Validation vs shadow: shadow WR 83.2% / -$20.00 (spread<=0.05 + allowed assets, matches pilot) | live WR 82.8% | shadow P&L negative; no revival
  - No-revival audit: late-settled live rows do not override the permanent kill; the matching shadow bucket remains loss-asymmetric after fees and repeated observations.
  - Scale-up criteria: disabled while KILL_MODERATE_FAVORITES is present; any revival requires a new forward-only strategy identity and explicit operator approval.
  - Mean reversion shadow freshness: last_row=2026-04-22T03:02:54Z age=76.4d live_match_last=2026-04-21T02:43:31Z post_kill_shadow_rows=0 post_kill_live_placements=0 | gate=STALE_NO_FORWARD_EVIDENCE
  - Forecast accuracy (live-matched 0.85-0.90): 194W-23L (89.4%) | -$379.31
  - Forecast accuracy first-ticker live-match: 190W-21L (90.0%) | -$93.63 | Wilson 85.3% vs BE 90.3% | gate=CONTINUE_SHADOW
  - Forecast accuracy YES 90-93 above-live-threshold: event-first 133W-4L n=137 | +$1,391.16 avg_ask=0.914 | Wilson 92.7% vs BE 92.5% margin=+0.2pp | recent 53W-3L n=56 Wilson 85.4% vs BE 92.6% | pending=0 stale_pending=0 | gate=THIN_MARGIN_RECENT_UNDERPOWERED_FORWARD_ONLY
  - Forecast accuracy high-ask NO event-first: ask>=0.98 all 1034W-8L n=1042 | +$1,229.10 avg_ask=0.985 | Wilson 98.5% vs BE 98.7%
  - Forecast accuracy high-ask NO ex-LAX: 948W-5L n=953 | +$1,591.02 avg_ask=0.985 | Wilson 98.8% vs BE 98.7% | unresolved_live_est_events=20 | gate=FORWARD_WATCH_ONLY
  - Forecast accuracy high-ask NO native preflight: rows=64849 events=278 actionable_qty1=1980 latest=2026-07-07T12:19:04+00:00 | reasons: missing_native_no_ask=54726, nonpositive_qty1_win:0.0000=4921, actionable_qty1_fee_positive=1980, native_no_ask_out_of_band:0.9700=565 | latest_run=2026-07-07T12:14:02+00:00 candidates=20 checked=20 actionable=5 run_reasons={"actionable_qty1_fee_positive": 5, "missing_native_no_ask": 8, "native_no_ask_out_of_band:0.9500": 1, "native_no_ask_out_of_band:0.9600": 1, "nonpositive_qty1_win:0.0000": 5}
  - Forecast accuracy high-ask NO latest actionables: captured=2026-07-07T12:19:04+00:00 events=12 actionable_events=2 best=KXHIGHCHI-26JUL07-T81 city=CHI event=KXHIGHCHI-26JUL07 due=2026-07-08T14:00:00+00:00 no_ask=0.98 depth=1077.57 win1=+$0.01 loss1=-$0.99
  - Forecast accuracy high-ask NO native gate: native_events=92 resolved=76 pending=16 73W-3L native_pnl=-$2.24 Wilson 89.0% vs BE 99.0% next_pending=KXLOWTPHIL-26JUL06-T64 city=PHIL event=KXLOWTPHIL-26JUL06 due=2026-07-07T19:00:00+00:00 ttl=52.9h no_ask=0.98 depth=6.00 win1=+$0.01 loss1=-$0.99
  - Forecast accuracy NO candidate-cell preflight: rows=45466 cohorts=2 events=98 actionable_qty1=12261 latest=2026-07-07T12:18:53+00:00 | latest_run=2026-07-07T12:18:53+00:00 candidates=8 checked=8 actionable=5 run_reasons={"no_90_95_min_probe_v1:native_no_ask_out_of_band:0.9900": 1, "no_95_98_zero_loss_cities_v1:actionable_qty1_fee_positive": 5, "no_95_98_zero_loss_cities_v1:missing_native_no_ask": 1, "no_95_98_zero_loss_cities_v1:native_no_ask_out_of_band:0.9100": 1}
  - Forecast accuracy NO candidate-cell cohorts: no_95_98_zero_loss_cities_v1 rows=40702 events=96 actionable=11361; no_90_95_min_probe_v1 rows=4764 events=13 actionable=900
  - Forecast accuracy NO candidate-cell latest cohort actionables: no_90_95_min_probe_v1 captured=2026-07-07T12:18:53+00:00 events=1 actionable_events=0 top_reason=native_no_ask_out_of_band:0.9900; no_95_98_zero_loss_cities_v1 captured=2026-07-07T12:18:53+00:00 events=7 actionable_events=5 best=KXHIGHTMIN-26JUL07-T86 city=MIN event=KXHIGHTMIN-26JUL07 due=2026-07-08T19:00:00+00:00 no_ask=0.95 depth=19.52 win1=+$0.04 loss1=-$0.96
  - Forecast accuracy NO candidate-cell historical control: all-city 95-98 980W-31L n=1011 Wilson 95.7% vs BE 96.7%; selected-cities 337W-2L n=339 Wilson 97.9% vs BE 96.8%; weakest_city=AUS 44W-1L n=45 Wilson 88.4% vs BE 96.9% | selected-city filter is in-sample; no live order
  - Forecast accuracy NO candidate-cell forward gate: no_90_95_min_probe_v1 native_events=13 resolved=12 pending=1 11W-1L native_pnl=-$0.34 Wilson 64.6% vs BE 94.4% next_pending=KXHIGHTMIN-26JUL07-T93 city=MIN event=KXHIGHTMIN-26JUL07 due=2026-07-08T19:00:00+00:00 ttl=43.6h no_ask=0.92 depth=13.00 win1=+$0.07 loss1=-$0.93; no_95_98_zero_loss_cities_v1 native_events=92 resolved=84 pending=8 82W-2L native_pnl=+$0.06 Wilson 91.7% vs BE 97.5% next_pending=KXLOWTMIA-26JUL06-B75.5 city=MIA event=KXLOWTMIA-26JUL06 due=2026-07-07T19:00:00+00:00 ttl=52.0h no_ask=0.96 depth=206.00 win1=+$0.03 loss1=-$0.97 best_pending=KXHIGHTLV-26JUL07-B110.5 city=LV event=KXHIGHTLV-26JUL07 due=2026-07-08T19:00:00+00:00 no_ask=0.95 depth=1.00 win1=+$0.04 loss1=-$0.96
  - Legacy untapped FX/Index NO shadow: bid=0.85-0.90 12-24h first-ticker-side 483W-33L n=516 | +$3,334.03 | avg_bid=0.865 | Wilson 91.2% vs modeled BE 87.1% margin=+4.1pp | pending=13 | gate=LEGACY_MAKER_FORWARD_REQUIRED
  - Legacy untapped FX/Index NO recency: since_2026-06-17 157W-8L n=165 +$1,287.11 pending=13 Wilson 90.7% vs modeled BE 87.2% | forward_since_2026-06-25T09:25Z resolved=80 pending=13 | KXEURUSD 25W-2L pending=1, KXINX 26W-2L pending=1, KXNASDAQ100 16W-0L pending=1, KXUSDJPY 27W-1L pending=1 | next_pending=KXUSDJPY-26JUL0710-B161.875 category=FX due_est=2026-07-07T13:59:59.070771+00:00 ttl_at_capture=14.7h bid=0.87 ask=0.89 | bid-side/maker-priced shadow, not taker-executable
  - Legacy untapped FX/Index NO event collapse: event-side 94W-5L n=99 +$725.55 pending=4 Wilson 88.7% vs modeled BE 87.6% margin=+1.2pp | recent_event_side 36W-2L n=38 Wilson 82.7% vs BE 87.5% | forward_event_side resolved=17 pending=4 | gate=RECENT_EVENT_UNDERPOWERED_MAKER_FORWARD_REQUIRED
  - Legacy untapped FX/Index NO maker/cancel proxy: v2 side_bid=0.85-0.90 candidates=650 markets=41 fills=31 pending_fills=5 resolved_indep=26/50 23W-3L pnl=-$5.00 Wilson 71.0% vs modeled BE 90.3% | cancels=619 late_cross_ttl=10 open=0 | gate=MAKER_FILL_FORWARD_REQUIRED
  - Legacy weather-city NO shadow: bid>=0.88 first-ticker-side 5911W-292L n=6203 | +$10,178.84 | avg_bid=0.932 | Wilson 94.7% vs modeled BE 93.7% margin=+1.1pp | pending=113 | gate=LEGACY_MAKER_FORWARD_REQUIRED
  - Legacy weather-city NO recency: since_2026-06-17 2499W-113L n=2612 +$3,863.17 pending=111 Wilson 94.8% vs modeled BE 94.2% | forward_since_2026-06-25T09:35Z resolved=1469 pending=111 | blocked 1702W-95L +$2,005.49, unblocked 4209W-197L +$8,173.35 | best=KXHIGHTPHX 248W-6L +$919.13; worst=KXLOWTDEN 245W-21L -$426.11 | next_pending=KXHIGHPHIL-26JUL07-B81.5 city=PHIL due_est=2026-07-08T04:58:59.462690+00:00 ttl_at_capture=24.8h bid=0.88 overdue_pending=13 | bid-side/maker-priced shadow, not taker-executable
  - Legacy weather-city NO event collapse: event-side 1176W-22L n=1198 +$3,903.25 pending=26 Wilson 97.2% vs modeled BE 94.9% margin=+2.3pp | recent_event_side 489W-13L n=502 Wilson 95.6% vs BE 95.4% | forward_event_side resolved=286 pending=26 | gate=EVENT_MAKER_FORWARD_REQUIRED
  - Legacy weather-city NO maker/cancel proxy: v2 side_bid>=0.88 candidates=162 markets=76 fills=50 pending_fills=2 resolved_indep=48/50 47W-1L pnl=+$21.12 Wilson 89.1% vs modeled BE 93.5% | cancels=111 late_cross_ttl=19 open=1 | gate=MAKER_FILL_FORWARD_REQUIRED
  - Crypto price-range bid-side shadow: side-aware ticker+side first rows 612W-0L n=612 | +$3,775.00 | Wilson 99.4% vs modeled BE 93.8% | pending=0 | gate=MAKER_FILL_FORWARD_REQUIRED
  - Crypto price-range bid-side recency: since_2026-06-17 134W-0L n=134 +$810.56 pending=0 | forward_since_2026-06-25T07:30Z resolved=87 pending=0 | YES 60W-0L pending=0, NO 47W-0L pending=0 | bid-side shadow, not taker-executable
  - Crypto price-range bid-side event collapse: event-side 107W-0L n=107 +$650.90 pending=0 Wilson 96.5% vs BE 93.9% margin=+2.6pp | event_only 73W-0L n=73 Wilson 95.0% vs BE 93.9% margin=+1.1pp | recent_event_side 35W-0L n=35 Wilson 90.1% vs BE 94.0% | forward_event_side resolved=23 pending=0 | gate=RECENT_EVENT_UNDERPOWERED_MAKER_FORWARD_REQUIRED
  - Crypto long-expiry bid-side shadow: 24-72h bid=0.90-0.95 event-side 65W-1L n=66 | +$382.46 | avg_bid=0.921 | Wilson 91.9% vs modeled BE 92.7% margin=-0.8pp | pending=10 | gate=NO_GO_EVENT_ONLY_COLLAPSE
  - Crypto long-expiry bid-side collapse: event_only 37W-0L n=37 +$260.81 Wilson 90.6% vs BE 93.0% | ticker-side_raw 409W-5L n=414 +$2,671.44 pending=91 | YES 35W-0L pending=5, NO 30W-1L pending=5
  - Crypto long-expiry bid-side recency: since_2026-06-17 event-side 20W-1L n=21 +$47.71 pending=6 Wilson 77.3% vs modeled BE 93.0% | forward_since_2026-06-25T09:50Z resolved=6 pending=2 | next_pending=none overdue_pending=10 | bid-side/maker-priced shadow, not taker-executable
  - Crypto long-expiry maker/cancel proxy: v2 crypto side_bid=0.90-0.95 candidates=618 markets=348 fills=144 pending_fills=5 resolved_indep=139/50 130W-9L pnl=-$2.42 Wilson 88.2% vs modeled BE 93.7% | 24hplus_candidates=122 24hplus_fills=20 24hplus_pending_fills=1 | cancels=441 late_cross_ttl=54 open=33 | gate=MAKER_FILL_FORWARD_REQUIRED
  - Crypto price-range maker/cancel shadow: v2 side_bid=0.92-0.94 candidates=333 markets=203 fills=87 filled_units=87 pending_fills=4 resolved_indep=83/50 79W-4L pnl=+$8.19 Wilson 88.3% vs modeled BE 94.2% | cancels=230 late_cross_ttl=26 open=16 | gate=MAKER_FILL_FORWARD_REQUIRED
  - Crypto price-range maker/cancel sides: NO rows=176 markets=103 fills=40 pending=0 resolved_rows=40; YES rows=157 markets=100 fills=47 pending=4 resolved_rows=43 | source=kalshi_high_price_maker_cancel_shadow | no live orders
  - Crypto legacy taker NO shadow: ask=0.90-0.95 12-24h first-ticker-side 250W-16L n=266 | +$520.34 | avg_ask=0.915 | Wilson 90.5% vs modeled BE 92.0% margin=-1.6pp | pending=5 | gate=NO_GO
  - Crypto favorite taker native preflight: rows=14063 cohorts=2 contracts=76 actionable_obs=3767 latest=2026-07-07T12:18:02+00:00 | latest_run=2026-07-07T12:18:02+00:00 candidates=14 checked=14 actionable=7 reasons={"crypto_favorite_no_90_95_12_24h:actionable_qty1_fee_positive": 2, "crypto_favorite_no_90_95_12_24h:missing_native_no_ask": 1, "crypto_favorite_no_90_95_12_24h:native_no_ask_out_of_band:0.9600": 1, "crypto_favorite_no_90_95_12_24h:native_no_ask_out_of_band:0.9700": 1, "crypto_favorite_no_90_95_12_24h:native_no_ask_out_of_band:0.9900": 1, "crypto_near_certain_95_99_12_24h:actionable_qty1_fee_positive": 5, "crypto_near_certain_95_99_12_24h:nonpositive_qty1_win:0.0000": 3} | no order path
  - Crypto favorite taker native cohorts: crypto_near_certain_95_99_12_24h rows=10465 contracts=57 actionable_obs=2944; crypto_favorite_no_90_95_12_24h rows=3598 contracts=21 actionable_obs=823
  - Crypto favorite taker latest cohort actionables: crypto_favorite_no_90_95_12_24h captured=2026-07-07T12:18:02+00:00 contracts=6 actionable_contracts=2 best=KXETHD-26JUL0717-T1829.99 side=NO asset=ETH event=KXETHD-26JUL0717 due=2026-07-07T20:59:59.408669+00:00 ask=0.91 depth=20389.00 win1=+$0.08 loss1=-$0.92; crypto_near_certain_95_99_12_24h captured=2026-07-07T12:18:02+00:00 contracts=8 actionable_contracts=5 best=KXBTCD-26JUL0717-T62249.99 side=YES asset=BTC event=KXBTCD-26JUL0717 due=2026-07-07T20:59:59.593079+00:00 ask=0.96 depth=1462.00 win1=+$0.03 loss1=-$0.97
  - Crypto favorite taker native gate: crypto_favorite_no_90_95_12_24h first_actionable_contracts=19 resolved=13 pending=6 11W-2L native_pnl=-$0.99 Wilson 57.8% vs BE 92.4% next_pending=KXETHD-26JUL0717-T1829.99 side=NO asset=ETH event=KXETHD-26JUL0717 due=2026-07-07T20:59:59.408669+00:00 ask=0.92 depth=706.00 win1=+$0.07 loss1=-$0.93 gate=NATIVE_FORWARD_ACCUMULATING; crypto_near_certain_95_99_12_24h first_actionable_contracts=54 resolved=46 pending=8 45W-1L native_pnl=+$0.10 Wilson 88.7% vs BE 97.5% next_pending=KXETHD-26JUL0717-T1869.99 side=NO asset=ETH event=KXETHD-26JUL0717 due=2026-07-07T20:59:59.207141+00:00 ask=0.95 depth=15057.00 win1=+$0.04 loss1=-$0.96 gate=NATIVE_FORWARD_ACCUMULATING
  - Crypto contrarian NO underdog shadow: ask=0.20-0.25 18-24h event-first 21W-44L n=65 +$534.53 avg_ask=0.228 Wilson 22.2% vs modeled BE 24.1% pending=3 active_pending=2 stale_pending=1 old_live_match_events=7/68 | gate=ALL_PERIOD_BELOW_BREAKEVEN_POSTHOC
  - Crypto contrarian NO recency: since_2026-06-17 13W-17L n=30 +$571.65 pending=2 Wilson 27.4% vs modeled BE 24.3% | forward_since_2026-06-25T10:40Z resolved=12 pending=2 | 2026-04 8W-27L -$37.12, 2026-06 13W-11L +$711.92 | BTC 8W-19L +$144.37 pending=1, ETH 9W-10L +$455.98 pending=0, SOL 4W-15L -$65.82 pending=2 | next_pending=KXBTCD-26JUL0717-T63249.99 event=KXBTCD-26JUL0717 due_est=2026-07-07T20:59:59.633653+00:00 ttl=8.7h ask=0.20 spread=0.01 active_pending=2 stale_pending=1 unknown_pending=0 | exploratory ask-priced shadow; no live orders
  - Crypto last-hour longshot NO shadow: event-first 1318W-85L n=1403 | +$6,950.48 avg_ask=0.883 | Wilson 92.6% vs modeled BE 89.0% | recent 897W-71L +$3,116.66 | gate=LIQUIDITY_PROXY_FAIL_FORWARD_ONLY
  - Crypto last-hour longshot liquidity: volume=0 620W-9L +$7,049.93; volume>=500/spread<=5c 476W-47L +$235.45 Wilson 88.3% vs BE 90.6%; 80-85c volume-backed 52W-5L +$419.10 Wilson 81.1% vs BE 83.9%; 90-95c volume-backed 305W-22L +$148.38 Wilson 90.0% vs BE 92.8%; 95-99c volume-backed 686W-27L -$661.86 Wilson 94.5% vs BE 97.1%; forward_since_2026-06-25T11:20Z 521W-47L +$1,130.88 Wilson 89.2% vs BE 89.7% resolved=568 pending=2 | no live orders
  - Crypto last-hour longshot native preflight: rows=7466 events=568 actionable_qty1=2134 latest=2026-07-07T12:16:13+00:00 | latest_run=2026-07-07T12:16:13+00:00 candidates=2 checked=2 actionable=0 reasons={"native_no_ask_out_of_band:0.5300": 1, "native_no_ask_out_of_band:0.6600": 1} | no order path
  - Crypto last-hour longshot latest actionables: captured=2026-07-07T12:16:13+00:00 events=2 contracts=2 actionable_contracts=0 top_reason=native_no_ask_out_of_band:0.6600
  - Crypto last-hour longshot native gate: native_events=437 resolved=435 pending=2 active_pending=2 stale_pending=0 unknown_pending=0 394W-41L native_pnl=-$0.28 Wilson 87.5% vs BE 90.6% next_pending=KXBTCD-26JUL0709-T63699.99 asset=BTC event=KXBTCD-26JUL0709 due=2026-07-07T12:59:59.188159+00:00 no_ask=0.80 depth=475.00 win1=+$0.18 loss1=-$0.82 | gate=NATIVE_FORWARD_ACCUMULATING
  - SOL vol model executable shadow: would_place_live row 47W-38L resolved=86 -$1,824.00 flat=1 pending=20 | first-ticker 35W-11L resolved=46 +$157.00 pending=5 | first-event 7W-4L resolved=11 -$108.00 pending=2 avg_ask=0.685 Wilson 35.4% | gate=EVENT_FORWARD_RECENCY_FAIL
  - SOL vol model recency: since_2026-06-17 first-event 2W-3L resolved=5 -$186.00 pending=1 Wilson 11.8% | last_candidate=2026-07-07 08:05:52 | live_placements=0 open=0 | stored taker-fee P&L; no new live orders
  - Weather near-expiry favorite shadow: 1-4h ask>=0.90 event-first 54W-0L n=54 +$308.00 avg_ask=0.943 Wilson 93.4% vs modeled BE 94.7% pending=1 overdue_pending=1 | gate=UNDERPOWERED_BELOW_BREAKEVEN
  - Weather near-expiry favorite recency: since_2026-06-17 39W-0L n=39 +$232.00 pending=1 Wilson 91.0% vs modeled BE 94.4% | best_event_price_cell=2-4h/p90_95 33W-0L n=33 +$247.00 pending=1 | next_pending=KXLOWTMIA-26JUL06-B77.5 event=KXLOWTMIA-26JUL06 due_est=2026-07-07T04:59:59+00:00 ask=0.92 spread=0.06 | ask-priced near-expiry shadow; no live orders
  - Commodity WTI high-bid blocked shadow: NO first-market 174W-5L n=179 +$854.40; event-side 22W-1L n=23 +$60.78 Wilson 79.0% vs BE 93.0% | YES first-market 113W-6L n=119 +$259.33; event-side 22W-3L n=25 -$116.69 Wilson 70.0% vs BE 92.7% | gate=EVENT_FORWARD_N50_REQUIRED
  - Commodity WTI blocked recency: since_2026-06-17 event-side NO 6W-0L n=6 +$35.48 pending=0, YES 4W-1L n=5 -$66.35 pending=0 | blocked-category diagnostic; no live orders
  - Commodity WTI contrarian NO longshot: event-side 5W-16L n=21 +$191.48 Wilson 10.6% vs BE 14.7% pending_events=1 | first-market 12W-58L n=70 +$381.51 | gate=EVENT_FORWARD_N50_REQUIRED
  - Commodity WTI contrarian recency: since_2026-06-17 event-side 2W-9L n=11 +$39.87 pending=1 | ask-priced live_match; high-variance longshot; no live orders
  - [2.3I] High-Price Maker/Cancel Shadow
  - Cohort: fx_aq_high_price_maker_cancel_shadow_600s_2026_06_24 | scanner=v2_high_price_maker_cancel_ttl_precedence_600s
  - Protocol: discovery cadence target 300s | quote TTL 600s | series fetch delay 2.0s | TTL checked before fill simulation.
  - Summary: rows=10956 open=255 fills=2529 markets=2271 cancels=8172 late_cross_ttl=612 resolved=2141 markets=1935 pnl=-5154.79 last=2026-07-07T12:15:53+00:00
  - Pending fills: unresolved=388 markets=336 next=KXSOLD-26JUL0709-T81.9999 crypto NO close=2026-07-07T13:00:00+00:00 expiration=2026-07-14T13:00:00+00:00 | units=388 active=388 stale=0 unknown=0
  - Overall independent fills: resolved=2141 1354W-787L pnl=-5154.79 wilson_low=61.2% breakeven=87.3% toxic=787 status=NO_GO_REVIEW
  - Review progress: best_cell=sports NO resolved_independent=707/50 indep=509W-198L pnl=-1084.11 wilson_low=68.6% breakeven=87.3% toxic=198 pending_markets=225 filled_markets=932 next_close=2026-07-07T15:05:00+00:00 status=NO_GO_REVIEW
  - Cell scan: resolved_cells=7 edge_positive_cells=0 leader=sports NO resolved_indep=707 best_edge_positive=none best_alternate=crypto NO resolved_indep=432 215W-217L pnl=-1577.75 wilson_low=45.1% breakeven=86.3% toxic=217 status=NO_GO_REVIEW
  - KALSHI CRYPTO LOW-PRICE NO CELL AUDIT
  - Status: SHADOW_ONLY | broad low-price NO kill=present | standard DS kill=present
  - NO <10c first-market: n=12 9W-3L wr=75.0% wilson_low=46.8% breakeven=4.4% pnl=+8.51 avg=+0.7092
  - NO <10c first-eligible: n=20 16W-4L wr=80.0% wilson_low=58.4% breakeven=5.0% pnl=+15.07 avg=+0.7535
  - NO <10c concentration: underliers=2 top=BTC n=17 share=85.0% pnl=+12.21 worst=ETH n=3 pnl=+2.86
  - NO <10c day stability: days=2 positive=2 losing=0 worst=2026-07-05 n=7 pnl=+3.57
  - NO <10c UTC-hour stability: hours=3 positive=3 losing=0 worst=03Z n=5 pnl=+3.81
  - Post-kill NO <10c first-market: n=12 9W-3L wr=75.0% wilson_low=46.8% breakeven=4.4% pnl=+8.51 avg=+0.7092
  - Post-kill NO <10c first-eligible: n=20 16W-4L wr=80.0% wilson_low=58.4% breakeven=5.0% pnl=+15.07 avg=+0.7535
  - Review: post-kill NO <10c first-eligible progress 20/50 status=ACCUMULATING reason=native taker NO ask <10c evidence absent
  - Post-kill NO <10c first-eligible concentration: underliers=2 top=BTC n=17 share=85.0% pnl=+12.21 worst=ETH n=3 pnl=+2.86
  - Post-kill NO <10c first-eligible day stability: days=2 positive=2 losing=0 worst=2026-07-05 n=7 pnl=+3.57
  - Post-kill NO <10c first-eligible UTC-hour stability: hours=3 positive=3 losing=0 worst=03Z n=5 pnl=+3.81
  - Post-kill NO <10c first-eligible loss cluster: losses=4 loss_hours=3 top_hour=02Z top_hour_losses=2/4 share=50.0% top_underlier=BTC 2/2 | excluding_top_loss_hour=POST_HOC_FORWARD_ONLY n=12 10W-2L pnl=+9.37 Wilson 55.2% vs modeled BE 5.6%
  - Post-kill NO <10c first-eligible source provenance: rows=20 sources=1 top=kalshi.shadow_deterministic_settlement n=20 distinct_source_row_ids=20 missing_source_row_ids=0
  - Post-kill NO <10c first-eligible native source check: source_ids=20 checked=16 native_taker_ask_lt10c=0/16 min=0.6900 avg=0.9156 max=0.9900
  - Fresh non-04Z NO <10c first-eligible: n=16 11W-5L wr=68.8% wilson_low=44.4% breakeven=3.9% pnl=+10.42 avg=+0.6512
  - Forward gate: fresh non-04Z NO <10c first-eligible start=2026-06-25T08:30:00+00:00 excluded_hour=04Z progress 16/50 pending_markets=0 status=ACCUMULATING reason=resolved 16/50; needs 34 new markets after pending; native taker NO ask <10c evidence absent
  - Fresh non-04Z NO <10c first-eligible pending horizon: resolved=16/50 pending_markets=0 max_if_all_pending_resolve=16/50 need_new_after_pending=34 next_due=unknown last_due=unknown next_backfill_after=unknown last_backfill_after=unknown
  - Fresh 04Z excluded-control NO <10c first-eligible: n=9 8W-1L wr=88.9% wilson_low=56.5% breakeven=5.9% pnl=+7.50 avg=+0.8333
  - Fresh non-04Z NO <10c first-eligible source provenance: rows=16 sources=1 top=kalshi.shadow_deterministic_settlement n=16 distinct_source_row_ids=16 missing_source_row_ids=0
  - Fresh non-04Z NO <10c first-eligible native source check: source_ids=16 checked=11 native_taker_ask_lt10c=0/11 min=0.7400 avg=0.9209 max=0.9900
  - Fresh non-04Z NO <10c first-eligible concentration: underliers=2 top=BTC n=13 share=81.2% pnl=+8.53 worst=ETH n=3 pnl=+1.89
  - Fresh non-04Z NO <10c first-eligible day stability: days=2 positive=2 losing=0 worst=2026-07-05 n=6 pnl=+1.78
  - Fresh non-04Z NO <10c first-eligible UTC-hour stability: hours=3 positive=3 losing=0 worst=05Z n=3 pnl=+0.91
  - Post-kill pending NO: rows=0 markets=0 actionable=0 qty50=0 avg_price=n/a first=none last=none
  - Post-kill pending NO <10c first-eligible: rows=0 markets=0 actionable=0 qty50=0 avg_price=n/a first=none last=none
  - Post-kill NO <10c first-eligible pending horizon: resolved=20/50 pending_markets=0 max_if_all_pending_resolve=20/50 need_new_after_pending=30 next_due=unknown last_due=unknown next_backfill_after=unknown last_backfill_after=unknown
  - Post-kill NO <10c first-eligible live pending preview: pending_first_eligible=0 live_actionable=0 settlement_pending_or_ineligible=0 now=2026-07-07T12:19:11+00:00 | no order path
  - Pilot readiness: NOT_READY | proposed_strategy=kalshi_crypto_no_lt10c_first_eligible_pilot | new identity required; do not revive ds_low_price_no | reason=resolved 20/50; needs 30 new markets after pending; native taker NO ask <10c evidence absent
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
  - FX first-symbol: 11W-162L n=173 | P&L -$1,202.63 | Wilson 3.6% vs BE 20.9% | native_NO 100.0% | side_match 100.0% | live YES/NO 166/7
  - INDEX first-symbol: 24W-388L n=412 | P&L -$617.18 | Wilson 3.9% vs BE 8.9% | native_NO 100.0% | side_match 100.0% | live YES/NO 412/0
  - Raw predicate: 45W-9L n=54 | P&L -$46.35 | Wilson 71.3% vs BE 86.8%
  - First-symbol: 41W-8L n=49 | P&L -$37.33 | Wilson 71.0% vs BE 86.7%
  - Pending predicate rows: 0
  - Review: first-30 progress 54/30 status=FAILED
  - KALSHI INDEX/FX SIDE-EQUIVALENCE FS SHADOW
  - Status: REJECTED_NATIVE_CONTROL | no live pilot
  - Pending native-actionable rows: FX=12686, INDEX=33442
  - Gate: failed; native executable rows disprove Index/FX favorite-tracking salvage

## Storage State
- DATABASE STORAGE HEALTH
-   Overall status: GREEN / TARGET
-   Disk: 308.29 GiB used / 936.79 GiB total (32.9%), 580.84 GiB free
-   Envelope: TARGET 50.0%, WARN 65.0%, CRITICAL 75.0%, HARD_LIMIT 85.0%
-   DS storage: active 1.19 GiB (state TARGET), hot 13.42 GiB, warm 0.16 GiB, cold 0.00 GiB, archive_state TARGET, total 14.79 GiB (1.6% of disk)
-   Archive sidecars: OK
-   Retention engine: last=2026-07-07T06:17:02+00:00 status=OK dry_run=False rows_selected=636 rows_archived=636 rows_pruned=0
-   Archive compression: status=OK actions=0 warm_days=7 min_file_mb=100
-   Tier rotation: last=2026-07-07T09:37:30+00:00 status=OK actions=0
-   Autonomous maintenance: last=2026-07-06T10:56:17+00:00 status=OK backups=4/5 integrity_failures=1 drift_flags=0
-   PROTECT_TRADING mode: NO
-   TOP_RISK: disk_used_pct grew 10.2pp over 24h
-   TOP_RISK: database integrity issue polymarket_shadow status=MISSING
-   TOP_RISK: gemini_trades trading DB may need operator-approved maintenance window

## Kalshi Same-Strike Complementarity
- source: daily-reports/same-strike-rollup-2026-07-04.md
- Date: 2026-07-04 UTC
- Scanner uptime: 22.3% (626 observed scan timestamps)
- Total: 54972
- Crypto: 38192
- Weather: 12154
- FX: 2458
- Index: 2168
- descriptive: 0
- fresh_simultaneous: 46837
- execution_ready: 8135
- All tiers: 2 (best edge $0.0100 on KXSOLD-26JUL0402-T84.9999)
- Fresh simultaneous: 2 (best edge $0.0100 on KXSOLD-26JUL0402-T84.9999)
- Execution ready: 0 (best edge $-0.0100 on KXHIGHCHI-26JUL04-T92)
- Independent opportunities (deduplicated by market_ticker): 0
- Empirical edge frequency: always tight
- Pilot-decision criteria status: deferred; no strategy attached; broker YES+NO simultaneous holding unverified

## Kalshi WS Per-Ticker Execution Gate
- command: `python3 scripts/kalshi_ws_orderbook_per_ticker_execution_gate.py --json`
- status: WS_PER_TICKER_EXECUTION_REVIEW | ready=false | live_ready=false | ready_tickers=0/2 | required_consecutive_ready=2 | scope=per-ticker WS infrastructure gate; not strategy authorization
- KXBTCD-26JUL0717-T61999.99: status=WS_TICKER_EXECUTION_REVIEW ready=false streak=0/2 latest_run=48 deltas=44 latency_max_ms=30.370 staleness_s=0.348 blockers=eligible_runs<2:1; run_age_s>180:1060.506
- KXHIGHMIA-26JUL07-B88.5: status=WS_TICKER_EXECUTION_REVIEW ready=false streak=0/2 latest_run=48 deltas=28 latency_max_ms=17.547 staleness_s=1.595 blockers=run_age_s>180:1060.528

## Kalshi WS Queue Capture Gate
- command: `python3 scripts/kalshi_ws_queue_capture_gate.py --json --max-age-s 180 --limit 40 --display-limit 8`
- status: WS_QUEUE_CAPTURE_STALE_OR_NO_CURRENT_COVERAGE | ready=false | live_ready=false | scope=read-only native WS book-event capture gate for maker queue/fill modeling
- summary: book_event_table=true | book_event_rows=137 | runs=3 | tickers=4 | latest_age_s=1060.6 | current_raw=15 | raw_fresh_queue=0 | clean_current=3 | clean_fresh_queue=0
- blockers: no_fresh_book_events_for_current_raw_candidates
- KXBTCD-26JUL0717-T60999.99: surface=crypto_favorite_taker side=YES raw=true inside=false analog=category_side:MAKER_ANALOG_NO_GO queue_fresh=false events=0 snapshots=0 deltas=0 levels=0 latest_age_s=n/a
- KXBTCD-26JUL0717-T61999.99: surface=crypto_favorite_taker side=YES raw=true inside=false analog=category_side:MAKER_ANALOG_NO_GO queue_fresh=false events=69 snapshots=25 deltas=44 levels=50 latest_age_s=1060.6
- KXBTCD-26JUL0717-T62249.99: surface=crypto_favorite_taker side=YES raw=true inside=true analog=exact:MAKER_ANALOG_REVIEW queue_fresh=false events=0 snapshots=0 deltas=0 levels=0 latest_age_s=n/a
- KXBTCD-26JUL0717-T65249.99: surface=crypto_favorite_taker side=NO raw=true inside=true analog=category_side:MAKER_ANALOG_NO_GO queue_fresh=false events=0 snapshots=0 deltas=0 levels=0 latest_age_s=n/a
- KXETHD-26JUL0717-T1829.99: surface=crypto_favorite_taker side=NO raw=true inside=false analog=price:MAKER_ANALOG_NO_GO queue_fresh=false events=0 snapshots=0 deltas=0 levels=0 latest_age_s=n/a
- KXETHD-26JUL0717-T1869.99: surface=crypto_favorite_taker side=NO raw=true inside=false analog=category_side:MAKER_ANALOG_NO_GO queue_fresh=false events=0 snapshots=0 deltas=0 levels=0 latest_age_s=n/a
- KXSOLD-26JUL0717-T83.9999: surface=crypto_favorite_taker side=NO raw=true inside=true analog=exact:MAKER_ANALOG_REVIEW queue_fresh=false events=0 snapshots=0 deltas=0 levels=0 latest_age_s=n/a
- KXHIGHCHI-26JUL07-T81: surface=weather_high_ask_no side=NO raw=true inside=false analog=category_side:MAKER_ANALOG_NO_GO queue_fresh=false events=0 snapshots=0 deltas=0 levels=0 latest_age_s=n/a

## Kalshi WS Queue Model Review
- command: `python3 scripts/kalshi_ws_queue_model_review.py --json --max-age-s 180 --limit 40 --display-limit 8`
- status: WS_QUEUE_MODEL_STALE_OR_NO_CURRENT_COVERAGE | ready=false | live_ready=false | scope=read-only queue-position/fill/adverse-selection model over persisted native WS book events
- summary: book_event_rows=137 | runs=3 | tickers=4 | latest_age_s=1061.2 | raw=15 | raw_fresh=0 | position_ready=0 | fill_observable=0 | same_level=0
- blockers: no_fresh_book_events_for_current_raw_candidates
- KXBTCD-26JUL0717-T60999.99: side=YES raw=true fresh=false run=n/a passive=0.97 coord=NO_SNAPSHOT_LEVELS_FOR_SIDE queue_ahead=n/a queue_after=n/a deltas=0/0 same_level=0 add=0.00 deplete=0.00 best_move=n/a opp_move=n/a adverse=false blockers=no_book_events_for_ticker; queue_capture_stale_or_missing; snapshot_events=0; side_snapshot_levels=0; coordinate_status=NO_SNAPSHOT_LEVELS_FOR_SIDE; delta_events=0; priced_delta_events=0; same_level_delta_rows=0
- KXBTCD-26JUL0717-T61999.99: side=YES raw=true fresh=false run=48 passive=0.96 coord=PASSIVE_LEVEL_NOT_IN_SNAPSHOT queue_ahead=n/a queue_after=n/a deltas=44/44 same_level=0 add=0.00 deplete=0.00 best_move=0.6400 opp_move=0.0000 adverse=false blockers=queue_capture_stale_or_missing; coordinate_status=PASSIVE_LEVEL_NOT_IN_SNAPSHOT; same_level_delta_rows=0; execution_not_ready; strategy_gate_no_live; maker_analog_not_clean; passive_inside_spread_unavailable
- KXBTCD-26JUL0717-T62249.99: side=YES raw=true fresh=false run=n/a passive=0.95 coord=NO_SNAPSHOT_LEVELS_FOR_SIDE queue_ahead=n/a queue_after=n/a deltas=0/0 same_level=0 add=0.00 deplete=0.00 best_move=n/a opp_move=n/a adverse=false blockers=no_book_events_for_ticker; queue_capture_stale_or_missing; snapshot_events=0; side_snapshot_levels=0; coordinate_status=NO_SNAPSHOT_LEVELS_FOR_SIDE; delta_events=0; priced_delta_events=0; same_level_delta_rows=0
- KXBTCD-26JUL0717-T65249.99: side=NO raw=true fresh=false run=n/a passive=0.96 coord=NO_SNAPSHOT_LEVELS_FOR_SIDE queue_ahead=n/a queue_after=n/a deltas=0/0 same_level=0 add=0.00 deplete=0.00 best_move=n/a opp_move=n/a adverse=false blockers=no_book_events_for_ticker; queue_capture_stale_or_missing; snapshot_events=0; side_snapshot_levels=0; coordinate_status=NO_SNAPSHOT_LEVELS_FOR_SIDE; delta_events=0; priced_delta_events=0; same_level_delta_rows=0
- KXETHD-26JUL0717-T1829.99: side=NO raw=true fresh=false run=n/a passive=0.90 coord=NO_SNAPSHOT_LEVELS_FOR_SIDE queue_ahead=n/a queue_after=n/a deltas=0/0 same_level=0 add=0.00 deplete=0.00 best_move=n/a opp_move=n/a adverse=false blockers=no_book_events_for_ticker; queue_capture_stale_or_missing; snapshot_events=0; side_snapshot_levels=0; coordinate_status=NO_SNAPSHOT_LEVELS_FOR_SIDE; delta_events=0; priced_delta_events=0; same_level_delta_rows=0
- KXETHD-26JUL0717-T1869.99: side=NO raw=true fresh=false run=n/a passive=0.97 coord=NO_SNAPSHOT_LEVELS_FOR_SIDE queue_ahead=n/a queue_after=n/a deltas=0/0 same_level=0 add=0.00 deplete=0.00 best_move=n/a opp_move=n/a adverse=false blockers=no_book_events_for_ticker; queue_capture_stale_or_missing; snapshot_events=0; side_snapshot_levels=0; coordinate_status=NO_SNAPSHOT_LEVELS_FOR_SIDE; delta_events=0; priced_delta_events=0; same_level_delta_rows=0
- KXSOLD-26JUL0717-T83.9999: side=NO raw=true fresh=false run=n/a passive=0.91 coord=NO_SNAPSHOT_LEVELS_FOR_SIDE queue_ahead=n/a queue_after=n/a deltas=0/0 same_level=0 add=0.00 deplete=0.00 best_move=n/a opp_move=n/a adverse=false blockers=no_book_events_for_ticker; queue_capture_stale_or_missing; snapshot_events=0; side_snapshot_levels=0; coordinate_status=NO_SNAPSHOT_LEVELS_FOR_SIDE; delta_events=0; priced_delta_events=0; same_level_delta_rows=0
- KXHIGHCHI-26JUL07-T81: side=NO raw=true fresh=false run=n/a passive=0.97 coord=NO_SNAPSHOT_LEVELS_FOR_SIDE queue_ahead=n/a queue_after=n/a deltas=0/0 same_level=0 add=0.00 deplete=0.00 best_move=n/a opp_move=n/a adverse=false blockers=no_book_events_for_ticker; queue_capture_stale_or_missing; snapshot_events=0; side_snapshot_levels=0; coordinate_status=NO_SNAPSHOT_LEVELS_FOR_SIDE; delta_events=0; priced_delta_events=0; same_level_delta_rows=0

## Kalshi Post-Only Cancel/Replace Dry-Run Gate
- command: `python3 scripts/kalshi_post_only_cancel_replace_dry_run_gate.py --json --max-age-s 180 --quote-ttl-s 60 --cancel-move-cents 2 --min-spread-cents 2 --limit 40 --display-limit 8`
- status: POST_ONLY_CANCEL_REPLACE_STALE_OR_NO_QUEUE_MODEL | ready=false | live_ready=false | dry_run_targets=0 | cancel_now=8 | replace_now=8 | scope=read-only post-only cancel/replace dry-run gate over native WS queue model; blocks live orders until queue freshness, per-ticker execution, maker analog, quote-age, spread, passive-coordinate, and operator-review controls all clear
- queue_summary: status=WS_QUEUE_MODEL_STALE_OR_NO_CURRENT_COVERAGE | raw=15 | raw_fresh=0 | position_ready=0 | fill_observable=0 | same_level=0 | latest_age_s=1061.9
- controls: post_only=true | quote_qty=1 | max_open_quotes=1 | quote_ttl_s=60 | max_queue_age_s=180 | cancel_move_cents=2.0 | min_spread_cents=2.0 | first_fill_review=true | no_live_orders=true
- blockers: cancel_queue_age>180s=1; cancel_queue_age_missing=7; execution_not_ready=8; maker_analog_gate_not_clean=8; maker_analog_not_specific=5; maker_analog_pnl<=0=6; maker_analog_resolved<30=3; maker_analog_toxic>0=6; passive_inside_spread_unavailable=5; queue_fill_model_not_observable=8; queue_model_not_fresh=8; queue_position_not_ready=8; replace_best_side_move>=2.0c=1; replace_passive_coordinate=NO_SNAPSHOT_LEVELS_FOR_SIDE=7; replace_passive_coordinate=PASSIVE_LEVEL_NOT_IN_SNAPSHOT=1; replace_spread<2.0c=5
- KXBTCD-26JUL0717-T60999.99: side=YES surface=crypto_favorite_taker category=crypto action=cancel dry_run_ready=false live_promotion_ready=false raw=true execution_ready=false strategy_ready=false fresh=false age_s=n/a age_status=QUEUE_AGE_MISSING ask=0.98 bid=0.97 spread=0.01 passive=0.97 coord=NO_SNAPSHOT_LEVELS_FOR_SIDE queue_ahead=n/a queue_after=n/a position_ready=false fill_observable=false same_level=false best_move=n/a opp_move=n/a adverse=false analog=category_side:MAKER_ANALOG_NO_GO resolved=399 pnl=-1212.58 toxic=176 cancel_reasons=queue_age_missing replace_reasons=spread<2.0c; passive_coordinate=NO_SNAPSHOT_LEVELS_FOR_SIDE dry_blockers=execution_not_ready; queue_model_not_fresh; passive_inside_spread_unavailable; queue_position_not_ready; queue_fill_model_not_observable; maker_analog_not_specific; maker_analog_gate_not_clean; maker_analog_pnl<=0; maker_analog_toxic>0; cancel_queue_age_missing; replace_spread<2.0c; replace_passive_coordinate=NO_SNAPSHOT_LEVELS_FOR_SIDE live_blockers=dry_run_not_ready; strategy_gate_no_live; execution_not_ready; cancel_required_before_live; replace_required_before_live; same_level_fill_signal_missing; operator_review_required; live_orders_disabled_in_gate
- KXBTCD-26JUL0717-T61999.99: side=YES surface=crypto_favorite_taker category=crypto action=cancel dry_run_ready=false live_promotion_ready=false raw=true execution_ready=false strategy_ready=false fresh=false age_s=1061.9 age_status=STALE_QUEUE_DATA ask=0.97 bid=0.96 spread=0.01 passive=0.96 coord=PASSIVE_LEVEL_NOT_IN_SNAPSHOT queue_ahead=n/a queue_after=n/a position_ready=false fill_observable=false same_level=false best_move=0.6400 opp_move=0.0000 adverse=false analog=category_side:MAKER_ANALOG_NO_GO resolved=399 pnl=-1212.58 toxic=176 cancel_reasons=queue_age>180s replace_reasons=spread<2.0c; passive_coordinate=PASSIVE_LEVEL_NOT_IN_SNAPSHOT; best_side_move>=2.0c dry_blockers=execution_not_ready; queue_model_not_fresh; passive_inside_spread_unavailable; queue_position_not_ready; queue_fill_model_not_observable; maker_analog_not_specific; maker_analog_gate_not_clean; maker_analog_pnl<=0; maker_analog_toxic>0; cancel_queue_age>180s; replace_spread<2.0c; replace_passive_coordinate=PASSIVE_LEVEL_NOT_IN_SNAPSHOT; replace_best_side_move>=2.0c live_blockers=dry_run_not_ready; strategy_gate_no_live; execution_not_ready; cancel_required_before_live; replace_required_before_live; same_level_fill_signal_missing; operator_review_required; live_orders_disabled_in_gate
- KXBTCD-26JUL0717-T62249.99: side=YES surface=crypto_favorite_taker category=crypto action=cancel dry_run_ready=false live_promotion_ready=false raw=true execution_ready=false strategy_ready=false fresh=false age_s=n/a age_status=QUEUE_AGE_MISSING ask=0.96 bid=0.94 spread=0.02 passive=0.95 coord=NO_SNAPSHOT_LEVELS_FOR_SIDE queue_ahead=n/a queue_after=n/a position_ready=false fill_observable=false same_level=false best_move=n/a opp_move=n/a adverse=false analog=exact:MAKER_ANALOG_REVIEW resolved=26 pnl=14.56 toxic=0 cancel_reasons=queue_age_missing replace_reasons=passive_coordinate=NO_SNAPSHOT_LEVELS_FOR_SIDE dry_blockers=execution_not_ready; queue_model_not_fresh; queue_position_not_ready; queue_fill_model_not_observable; maker_analog_gate_not_clean; maker_analog_resolved<30; cancel_queue_age_missing; replace_passive_coordinate=NO_SNAPSHOT_LEVELS_FOR_SIDE live_blockers=dry_run_not_ready; strategy_gate_no_live; execution_not_ready; cancel_required_before_live; replace_required_before_live; same_level_fill_signal_missing; operator_review_required; live_orders_disabled_in_gate
- KXBTCD-26JUL0717-T65249.99: side=NO surface=crypto_favorite_taker category=crypto action=cancel dry_run_ready=false live_promotion_ready=false raw=true execution_ready=false strategy_ready=false fresh=false age_s=n/a age_status=QUEUE_AGE_MISSING ask=0.97 bid=0.95 spread=0.02 passive=0.96 coord=NO_SNAPSHOT_LEVELS_FOR_SIDE queue_ahead=n/a queue_after=n/a position_ready=false fill_observable=false same_level=false best_move=n/a opp_move=n/a adverse=false analog=category_side:MAKER_ANALOG_NO_GO resolved=432 pnl=-1577.75 toxic=217 cancel_reasons=queue_age_missing replace_reasons=passive_coordinate=NO_SNAPSHOT_LEVELS_FOR_SIDE dry_blockers=execution_not_ready; queue_model_not_fresh; queue_position_not_ready; queue_fill_model_not_observable; maker_analog_not_specific; maker_analog_gate_not_clean; maker_analog_pnl<=0; maker_analog_toxic>0; cancel_queue_age_missing; replace_passive_coordinate=NO_SNAPSHOT_LEVELS_FOR_SIDE live_blockers=dry_run_not_ready; strategy_gate_no_live; execution_not_ready; cancel_required_before_live; replace_required_before_live; same_level_fill_signal_missing; operator_review_required; live_orders_disabled_in_gate
- KXETHD-26JUL0717-T1829.99: side=NO surface=crypto_favorite_taker category=crypto action=cancel dry_run_ready=false live_promotion_ready=false raw=true execution_ready=false strategy_ready=false fresh=false age_s=n/a age_status=QUEUE_AGE_MISSING ask=0.91 bid=0.90 spread=0.01 passive=0.90 coord=NO_SNAPSHOT_LEVELS_FOR_SIDE queue_ahead=n/a queue_after=n/a position_ready=false fill_observable=false same_level=false best_move=n/a opp_move=n/a adverse=false analog=price:MAKER_ANALOG_NO_GO resolved=26 pnl=-6.81 toxic=3 cancel_reasons=queue_age_missing replace_reasons=spread<2.0c; passive_coordinate=NO_SNAPSHOT_LEVELS_FOR_SIDE dry_blockers=execution_not_ready; queue_model_not_fresh; passive_inside_spread_unavailable; queue_position_not_ready; queue_fill_model_not_observable; maker_analog_gate_not_clean; maker_analog_resolved<30; maker_analog_pnl<=0; maker_analog_toxic>0; cancel_queue_age_missing; replace_spread<2.0c; replace_passive_coordinate=NO_SNAPSHOT_LEVELS_FOR_SIDE live_blockers=dry_run_not_ready; strategy_gate_no_live; execution_not_ready; cancel_required_before_live; replace_required_before_live; same_level_fill_signal_missing; operator_review_required; live_orders_disabled_in_gate
- KXETHD-26JUL0717-T1869.99: side=NO surface=crypto_favorite_taker category=crypto action=cancel dry_run_ready=false live_promotion_ready=false raw=true execution_ready=false strategy_ready=false fresh=false age_s=n/a age_status=QUEUE_AGE_MISSING ask=0.98 bid=0.97 spread=0.01 passive=0.97 coord=NO_SNAPSHOT_LEVELS_FOR_SIDE queue_ahead=n/a queue_after=n/a position_ready=false fill_observable=false same_level=false best_move=n/a opp_move=n/a adverse=false analog=category_side:MAKER_ANALOG_NO_GO resolved=432 pnl=-1577.75 toxic=217 cancel_reasons=queue_age_missing replace_reasons=spread<2.0c; passive_coordinate=NO_SNAPSHOT_LEVELS_FOR_SIDE dry_blockers=execution_not_ready; queue_model_not_fresh; passive_inside_spread_unavailable; queue_position_not_ready; queue_fill_model_not_observable; maker_analog_not_specific; maker_analog_gate_not_clean; maker_analog_pnl<=0; maker_analog_toxic>0; cancel_queue_age_missing; replace_spread<2.0c; replace_passive_coordinate=NO_SNAPSHOT_LEVELS_FOR_SIDE live_blockers=dry_run_not_ready; strategy_gate_no_live; execution_not_ready; cancel_required_before_live; replace_required_before_live; same_level_fill_signal_missing; operator_review_required; live_orders_disabled_in_gate
- KXSOLD-26JUL0717-T83.9999: side=NO surface=crypto_favorite_taker category=crypto action=cancel dry_run_ready=false live_promotion_ready=false raw=true execution_ready=false strategy_ready=false fresh=false age_s=n/a age_status=QUEUE_AGE_MISSING ask=0.92 bid=0.90 spread=0.02 passive=0.91 coord=NO_SNAPSHOT_LEVELS_FOR_SIDE queue_ahead=n/a queue_after=n/a position_ready=false fill_observable=false same_level=false best_move=n/a opp_move=n/a adverse=false analog=exact:MAKER_ANALOG_REVIEW resolved=7 pnl=6.24 toxic=0 cancel_reasons=queue_age_missing replace_reasons=passive_coordinate=NO_SNAPSHOT_LEVELS_FOR_SIDE dry_blockers=execution_not_ready; queue_model_not_fresh; queue_position_not_ready; queue_fill_model_not_observable; maker_analog_gate_not_clean; maker_analog_resolved<30; cancel_queue_age_missing; replace_passive_coordinate=NO_SNAPSHOT_LEVELS_FOR_SIDE live_blockers=dry_run_not_ready; strategy_gate_no_live; execution_not_ready; cancel_required_before_live; replace_required_before_live; same_level_fill_signal_missing; operator_review_required; live_orders_disabled_in_gate
- KXHIGHCHI-26JUL07-T81: side=NO surface=weather_high_ask_no category=weather action=cancel dry_run_ready=false live_promotion_ready=false raw=true execution_ready=false strategy_ready=false fresh=false age_s=n/a age_status=QUEUE_AGE_MISSING ask=0.98 bid=0.97 spread=0.01 passive=0.97 coord=NO_SNAPSHOT_LEVELS_FOR_SIDE queue_ahead=n/a queue_after=n/a position_ready=false fill_observable=false same_level=false best_move=n/a opp_move=n/a adverse=false analog=category_side:MAKER_ANALOG_NO_GO resolved=165 pnl=-133.80 toxic=31 cancel_reasons=queue_age_missing replace_reasons=spread<2.0c; passive_coordinate=NO_SNAPSHOT_LEVELS_FOR_SIDE dry_blockers=execution_not_ready; queue_model_not_fresh; passive_inside_spread_unavailable; queue_position_not_ready; queue_fill_model_not_observable; maker_analog_not_specific; maker_analog_gate_not_clean; maker_analog_pnl<=0; maker_analog_toxic>0; cancel_queue_age_missing; replace_spread<2.0c; replace_passive_coordinate=NO_SNAPSHOT_LEVELS_FOR_SIDE live_blockers=dry_run_not_ready; strategy_gate_no_live; execution_not_ready; cancel_required_before_live; replace_required_before_live; same_level_fill_signal_missing; operator_review_required; live_orders_disabled_in_gate

## Kalshi Realtime Candidate Execution Readiness
- command: `python3 scripts/kalshi_realtime_candidate_execution_readiness.py --json --limit 12 --max-per-surface 12`
- status: RAW_ACTIONABLE_CANDIDATES_EXECUTION_BLOCKED_OR_UNKNOWN | ready=false | live_ready=false | raw_actionable=15 | raw_actionable_ws_ready=0 | execution_ready_rows=0 | strategy_ready=0 | scope=read-only latest native preflight rows joined to per-ticker WS telemetry; strategy proof gates are not authorization here
- ws_gate: status=WS_PER_TICKER_EXECUTION_REVIEW | ready_tickers=0/39
- sources: weather_high_ask_no latest=2026-07-07T12:19:04+00:00 rows=20 loaded=12 raw_actionable=3 ; weather_yes_90_93 latest=2026-07-07T07:56:19+00:00 rows=1 loaded=1 raw_actionable=0 ; weather_no_candidate latest=2026-07-07T12:18:53+00:00 rows=8 loaded=8 raw_actionable=5 ; other_longshot_no_80_90 latest=2026-07-07T12:16:12+00:00 rows=6 loaded=6 raw_actionable=0 ; crypto_favorite_taker latest=2026-07-07T12:18:02+00:00 rows=14 loaded=12 raw_actionable=7 ; crypto_last_hour_longshot_no latest=2026-07-07T12:16:13+00:00 rows=2 loaded=2 raw_actionable=0 ; moderate_favorites_eth_yes latest=2026-07-07T03:56:09+00:00 rows=1 loaded=1 raw_actionable=0
- KXBTCD-26JUL0717-T60999.99: surface=crypto_favorite_taker side=YES context=asset=BTC,cohort_label=crypto_near_certain_95_99_12_24h,expiry_band=12-24h,price_band=near_certain_95+ status=RAW_ACTIONABLE_EXECUTION_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.98 depth=207 spread=0.01 qty1=0.01/-0.99 ws_run=45 reason=actionable_qty1_fee_positive blockers=run_age_s>180:7532.562; strategy_gate_no_live
- KXBTCD-26JUL0717-T61999.99: surface=crypto_favorite_taker side=YES context=asset=BTC,cohort_label=crypto_near_certain_95_99_12_24h,expiry_band=12-24h,price_band=near_certain_95+ status=RAW_ACTIONABLE_EXECUTION_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.97 depth=25 spread=0.01 qty1=0.02/-0.98 ws_run=48 reason=actionable_qty1_fee_positive blockers=eligible_runs<2:1; run_age_s>180:1062.584; strategy_gate_no_live
- KXBTCD-26JUL0717-T62249.99: surface=crypto_favorite_taker side=YES context=asset=BTC,cohort_label=crypto_near_certain_95_99_12_24h,expiry_band=12-24h,price_band=near_certain_95+ status=RAW_ACTIONABLE_EXECUTION_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.96 depth=1462 spread=0.02 qty1=0.03/-0.97 ws_run=n/a reason=actionable_qty1_fee_positive blockers=eligible_runs<2:0; no_eligible_runs; strategy_gate_no_live
- KXBTCD-26JUL0717-T65249.99: surface=crypto_favorite_taker side=NO context=asset=BTC,cohort_label=crypto_near_certain_95_99_12_24h,expiry_band=12-24h,price_band=near_certain_95+ status=RAW_ACTIONABLE_EXECUTION_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.97 depth=690 spread=0.02 qty1=0.02/-0.98 ws_run=n/a reason=actionable_qty1_fee_positive blockers=eligible_runs<2:0; no_eligible_runs; strategy_gate_no_live
- KXETHD-26JUL0717-T1829.99: surface=crypto_favorite_taker side=NO context=asset=ETH,cohort_label=crypto_favorite_no_90_95_12_24h,expiry_band=12-24h,price_band=strong_fav_90-95 status=RAW_ACTIONABLE_EXECUTION_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.91 depth=20389 spread=0.01 qty1=0.08/-0.92 ws_run=45 reason=actionable_qty1_fee_positive blockers=run_age_s>180:7532.612; strategy_gate_no_live
- KXETHD-26JUL0717-T1869.99: surface=crypto_favorite_taker side=NO context=asset=ETH,cohort_label=crypto_near_certain_95_99_12_24h,expiry_band=12-24h,price_band=near_certain_95+ status=RAW_ACTIONABLE_EXECUTION_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.98 depth=594 spread=0.01 qty1=0.01/-0.99 ws_run=43 reason=actionable_qty1_fee_positive blockers=run_age_s>180:11879.623; strategy_gate_no_live
- KXSOLD-26JUL0717-T83.9999: surface=crypto_favorite_taker side=NO context=asset=SOL,cohort_label=crypto_favorite_no_90_95_12_24h,expiry_band=12-24h,price_band=strong_fav_90-95 status=RAW_ACTIONABLE_EXECUTION_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.92 depth=200 spread=0.02 qty1=0.07/-0.93 ws_run=43 reason=actionable_qty1_fee_positive blockers=run_age_s>180:11879.758; strategy_gate_no_live
- KXHIGHCHI-26JUL07-T81: surface=weather_high_ask_no side=NO context=city=CHI status=RAW_ACTIONABLE_EXECUTION_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.98 depth=1078 spread=0.01 qty1=0.01/-0.99 ws_run=n/a reason=actionable_qty1_fee_positive blockers=eligible_runs<2:0; no_eligible_runs; strategy_gate_no_live
- KXHIGHTHOU-26JUL07-T92: surface=weather_high_ask_no side=NO context=city=HOU status=RAW_ACTIONABLE_EXECUTION_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.98 depth=112 spread=0.01 qty1=0.01/-0.99 ws_run=45 reason=actionable_qty1_fee_positive blockers=run_age_s>180:7532.690; ticker_deltas<1:KXHIGHTHOU-26JUL07-T92; ticker_missing_latency:KXHIGHTHOU-26JUL07-T92; ticker_staleness_s>2:KXHIGHTHOU-26JUL07-T92:12.114; strategy_gate_no_live
- KXHIGHTSEA-26JUL07-T82: surface=weather_high_ask_no side=NO context=city=SEA status=RAW_ACTIONABLE_EXECUTION_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.98 depth=2420 spread=0.01 qty1=0.01/-0.99 ws_run=41 reason=actionable_qty1_fee_positive blockers=eligible_runs<2:1; run_age_s>180:12654.735; ticker_deltas<1:KXHIGHTSEA-26JUL07-T82; ticker_missing_latency:KXHIGHTSEA-26JUL07-T82; ticker_staleness_s>2:KXHIGHTSEA-26JUL07-T82:10.086; strategy_gate_no_live
- KXHIGHMIA-26JUL07-B88.5: surface=weather_no_candidate side=NO context=city=MIA,cohort_label=no_95_98_zero_loss_cities_v1 status=RAW_ACTIONABLE_EXECUTION_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.96 depth=48 spread=0.02 qty1=0.03/-0.97 ws_run=48 reason=actionable_qty1_fee_positive blockers=run_age_s>180:1062.650; strategy_gate_no_live
- KXHIGHTDAL-26JUL07-B94.5: surface=weather_no_candidate side=NO context=city=DAL,cohort_label=no_95_98_zero_loss_cities_v1 status=RAW_ACTIONABLE_EXECUTION_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.98 depth=1835 spread=0.01 qty1=0.01/-0.99 ws_run=n/a reason=actionable_qty1_fee_positive blockers=eligible_runs<2:0; no_eligible_runs; strategy_gate_no_live

## Kalshi Candidate-Driven WS Probe Plan
- command: `python3 scripts/kalshi_candidate_ws_probe_runner.py --json --max-tickers 8 --max-per-surface 12`
- status: CANDIDATE_WS_PROBE_TARGETS_READY | mode=dry_run | ready=false | live_ready=false | selected_tickers=8 | scope=read-only raw candidate ticker selection for Kalshi WS probing
- pre_summary: raw_actionable=15 | raw_actionable_ws_ready=0 | strategy_ready=0
- KXETHD-26JUL0717-T1869.99: surface=crypto_favorite_taker side=NO context=asset=ETH,cohort_label=crypto_near_certain_95_99_12_24h,expiry_band=12-24h,price_band=near_certain_95+ ask=0.98 depth=594 spread=0.01 qty1=0.01/-0.99 due=2026-07-07T20:59:59.207141+00:00 reason=actionable_qty1_fee_positive
- KXETHD-26JUL0717-T1829.99: surface=crypto_favorite_taker side=NO context=asset=ETH,cohort_label=crypto_favorite_no_90_95_12_24h,expiry_band=12-24h,price_band=strong_fav_90-95 ask=0.91 depth=20389 spread=0.01 qty1=0.08/-0.92 due=2026-07-07T20:59:59.408669+00:00 reason=actionable_qty1_fee_positive
- KXBTCD-26JUL0717-T61999.99: surface=crypto_favorite_taker side=YES context=asset=BTC,cohort_label=crypto_near_certain_95_99_12_24h,expiry_band=12-24h,price_band=near_certain_95+ ask=0.97 depth=25 spread=0.01 qty1=0.02/-0.98 due=2026-07-07T20:59:59.582713+00:00 reason=actionable_qty1_fee_positive
- KXBTCD-26JUL0717-T62249.99: surface=crypto_favorite_taker side=YES context=asset=BTC,cohort_label=crypto_near_certain_95_99_12_24h,expiry_band=12-24h,price_band=near_certain_95+ ask=0.96 depth=1462 spread=0.02 qty1=0.03/-0.97 due=2026-07-07T20:59:59.593079+00:00 reason=actionable_qty1_fee_positive
- KXBTCD-26JUL0717-T60999.99: surface=crypto_favorite_taker side=YES context=asset=BTC,cohort_label=crypto_near_certain_95_99_12_24h,expiry_band=12-24h,price_band=near_certain_95+ ask=0.98 depth=207 spread=0.01 qty1=0.01/-0.99 due=2026-07-07T20:59:59.832726+00:00 reason=actionable_qty1_fee_positive
- KXBTCD-26JUL0717-T65249.99: surface=crypto_favorite_taker side=NO context=asset=BTC,cohort_label=crypto_near_certain_95_99_12_24h,expiry_band=12-24h,price_band=near_certain_95+ ask=0.97 depth=690 spread=0.02 qty1=0.02/-0.98 due=2026-07-07T20:59:59.914822+00:00 reason=actionable_qty1_fee_positive
- KXSOLD-26JUL0717-T83.9999: surface=crypto_favorite_taker side=NO context=asset=SOL,cohort_label=crypto_favorite_no_90_95_12_24h,expiry_band=12-24h,price_band=strong_fav_90-95 ask=0.92 depth=200 spread=0.02 qty1=0.07/-0.93 due=2026-07-07T20:59:59.927525+00:00 reason=actionable_qty1_fee_positive
- KXHIGHCHI-26JUL07-T81: surface=weather_high_ask_no side=NO context=city=CHI ask=0.98 depth=1078 spread=0.01 qty1=0.01/-0.99 due=2026-07-08T14:00:00+00:00 reason=actionable_qty1_fee_positive

## Kalshi Candidate Execution Quality
- command: `python3 scripts/kalshi_candidate_execution_quality.py --json --limit 8 --max-per-surface 12`
- status: REALTIME_EXECUTION_NOT_FRESH_FOR_CANDIDATES | ready=false | transport_ready=false | live_ready=false | raw_actionable=15 | raw_actionable_ws_ready=0 | inside_maker=3 | clean_analog=0 | quality_ready=0 | scope=read-only current native candidates scored for WS freshness, taker quote economics, inside-spread maker feasibility, and maker-shadow adverse-selection analogs
- shadow: available=true | rows=10956 | cohort=fx_aq_high_price_maker_cancel_shadow_600s_2026_06_24 | min_resolved=30 | edge_buffer=0.020
- KXBTCD-26JUL0717-T60999.99: surface=crypto_favorite_taker side=YES category=crypto context=asset=BTC,cohort_label=crypto_near_certain_95_99_12_24h,expiry_band=12-24h,price_band=near_certain_95+ status=RAW_ACTIONABLE_REALTIME_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.98 bid=0.97 spread=0.01 depth=207 passive=0.97 inside=false analog=category_side:MAKER_ANALOG_NO_GO resolved=399 pnl=-1212.58 toxic=176 edge_gap=-0.353 blockers=realtime_execution_not_fresh; run_age_s>180:7533.247; strategy_gate_no_live; spread<2c_for_inside_maker; passive_price_not_inside_book; maker_analog_pnl<=0; maker_analog_wilson<=BE+buffer; maker_analog_toxic>0; passive_inside_spread_unavailable
- KXBTCD-26JUL0717-T61999.99: surface=crypto_favorite_taker side=YES category=crypto context=asset=BTC,cohort_label=crypto_near_certain_95_99_12_24h,expiry_band=12-24h,price_band=near_certain_95+ status=RAW_ACTIONABLE_REALTIME_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.97 bid=0.96 spread=0.01 depth=25 passive=0.96 inside=false analog=category_side:MAKER_ANALOG_NO_GO resolved=399 pnl=-1212.58 toxic=176 edge_gap=-0.353 blockers=realtime_execution_not_fresh; eligible_runs<2:1; run_age_s>180:1063.268; strategy_gate_no_live; spread<2c_for_inside_maker; passive_price_not_inside_book; maker_analog_pnl<=0; maker_analog_wilson<=BE+buffer; maker_analog_toxic>0; passive_inside_spread_unavailable
- KXBTCD-26JUL0717-T62249.99: surface=crypto_favorite_taker side=YES category=crypto context=asset=BTC,cohort_label=crypto_near_certain_95_99_12_24h,expiry_band=12-24h,price_band=near_certain_95+ status=RAW_ACTIONABLE_REALTIME_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.96 bid=0.94 spread=0.02 depth=1462 passive=0.95 inside=true analog=exact:MAKER_ANALOG_REVIEW resolved=26 pnl=14.56 toxic=0 edge_gap=-0.073 blockers=realtime_execution_not_fresh; eligible_runs<2:0; no_eligible_runs; strategy_gate_no_live; maker_analog_resolved<30; maker_analog_wilson<=BE+buffer
- KXBTCD-26JUL0717-T65249.99: surface=crypto_favorite_taker side=NO category=crypto context=asset=BTC,cohort_label=crypto_near_certain_95_99_12_24h,expiry_band=12-24h,price_band=near_certain_95+ status=RAW_ACTIONABLE_REALTIME_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.97 bid=0.95 spread=0.02 depth=690 passive=0.96 inside=true analog=category_side:MAKER_ANALOG_NO_GO resolved=432 pnl=-1577.75 toxic=217 edge_gap=-0.412 blockers=realtime_execution_not_fresh; eligible_runs<2:0; no_eligible_runs; strategy_gate_no_live; maker_analog_pnl<=0; maker_analog_wilson<=BE+buffer; maker_analog_toxic>0
- KXETHD-26JUL0717-T1829.99: surface=crypto_favorite_taker side=NO category=crypto context=asset=ETH,cohort_label=crypto_favorite_no_90_95_12_24h,expiry_band=12-24h,price_band=strong_fav_90-95 status=RAW_ACTIONABLE_REALTIME_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.91 bid=0.90 spread=0.01 depth=20389 passive=0.90 inside=false analog=price:MAKER_ANALOG_NO_GO resolved=26 pnl=-6.81 toxic=3 edge_gap=-0.201 blockers=realtime_execution_not_fresh; run_age_s>180:7533.296; strategy_gate_no_live; spread<2c_for_inside_maker; passive_price_not_inside_book; maker_analog_resolved<30; maker_analog_pnl<=0; maker_analog_wilson<=BE+buffer; maker_analog_toxic>0; passive_inside_spread_unavailable
- KXETHD-26JUL0717-T1869.99: surface=crypto_favorite_taker side=NO category=crypto context=asset=ETH,cohort_label=crypto_near_certain_95_99_12_24h,expiry_band=12-24h,price_band=near_certain_95+ status=RAW_ACTIONABLE_REALTIME_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.98 bid=0.97 spread=0.01 depth=594 passive=0.97 inside=false analog=category_side:MAKER_ANALOG_NO_GO resolved=432 pnl=-1577.75 toxic=217 edge_gap=-0.412 blockers=realtime_execution_not_fresh; run_age_s>180:11880.307; strategy_gate_no_live; spread<2c_for_inside_maker; passive_price_not_inside_book; maker_analog_pnl<=0; maker_analog_wilson<=BE+buffer; maker_analog_toxic>0; passive_inside_spread_unavailable
- KXSOLD-26JUL0717-T83.9999: surface=crypto_favorite_taker side=NO category=crypto context=asset=SOL,cohort_label=crypto_favorite_no_90_95_12_24h,expiry_band=12-24h,price_band=strong_fav_90-95 status=RAW_ACTIONABLE_REALTIME_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.92 bid=0.90 spread=0.02 depth=200 passive=0.91 inside=true analog=exact:MAKER_ANALOG_REVIEW resolved=7 pnl=6.24 toxic=0 edge_gap=-0.265 blockers=realtime_execution_not_fresh; run_age_s>180:11880.442; strategy_gate_no_live; maker_analog_resolved<30; maker_analog_wilson<=BE+buffer
- KXHIGHCHI-26JUL07-T81: surface=weather_high_ask_no side=NO category=weather context=city=CHI status=RAW_ACTIONABLE_REALTIME_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.98 bid=0.97 spread=0.01 depth=1078 passive=0.97 inside=false analog=category_side:MAKER_ANALOG_NO_GO resolved=165 pnl=-133.80 toxic=31 edge_gap=-0.148 blockers=realtime_execution_not_fresh; eligible_runs<2:0; no_eligible_runs; strategy_gate_no_live; spread<2c_for_inside_maker; passive_price_not_inside_book; maker_analog_pnl<=0; maker_analog_wilson<=BE+buffer; maker_analog_toxic>0; passive_inside_spread_unavailable

## Kalshi Wide Non-Transport MM Gate
- command: `python3 scripts/kalshi_wide_nontransport_mm_gate.py --json --max-per-surface 50 --limit 200 --display-limit 8`
- status: WIDE_MM_NONTRANSPORT_BLOCKED | ready=false | live_ready=false | clean_ws_probe_rows=0 | scope=read-only wide current native-candidate MM gate before WS probing; requires raw-actionable native economics, inside-spread passive maker price, no quote blockers, and a specific clean maker-shadow analog before spending realtime WS probe budget
- params: max_per_surface=50 | row_limit=200 | analog_min_resolved=30 | analog_edge_buffer=2.0%
- summary: candidate_rows_loaded=52 | candidate_rows_reported=52 | raw_actionable=15 | raw_actionable_ws_ready=0 | inside_maker=16 | raw_inside=4 | raw_inside_specific=3 | raw_inside_specific_positive=3 | clean_analog=0 | quality_ready=0
- blockers: depth<1=16; maker_analog_fills=0=2; maker_analog_gate_not_clean=52; maker_analog_not_clean_enough_for_ws=52; maker_analog_not_specific=42; maker_analog_pnl<=0=47; maker_analog_resolved<30=8; maker_analog_toxic>0=46; maker_analog_wilson<=BE+buffer=50; maker_shadow_no_analog=2; missing_loss_pnl_qty1=16; missing_side_ask=16; missing_spread=16; not_raw_actionable=37; passive_inside_spread_unavailable=36; passive_price_not_inside_book=20; qty1_no_positive_after_fee=16; spread<2c_for_inside_maker=20
- KXBTCD-26JUL0717-T62249.99: surface=crypto_favorite_taker side=YES category=crypto clean_ws_probe=false raw_actionable=true execution_ready=false ask=0.96 bid=0.94 spread=0.02 passive=0.95 inside=true analog=exact:MAKER_ANALOG_REVIEW resolved=26 pnl=14.56 fill_rate=34.1% avg_adverse_move=0.0184 toxic=0 blockers=maker_analog_gate_not_clean; maker_analog_resolved<30; maker_analog_wilson<=BE+buffer; maker_analog_not_clean_enough_for_ws
- KXSOLD-26JUL0717-T83.9999: surface=crypto_favorite_taker side=NO category=crypto clean_ws_probe=false raw_actionable=true execution_ready=false ask=0.92 bid=0.90 spread=0.02 passive=0.91 inside=true analog=exact:MAKER_ANALOG_REVIEW resolved=7 pnl=6.24 fill_rate=13.5% avg_adverse_move=0.0265 toxic=0 blockers=maker_analog_gate_not_clean; maker_analog_resolved<30; maker_analog_wilson<=BE+buffer; maker_analog_not_clean_enough_for_ws
- KXHIGHMIA-26JUL07-B88.5: surface=weather_no_candidate side=NO category=weather clean_ws_probe=false raw_actionable=true execution_ready=false ask=0.96 bid=0.94 spread=0.02 passive=0.95 inside=true analog=exact:MAKER_ANALOG_REVIEW resolved=11 pnl=6.16 fill_rate=35.1% avg_adverse_move=0.0124 toxic=0 blockers=maker_analog_gate_not_clean; maker_analog_resolved<30; maker_analog_wilson<=BE+buffer; maker_analog_not_clean_enough_for_ws
- KXBTCD-26JUL0717-T65249.99: surface=crypto_favorite_taker side=NO category=crypto clean_ws_probe=false raw_actionable=true execution_ready=false ask=0.97 bid=0.95 spread=0.02 passive=0.96 inside=true analog=category_side:MAKER_ANALOG_NO_GO resolved=432 pnl=-1577.75 fill_rate=30.4% avg_adverse_move=0.1188 toxic=217 blockers=maker_analog_not_specific; maker_analog_gate_not_clean; maker_analog_pnl<=0; maker_analog_toxic>0; maker_analog_wilson<=BE+buffer; maker_analog_not_clean_enough_for_ws
- KXETHD-26JUL0717-T1829.99: surface=crypto_favorite_taker side=NO category=crypto clean_ws_probe=false raw_actionable=true execution_ready=false ask=0.91 bid=0.90 spread=0.01 passive=0.90 inside=false analog=price:MAKER_ANALOG_NO_GO resolved=26 pnl=-6.81 fill_rate=16.4% avg_adverse_move=0.0487 toxic=3 blockers=passive_inside_spread_unavailable; spread<2c_for_inside_maker; passive_price_not_inside_book; maker_analog_gate_not_clean; maker_analog_resolved<30; maker_analog_pnl<=0; maker_analog_toxic>0; maker_analog_wilson<=BE+buffer; maker_analog_not_clean_enough_for_ws
- KXHIGHTMIN-26JUL07-T86: surface=weather_no_candidate side=NO category=weather clean_ws_probe=false raw_actionable=true execution_ready=false ask=0.95 bid=0.94 spread=0.01 passive=0.94 inside=false analog=price:MAKER_ANALOG_NO_GO resolved=46 pnl=-34.24 fill_rate=46.2% avg_adverse_move=0.0265 toxic=6 blockers=passive_inside_spread_unavailable; spread<2c_for_inside_maker; passive_price_not_inside_book; maker_analog_gate_not_clean; maker_analog_pnl<=0; maker_analog_toxic>0; maker_analog_wilson<=BE+buffer; maker_analog_not_clean_enough_for_ws
- KXHIGHTOKC-26JUL07-T91: surface=weather_no_candidate side=NO category=weather clean_ws_probe=false raw_actionable=true execution_ready=false ask=0.96 bid=0.95 spread=0.01 passive=0.95 inside=false analog=price:MAKER_ANALOG_NO_GO resolved=46 pnl=-34.24 fill_rate=46.2% avg_adverse_move=0.0265 toxic=6 blockers=passive_inside_spread_unavailable; spread<2c_for_inside_maker; passive_price_not_inside_book; maker_analog_gate_not_clean; maker_analog_pnl<=0; maker_analog_toxic>0; maker_analog_wilson<=BE+buffer; maker_analog_not_clean_enough_for_ws
- KXHIGHCHI-26JUL07-T81: surface=weather_high_ask_no side=NO category=weather clean_ws_probe=false raw_actionable=true execution_ready=false ask=0.98 bid=0.97 spread=0.01 passive=0.97 inside=false analog=category_side:MAKER_ANALOG_NO_GO resolved=165 pnl=-133.80 fill_rate=45.0% avg_adverse_move=0.0310 toxic=31 blockers=passive_inside_spread_unavailable; spread<2c_for_inside_maker; passive_price_not_inside_book; maker_analog_not_specific; maker_analog_gate_not_clean; maker_analog_pnl<=0; maker_analog_toxic>0; maker_analog_wilson<=BE+buffer; maker_analog_not_clean_enough_for_ws

## Kalshi Candidate Execution Quality Forward Watch
- command: `python3 scripts/kalshi_candidate_execution_quality_forward_watch.py --record --json --limit 12 --max-per-surface 12 --latest-limit 8`
- status: FORWARD_WATCH_ACCUMULATING | mode=recorded | ready=false | watch_ready=false | live_ready=false | watch_id=candidate_execution_quality_mm_forward_watch_v1 | start_at=2026-07-07T08:36:00Z | scope=predeclared execution-quality/MM forward watch; no live authorization
- current: rows=12 | raw_actionable=12 | raw_actionable_execution_ready=0 | inside_spread=4 | watch_candidates=0 | execution_mm_ready=0 | recorded_rows=12
- forward: observations=334 | unique_tickers=27 | watch_candidate_observations=0 | execution_mm_ready_observations=0 | latest=2026-07-07T12:19:18Z | blockers=current_watch_candidates=0; current_raw_actionable_execution_ready=0
- KXBTCD-26JUL0717-T60999.99: side=YES surface=crypto_favorite_taker category=crypto status=RAW_ACTIONABLE_WATCH_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.98 bid=0.97 spread=0.01 passive=0.97 inside=false analog=category_side:MAKER_ANALOG_NO_GO resolved=399 pnl=-1212.58 toxic=176 blockers=execution_not_fresh; passive_inside_spread_unavailable; maker_analog_not_specific; maker_analog_no_go; maker_analog_toxic>0; maker_analog_pnl<=0
- KXBTCD-26JUL0717-T61999.99: side=YES surface=crypto_favorite_taker category=crypto status=RAW_ACTIONABLE_WATCH_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.97 bid=0.96 spread=0.01 passive=0.96 inside=false analog=category_side:MAKER_ANALOG_NO_GO resolved=399 pnl=-1212.58 toxic=176 blockers=execution_not_fresh; passive_inside_spread_unavailable; maker_analog_not_specific; maker_analog_no_go; maker_analog_toxic>0; maker_analog_pnl<=0
- KXBTCD-26JUL0717-T62249.99: side=YES surface=crypto_favorite_taker category=crypto status=RAW_ACTIONABLE_WATCH_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.96 bid=0.94 spread=0.02 passive=0.95 inside=true analog=exact:MAKER_ANALOG_REVIEW resolved=26 pnl=14.56 toxic=0 blockers=execution_not_fresh; maker_analog_underpowered:26<30
- KXBTCD-26JUL0717-T65249.99: side=NO surface=crypto_favorite_taker category=crypto status=RAW_ACTIONABLE_WATCH_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.97 bid=0.95 spread=0.02 passive=0.96 inside=true analog=category_side:MAKER_ANALOG_NO_GO resolved=432 pnl=-1577.75 toxic=217 blockers=execution_not_fresh; maker_analog_not_specific; maker_analog_no_go; maker_analog_toxic>0; maker_analog_pnl<=0
- KXETHD-26JUL0717-T1829.99: side=NO surface=crypto_favorite_taker category=crypto status=RAW_ACTIONABLE_WATCH_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.91 bid=0.90 spread=0.01 passive=0.90 inside=false analog=price:MAKER_ANALOG_NO_GO resolved=26 pnl=-6.81 toxic=3 blockers=execution_not_fresh; passive_inside_spread_unavailable; maker_analog_no_go; maker_analog_toxic>0; maker_analog_pnl<=0; maker_analog_resolved<30
- KXETHD-26JUL0717-T1869.99: side=NO surface=crypto_favorite_taker category=crypto status=RAW_ACTIONABLE_WATCH_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.98 bid=0.97 spread=0.01 passive=0.97 inside=false analog=category_side:MAKER_ANALOG_NO_GO resolved=432 pnl=-1577.75 toxic=217 blockers=execution_not_fresh; passive_inside_spread_unavailable; maker_analog_not_specific; maker_analog_no_go; maker_analog_toxic>0; maker_analog_pnl<=0
- KXSOLD-26JUL0717-T83.9999: side=NO surface=crypto_favorite_taker category=crypto status=RAW_ACTIONABLE_WATCH_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.92 bid=0.90 spread=0.02 passive=0.91 inside=true analog=exact:MAKER_ANALOG_REVIEW resolved=7 pnl=6.24 toxic=0 blockers=execution_not_fresh; maker_analog_underpowered:7<30
- KXHIGHCHI-26JUL07-T81: side=NO surface=weather_high_ask_no category=weather status=RAW_ACTIONABLE_WATCH_BLOCKED raw_actionable=true execution_ready=false strategy_ready=false ask=0.98 bid=0.97 spread=0.01 passive=0.97 inside=false analog=category_side:MAKER_ANALOG_NO_GO resolved=165 pnl=-133.80 toxic=31 blockers=execution_not_fresh; passive_inside_spread_unavailable; maker_analog_not_specific; maker_analog_no_go; maker_analog_toxic>0; maker_analog_pnl<=0

## Kalshi Quality-Aware WS Probe Plan
- command: `python3 scripts/kalshi_quality_ws_probe_runner.py --json --max-tickers 6 --max-per-surface 12`
- status: QUALITY_WS_PROBE_TARGETS_READY | mode=dry_run | selection_mode=quality_ranked | ready=false | live_ready=false | selected_tickers=6 | scope=read-only liquidity-aware execution-quality WS target selection
- pre_summary: raw_actionable=15 | raw_actionable_ws_ready=0 | inside_maker=16 | quality_ready=0
- clean_counts: raw_inside=4 | raw_inside_specific=3 | raw_inside_specific_positive=3 | clean_mm_probe=3 | clean_mm_probe_ws_ready=0
- selected_pre: raw_actionable=6 | inside_spread=4 | watch_plausible=3 | execution_ready=0 | clean_mm_probe=3
- KXBTCD-26JUL0717-T62249.99: side=YES surface=crypto_favorite_taker category=crypto ask=0.96 bid=0.94 spread=0.02 passive=0.95 inside=true analog=exact:MAKER_ANALOG_REVIEW resolved=26 pnl=14.56 toxic=0 rank=1 clean_mm_probe=true reasons=raw_actionable,inside_spread,specific_analog:exact,analog_zero_toxic,analog_positive_pnl
- KXSOLD-26JUL0717-T83.9999: side=NO surface=crypto_favorite_taker category=crypto ask=0.92 bid=0.90 spread=0.02 passive=0.91 inside=true analog=exact:MAKER_ANALOG_REVIEW resolved=7 pnl=6.24 toxic=0 rank=1 clean_mm_probe=true reasons=raw_actionable,inside_spread,specific_analog:exact,analog_zero_toxic,analog_positive_pnl
- KXHIGHMIA-26JUL07-B88.5: side=NO surface=weather_no_candidate category=weather ask=0.96 bid=0.94 spread=0.02 passive=0.95 inside=true analog=exact:MAKER_ANALOG_REVIEW resolved=11 pnl=6.16 toxic=0 rank=1 clean_mm_probe=true reasons=raw_actionable,inside_spread,specific_analog:exact,analog_zero_toxic,analog_positive_pnl
- KXBTCD-26JUL0717-T65249.99: side=NO surface=crypto_favorite_taker category=crypto ask=0.97 bid=0.95 spread=0.02 passive=0.96 inside=true analog=category_side:MAKER_ANALOG_NO_GO resolved=432 pnl=-1577.75 toxic=217 rank=4 clean_mm_probe=false reasons=raw_actionable,inside_spread
- KXETHD-26JUL0717-T1829.99: side=NO surface=crypto_favorite_taker category=crypto ask=0.91 bid=0.90 spread=0.01 passive=0.90 inside=false analog=price:MAKER_ANALOG_NO_GO resolved=26 pnl=-6.81 toxic=3 rank=3 clean_mm_probe=false reasons=raw_actionable,specific_analog:price
- KXHIGHTMIN-26JUL07-T86: side=NO surface=weather_no_candidate category=weather ask=0.95 bid=0.94 spread=0.01 passive=0.94 inside=false analog=price:MAKER_ANALOG_NO_GO resolved=46 pnl=-34.24 toxic=6 rank=3 clean_mm_probe=false reasons=raw_actionable,specific_analog:price

## Kalshi Clean-MM WS Probe Plan
- command: `python3 scripts/kalshi_quality_ws_probe_runner.py --json --max-tickers 6 --max-per-surface 12 --clean-only`
- status: QUALITY_WS_PROBE_TARGETS_READY | mode=dry_run | selection_mode=clean_mm_only | ready=false | live_ready=false | selected_tickers=3 | scope=read-only clean-MM execution-quality WS target selection
- pre_summary: raw_actionable=15 | raw_actionable_ws_ready=0 | inside_maker=16 | quality_ready=0
- clean_counts: raw_inside=4 | raw_inside_specific=3 | raw_inside_specific_positive=3 | clean_mm_probe=3 | clean_mm_probe_ws_ready=0
- selected_pre: raw_actionable=3 | inside_spread=3 | watch_plausible=3 | execution_ready=0 | clean_mm_probe=3
- KXBTCD-26JUL0717-T62249.99: side=YES surface=crypto_favorite_taker category=crypto ask=0.96 bid=0.94 spread=0.02 passive=0.95 inside=true analog=exact:MAKER_ANALOG_REVIEW resolved=26 pnl=14.56 toxic=0 rank=1 clean_mm_probe=true reasons=raw_actionable,inside_spread,specific_analog:exact,analog_zero_toxic,analog_positive_pnl
- KXSOLD-26JUL0717-T83.9999: side=NO surface=crypto_favorite_taker category=crypto ask=0.92 bid=0.90 spread=0.02 passive=0.91 inside=true analog=exact:MAKER_ANALOG_REVIEW resolved=7 pnl=6.24 toxic=0 rank=1 clean_mm_probe=true reasons=raw_actionable,inside_spread,specific_analog:exact,analog_zero_toxic,analog_positive_pnl
- KXHIGHMIA-26JUL07-B88.5: side=NO surface=weather_no_candidate category=weather ask=0.96 bid=0.94 spread=0.02 passive=0.95 inside=true analog=exact:MAKER_ANALOG_REVIEW resolved=11 pnl=6.16 toxic=0 rank=1 clean_mm_probe=true reasons=raw_actionable,inside_spread,specific_analog:exact,analog_zero_toxic,analog_positive_pnl

## Kalshi MM Near-Miss Adverse Selection
- command: `python3 scripts/kalshi_mm_near_miss_adverse_selection.py --json --near-miss-limit 4 --subcut-limit 3`
- status: MM_NEAR_MISS_ADVERSE_SELECTION_NO_GO | ready=false | live_ready=false | near_misses=4 | clean_current_subcuts=0 | shadow_rows=10956 | scope=read-only current MM near-miss adverse-selection explainer; no live authorization
- quality_summary: raw_actionable=15 | raw_actionable_ws_ready=0 | inside_maker=16 | quality_ready=0
- KXBTCD-26JUL0717-T65249.99: side=NO surface=crypto_favorite_taker category=crypto ask=0.97 bid=0.95 spread=0.02 analog=category_side:MAKER_ANALOG_NO_GO resolved=432 pnl=-1577.75 toxic=217 clean_subcuts=0 best_gate=CURRENT_SUBCUT_NO_GO best_filters=spread_band=<=2c best_resolved=99 best_pnl=4.03 best_toxic=11 best_blockers=toxic>0,wilson<=BE+buffer
- KXETHD-26JUL0717-T1829.99: side=NO surface=crypto_favorite_taker category=crypto ask=0.91 bid=0.90 spread=0.01 analog=price:MAKER_ANALOG_NO_GO resolved=26 pnl=-6.81 toxic=3 clean_subcuts=0 best_gate=CURRENT_SUBCUT_NO_GO best_filters=side_bid_band=90-92 best_resolved=31 best_pnl=-28.92 best_toxic=5 best_blockers=pnl<=0,toxic>0,wilson<=BE+buffer
- KXHIGHTMIN-26JUL07-T86: side=NO surface=weather_no_candidate category=weather ask=0.95 bid=0.94 spread=0.01 analog=price:MAKER_ANALOG_NO_GO resolved=46 pnl=-34.24 toxic=6 clean_subcuts=0 best_gate=CURRENT_SUBCUT_NO_GO best_filters=time_to_close_band=>24h best_resolved=154 best_pnl=-128.90 best_toxic=29 best_blockers=pnl<=0,toxic>0,wilson<=BE+buffer
- KXHIGHTOKC-26JUL07-T91: side=NO surface=weather_no_candidate category=weather ask=0.96 bid=0.95 spread=0.01 analog=price:MAKER_ANALOG_NO_GO resolved=46 pnl=-34.24 toxic=6 clean_subcuts=0 best_gate=CURRENT_SUBCUT_NO_GO best_filters=time_to_close_band=>24h best_resolved=154 best_pnl=-128.90 best_toxic=29 best_blockers=pnl<=0,toxic>0,wilson<=BE+buffer

## Kalshi Realtime/MM Infra Audit
- command: `python3 scripts/kalshi_realtime_mm_infra_audit.py --limit 6 --lookback-hours 24`
- status: same_strike=NO_CURRENT_EXECUTION_EDGE | maker_gate=NO_LIVE_MM_READY | ws_infra=WS_ORDERBOOK_VERIFIED | v3=NOT_INITIALIZED | live_ready=false | scope=read-only realtime execution/MM infrastructure audit
- same_strike_24h: observations=30242 | execution_ready=3620 | execution_ready_gross_positive=0 | qty10_positive=0 | max_gross_edge=0.0000 | max_qty10_net_edge=-0.0200
- maker_shadow: independent_resolved=2141 | wins=1354 | losses=787 | pnl=-5154.79 | toxic=787 | open_shadow_quotes=255
- websocket_latest: run=48 | captured_at=2026-07-07T12:01:34+00:00 | connected=true | tickers=2 | messages=75 | snapshots=2 | deltas=72 | latency_max_ms=30.370 | health_blockers=none
- live_maker_tables: kalshi_mve_locked_passive_maker_orders:exists=true rows=2 latest=2026-07-02T18:04:56+00:00 ; live_maker_orders:exists=true rows=1 latest=2026-07-02 18:04:56
- action: Keep same-strike complementarity in alert/telemetry mode; no current execution-ready positive edge.
- action: Do not run generic passive MM live; current maker shadow remains toxic or underpowered.
- action: Use Kalshi WebSocket orderbook telemetry as the realtime feed candidate; keep it read-only until strategy gates clear.
- action: Initialize V3 dry-run telemetry only after a fresh signal feed exists; current V3 tables are absent.

## Kalshi V3 Quote-Manager Dry-Run Gate
- command: `python3 scripts/kalshi_v3_quote_manager_dry_run_gate.py --json --limit 6`
- status: V3_QUOTE_MANAGER_DRY_RUN_BLOCKED | ready=false | live_ready=false | dry_run_targets=0 | live_promotion_candidates=0 | scope=read-only V3-style quote-manager dry-run gate; requires raw-actionable native signal, fresh per-ticker WS, inside-spread passive maker price, clean maker-shadow analog, post-only/cancel-replace controls, and first-fill review before any live promotion
- quality_summary: status=REALTIME_EXECUTION_NOT_FRESH_FOR_CANDIDATES | raw_actionable=15 | raw_actionable_ws_ready=0 | inside_maker=2 | clean_analog=0 | strategy_ready=0 | quality_ready=0
- controls: post_only=true | quote_qty=1 | max_open_quotes=1 | quote_ttl_s=60 | cancel_move_cents=2 | cancel_replace=book_move_or_ttl | first_fill_review_before_second_fill=true | no_live_orders=true
- blockers: eligible_runs<2:0=2; eligible_runs<2:1=1; maker_analog_gate_not_clean=6; maker_analog_not_specific=4; maker_analog_pnl<=0=5; maker_analog_resolved<30=2; maker_analog_toxic>0=5; maker_analog_wilson<=BE+buffer=6; no_eligible_runs=2; passive_inside_spread_unavailable=4; passive_price_not_inside_book=4; realtime_execution_not_fresh=6; run_age_s>180:1066.944=1; run_age_s>180:11883.983=1; run_age_s>180:7536.922=1; run_age_s>180:7536.972=1; spread<2c_for_inside_maker=4
- KXBTCD-26JUL0717-T60999.99: side=YES surface=crypto_favorite_taker category=crypto dry_run_ready=false live_promotion_ready=false ask=0.98 bid=0.97 spread=0.01 passive=0.97 post_only=true ttl_s=60 cancel_move_cents=2 analog=category_side:MAKER_ANALOG_NO_GO resolved=399 pnl=-1212.58 fill_rate=29.7% avg_adverse_move=0.1148 toxic=176 dry_blockers=realtime_execution_not_fresh; run_age_s>180:7536.922; passive_inside_spread_unavailable; spread<2c_for_inside_maker; passive_price_not_inside_book; maker_analog_not_specific; maker_analog_gate_not_clean; maker_analog_pnl<=0; maker_analog_toxic>0; maker_analog_wilson<=BE+buffer live_blockers=dry_run_not_ready; strategy_gate_no_live; execution_quality_not_ready; operator_review_required
- KXBTCD-26JUL0717-T61999.99: side=YES surface=crypto_favorite_taker category=crypto dry_run_ready=false live_promotion_ready=false ask=0.97 bid=0.96 spread=0.01 passive=0.96 post_only=true ttl_s=60 cancel_move_cents=2 analog=category_side:MAKER_ANALOG_NO_GO resolved=399 pnl=-1212.58 fill_rate=29.7% avg_adverse_move=0.1148 toxic=176 dry_blockers=realtime_execution_not_fresh; eligible_runs<2:1; run_age_s>180:1066.944; passive_inside_spread_unavailable; spread<2c_for_inside_maker; passive_price_not_inside_book; maker_analog_not_specific; maker_analog_gate_not_clean; maker_analog_pnl<=0; maker_analog_toxic>0; maker_analog_wilson<=BE+buffer live_blockers=dry_run_not_ready; strategy_gate_no_live; execution_quality_not_ready; operator_review_required
- KXBTCD-26JUL0717-T62249.99: side=YES surface=crypto_favorite_taker category=crypto dry_run_ready=false live_promotion_ready=false ask=0.96 bid=0.94 spread=0.02 passive=0.95 post_only=true ttl_s=60 cancel_move_cents=2 analog=exact:MAKER_ANALOG_REVIEW resolved=26 pnl=14.56 fill_rate=34.1% avg_adverse_move=0.0184 toxic=0 dry_blockers=realtime_execution_not_fresh; eligible_runs<2:0; no_eligible_runs; maker_analog_gate_not_clean; maker_analog_resolved<30; maker_analog_wilson<=BE+buffer live_blockers=dry_run_not_ready; strategy_gate_no_live; execution_quality_not_ready; operator_review_required
- KXBTCD-26JUL0717-T65249.99: side=NO surface=crypto_favorite_taker category=crypto dry_run_ready=false live_promotion_ready=false ask=0.97 bid=0.95 spread=0.02 passive=0.96 post_only=true ttl_s=60 cancel_move_cents=2 analog=category_side:MAKER_ANALOG_NO_GO resolved=432 pnl=-1577.75 fill_rate=30.4% avg_adverse_move=0.1188 toxic=217 dry_blockers=realtime_execution_not_fresh; eligible_runs<2:0; no_eligible_runs; maker_analog_not_specific; maker_analog_gate_not_clean; maker_analog_pnl<=0; maker_analog_toxic>0; maker_analog_wilson<=BE+buffer live_blockers=dry_run_not_ready; strategy_gate_no_live; execution_quality_not_ready; operator_review_required
- KXETHD-26JUL0717-T1829.99: side=NO surface=crypto_favorite_taker category=crypto dry_run_ready=false live_promotion_ready=false ask=0.91 bid=0.90 spread=0.01 passive=0.90 post_only=true ttl_s=60 cancel_move_cents=2 analog=price:MAKER_ANALOG_NO_GO resolved=26 pnl=-6.81 fill_rate=16.4% avg_adverse_move=0.0487 toxic=3 dry_blockers=realtime_execution_not_fresh; run_age_s>180:7536.972; passive_inside_spread_unavailable; spread<2c_for_inside_maker; passive_price_not_inside_book; maker_analog_gate_not_clean; maker_analog_resolved<30; maker_analog_pnl<=0; maker_analog_toxic>0; maker_analog_wilson<=BE+buffer live_blockers=dry_run_not_ready; strategy_gate_no_live; execution_quality_not_ready; operator_review_required
- KXETHD-26JUL0717-T1869.99: side=NO surface=crypto_favorite_taker category=crypto dry_run_ready=false live_promotion_ready=false ask=0.98 bid=0.97 spread=0.01 passive=0.97 post_only=true ttl_s=60 cancel_move_cents=2 analog=category_side:MAKER_ANALOG_NO_GO resolved=432 pnl=-1577.75 fill_rate=30.4% avg_adverse_move=0.1188 toxic=217 dry_blockers=realtime_execution_not_fresh; run_age_s>180:11883.983; passive_inside_spread_unavailable; spread<2c_for_inside_maker; passive_price_not_inside_book; maker_analog_not_specific; maker_analog_gate_not_clean; maker_analog_pnl<=0; maker_analog_toxic>0; maker_analog_wilson<=BE+buffer live_blockers=dry_run_not_ready; strategy_gate_no_live; execution_quality_not_ready; operator_review_required

## Kalshi Post-Expiration Active Scan
- command: `python3 scripts/kalshi_post_expiration_active_scanner.py --limit 1000 --max-pages 100 --pause-seconds 0.08 --min-age-minutes 1 --max-ask 0.25 --max-spread 0.20 --min-depth 1 --max-candidates 20 --record --json`
- latest_run: id=75 captured_at=2026-07-07T05:20:22+00:00 | markets_seen=40000 post_expiration_open_unresolved=1439 candidate_count=0 | direct_market_recheck=True pages=40 page_cap=True rate_limited=False | trigger_fields={"expected_expiration_time": 1439} | top_series=KXMVESPORTSMULTIGAMEEXTENDED=1108, KXMVECROSSCATEGORY=329, KXMLBTOTAL=2

## Kalshi Duplicate Proposition Scan
- command: `python3 scripts/kalshi_duplicate_proposition_scanner.py --series-title-regex '.' --max-series 100 --max-pages-per-series 1 --pause-seconds 0.05 --min-ask-gap 0.10 --min-bid-edge 0.05 --max-cheap-ask 0.75 --min-depth 1 --max-candidates 20 --record --json`
- latest_run: id=50 captured_at=2026-07-05T22:30:06+00:00 | mode=series_tickers series=80 offset=0 max_series=80 discovered_to_window_end=80 regex=0 prefix=12 markets_seen=1208 grouped_markets=1208 duplicate_groups=0 candidate_count=0 | pages=80 page_cap=false rate_limited=false | top_series=KXSOLE=200, KXWCGOAL=109, KXNASDAQ100U=100, KXMLBSPREAD=89, KXWCMATCHUP=62

## Kalshi Binary Complement Scan
- command: `python3 scripts/kalshi_binary_complement_scanner.py --series-title-regex '.' --max-series 100 --max-pages-per-series 1 --pause-seconds 0.05 --min-net-edge 0.005 --min-depth 1 --record --json`
- latest_run: id=56 captured_at=2026-07-05T22:24:26+00:00 | mode=global_open_cursor markets=100000 parsed=0 groups=0 relations=0 candidates=0 | pages=100 page_cap=true rate_limited=false | top_series=KXMVESPORTSMULTIGAMEEXTENDED=83775, KXMVECROSSCATEGORY=16205, KXWTACHALLENGERMATCH=10, KXATPGTOTAL=3, KXATPCHALLENGERMATCH=2 | parse_rejects=not_strict_binary_labels=100000

## Kalshi Date-Threshold Ladder Scan
- command: `python3 scripts/kalshi_date_threshold_ladder_scanner.py --limit 1000 --max-pages 120 --pause-seconds 0.05 --record --json`
- latest_run: captured_at=2026-07-05T21:25:01+00:00 | mode=whole_universe markets_seen=21000 parsed_markets=0 parsed_events=0 groups=0 orderbooks=0 candidates=0 best_edge=none | pages=21 page_cap=false rate_limited=true | top_series=KXMVESPORTSMULTIGAMEEXTENDED=17095, KXMVECROSSCATEGORY=3819, KXMLBHRR=46, KXMLBRBI=26, KXMLBSB=11

## Kalshi Series Ladder Dominance Scan
- command: `python3 scripts/kalshi_series_ladder_dominance_scanner.py --series-title-regex '<scalar ladder terms>' --max-series 50 --max-pages-per-series 1 --pause-seconds 0.05 --record`
- latest_run: id=56 captured_at=2026-07-05T01:26:03+00:00 | mode=whole_universe markets=5000 parsed=73 families=73 multi_row=0 relations=0 candidates=0 top_net=none | pages=5 page_cap=true rate_limited=false

## Kalshi Interval Partition Scan
- command: `python3 scripts/kalshi_interval_partition_scanner.py --series-title-regex '<numeric/interval terms>' --max-series 50 --max-pages-per-series 1 --pause-seconds 0.05 --record`
- latest_run: id=54 captured_at=2026-07-05T22:31:24+00:00 | mode=series_tickers series=80 offset=0 max_series=80 discovered_to_window_end=80 regex=0 prefix=12 markets=1552 parsed=592 groups=45 partitions=0/37 candidates=0 | pages=79 page_cap=false rate_limited=true | top_series=KXMLBTB=466, KXSOLD=200, KXMLBKS=111, KXNASDAQ100U=100, KXMLBDRAFTTOP=90 | non_partition=gap_between_intervals=22, missing_lower_tail=14, missing_upper_tail=1

## Kalshi Interval Relation Scan
- command: `python3 scripts/kalshi_interval_relation_scanner.py --series-title-regex '<numeric/interval terms>' --max-series 50 --max-pages-per-series 1 --pause-seconds 0.05 --record`
- latest_run: id=42 captured_at=2026-07-05T22:24:53+00:00 | mode=global_open_cursor markets=25000 parsed=13422 groups=12350 relations=0 candidates=0 | pages=25 page_cap=true rate_limited=false | top_series=KXMVESPORTSMULTIGAMEEXTENDED=20920, KXMVECROSSCATEGORY=4079, KXMLBSPREAD=1 | parse_rejects=not_interval_title=11578

## Kalshi Threshold Complement Scan
- command: `python3 scripts/kalshi_threshold_complement_scanner.py --series-title-regex '<numeric/interval terms>' --max-series 50 --max-pages-per-series 1 --pause-seconds 0.05 --record`
- latest_run: id=65 captured_at=2026-07-05T22:29:51+00:00 | mode=series_tickers series=80 offset=0 max_series=80 discovered_to_window_end=80 regex=0 prefix=12 markets=1316 parsed=66 groups=24 relations=19 candidates=0 | pages=80 page_cap=false rate_limited=false | top_series=KXMLBHR=223, KXETH=165, KXMLBTOTAL=147, KXMLBKS=111, KXMLBALLSTAR=95 | parse_rejects=not_single_threshold_title=1250

## Kalshi Post-Close Active Scan
- command: `python3 scripts/kalshi_post_close_active_scanner.py --limit 1000 --max-pages 100 --pause-seconds 0.05 --min-age-minutes 1 --max-ask 0.25 --max-spread 0.15 --min-depth 1 --max-candidates 20 --record`
- latest_run: id=55 captured_at=2026-07-07T00:27:07+00:00 | markets_seen=100000 post_close_open_unresolved=0 candidates=0 min_age_min=1.00 max_ask=0.30 max_spread=0.15 min_depth=1 | pages=100 page_cap=true rate_limited=false | categories=none | top_series=unknown

## Kalshi Public Result Active Scan
- command: `python3 scripts/kalshi_public_result_active_scanner.py --limit 1000 --max-pages 100 --pause-seconds 0.05 --max-ask 0.25 --max-spread 0.15 --min-depth 1 --max-candidates 20 --record`
- latest_run: id=79 captured_at=2026-07-07T05:17:57+00:00 | markets_seen=40000 public_result_active=0 candidates=0 max_ask=0.99 max_spread=0.05 min_depth=1 | pages=40 page_cap=true rate_limited=false | results=none | categories=none | top_series=unknown

## Kalshi Event Result Propagation Scan
- command: `python3 scripts/kalshi_event_result_propagation_scanner.py --limit 200 --max-pages 35 --max-details 1000 --pause-seconds 0.03 --max-ask 0.25 --min-depth 1 --print-limit 20`
- latest_run: id=47 captured_at=2026-07-07T03:20:34+00:00 | version=event_result_propagation_v1 events_seen=7143 events_examined=6172 mutex_events=2501 details=2500/2500 detail_cap=true markets=26992 locked=0 actionable_qty1=0 max_ask=0.25 min_depth=1 | pages=36 page_cap=false rate_limited=false | reasons=event_not_mutually_exclusive_summary=3671, no_exhaustive_proof=2497, exhaustive_active_count_not_one=3, detail_cap_reached=1

## Kalshi Event Mutex Bundle Scan
- command: `python3 scripts/kalshi_event_mutex_bundle_scanner.py --event-limit 200 --max-event-pages 80 --max-details 1000 --pause-seconds 0.03 --detail-pause-seconds 0.03 --min-net-edge 0.01 --record`
- latest_run: id=56 captured_at=2026-07-07T00:29:21+00:00 | events_seen=4000 mutex_events=1508 details=200/200 markets=1861 tradable_no=1283 candidates=0 top_net=-3.0pp | pages=20 page_cap=true rate_limited=false | categories=Elections=1022, Sports=327, Entertainment=40, Economics=34, Politics=34, Financials=28 | detail_errors=none
- nearest_no_bundles: GOVPARTYMT-28 GOVPARTYMT k=2 floor=1.00 cost=1.01 fees=0.02 net=-3.0pp tickers=GOVPARTYMT-28-R,GOVPARTYMT-28-D ; GOVPARTYMO-28 GOVPARTYMO k=2 floor=1.00 cost=1.01 fees=0.02 net=-3.4pp tickers=GOVPARTYMO-28-R,GOVPARTYMO-28-D ; KXNEXTUKPM-30 KXNEXTUKPM k=2 floor=1.00 cost=1.01 fees=0.02 net=-3.5pp tickers=KXNEXTUKPM-30-ABUR,KXNEXTUKPM-30-EMIL ; KXG7LEADEROUT-45JAN01 KXG7LEADEROUT k=2 floor=1.00 cost=1.02 fees=0.02 net=-3.6pp tickers=KXG7LEADEROUT-45JAN01-KSTA,KXG7LEADEROUT-45JAN01-EMAC ; KXCAGOVLAMAYOR-26NOV KXCAGOVLAMAYOR k=4 floor=3.00 cost=2.98 fees=0.06 net=-4.0pp tickers=KXCAGOVLAMAYOR-26NOV-BAS-BEC,KXCAGOVLAMAYOR-26NOV-RAM-BEC,KXCAGOVLAMAYOR-26NOV-BAS-HIL
- unsafe_all_yes_positive_requires_exhaustive_validation: count=12 best_net=+72.3pp

## Kalshi Exhaustive YES Basket Audit
- command: `PYTHONPATH=scripts python3 scripts/kalshi_event_exhaustive_yes_audit.py --event-limit 300 --max-event-pages 6 --pause-seconds 0.08 --detail-pause-seconds 0.08 --min-net-edge 0.005 --print-limit 20 --record`
- latest_run: id=41 captured_at=2026-07-07T01:21:42+00:00 | version=event_exhaustive_yes_v2_esports events_seen=452 event_details=452 baskets_checked=396 actionable_qty1=0 min_net_edge=0.000 | series=14 page_limits=[200] | counts=KXATPCHALLENGERMATCH=63, KXITFMATCH=106, KXITFWMATCH=95, KXLOLGAME=27, KXLOLMAP=26, KXMLBGAME=48, KXNBAGAME=0, KXNHLGAME=0 | reasons=exhaustive_basket_checked=396, two_way_sports_shape_mismatch=53, event_not_mutually_exclusive=2, two_way_no_tie_match_shape_mismatch=1
- nearest_baskets: KXVALORANTGAME-26JUL071330PLTSE two_way_no_tie_sports_match contracts=2 sum_asks=0.980 fees=0.040 net=-0.020 depth=1 actionable=0 ; KXATPCHALLENGERMATCH-26JUL07HUADEN two_way_no_tie_sports_match contracts=2 sum_asks=1.000 fees=0.020 net=-0.020 depth=4 actionable=0 ; KXATPCHALLENGERMATCH-26JUL07ZHOCAT two_way_no_tie_sports_match contracts=2 sum_asks=1.000 fees=0.020 net=-0.020 depth=1000 actionable=0 ; KXITFMATCH-26JUL07TALPIE two_way_no_tie_sports_match contracts=2 sum_asks=0.990 fees=0.040 net=-0.030 depth=396 actionable=0 ; KXITFMATCH-26JUL07BOUMOC two_way_no_tie_sports_match contracts=2 sum_asks=0.990 fees=0.040 net=-0.030 depth=499 actionable=0

## Kalshi Crypto NO <10c Gate Check
- command: `python3 scripts/kalshi_crypto_no_lt10c_gate_check.py --json`
- status: NOT_READY | ready=false
- broad_pilot_note: old_strategy=kalshi_crypto_no_lt10c_first_eligible_pilot kill=present | active_live_path=kalshi_crypto_no_lt10c_non04z_first_eligible_forward_pilot kill=present
- reasons: resolved 20/50; wilson 58.4% < 90.0%; open_filled_trades=5; source reconciliation mismatches 51; native taker NO ask <10c evidence absent
- resolved: 20/50 | 16W-4L | pnl=+15.07 | wilson=58.4%
- pending: 0 markets | max_if_pending=20/50 | need_new_after_pending=30
- risk: open_filled=5 | sports_open=0 | live_maker_open_like=0
- source_reconciliation: checked=20/20 | mismatches=51 | native_taker_ask_lt10c=0/16
- candidate_preview: available=false | pending_first_eligible=0 | shadow_live_actionable=0 | native_taker_actionable=0 | native_taker_blocked=0 | settlement_pending_or_ineligible=0 | expired_unresolved=0 | reason=no unresolved first-eligible <10c candidate remains before settlement
- fresh_non04z_review: status=NOT_READY | ready=false | reason=fresh gate status ACCUMULATING; resolved 16/50; wilson 44.4% < 90.0%; open_filled_trades=5; source reconciliation mismatches 46; native taker NO ask <10c evidence absent | resolved=16/50 | 11W-5L | pnl=+10.42 | wilson=44.4% | pending=0 | shadow_live_actionable=0 | native_taker_actionable=0 | native_taker_blocked=0 | expired_unresolved=0 | next_backfill_after=unknown | source_reconciliation=16/16 mismatches=46 | native_taker_ask_lt10c=0/11
- pilot_launcher: script=scripts/kalshi_crypto_no_lt10c_pilot.py | strategy=kalshi_crypto_no_lt10c_first_eligible_pilot | tracking_rows=0 | live_placed_rows=0 | pilot_kill=present | first_live_review_ack=absent | execute_blocked_rows=0 | dry_run_ready_rows=0 | latest=none
- first_live_verifier: status=WAITING_FOR_FIRST_LIVE_ROW | ok=true | placed_tracking_rows=0 | errors=none
- non04z_pilot_launcher: script=scripts/kalshi_crypto_no_lt10c_non04z_pilot.py | strategy=kalshi_crypto_no_lt10c_non04z_first_eligible_forward_pilot | tracking_rows=1 | live_placed_rows=0 | pilot_kill=present | first_live_review_ack=absent | execute_blocked_rows=1 | dry_run_ready_rows=0 | latest=2026-06-25 17:34:38 KXBTCD-26JUN2514-T60199.99 dry_run=0 status=BLOCKED
- non04z_first_live_verifier: status=WAITING_FOR_FIRST_LIVE_ROW | ok=true | placed_tracking_rows=0 | errors=none

## Kalshi Native Forward Gate Leaderboard
- command: `python3 scripts/kalshi_native_forward_leaderboard.py --json`
- status: NO_LIVE_READY | ready=false | cells=9 | ready_cells=0 | min_resolved=30 | edge_buffer=+2.0pp | pending=43 active=43 stale=0 unknown=0 | next_pending=crypto_last_hour_longshot_no:KXBTCD-26JUL0709-T63699.99 status=active due=2026-07-07T12:59:59.188159+00:00
- best: crypto_last_hour_longshot_no | gate=NATIVE_FORWARD_ACCUMULATING | native_events=437 resolved=435 pending=2 active=2 stale=0 unknown=0 | 394W-41L | pnl=-0.28 | Wilson 87.5% vs BE 90.6% | gap=-3.1pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=309 | next_pending=KXBTCD-26JUL0709-T63699.99 status=active due=2026-07-07T12:59:59.188159+00:00 ask=0.80
- rank 1: crypto_last_hour_longshot_no | gate=NATIVE_FORWARD_ACCUMULATING | native_events=437 resolved=435 pending=2 active=2 stale=0 unknown=0 | 394W-41L | pnl=-0.28 | Wilson 87.5% vs BE 90.6% | gap=-3.1pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=309 | next_pending=KXBTCD-26JUL0709-T63699.99 status=active due=2026-07-07T12:59:59.188159+00:00 ask=0.80
- rank 2: weather_no_candidate:no_95_98_zero_loss_cities_v1 | gate=NATIVE_FORWARD_ACCUMULATING | native_events=92 resolved=84 pending=8 active=8 stale=0 unknown=0 | 82W-2L | pnl=+0.06 | Wilson 91.7% vs BE 97.5% | gap=-5.8pp | blockers=wilson<BE+2pp | perfect_wins_needed=1371 | next_pending=KXLOWTMIA-26JUL06-B75.5 status=active due=2026-07-07T19:00:00+00:00 ask=0.96
- rank 3: crypto_favorite_taker:crypto_near_certain_95_99_12_24h | gate=NATIVE_FORWARD_ACCUMULATING | native_events=54 resolved=46 pending=8 active=8 stale=0 unknown=0 | 45W-1L | pnl=+0.10 | Wilson 88.7% vs BE 97.5% | gap=-8.8pp | blockers=wilson<BE+2pp | perfect_wins_needed=1005 | next_pending=KXETHD-26JUL0717-T1869.99 status=active due=2026-07-07T20:59:59.207141+00:00 ask=0.95
- rank 4: weather_high_ask_no | gate=NATIVE_FORWARD_ACCUMULATING | native_events=92 resolved=76 pending=16 active=16 stale=0 unknown=0 | 73W-3L | pnl=-2.24 | Wilson 89.0% vs BE 99.0% | gap=-10.0pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=>5000_or_target_impossible | next_pending=KXLOWTPHIL-26JUL06-T64 status=active due=2026-07-07T19:00:00+00:00 ask=0.98
- rank 5: weather_yes_90_93:yes_90_93_above_live_threshold_v1 | gate=NATIVE_FORWARD_ACCUMULATING | native_events=35 resolved=35 pending=0 active=0 stale=0 unknown=0 | 32W-3L | pnl=-0.32 | Wilson 77.6% vs BE 92.3% | gap=-14.7pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=117
- rank 6: other_longshot_no_80_90:other_weak_no_80_90_4_24h_v1 | gate=NATIVE_FORWARD_ACCUMULATING | native_events=8 resolved=8 pending=0 active=0 stale=0 unknown=0 | 8W-0L | pnl=+1.05 | Wilson 67.6% vs BE 86.9% | gap=-19.3pp | blockers=resolved<30; wilson<BE+2pp | perfect_wins_needed=23

## Kalshi Native Preflight Cut Miner
- command: `python3 scripts/kalshi_native_preflight_cut_miner.py --limit 8`
- status: NO_NATIVE_CUT_READY | ready=false | observations=22131 | cuts=2481 | display_cuts=677 | candidate_cuts=0 | ready_cuts=0 | min_resolved=30 | min_display_resolved=10 | edge_buffer=+2.0pp | scope=posthoc_native_executable_cut_discovery_requires_predeclared_forward_gate
- best: crypto_last_hour_longshot_no|minutes_to_expiry_band=20-40m|native_ask_band=80-85 | gate=NATIVE_CUT_ACCUMULATING | type=pair | observations=76 resolved=76 pending=0 active=0 stale=0 unknown=0 | 71W-5L | pnl=+$7.21 | Wilson 85.5% vs target 85.9% (BE 83.9%) | gap=-0.4pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=3
- rank 1: crypto_last_hour_longshot_no|minutes_to_expiry_band=20-40m|native_ask_band=80-85 | gate=NATIVE_CUT_ACCUMULATING | type=pair | observations=76 resolved=76 pending=0 active=0 stale=0 unknown=0 | 71W-5L | pnl=+$7.21 | Wilson 85.5% vs target 85.9% (BE 83.9%) | gap=-0.4pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=3
- rank 2: crypto_last_hour_longshot_no|captured_weekday=Tue | gate=NATIVE_CUT_ACCUMULATING | type=single | observations=73 resolved=71 pending=2 active=2 stale=0 unknown=0 | 70W-1L | pnl=+$4.95 | Wilson 92.4% vs target 93.4% (BE 91.4%) | gap=-1.0pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=11 | next_pending=KXBTCD-26JUL0709-T63699.99 status=active due=2026-07-07T12:59:59.188159+00:00 ask=0.80
- rank 3: crypto_last_hour_longshot_no|shadow_entry_band=80-85 | gate=NATIVE_CUT_ACCUMULATING | type=single | observations=62 resolved=62 pending=0 active=0 stale=0 unknown=0 | 59W-3L | pnl=+$5.25 | Wilson 86.7% vs target 88.7% (BE 86.7%) | gap=-2.0pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=12
- rank 4: crypto_last_hour_longshot_no|signal_tier=moderate|native_ask_band=90-95 | gate=NATIVE_CUT_ACCUMULATING | type=pair | observations=112 resolved=112 pending=0 active=0 stale=0 unknown=0 | 109W-3L | pnl=+$5.25 | Wilson 92.4% vs target 94.6% (BE 92.6%) | gap=-2.2pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=49
- rank 5: crypto_last_hour_longshot_no|native_spread_band=<=1c|native_depth_band=10-99 | gate=NATIVE_CUT_ACCUMULATING | type=pair | observations=120 resolved=120 pending=0 active=0 stale=0 unknown=0 | 114W-6L | pnl=+$5.90 | Wilson 89.5% vs target 92.1% (BE 90.1%) | gap=-2.6pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=41
- rank 6: crypto_last_hour_longshot_no|native_ask_band=85-90 | gate=NATIVE_CUT_ACCUMULATING | type=single | observations=250 resolved=250 pending=0 active=0 stale=0 unknown=0 | 227W-23L | pnl=+$6.30 | Wilson 86.6% vs target 90.3% (BE 88.3%) | gap=-3.7pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=99
- rank 7: crypto_last_hour_longshot_no|shadow_spread_band=<=1c | gate=NATIVE_CUT_ACCUMULATING | type=single | observations=296 resolved=295 pending=1 active=1 stale=0 unknown=0 | 274W-21L | pnl=+$5.06 | Wilson 89.4% vs target 93.1% (BE 91.1%) | gap=-3.8pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=167 | next_pending=KXETHD-26JUL0709-T1789.99 status=active due=2026-07-07T12:59:59.553643+00:00 ask=0.84
- rank 8: crypto_last_hour_longshot_no|native_spread_band=<=1c | gate=NATIVE_CUT_ACCUMULATING | type=single | observations=368 resolved=367 pending=1 active=1 stale=0 unknown=0 | 338W-29L | pnl=+$4.33 | Wilson 88.9% vs target 92.9% (BE 90.9%) | gap=-4.0pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=212 | next_pending=KXBTCD-26JUL0709-T63699.99 status=active due=2026-07-07T12:59:59.188159+00:00 ask=0.80

## Kalshi Native Forward Watchlist
- command: `python3 scripts/kalshi_native_forward_watchlist.py --limit 13`
- status: NO_FORWARD_WATCH_READY | ready=false | watches=13 | ready_watches=0 | min_resolved=30 | edge_buffer=+2.0pp | scope=predeclared_forward_only_after_posthoc_cut_discovery
- best: native_watch|crypto_spread_le1_depth_100_999 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-07-01T11:00:00+00:00 | observations=131 resolved=130 pending=1 active=1 stale=0 unknown=0 | 117W-13L | pnl=$-1.14 | Wilson 83.6% vs target 92.9% (BE 90.9%) | gap=-9.2pp | blockers=pnl<=0;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=177 | next_pending=KXBTCD-26JUL0709-T63699.99 status=active due=2026-07-07T12:59:59.188159+00:00 ask=0.80 | excluded_post_start_actionables=685 (native_spread_band=<=5c=241, native_depth_band=1000+=182, native_spread_band=<=2c=154, native_depth_band=10-99=80) | excluded_sample=KXBTCD-26JUL0108-T58799.99 native_depth_band=10-99 ask=0.85 | target_window_misses=298 (not_actionable=298) | target_window_sample=KXBTCD-26JUL0108-T58799.99 not_actionable ask=0.99
- rank 1: native_watch|crypto_spread_le1_depth_100_999 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-07-01T11:00:00+00:00 | observations=131 resolved=130 pending=1 active=1 stale=0 unknown=0 | 117W-13L | pnl=$-1.14 | Wilson 83.6% vs target 92.9% (BE 90.9%) | gap=-9.2pp | blockers=pnl<=0;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=177 | next_pending=KXBTCD-26JUL0709-T63699.99 status=active due=2026-07-07T12:59:59.188159+00:00 ask=0.80 | excluded_post_start_actionables=685 (native_spread_band=<=5c=241, native_depth_band=1000+=182, native_spread_band=<=2c=154, native_depth_band=10-99=80) | excluded_sample=KXBTCD-26JUL0108-T58799.99 native_depth_band=10-99 ask=0.85 | target_window_misses=298 (not_actionable=298) | target_window_sample=KXBTCD-26JUL0108-T58799.99 not_actionable ask=0.99
- rank 2: native_watch|crypto_strong_no_90_95 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-07-01T11:00:00+00:00 | observations=73 resolved=73 pending=0 active=0 stale=0 unknown=0 | 64W-9L | pnl=$-4.27 | Wilson 78.2% vs target 95.5% (BE 93.5%) | gap=-17.3pp | blockers=pnl<=0;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=304 | excluded_post_start_actionables=855 (signal_tier=moderate=348, signal_tier=weak=341, native_ask_band=85-90=75, native_ask_band=95-98=56) | excluded_sample=KXBTCD-26JUL0108-T58799.99 native_ask_band=85-90 ask=0.89 | target_window_misses=1081 (not_actionable_native_ask_band=missing=361, not_actionable_native_ask_band=99+=147, not_actionable_native_ask_band=98-99=138, not_actionable_native_ask_band=<80=134) | target_window_sample=KXBTCD-26JUL0108-T58799.99 native_ask_band=85-90 ask=0.89
- rank 3: native_watch|crypto_btc_no_85_90 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-06-30T07:13:19+00:00 | observations=59 resolved=59 pending=0 active=0 stale=0 unknown=0 | 49W-10L | pnl=$-3.07 | Wilson 71.5% vs target 90.3% (BE 88.3%) | gap=-18.7pp | blockers=pnl<=0;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=125 | excluded_post_start_actionables=1155 (asset=ETH=344, asset=SOL=334, native_ask_band=90-95=317, native_ask_band=95-98=82) | excluded_sample=KXBTCD-26JUN3005-T59699.99 native_ask_band=90-95 ask=0.94 | target_window_misses=1921 (not_actionable_native_ask_band=missing=657, native_ask_band=90-95=317, not_actionable_native_ask_band=98-99=212, not_actionable_native_ask_band=<80=201) | target_window_sample=KXBTCD-26JUN3004-T59799.99 not_actionable_native_ask_band=98-99 ask=0.98
- rank 4: native_watch|crypto_spread_le1_depth_10_99 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-07-01T07:10:00+00:00 | observations=57 resolved=57 pending=0 active=0 stale=0 unknown=0 | 52W-5L | pnl=$+0.65 | Wilson 81.1% vs target 92.1% (BE 90.1%) | gap=-11.0pp | blockers=wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=87 | excluded_post_start_actionables=984 (native_depth_band=100-999=374, native_spread_band=<=5c=243, native_depth_band=1000+=183, native_spread_band=<=2c=156) | excluded_sample=KXBTCD-26JUL0104-T58899.99 native_depth_band=100-999 ask=0.93 | target_window_misses=92 (not_actionable=92) | target_window_sample=KXSOLD-26JUL0107-T75.9999 not_actionable ask=0.99
- rank 5: native_watch|crypto_20_40m_no_80_85 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-06-29T11:05:00+00:00 | observations=46 resolved=46 pending=0 active=0 stale=0 unknown=0 | 42W-4L | pnl=$+3.33 | Wilson 79.7% vs target 86.1% (BE 84.1%) | gap=-6.4pp | blockers=wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=24 | excluded_post_start_actionables=1437 (minutes_band=40-60m=827, native_ask_band=90-95=245, native_ask_band=85-90=127, minutes_band=10-20m=122) | excluded_sample=KXBTCD-26JUN2908-T60299.99 minutes_band=40-60m ask=0.95 | target_window_misses=1719 (not_actionable_native_ask_band=missing=302, not_actionable_native_ask_band=98-99=266, not_actionable_native_ask_band=99+=249, native_ask_band=90-95=245) | target_window_sample=KXBTCD-26JUN2908-T60299.99 not_actionable_native_ask_band=98-99 ask=0.98
- rank 6: native_watch|crypto_sol_no_85_90 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-07-01T13:00:00+00:00 | observations=33 resolved=33 pending=0 active=0 stale=0 unknown=0 | 29W-4L | pnl=$-0.18 | Wilson 72.7% vs target 90.4% (BE 88.4%) | gap=-17.8pp | blockers=pnl<=0;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=70 | excluded_post_start_actionables=944 (asset=BTC=521, asset=ETH=257, native_ask_band=90-95=99, native_ask_band=80-85=39) | excluded_sample=KXBTCD-26JUL0110-T59199.99 asset=BTC ask=0.93 | target_window_misses=610 (not_actionable_native_ask_band=missing=124, native_ask_band=90-95=99, not_actionable_native_ask_band=99+=98, not_actionable_native_ask_band=<80=91) | target_window_sample=KXSOLD-26JUL0111-T79.9999 not_actionable_native_ask_band=missing
- rank 7: native_watch|crypto_btc_strong_no_90_95_spread_le1_depth_100_999 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-07-01T14:00:00+00:00 | observations=27 resolved=27 pending=0 active=0 stale=0 unknown=0 | 25W-2L | pnl=$-0.22 | Wilson 76.6% vs target 95.4% (BE 93.4%) | gap=-18.8pp | blockers=resolved<30;pnl<=0;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=128 | excluded_post_start_actionables=955 (asset=ETH=257, asset=SOL=241, signal_tier=moderate=188, signal_tier=weak=95) | excluded_sample=KXETHD-26JUL0111-T1609.99 asset=ETH ask=0.90 | target_window_misses=157 (not_actionable_native_ask_band=95-98=37, not_actionable_native_ask_band=99+=28, not_actionable_native_ask_band=<80=26, native_ask_band=85-90=25) | target_window_sample=KXBTCD-26JUL0112-T60099.99 native_ask_band=85-90 ask=0.89
- rank 8: native_watch|crypto_tue_no_any_ask | gate=FORWARD_WATCH_ACCUMULATING | start=2026-07-01T07:10:00+00:00 | observations=21 resolved=19 pending=2 active=2 stale=0 unknown=0 | 18W-1L | pnl=$+0.41 | Wilson 75.4% vs target 94.6% (BE 92.6%) | gap=-19.2pp | blockers=resolved<30;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=82 | next_pending=KXBTCD-26JUL0709-T63699.99 status=active due=2026-07-07T12:59:59.188159+00:00 ask=0.80 | excluded_post_start_actionables=989 (captured_weekday=Sat=305, captured_weekday=Sun=197, captured_weekday=Fri=180, captured_weekday=Thu=165) | excluded_sample=KXBTCD-26JUL0104-T58899.99 captured_weekday=Wed ask=0.93 | target_window_misses=213 (not_actionable=213) | target_window_sample=KXETHD-26JUL0621-T1809.99 not_actionable ask=0.96
- rank 9: native_watch|crypto_shadow_spread_le1 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-07-07T10:00:00+00:00 | observations=4 resolved=3 pending=1 active=1 stale=0 unknown=0 | 3W-0L | pnl=$+0.31 | Wilson 43.8% vs target 91.7% (BE 89.7%) | gap=-47.8pp | blockers=resolved<30;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=40 | next_pending=KXETHD-26JUL0709-T1789.99 status=active due=2026-07-07T12:59:59.553643+00:00 ask=0.84 | excluded_post_start_actionables=1 (shadow_spread_band=<=2c=1) | excluded_sample=KXBTCD-26JUL0709-T63699.99 shadow_spread_band=<=2c ask=0.80 | target_window_misses=26 (not_actionable=26) | target_window_sample=KXETHD-26JUL0707-T1789.99 not_actionable ask=0.93
- rank 10: native_watch|crypto_no_85_90 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-07-07T10:00:00+00:00 | observations=2 resolved=2 pending=0 active=0 stale=0 unknown=0 | 2W-0L | pnl=$+0.20 | Wilson 34.2% vs target 92.0% (BE 90.0%) | gap=-57.8pp | blockers=resolved<30;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=43 | excluded_post_start_actionables=10 (native_ask_band=90-95=5, native_ask_band=80-85=4, native_ask_band=95-98=1) | excluded_sample=KXBTCD-26JUL0707-T63499.99 native_ask_band=80-85 ask=0.81 | target_window_misses=38 (not_actionable_native_ask_band=missing=11, not_actionable_native_ask_band=<80=7, not_actionable_native_ask_band=98-99=6, native_ask_band=90-95=5) | target_window_sample=KXETHD-26JUL0707-T1789.99 not_actionable_native_ask_band=90-95 ask=0.93
- rank 11: native_watch|crypto_depth_10_99 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-07-07T10:00:00+00:00 | observations=2 resolved=1 pending=1 active=1 stale=0 unknown=0 | 1W-0L | pnl=$+0.08 | Wilson 20.7% vs target 94.0% (BE 92.0%) | gap=-73.3pp | blockers=resolved<30;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=60 | next_pending=KXETHD-26JUL0709-T1789.99 status=active due=2026-07-07T12:59:59.553643+00:00 ask=0.84 | excluded_post_start_actionables=9 (native_depth_band=100-999=6, native_depth_band=<10=2, native_depth_band=1000+=1) | excluded_sample=KXETHD-26JUL0707-T1789.99 native_depth_band=100-999 ask=0.89
- rank 12: native_watch|crypto_moderate_no_90_95 | gate=FORWARD_WATCH_ACCUMULATING | start=2026-07-07T10:00:00+00:00 | observations=1 resolved=1 pending=0 active=0 stale=0 unknown=0 | 1W-0L | pnl=$+0.06 | Wilson 20.7% vs target 96.0% (BE 94.0%) | gap=-75.3pp | blockers=resolved<30;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=92 | excluded_post_start_actionables=9 (signal_tier=strong=8, native_ask_band=85-90=1) | excluded_sample=KXETHD-26JUL0707-T1789.99 native_ask_band=85-90 ask=0.89 | target_window_misses=9 (not_actionable_native_ask_band=missing=6, native_ask_band=85-90=1, not_actionable=1, not_actionable_native_ask_band=98-99=1) | target_window_sample=KXETHD-26JUL0707-T1789.99 not_actionable ask=0.93
- rank 13: native_watch|crypto_shadow_entry_80_85 | gate=FORWARD_WATCH_WAITING | start=2026-07-07T10:00:00+00:00 | observations=0 resolved=0 pending=0 active=0 stale=0 unknown=0 | 0W-0L | pnl=$+0.00 | Wilson 0.0% vs target 2.0% (BE 0.0%) | gap=-2.0pp | blockers=no_forward_observations;resolved<30;wilson<BE+buffer | promotion_blockers=predeclared_forward_only_until_gate_ready | perfect_wins_needed=>5000_or_target_impossible | excluded_post_start_actionables=12 (shadow_entry_band=90-95=8, shadow_entry_band=85-90=4) | excluded_sample=KXETHD-26JUL0707-T1789.99 shadow_entry_band=85-90 ask=0.89

## Kalshi Native Cut Promotion Bridge
- command: `python3 scripts/kalshi_native_cut_promotion_bridge.py --json --limit 6`
- status: NATIVE_PROMOTION_BLOCKED | ready=false | live_ready=false | posthoc_cuts=6 | equivalent_watch_rows=6 | promotion_review_rows=0 | scope=read-only posthoc-native-cut to predeclared-forward-watch promotion bridge; no live authorization
- source_status: cuts=NO_NATIVE_CUT_READY | watches=NO_FORWARD_WATCH_READY
- crypto_last_hour_longshot_no|minutes_to_expiry_band=20-40m|native_ask_band=80-85 | bridge_gate=NATIVE_PROMOTION_BLOCKED | cut_gate=NATIVE_CUT_ACCUMULATING | cut=71W-5L resolved=76 pnl=+7.21 gap=-0.4pp perfect_wins_needed=3 | watch=equivalent:native_watch|crypto_20_40m_no_80_85 gate=FORWARD_WATCH_ACCUMULATING 42W-4L resolved=46 pnl=+3.33 gap=-6.4pp gap_delta=-6.0pp perfect_wins_needed=24 | blockers=wilson<BE+2pp; posthoc_cut_not_ready; equivalent_forward_watch_not_ready
- crypto_last_hour_longshot_no|captured_weekday=Tue | bridge_gate=NATIVE_PROMOTION_BLOCKED | cut_gate=NATIVE_CUT_ACCUMULATING | cut=70W-1L resolved=71 pnl=+4.95 gap=-1.0pp perfect_wins_needed=11 | watch=equivalent:native_watch|crypto_tue_no_any_ask gate=FORWARD_WATCH_ACCUMULATING 18W-1L resolved=19 pnl=+0.41 gap=-19.2pp gap_delta=-18.3pp perfect_wins_needed=82 | blockers=wilson<BE+2pp; posthoc_cut_not_ready; equivalent_forward_watch_not_ready
- crypto_last_hour_longshot_no|shadow_entry_band=80-85 | bridge_gate=NATIVE_PROMOTION_BLOCKED | cut_gate=NATIVE_CUT_ACCUMULATING | cut=59W-3L resolved=62 pnl=+5.25 gap=-2.0pp perfect_wins_needed=12 | watch=equivalent:native_watch|crypto_shadow_entry_80_85 gate=FORWARD_WATCH_WAITING 0W-0L resolved=0 pnl=+0.00 gap=-2.0pp gap_delta=-0.0pp perfect_wins_needed=none | blockers=wilson<BE+2pp; posthoc_cut_not_ready; equivalent_forward_watch_not_ready
- crypto_last_hour_longshot_no|signal_tier=moderate|native_ask_band=90-95 | bridge_gate=NATIVE_PROMOTION_BLOCKED | cut_gate=NATIVE_CUT_ACCUMULATING | cut=109W-3L resolved=112 pnl=+5.25 gap=-2.2pp perfect_wins_needed=49 | watch=equivalent:native_watch|crypto_moderate_no_90_95 gate=FORWARD_WATCH_ACCUMULATING 1W-0L resolved=1 pnl=+0.06 gap=-75.3pp gap_delta=-73.1pp perfect_wins_needed=92 | blockers=wilson<BE+2pp; posthoc_cut_not_ready; equivalent_forward_watch_not_ready
- crypto_last_hour_longshot_no|native_spread_band=<=1c|native_depth_band=10-99 | bridge_gate=NATIVE_PROMOTION_BLOCKED | cut_gate=NATIVE_CUT_ACCUMULATING | cut=114W-6L resolved=120 pnl=+5.90 gap=-2.6pp perfect_wins_needed=41 | watch=equivalent:native_watch|crypto_spread_le1_depth_10_99 gate=FORWARD_WATCH_ACCUMULATING 52W-5L resolved=57 pnl=+0.65 gap=-11.0pp gap_delta=-8.5pp perfect_wins_needed=87 | blockers=wilson<BE+2pp; posthoc_cut_not_ready; equivalent_forward_watch_not_ready
- crypto_last_hour_longshot_no|native_ask_band=85-90 | bridge_gate=NATIVE_PROMOTION_BLOCKED | cut_gate=NATIVE_CUT_ACCUMULATING | cut=227W-23L resolved=250 pnl=+6.30 gap=-3.7pp perfect_wins_needed=99 | watch=equivalent:native_watch|crypto_no_85_90 gate=FORWARD_WATCH_ACCUMULATING 2W-0L resolved=2 pnl=+0.20 gap=-57.8pp gap_delta=-54.1pp perfect_wins_needed=43 | blockers=wilson<BE+2pp; posthoc_cut_not_ready; equivalent_forward_watch_not_ready

## Kalshi Native Preflight Walk-Forward Validation
- command: `python3 scripts/kalshi_native_preflight_walkforward.py --limit 8`
- status: NO_WALKFORWARD_NATIVE_CUT | ready=false | observations=22131 | cuts=2481 | display_cuts=327 | validated_cuts=0 | ready_cuts=0 | split_cutoff=2026-07-02T02:59:47+00:00 | min_train=30 | min_validation=15 | edge_buffer=+2.0pp | scope=posthoc_walkforward_native_cut_validation_requires_predeclared_forward_gate
- best: crypto_last_hour_longshot_no|native_ask_band=80-85 | gate=WALKFORWARD_REJECT | type=single | train=93 resolved 77W-16L -$0.96 Wilson 73.9% vs target 85.8% gap=-12.0pp | validation=61 resolved 57W-4L +$5.81 Wilson 84.3% vs target 85.9% gap=-1.6pp | blockers=train_pnl<=0;train_wilson<BE+buffer;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXBTCD-26JUL0709-T63699.99 status=active due=2026-07-07T12:59:59.188159+00:00 ask=0.80
- rank 1: crypto_last_hour_longshot_no|native_ask_band=80-85 | gate=WALKFORWARD_REJECT | type=single | train=93 resolved 77W-16L -$0.96 Wilson 73.9% vs target 85.8% gap=-12.0pp | validation=61 resolved 57W-4L +$5.81 Wilson 84.3% vs target 85.9% gap=-1.6pp | blockers=train_pnl<=0;train_wilson<BE+buffer;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXBTCD-26JUL0709-T63699.99 status=active due=2026-07-07T12:59:59.188159+00:00 ask=0.80
- rank 2: weather_no_candidate:no_95_98_zero_loss_cities_v1|captured_weekday=Wed | gate=WALKFORWARD_REJECT | type=single | train=15 resolved 15W-0L +$0.38 Wilson 79.6% vs target 99.5% gap=-19.9pp | validation=0 resolved 0W-0L +$0.00 Wilson 0.0% vs target 2.0% gap=-2.0pp | blockers=train_resolved<30;train_wilson<BE+buffer;validation_resolved<15;validation_pnl<=0;validation_wilson<BE+buffer | promotion_blockers=none
- rank 3: crypto_last_hour_longshot_no|captured_weekday=Wed | gate=WALKFORWARD_REJECT | type=single | train=47 resolved 38W-9L -$4.72 Wilson 67.5% vs target 92.9% gap=-25.4pp | validation=0 resolved 0W-0L +$0.00 Wilson 0.0% vs target 2.0% gap=-2.0pp | blockers=train_pnl<=0;train_wilson<BE+buffer;validation_resolved<15;validation_pnl<=0;validation_wilson<BE+buffer | promotion_blockers=none
- rank 4: crypto_ladder_dislocation|captured_weekday=Wed | gate=WALKFORWARD_REJECT | type=single | train=15 resolved 11W-4L -$1.56 Wilson 48.0% vs target 85.7% gap=-37.7pp | validation=0 resolved 0W-0L +$0.00 Wilson 0.0% vs target 2.0% gap=-2.0pp | blockers=train_resolved<30;train_pnl<=0;train_wilson<BE+buffer;validation_resolved<15;validation_pnl<=0;validation_wilson<BE+buffer | promotion_blockers=none
- rank 5: crypto_last_hour_longshot_no|asset=ETH|native_ask_band=85-90 | gate=WALKFORWARD_REJECT | type=pair | train=39 resolved 35W-4L +$0.59 Wilson 76.4% vs target 90.2% gap=-13.8pp | validation=26 resolved 26W-0L +$3.09 Wilson 87.1% vs target 90.1% gap=-3.0pp | blockers=train_wilson<BE+buffer;validation_wilson<BE+buffer | promotion_blockers=none
- rank 6: crypto_last_hour_longshot_no|shadow_volume_band=1000-4999 | gate=WALKFORWARD_REJECT | type=single | train=82 resolved 75W-7L +$0.59 Wilson 83.4% vs target 92.7% gap=-9.3pp | validation=47 resolved 46W-1L +$3.44 Wilson 88.9% vs target 92.4% gap=-3.5pp | blockers=train_wilson<BE+buffer;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXBTCD-26JUL0709-T63699.99 status=active due=2026-07-07T12:59:59.188159+00:00 ask=0.80
- rank 7: crypto_last_hour_longshot_no|minutes_to_expiry_band=40-60m|native_ask_band=80-85 | gate=WALKFORWARD_REJECT | type=pair | train=50 resolved 39W-11L -$2.97 Wilson 64.8% vs target 85.9% gap=-21.2pp | validation=43 resolved 40W-3L +$3.95 Wilson 81.4% vs target 85.8% gap=-4.4pp | blockers=train_pnl<=0;train_wilson<BE+buffer;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXBTCD-26JUL0709-T63699.99 status=active due=2026-07-07T12:59:59.188159+00:00 ask=0.80
- rank 8: crypto_last_hour_longshot_no|minutes_to_expiry_band=10-20m | gate=WALKFORWARD_REJECT | type=single | train=70 resolved 60W-10L -$3.63 Wilson 75.7% vs target 92.9% gap=-17.2pp | validation=44 resolved 43W-1L +$3.10 Wilson 88.2% vs target 92.7% gap=-4.5pp | blockers=train_pnl<=0;train_wilson<BE+buffer;validation_wilson<BE+buffer | promotion_blockers=none

## Kalshi Crypto Last-Hour Native Subcell Audit
- command: `python3 scripts/kalshi_crypto_last_hour_subcell_audit.py --json`
- status: NO_NATIVE_SUBCELL_READY | ready=false | cells=6 | ready_cells=0 | mapped_shadow_candidate_cells=3 | min_resolved=30 | edge_buffer=+2.0pp | scope=first native-actionable event per crypto hour split by shadow tier/entry band
- best: crypto_last_hour_native_subcell:moderate:80-90 | gate=NATIVE_FORWARD_ACCUMULATING | mapped_shadow_candidate=true | native_events=81 resolved=81 pending=0 active=0 stale=0 unknown=0 | 76W-5L | pnl=+4.21 | Wilson 86.4% vs BE 88.6% | gap=-2.3pp | blockers=wilson<BE+2pp | perfect_wins_needed=40
- rank 1: crypto_last_hour_native_subcell:moderate:80-90 | gate=NATIVE_FORWARD_ACCUMULATING | mapped_shadow_candidate=true | native_events=81 resolved=81 pending=0 active=0 stale=0 unknown=0 | 76W-5L | pnl=+4.21 | Wilson 86.4% vs BE 88.6% | gap=-2.3pp | blockers=wilson<BE+2pp | perfect_wins_needed=40
- rank 2: crypto_last_hour_native_subcell:strong:90-95 | gate=NATIVE_FORWARD_ACCUMULATING | mapped_shadow_candidate=true | native_events=193 resolved=191 pending=2 active=2 stale=0 unknown=0 | 175W-16L | pnl=-2.81 | Wilson 86.8% vs BE 93.0% | gap=-6.2pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=323 | next_pending=KXBTCD-26JUL0709-T63699.99 status=active due=2026-07-07T12:59:59.188159+00:00 ask=0.80
- rank 3: crypto_last_hour_native_subcell:weak:80-90 | gate=NATIVE_FORWARD_ACCUMULATING | mapped_shadow_candidate=true | native_events=111 resolved=111 pending=0 active=0 stale=0 unknown=0 | 96W-15L | pnl=-1.15 | Wilson 78.9% vs BE 87.5% | gap=-8.6pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=120
- rank 4: crypto_last_hour_native_subcell:native_ask:80-90 | gate=NATIVE_FORWARD_ACCUMULATING | mapped_shadow_candidate=false | native_events=195 resolved=193 pending=2 active=2 stale=0 unknown=0 | 171W-22L | pnl=+3.57 | Wilson 83.3% vs BE 86.7% | gap=-3.4pp | blockers=wilson<BE+2pp | perfect_wins_needed=96 | next_pending=KXBTCD-26JUL0709-T63699.99 status=active due=2026-07-07T12:59:59.188159+00:00 ask=0.80
- rank 5: crypto_last_hour_native_subcell:native_ask:90-95 | gate=NATIVE_FORWARD_ACCUMULATING | mapped_shadow_candidate=false | native_events=190 resolved=190 pending=0 active=0 stale=0 unknown=0 | 175W-15L | pnl=-1.93 | Wilson 87.4% vs BE 93.1% | gap=-5.7pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=312
- rank 6: crypto_last_hour_native_subcell:moderate:90-95 | gate=NATIVE_FORWARD_ACCUMULATING | mapped_shadow_candidate=false | native_events=52 resolved=52 pending=0 active=0 stale=0 unknown=0 | 47W-5L | pnl=-0.53 | Wilson 79.4% vs BE 91.4% | gap=-12.0pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=121

## Kalshi Crypto Last-Hour Entry Timing Audit
- command: `python3 scripts/kalshi_crypto_last_hour_entry_timing_audit.py --limit 8`
- status: NO_ENTRY_TIMING_CANDIDATE | ready=false | posthoc_candidates=0 | source_actionable_rows=2134 | selected_observations=1097 | cuts=381 | min_resolved=30 | edge_buffer=+2.0pp
- best: crypto_last_hour_entry_timing:latest_actionable|native_ask_band=90-95 | gate=ENTRY_TIMING_ACCUMULATING | observations=232 resolved=232 pending=0 | 225W-7L | pnl=+$7.96 | Wilson 93.9% vs target 95.6% (BE 93.6%) | gap=-1.6pp | blockers=wilson<BE+2pp
- rank 1: crypto_last_hour_entry_timing:latest_actionable|native_ask_band=90-95 | gate=ENTRY_TIMING_ACCUMULATING | observations=232 resolved=232 pending=0 | 225W-7L | pnl=+$7.96 | Wilson 93.9% vs target 95.6% (BE 93.6%) | gap=-1.6pp | blockers=wilson<BE+2pp
- rank 2: crypto_last_hour_entry_timing:latest_actionable|signal_tier=moderate|native_ask_band=90-95 | gate=ENTRY_TIMING_ACCUMULATING | observations=77 resolved=77 pending=0 | 76W-1L | pnl=+$4.15 | Wilson 93.0% vs target 95.3% (BE 93.3%) | gap=-2.3pp | blockers=wilson<BE+2pp
- rank 3: crypto_last_hour_entry_timing:first_actionable|native_depth_band=1000+ | gate=ENTRY_TIMING_ACCUMULATING | observations=104 resolved=104 pending=0 | 100W-4L | pnl=+$4.67 | Wilson 90.5% vs target 93.7% (BE 91.7%) | gap=-3.1pp | blockers=wilson<BE+2pp
- rank 4: crypto_last_hour_entry_timing:latest_actionable|asset=BTC|native_ask_band=90-95 | gate=ENTRY_TIMING_ACCUMULATING | observations=109 resolved=109 pending=0 | 106W-3L | pnl=+$3.85 | Wilson 92.2% vs target 95.7% (BE 93.7%) | gap=-3.5pp | blockers=wilson<BE+2pp
- rank 5: crypto_last_hour_entry_timing:first_actionable|native_spread_band=<=1c | gate=ENTRY_TIMING_ACCUMULATING | observations=296 resolved=295 pending=1 | 274W-21L | pnl=+$5.63 | Wilson 89.4% vs target 92.9% (BE 90.9%) | gap=-3.6pp | blockers=wilson<BE+2pp
- rank 6: crypto_last_hour_entry_timing:latest_actionable|asset=BTC|native_ask_band=95-98 | gate=ENTRY_TIMING_ACCUMULATING | observations=57 resolved=57 pending=0 | 57W-0L | pnl=+$2.28 | Wilson 93.7% vs target 98.0% (BE 96.0%) | gap=-4.3pp | blockers=wilson<BE+2pp
- rank 7: crypto_last_hour_entry_timing:latest_actionable|asset=ETH|native_ask_band=90-95 | gate=ENTRY_TIMING_ACCUMULATING | observations=60 resolved=60 pending=0 | 59W-1L | pnl=+$2.86 | Wilson 91.1% vs target 95.6% (BE 93.6%) | gap=-4.4pp | blockers=wilson<BE+2pp
- rank 8: crypto_last_hour_entry_timing:first_actionable|native_spread_band=<=1c|native_depth_band=1000+ | gate=ENTRY_TIMING_ACCUMULATING | observations=90 resolved=90 pending=0 | 86W-4L | pnl=+$3.54 | Wilson 89.1% vs target 93.6% (BE 91.6%) | gap=-4.5pp | blockers=wilson<BE+2pp

## Kalshi Crypto Ladder Dislocation Preflight
- command: `python3 scripts/kalshi_crypto_ladder_dislocation_preflight.py --json`
- latest_run: captured_at=2026-07-07T12:14:27+00:00 | lookahead=75m | events=5 rows_per_event=40 | candidates=112 checked=112 dislocation_qty1=0 | min_source_edge=0.03 max_source_age=300s | top_reasons=missing_native_no_ask=108, source_age_too_old:753s=3, source_age_too_old:754s=1
- latest_rows: KXETHD-26JUL0709-T1789.99 ETH/strong source_no=0.93 native_no_ask=0.55 edge=0.38 age=753s spread=0.03 depth=1401 win=0.43 due=2026-07-07T12:59:59.553643+00:00 reason=source_age_too_old:753s ; KXSOLD-26JUL0709-T81.9999 SOL/strong source_no=0.94 native_no_ask=0.73 edge=0.21 age=753s spread=0.07 depth=200 win=0.25 due=2026-07-07T12:59:59.217749+00:00 reason=source_age_too_old:753s ; KXBTCD-26JUL0709-T64299.99 BTC/extreme source_no=0.99 native_no_ask=0.95 edge=0.04 age=754s spread=0.02 depth=98 win=0.04 due=2026-07-07T12:59:59.240058+00:00 reason=source_age_too_old:754s ; KXETHD-26JUL0709-T1809.99 ETH/extreme source_no=0.98 native_no_ask=0.99 edge=-0.01 age=753s spread=0.02 depth=4152 win=0.00 due=2026-07-07T12:59:59.560939+00:00 reason=source_age_too_old:753s ; KXBTCD-26JUL0709-T64699.99 BTC/extreme source_no=0.99 native_no_ask=missing edge=missing age=754s spread=missing depth=0 win=missing due=2026-07-07T12:59:59.282523+00:00 reason=missing_native_no_ask ; KXBTCD-26JUL0709-T64799.99 BTC/extreme source_no=0.99 native_no_ask=missing edge=missing age=754s spread=missing depth=0 win=missing due=2026-07-07T12:59:59.309472+00:00 reason=missing_native_no_ask

## Kalshi Crypto Ladder Dislocation Forward Audit
- command: `python3 scripts/kalshi_crypto_ladder_dislocation_audit.py --limit 8`
- status: NO_LIVE_READY | ready=false | cells=6 | ready_cells=0 | observations=117 | min_resolved=30 | edge_buffer=+2.0pp | scope=source-vs-native ladder gaps only; not riskless structural arbitrage
- best: event_first | gate=LADDER_DISLOCATION_ACCUMULATING | observations=75 resolved=75 pending=0 active=0 stale=0 | 54W-21L pnl_qty1=-$7.35 | Wilson 61.0% vs target 83.8% gap=-22.8pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=117
- rank 1: event_first | gate=LADDER_DISLOCATION_ACCUMULATING | observations=75 resolved=75 pending=0 active=0 stale=0 | 54W-21L pnl_qty1=-$7.35 | Wilson 61.0% vs target 83.8% gap=-22.8pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=117
- rank 2: ticker_first | gate=LADDER_DISLOCATION_ACCUMULATING | observations=79 resolved=79 pending=0 active=0 stale=0 | 57W-22L pnl_qty1=-$8.07 | Wilson 61.4% vs target 84.4% gap=-22.9pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=128
- rank 3: all_rows | gate=LADDER_DISLOCATION_ACCUMULATING | observations=117 resolved=117 pending=0 active=0 stale=0 | 79W-38L pnl_qty1=-$13.55 | Wilson 58.6% vs target 81.1% gap=-22.5pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=151
- rank 4: asset_btc | gate=LADDER_DISLOCATION_ACCUMULATING | observations=8 resolved=8 pending=0 active=0 stale=0 | 5W-3L pnl_qty1=-$2.17 | Wilson 30.6% vs target 91.6% gap=-61.1pp | blockers=resolved<30; pnl<=0; wilson<BE+2pp | perfect_wins_needed=93
- rank 5: asset_eth | gate=LADDER_DISLOCATION_ACCUMULATING | observations=52 resolved=52 pending=0 active=0 stale=0 | 35W-17L pnl_qty1=-$6.05 | Wilson 53.8% vs target 80.9% gap=-27.2pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=85
- rank 6: asset_sol | gate=LADDER_DISLOCATION_ACCUMULATING | observations=57 resolved=57 pending=0 active=0 stale=0 | 39W-18L pnl_qty1=-$5.33 | Wilson 55.5% vs target 79.8% gap=-24.3pp | blockers=pnl<=0; wilson<BE+2pp | perfect_wins_needed=78

## Kalshi Hourly Temperature State Audit
- command: `python3 scripts/kalshi_hourly_temp_state_audit.py --max-pages-per-series 2 --limit 1000 --max-dates 4 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-05T13:21:03+00:00 | markets_checked=24 parsed=24 source_observations=58 locked_rows=0 actionable_qty1=0 | max_ask=0.98 min_depth=1 | series=KXTEMPNYCH dates=2026-07-05 | state_keys=10 observations_raw=58 source=weathercom_kalshi_metar_primary source_errors=0 | counts=KXTEMPNYCH=24 | reasons=hourly_temp_observation_missing_or_future=24

## Kalshi Direct MLB Player Prop State Audit
- command: `python3 scripts/kalshi_mlb_player_prop_state_audit.py --max-pages-per-series 6 --limit 1000 --max-dates 6 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-05T21:22:23+00:00 | markets_checked=3098 parsed=3098 espn_games=11 locked_rows=425 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXMLBKS,KXMLBOUTS,KXMLBHIT,KXMLBHRR,KXMLBHR,KXMLBTB,KXMLBRBI,KXMLBSB dates=2026-07-05 | state_games=11 | reasons=player_stat_waiting_for_threshold_or_final=1542, player_stat_missing_after_final=571, mlb_player_stat_already_reached=425, mlb_boxscore_not_current=347, player_stat_missing_before_final=213
- locked_rows: KXMLBHIT-26JUL051230NYMATL-ATLARILEY27-1 YES ask=1.00 depth=0 bid=0.99 win=0.00 stat=hits:2/1 game=NYM@ATL 10-9 STATUS_IN_PROGRESS reason=mlb_player_stat_already_reached actionable=0 ; KXMLBHIT-26JUL051230NYMATL-ATLARILEY27-2 YES ask=1.00 depth=0 bid=0.99 win=0.00 stat=hits:2/2 game=NYM@ATL 10-9 STATUS_IN_PROGRESS reason=mlb_player_stat_already_reached actionable=0 ; KXMLBHIT-26JUL051230NYMATL-ATLDBALDWIN30-1 YES ask=1.00 depth=0 bid=0.99 win=0.00 stat=hits:2/1 game=NYM@ATL 10-9 STATUS_IN_PROGRESS reason=mlb_player_stat_already_reached actionable=0 ; KXMLBHIT-26JUL051230NYMATL-ATLDBALDWIN30-2 YES ask=1.00 depth=0 bid=0.99 win=0.00 stat=hits:2/2 game=NYM@ATL 10-9 STATUS_IN_PROGRESS reason=mlb_player_stat_already_reached actionable=0 ; KXMLBHIT-26JUL051230NYMATL-ATLDSMITH8-1 YES ask=1.00 depth=0 bid=0.99 win=0.00 stat=hits:1/1 game=NYM@ATL 10-9 STATUS_IN_PROGRESS reason=mlb_player_stat_already_reached actionable=0 ; KXMLBHIT-26JUL051230NYMATL-ATLMDUBN14-1 YES ask=1.00 depth=0 bid=0.99 win=0.00 stat=hits:3/1 game=NYM@ATL 10-9 STATUS_IN_PROGRESS reason=mlb_player_stat_already_reached actionable=0 ; KXMLBHIT-26JUL051230NYMATL-ATLMDUBN14-2 YES ask=1.00 depth=0 bid=0.99 win=0.00 stat=hits:3/2 game=NYM@ATL 10-9 STATUS_IN_PROGRESS reason=mlb_player_stat_already_reached actionable=0 ; KXMLBHIT-26JUL051230NYMATL-ATLMDUBN14-3 YES ask=1.00 depth=0 bid=0.99 win=0.00 stat=hits:3/3 game=NYM@ATL 10-9 STATUS_IN_PROGRESS reason=mlb_player_stat_already_reached actionable=0

## Kalshi MVE Component Result Audit
- command: `python3 scripts/kalshi_mve_component_result_audit.py --series KXMVESPORTSMULTIGAMEEXTENDED,KXMVECROSSCATEGORY --limit 1000 --max-pages 20 --max-component-events 250 --pause-seconds 0.3 --max-target-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-05T14:17:35+00:00 | markets_checked=204000 with_legs=204000 component_events=566/566 fetched=566 component_markets=5458 resolved=2781 locked_rows=8870 actionable_qty1=0 | max_target_ask=0.25 min_depth=1 | series=KXMVESPORTSMULTIGAMEEXTENDED,KXMVECROSSCATEGORY counts=KXMVECROSSCATEGORY=44000, KXMVESPORTSMULTIGAMEEXTENDED=160000 | page_cap=KXMVESPORTSMULTIGAMEEXTENDED rate_limited=KXMVECROSSCATEGORY component_cap=false component_rate_limited=false | reasons=not_locked_by_component_results=195130, component_false_locks_mve_no=7843, component_market_resolved=2781, all_components_true_locks_mve_yes=1027
- latest_rows: KXMVECROSSCATEGORY-S202634C3F6A4ACC-F8F06C79EEA YES ask=0.00 depth=0 bid=0.00 win=1.00 series=KXMVECROSSCATEGORY legs=2/2 decisive=KXETH15M-26JUL051015-15:YES->YES reason=all_components_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S20263C03AD3451F-5F3285533F8 YES ask=0.00 depth=0 bid=0.00 win=1.00 series=KXMVECROSSCATEGORY legs=2/2 decisive=KXXRP15M-26JUL051015-15:NO->NO reason=all_components_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S20264CF5052B0D0-BFD1EF6054B YES ask=0.00 depth=0 bid=0.00 win=1.00 series=KXMVECROSSCATEGORY legs=3/3 decisive=KXXRP15M-26JUL051015-15:NO->NO reason=all_components_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S202659B334FB0CD-4278DFD073F YES ask=0.00 depth=0 bid=0.00 win=1.00 series=KXMVECROSSCATEGORY legs=2/2 decisive=KXXRP15M-26JUL051015-15:NO->NO reason=all_components_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S202689F863A6A89-9BFFF540A3E YES ask=0.00 depth=0 bid=0.00 win=1.00 series=KXMVECROSSCATEGORY legs=2/2 decisive=KXDOGE15M-26JUL051015-15:NO->NO reason=all_components_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S2026AEEB65CDA5D-5DE6D97F12D YES ask=0.00 depth=0 bid=0.00 win=1.00 series=KXMVECROSSCATEGORY legs=2/2 decisive=KXXRP15M-26JUL051015-15:NO->NO reason=all_components_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S2026B9E7997B4AE-5CA65BE5886 YES ask=0.00 depth=0 bid=0.00 win=1.00 series=KXMVECROSSCATEGORY legs=2/2 decisive=KXSOL15M-26JUL051015-15:NO->NO reason=all_components_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S2026BFF507B28FA-DCB332E8AA4 YES ask=0.00 depth=0 bid=0.00 win=1.00 series=KXMVECROSSCATEGORY legs=3/3 decisive=KXSOL15M-26JUL051015-15:NO->NO reason=all_components_true_locks_mve_yes actionable=0

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
- status: live_rows=1 dry_runs=26 filled_rows=0 cancelled_rows=0 | strategy_open=0 strategy_open_cost=$0.00 | all_live_pilot_open=5 all_live_pilot_cost=$0.50
- latest_rows: id=138 live=false status=DRY_RUN ticker=KXBTCD-26JUL0623-T64099.99 side=NO qty=1 limit=0.98 bid=0.97 ask=0.98 depth=2049 spread=0.01 trade_id=none order=none fill_confirmed=0 cost=$unknown fee=$unknown spot=63742.07 threshold=64099.99 cushion=$357.93 subcell=74W-5L wilson=0.86 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=native_no_ask_out_of_guard:0.9800 ; id=137 live=false status=DRY_RUN ticker=KXBTCD-26JUL0623-T64099.99 side=NO qty=1 limit=0.91 bid=0.90 ask=0.91 depth=574 spread=0.01 trade_id=none order=none fill_confirmed=0 cost=$unknown fee=$unknown spot=63833.54 threshold=64099.99 cushion=$266.44 subcell=74W-5L wilson=0.86 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=native_no_ask_out_of_guard:0.9100 ; id=124 live=false status=DRY_RUN ticker=KXBTCD-26JUL0516-T62899.99 side=NO qty=1 limit=0.82 bid=0.81 ask=0.82 depth=275 spread=0.01 trade_id=none order=none fill_confirmed=0 cost=$unknown fee=$unknown spot=62795.03 threshold=62899.99 cushion=$104.97 subcell=73W-5L wilson=0.86 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=static_preflight_failed ; id=123 live=false status=DRY_RUN ticker=KXBTCD-26JUL0516-T62899.99 side=NO qty=1 limit=0.84 bid=0.83 ask=0.84 depth=2182 spread=0.01 trade_id=none order=none fill_confirmed=0 cost=$unknown fee=$unknown spot=62772.15 threshold=62899.99 cushion=$127.83 subcell=73W-5L wilson=0.86 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=static_preflight_failed ; id=121 live=false status=DRY_RUN ticker=KXBTCD-26JUL0514-T62799.99 side=NO qty=1 limit=0.98 bid=0.97 ask=0.98 depth=1068 spread=0.01 trade_id=none order=none fill_confirmed=0 cost=$unknown fee=$unknown spot=62630.57 threshold=62799.99 cushion=$169.41 subcell=73W-5L wilson=0.86 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=native_no_ask_out_of_guard:0.9800

## Kalshi Weather Chicago Low 77-78 YES Pilot
- strategy: kalshi_live_pilot_weather_chi_low_77_78_yes_v1
- check_command: `python3 scripts/kalshi_weather_chi_low_77_78_yes_pilot.py`
- status: live_rows=1 dry_runs=0 filled_rows=0 cancelled_rows=0 | strategy_open=0 strategy_open_cost=$0.00 | all_live_pilot_open=5 all_live_pilot_cost=$0.50
- latest_rows: id=1 live=true status=RESOLVED_LOSS ticker=KXLOWTCHI-26JUL02-B77.5 side=YES qty=1 limit=0.81 bid=0.80 ask=0.81 depth=205 spread=0.01 trade_id=7105 order=059f7bf4 fill_confirmed=1 cost=$0.81 fee=$0.01 observed_min_f=78.08 forecast_min_f=83.00 resolution=LOSS pnl=-0.82 reason=none

## Kalshi Netflix Top Views NO Pilot
- strategy: kalshi_live_pilot_netflix_top_views_movie_25m_no_v1
- check_command: `python3 scripts/kalshi_netflix_top_views_no_pilot.py`
- status: live_rows=1 dry_runs=12 filled_rows=0 cancelled_rows=0 | strategy_open=0 strategy_open_cost=$0.00 | all_live_pilot_open=5 all_live_pilot_cost=$0.50
- latest_rows: id=13 live=false status=DRY_RUN ticker=KXNETFLIXTOPVIEWSMOVIE-26JUL06-25 side=NO qty=1 limit=0.65 bid=0.62 ask=0.65 depth=5 spread=0.03 trade_id=none order=none fill_confirmed=0 cost=$unknown fee=$unknown target_week=2026-07-05 latest_week=2026-06-28 latest_views_m=31.00 primary_no=13/23 primary_wilson=0.37 recent_no=5/15 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=native_no_ask_out_of_guard:0.6500 ; id=12 live=false status=DRY_RUN ticker=KXNETFLIXTOPVIEWSMOVIE-26JUL06-25 side=NO qty=1 limit=0.51 bid=0.26 ask=0.51 depth=23 spread=0.25 trade_id=none order=none fill_confirmed=0 cost=$unknown fee=$unknown target_week=2026-07-05 latest_week=2026-06-28 latest_views_m=31.00 primary_no=13/23 primary_wilson=0.37 recent_no=5/15 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=native_no_ask_out_of_guard:0.5100 ; id=11 live=false status=DRY_RUN ticker=KXNETFLIXTOPVIEWSMOVIE-26JUL06-25 side=NO qty=1 limit=0.29 bid=0.26 ask=0.29 depth=35 spread=0.03 trade_id=none order=none fill_confirmed=0 cost=$unknown fee=$unknown target_week=2026-07-05 latest_week=2026-06-28 latest_views_m=31.00 primary_no=13/23 primary_wilson=0.37 recent_no=5/15 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=native_no_ask_out_of_guard:0.2900 ; id=10 live=false status=DRY_RUN ticker=KXNETFLIXTOPVIEWSMOVIE-26JUL06-25 side=NO qty=1 limit=0.29 bid=0.25 ask=0.29 depth=34 spread=0.04 trade_id=none order=none fill_confirmed=0 cost=$unknown fee=$unknown target_week=2026-07-05 latest_week=2026-06-28 latest_views_m=31.00 primary_no=13/23 primary_wilson=0.37 recent_no=5/15 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=native_no_ask_out_of_guard:0.2900 ; id=9 live=false status=DRY_RUN ticker=KXNETFLIXTOPVIEWSMOVIE-26JUL06-25 side=NO qty=1 limit=0.19 bid=0.18 ask=0.19 depth=1 spread=0.01 trade_id=none order=none fill_confirmed=0 cost=$unknown fee=$unknown target_week=2026-07-05 latest_week=2026-06-28 latest_views_m=31.00 primary_no=13/23 primary_wilson=0.37 recent_no=5/15 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=native_no_ask_out_of_guard:0.1900

## Kalshi Netflix Top10 Rank Audit
- command: `python3 scripts/kalshi_netflix_top10_rank_audit.py --series KXNETFLIXRANKSHOWRUNNERUP,KXNETFLIXRANKSHOWGLOBAL,KXNETFLIXRANKMOVIEGLOBAL --limit 1000 --max-pages-per-series 2 --pause-seconds 0.05 --max-ask 0.25 --min-depth 1 --record --json`
- latest_run: captured_at=2026-07-05T17:23:46+00:00 | kalshi_markets=31 events=3 netflix_rows=30 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXNETFLIXRANKSHOWRUNNERUP,KXNETFLIXRANKSHOWGLOBAL,KXNETFLIXRANKMOVIEGLOBAL counts=KXNETFLIXRANKMOVIEGLOBAL=10, KXNETFLIXRANKSHOWGLOBAL=10, KXNETFLIXRANKSHOWRUNNERUP=11 | source_week_end=2026-06-28 | charts=KXNETFLIXRANKMOVIEGLOBAL:week=2026-06-28 range=Global | 6/22/26 - 6/28/26 rank1=Voicemails for Isabelle ; KXNETFLIXRANKSHOWGLOBAL:week=2026-06-28 range=Global | 6/22/26 - 6/28/26 rank1=I Will Find You: Limited Series ; KXNETFLIXRANKSHOWRUNNERUP:week=2026-06-28 range=United States | 6/22/26 - 6/28/26 rank2=Avatar: The Last Airbender: Season 2 | page_cap=none rate_limited=none | reasons=source_week_not_target=31

## Kalshi X Post Count Audit
- command: `python3 scripts/kalshi_x_post_count_audit.py --series KXIMFTWEETS,KXWEFTWEETS --limit 1000 --max-pages-per-series 2 --pause-seconds 0.05 --max-ask 0.25 --min-depth 1 --record --json`
- latest_run: captured_at=2026-07-05T17:23:46+00:00 | markets_checked=12 events=2 timelines=2 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXIMFTWEETS,KXWEFTWEETS counts=KXIMFTWEETS=6, KXWEFTWEETS=6 | events_summary=KXIMFTWEETS-26JUL09:handle=IMFNews visible=7 complete=true after_close=false window=2026-07-02T16:00:00+00:00->2026-07-09T16:00:00+00:00 ; KXWEFTWEETS-26JUL09:handle=wef visible=1 complete=true after_close=false window=2026-07-02T16:00:00+00:00->2026-07-09T16:00:00+00:00 | reasons=range_not_irreversible=8, over_not_irreversible=2, under_not_irreversible=2

## Kalshi MVE MLB Player State Audit
- command: `python3 scripts/kalshi_mve_mlb_player_state_audit.py --limit 0 --max-components 500 --max-dates 6 --pause-seconds 0.02 --max-target-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-05T03:21:47+00:00 | markets_checked=12000 supported_markets=12000 supported_legs=46265 espn_games=16 locked_rows=232 actionable_qty1=0 | max_target_ask=0.25 min_depth=1 | component_titles=40 component_failures=0 state_games=16 index_rows=160000 | reasons=supported_mlb_player_legs_not_locked=11259, some_supported_mlb_player_legs_true_but_mve_not_locked=509, mlb_player_state_false_selected_leg_locks_mve_no=220, all_supported_mlb_player_state_legs_true_locks_mve_yes=12
- locked_rows: KXMVECROSSCATEGORY-S202610DCC18F490-479043137B1 YES ask=0.00 depth=0 bid=0.00 win=1.00 legs=3/3/3 decisive=KXMLBHIT-26JUL042008NYMATL-ATLOALBIES1-1:YES reason=mlb_player_stat_already_reached lock=all_supported_mlb_player_state_legs_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S20266371518C664-4FB7C4082F8 YES ask=0.00 depth=0 bid=0.00 win=1.00 legs=4/4/4 decisive=KXMLBHIT-26JUL042008NYMATL-ATLMOLSON28-1:YES reason=mlb_player_stat_already_reached lock=all_supported_mlb_player_state_legs_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S202691D307B2015-F702E71AF8A YES ask=0.00 depth=0 bid=0.00 win=1.00 legs=5/5/5 decisive=KXMLBHIT-26JUL042008NYMATL-ATLOALBIES1-1:YES reason=mlb_player_stat_already_reached lock=all_supported_mlb_player_state_legs_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S20269A17A877BB8-6037FD81F6F YES ask=0.00 depth=0 bid=0.00 win=1.00 legs=2/2/2 decisive=KXMLBHIT-26JUL042008NYMATL-ATLMOLSON28-1:YES reason=mlb_player_stat_already_reached lock=all_supported_mlb_player_state_legs_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S2026C3EC14D7C2E-D838D77668C YES ask=0.00 depth=0 bid=0.00 win=1.00 legs=3/3/3 decisive=KXMLBHIT-26JUL042008NYMATL-ATLOALBIES1-1:YES reason=mlb_player_stat_already_reached lock=all_supported_mlb_player_state_legs_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S2026C666F320F37-3A4AB92B84A YES ask=0.00 depth=0 bid=0.00 win=1.00 legs=2/2/2 decisive=KXMLBHIT-26JUL042008NYMATL-ATLOALBIES1-1:YES reason=mlb_player_stat_already_reached lock=all_supported_mlb_player_state_legs_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S2026C666F320F37-44BDD98F93D YES ask=0.00 depth=0 bid=0.00 win=1.00 legs=2/2/2 decisive=KXMLBHIT-26JUL042008NYMATL-ATLMDUBN14-1:YES reason=mlb_player_stat_already_reached lock=all_supported_mlb_player_state_legs_true_locks_mve_yes actionable=0 ; KXMVECROSSCATEGORY-S2026C666F320F37-48B3963C435 YES ask=0.00 depth=0 bid=0.00 win=1.00 legs=2/2/2 decisive=KXMLBHIT-26JUL042008NYMATL-ATLMOLSON28-1:YES reason=mlb_player_stat_already_reached lock=all_supported_mlb_player_state_legs_true_locks_mve_yes actionable=0

## Kalshi MLB Partial-Game State Audit
- command: `python3 scripts/kalshi_mlb_partial_game_state_audit.py --max-pages-per-series 6 --limit 1000 --max-dates 8 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-05T21:22:23+00:00 | markets_checked=559 parsed=553 espn_games=33 locked_rows=69 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXMLBRFI,KXMLBF3,KXMLBF5,KXMLBF5SPREAD,KXMLBF5TOTAL,KXMLBF7,KXMLBTEAMTOTAL,KXMLBEXTRAS dates=2026-07-05,2026-07-06,2026-07-07 | state_games=33 | counts=KXMLBEXTRAS=36, KXMLBF3=30, KXMLBF5=39, KXMLBF5SPREAD=52, KXMLBF5TOTAL=91, KXMLBF7=45, KXMLBRFI=28, KXMLBTEAMTOTAL=238 | reasons=mlb_teamtotal_game_not_final=195, mlb_f5total_window_not_complete=73, mlb_f5spread_window_not_complete=48, mlb_f7_window_not_complete=45, mlb_teamtotal_over_already_exceeded=43, mlb_f5_window_not_complete=36, mlb_extras_game_not_final=33, mlb_f3_window_not_complete=30
- locked_rows: KXMLBF5-26JUL051530DETTEX-DET YES ask=1.00 depth=0 bid=0.99 win=0.00 type=f5 window=5 target=DET threshold=missing margin=4.00 total=None game=DET@TEX 6-2 STATUS_IN_PROGRESS reason=mlb_f5_window_final actionable=0 ; KXMLBF5-26JUL051530DETTEX-TEX NO ask=1.00 depth=0 bid=0.99 win=0.00 type=f5 window=5 target=TEX threshold=missing margin=-4.00 total=None game=DET@TEX 6-2 STATUS_IN_PROGRESS reason=mlb_f5_window_final actionable=0 ; KXMLBF5-26JUL051530DETTEX-TIE NO ask=1.00 depth=0 bid=0.99 win=0.00 type=f5 window=5 target=TIE threshold=missing margin=0.00 total=None game=DET@TEX 6-2 STATUS_IN_PROGRESS reason=mlb_f5_window_final actionable=0 ; KXMLBF5SPREAD-26JUL051530DETTEX-DET2 YES ask=1.00 depth=0 bid=0.99 win=0.00 type=f5spread window=5 target=DET threshold=1.50 margin=4.00 total=None game=DET@TEX 6-2 STATUS_IN_PROGRESS reason=mlb_f5spread_window_final actionable=0 ; KXMLBF5SPREAD-26JUL051530DETTEX-DET3 YES ask=1.00 depth=0 bid=0.99 win=0.00 type=f5spread window=5 target=DET threshold=2.50 margin=4.00 total=None game=DET@TEX 6-2 STATUS_IN_PROGRESS reason=mlb_f5spread_window_final actionable=0 ; KXMLBF5SPREAD-26JUL051530DETTEX-TEX2 NO ask=1.00 depth=0 bid=0.99 win=0.00 type=f5spread window=5 target=TEX threshold=1.50 margin=-4.00 total=None game=DET@TEX 6-2 STATUS_IN_PROGRESS reason=mlb_f5spread_window_final actionable=0 ; KXMLBF5SPREAD-26JUL051530DETTEX-TEX3 NO ask=1.00 depth=0 bid=0.99 win=0.00 type=f5spread window=5 target=TEX threshold=2.50 margin=-4.00 total=None game=DET@TEX 6-2 STATUS_IN_PROGRESS reason=mlb_f5spread_window_final actionable=0 ; KXMLBF5TOTAL-26JUL051530DETTEX-1 YES ask=1.00 depth=0 bid=0.99 win=0.00 type=f5total window=5 target=None threshold=0.50 margin=missing total=8 game=DET@TEX 6-2 STATUS_IN_PROGRESS reason=mlb_f5total_over_already_exceeded actionable=0

## Kalshi WNBA Game State Audit
- command: `python3 scripts/kalshi_wnba_game_state_audit.py --max-pages-per-series 5 --limit 1000 --max-dates 8 --pause-seconds 1.0 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-05T17:44:26+00:00 | markets_checked=284 parsed=284 espn_games=5 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXWNBAGAME,KXWNBASPREAD,KXWNBATOTAL,KXWNBAOT,KXWNBA1QWINNER,KXWNBA2QWINNER,KXWNBA3QWINNER,KXWNBA4QWINNER,KXWNBA1HWINNER,KXWNBA2HWINNER,KXWNBA1QSPREAD,KXWNBA2QSPREAD,KXWNBA3QSPREAD,KXWNBA4QSPREAD,KXWNBA1HSPREAD,KXWNBA2HSPREAD,KXWNBA1QTOTAL,KXWNBA2QTOTAL,KXWNBA3QTOTAL,KXWNBA4QTOTAL,KXWNBA1HTOTAL,KXWNBA2HTOTAL dates=2026-07-05,2026-07-06 | state_games=5 | counts=KXWNBA1HSPREAD=6, KXWNBA1HTOTAL=2, KXWNBA1HWINNER=6, KXWNBA1QSPREAD=14, KXWNBA1QTOTAL=14, KXWNBA1QWINNER=6, KXWNBA2HSPREAD=14, KXWNBA2HTOTAL=14, KXWNBA2HWINNER=6, KXWNBA2QSPREAD=0, KXWNBA2QTOTAL=14, KXWNBA2QWINNER=6, KXWNBA3QSPREAD=14, KXWNBA3QTOTAL=14, KXWNBA3QWINNER=6, KXWNBA4QSPREAD=14, KXWNBA4QTOTAL=14, KXWNBA4QWINNER=6, KXWNBAGAME=10, KXWNBAOT=5, KXWNBASPREAD=54, KXWNBATOTAL=45 | reasons=wnba_spread_game_not_final=54, wnba_total_game_not_final=45, wnba_1q_spread_not_complete=14, wnba_1q_total_not_complete=14, wnba_2h_spread_not_complete=14, wnba_2h_total_not_complete=14, wnba_2q_total_not_complete=14, wnba_3q_spread_not_complete=14

## Kalshi WNBA Player Prop State Audit
- command: `python3 scripts/kalshi_wnba_player_prop_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-05T21:18:36+00:00 | markets_checked=52 parsed=52 espn_games=1 locked_rows=0 actionable_qty1=0 | max_ask=0.98 min_depth=1 | series=KXWNBAPTS,KXWNBAREB,KXWNBAAST,KXWNBA3PT dates=2026-07-05 | state_games=1 titles=52 title_failures=0 summary_fetches=1 | counts=KXWNBA3PT=10, KXWNBAAST=4, KXWNBAPTS=23, KXWNBAREB=15 | reasons=wnba_player_boxscore_not_current=52

## Kalshi WNBA Player Prop Live Pilot
- strategy: kalshi_live_pilot_wnba_player_prop_boxscore_lock_v1
- check_command: `python3 scripts/kalshi_wnba_player_prop_live_pilot.py`
- status: live_rows=1 dry_runs=2 filled_rows=1 cancelled_rows=0 | strategy_open=0 strategy_open_cost=$0.00 | all_live_pilot_open=5 all_live_pilot_cost=$0.50
- latest_rows: id=3 live=false status=DRY_RUN_READY ticker=KXWNBAREB-26JUL04GSATL-ATLAREESE5-12 side=YES qty=1 limit=0.98 bid=0.43 ask=0.98 depth=2 modeled_fee=$0.01 win_pnl=$0.01 trade_id=none order=none fill_confirmed=0 cost=$unknown ledger_fee=$unknown player=Angel Reese stat=rebounds 12/12 clock=3:16 period=4 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=dry_run_ready ; id=2 live=false status=DRY_RUN_READY ticker=KXWNBAREB-26JUL04GSATL-ATLAREESE5-12 side=YES qty=1 limit=0.98 bid=0.43 ask=0.98 depth=26 modeled_fee=$0.01 win_pnl=$0.01 trade_id=none order=none fill_confirmed=0 cost=$unknown ledger_fee=$unknown player=Angel Reese stat=rebounds 12/12 clock=3:33 period=4 pred_p=unknown edge=unknown resolution=unresolved pnl=unknown reason=dry_run_ready ; id=1 live=true status=PLACED_FILLED ticker=KXWNBAREB-26JUL02ATLWSH-ATLAGRAY15-2 side=YES qty=1 limit=0.98 bid=0.97 ask=0.98 depth=10 modeled_fee=$0.01 win_pnl=$0.01 trade_id=7107 order=face9810 fill_confirmed=1 cost=$0.98 ledger_fee=$0.00 player=Allisha Gray stat=rebounds 2/2 clock=2:44 period=1 pred_p=1.00 edge=0.02 resolution=WIN pnl=+0.01 reason=wnba_player_stat_already_reached

## Kalshi AFL Game State Audit
- command: `python3 scripts/kalshi_afl_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 10 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-04T05:17:39+00:00 | markets_checked=18 parsed=18 espn_games=9 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXAFLGAME dates=2026-07-04,2026-07-03,2026-07-05,2026-07-06,2026-07-09,2026-07-10,2026-07-11 | state_games=9 | counts=KXAFLGAME=18 | reasons=afl_game_not_final=18

## Kalshi CFL Game State Audit
- command: `python3 scripts/kalshi_cfl_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-04T05:17:39+00:00 | markets_checked=8 parsed=8 official_games=93 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXCFLGAME dates=2026-07-04,2026-07-05,2026-07-09,2026-07-10 | state_games=4 rounds_raw=27 tournaments_raw=93 supported_games=93 | counts=KXCFLGAME=8 | source_errors=0 | reasons=cfl_game_not_final=8

## Kalshi BIG3 Game State Audit
- command: `python3 scripts/kalshi_big3_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-04T05:17:56+00:00 | markets_checked=8 parsed=8 official_games=32 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXBIG3GAME dates=2026-07-05 | state_games=4 events_raw=32 supported_games=32 | counts=KXBIG3GAME=8 | source_errors=0 | reasons=big3_game_not_final=8

## Kalshi Asia Baseball Game State Audit
- command: `python3 scripts/kalshi_asia_baseball_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 12 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-04T05:17:39+00:00 | markets_checked=66 parsed=66 official_games=33 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXKBOGAME,KXNPBGAME dates=2026-07-04,2026-07-05,2026-07-07 | state_games=33 | counts=KXKBOGAME=30, KXNPBGAME=36 | source_errors=0 | reasons=npb_game_not_final=36, kbo_game_not_final=30

## Kalshi LMB Game State Audit
- command: `python3 scripts/kalshi_lmb_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 10 --pause-seconds 0.5 --max-ask 0.25 --min-depth 1 --tolerance-minutes 180`
- latest_run: captured_at=2026-07-04T05:17:39+00:00 | markets_checked=76 parsed=76 official_games=60 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXLMBGAME dates=2026-07-04,2026-07-03,2026-07-05,2026-07-02,2026-07-06,2026-07-07 | state_games=54 schedule_games=60 teams=20 | counts=KXLMBGAME=76 | source_errors=0 | reasons=lmb_game_not_final=54, no_matching_official_lmb_game_state=16, lmb_game_postponed_or_canceled=6

## Kalshi R6 Game State Audit
- command: `python3 scripts/kalshi_r6_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.5 --max-ask 0.25 --min-depth 1 --tolerance-minutes 180`
- latest_run: captured_at=2026-07-05T20:27:18+00:00 | markets_checked=4 parsed=4 official_games=48 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXR6GAME dates=2026-07-06 | state_games=4 calendar=2026-7 matches_raw=92 supported_games=48 | counts=KXR6GAME=4 | source_errors=0 | reasons=r6_game_not_final=4

## Kalshi VALORANT Game State Audit
- command: `python3 scripts/kalshi_valorant_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.5 --max-ask 0.25 --min-depth 1 --tolerance-minutes 180`
- latest_run: captured_at=2026-07-05T21:22:23+00:00 | markets_checked=36 parsed=32 official_games=80 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXVALORANTGAME dates=2026-07-05,2026-07-06,2026-07-07 | state_games=28 events_raw=80 supported_games=80 | counts=KXVALORANTGAME=36 | source_errors=0 | reasons=no_matching_official_valorant_game_state=18, valorant_game_not_final=14

## Kalshi LoL Game State Audit
- command: `python3 scripts/kalshi_lol_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.5 --max-ask 0.25 --min-depth 1 --tolerance-minutes 180`
- latest_run: captured_at=2026-07-05T21:22:23+00:00 | markets_checked=28 parsed=18 official_games=80 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXLOLGAME dates=2026-07-05,2026-07-06,2026-07-07 | state_games=14 events_raw=80 supported_games=80 | counts=KXLOLGAME=28 | source_errors=0 | reasons=lol_game_not_final=18

## Kalshi CS2 Game State Audit
- command: `python3 scripts/kalshi_cs2_game_state_audit.py --max-pages-per-series 2 --limit 1000 --hltv-offsets 2 --hltv-pause-seconds 0.2 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-05T21:22:25+00:00 | markets_checked=20 groups=10 hltv_results=72 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXCS2GAME counts=KXCS2GAME=20 | hltv_index_pairs=72 fetches=1 raw_results=72 | reasons=no_hltv_match_pair=10

## Kalshi CS2 Total Maps State Audit
- command: `python3 scripts/kalshi_cs2_total_maps_state_audit.py --max-pages-per-series 2 --limit 1000 --hltv-offsets 2 --hltv-pause-seconds 0.2 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-05T17:28:46+00:00 | markets_checked=10 parsed=10 hltv_results=16682 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXCS2TOTALMAPS counts=KXCS2TOTALMAPS=10 | hltv_index_pairs=10099 fetches=200 raw_results=16682 | reasons=no_hltv_match_pair=10

## Kalshi Tennis Final-State Audit
- command: `python3 scripts/kalshi_tennis_final_state_audit.py --series KXATPMATCH,KXWTAMATCH,KXATPDOUBLES,KXWTADOUBLES --limit 1000 --max-pages-per-series 2 --espn-event-limit 700 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-05T21:22:58+00:00 | kalshi_markets=52 groups=26 espn_matches=694 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXATPMATCH,KXWTAMATCH,KXATPDOUBLES,KXWTADOUBLES counts=KXATPDOUBLES=12, KXATPMATCH=12, KXWTADOUBLES=16, KXWTAMATCH=12 | espn_events=atp=1, wta=3 competitions=atp=320, wta=374 status_fetches=694 | reasons=espn_match_not_unique_completed=21, no_espn_match_pair=5

## Kalshi ITF Flashscore Match Audit
- command: `python3 scripts/kalshi_itf_flashscore_match_audit.py --series KXITFMATCH,KXITFWMATCH --limit 1000 --max-pages-per-series 2 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T21:22:44+00:00 | kalshi_markets=76 groups=38 flashscore_tournaments=20 flashscore_matches=591 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXITFMATCH,KXITFWMATCH counts=KXITFMATCH=36, KXITFWMATCH=40 | category_tournaments=KXITFMATCH=17, KXITFWMATCH=13 matched_tournaments=20 tournament_match_failures=0 | reasons=flashscore_match_not_unique_completed=34, no_flashscore_match_pair=4

## Kalshi Tennis Set-Score State Audit
- command: `python3 scripts/kalshi_tennis_set_score_audit.py --series KXATPSETWINNER,KXWTASETWINNER,KXATPEXACTMATCH,KXWTAEXACTMATCH --limit 1000 --max-pages-per-series 2 --espn-event-limit 700 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-03T22:21:24+00:00 | kalshi_markets=192 groups=72 espn_matches=602 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXATPSETWINNER,KXWTASETWINNER,KXATPEXACTMATCH,KXWTAEXACTMATCH counts=KXATPEXACTMATCH=72, KXATPSETWINNER=72, KXWTAEXACTMATCH=0, KXWTASETWINNER=48 | espn_events=atp=1, wta=1 competitions=atp=304, wta=298 status_fetches=602 linescore_fetches=1204 | reasons=espn_match_not_unique_completed=72

## Kalshi Esports Map Sweep Audit
- command: `python3 scripts/kalshi_esports_map_sweep_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.5 --max-ask 0.25 --min-depth 1 --tolerance-minutes 180`
- latest_run: captured_at=2026-07-05T17:26:36+00:00 | markets_checked=98 parsed=98 official_games=160 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXVALORANTMAP,KXLOLMAP dates=2026-07-05,2026-07-06,2026-07-07,2026-07-08 | state_games=70 events_raw=160 supported_games=160 | counts=KXLOLMAP=24, KXVALORANTMAP=74 | source_errors=0 | proof=completed_clean_sweep_only | reasons=no_matching_official_valorant_map_sweep_state=42, valorant_match_not_final=32, lol_match_not_final=24

## Kalshi FIBA Game State Audit
- command: `python3 scripts/kalshi_fiba_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1 --match-window-minutes 90`
- latest_run: captured_at=2026-07-04T05:17:46+00:00 | markets_checked=96 parsed=96 official_games=41 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXFIBAGAME dates=2026-06-30,2026-07-02,2026-07-04,2026-07-05,2026-07-06 | state_games=82 matched_markets=82 raw_games=210 supported_games=88 | counts=KXFIBAGAME=96 | source_errors=0 | reasons=fiba_game_not_final=82, no_matching_official_fiba_game_state=14

## Kalshi NZNBL Game State Audit
- command: `python3 scripts/kalshi_nznbl_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-04T05:17:56+00:00 | markets_checked=6 parsed=6 official_games=26 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXNZNBLGAME dates=2026-07-04,2026-07-05 | state_games=2 widget_rows=52 supported_games=26 | counts=KXNZNBLGAME=6 | source_errors=0 | reasons=nznbl_game_not_final=6

## Kalshi VBA Game State Audit
- command: `python3 scripts/kalshi_vba_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-04T05:17:56+00:00 | markets_checked=4 parsed=4 official_games=16 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXVBAGAME dates=2026-07-04,2026-07-05 | state_games=2 widget_rows=16 supported_games=16 | counts=KXVBAGAME=4 | source_errors=0 | reasons=vba_game_not_final=4

## Kalshi NBA Summer Game State Audit
- command: `python3 scripts/kalshi_nba_summer_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 10 --pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-05T20:27:48+00:00 | markets_checked=46 parsed=28 espn_games=14 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXNBASUMMERGAME dates=2026-07-05,2026-07-06,2026-07-07,2026-07-09,2026-07-10 | state_games=14 | counts=KXNBASUMMERGAME=46 | leagues=nba-summer-california=8, nba-summer-las-vegas=15, nba-summer-utah=4 | reasons=nba_summer_game_not_final=28

## Kalshi World Cup Corner State Audit
- command: `python3 scripts/kalshi_worldcup_corner_state_audit.py --max-pages-per-series 2 --limit 1000 --max-dates 8 --pause-seconds 0.25 --espn-pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-05T12:25:19+00:00 | markets_checked=0 parsed=0 espn_games=0 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXWCCORNERS,KXWCTCORNERS dates= | state_games=0 needed_events=0 | counts=KXWCCORNERS=0, KXWCTCORNERS=0 | reasons=none

## Kalshi World Cup Player Contribution State Audit
- command: `python3 scripts/kalshi_worldcup_player_contribution_state_audit.py --max-pages-per-series 2 --limit 1000 --max-dates 8 --pause-seconds 0.25 --espn-pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-04T05:17:18+00:00 | markets_checked=258 parsed=258 espn_games=6 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXWCGOAL,KXWCAST,KXWCSOA dates=2026-07-04,2026-07-05,2026-07-06 | state_games=6 needed_events=6 | counts=KXWCAST=89, KXWCGOAL=108, KXWCSOA=61 | reasons=wc_player_goal_waiting_for_threshold_or_final=108, wc_player_assist_waiting_for_threshold_or_final=89, wc_player_score_or_assist_waiting_for_threshold_or_final=61

## Kalshi World Cup Starting Lineup State Audit
- command: `python3 scripts/kalshi_worldcup_starting_lineup_state_audit.py --max-pages-per-series 2 --limit 1000 --max-dates 8 --pause-seconds 0.25 --espn-pause-seconds 0.25 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-04T05:17:14+00:00 | markets_checked=52 parsed=52 espn_games=1 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXWCSTART dates=2026-07-06 | state_games=1 needed_events=1 | counts=KXWCSTART=52 | reasons=wc_start_lineup_not_available=52

## Kalshi Soccer Game State Audit
- command: `python3 scripts/kalshi_soccer_game_state_audit.py --max-pages-per-series 4 --limit 1000 --max-dates 8 --pause-seconds 1.0 --max-ask 0.25 --min-depth 1`
- latest_run: captured_at=2026-07-05T20:27:48+00:00 | markets_checked=96 parsed=3 espn_games=4 locked_rows=0 actionable_qty1=0 | max_ask=0.25 min_depth=1 | series=KXCHNSLGAME,KXALLSVENSKANGAME,KXBRASILEIROBGAME,KXBRASILEIROCGAME,KXUSLGAME,KXECULPGAME dates=2026-07-05,2026-07-04,2026-07-06,2026-07-03,2026-07-07,2026-07-02,2026-07-08 | state_games=4 | counts=KXALLSVENSKANGAME=6, KXBRASILEIROBGAME=36, KXBRASILEIROCGAME=33, KXCHNSLGAME=0, KXECULPGAME=12, KXUSLGAME=9 | reasons=soccer_game_not_final=3

## Kalshi Broad Event-First Shadow Audit
- command: `python3 scripts/kalshi_shadow_event_first_audit.py --json`
- status: SHADOW_EVENT_FIRST_CANDIDATES | ready=false | eligible_cells=169 | candidate_cells=3 | ready_cells=0 | min_events=30 | edge_buffer=+2.0pp | scope=event-first shadow only; native execution still requires a separate forward gate
- best: shadow_longshot_fading:other:NO:weak:80-90:4-24h | gate=SHADOW_EVENT_FIRST_CANDIDATE | events=58 | 57W-1L | pnl=+817.46 | Wilson 90.9% vs target 85.4% (avg_price 83.4%) | target_gap=+5.5pp | blockers=none
- rank 1: shadow_longshot_fading:other:NO:weak:80-90:4-24h | gate=SHADOW_EVENT_FIRST_CANDIDATE | events=58 | 57W-1L | pnl=+817.46 | Wilson 90.9% vs target 85.4% (avg_price 83.4%) | target_gap=+5.5pp | blockers=none
- rank 2: shadow_longshot_fading:crypto:NO:moderate:80-90:<1h | gate=SHADOW_EVENT_FIRST_CANDIDATE | events=647 | 598W-49L | pnl=+2658.32 | Wilson 90.1% vs target 89.6% (avg_price 87.6%) | target_gap=+0.6pp | blockers=none
- rank 3: shadow_longshot_fading:crypto:NO:weak:80-90:<1h | gate=SHADOW_EVENT_FIRST_CANDIDATE | events=929 | 813W-116L | pnl=+3386.45 | Wilson 85.2% vs target 84.9% (avg_price 82.9%) | target_gap=+0.4pp | blockers=none

## Kalshi Shadow Longshot Stability Audit
- command: `python3 scripts/kalshi_shadow_longshot_stability_audit.py --limit 8`
- status: NO_SHADOW_STABILITY_CANDIDATES | ready=false | event_rows=7753 | eligible_cells=25 | base_candidate_cells=3 | stable_candidate_cells=0 | ready_cells=0 | min_events=30 | min_train=30 | min_validation=15 | min_slice=20 | edge_buffer=+2.0pp
- 1. shadow_longshot_fading:other:NO:weak:80-90:4-24h | gate=SHADOW_STABILITY_REJECT | aggregate=58ev 57W-1L +817.46 Wilson 90.9% vs target 85.4% gap +5.5pp | train=40ev 39W-1L +517.32 Wilson 87.1% vs target 85.8% gap +1.3pp | validation=18ev 18W-0L +300.14 Wilson 82.4% vs target 84.4% gap -2.0pp | worst_asset=none>=min_slice | worst_hour=none>=min_slice | blockers=validation_wilson<avg_price+buffer
- 2. shadow_longshot_fading:crypto:NO:moderate:80-90:<1h | gate=SHADOW_STABILITY_REJECT | aggregate=647ev 598W-49L +2658.32 Wilson 90.1% vs target 89.6% gap +0.6pp | train=452ev 419W-33L +1967.66 Wilson 89.9% vs target 89.6% gap +0.3pp | validation=195ev 179W-16L +690.66 Wilson 87.1% vs target 89.5% gap -2.4pp | worst_asset=KXETHD 104ev 97W-7L +531.19 Wilson 86.8% vs target 89.4% gap -2.6pp | worst_hour=15Z 26ev 19W-7L -396.92 Wilson 53.9% vs target 89.6% gap -35.7pp | blockers=validation_wilson<avg_price+buffer;asset_slice_wilson<avg_price:KXETHD;utc_hour_slice_pnl<=0:15Z;utc_hour_slice_wilson<avg_price:15Z
- 3. shadow_longshot_fading:crypto:NO:weak:80-90:<1h | gate=SHADOW_STABILITY_REJECT | aggregate=929ev 813W-116L +3386.45 Wilson 85.2% vs target 84.9% gap +0.4pp | train=650ev 579W-71L +3556.36 Wilson 86.4% vs target 84.6% gap +1.8pp | validation=279ev 234W-45L -169.91 Wilson 79.1% vs target 85.5% gap -6.4pp | worst_asset=KXSOLD 173ev 152W-21L +605.10 Wilson 82.2% vs target 85.4% gap -3.2pp | worst_hour=13Z 38ev 27W-11L -504.02 Wilson 55.2% vs target 85.3% gap -30.1pp | blockers=validation_pnl<=0;validation_wilson<avg_price+buffer;asset_slice_wilson<avg_price:KXSOLD;utc_hour_slice_pnl<=0:13Z;utc_hour_slice_wilson<avg_price:13Z

## Kalshi Shadow Longshot Filtered Stability Audit
- command: `python3 scripts/kalshi_shadow_longshot_filtered_stability_audit.py --limit 8`
- status: NO_FILTERED_SHADOW_STABILITY_CANDIDATES | ready=false | event_rows=7753 | base_candidate_cells=3 | filtered_cells=74 | filtered_candidate_cells=0 | ready_cells=0 | min_events=30 | min_train=30 | min_validation=15 | min_slice=20 | edge_buffer=+2.0pp
- 1. shadow_longshot_fading:crypto:NO:moderate:80-90:<1h|exclude_asset=KXETHD,exclude_hour=15Z | gate=FILTERED_SHADOW_STABILITY_REJECT | filter=exclude_asset=KXETHD,exclude_hour=15Z | excluded=126 | aggregate=521ev 485W-36L +2467.19 Wilson 90.6% vs target 89.6% gap +1.0pp | train=364ev 338W-26L +1624.17 Wilson 89.7% vs target 89.6% gap +0.1pp | validation=157ev 147W-10L +843.02 Wilson 88.7% vs target 89.5% gap -0.8pp | worst_asset=KXSOLD 112ev 105W-7L +610.98 Wilson 87.7% vs target 89.5% gap -1.9pp | worst_hour=13Z 21ev 17W-4L -156.02 Wilson 60.0% vs target 89.6% gap -29.6pp | blockers=validation_wilson<avg_price+buffer;utc_hour_slice_pnl<=0:13Z;utc_hour_slice_wilson<avg_price:13Z
- 2. shadow_longshot_fading:crypto:NO:moderate:80-90:<1h|exclude_hour=15Z | gate=FILTERED_SHADOW_STABILITY_REJECT | filter=exclude_hour=15Z | excluded=26 | aggregate=621ev 579W-42L +3055.24 Wilson 91.0% vs target 89.6% gap +1.4pp | train=434ev 405W-29L +2160.31 Wilson 90.6% vs target 89.6% gap +1.0pp | validation=187ev 174W-13L +894.93 Wilson 88.5% vs target 89.5% gap -1.0pp | worst_asset=KXSOLD 112ev 105W-7L +610.98 Wilson 87.7% vs target 89.5% gap -1.9pp | worst_hour=13Z 23ev 19W-4L -131.61 Wilson 62.9% vs target 89.6% gap -26.7pp | blockers=validation_wilson<avg_price+buffer;utc_hour_slice_pnl<=0:13Z;utc_hour_slice_wilson<avg_price:13Z
- 3. shadow_longshot_fading:crypto:NO:moderate:80-90:<1h|exclude_hour=02Z | gate=FILTERED_SHADOW_STABILITY_REJECT | filter=exclude_hour=02Z | excluded=38 | aggregate=609ev 565W-44L +2695.52 Wilson 90.4% vs target 89.6% gap +0.9pp | train=426ev 395W-31L +1848.46 Wilson 89.9% vs target 89.6% gap +0.2pp | validation=183ev 170W-13L +847.06 Wilson 88.2% vs target 89.5% gap -1.3pp | worst_asset=KXSOLD 107ev 100W-7L +542.38 Wilson 87.1% vs target 89.6% gap -2.5pp | worst_hour=15Z 26ev 19W-7L -396.92 Wilson 53.9% vs target 89.6% gap -35.7pp | blockers=validation_wilson<avg_price+buffer;asset_slice_wilson<avg_price:KXSOLD;utc_hour_slice_pnl<=0:15Z;utc_hour_slice_wilson<avg_price:15Z
- 4. shadow_longshot_fading:crypto:NO:moderate:80-90:<1h|exclude_hour=13Z | gate=FILTERED_SHADOW_STABILITY_REJECT | filter=exclude_hour=13Z | excluded=23 | aggregate=624ev 579W-45L +2789.93 Wilson 90.5% vs target 89.6% gap +0.9pp | train=436ev 405W-31L +1979.96 Wilson 90.1% vs target 89.6% gap +0.5pp | validation=188ev 174W-14L +809.97 Wilson 87.9% vs target 89.5% gap -1.6pp | worst_asset=KXETHD 102ev 95W-7L +506.78 Wilson 86.5% vs target 89.4% gap -2.9pp | worst_hour=15Z 26ev 19W-7L -396.92 Wilson 53.9% vs target 89.6% gap -35.7pp | blockers=validation_wilson<avg_price+buffer;asset_slice_wilson<avg_price:KXETHD;utc_hour_slice_pnl<=0:15Z;utc_hour_slice_wilson<avg_price:15Z
- 5. shadow_longshot_fading:crypto:NO:moderate:80-90:<1h|exclude_hour=05Z | gate=FILTERED_SHADOW_STABILITY_REJECT | filter=exclude_hour=05Z | excluded=21 | aggregate=626ev 579W-47L +2606.77 Wilson 90.2% vs target 89.6% gap +0.6pp | train=438ev 405W-33L +1799.64 Wilson 89.6% vs target 89.6% gap +0.0pp | validation=188ev 174W-14L +807.13 Wilson 87.9% vs target 89.5% gap -1.6pp | worst_asset=KXETHD 100ev 93W-7L +482.37 Wilson 86.3% vs target 89.4% gap -3.2pp | worst_hour=15Z 26ev 19W-7L -396.92 Wilson 53.9% vs target 89.6% gap -35.7pp | blockers=validation_wilson<avg_price+buffer;asset_slice_wilson<avg_price:KXETHD;utc_hour_slice_pnl<=0:15Z;utc_hour_slice_wilson<avg_price:15Z
- 6. shadow_longshot_fading:crypto:NO:moderate:80-90:<1h|exclude_hour=09Z | gate=FILTERED_SHADOW_STABILITY_REJECT | filter=exclude_hour=09Z | excluded=23 | aggregate=624ev 576W-48L +2491.85 Wilson 89.9% vs target 89.5% gap +0.4pp | train=436ev 402W-34L +1684.71 Wilson 89.3% vs target 89.6% gap -0.3pp | validation=188ev 174W-14L +807.14 Wilson 87.9% vs target 89.5% gap -1.6pp | worst_asset=KXETHD 100ev 93W-7L +483.33 Wilson 86.3% vs target 89.4% gap -3.1pp | worst_hour=15Z 26ev 19W-7L -396.92 Wilson 53.9% vs target 89.6% gap -35.7pp | blockers=train_wilson<avg_price+buffer;validation_wilson<avg_price+buffer;asset_slice_wilson<avg_price:KXETHD;utc_hour_slice_pnl<=0:15Z;utc_hour_slice_wilson<avg_price:15Z
- 7. shadow_longshot_fading:crypto:NO:moderate:80-90:<1h|exclude_hour=21Z | gate=FILTERED_SHADOW_STABILITY_REJECT | filter=exclude_hour=21Z | excluded=26 | aggregate=621ev 574W-47L +2559.02 Wilson 90.1% vs target 89.5% gap +0.5pp | train=434ev 401W-33L +1760.30 Wilson 89.5% vs target 89.6% gap -0.1pp | validation=187ev 173W-14L +798.72 Wilson 87.8% vs target 89.5% gap -1.6pp | worst_asset=KXSOLD 113ev 105W-8L +521.29 Wilson 86.6% vs target 89.5% gap -2.9pp | worst_hour=15Z 26ev 19W-7L -396.92 Wilson 53.9% vs target 89.6% gap -35.7pp | blockers=train_wilson<avg_price+buffer;validation_wilson<avg_price+buffer;asset_slice_wilson<avg_price:KXSOLD;utc_hour_slice_pnl<=0:15Z;utc_hour_slice_wilson<avg_price:15Z
- 8. shadow_longshot_fading:crypto:NO:moderate:80-90:<1h|exclude_hour=07Z | gate=FILTERED_SHADOW_STABILITY_REJECT | filter=exclude_hour=07Z | excluded=27 | aggregate=620ev 573W-47L +2543.96 Wilson 90.1% vs target 89.6% gap +0.5pp | train=434ev 401W-33L +1755.56 Wilson 89.5% vs target 89.6% gap -0.1pp | validation=186ev 172W-14L +788.40 Wilson 87.8% vs target 89.5% gap -1.7pp | worst_asset=KXSOLD 114ev 106W-8L +534.43 Wilson 86.8% vs target 89.5% gap -2.8pp | worst_hour=15Z 26ev 19W-7L -396.92 Wilson 53.9% vs target 89.6% gap -35.7pp | blockers=train_wilson<avg_price+buffer;validation_wilson<avg_price+buffer;asset_slice_wilson<avg_price:KXSOLD;utc_hour_slice_pnl<=0:15Z;utc_hour_slice_wilson<avg_price:15Z

## Kalshi Legacy Shadow Surface Audit
- command: `python3 scripts/kalshi_legacy_shadow_surface_audit.py --limit 8`
- status: LEGACY_SHADOW_FORWARD_REQUIRED | ready=false | eligible_cells=144 | candidate_cells=1 | ready_cells=0 | min_events=30 | edge_buffer=+2.0pp | scope=legacy_shadow_only_requires_native_or_maker_forward_gate
- best: moderate_favorites:CRYPTO:ETH:YES:80-90:0-1H:liq1:spread1 | gate=LEGACY_SHADOW_FORWARD_REQUIRED | execution=legacy_taker_like_shadow | events=77 | 74W-3L | pnl=+$1033.00 | Wilson 89.2% vs target 84.5% (BE 82.5%, avg_price 82.7%) | gap=+4.6pp | blockers=none | promotion_blockers=requires_native_or_maker_forward_gate
- rank 1: moderate_favorites:CRYPTO:ETH:YES:80-90:0-1H:liq1:spread1 | gate=LEGACY_SHADOW_FORWARD_REQUIRED | execution=legacy_taker_like_shadow | events=77 | 74W-3L | pnl=+$1033.00 | Wilson 89.2% vs target 84.5% (BE 82.5%, avg_price 82.7%) | gap=+4.6pp | blockers=none | promotion_blockers=requires_native_or_maker_forward_gate
- rank 2: weather_city_bid_side:KXHIGHTSEA:NO:90-95:unblocked | gate=LEGACY_SHADOW_REJECT | execution=legacy_bid_side_maker | events=49 | 49W-0L | pnl=+$352.48 | Wilson 92.7% vs target 94.8% (BE 92.8%, avg_price 92.3%) | gap=-2.0pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=21
- rank 3: weather_city_bid_side:KXHIGHTMIN:NO:90-95:unblocked | gate=LEGACY_SHADOW_REJECT | execution=legacy_bid_side_maker | events=48 | 48W-0L | pnl=+$340.30 | Wilson 92.6% vs target 94.9% (BE 92.9%, avg_price 92.4%) | gap=-2.3pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=24
- rank 4: untapped_bid_side:FX:NO:90-95:4-24h | gate=LEGACY_SHADOW_REJECT | execution=legacy_bid_side_maker | events=47 | 47W-0L | pnl=+$324.36 | Wilson 92.4% vs target 95.1% (BE 93.1%, avg_price 92.6%) | gap=-2.6pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=28
- rank 5: weather_city_bid_side:KXHIGHTHOU:NO:90-95:unblocked | gate=LEGACY_SHADOW_REJECT | execution=legacy_bid_side_maker | events=45 | 45W-0L | pnl=+$315.97 | Wilson 92.1% vs target 94.9% (BE 92.9%, avg_price 92.5%) | gap=-2.8pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=28
- rank 6: weather_city_bid_side:KXHIGHMIA:NO:90-95:unblocked | gate=LEGACY_SHADOW_REJECT | execution=legacy_bid_side_maker | events=41 | 41W-0L | pnl=+$311.51 | Wilson 91.4% vs target 94.4% (BE 92.4%, avg_price 91.9%) | gap=-2.9pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=24
- rank 7: sell_inverse:WEATHER:NO:95+:4-24h | gate=LEGACY_SHADOW_REJECT | execution=legacy_inverse_shadow | events=765 | 8W-757L | pnl=-$610.21 | Wilson 0.5% vs target 3.9% (BE 1.9%, avg_price 98.3%) | gap=-3.3pp | blockers=pnl<=0;wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=34
- rank 8: price_range_bid_side:CRYPTO:YES:90-95:4-24h | gate=LEGACY_SHADOW_REJECT | execution=legacy_bid_side_maker | events=47 | 47W-0L | pnl=+$286.70 | Wilson 92.4% vs target 95.9% (BE 93.9%, avg_price 93.5%) | gap=-3.4pp | blockers=wilson<BE+2pp | promotion_blockers=none | perfect_wins_needed=43

## Kalshi Moderate Favorites ETH YES Native Preflight
- command: `python3 scripts/kalshi_moderate_favorites_eth_yes_preflight.py --json --fetch-delay-seconds 0`
- latest_run: captured_at=2026-07-07T12:16:04+00:00 | cohort=moderate_favorites_eth_yes_80_90_0_1h_v1 | start=2026-07-03T16:50:00+00:00 | include_pre_cutoff_live=false | candidates=0 checked=0 actionable_qty1=0 | top_reasons=none

## Kalshi Weather YES 90-93 Native Preflight
- command: `python3 scripts/kalshi_weather_yes_90_93_preflight.py --json --fetch-delay-seconds 0`
- latest_run: captured_at=2026-07-07T12:15:32+00:00 | cohort=yes_90_93_above_live_threshold_v1 | start=2026-06-25T11:45:00+00:00 | include_pre_cutoff_live=true | candidates=0 checked=0 actionable_qty1=0 | top_reasons=none

## Kalshi Weather NO Candidate Native Preflight
- command: `python3 scripts/kalshi_weather_no_candidate_preflight.py --json --fetch-delay-seconds 0`
- latest_run: captured_at=2026-07-07T12:18:53+00:00 | start=2026-06-25T07:05:00+00:00 | include_pre_cutoff_live=true | candidates=8 checked=8 actionable_qty1=5 | top_reasons=no_95_98_zero_loss_cities_v1:actionable_qty1_fee_positive=5, no_90_95_min_probe_v1:native_no_ask_out_of_band:0.9900=1, no_95_98_zero_loss_cities_v1:missing_native_no_ask=1, no_95_98_zero_loss_cities_v1:native_no_ask_out_of_band:0.9100=1
- latest_rows: KXHIGHTDAL-26JUL07-B94.5 cohort=no_95_98_zero_loss_cities_v1 city=DAL no_ask=0.98 no_ask_depth=1835 qty1=+0.01/-0.99 reason=actionable_qty1_fee_positive due=2026-07-08T19:00:00+00:00 ; KXHIGHMIA-26JUL07-B88.5 cohort=no_95_98_zero_loss_cities_v1 city=MIA no_ask=0.96 no_ask_depth=48 qty1=+0.03/-0.97 reason=actionable_qty1_fee_positive due=2026-07-08T14:00:00+00:00 ; KXHIGHTMIN-26JUL07-T86 cohort=no_95_98_zero_loss_cities_v1 city=MIN no_ask=0.95 no_ask_depth=20 qty1=+0.04/-0.96 reason=actionable_qty1_fee_positive due=2026-07-08T19:00:00+00:00 ; KXHIGHTOKC-26JUL07-T91 cohort=no_95_98_zero_loss_cities_v1 city=OKC no_ask=0.96 no_ask_depth=1054 qty1=+0.03/-0.97 reason=actionable_qty1_fee_positive due=2026-07-08T19:00:00+00:00 ; KXHIGHTSEA-26JUL07-B81.5 cohort=no_95_98_zero_loss_cities_v1 city=SEA no_ask=0.97 no_ask_depth=126 qty1=+0.02/-0.98 reason=actionable_qty1_fee_positive due=2026-07-08T19:00:00+00:00 ; KXHIGHTMIN-26JUL07-T93 cohort=no_90_95_min_probe_v1 city=MIN no_ask=0.99 no_ask_depth=484 qty1=+0.00/-1.00 reason=native_no_ask_out_of_band:0.9900 due=2026-07-08T19:00:00+00:00 ; KXLOWTAUS-26JUL07-B77.5 cohort=no_95_98_zero_loss_cities_v1 city=AUS no_ask=missing no_ask_depth=0 qty1=n/a/n/a reason=missing_native_no_ask due=2026-07-08T19:00:00+00:00 ; KXHIGHTLV-26JUL07-B110.5 cohort=no_95_98_zero_loss_cities_v1 city=LV no_ask=0.91 no_ask_depth=5 qty1=+0.08/-0.92 reason=native_no_ask_out_of_band:0.9100 due=2026-07-08T19:00:00+00:00

## Kalshi Other Longshot NO Native Preflight
- command: `python3 scripts/kalshi_other_longshot_no_80_90_preflight.py --json --fetch-delay-seconds 0`
- latest_run: captured_at=2026-07-07T12:16:12+00:00 | cohort=all | start=2026-06-25T20:00:00+00:00 | include_pre_cutoff_live=true | candidates=6 checked=6 actionable_qty1=0 | top_reasons=other_strong_no_90_95_4_24h_v1:missing_native_no_ask=2, other_weak_no_80_90_4_24h_v1:missing_native_no_ask=2, other_strong_no_90_95_4_24h_v1:native_no_ask_out_of_band:0.9500=1, other_strong_no_90_95_4_24h_v1:native_no_ask_out_of_band:0.9800=1
- latest_rows: KXUSDJPY-26JUL0710-B163.125 cohort=other_strong_no_90_95_4_24h_v1 group=FX no_ask=0.98 no_ask_depth=100 spread=0.04 qty1=+0.01/-0.99 reason=native_no_ask_out_of_band:0.9800 ; KXEURUSD-26JUL0710-B1.147 cohort=other_strong_no_90_95_4_24h_v1 group=FX no_ask=0.95 no_ask_depth=4 spread=0.27 qty1=+0.04/-0.96 reason=native_no_ask_out_of_band:0.9500 ; KXINX-26JUL07H1600-B7812 cohort=other_weak_no_80_90_4_24h_v1 group=INDEX no_ask=missing no_ask_depth=0 spread=unknown qty1=n/a/n/a reason=missing_native_no_ask ; KXINX-26JUL07H1600-B7812 cohort=other_strong_no_90_95_4_24h_v1 group=INDEX no_ask=missing no_ask_depth=0 spread=unknown qty1=n/a/n/a reason=missing_native_no_ask ; KXNASDAQ100-26JUL07H1600-B30650 cohort=other_weak_no_80_90_4_24h_v1 group=INDEX no_ask=missing no_ask_depth=0 spread=unknown qty1=n/a/n/a reason=missing_native_no_ask

## Kalshi Index/FX Low-Price NO Favtrack Native Preflight
- command: `python3 scripts/kalshi_index_fx_low_price_no_favorite_tracking_preflight.py --json --fetch-delay-seconds 0`
- methodology_status: non-live favorite_tracking source; native-forward evidence only
- latest_run: captured_at=2026-07-05T21:13:24+00:00 | start=2026-06-26T17:10:00+00:00 | include_pre_cutoff_live=false | candidates=0 checked=0 actionable_qty1=0 | top_reasons=none

## Kalshi Maker Forward Proxy Leaderboard
- command: `python3 scripts/kalshi_maker_forward_leaderboard.py --json`
- status: NO_LIVE_READY | ready=false | cells=15 | ready_cells=0 | review_min=50 | fills=2529 pending_units=388 active=388 stale=0 unknown=0 overall_resolved_indep=2141 toxic=787 | next_pending=cell_crypto_no:KXSOLD-26JUL0709-T81.9999 status=active close=2026-07-07T13:00:00+00:00
- best: cell_sports_no | gate=NO_GO_REVIEW | resolved_indep=707/50 max_if_pending_resolve=932 new_needed_after_pending=0 | 509W-198L | pnl=-1084.11 | Wilson 68.6% vs BE 87.3% | gap=-18.8pp | fills=932/3665 fill_rate=25.4% pending_units=225 active=225 stale=0 unknown=0 toxic=198 | blockers=pnl<=0; wilson<=BE; toxic>0 | perfect_benign_wins_needed=blocked_or_>5000 | next_pending=KXMLBSPREAD-26JUL041105PITWSH-PIT6 status=active close=2026-07-07T15:05:00+00:00 price=0.87
- rank 1: cell_sports_no | gate=NO_GO_REVIEW | resolved_indep=707/50 max_if_pending_resolve=932 new_needed_after_pending=0 | 509W-198L | pnl=-1084.11 | Wilson 68.6% vs BE 87.3% | gap=-18.8pp | fills=932/3665 fill_rate=25.4% pending_units=225 active=225 stale=0 unknown=0 toxic=198 | blockers=pnl<=0; wilson<=BE; toxic>0 | perfect_benign_wins_needed=blocked_or_>5000 | next_pending=KXMLBSPREAD-26JUL041105PITWSH-PIT6 status=active close=2026-07-07T15:05:00+00:00 price=0.87
- rank 2: cell_crypto_no | gate=NO_GO_REVIEW | resolved_indep=432/50 max_if_pending_resolve=450 new_needed_after_pending=0 | 215W-217L | pnl=-1577.75 | Wilson 45.1% vs BE 86.3% | gap=-41.2pp | fills=450/1478 fill_rate=30.4% pending_units=18 active=18 stale=0 unknown=0 toxic=217 | blockers=pnl<=0; wilson<=BE; toxic>0 | perfect_benign_wins_needed=blocked_or_>5000 | next_pending=KXSOLD-26JUL0709-T81.9999 status=active close=2026-07-07T13:00:00+00:00 price=0.91
- rank 3: cell_crypto_yes | gate=NO_GO_REVIEW | resolved_indep=399/50 max_if_pending_resolve=425 new_needed_after_pending=0 | 223W-176L | pnl=-1212.58 | Wilson 51.0% vs BE 86.3% | gap=-35.3pp | fills=425/1429 fill_rate=29.7% pending_units=26 active=26 stale=0 unknown=0 toxic=176 | blockers=pnl<=0; wilson<=BE; toxic>0 | perfect_benign_wins_needed=blocked_or_>5000 | next_pending=KXBTCD-26JUL0717-T61999.99 status=active close=2026-07-07T21:00:00+00:00 price=0.94
- rank 4: cell_sports_yes | gate=NO_GO_REVIEW | resolved_indep=272/50 max_if_pending_resolve=364 new_needed_after_pending=0 | 126W-146L | pnl=-1112.39 | Wilson 40.5% vs BE 87.2% | gap=-46.7pp | fills=364/568 fill_rate=64.1% pending_units=92 active=92 stale=0 unknown=0 toxic=146 | blockers=pnl<=0; wilson<=BE; toxic>0 | perfect_benign_wins_needed=blocked_or_>5000 | next_pending=KXMLBSPREAD-26JUL041105PITWSH-PIT5 status=active close=2026-07-07T15:05:00+00:00 price=0.88
- rank 5: cell_weather_no | gate=NO_GO_REVIEW | resolved_indep=165/50 max_if_pending_resolve=170 new_needed_after_pending=0 | 134W-31L | pnl=-133.80 | Wilson 74.6% vs BE 89.3% | gap=-14.8pp | fills=170/378 fill_rate=45.0% pending_units=5 active=5 stale=0 unknown=0 toxic=31 | blockers=pnl<=0; wilson<=BE; toxic>0 | perfect_benign_wins_needed=blocked_or_>5000 | next_pending=KXHIGHMIA-26JUL07-B90.5 status=active close=2026-07-08T04:59:00+00:00 price=0.79
- rank 6: watch_crypto_bid_90_95 | gate=NO_GO_REVIEW | resolved_indep=139/50 max_if_pending_resolve=144 new_needed_after_pending=0 | 130W-9L | pnl=-2.42 | Wilson 88.2% vs BE 93.7% | gap=-5.5pp | fills=144/618 fill_rate=23.3% pending_units=5 active=5 stale=0 unknown=0 toxic=9 | blockers=pnl<=0; wilson<=BE; toxic>0 | perfect_benign_wins_needed=blocked_or_>5000 | next_pending=KXBTCD-26JUL0717-T61999.99 status=active close=2026-07-07T21:00:00+00:00 price=0.94
- rank 7: cell_index_no | gate=NO_GO_REVIEW | resolved_indep=127/50 max_if_pending_resolve=149 new_needed_after_pending=0 | 113W-14L | pnl=-39.44 | Wilson 82.3% vs BE 92.0% | gap=-9.7pp | fills=149/3350 fill_rate=4.4% pending_units=22 active=22 stale=0 unknown=0 toxic=14 | blockers=pnl<=0; wilson<=BE; toxic>0 | perfect_benign_wins_needed=blocked_or_>5000 | next_pending=KXINX-26JUL07H1600-B7462 status=active close=2026-07-07T20:00:00+00:00 price=0.93
- rank 8: watch_crypto_bid_92_94 | gate=NO_GO_REVIEW | resolved_indep=83/50 max_if_pending_resolve=87 new_needed_after_pending=0 | 79W-4L | pnl=+8.19 | Wilson 88.3% vs BE 94.2% | gap=-5.9pp | fills=87/333 fill_rate=26.1% pending_units=4 active=4 stale=0 unknown=0 toxic=4 | blockers=wilson<=BE; toxic>0 | perfect_benign_wins_needed=blocked_or_>5000 | next_pending=KXBTCD-26JUL0717-T61999.99 status=active close=2026-07-07T21:00:00+00:00 price=0.94

## Kalshi Maker Price-Band Cut Audit
- query: `kalshi_high_price_maker_cancel_shadow` grouped by category/side/maker_price_band
- scope: discovery-only subcell audit; live trading still requires the main maker gate and toxic=0
- status: NO_MAKER_CUT_READY | ready=false | cells=24 | display_cells=20 | ready_cells=0 | positive_cells=4 | review_min=50
- best: index NO maker_band=85-90 | gate=ACCUMULATING | resolved_indep=16/50 | 15W-1L | pnl=+9.64 | Wilson 71.7% vs BE 87.7% | gap=-16.0pp | candidates=471 fills=17 fill_rate=3.6% pending_units=1 toxic=1 | blockers=resolved<50; wilson<=BE; toxic>0
- rank 1: index NO maker_band=85-90 | gate=ACCUMULATING | resolved_indep=16/50 | 15W-1L | pnl=+9.64 | Wilson 71.7% vs BE 87.7% | gap=-16.0pp | candidates=471 fills=17 fill_rate=3.6% pending_units=1 toxic=1 | blockers=resolved<50; wilson<=BE; toxic>0
- rank 2: weather YES maker_band=<85 | gate=ACCUMULATING | resolved_indep=20/50 | 17W-3L | pnl=+5.56 | Wilson 64.0% vs BE 82.2% | gap=-18.3pp | candidates=39 fills=20 fill_rate=51.3% pending_units=0 toxic=3 | blockers=resolved<50; wilson<=BE; toxic>0
- rank 3: weather YES maker_band=90-95 | gate=ACCUMULATING | resolved_indep=6/50 | 6W-0L | pnl=+4.65 | Wilson 61.0% vs BE 92.2% | gap=-31.3pp | candidates=16 fills=6 fill_rate=37.5% pending_units=0 toxic=0 | blockers=resolved<50; wilson<=BE
- rank 4: crypto YES maker_band=90-95 | gate=NO_GO_REVIEW | resolved_indep=119/50 | 105W-14L | pnl=-58.37 | Wilson 81.2% vs BE 93.1% | gap=-11.9pp | candidates=474 fills=126 fill_rate=26.6% pending_units=7 toxic=14 | blockers=pnl<=0; wilson<=BE; toxic>0
- rank 5: index NO maker_band=90-95 | gate=NO_GO_REVIEW | resolved_indep=107/50 | 94W-13L | pnl=-55.72 | Wilson 80.3% vs BE 93.0% | gap=-12.7pp | candidates=2825 fills=128 fill_rate=4.5% pending_units=21 toxic=13 | blockers=pnl<=0; wilson<=BE; toxic>0
- rank 6: weather NO maker_band=90-95 | gate=NO_GO_REVIEW | resolved_indep=84/50 | 74W-10L | pnl=-45.73 | Wilson 79.5% vs BE 93.5% | gap=-14.1pp | candidates=220 fills=86 fill_rate=39.1% pending_units=2 toxic=10 | blockers=pnl<=0; wilson<=BE; toxic>0
- rank 7: sports NO maker_band=<85 | gate=NO_GO_REVIEW | resolved_indep=271/50 | 187W-84L | pnl=-364.44 | Wilson 63.3% vs BE 82.5% | gap=-19.2pp | candidates=2048 fills=370 fill_rate=18.1% pending_units=99 toxic=84 | blockers=pnl<=0; wilson<=BE; toxic>0
- rank 8: sports NO maker_band=85-90 | gate=NO_GO_REVIEW | resolved_indep=211/50 | 152W-59L | pnl=-331.74 | Wilson 65.6% vs BE 87.8% | gap=-22.1pp | candidates=982 fills=274 fill_rate=27.9% pending_units=63 toxic=59 | blockers=pnl<=0; wilson<=BE; toxic>0

## Kalshi Maker Walk-Forward Validation
- command: `python3 scripts/kalshi_maker_walkforward.py --limit 8`
- status: NO_MAKER_WALKFORWARD_CUT | ready=false | observations=2529 | cuts=189 | display_cuts=131 | validated_cuts=0 | ready_cuts=0 | split_cutoff=2026-06-30T19:37:35+00:00 | min_train=30 | min_validation=15 | edge_buffer=+2.0pp | scope=posthoc_maker_cut_walkforward_requires_predeclared_live_spec
- best: maker_all_fills|category=crypto|spread_band=<=2c | gate=MAKER_WALKFORWARD_REJECT | type=pair | train=95 resolved 85W-10L +$12.57 toxic=10 Wilson 81.7% vs target 90.2% gap=-8.5pp | validation=108 resolved 100W-8L +$31.11 toxic=8 Wilson 86.1% vs target 91.7% gap=-5.7pp | blockers=train_toxic>0;train_wilson<BE+buffer;validation_toxic>0;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXBTCD-26JUL0717-T61999.99 status=active due=2026-07-07T21:00:00+00:00 price=0.94
- rank 1: maker_all_fills|category=crypto|spread_band=<=2c | gate=MAKER_WALKFORWARD_REJECT | type=pair | train=95 resolved 85W-10L +$12.57 toxic=10 Wilson 81.7% vs target 90.2% gap=-8.5pp | validation=108 resolved 100W-8L +$31.11 toxic=8 Wilson 86.1% vs target 91.7% gap=-5.7pp | blockers=train_toxic>0;train_wilson<BE+buffer;validation_toxic>0;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXBTCD-26JUL0717-T61999.99 status=active due=2026-07-07T21:00:00+00:00 price=0.94
- rank 2: maker_all_fills|category=weather|spread_band=<=5c | gate=MAKER_WALKFORWARD_REJECT | type=pair | train=25 resolved 21W-4L -$8.48 toxic=4 Wilson 65.3% vs target 89.4% gap=-24.0pp | validation=29 resolved 28W-1L +$23.08 toxic=1 Wilson 82.8% vs target 90.6% gap=-7.8pp | blockers=train_resolved<30;train_pnl<=0;train_toxic>0;train_wilson<BE+buffer;validation_toxic>0;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXHIGHMIA-26JUL07-B90.5 status=active due=2026-07-08T04:59:00+00:00 price=0.79
- rank 3: maker_all_fills|spread_band=<=2c | gate=MAKER_WALKFORWARD_REJECT | type=single | train=257 resolved 220W-37L -$74.31 toxic=37 Wilson 80.8% vs target 90.5% gap=-9.7pp | validation=175 resolved 155W-20L -$6.42 toxic=20 Wilson 83.0% vs target 90.9% gap=-7.9pp | blockers=train_pnl<=0;train_toxic>0;train_wilson<BE+buffer;validation_pnl<=0;validation_toxic>0;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXMLBSPREAD-26JUL041105PITWSH-WSH2 status=active due=2026-07-07T15:05:00+00:00 price=0.79
- rank 4: maker_all_fills|side=YES|side_bid_band=80-85 | gate=MAKER_WALKFORWARD_REJECT | type=pair | train=52 resolved 44W-8L -$5.74 toxic=8 Wilson 72.5% vs target 87.7% gap=-15.2pp | validation=43 resolved 39W-4L +$21.57 toxic=4 Wilson 78.4% vs target 87.7% gap=-9.3pp | blockers=train_pnl<=0;train_toxic>0;train_wilson<BE+buffer;validation_toxic>0;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXMLBSPREAD-26JUL041335MINNYY-MIN5 status=active due=2026-07-07T17:35:00+00:00 price=0.92
- rank 5: maker_all_fills|side_bid_band=92-94 | gate=MAKER_WALKFORWARD_REJECT | type=single | train=88 resolved 81W-7L -$18.00 toxic=7 Wilson 84.5% vs target 96.1% gap=-11.6pp | validation=72 resolved 68W-4L +$2.13 toxic=4 Wilson 86.6% vs target 96.1% gap=-9.6pp | blockers=train_pnl<=0;train_toxic>0;train_wilson<BE+buffer;validation_toxic>0;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXMLBSPREAD-26JUL041335MINNYY-NYY3 status=active due=2026-07-07T17:35:00+00:00 price=0.94
- rank 6: maker_all_fills|category=crypto|side_bid_band=92-94 | gate=MAKER_WALKFORWARD_REJECT | type=pair | train=28 resolved 27W-1L +$6.31 toxic=1 Wilson 82.3% vs target 96.2% gap=-13.9pp | validation=55 resolved 52W-3L +$1.88 toxic=3 Wilson 85.1% vs target 96.2% gap=-11.1pp | blockers=train_resolved<30;train_toxic>0;train_wilson<BE+buffer;validation_toxic>0;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXBTCD-26JUL0717-T61999.99 status=active due=2026-07-07T21:00:00+00:00 price=0.94
- rank 7: maker_all_fills|side_bid_band=90-92 | gate=MAKER_WALKFORWARD_REJECT | type=single | train=69 resolved 63W-6L -$11.37 toxic=6 Wilson 82.3% vs target 94.9% gap=-12.6pp | validation=47 resolved 44W-3L +$3.23 toxic=3 Wilson 82.8% vs target 94.9% gap=-12.1pp | blockers=train_pnl<=0;train_toxic>0;train_wilson<BE+buffer;validation_toxic>0;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXMLBSPREAD-26JUL041335MINNYY-NYY2 status=active due=2026-07-07T17:35:00+00:00 price=0.94
- rank 8: maker_all_fills|side=YES|side_bid_band=92-94 | gate=MAKER_WALKFORWARD_REJECT | type=pair | train=19 resolved 18W-1L +$1.18 toxic=1 Wilson 75.4% vs target 96.1% gap=-20.8pp | validation=31 resolved 30W-1L +$8.17 toxic=1 Wilson 83.8% vs target 96.1% gap=-12.3pp | blockers=train_resolved<30;train_toxic>0;train_wilson<BE+buffer;validation_toxic>0;validation_wilson<BE+buffer | promotion_blockers=none | next_pending=KXBTCD-26JUL0717-T61999.99 status=active due=2026-07-07T21:00:00+00:00 price=0.94

## Kalshi Maker Ex-Ante Cut Miner
- command: `python3 scripts/kalshi_maker_ex_ante_cut_miner.py --json --limit 8 --max-dims 4`
- status: NO_EX_ANTE_CUT_READY | ready=false | live_ready=false | groups=3344 | resolved_indep=2141 | pending_units=388 active=388 stale=0 unknown=0 | scope=posthoc ex-ante cut mining; forward validation and guarded pilot required before live use
- clean_ex_ante_forward_watch_candidates: none
- near_clean 1: category=crypto|side=YES|maker_price_band=94-96|side_bid_band=92-94 | gate=EX_ANTE_CUT_ACCUMULATING | resolved=33/30 | 33W-0L | pnl=+18.48 | Wilson 89.6% vs BE 94.4%+2pp | gap=-4.8pp | toxic=0 pending_units=3 active=3 stale=0 perfect_wins_needed=70 | blockers=wilson<=BE+buffer | next_pending=KXBTCD-26JUL0717-T61999.99 status=active close=2026-07-07T21:00:00+00:00 price=0.94
- near_clean 2: maker_price_band=94-96|spread_band=<=5c | gate=EX_ANTE_CUT_ACCUMULATING | resolved=52/30 | 51W-1L | pnl=+19.16 | Wilson 89.9% vs BE 94.4%+2pp | gap=-4.5pp | toxic=1 pending_units=7 active=7 stale=0 perfect_wins_needed=blocked_or_>5000 | blockers=toxic>0; wilson<=BE+buffer | next_pending=KXMLBSPREAD-26JUL041335MINNYY-NYY2 status=active close=2026-07-07T17:35:00+00:00 price=0.94
- near_clean 3: category=crypto|maker_price_band=90-92|side_bid_band=85-90 | gate=EX_ANTE_CUT_ACCUMULATING | resolved=35/30 | 34W-1L | pnl=+21.47 | Wilson 85.5% vs BE 91.0%+2pp | gap=-5.5pp | toxic=1 pending_units=3 active=3 stale=0 perfect_wins_needed=blocked_or_>5000 | blockers=toxic>0; wilson<=BE+buffer | next_pending=KXSOLD-26JUL0709-T81.9999 status=active close=2026-07-07T13:00:00+00:00 price=0.91
- near_clean 4: category=crypto|side=YES|side_bid_band=92-94 | gate=EX_ANTE_CUT_ACCUMULATING | resolved=43/30 | 42W-1L | pnl=+14.98 | Wilson 87.9% vs BE 94.2%+2pp | gap=-6.2pp | toxic=1 pending_units=4 active=4 stale=0 perfect_wins_needed=blocked_or_>5000 | blockers=toxic>0; wilson<=BE+buffer | next_pending=KXBTCD-26JUL0717-T61999.99 status=active close=2026-07-07T21:00:00+00:00 price=0.94
- near_clean 5: category=crypto|maker_price_band=94-96|spread_band=<=2c | gate=EX_ANTE_CUT_ACCUMULATING | resolved=43/30 | 42W-1L | pnl=+14.08 | Wilson 87.9% vs BE 94.4%+2pp | gap=-6.5pp | toxic=1 pending_units=2 active=2 stale=0 perfect_wins_needed=blocked_or_>5000 | blockers=toxic>0; wilson<=BE+buffer | next_pending=KXBTCD-26JUL0717-T61999.99 status=active close=2026-07-07T21:00:00+00:00 price=0.94
- near_clean 6: category=crypto|maker_price_band=94-96|side_bid_band=92-94|spread_band=<=2c | gate=EX_ANTE_CUT_ACCUMULATING | resolved=43/30 | 42W-1L | pnl=+14.08 | Wilson 87.9% vs BE 94.4%+2pp | gap=-6.5pp | toxic=1 pending_units=2 active=2 stale=0 perfect_wins_needed=blocked_or_>5000 | blockers=toxic>0; wilson<=BE+buffer | next_pending=KXBTCD-26JUL0717-T61999.99 status=active close=2026-07-07T21:00:00+00:00 price=0.94
- near_clean 7: side=NO|maker_price_band=94-96|spread_band=<=5c | gate=EX_ANTE_CUT_ACCUMULATING | resolved=42/30 | 41W-1L | pnl=+13.56 | Wilson 87.7% vs BE 94.4%+2pp | gap=-6.7pp | toxic=1 pending_units=5 active=5 stale=0 perfect_wins_needed=blocked_or_>5000 | blockers=toxic>0; wilson<=BE+buffer | next_pending=KXMLBSPREAD-26JUL041335MINNYY-NYY2 status=active close=2026-07-07T17:35:00+00:00 price=0.94
- near_clean 8: side=NO|maker_price_band=94-96|side_bid_band=92-94|time_to_close_band=>24h | gate=EX_ANTE_CUT_ACCUMULATING | resolved=39/30 | 38W-1L | pnl=+12.12 | Wilson 86.8% vs BE 94.3%+2pp | gap=-7.5pp | toxic=1 pending_units=7 active=7 stale=0 perfect_wins_needed=blocked_or_>5000 | blockers=toxic>0; wilson<=BE+buffer | next_pending=KXMLBSPREAD-26JUL041335MINNYY-NYY3 status=active close=2026-07-07T17:35:00+00:00 price=0.94
- top_positive 1: category=crypto|spread_band=<=2c | gate=EX_ANTE_CUT_ACCUMULATING | resolved=203/30 | 185W-18L | pnl=+43.68 | Wilson 86.4% vs BE 89.0%+2pp | gap=-2.6pp | toxic=18 pending_units=9 active=9 stale=0 perfect_wins_needed=blocked_or_>5000 | blockers=toxic>0; wilson<=BE+buffer | next_pending=KXBTCD-26JUL0717-T61999.99 status=active close=2026-07-07T21:00:00+00:00 price=0.94
- top_positive 2: category=crypto|side=YES|spread_band=<=2c | gate=EX_ANTE_CUT_ACCUMULATING | resolved=104/30 | 97W-7L | pnl=+39.65 | Wilson 86.8% vs BE 89.5%+2pp | gap=-2.7pp | toxic=7 pending_units=6 active=6 stale=0 perfect_wins_needed=blocked_or_>5000 | blockers=toxic>0; wilson<=BE+buffer | next_pending=KXBTCD-26JUL0717-T61999.99 status=active close=2026-07-07T21:00:00+00:00 price=0.94
- top_positive 3: maker_price_band=94-96|spread_band=<=5c | gate=EX_ANTE_CUT_ACCUMULATING | resolved=52/30 | 51W-1L | pnl=+19.16 | Wilson 89.9% vs BE 94.4%+2pp | gap=-4.5pp | toxic=1 pending_units=7 active=7 stale=0 perfect_wins_needed=blocked_or_>5000 | blockers=toxic>0; wilson<=BE+buffer | next_pending=KXMLBSPREAD-26JUL041335MINNYY-NYY2 status=active close=2026-07-07T17:35:00+00:00 price=0.94
- top_positive 4: category=crypto|side=YES|maker_price_band=94-96|side_bid_band=92-94 | gate=EX_ANTE_CUT_ACCUMULATING | resolved=33/30 | 33W-0L | pnl=+18.48 | Wilson 89.6% vs BE 94.4%+2pp | gap=-4.8pp | toxic=0 pending_units=3 active=3 stale=0 perfect_wins_needed=70 | blockers=wilson<=BE+buffer | next_pending=KXBTCD-26JUL0717-T61999.99 status=active close=2026-07-07T21:00:00+00:00 price=0.94
- top_positive 5: category=crypto|spread_band=<=2c|time_to_close_band=12-24h | gate=EX_ANTE_CUT_ACCUMULATING | resolved=83/30 | 76W-7L | pnl=+24.86 | Wilson 83.6% vs BE 88.6%+2pp | gap=-5.0pp | toxic=7 pending_units=9 active=9 stale=0 perfect_wins_needed=blocked_or_>5000 | blockers=toxic>0; wilson<=BE+buffer | next_pending=KXBTCD-26JUL0717-T61999.99 status=active close=2026-07-07T21:00:00+00:00 price=0.94

## Kalshi Maker Ex-Ante Forward Watch
- command: `python3 scripts/kalshi_maker_ex_ante_forward_watch.py --json`
- status: FORWARD_WATCH_ACCUMULATING | ready=false | watch_ready=false | live_ready=false | watch_id=maker_ex_ante_crypto_yes_94_96_bid_92_94_forward_watch_v1 | start_at=2026-07-07T07:19:41Z | scope=predeclared forward watch; no live authorization
- predicate: category=crypto side=YES maker_price=[0.94,0.96) side_bid=[0.92,0.94)
- forward: candidates=0 fills=0 resolved=0/30 0W-0L pnl=+0.00 toxic=0 | Wilson n/a vs BE n/a+2pp gap=n/a | pending=0 active=0 stale=0 unknown=0 perfect_wins_needed=blocked_or_>5000 | blockers=candidates=0; resolved<30; pnl<=0; wilson<=BE+buffer
- pre_start_posthoc_reference: candidates=103 resolved=33 33W-0L pnl=+18.48 toxic=0 | scope=pre-start posthoc reference only; excluded from forward gate

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
- status: native=NO_LIVE_READY pending=43 active=43 stale=0 unknown=0 | maker=NO_LIVE_READY pending_units=388 active=388 stale=0 unknown=0 | queued=20
- 1. native:crypto_last_hour_longshot_no | ticker=KXBTCD-26JUL0709-T63699.99 | status=active | time=2026-07-07T12:59:59.188159+00:00 | resolved=435 pending=2
- 2. maker:cell_crypto_no | ticker=KXSOLD-26JUL0709-T81.9999 | status=active | time=2026-07-07T13:00:00+00:00 | resolved_indep=432 pending_units=18
- 3. native:other_longshot_no_80_90:other_strong_no_90_95_4_24h_v1 | ticker=KXUSDJPY-26JUL0710-B163.125 | status=active | time=2026-07-07T13:59:59.267471+00:00 | resolved=9 pending=2
- 4. maker:cell_sports_no | ticker=KXMLBSPREAD-26JUL041105PITWSH-PIT6 | status=active | time=2026-07-07T15:05:00+00:00 | resolved_indep=707 pending_units=225
- 5. maker:cell_sports_yes | ticker=KXMLBSPREAD-26JUL041105PITWSH-PIT5 | status=active | time=2026-07-07T15:05:00+00:00 | resolved_indep=272 pending_units=92
- 6. native:weather_high_ask_no | ticker=KXLOWTPHIL-26JUL06-T64 | status=active | time=2026-07-07T19:00:00+00:00 | resolved=76 pending=16
- 7. native:weather_no_candidate:no_95_98_zero_loss_cities_v1 | ticker=KXLOWTMIA-26JUL06-B75.5 | status=active | time=2026-07-07T19:00:00+00:00 | resolved=84 pending=8
- 8. maker:cell_index_no | ticker=KXINX-26JUL07H1600-B7462 | status=active | time=2026-07-07T20:00:00+00:00 | resolved_indep=127 pending_units=22
- 9. maker:watch_fx_index_no_85_90 | ticker=KXINX-26JUL07H1600-B7487 | status=active | time=2026-07-07T20:00:00+00:00 | resolved_indep=26 pending_units=5
- 10. native:crypto_favorite_taker:crypto_near_certain_95_99_12_24h | ticker=KXETHD-26JUL0717-T1869.99 | status=active | time=2026-07-07T20:59:59.207141+00:00 | resolved=46 pending=8

## Kalshi Academic-Prior Aligned Queue
- command: `python3 scripts/kalshi_academic_prior_queue.py --report --per-family 2`
- KALSHI ACADEMIC-PRIOR ALIGNED QUEUE
- generated_at=2026-07-07T12:19:39.116376+00:00 db=/home/eric-king/kalshi_favorites_bot/trades.db
- Lower rank_score means closer to review, not approval.
- 1. high_price_native_taker:crypto_last_hour_longshot_no | status=NATIVE_FORWARD_ACCUMULATING rank=0.0514 | 435 resolved 394W-41L -$0.28 | Wilson 87.5% vs target 92.6% | next=KXBTCD-26JUL0709-T63699.99 active due=2026-07-07T12:59:59.188159+00:00 | blockers=pnl<=0, wilson<BE+2pp | next=wait for native-actionable forward rows to resolve; no live order until target clears
- 2. high_price_native_taker:weather_no_candidate:no_95_98_zero_loss_cities_v1 | status=NATIVE_FORWARD_ACCUMULATING rank=0.0777 | 84 resolved 82W-2L +$0.06 | Wilson 91.7% vs target 99.5% | next=KXLOWTMIA-26JUL06-B75.5 active due=2026-07-07T19:00:00+00:00 | blockers=wilson<BE+2pp | next=wait for native-actionable forward rows to resolve; no live order until target clears
- 3. source_shadow_requires_native:shadow_longshot_fading:crypto:NO:moderate:80-90:<1h | status=SHADOW_STABILITY_REJECT rank=0.2500 | 647 events 598W-49L +$2658.32 | Wilson 90.1% vs target 89.6% | stability_validation=195ev 179W-16L +$690.66 Wilson 87.1% vs target 89.5% | blockers=source_only_requires_native_forward_gate, shadow_stability_reject, validation_wilson<avg_price+buffer, asset_slice_wilson<avg_price:KXETHD, utc_hour_slice_pnl<=0:15Z, utc_hour_slice_wilson<avg_price:15Z | next=only promote if a matching native first-actionable gate clears after fees and depth
- 4. source_shadow_requires_native:shadow_longshot_fading:other:NO:weak:80-90:4-24h | status=SHADOW_STABILITY_REJECT rank=0.2500 | 58 events 57W-1L +$817.46 | Wilson 90.9% vs target 85.4% | stability_validation=18ev 18W-0L +$300.14 Wilson 82.4% vs target 84.4% | blockers=source_only_requires_native_forward_gate, shadow_stability_reject, validation_wilson<avg_price+buffer | next=only promote if a matching native first-actionable gate clears after fees and depth
- 5. maker_adverse_selection:cell_sports_no | status=NO_GO_REVIEW rank=0.6876 | 707 independent resolved 509W-198L -$1084.11 | Wilson 68.6% vs BE 87.3% | toxic=198 fill_rate=25.4% | blockers=pnl<=0, wilson<=BE, toxic>0 | next=continue shadow fill/toxicity measurement; no maker pilot with toxic or Wilson blockers
- 6. maker_adverse_selection:cell_crypto_no | status=NO_GO_REVIEW rank=0.9121 | 432 independent resolved 215W-217L -$1577.75 | Wilson 45.1% vs BE 86.3% | toxic=217 fill_rate=30.4% | blockers=pnl<=0, wilson<=BE, toxic>0 | next=continue shadow fill/toxicity measurement; no maker pilot with toxic or Wilson blockers
- 7. structural_arbitrage:same_strike_last_24h | status=WATCH_ONLY rank=1.0000 | 30242 observations | fresh_pairs=30242 execution_ready_tier=3620 gross_positive=0 execution_ready_gross_positive=0 qty10_positive=0 execution_ready_qty10_positive=0 best_gross_edge=0.0 | blockers=no_gross_positive_same_strike, no_execution_ready_gross_positive, no_execution_ready_fee_net_qty10_positive | next=continue simultaneous quote scans; only trade fee-net positive executable dislocations

## Kalshi Shadow Longshot Fading Resolver
- timer: kalshi-shadow-longshot-fading-backfill.timer active/enabled | service=kalshi-shadow-longshot-fading-backfill.service
- recent_36h_backlog: unresolved=2100 | expired_after_60s_grace=62 | oldest_expired=2026-07-07 04:59:59 | oldest_expected=2026-07-07 04:59:59
- recent_36h_crypto_backlog: unresolved=220 | expired_after_60s_grace=0 | oldest_expired=none | oldest_expected=2026-07-07 12:59:59
- native_gate_stale_unresolved=0
- resolved_last_30m=163
- all_expired_backlog: unresolved=6588 | crypto=6171 | other=352 | weather=65 | oldest_expired=2026-04-15 21:59:59 | newest_expired=2026-07-07 05:00:00
- legacy_pre36h_expired_backlog: unresolved=6526 | crypto=6171 | other=352 | weather=3 | oldest_expired=2026-04-15 21:59:59 | newest_expired=2026-07-02 16:59:59
- scope: evidence-only resolver; no order placement path; timer category=crypto lookback=36h; prioritizes stale native-gate rows

## Kalshi Shadow Forecast Accuracy Resolver
- timer: kalshi-shadow-forecast-accuracy-backfill.timer active/enabled | service=kalshi-shadow-forecast-accuracy-backfill.service
- recent_72h_backlog: unresolved=251 | expired_after_60s_grace=28 | oldest_expired=2026-07-07 04:59:59 | oldest_expected=2026-07-07 04:59:59
- native_weather_gate_stale_unresolved=0 | next_due=2026-07-07T19:00:00+00:00
- scope: evidence-only resolver; no order placement path; lookback=72h; resolves binary/scalar public Kalshi outcomes

## Broad Favorite-Longshot Maker Edge
- command: `python3 scripts/favorite_longshot_maker_edge.py --report`
- FAVORITE-LONGSHOT MAKER EDGE
-   Cohort: fx_y_forward_only_2026_06_23 | start=2026-06-23T03:11:18+00:00 | source=gemini_maker_fp_only | mode=SHADOW_ONLY_NO_PLACEMENT
-   Verdict: NO-GO_EXECUTABLE_EDGE | all observed bands have fill rate <5%; toxic fills dominate 9/9 mature bands; no live capital.
-   5-10c: candidates=78300 fill=0.2% resolved=35 benign/toxic=12/23 net=$-13.10 benign=$+9.25 Wilson=75.7% BE=0.0% margin=+75.7pp | NO-GO_FILL_RATE+TOXIC_DOMINANT+NONPOSITIVE_NET_PNL
-   10-20c: candidates=72683 fill=0.4% resolved=52 benign/toxic=17/35 net=$-39.09 benign=$+47.52 Wilson=81.6% BE=0.0% margin=+81.6pp | NO-GO_FILL_RATE+TOXIC_DOMINANT+NONPOSITIVE_NET_PNL
-   20-35c: candidates=69099 fill=0.5% resolved=65 benign/toxic=25/40 net=$-12.04 benign=$+84.02 Wilson=86.7% BE=0.0% margin=+86.7pp | NO-GO_FILL_RATE+TOXIC_DOMINANT+NONPOSITIVE_NET_PNL
-   35-50c: candidates=44178 fill=0.5% resolved=46 benign/toxic=16/30 net=$+5.42 benign=$+70.04 Wilson=80.6% BE=0.0% margin=+80.6pp | NO-GO_FILL_RATE+TOXIC_DOMINANT
-   50-65c: candidates=43488 fill=0.7% resolved=45 benign/toxic=12/33 net=$-59.47 benign=$+50.56 Wilson=75.7% BE=0.0% margin=+75.7pp | NO-GO_FILL_RATE+TOXIC_DOMINANT+NONPOSITIVE_NET_PNL
-   65-80c: candidates=37440 fill=0.6% resolved=59 benign/toxic=17/42 net=$-11.72 benign=$+79.23 Wilson=81.6% BE=0.0% margin=+81.6pp | NO-GO_FILL_RATE+TOXIC_DOMINANT+NONPOSITIVE_NET_PNL
-   80-90c: candidates=34641 fill=0.6% resolved=61 benign/toxic=15/46 net=$+10.34 benign=$+35.81 Wilson=79.6% BE=0.0% margin=+79.6pp | NO-GO_FILL_RATE+TOXIC_DOMINANT
-   90-95c: candidates=20686 fill=0.4% resolved=40 benign/toxic=11/29 net=$-19.52 benign=$+10.53 Wilson=74.1% BE=0.0% margin=+74.1pp | NO-GO_FILL_RATE+TOXIC_DOMINANT+NONPOSITIVE_NET_PNL
-   95-99c: candidates=39616 fill=0.2% resolved=45 benign/toxic=8/37 net=$-0.93 benign=$+2.74 Wilson=67.6% BE=0.0% margin=+67.6pp | NO-GO_FILL_RATE+TOXIC_DOMINANT+NONPOSITIVE_NET_PNL

## Timers
```
NEXT                                  LEFT LAST                              PASSED UNIT                                                   ACTIVATES
Tue 2026-07-07 07:19:47 CDT             4s Tue 2026-07-07 07:19:12 CDT      30s ago kalshi-worldcup-score-state-live-pilot.timer           kalshi-worldcup-score-state-live-pilot.service
Tue 2026-07-07 07:19:52 CDT            10s Tue 2026-07-07 07:18:49 CDT      53s ago kalshi-worldcup-final-state-live-pilot.timer           kalshi-worldcup-final-state-live-pilot.service
Tue 2026-07-07 07:19:55 CDT            13s Tue 2026-07-07 07:14:55 CDT 4min 46s ago gemini-maker-fill-simulator.timer                      gemini-maker-fill-simulator.service
Tue 2026-07-07 07:20:00 CDT            17s Tue 2026-07-07 07:19:00 CDT      42s ago cushion-ds-multi-series-scanner.timer                  cushion-ds-multi-series-scanner.service
Tue 2026-07-07 07:20:00 CDT            17s Tue 2026-07-07 07:10:00 CDT     9min ago full-picture-latest-refresh.timer                      full-picture-latest-refresh.service
Tue 2026-07-07 07:20:00 CDT            17s Tue 2026-07-07 07:19:30 CDT      12s ago gemini-cushion-ds-scanner.timer                        gemini-cushion-ds-scanner.service
Tue 2026-07-07 07:20:03 CDT            21s Tue 2026-07-07 06:50:03 CDT    29min ago eth-ds-fg-filter-blocks-resolver.timer                 eth-ds-fg-filter-blocks-resolver.service
Tue 2026-07-07 07:20:12 CDT            29s Tue 2026-07-07 07:19:12 CDT      30s ago goal-loop-watchdog.timer                               goal-loop-watchdog.service
Tue 2026-07-07 07:20:36 CDT            54s Tue 2026-07-07 07:15:32 CDT  4min 9s ago kalshi-weather-yes-90-93-preflight.timer               kalshi-weather-yes-90-93-preflight.service
Tue 2026-07-07 07:20:49 CDT        1min 6s Tue 2026-07-07 07:15:49 CDT 3min 53s ago kalshi-side-equivalence-scanner.timer                  kalshi-side-equivalence-scanner.service
Tue 2026-07-07 07:21:08 CDT       1min 26s Tue 2026-07-07 07:17:53 CDT 1min 48s ago kalshi-sports-final-state-live-pilot.timer             kalshi-sports-final-state-live-pilot.service
Tue 2026-07-07 07:21:11 CDT       1min 29s Tue 2026-07-07 07:16:04 CDT 3min 38s ago kalshi-moderate-favorites-eth-yes-preflight.timer      kalshi-moderate-favorites-eth-yes-preflight.service
Tue 2026-07-07 07:21:12 CDT       1min 30s Tue 2026-07-07 07:16:12 CDT 3min 30s ago kalshi-other-longshot-no-80-90-preflight.timer         kalshi-other-longshot-no-80-90-preflight.service
Tue 2026-07-07 07:21:14 CDT       1min 32s Tue 2026-07-07 07:06:14 CDT    13min ago gemini-categorical-resolver.timer                      gemini-categorical-resolver.service
Tue 2026-07-07 07:21:20 CDT       1min 37s Tue 2026-07-07 07:16:12 CDT 3min 29s ago kalshi-crypto-last-hour-longshot-no-preflight.timer    kalshi-crypto-last-hour-longshot-no-preflight.service
Tue 2026-07-07 07:21:22 CDT       1min 40s Tue 2026-07-07 07:16:13 CDT 3min 28s ago kalshi-shadow-deterministic-settlement-backfill.timer  kalshi-shadow-deterministic-settlement-backfill.service
Tue 2026-07-07 07:22:30 CDT       2min 47s Tue 2026-07-07 07:17:30 CDT 2min 12s ago kalshi-shadow-forecast-accuracy-backfill.timer         kalshi-shadow-forecast-accuracy-backfill.service
Tue 2026-07-07 07:22:40 CDT       2min 58s Tue 2026-07-07 07:17:38 CDT  2min 4s ago kalshi-shadow-longshot-fading-backfill.timer           kalshi-shadow-longshot-fading-backfill.service
Tue 2026-07-07 07:23:03 CDT       3min 21s Tue 2026-07-07 07:18:02 CDT 1min 39s ago kalshi-crypto-favorite-taker-preflight.timer           kalshi-crypto-favorite-taker-preflight.service
Tue 2026-07-07 07:23:53 CDT       4min 10s Tue 2026-07-07 07:18:53 CDT      49s ago kalshi-weather-no-candidate-preflight.timer            kalshi-weather-no-candidate-preflight.service
Tue 2026-07-07 07:24:01 CDT       4min 19s Tue 2026-07-07 07:19:01 CDT      40s ago gemini-reward-post-only-safety.timer                   gemini-reward-post-only-safety.service
Tue 2026-07-07 07:24:06 CDT       4min 23s Tue 2026-07-07 07:19:03 CDT      38s ago kalshi-weather-high-ask-no-preflight.timer             kalshi-weather-high-ask-no-preflight.service
Tue 2026-07-07 07:25:02 CDT           5min Tue 2026-07-07 06:55:02 CDT    24min ago gemini-db-size-monitor.timer                           gemini-db-size-monitor.service
Tue 2026-07-07 07:26:08 CDT           6min Tue 2026-07-07 07:11:08 CDT     8min ago gemini-ds-source-parity.timer                          gemini-ds-source-parity.service
Tue 2026-07-07 07:26:20 CDT           6min Tue 2026-07-07 07:11:20 CDT     8min ago kalshi-side-equivalence-resolver.timer                 kalshi-side-equivalence-resolver.service
Tue 2026-07-07 07:28:15 CDT           8min Tue 2026-07-07 07:18:12 CDT 1min 29s ago ds-shadow-continuous-archive.timer                     ds-shadow-continuous-archive.service
Tue 2026-07-07 07:29:11 CDT           9min Tue 2026-07-07 07:14:11 CDT     5min ago ds-storage-pressure-monitor.timer                      ds-storage-pressure-monitor.service
Tue 2026-07-07 07:30:00 CDT          10min Tue 2026-07-07 07:15:00 CDT 4min 41s ago cushion-ds-multi-series-resolver.timer                 cushion-ds-multi-series-resolver.service
Tue 2026-07-07 07:30:00 CDT          10min Tue 2026-07-07 07:15:00 CDT 4min 41s ago gemini-cushion-ds-resolver.timer                       gemini-cushion-ds-resolver.service
Tue 2026-07-07 07:30:00 CDT          10min Tue 2026-07-07 06:30:00 CDT    49min ago gemini-direct-index-ds-first-resolution-verifier.timer gemini-direct-index-ds-first-resolution-verifier.service
Tue 2026-07-07 07:31:23 CDT          11min Tue 2026-07-07 07:16:23 CDT 3min 18s ago btc-moderate-v2-shadow-resolver.timer                  btc-moderate-v2-shadow-resolver.service
Tue 2026-07-07 07:31:23 CDT          11min Tue 2026-07-07 07:16:23 CDT 3min 18s ago gemini-categorical-scanner.timer                       gemini-categorical-scanner.service
Tue 2026-07-07 07:40:00 CDT          20min Tue 2026-07-07 07:05:00 CDT    14min ago ibkr-deterministic-fx-poc.timer                        ibkr-deterministic-fx-poc.service
Tue 2026-07-07 07:45:09 CDT          25min Tue 2026-07-07 07:15:09 CDT 4min 32s ago ds-storage-monitor.timer                               ds-storage-monitor.service
Tue 2026-07-07 08:06:07 CDT          46min Tue 2026-07-07 07:04:09 CDT    15min ago macro-release-resolver.timer                           macro-release-resolver.service
Tue 2026-07-07 08:07:00 CDT          47min Tue 2026-07-07 07:07:00 CDT    12min ago claude-partition-arb-scan.timer                        claude-partition-arb-scan.service
Tue 2026-07-07 08:07:17 CDT          47min Tue 2026-07-07 07:07:00 CDT    12min ago ladder-coherence-two-leg-resolver.timer                ladder-coherence-two-leg-resolver.service
Tue 2026-07-07 09:02:00 CDT       1h 42min Mon 2026-07-06 20:57:00 CDT      10h ago claude-crossing-no-v3.timer                            claude-crossing-no-v3.service
Tue 2026-07-07 09:14:13 CDT       1h 54min Mon 2026-07-06 09:14:13 CDT      22h ago launchpadlib-cache-clean.timer                         launchpadlib-cache-clean.service
Tue 2026-07-07 09:18:56 CDT       1h 59min Mon 2026-07-06 09:18:56 CDT      22h ago gemini-fp-retention.timer                              gemini-fp-retention.service
Tue 2026-07-07 09:19:00 CDT       1h 59min Tue 2026-07-07 03:19:00 CDT  4h 0min ago ds-shadow-db-maintenance.timer                         ds-shadow-db-maintenance.service
Tue 2026-07-07 09:19:10 CDT       1h 59min Tue 2026-07-07 06:19:10 CDT  1h 0min ago db-auto-vacuum.timer                                   db-auto-vacuum.service
Tue 2026-07-07 09:24:20 CDT        2h 4min Tue 2026-07-07 03:24:20 CDT 3h 55min ago ds-shadow-archive.timer                                ds-shadow-archive.service
Tue 2026-07-07 12:10:00 CDT       4h 50min Tue 2026-07-07 06:10:00 CDT  1h 9min ago claude-chat-sync.timer                                 claude-chat-sync.service
Tue 2026-07-07 13:17:00 CDT       5h 57min Tue 2026-07-07 07:17:01 CDT 2min 41s ago ds-shadow-retention-engine.timer                       ds-shadow-retention-engine.service
Tue 2026-07-07 16:13:00 CDT             8h Tue 2026-07-07 04:13:00 CDT  3h 6min ago claude-calibration-logger.timer                        claude-calibration-logger.service
Wed 2026-07-08 03:15:00 CDT            19h Tue 2026-07-07 03:15:00 CDT  4h 4min ago shadow-verification.timer                              shadow-verification.service
Wed 2026-07-08 03:30:00 CDT            20h Tue 2026-07-07 03:30:00 CDT 3h 49min ago ibkr-independent-verification.timer                    ibkr-independent-verification.service
Wed 2026-07-08 04:30:00 CDT            21h Tue 2026-07-07 04:30:00 CDT 2h 49min ago tax-ledger-ingest.timer                                tax-ledger-ingest.service
Wed 2026-07-08 04:41:58 CDT            21h Tue 2026-07-07 04:37:30 CDT 2h 42min ago ds-archive-tier-rotation.timer                         ds-archive-tier-rotation.service
Wed 2026-07-08 05:20:00 CDT            22h Tue 2026-07-07 05:20:00 CDT 1h 59min ago logrotate-user.timer                                   logrotate-user.service
Wed 2026-07-08 05:30:00 CDT            22h Tue 2026-07-07 05:30:00 CDT 1h 49min ago disk-hygiene-audit.timer                               disk-hygiene-audit.service
Wed 2026-07-08 05:30:00 CDT            22h Tue 2026-07-07 05:30:00 CDT 1h 49min ago full-picture-daily-save.timer                          full-picture-daily-save.service
Fri 2026-07-10 09:16:55 CDT         3 days Fri 2026-07-03 09:16:55 CDT   3 days ago ubuntu-insights-upload.timer                           ubuntu-insights-upload.service
Sun 2026-07-12 02:00:00 CDT         4 days Sun 2026-07-05 02:00:00 CDT   2 days ago gemini-archive-compression.timer                       gemini-archive-compression.service
Sun 2026-08-02 19:43:55 CDT 3 weeks 5 days Fri 2026-07-03 09:13:55 CDT   3 days ago ubuntu-insights-collect.timer                          ubuntu-insights-collect.service
-                                        - Tue 2026-07-07 07:19:01 CDT      41s ago btc-moderate-v2-shadow-scanner.timer                   btc-moderate-v2-shadow-scanner.service
-                                        - Tue 2026-07-07 05:40:00 CDT 1h 39min ago database-autonomous-maintenance.timer                  database-autonomous-maintenance.service
-                                        - Tue 2026-07-07 07:19:36 CDT       5s ago gateway-watchdog.timer                                 gateway-watchdog.service
-                                        - Tue 2026-07-07 07:19:30 CDT      12s ago gemini-db-retention.timer                              gemini-db-retention.service
-                                        - Tue 2026-07-07 07:19:37 CDT       4s ago gemini-ds-index-micro-parity.timer                     gemini-ds-index-micro-parity.service
-                                        - Tue 2026-07-07 07:18:43 CDT      58s ago gemini-ds-index-parity.timer                           gemini-ds-index-parity.service
-                                        - Tue 2026-07-07 07:19:01 CDT      40s ago gemini-fp-orderbook-capture.timer                      gemini-fp-orderbook-capture.service
-                                        - Tue 2026-07-07 07:18:28 CDT 1min 13s ago gemini-liquidity-rewards-scanner.timer                 gemini-liquidity-rewards-scanner.service
-                                        - Tue 2026-07-07 05:33:28 CDT 1h 46min ago gemini-reward-account-monitor.timer                    gemini-reward-account-monitor.service
-                                        - Tue 2026-07-07 05:29:28 CDT 1h 50min ago gemini-reward-inventory-exit.timer                     gemini-reward-inventory-exit.service
-                                        - Tue 2026-07-07 05:31:21 CDT 1h 48min ago gemini-reward-live-readiness.timer                     gemini-reward-live-readiness.service
-                                        - Tue 2026-07-07 05:28:44 CDT 1h 50min ago gemini-reward-quote-pilot.timer                        gemini-reward-quote-pilot.service
-                                        - Tue 2026-07-07 07:17:40 CDT  2min 2s ago gemini-trade-print-capture.timer                       gemini-trade-print-capture.service
-                                        - Tue 2026-07-07 07:19:33 CDT       9s ago kalshi-crypto-ladder-dislocation-preflight.timer       kalshi-crypto-ladder-dislocation-preflight.service
-                                        - Tue 2026-07-07 07:18:46 CDT      56s ago kalshi-mve-component-result-live-pilot.timer           kalshi-mve-component-result-live-pilot.service
-                                        - Fri 2026-07-03 15:00:00 CDT   3 days ago snap.firmware-updater.firmware-notifier.timer          snap.firmware-updater.firmware-notifier.service

72 timers listed.
```

## Repo State
- gemini: head=fd8d19d branch=master in_sync=true remote=https://github.com/PhotonRahm/gemini_prediction_bot.git dirty=yes
- ibkr: head=3a580e4 branch=master in_sync=true remote=https://github.com/PhotonRahm/ibkr_forecast_bot.git dirty=yes
- kalshi: head=99546b4 branch=master in_sync=true remote=https://github.com/PhotonRahm/kalshi_favorites_bot.git dirty=yes
- operations-knowledge: head=3c823a0 branch=master in_sync=true remote=https://github.com/PhotonRahm/operations-knowledge.git dirty=yes
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

## Today's Research Files (2026-07-07 America/Chicago)
- research/2026-07-07-fx-no-kalshi-rolling-ws-health-and-0459-crypto-boundary-no-go.md
- research/2026-07-07-fx-np-kalshi-realtime-ws-reseed-gate-post-expiration-sports-hardening-no-go.md
- research/2026-07-07-fx-nq-kalshi-realtime-execution-gate-db-lock-hardening-0559-crypto-no-go.md
- research/2026-07-07-fx-nr-kalshi-maker-toxicity-attribution-live-gate-refresh-no-go.md
- research/2026-07-07-fx-ns-kalshi-maker-ex-ante-cut-miner-no-go.md
- research/2026-07-07-fx-nt-kalshi-maker-ex-ante-forward-watch-no-go.md
- research/2026-07-07-fx-nu-kalshi-ws-per-ticker-execution-gate-no-go.md
- research/2026-07-07-fx-nv-kalshi-realtime-candidate-execution-readiness-no-go.md
- research/2026-07-07-fx-nw-kalshi-candidate-driven-ws-probe-strategy-blocked.md
- research/2026-07-07-fx-nx-kalshi-candidate-execution-quality-mm-analog-no-go.md
- research/2026-07-07-fx-ny-kalshi-candidate-execution-quality-forward-watch-no-go.md
- research/2026-07-07-fx-nz-kalshi-quality-aware-ws-probe-selector-no-go.md
- research/2026-07-07-fx-oa-kalshi-clean-mm-ws-probe-gate-no-go.md
- research/2026-07-07-fx-ob-kalshi-mm-near-miss-adverse-selection-no-go.md
- research/2026-07-07-fx-oc-kalshi-native-cut-promotion-bridge-no-go.md
- research/2026-07-07-fx-od-kalshi-native-forward-watch-coverage-no-go.md
- research/2026-07-07-fx-oe-kalshi-realtime-mm-infra-audit-no-go.md
- research/2026-07-07-fx-of-kalshi-v3-quote-manager-dry-run-gate-no-go.md
- research/2026-07-07-fx-og-kalshi-wide-nontransport-mm-gate-no-go.md
- research/2026-07-07-fx-oh-goal-integrity-gemini-snapshot-fallback.md
- research/2026-07-07-fx-oi-kalshi-ws-queue-capture-gate.md
- research/2026-07-07-fx-oj-kalshi-ws-queue-model-review-no-go.md
- research/2026-07-07-fx-ok-kalshi-fresh-queue-model-probe-no-go.md
- research/2026-07-07-fx-ol-kalshi-post-only-cancel-replace-dry-run-gate-no-go.md

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
