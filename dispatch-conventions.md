# Dispatch Conventions

Last updated: 2026-05-09

This document captures conventions that dispatch reports must follow so audits and operator review can verify claims at face value. Established after the 2026-05-09 evening audit found several reporting drifts.

## Reconciliation reporting

Dispatch reports that mention reconciliation must surface the actual cash gap as a numeric value, not a pass/fail flag.

- Acceptable: `Reconciliation: cash gap $0.00 (recon_adj $-6.52, baseline $90.55)`
- Acceptable: `Reconciliation: cash gap $0.00`
- Not acceptable: `Reconciliation: PASS`
- Not acceptable: `Reconciliation: ✓` (without a numeric reading)

The Kalshi/Gemini reconciliation system uses three distinct quantities. They must not be confused.

- `cash_gap`: actual_cash_from_API − expected_cash_from_equation. This is what reconciliation discipline ("deposits + SUM(pnl) + mark_of_open must equal exchange balance; gap = bug") refers to. Acceptable PASS only if `abs(cash_gap) < $1.00`.
- `recon_adj`: auto-computed correction term that the bot inserts into the equation so cash_gap stays at $0.00 by construction. This value moves as positions open/close and as new resolutions accumulate. A drift of more than $5 between consecutive snapshots indicates a recent trade may have wrong P&L; the report's HARD CHECK section calls this out automatically.
- `documented_baseline`: a one-time absorption that captures structural unverifiable variance (Kalshi has $90.55, Gemini does not yet have one). Recon_adj is then the residual on top of the baseline.

The Kalshi/Gemini bot status reports already render all three correctly in the `RECONCILIATION CHECK` section. Dispatch summaries that condense this should preserve the cash_gap value, not just the pass/fail.

## IBKR-specific

IBKR has two separate reconciliation tracks:

- Cash reconciliation: must show $0.00 gap. The IBKR status report's `[9] RECONCILIATION` block reports this as `cash gap $XX.XX`.
- `statement_live_nlv_delta`: market movement between when the Flex statement snapshot was taken and the current API NLV reading. Expected to be non-zero between snapshots; not a gap. The IBKR status report exposes this separately.

Dispatch reports that mention IBKR reconciliation must distinguish these two. A `statement_live_nlv_delta` of $20 or less is normal market movement; values above $20 warrant operator awareness but do not automatically halt a deploy.

## Scope boundaries

As of 2026-05-09 EOD, IBKR ForecastEx is under autonomous Codex goal control.
Operator-authored dispatches must mark IBKR as out-of-scope unless the operator
explicitly lifts that boundary. Cross-platform reports may reference IBKR data
for context, but operator dispatches must not propose or execute IBKR actions,
restart `ibkr-scan-loop.service`, edit `ibkr_forecast_bot`, or change IBKR
strategy configuration.

## Pre-flight reconciliation gate

Every dispatch's pre-flight verification must:

1. Read the bot's `reconciliation_adjustments` table for each platform.
2. Compute the cash gap using the same formula the bot's `_compute_hard_reconciliation` uses (deposits + resolved + recon_adj + documented_baseline − open_cost − open_fees [− legacy] = expected_cash; cash_gap = cash − expected_cash).
3. Surface the cash_gap value, the recon_adj value, the documented_baseline (if any), and the previous-vs-current recon_adj drift.
4. If any platform's cash_gap > $1.00, the dispatch must FLAG and surface for operator awareness before proceeding.
5. If recon_adj has drifted by more than $5 in the past 24 hours, surface as a warning but do not block.

## Test count claims

Dispatch reports must be explicit about test scope. Acceptable forms:

- `focused storage suite 38/38 OK` — when a specific subset is run.
- `full workspace test suite 253/254 OK (1 known cross-module memoization failure: test_gemini_weather_range_actual_outcome_from_cached_nws — passes in isolation)` — when the whole suite is run.
- `Kalshi: 23/23 top-level + 51/51 scripts OK; Gemini: 28/28 scripts OK; Workspace: 253/254 OK` — when multiple repos.

Not acceptable: `38/38 tests pass` without scope, when the actual full suite has 254 tests.

## Commit and push reporting

Dispatch reports must be honest about whether commits were pushed to a remote.

- If a remote is configured: `committed; pushed to origin (verified with git ls-remote)`.
- If no remote is configured: `committed locally; remote not configured (deferred for operator)`.
- Not acceptable: `pushed to origin` when no remote is configured.

As of 2026-05-09, the four repos (kalshi_favorites_bot, gemini_prediction_bot, .openclaw/workspace, operations-knowledge) have no remote configured. All historical "pushed to origin" claims were inaccurate; commits were local-only. The operator will provide remote URLs in a follow-up dispatch.

## Numeric drift in cohort reports

Cohort tracker numbers (resolved count, W-L, P&L) shift through the day as natural fills resolve. Dispatch reports that quote a snapshot must:

- Mark the snapshot timestamp (UTC).
- Note that the cohort is OPEN and accumulating if applicable.
- Allow the audit to find a slightly higher resolved count without flagging as a discrepancy.

