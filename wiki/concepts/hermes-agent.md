---
title: Hermes Agent
category: concept
summary: VPS-deployed personal AI assistant with five pillars (skills, cron, Telegram, GitHub backup, multi-agent scaling); positioned as a parallel substrate to [[claude-code]] and [[openclaw]] for always-on second-brain / personal-assistant use cases; in 2026-05 reaches mainstream-creator awareness via [[nate-herk]] (1hr full course, 21K views) and [[corey-ganim]] (LLM-Wiki-on-Hermes walkthrough); in 2026-06-08 [[jack-roberts]] uses Hermes as the **agentic-OS host** for a [[graphify]] knowledge-graph "brain" — one shared context substrate across Claude Code, laptop, and mobile
tags: [hermes-agent, personal-ai, vps, hostinger, telegram, claude-code, openclaw, codex, second-brain, parallel-substrate, graphify, agentic-os, knowledge-graph, cross-device, shared-brain, jack-roberts]
sources: 2
updated: 2026-06-09
---

# Hermes Agent

## Definition

**Hermes Agent** — a VPS-deployed personal AI assistant framework. Positioned as an alternative to [[claude-code]] (local-terminal session-based) and [[openclaw]] (chatbot-wrapper-turned-runtime) for use cases that need an always-on agent: scheduled work, mobile/Telegram surfaces, multi-agent orchestration.

Surfaced in this vault via [[youtube-digest-apify-2026-05-10]]:
- **#5** [[nate-herk]] — *Hermes Agent: Zero to Personal AI Assistant (1 Hour Course)* (21.4K views, 58 minutes)
- **#3** [[corey-ganim]] — *I Built the ULTIMATE AI Second Brain (Karpathy's LLM Wiki Setup Guide)* (3.3K views) — LLM-Wiki-on-Hermes implementation walkthrough

## The Five Pillars (per [[nate-herk]] #5 chapter at 7:30)

Specifics gated to transcript, but the chapter scope and surrounding material strongly suggest:

