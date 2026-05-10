# Rahm Live Strategy Glossary

Last updated: 2026-05-10

This glossary names each live strategy by actual mechanism. Legacy strategy keys
and kill-switch paths are preserved where changing them would create operational
risk.

| Strategy display name | Strategy key | Mechanism | Methodology class | Kill switch |
| --- | --- | --- | --- | --- |
| Gemini Mean Reversion | mean_reversion | Prediction-market mean reversion with 0.75x Kelly live sizing, empirical-Bayes probability calibration where per-asset forward sample is sufficient, and permanent 50% per-asset concentration cap | Live MR with evidence-gated Kelly multiplier scale-up from 0.625 to 0.75 on 2026-05-10; 50 resolved post-deploy MR placements required before any further multiplier review | Gemini MR kill paths in repo CLAUDE.md |
| Gemini Crypto DS High-Price ETH Pilot | deterministic_settlement | Final-window ETH cushion settlement with price >=0.95 and cushion >=0.10%, no depth enforcement, qty 50, max_open 3, daily CB -$100, lifetime CB -$300; depth is still recorded for bucket analysis. Active cohort name: `filter_combined_eth_high_price_qty_50_pilot` (started 2026-05-09 14:01:37 UTC / 09:01:37 CDT). Closed cohort names: `filter_combined_eth_high_price_pilot` (qty-10 ETH high-price pilot, passed 2026-05-09 at 52 resolved, 52W-0L, Wilson 93.1%, P&L +$15.50), `filter_combined_btc_eth_high_price_pilot` (BTC/ETH high-price pilot, failed 2026-05-08 at 53 resolved, 51W-2L, Wilson 87.2%, P&L -$3.48 after BTC loss concentration), `parallel_filter_btc_eth_pilot` (BTC/ETH price>=0.90 pilot, failed 2026-05-07 at 42 resolved, 37W-5L, Wilson 75.0%, P&L -$24.63, daily CB breach), `parallel_filter_pilot` (BTC/ETH/SOL pilot, closed 2026-05-06 16:28:46 after SOL loss concentration), and `strict_filter_pilot` (earlier strict-filter pilot, closed 2026-05-05 18:12:00 when parallel pilot started). | Live bounded qty-50 ETH continuation of the Kalshi-matched high-price+cushion filter structure; prior qty-10 rows are informative only and not inherited | `KILL_DETERMINISTIC_SETTLEMENT` |
| Kalshi Mean Reversion | mean_reversion | Prediction-market mean reversion with surgical cell controls: KXHIGH/KXETHD/KXBTCD retired via MR-only pattern blocks, WEATHER_LOW YES total_cost >=$150 permanently blocked, INDEX capped at max 2 per underlier/event and max 4 total INDEX positions per settlement hour, NO side intentionally active where not otherwise retired | Live MR with forward allowed-cell P&L tracker from 2026-05-07 20:20:23 UTC | Kalshi MR kill paths in repo CLAUDE.md |
| Kalshi Crypto DS | deterministic_settlement | Final-window crypto cushion settlement on BTC/ETH, per-asset sizing BTC qty 600 / ETH qty 275, daily CB -$600, lifetime CB -$1,800, max_open 8, max 4 open positions per asset/settlement-hour, combined filter price >=0.93 and cushion >=0.10%, qty and filter cohort trackers active | Proper cushion DS with per-asset rollback after aggregate qty-400 gate failure; BTC qty 600 and ETH qty 275 one-parameter pilots continue, and the $0.93 min-price filter cohort opened 2026-05-10 after the comprehensive loss forensic found it was the only Bonferroni-surviving surgical filter | `KILL_DETERMINISTIC_SETTLEMENT` |
| Kalshi Index Longshot Fade | deterministic_settlement_index | Cheap-side longshot fade using audited TTE-bucketed heuristic rows | Paused: first live cohort 0W-4L on 2026-05-04 | `KILL_DETERMINISTIC_SETTLEMENT_INDEX` |
| Kalshi FX Longshot Fade | deterministic_settlement_fx | Cheap-side longshot fade using audited TTE-bucketed heuristic rows | Paused: first live cohort 0W-4L on 2026-05-04 | `KILL_DETERMINISTIC_SETTLEMENT_FX` |
| Kalshi Moderate Favorites | moderate_favorites | Narrow-band favorite pilot | Paused live pilot | `KILL_MODERATE_FAVORITES` |
| IBKR Long+Short-dated | bot_strategy | ForecastEx economics/FX filter stack | Live IBKR strategy | IBKR repo CLAUDE.md |
| IBKR Weather DS Per-Cell Pilots | deterministic_settlement_weather | NWS-cushion weather settlement pilots on live cells `UHBNA_YES_cushion_2_to_5f`, `UHPHX_YES_cushion_2_to_5f`, `UHJAX_YES_cushion_lt_2f`, `UHSFO_YES_cushion_2_to_5f`, and `UHCLT_YES_cushion_2_to_5f`; qty 25, max_open 2 per live cell, per-cell daily/lifetime CB -$75/-$150, aggregate daily/lifetime CB -$200/-$400. `edge_threshold=0.40` means `model_probability - ask >= 0.40`, effectively ask <= $0.40 for current model 0.80 cells. Dropped cells `UHATL_YES_cushion_lt_2f`, `UHPHL_YES_cushion_lt_2f`, and `UHLAX_YES_cushion_lt_2f` are shadow-tracked in `ds_weather_shadow_signals` with graduation criteria n>=30 forward shadow, WR>=90%, Wilson lower>=80%, positive hypothetical P&L. Historical Weather DS rows are not inherited. | Live bounded per-cell pilot from 2026-05-08 15:20:00 UTC after operator approval and Option A tightening; Bug class #17 partial-fill attribution fix coupled and historical drift cleanup authorized | `KILL_DETERMINISTIC_SETTLEMENT_WEATHER` |

