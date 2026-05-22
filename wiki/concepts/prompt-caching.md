---
title: Prompt Caching (Anthropic / Substrate Economics)
category: concept
summary: The Anthropic substrate-economics primitive that "saves 300M+ tokens a week without you doing anything" — cache writes are slightly above standard input cost, **cache reads are ~90% cheaper than fresh inference**, the **hit rate is the metric that matters**; first explicit deep-dive in this vault from [[nate-herk]] 2026-05-21 (17K views, 10:43), referencing **Thariq's article** (`x.com/trq212/...`) as the canonical authoritative source; names **the cache grows each turn** (prefix appends compound across session), **cache TTL** (~5min default), and **three habits** to protect session limits (stable instructions / append-don't-insert / TTL-aware long-context use) + **what breaks the cache** (system-prompt changes / file rearrangement / mid-session tool changes); the per-session economics complement to [[free-sample-phase]] (macro-economics)
tags: [prompt-caching, anthropic, claude-code, cache-hit-rate, session-economics, substrate-pricing, nate-herk, thariq, ttl, token-savings, claude-skills, free-sample-phase, agent-metering]
sources: 1
updated: 2026-05-22
---

# Prompt Caching (Anthropic / Substrate Economics)

## What it is

Anthropic's API-level primitive that caches the **prefix** of an LLM conversation so subsequent turns can reuse it at ~10% of standard inference cost. The mechanic is invisible to users in most Claude Code sessions, but the economics drive **substantial savings** at scale — [[nate-herk]] cites "300M+ tokens a week" saved in his own usage without manual intervention.