1. **Skills** — procedural-knowledge units (likely [[claude-skills]]-format-compatible or close)
2. **Cron / scheduling** — recurring agent runs (analog to [[claude-code]] Routines / `/loop`)
3. **Telegram integration** — first-party Telegram channel (analog to Anthropic Channels per [[brad-bonanno]] #4)
4. **GitHub backup** — agent state persisted to git (analog to this vault's git-tracked state)
5. **Multi-agent scaling** — multiple Hermes instances on one VPS without breaking each other

The five pillars map cleanly onto the same primitives [[claude-code]] exposes locally — the difference is **deployment topology**, not capability.

## Architecture

- **VPS-deployed** (Hostinger one-click is the canonical host per both videos)
- **OpenAI Codex backend** (per [[corey-ganim]] #3) — Hermes uses OpenAI's coding agent as the underlying LLM workhorse, not Anthropic Claude
- **Telegram channel** for user surface — phone-first interaction pattern
- **GitHub** for state backup
- **Cron** for scheduled runs

This is a **substantively different stack** from this vault:
- This vault: Claude Code + Obsidian + local filesystem + Apple ecosystem
- Hermes: Codex + Hostinger VPS + Telegram + GitHub

Same architectural pattern (skills, cron, channel, backup); different substrate.

## Hermes vs [[claude-code]] vs [[openclaw]]

| Dimension | [[claude-code]] | [[openclaw]] | Hermes Agent |
|---|---|---|---|
| Where it runs | Local terminal | Local + cloud bridge | **VPS-hosted always-on** |
| Primary surface | Terminal / IDE | Telegram + terminal | **Telegram (mobile-first)** |
| Backend model | Anthropic Claude | Multi-vendor (now per [[nate-b-jones]] #8) | OpenAI Codex |
| Scheduling | Routines / `/loop` | Wraps Claude Code's | Built-in cron |
| Memory | Auto Memory at `~/.claude/` | OpenBrain (query-time) | (TBD — likely file-based; transcript needed) |
| Session model | Active session | Persistent wrapper | Always-on agent |
| Best for | Active dev work | Cross-vendor work routing | Ambient / scheduled / mobile |

**Convergent thesis**: these are not strictly competitors. They occupy different points on the *(deployment, surface, backend, session model)* matrix. A serious AI operator may use all three for different use cases.

## ⚠️ Contradiction with this vault

[[corey-ganim]] #3 explicitly claims "Hermes beats Claude Code, OpenClaw, and Obsidian for a second brain." This vault is built on Claude Code + Obsidian and runs the [[karpathy-llm-wiki]] pattern with no apparent friction.

Resolution probably hinges on **session model**:
- **Hermes always-on** is better when the user wants the agent to *come to them* (Telegram pings, scheduled summaries, mobile-first interaction)
- **Claude Code session-based** is better when the user is *actively driving* (active development, terminal work, deep flow)

For *second-brain ingest* specifically (the use case Corey claims Hermes wins on), the verdict is probably "Hermes wins for ingest-from-mobile workflows; Claude Code wins for ingest-during-active-work workflows." The two may be complementary rather than competitive.

Open: ingest a transcript of [[corey-ganim]] #3 to extract his specific comparison criteria.

## Adoption-tier signal

Two creators shipping Hermes content in the same week (one tier-1 at 708K subs, one tier-3/4 at 3K-views) is the **mainstream-creator-awareness threshold** — the same shape [[claude-skills]] crossed in [[youtube-digest-apify-2026-05-03]]. Expect more Hermes coverage across the next 2-4 weeks if the pattern holds.

## Hostinger as canonical host

Both videos route through **Hostinger affiliate codes** (NATEHERK, COREY10). Hostinger is positioning itself as the canonical VPS for AI-agent deployments — a clear creator-affiliate program targeting the [[hermes-agent]] / always-on-AI category. Worth tracking as the **infrastructure-side play** parallel to Anthropic's substrate-side play.

## As an agentic-OS host for [[graphify]] ([[jack-roberts]] in [[youtube-digest-apify-2026-06-09]])

[[jack-roberts]]' *Claude Code + Graphify = Insane Agentic OS* (23.4K views, 2026-06-08) uses Hermes as the **always-on host for a cross-device "agentic operating system."** The new ingredient is a [[graphify]] knowledge graph of a repo (so [[claude-code]] reads a *map* instead of re-skimming the whole repo every session — cheaper, fewer tokens); Hermes + a custom dashboard then serve that graph as **one shared brain across Claude Code, laptop, and mobile**, with the ability to **import any GitHub repo** into the graph.

This sharpens Hermes's role in the vault: not just an always-on assistant, but the **multi-surface serving layer for a shared context substrate**. Where the Five Pillars described Hermes's *capabilities*, this shows Hermes as the *distribution topology* for a context brain — the cross-device realization of [[ai-operating-system]]'s "one source of truth," here a repo graph rather than a wiki. Also the first vault mention of **AntiGravity** (`antigravity.google/`), connected into the same dashboard.

→ See [[graphify]] for the knowledge-graph layer. Open: whether the "agentic OS" is a Graphify product, a Hermes integration, or Jack's own assembled stack (origin unclear — same ambiguity Hermes itself carries).

## Why it matters for 3Ps

1. **Track-but-don't-adopt by default** — for any 3Ps client doing local development with Claude Code, Hermes is interesting but not a forced migration. For clients wanting *team-shared always-on agents*, Hermes may be the right substrate.
2. **Substrate-comparison content** — "Claude Code vs Hermes vs OpenClaw: when to use each" is publishable 3Ps content; the substrate-choice question is now real, not hypothetical.
3. **Hostinger affiliate** — the creator-affiliate path is reproducible; if 3Ps content includes any infrastructure recommendations, joining the Hostinger affiliate program is a low-effort revenue line.
4. **Cross-vendor backend** — Hermes' use of Codex (OpenAI) confirms that the architectural primitives this vault tracks are vendor-portable. 3Ps positioning can credibly cover OpenAI-backend stacks via Hermes.

## Open questions

- **Origin** — is Hermes Anthropic-affiliated, OpenClaw-fork, OpenAI-Codex-bundled, or independent? Both videos refer to it as a product but origin isn't named.
- **Pricing / open-source** — paid product, OSS, or affiliate-distributed via Hostinger?
- **MCP support** — does Hermes consume MCP servers natively?
- **Skills format compatibility** — are Hermes Skills file-format-compatible with [[claude-skills]] and [[codex]] Skills, or yet another spec?
- **Memory architecture** — write-time-compiled (Karpathy/wiki side) or query-time (OpenBrain side)? See [[karpathy-wiki-vs-openbrain]] for the fork.
- **Multi-agent specifics** — does the Hermes "scaling multiple agents" pillar mean isolated agents or coordinating-agent orchestration?
- **OpenClaw relationship** — is Hermes a fork, a sibling, or a competitor? (The framing in #5 suggests sibling; verify.)

## Related pages

- [[claude-code]] — sibling substrate (local, session-based)
- [[openclaw]] — sibling substrate (cross-vendor runtime, per [[nate-b-jones]] #8)
- [[codex]] — Hermes's reported backend
- [[karpathy-llm-wiki]] — pattern Corey implements on Hermes
- [[anthropic]] — substrate for [[claude-code]] (Hermes's competitor)
- [[claude-skills]] — pattern Hermes Skills likely adapt
- [[nate-herk]] — primary creator (1hr course)
- [[corey-ganim]] — secondary creator (LLM-Wiki implementation)
- [[jack-roberts]] — Graphify-on-Hermes agentic-OS build (2026-06-08)
- [[graphify]] — knowledge-graph context brain served via Hermes
- [[claude-code]] — the agent querying the Graphify graph
- [[youtube-digest-apify-2026-05-10]] — primary citation
- [[youtube-digest-apify-2026-06-09]] — Graphify agentic-OS citation