Live strategy policy notes:

Depth filter forward shadow:

- `depth_at_limit_price` means the venue depth observed at the intended DS
  limit price at placement time. For Kalshi DS the comparable live-trade field
  is `ask_depth_at_entry`.
- As of 2026-05-10, depth is not a live filter for Gemini DS or Kalshi DS. It
  is tracked in the forward-only `shadow_depth_filter_comparison` harness with
  clean cohorts `gemini_ds_depth_filter_pilot` and
  `kalshi_ds_depth_filter_pilot`.
- Fixed pilot thresholds: Gemini `depth_at_limit_price >= 5555`; Kalshi
  `ask_depth_at_entry >= 74`.
- Future live deployment requires the pre-committed gate in
  `research/2026-05-10-depth-filter-pilot-pre-commit.md`. Historical depth
  rows are informative only and do not count toward that gate.

Reconciliation vocabulary:

- **True P&L**: cumulative platform balance minus deposits across all activity
  since the platform was funded. It includes pre-strategy historical drag and is
  not, by itself, a current-bleed indicator.
- **Documented baseline**: an absorbed structural offset for known historical
  losses or unverifiable platform/account movement. The rendered
  RECONCILIATION block uses it so `cash_gap` can remain `$0.00` while preserving
  the historical context.
- **Forward strategy P&L**: P&L from cohort-framework-managed strategies only.
  This is the operationally relevant number for whether the current strategy
  stack is working.
- **24h P&L**: the correct current-bleed indicator. If 24h P&L and rendered
  `cash_gap` are healthy, cumulative True P&L can remain negative without
  implying current operational drain.

Calibration probability vocabulary:

- **`raw_model_probability`**: the model output before side adjustment,
  empirical-Bayes shrinkage, Kelly sizing, or concentration caps. Historical
  rows before 2026-05-10 usually cannot reconstruct this value and should show
  `INSUFFICIENT_DATA` rather than fabricating it.
- **`side_adjusted_trade_win_probability`**: probability that the placed trade,
  on its actual side, resolves as a winner. New calibration analyses should use
  this column when comparing predicted probability to realized win rate.
- **`live_sizing_probability`**: probability used by the live sizing decision
  at placement time. It may equal side-adjusted probability, or differ when
  EB shrinkage, Kelly modifiers, or hard concentration caps apply.
- **Legacy `predicted_probability`**: pre-2026-05-10 compatibility field with
  ambiguous semantics across strategies. It remains in reports for historical
  continuity but should not be used for new remediation decisions when the
  semantic columns are available.

Kalshi MR retired subseries and permanent controls:

- `KXHIGH*` (Weather High) is RETIRED for MR. Investigation evidence: Weather
  High was structurally negative with large-loss asymmetry; recent 30d
  decomposition showed 14W-2L, -$498.72 and lifetime Weather High combined
  loss around -$929.80. Runtime enforcement remains the MR-only
  `MR_BLOCKED_PATTERNS` prefix.
