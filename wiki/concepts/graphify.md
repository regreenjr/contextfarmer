---
title: Graphify (Knowledge Graph for Claude Code)
category: concept
summary: An open-source tool ([github.com/safishamsi/graphify](https://github.com/safishamsi/graphify)) that builds a **knowledge graph of a codebase** so [[claude-code]] can read the *map* instead of skimming the whole repo every session — cheaper, faster, more accurate answers and far fewer wasted tokens. Surfaced via [[jack-roberts]]' *Claude Code + Graphify = Insane Agentic OS* (23.4K views, 2026-06-08, 10:21). The video's larger move: plug Graphify into an **agentic operating system** with [[hermes-agent|Hermes]] + a custom dashboard to get **one shared brain across Claude Code, laptop, and mobile** — and import any GitHub repo into the graph. A retrieval/context-compression substrate layer; the codebase-scale, query-time instantiation of the [[retrieval-contract]] problem
tags: [graphify, knowledge-graph, claude-code, jack-roberts, token-savings, code-retrieval, context-compression, agentic-os, hermes-agent, antigravity, repo-map, retrieval-contract, code-comprehensibility, open-source, safishamsi, shared-brain, cross-device]
sources: 1
updated: 2026-06-09
---

# Graphify

## What it is

**Graphify** is an open-source tool that **builds a knowledge graph of any project** so an agent can query the graph instead of re-reading the repository on every session. Repo: `github.com/safishamsi/graphify`. Surfaced in this vault via [[jack-roberts]]' *Claude Code + Graphify = Insane Agentic OS* ([[youtube-digest-apify-2026-06-09]] #5, 23.4K views, 2026-06-08, 10:21).

The problem it targets (Jack's framing): *"Graphify just solved Claude Code's biggest problem… it builds a knowledge graph of any project so Claude can read it instead of skimming the whole repo every single session. That means cheaper, faster, more accurate answers, and way fewer wasted tokens."*

The mechanism: instead of the agent burning context re-discovering a codebase's structure each run (skim files → infer relationships → answer), Graphify **pre-compiles** that structure into a graph the agent reads as a map. The map names the entities (files, modules, functions) and their relationships up front.

## How it works (chapter map)

| Time | Chapter | What it covers |
|---|---|---|
| 0:00 | Graphify Solves Claude's Problem | the re-skimming waste |
| 0:46 | What Graphify Actually Does | builds the project knowledge graph |
| 1:21 | **How The Map Works** | the graph structure |
| 2:10 | **Why Maps Save Tokens** | read the map, not the whole repo |
| 3:17 | Install And Set Up | |
| 4:38 | See The Knowledge Graph | visual graph of the repo |
| 5:04 | **Query Any Repo Live** | ask questions against the graph |
| 5:43 | Take It Further | |
| 6:07 | Inside The Operating System | the [[hermes-agent|Hermes]]-based agentic OS |
| 7:32 | **Import Any GitHub Repo** | pull any repo into the graph |
| 8:07 | Chat To Your Projects | conversational query over the graph |
| 9:04 | **Connect Everything Together** | one shared brain across devices |
| 10:04 | Visual Interface Wins | dashboard over raw terminal |

## Why maps save tokens (chapter 2:10)

The substrate-economics core. Re-reading a large repo on every session is a recurring token tax: the agent pays to rediscover the same structure each time. A compiled graph turns that recurring cost into a **one-time build** plus cheap lookups. This is the same "stop paying for rediscovery on every run" argument [[nate-b-jones]] makes for [[retrieval-contract]] — Graphify is that thesis **instantiated at codebase scale, query-time**: it's a compiled-knowledge retrieval layer where the "documents" are source files and the "entities/relationships" are the call graph and module structure.

It's also the **read-side complement** to [[code-comprehensibility]]: where Mythos reads code to find vulnerabilities at scale, Graphify reads code to make its *structure* cheaply queryable — both treat "the agent can understand this codebase" as the unlock, one for security, one for token-efficient navigation.

## The agentic OS layer (chapters 6:07–9:04)

The video's bigger claim is not just the graph but the **system it plugs into**: Graphify + [[hermes-agent|Hermes]] + a custom dashboard = an **agentic operating system** with **one shared brain across Claude Code, your laptop, and your mobile**. You can **import any GitHub repo** (7:32) into the graph and **chat to your projects** (8:07) conversationally. *"Connect everything together"* (9:04) is the one-shared-brain payoff: the same context substrate accessible from terminal, desktop, and phone.

This makes Graphify a **context layer inside [[hermes-agent]]'s always-on topology** — the knowledge-graph "brain" that Hermes serves across surfaces. It's the cross-device shared-context pattern [[ai-operating-system]] gestures at ("one source of truth"), built on a repo graph rather than a wiki.

## Tools named

- **Graphify** — `github.com/safishamsi/graphify` (open source)
- **[[claude-code]]** — the agent that queries the graph
- **[[hermes-agent|Hermes]]** — the always-on agent the OS is built around
- **AntiGravity** (`antigravity.google/`) — Google's agentic IDE, connected into the dashboard (first vault surfacing by name)
- **GitHub** — repo source for imports

## Strategic significance

1. **Retrieval-as-substrate goes mainstream-creator** — a tier-2 creator (203K subs) shipping "knowledge graph for your repo cuts Claude's token cost" content means the [[retrieval-contract]] thesis has reached the build-tutorial layer, not just [[nate-b-jones]]' analyst framing. The *rediscovery problem* now has a named, installable, open-source answer in the vault.
2. **Token-cost is the headline benefit** — same operator-economics frontier as [[dynamic-workflows]]' token warning, [[claude-subagents]]' cheaper-model levers, and [[prompt-caching]] habits. The 2026 creator consensus is consolidating around "the binding constraint is context/tokens, manage them" (cf. [[harness-over-model]]).
3. **Cross-device shared brain is the [[ai-operating-system]] frontier** — "one brain across Claude Code, laptop, mobile" is the multi-surface version of the AIOS "one source of truth" thesis, here realized through a graph + Hermes rather than a local wiki. A concrete reference architecture for the always-on, multi-surface operator setup.
4. **Open-source + third-party** — unlike Anthropic-first primitives (subagents, workflows), Graphify is community tooling. Worth tracking whether Anthropic ships a first-party repo-graph/index feature that obsoletes it (the same "first-party absorbs the wrapper" pattern that hit [[openclaw]]).

## Why it matters for 3Ps

- **A billable token-optimization deliverable** — "install Graphify so your Claude Code stops re-reading the repo every session" is a concrete, measurable cost win for any client with a large codebase. Sits alongside [[prompt-caching]] habits and [[claude-subagents]] cost levers in a "cut your Claude bill" service line.
- **Reference architecture for multi-surface clients** — the Graphify + Hermes + dashboard stack is a publishable "one shared brain across your devices" pattern for clients who want mobile + desktop + terminal continuity.

## Open questions

- **Graph freshness** — how does the graph stay in sync as the repo changes? On-commit rebuild, watch mode, manual re-index? (Stale graphs are the classic compiled-knowledge failure mode [[retrieval-contract]] flags.)
- **MCP vs CLI delivery** — does Graphify expose itself to Claude Code as an MCP server or a CLI? (The [[printing-press]] "CLI eats fewer tokens than MCP" argument would favor CLI.)
- **Scale limits** — how large a repo / monorepo before the graph itself gets expensive to build or query?
- **Hermes coupling** — is the "agentic OS" a Graphify product, a Hermes integration, or Jack's own assembled stack? (Origin unclear from the digest — same ambiguity [[hermes-agent]] carries.)
- **AntiGravity's role** — how does Google's AntiGravity connect into the dashboard? First named here; no prior vault coverage.

## Related pages

- [[retrieval-contract]] — the analyst-side framework Graphify instantiates at codebase scale (stop paying for rediscovery every run)
- [[claude-code]] — the agent that queries the graph; "Claude's biggest problem" Graphify targets
- [[hermes-agent]] — the always-on agent the agentic OS is built around; Graphify as its context brain
- [[code-comprehensibility]] — the read-side sibling (Mythos reads code for security; Graphify reads code for navigation)
- [[ai-operating-system]] — "one source of truth" / "one shared brain" thesis, here cross-device
- [[prompt-caching]], [[claude-subagents]], [[dynamic-workflows]] — the token-economics cluster Graphify joins
- [[printing-press]] — CLI-vs-MCP token argument relevant to Graphify's delivery
- [[jack-roberts]] — primary creator
- [[youtube-digest-apify-2026-06-09]] — primary citation

## Used in

- [[youtube-digest-apify-2026-06-09]] — primary citation ([[jack-roberts]] #5)
- [[jack-roberts]] — primary creator
- [[hermes-agent]] — agentic-OS context layer
