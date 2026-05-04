---
title: Context Farming
category: concept
summary: Pattern of running scheduled agents that pull fresh context from external systems (Slack, meetings, YouTube, X) into a local knowledge base on autopilot
tags: [context-farming, second-brain, claude-code, mcp, automation, brad-bonanno]
sources: 1
updated: 2026-05-03
---

# Context Farming

## Definition
A pattern where scheduled Claude Code routines ("farmers") pull fresh context from external systems (Slack, Fireflies meetings, YouTube via Apify, X/Twitter via Apify, etc.) into a local knowledge vault — typically an Obsidian / [[karpathy-llm-wiki]] structure — without manual intervention. Each farmer is a small markdown config that defines: source, schedule, dedup state, ingest pattern.

**This vault uses context farming.** The `farmer/` skill + per-source farmer configs (`farmers/<name>.md`) implement this pattern directly.

## Origin
Term popularized by [[brad-bonanno]] in his April 2026 video *I Turned My Second Brain Into a Company Brain (Now it reads Slack for me)* ([[youtube-digest-apify-2026-05-03]] #23). His repo at `github.com/bradautomates/seco...` (full URL truncated in source) is the canonical reference implementation.

[[nate-b-jones]] #14 generalizes the principle: "memory is the heart of the system and most people get the pipeline side wrong" — context farming is the pipeline side.

## Key claims (from [[youtube-digest-apify-2026-05-03]])

- **Layered context from multiple sources** creates a unified knowledge base ([[brad-bonanno]] #23)
- **`/create-farmer` meta-skill** — a Claude Code skill that builds and schedules new farmers automatically; reduces farmer-creation overhead ([[brad-bonanno]] #23)
- **Cloud-scheduled routines** keep farmers running while you sleep — Claude Code Routines ([[claude-code]]) are the canonical scheduling primitive
- **Context bloat is the cost** — running too many farmers or wiring them poorly burns tokens; **Context Audit skill** ([[brad-bonanno]] #19) scans setup and recommends cuts
- **MCP > everything for connecting external systems** — Slack MCP, Fireflies MCP, etc. ([[brad-bonanno]] #23). But context bloat counter-pressure pushes toward CLI replacements where possible ([[brad-bonanno]] #19, [[mcp]])

## Implementations observed

| Implementation | Sources fed | Substrate |
|---|---|---|
| [[brad-bonanno]] (canonical) | Slack, Fireflies meetings | Obsidian + Claude Code skills |
| **This vault** | YouTube (Apify, yt-search) | Same; `farmer/` skill, per-source configs in `farmers/` |
| (Implied) [[nate-herk]] AIOS | Multi-source | Cadence + Cloud Routines (#3) |

## Adjacent patterns

- **[[karpathy-llm-wiki]]** — the *destination* for farmed context; wiki is structure, farming is supply chain
- **[[mcp]]** — the *connector layer* most farmers depend on
- **Claude Code Routines** — the *scheduler* most farmers run on
- **AIOS / Operating Systems** ([[nate-herk]] #3) — the *opinionated stack* that bundles farming + wiki + dashboards

## Contrasts with

- **Manual ingest** — user reads articles, drops into raw/, runs `/wiki-ingest` one at a time
- **RAG over external systems** — query-time retrieval from Slack/Notion/GDrive without compiling into a structured vault
- **Webhook ingestion** — push-driven from external systems (Slack webhook → ingest); context farming is pull-driven

## Open questions / disagreements

- ⚠️ **MCP vs CLI for farmers** — [[brad-bonanno]] #23 wires MCP servers; [[brad-bonanno]] #19 (his own later video) explicitly recommends replacing MCPs with CLIs to cut context bloat. The pattern is unstable; canonical answer depends on whether the farmer runs interactively or in a routine.
- **Dedup state placement** — per-farmer JSON file vs central database vs git history? Implementations vary.
- **Schedule cadence** — how often is "right"? Daily defaults are common; some sources (X trending) might warrant hourly; static sources (Karpathy gist) need only on-change triggers (which farming doesn't yet handle).
- **Trust/quality gates** — farmers ingest unfiltered; the wiki ingest step is the only quality gate. Should farmers themselves have selection logic? (The yt-search digest does some scoring; Apify-based farmers don't.)

## Why it matters for 3Ps

- **The user already runs this pattern** — every architectural improvement [[brad-bonanno]] ships is directly applicable
- **Productization angle**: a "Context Farming Starter Kit" / template repo is a credible content + lead-magnet asset
- **Competitive intel feeder**: each farmer is a competitive-intel pipeline; the YouTube farmer (this digest) is the first one running, X and competitive-ads-extractor are obvious next targets

## Used in
- [[youtube-digest-apify-2026-05-03]] — primary citation (Brad Bonanno videos)
- [[brad-bonanno]] — primary author
- [[karpathy-llm-wiki]] — feeds into this
- [[mcp]] — supplies connectors
- [[claude-code]] — substrate
- (Future) [[3ps-consulting]] — content + product angle