- `KXETHD*` (ETH daily crypto) is RETIRED for MR. Investigation evidence:
  ETH-YES asymmetry remained structurally negative despite high WR; recent 30d
  ETH YES was 26W-3L, -$367.89 and lifetime ETH YES was 32W-3L, -$276.26.
  Runtime enforcement remains the MR-only `MR_BLOCKED_PATTERNS` prefix.
- `KXBTCD*` (BTC daily crypto) is RETIRED for MR. The block is retained for
  lifetime tail-loss asymmetry even though some recent BTC slices were
  positive. Runtime enforcement remains the MR-only `MR_BLOCKED_PATTERNS`
  prefix.
- WEATHER_LOW YES total_cost >= $150 is permanent MR policy. The cap preserves
  the small-cost WEATHER_LOW YES slice and blocks the above-cap tail; today it
  blocked 4/4 attempts around $331-$345. WEATHER_LOW NO remains unrestricted.
- INDEX cluster cap is permanent MR policy as of 2026-05-07: max 2 open
  positions per underlier/event and max 4 total open INDEX positions per
  settlement hour. Existing open positions at deploy are grandfathered.
- Kalshi MR forward allowed-cell tracking starts 2026-05-07 20:20:23 UTC and
  answers whether the refined, currently allowed portfolio is profitable while
  preserving lifetime P&L as historical context.

Shadow-only streams that should not be confused with live strategy keys:

- Principle 29 applies to every stream below: aggregate metrics are descriptive
  only, and live-pilot decisions require n>=50 resolved per defined cell with
  Wilson lower above breakeven for that cell.
- Cushion-DS methodology: proper final-30m deterministic settlement on a
  numeric underlying and numeric strike. Entry is taker-side at best ask.
  The live Kalshi crypto filter is `entry_price >= 0.93` and
  `abs(spot - strike) / strike >= 0.10%` as of 2026-05-10. The live Gemini
  ETH filter remains `entry_price >= 0.95` and cushion >=0.10%.
- Favorite-tracking methodology: broad favorite-vs-longshot observation logic
  used in the existing DS SHADOW EXPANSION section. It is not equivalent to
  cushion-DS; confusing this with proper cushion-DS caused the legacy
  Index/FX Longshot Fade live failure.
- `spot_age_at_placement_seconds`: forward-only post-2026-05-10 live DS trade
  instrumentation. Age of the spot reading used by the bot's placement filter
  decision. Older rows remain NULL.
- `spot_age_at_fill_seconds`: forward-only live DS trade instrumentation. Age
  of the same spot reading at the post-submit fill check, capturing order dwell
  time without adding hot-path spot API calls.
- `spot_value_at_placement` / `spot_value_at_fill`: spot values stored with the
  age fields for future cushion-correctness checks.
- `spot_source_at_placement`: source label for spot-age diagnostics, currently
  `shadow_deterministic_settlement` for Gemini/Kalshi crypto DS.
- Unit of independence: the denominator used for statistical confidence and
  gate decisions when shadow rows are correlated. If a scanner records many
  observations for the same underlying contract or settlement event, row count
  is descriptive only; Wilson lower, Fisher tests, and promotion gates use the
  independent risk unit. Weather cushion-DS uses contract-date. Cushion-DS
  final-30m scanners use contract-settlement. Per-trade execution shadows use
  the trade row because row count already equals the independent unit. Encoded
  as AGENTS.md Principle 51 on 2026-05-10 after the Gemini weather forensic.
- Proper Index/FX cushion DS shadow: workspace
  `scripts/cushion_ds_multi_series_scanner.py`, table
  `shadow_index_fx_cushion_ds`. Mechanism: proper final-30m cushion DS
  on continuous index/FX underlyings. Spot feeds are Yahoo 1-minute chart
  metadata, rows are skipped when `spot_age_seconds > 60`, and Kalshi
  settlement is the resolver. Reports show row-level descriptive metrics plus
  contract-settlement-collapsed decision-grade metrics. Gate: n>=30 independent
  executable contract-settlements per series with Wilson lower above breakeven
  and positive collapsed P&L before live pilot evaluation.
- Gemini proper cushion DS shadow: workspace
  `scripts/gemini_cushion_ds_shadow.py`, table
  `gemini_cushion_ds_shadow`. Mechanism: proper final-30m cushion DS on
  numeric crypto and commodity ladder contracts. It excludes reference-strike
  UP contracts and path-dependent touch contracts. Fillability is depth-aware
  via Gemini REST `/v1/book/{instrumentSymbol}`.