**The framing claim** (from [[nate-herk]]'s deep-dive): *"Prompt caching is the reason Claude Code can save you 300M+ tokens a week without you doing anything."*

## Why Anthropic cares about hit rate (chapter 1:14)

Anthropic's pricing model **rewards cache hits** — cache reads are ~90% cheaper than fresh inference. This means:

- **User incentive**: cheaper sessions when you build cache-friendly habits
- **Anthropic incentive**: lower compute load per active user → higher infrastructure margin
- **Aligned incentive**: behaviors that build caches are mutually beneficial

The hit rate is therefore the **canonical instrumentation surface** for both sides. Pairs with [[agent-metering]]'s "the meter is changing" thesis from a substrate-economics angle — caching is **how the token-meter is partially offset** at the substrate level.

## How the cache grows each turn (chapter 2:16)

The mechanic:
- Cache stores the **prefix** of a conversation (system prompt + early turns + tool/skill definitions)
- Each new turn appends to the prefix
- The cache prefix gets **longer the deeper you go** in a session
- Deeper sessions = more cached tokens = cheaper-per-turn marginal cost

The compounding mechanic means **long sessions are more economical than short sessions** for the same total work — opposite intuition to most cost optimization patterns.

## Cache TTL confusion (chapter 5:00)

- **Default TTL**: ~5 minutes (the Anthropic prompt-cache window)
- **Implication**: gaps over 5 minutes between turns invalidate the cache
- **Extension**: TTL can be extended at higher cache-write cost; pricing trade-off
- **Vault-relevant**: this is why long-running sessions with frequent activity outperform long-running sessions with sparse activity. Scheduled farmers (this vault's `ai-creators-youtube` daily cron) optimize cache-friendliness if the cron cadence is **inside the TTL window** for any given session.

## Three habits to stop burning tokens (chapter 6:14)

The behavioral checklist:

| Habit | What it means | Anti-pattern |
|---|---|---|
| **1. Keep instructions stable across turns** | Don't rewrite CLAUDE.md / system prompts mid-session | Editing CLAUDE.md while a session is active |
| **2. Append, don't insert** | New context goes at the end of the conversation; never inserted into earlier turns | Editing prior messages mid-session |
| **3. Use long-context less aggressively when caching matters** | TTL renewal on small turns is cheaper than full context reload | Stuffing every turn with maximum context |

The three habits map cleanly onto **vault practice**:
- Stable CLAUDE.md (this vault: schema-frozen)
- Append-only log.md (this vault: log.md is append-only by spec)
- TTL renewal pattern (this vault: scheduled farms hit cache repeatedly)

The vault's architecture is **already cache-friendly by design**. The three habits formalize what `/wiki-ingest` and `/wiki-query` patterns implicitly follow.

## What breaks the cache (chapter 7:43)

The cache-invalidation surface:

| Trigger | Why it breaks |
|---|---|
| **System prompt change** | Cache prefix starts at system prompt; changing it invalidates everything |
| **CLAUDE.md change** | Same reason — CLAUDE.md is part of the prefix |
| **File rearrangement** | Order of inputs changes the prefix; reorder = new cache |
| **Tool/skill definition change** | Tool schemas live in the prefix; changing schemas mid-session = new cache |
| **TTL expiry** | Default 5-min window — long gaps = new cache |

Implication for vault maintenance: **edit CLAUDE.md only between sessions**, not during. Same for skills, tool definitions, and farmer configs.

## "91 Million Tokens Saved" (intro hook, chapter 0:00)

The headline anchor — Nate's personal usage shows 91M tokens saved by caching over a single accounting window. Used as the **canonical scale anchor** for "this matters at individual scale, not just enterprise."

## Free Token Dashboard + Session Handoff Skill (chapter 9:15)

[[nate-herk]] mentions two community-gated artifacts:
- **Free Token Dashboard** — visualizes cache hit rate + token consumption (gated to his Skool community)
- **Session Handoff Skill** — preserves session context across explicit handoff boundaries (also community-gated)

Both are **diagnostic + intervention tools** — pairs with [[brad-bonanno]]'s Context Audit skill as the two community-shipped token-economics tools tracked in this vault.

## Thariq's article reference

Nate cites **Thariq Shihipar's article** (`x.com/trq212/status/202457413...`) as the upstream authoritative source on prompt-caching mechanics. This is the **canonical reference doc** for prompt-caching deep-dive — worth ingesting separately as a raw source in a future cycle.

Open question: is the Thariq article a standalone X thread or a longer published piece (Substack, Medium, blog)?

## Position in the substrate-economics stack

| Layer | Framework | Time-scale |
|---|---|---|
| **Macro** | [[free-sample-phase]] | Months (retention war between labs) |
| **Pricing model** | [[agent-metering]] | Renewal cycle (per-vendor metering shape) |
| **Per-session** | **[[prompt-caching]]** | **Within-session (5-min TTL window)** |

The three frameworks together describe **the full economics surface** Anthropic users navigate:
- Free-sample-phase: macro lock-in dynamics during the retention war
- Agent-metering: per-vendor pricing primitives at renewal
- Prompt-caching: per-session cost mechanics

## Strategic significance

1. **First explicit prompt-caching deep dive** in this vault — fills a gap that prior coverage ([[free-sample-phase]] macro / [[agent-metering]] pricing) didn't directly address
2. **The hit-rate metric is the canonical instrumentation surface** — pairs with [[brad-bonanno]]'s Context Audit skill (token-bloat scanner) as the two power-user diagnostic tools
3. **"Anthropic cares about hit rate"** is explicit substrate-economics signal — Anthropic's pricing rewards cache-friendly behavior. The user's vault behavior compounds favorably with Anthropic's incentive structure.
4. **The three habits formalize this vault's accidental cache-friendliness** — stable CLAUDE.md, append-only log.md, scheduled-cron cadence are all cache-friendly. The vault's design is **already economically optimal** for prompt-caching.
5. **Thariq's article is an upstream authoritative reference** — worth ingesting separately as a raw source

## Related

- [[nate-herk]] — author of the deep dive
- [[free-sample-phase]] — macro-economics complement
- [[agent-metering]] — pricing-layer complement
- [[claude-code]] — primary substrate
- [[claude-skills]] — skill definitions live in the cached prefix
- [[anthropic]] — substrate sponsor
- [[brad-bonanno]] — Context Audit skill (token-bloat scanner) sibling
- [[ai-question-method]] — long-running senior-partner sessions benefit from caching economics
- [[karpathy-llm-wiki]] — long-session memory layer + caching = compounding economics

## Used in

- [[youtube-digest-apify-2026-05-22]] — primary citation ([[nate-herk]] #9)

## Open questions

- **Thariq's article** — full text + format (standalone thread / longer piece)? Worth ingesting as raw/.
- **Cache TTL extension pricing** — exact ratio of extended-TTL write cost to default-TTL write cost
- **Multi-session cache** — does Claude Code reuse cache across sessions when prefixes match? (Or is cache session-scoped?)
- **Free Token Dashboard internals** — what specifically does it visualize? (Worth joining [[nate-herk]]'s Skool to inspect)
- **Cache + skill loading interaction** — when skills are dynamically loaded mid-session, does that invalidate cache for the unloaded skills?
- **OpenAI / [[codex]] equivalent** — does Codex have parallel caching mechanics, or is this an Anthropic-specific economics primitive? (Critical for [[free-sample-phase]] portability)
