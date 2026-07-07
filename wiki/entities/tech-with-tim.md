---
title: Tech With Tim
category: entity
summary: Developer-education YouTuber (large Python/coding-tutorial channel) + `techwithtim.net` newsletter operator; enters the vault via *The Only Claude Code Plugins You Actually Need* (5.2K views on this video, 2026-07-06, 21:54) — the first creator in this vault to make an **explicit tool-count-as-a-cost** argument for [[claude-code|Claude Code]] [[plugins|plugins]]/[[mcp|MCP]] servers → new concept [[tool-overload]] (*"once Claude can see more than ~50 tools it starts picking the wrong ones and your agent gets worse, not better"*); ships a **curated-not-maximal** slate (TigerData, GitHub, Context7, Figma, Frontend Design) — the inverse of the "install as many as possible" curation tier
tags: [creator, youtube, developer-education, coding-tutorials, claude-code, plugins, mcp, tool-overload, plugin-curation, fifty-tool-ceiling, tigerdata, github-mcp, context7, figma, frontend-design, newsletter, techwithtim, monetization, openclaw, wispr-flow]
sources: 1
updated: 2026-07-07
---

# Tech With Tim

## What it is

Person + YouTube channel **Tech With Tim** — a long-running, large developer-education channel (Python, software engineering, coding tutorials) that has pivoted meaningful coverage into the AI-coding / [[claude-code|Claude Code]] space. Operates a free newsletter at `techwithtim.net/newsletter` (lead magnet: *How to Make Money With Coding*) with an explicit **careers / monetization / leverage** angle. Sponsorship + affiliate stack includes TigerData, Hostinger (VPS / OpenClaw setup), and Wispr Flow (AI dictation).

## Why it matters for this wiki

**He ships the first explicit "curate down, don't max out" plugin thesis in the vault.** Where the established curation tier ([[nate-herk]], [[brock-mesarich]], [[dubibubii]], [[zinho-automates]]) answers *"which skills/tools are best,"* Tim answers a sharper question: *"how many tools can Claude hold before selection degrades?"* — and puts a number on it (~50). That reframes [[plugins]]/[[mcp]] curation from a taste exercise into a **cost/ceiling** exercise → new concept [[tool-overload]].

He's also a **developer-audience** voice (vs the mainstream-operator tier), which makes his slate a useful cross-check: the tools that survive a working engineer's daily use, not a make-money-online content list.

## Key video in [[youtube-digest-apify-2026-07-07]]

- **#3** *The Only Claude Code Plugins You Actually Need* — 5.2K views (on this video), 2026-07-06, 21:54

**The framing claim**: *"Everyone tells you to install as many Claude Code plugins and MCP servers as possible. Here's the problem: once Claude can see more than about **50 tools** at once, it starts picking the wrong ones — and your agent actually gets **worse, not better**. In this video I went through the entire plugin marketplace and wider MCP ecosystem to find the plugins that genuinely earn their spot."*

**The curated slate** (from the description's video resources):

| Tool | What it does | Reference |
|---|---|---|
| **TigerData MCP** | Control databases from inside Claude (the sponsor) | `tsdb.co`; CLI-first quickstart |
| **GitHub MCP** | Repo/PR/issue access | `github/github-mcp-server` |
| **Context7** | Library/docs MCP (this vault uses it too) | `upstash/context7` |
| **Figma** | Design-file access | `claude.com/plugins/figma` |
| **Frontend Design** | Anthropic first-party front-end generation plugin | `anthropics/claude-code/plugins/frontend-design` |

**The selection-degradation mechanism** (→ [[tool-overload]]): more tools loaded ≠ more capable agent. Past a ceiling (~50 tools), the model's tool-selection accuracy drops because too many similar options crowd the decision. This is the empirical, tool-count-specific version of [[nate-b-jones]]' *"you're wasting 40% of your AI time"* wrong-layer argument ([[plugins]]) and dovetails with [[brad-bonanno]]'s MCP-token-cost / CLI-replacement thesis ([[mcp]], [[printing-press]]) — but the failure mode here is **selection quality**, not just token cost.

## Distribution / monetization

- **YouTube** — `Tech With Tim` (large developer-education channel; this specific video 5.2K views but the channel skews far larger)
- **Newsletter** — `techwithtim.net/newsletter`; lead magnet *How to Make Money With Coding*; explicit careers/monetization/leverage positioning
- **Affiliates / sponsors** — TigerData (`tsdb.co`), Hostinger (VPS + OpenClaw setup, code `techwithtim`), Wispr Flow (AI dictation)

## Related

- [[tool-overload]] — the concept his video introduces (the ~50-tool selection ceiling)
- [[plugins]] — the taxonomy his curation prunes
- [[mcp]] — half his slate is MCP servers; his ceiling argument is a cost lever on MCP sprawl
- [[claude-code]] — substrate
- [[printing-press]] — [[nate-herk]]'s CLI-over-MCP packaged product; token-cost sibling to Tim's selection-cost argument
- [[dubibubii]] — the maximalist-curation counterpoint (33 tools) Tim implicitly argues against
- [[nate-herk]], [[brock-mesarich]], [[zinho-automates]] — fellow curation-tier creators

## Appears in

- [[youtube-digest-apify-2026-07-07]] — primary source (#3)

## Open questions

- **Where exactly is the ~50-tool ceiling** — is it a hard model limit, a context-window artifact, or a soft "quality starts dropping" threshold? The video asserts it; the mechanism is worth verifying against Anthropic docs.
- **Does the ceiling move with the model** (Opus 4.8 vs Fable 5 vs Haiku)? Larger context ≠ better selection necessarily.
- **His full pruned list** — the 5 named here are from the description; the video likely covers a longer shortlist.
- Cross-platform reach + newsletter size as a competitive/audience benchmark.