- `shadow_gemini_cushion_ds`: forward-only proper cushion-DS shadow on
  Gemini's full crypto ladder universe: BTC, ETH, SOL, XRP, and ZEC. It is
  populated by `scripts/gemini_cushion_ds_scanner.py` on a separate passive
  timer and records spot age, 60-second spot jitter, and side-specific depth
  bands. Reports show row-level descriptive metrics plus
  contract-settlement-collapsed decision-grade metrics. Gate: n>=30 independent
  executable contract-settlements per asset with Wilson lower above breakeven
  and positive collapsed P&L before any live pilot or expansion evaluation. This is distinct from the
  legacy `gemini crypto` favorite-tracking shadow and from the older
  `gemini_cushion_ds_shadow` broad numeric-ladder table.
- Gemini DS edge hypothesis: Scope 3 research file
  `research/2026-05-10-gemini-ds-edge-investigation.md` compares Gemini DS
  against Kalshi DS on breakeven economics, cushion, spot staleness, depth,
  and settlement-window timing. The current working hypothesis is that
  Gemini's tight breakeven is a compounding economics problem: high entry
  prices make losses much larger than wins, while narrow cushion and spot
  movement leave little margin for error.
- Weather cushion DS shadow: workspace
  `scripts/weather_cushion_ds_shadow.py`, table
  `weather_cushion_ds_shadow`. Mechanism: NWS-cushion weather DS normalized
  per platform/city-or-station/direction/side/cushion-bucket cell from Kalshi
  and IBKR source rows plus Gemini mapped weather rows. Gemini station mapping
  source: `gemini-weather-nws-mapping.md`. Reports show row-level descriptive
  metrics plus contract-date-collapsed decision-grade metrics; gate decisions
  require n>=30 independent executable contract-date groups with Wilson lower
  above breakeven and positive collapsed P&L. Gemini weather rows persist
  actual NWS settlement temperatures forward-only at resolution time:
  `actual_temp_f`, `actual_temp_station`, `actual_temp_event_date`,
  `actual_temp_source`, and `actual_temp_fetched_at`. Future live pilot
  consideration must use the pre-committed Weather DS time-window rule in
  `dispatch-conventions.md`: high-temperature contracts use actionable
  observations from 10:00 local station time through the stated high cutoff;
  low-temperature contracts use 00:00-08:00 local station time.
- Gemini sports mapping audit: workspace
  `scripts/gemini_sports_mapping_audit.py`, tables
  `gemini_sports_mapping_audit` and `gemini_sports_espn_mapping`.
  Mechanism: prerequisite cell mapping only; no sports DS row is valid unless
  the contract is a single-game moneyline/totals/spreads contract mapped to an
  ESPN game id. Current mapping source:
  `gemini-sports-espn-mapping.md`.
- Gemini expanded-universe shadow: workspace
  `scripts/gemini_universe_enumerator.py`, table
  `gemini_universe_observations`.
- Comprehensive DS coverage inventory: workspace
  `scripts/ds_shadow_coverage_inventory.py`; report section
  `SHADOW COVERAGE INVENTORY`.
- Sports DS forward quote capture: workspace
  `scripts/sports_ds_forward_scanner.py`, tables
  `sports_ds_forward_detections`, `sports_ds_forward_quotes`.
  Sports is not forced into `shadow_index_fx_cushion_ds` because game state
  lacks a simple numeric spot/strike cushion; it remains a separate
  quote-capture and per-cell research path.
- Volatility-Implied Binary Pricing: workspace
  `scripts/vol_implied_binary_scanner.py`, table `vol_implied_signals` in
  Gemini/Kalshi bot DBs. Paused 2026-05-05 with
  `KILL_VOL_IMPLIED_BINARY` pending methodology rebuild for timing
  contamination and side-aware aggregation issues.
- Comprehensive coverage map: operations knowledge
  `comprehensive-shadow-coverage.md`.

Shadow storage lifecycle:

- DS shadow archive layer: workspace `scripts/ds_shadow_archive.py`,
  `scripts/ds_shadow_archive_policy.py`, and `scripts/ds_shadow_archive_reader.py`.
  Active writes stay in `data/ds_shadow_expansion.db`; read-only monthly
  archives live under `data/archive/`. Live strategies do not write this DB.
  Resolvers update active rows only. Per-table policy keeps resolver-mutable
  rows active until safe and archives immutable observation logs by age.
  Lifetime reports and decision-grade per-cell evaluations use archive-aware
  `all_<table>` views.