Acceptable example: `filter_combined_qty_500_btc_pilot CLOSED at 60 resolved 59W-1L +$435.94 (snapshot 2026-05-09T13:56 UTC; subsequent natural fills can move this slightly higher)`.

## SHA verification depth and method

Use `git rev-parse <sha>` (or `git rev-parse --verify <sha>`) to confirm a SHA exists. This works regardless of how deep the commit is in history and regardless of whether it's on the current branch.

Do not rely solely on `git log --oneline | grep <sha>` for verification — the 2026-05-09 audit's `git log -10 | grep` was both too shallow (only 10 commits) and unreliable (`325a87c6` exists in operations-knowledge as `325a87c Classify Kalshi sports storage and retention escalation` but the grep didn't find it on the first remediation pass). `rev-parse` is authoritative.

If the dispatch report cites a SHA, the pre-flight check should fail the dispatch when `git rev-parse <sha>` returns non-zero.

## Remote configuration verification

Use `git remote -v` and `git rev-parse origin/master` (or `origin/main`) to verify a remote is configured and to read the remote HEAD. Do not use `git rev-parse origin/HEAD` — origin/HEAD is a symbolic ref that is not always set on cloned-then-detached working copies, and its absence does not mean no remote is configured.

Example correct check:

```bash
git -C <repo> remote -v                 # shows fetch + push URLs
git -C <repo> rev-parse origin/master   # shows remote master HEAD
git -C <repo> rev-list --left-right --count master...origin/master  # ahead/behind
```

The 2026-05-09 audit and the first remediation pass both falsely concluded "no remotes configured on any of the four repos" because they used `git rev-parse origin/HEAD`. In fact all four repos (kalshi_favorites_bot, gemini_prediction_bot, .openclaw/workspace as `rahm-workspace`, operations-knowledge) have GitHub remotes pointing at the operator's PhotonRahm account. `gh auth status` confirms operator authentication; `gh repo list` shows all repos.

## Numeric claims about row counts

Numeric claims about table row counts in dispatch reports should specify:
- The exact table name.
- The platform/category/other filter applied.
- The timestamp of the count (in UTC).
- The SQL query used.

Drift over hours or days is expected because autonomous retention engines, archives, and pruning runs all change row counts. The 2026-05-09 storage stabilization dispatch's "401,173 active rows" claim could not be reproduced after-the-fact because the count was a snapshot during a transition state. Future dispatches should phrase such numbers as `"snapshot at HH:MM UTC: 401,173 rows in <table> matching <filter>"` rather than as a stable assertion.

## Repo sync health invariant

Every dispatch's pre-flight should run `verify_repo_sync()` (per `database_autonomous_maintenance.py`) on the four tracked repos and report:

| Field | Meaning |
|---|---|
| `has_remote` | true if `remote.origin.url` is configured |
| `remote_url` | the URL itself |
| `local_head` | local HEAD SHA |
| `remote_head` | origin/master (or origin/main) HEAD SHA |
| `in_sync` | local_head == remote_head |
| `ahead` | commits on local not on remote |
| `behind` | commits on remote not on local |
| `hours_since_local_commit` | for ahead-but-not-pushed cases |

A dispatch must FLAG if any repo has `has_remote=false`, `behind > 0`, or `ahead > 0` with `hours_since_local_commit > 24`. The daily 05:40 maintenance run includes this check and surfaces failures as TOP_RISK in the daily report.

The four tracked repos are:
- `~/kalshi_favorites_bot` → `https://github.com/PhotonRahm/kalshi_favorites_bot.git`
- `~/gemini_prediction_bot` → `https://github.com/PhotonRahm/gemini_prediction_bot.git`
- `~/.openclaw/workspace` → `https://github.com/PhotonRahm/rahm-workspace.git`
- `~/operations-knowledge` → `https://github.com/PhotonRahm/operations-knowledge.git`

`~/.openclaw/workspace/ibkr_forecast_bot` is a nested git repo with its own remote at `https://github.com/PhotonRahm/ibkr_forecast_bot.git`; the workspace's `.gitignore` excludes it from the workspace tree. It is pushed by the same daily backup script.

## Cross-agent context

Dispatches authored by Claude-in-chat:
- Must reference `current-state.md` for live operational claims.
- Must cite AGENTS.md principle numbers when invoking architectural rules.
- Must cite this file when invoking vocabulary or reporting conventions.
- Must be standalone for Codex/Claude Code execution; do not assume hidden
  prior-chat context.

Reports authored by Codex or Claude Code:
- Use this vocabulary exactly, especially `cash_gap`, `recon_adj`, and
  `documented_baseline`.
- Cite commit SHAs verified with `git rev-parse`, not shallow `git log | grep`.
- Surface numeric gap values, not only PASS/FAIL labels.
- Distinguish claimed, configured, running-process, and report-rendered state.

Stable cross-references:
- Dispatch date + section number.
- Commit SHA.
- Cohort name.
- Verification-deferred trigger id.
