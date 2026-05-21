# Claude-In-Chat Startup Procedure

This file is loaded into Claude.ai project knowledge from the public
`PhotonRahm/rahm-claude-chat-bundle` repository.

When you start a new Rahm project conversation, do this before answering the
operator's first message.

## Step 1: Fetch The Bundle Index

Use `web_fetch` on:

`https://raw.githubusercontent.com/PhotonRahm/rahm-claude-chat-bundle/main/INDEX.md`

The index gives the URLs, tiers, and checksums for the current public bundle.

## Step 2: Fetch Tier 1

Always fetch:

- `https://raw.githubusercontent.com/PhotonRahm/rahm-claude-chat-bundle/main/current-state.md`
- `https://raw.githubusercontent.com/PhotonRahm/rahm-claude-chat-bundle/main/CLAUDE-CHAT.md`

`current-state.md` gives live operational state: bot PIDs, reconciliation
status, active cohorts, P&L excerpts, deferred items, recent decisions, storage
state, timers, and repo state.

## Step 3: Decide Whether To Fetch Tier 2/3

- Dispatch authoring or strategic analysis: fetch `AGENTS.md` and
  `dispatch-conventions.md`.
- Storage/database questions: fetch `ds-storage-runbook.md`.
- Historical-decision questions: fetch `operator-decision-log.md`.
- Strategy naming/config questions: fetch `strategies-glossary.md`.
- Quick conversational questions: skip Tier 2/3.

Re-fetch mid-conversation if the topic shifts. `web_fetch` is fast, but fetched
files consume context tokens, so be deliberate.

## Step 4: Verify Freshness

Use a two-layer freshness check.

### Layer 1: Pipeline Heartbeat (Primary)

Check `pipeline_heartbeat_utc` from `INDEX.md` first. Compare it with the
operator wall-clock. If it is older than 12 hours, surface:

`Bundle pipeline_heartbeat is <X> hours old. Either the autonomous sync is failing OR a caching layer is serving stale content. Investigate before relying on operational claims.`

This is the primary freshness signal because it is written from wall-clock time
at sync/generation time and catches both server-side sync failure and
consumer-side stale-cache reads.

### Layer 2: Current-State Timestamp (Secondary)

Check the `last_updated_utc` timestamp in `current-state.md`. If it is older
than 12 hours, surface:

`Current-state is from <X> hours ago; the autonomous sync runs every 6 hours, so this may indicate a sync failure. Should we investigate?`

### What This Catches

- `pipeline_heartbeat_utc` stale: the bundle you fetched may be old even if a
  cached `current-state.md` appears internally consistent.
- `last_updated_utc` stale: the generated operational snapshot itself may be
  old even if the index was reachable.
- Both stale: treat the bundle as operationally unsafe until Codex verifies the
  sync pipeline from Rahm.

## Step 5: Respond

With state loaded, respond to the operator's first message.

## Operating Model

Claude-in-chat is one of four entities in the Rahm operation:

- Codex executes dispatches on Rahm.
- Claude Code audits and edits from the Rahm filesystem.
- Rahm is the live Ubuntu host and single source of truth.
- Claude-in-chat authors dispatches and strategic analysis from claude.ai.

## Core Vocabulary

- `cash_gap`: actual cash minus expected cash. This is the reconciliation gate.
- `recon_adj`: accounting correction term, not the pass/fail value.
- `documented_baseline`: explicit known baseline in the hard-check equation.
- `PROTECT_TRADING`: storage hard-limit mode that blocks non-trading shadow
  writes; live trading bots remain untouched.
- `TIER_A` through `TIER_E`: storage value tiers. Only explicit TIER_E can be
  autonomously pruned.

## Avoid

- Do not assume knowledge from prior chats without checking `current-state.md`.
- Do not claim commits, pushes, deploys, or service restarts occurred.
- Do not invent environment details not present in fetched current state.
- Do not treat `recon_adj` drift as a reconciliation failure when `cash_gap` is
  zero.

## Token Budget Guidance

Tier 1 is the default overhead for every Rahm chat. Tier 2 is for dispatches and
operational analysis. Tier 3 is topic-specific. Do not fetch the full bundle
unless the operator's request needs it.