- DS shadow category storage controls: workspace
  `scripts/ds_shadow_expansion_lib.py`, `scripts/gemini_universe_enumerator.py`,
  and `scripts/db_category_storage_monitor.py`. The broad DS scanner honors
  reversible `DS_SHADOW_DISABLED_CATEGORIES` platform-scoped tokens plus the
  targeted `DS_SHADOW_SPORTS_BROAD_BACKFILL_ENABLED` broad-sports gate. As of
  2026-05-05 the disabled category set is `kalshi:politics`,
  `kalshi:culture`, `kalshi:business`, `kalshi:tech`,
  `kalshi:climate_science`, `gemini:politics`, `gemini:business`,
  `gemini:culture`, `gemini:tech`, `gemini:economics`, and
  `gemini:weather`; broad sports backfill is disabled separately so
  `sports-ds-forward-scanner.service` can keep its per-cell quote path. Gemini
  commodities remains enabled pending more commodity-cell evidence. Broad
  scanner daily caps are report-visible and default high enough for normal
  productive streams while catching runaway categories. Archive cadence is
  every 6 hours at 03:24/09:24/15:24/21:24 CDT; continuous archive runs every
  10 minutes; storage monitoring runs at 03:40/09:40/15:40/21:40 CDT.

Sizing and scaling shadow-comparison infrastructure:

- Kalshi MR Shadow Kelly Comparison: Kalshi repo
  `kelly_uncertainty_aware.py`, `kelly_drawdown_aware.py`, and
  `kelly_shadow.py`, table `kalshi_mr_kelly_shadow_comparison`.
  Mechanism: Wilson/Bayesian/sample-size-discounted Kelly multiplied by a
  drawdown-tolerance multiplier. It records would-have-sized recommendations
  for each MR placement but does not feed production sizing; existing
  `kelly.py` remains the live path.
- Kalshi DS Cohort Trackers: Kalshi repo `ds_clustered_kelly.py`,
  `ds_cohort_tracker.py`, and `ds_qty_cohort_tracker.py`. Mechanism:
  cap-level cohort decomposition, qty-level cohort decomposition, and
  settlement-hour cluster risk analysis for crypto DS. The cap tracker informs
  max_open decisions only; the qty tracker informs per-trade sizing decisions;
  the `filter_combined_pilot` section tracks the 2026-05-05 price >=0.90 and
  cushion >=0.10% filter cohort.
  Current production DS cap is max_open 8 with max 4 open positions per
  asset/settlement-hour as of 2026-05-06. After the aggregate qty-400 gate
  failed, ETH rolls back to qty 225 and BTC moved qty 400 -> 500 on
  2026-05-07 after `filter_combined_qty_400_btc_pilot` reached 33W-0L,
  Wilson lower 89.6%, +$389.36 P&L; max_open was restored from 5 to 8 to
  improve ETH-heavy window utilization while preserving the asset-hour
  cluster cap. The current qty-specific cohorts are
  `filter_combined_qty_500_btc_pilot` and
  `filter_combined_qty_225_eth_pilot`, each with a 30-resolution review gate.
- Kalshi DS Low-Price NO Pilot: Kalshi repo `bot.py` strategy key
  `ds_low_price_no`, signal table `ds_low_price_no_signals`, and cohort
  tracker `ds_low_price_no_cohort_tracker.py`. Mechanism: independent
  low-stakes live pilot for corrected H1 crypto cells, buying NO only when
  entry price is below $0.80 on BTC/ETH/SOL with pilot qty 10, max open 3,
  separate kill switch `KILL_DS_LOW_PRICE_NO_PILOT`, and separate CB ledgers.
  It does not inherit Kalshi MR blocks, Moderate Favorites state, or the
  high-price crypto DS combined filter.
  Paused 2026-05-06 after 21 resolved trades made the 90% WR gate
  mathematically unreachable; existing open positions settle naturally.
- IBKR Long+Short Kelly Framework: IBKR repo `kelly.py`, table
  `ibkr_long_short_kelly_shadow_comparison`. Mechanism:
  uncertainty-discounted Kelly shadow comparison with an inactive n>=100
  activation gate. Production sizing remains flat `QTY_PER_POSITION=60` until
  a later operator-approved activation decision.
