---
title: The Prediction Engineer
category: entity
summary: Builder-AI-lab YouTuber ("The Prediction Engineer") focused on **code + AI agents + data to find edges in markets and business** (crypto trading); enters the vault via *I Rebuilt My Ai's Brain Using the Karpathy Method (LLM Wiki)* (2.1K views, 2026-04-06) — a **Day-8 build-log** where his autonomous crypto-trading agent is *"demented"* (no state/memory between days, forgets APIs, file structures, strategy), so he **rebuilds its memory architecture using Karpathy's [[karpathy-llm-wiki|LLM Wiki]] method instead of vector-DB RAG** ("too slow and imprecise for coding tasks"), gives the agent **autonomy to edit its own wiki files**, and runs a **start-of-day `daily_plan.md` / end-of-day lessons-learned** loop; a **vertical (crypto-trading) instantiation of the exact pattern this vault runs on** — the trading-domain sibling of [[tonbi-onchain-ai-garage]] and [[corey-ganim]]
tags: [creator, youtube, karpathy-llm-wiki, llm-wiki, crypto-trading, autonomous-agents, state-management, memory-architecture, anti-rag, vector-db, daily-plan, self-editing-wiki, prediction-engineer, build-log, discord, vertical-implementation]
sources: 1
updated: 2026-06-24
---

# The Prediction Engineer

## What it is

Person + YouTube channel **The Prediction Engineer**, plus a Discord community ("**Prediction Engineer Build Lab**") — *"a builder AI lab for people using code, AI agents, and data to find edges in markets and business."* The lens is **autonomous crypto-trading agents.** Enters the vault through the [[youtube-digest-apify-2026-06-24]] batch.

## Key video in [[youtube-digest-apify-2026-06-24]]

- #14 *I Rebuilt My Ai's Brain Using the Karpathy Method (LLM Wiki)* — 2.1K views, 2026-04-06, 7:55. A **back-catalog** entry, framed as **"Day 8"** of a build series.

**The problem:** building an autonomous AI agent for crypto trading, his agent is *"demented"* — *"it has no concept of state or state management between days, meaning it constantly forgets APIs, file structures, and strategy decisions."* Silent failures everywhere.

**The rejected fix:** *"Standard RAG (Retrieval-Augmented Generation) using Vector DBs is too slow and imprecise for coding tasks."* — an explicit **anti-vector-DB** stance for agentic coding/state work.

**The solution:** he **rebuilds the agent's entire "brain" and memory architecture using the [[karpathy-llm-wiki|LLM Wiki]] method championed by [[andrej-karpathy]]**:

- Gives the AI agent **autonomy to edit its own wiki files** (1:51)
- **Start-of-day workflow** producing a `daily_plan.md` (2:33)
- **End-of-day** capture of lessons learned + updates to the long-term wiki (3:27)
- Re-deploys a prior failure against the new memory (Day-9 teaser, 4:13)

*(Disclaimer in-source: NOT FINANCIAL ADVICE.)*

## Why it matters for this wiki

- **A vertical, agentic instantiation of the exact pattern this vault runs on.** Where most vault [[karpathy-llm-wiki]] coverage is *human-facing knowledge management* ([[nate-herk]], Teacher's Tech, [[brad-bonanno]]'s company brain), the Prediction Engineer uses the wiki as **an autonomous agent's working memory** — the agent both *reads and writes* its own wiki to maintain state across runs. That's the LLM-Wiki-as-agent-state-store variant.
- **The start-of-day/end-of-day loop mirrors this vault's farm cadence** — `daily_plan.md` + end-of-day lessons-learned is structurally the same as the vault's scheduled farm → ingest → log rhythm, and a close cousin of [[self-improving-skills]]' overnight convergence.
- **An explicit anti-RAG datapoint for agentic state** — reinforces the [[karpathy-llm-wiki]] "write-time structured memory beats query-time chunk retrieval" thesis, specifically for *coding/state* tasks where precision matters.
- **The trading-domain sibling of [[tonbi-onchain-ai-garage]]** (trading-strategy wiki) and [[corey-ganim]] (Hermes-on-Hostinger second brain) — confirms the pattern keeps recurring in the crypto/markets vertical.

## Adoption-tier signal

A **Tier-3 (sub-3K-view) vertical implementation** — small channel, but a *distinct architectural variant* (agent self-editing its own wiki as state) rather than another generic explainer. Adds the **autonomous-agent-state** cell to the [[karpathy-llm-wiki]] implementation matrix.

## Distribution channels

- YouTube (primary, build-log series format)
- **Discord** — "Prediction Engineer Build Lab" (`discord.gg/tcrF2kNUzs`)
- Business/consulting contact: `predictionengineer@gmail.com`

## Why track him for 3Ps

- **Agent-state-via-wiki is a portable architecture** — the self-editing-wiki-as-memory pattern is directly relevant to any long-running autonomous agent the vault might run; worth diffing against the vault's farm-state approach.
- **Build-log format** — the "Day N" series is a credible content model for documenting an evolving AI system in public ([[public-ai-work]]).

## Open questions

- **Channel size / cadence**, and how far the "Day N" series runs.
- **Does the self-editing wiki hold up** over many trading days, or does editorial drift accumulate (the [[karpathy-llm-wiki]] "errors get baked in" risk, amplified when the *agent* is the editor)?
- **What's the trading edge** (if any) — or is the channel primarily about the architecture? (NOT FINANCIAL ADVICE caveat noted.)

## Related

- [[karpathy-llm-wiki]] — the method he implements as agent state (self-editing variant)
- [[tonbi-onchain-ai-garage]] — trading-strategy wiki; nearest vertical neighbor
- [[corey-ganim]] — second-brain implementation sibling
- [[self-improving-skills]] — the overnight-loop cousin of his day-cycle
- [[andrej-karpathy]] — originator of the LLM Wiki pattern
- [[public-ai-work]] — the build-in-public format
- [[youtube-digest-apify-2026-06-24]] — vault entry point
