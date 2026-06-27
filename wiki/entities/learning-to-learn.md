---
title: LearningToLearn
category: entity
summary: Small YouTube channel (**LearningToLearn**) that ships a beginner-tier, multi-tool walkthrough of the [[karpathy-llm-wiki]] pattern — *How to Create a Karpathy LLM Wiki for your Notes* (332 views, 2026-06-08, 12:09). Two things make it distinctive in the vault's wiki-implementer matrix: (1) it builds the wiki with **Google Antigravity** (and notes Claude Code as an alternative) rather than Claude Code, and (2) it targets **Apple Notes** *and* Obsidian as destinations, plus a **zettelkasten** variant — the first **Apple Notes** wiki target and the first **Antigravity** substrate tracked here. Also demos **skills in Antigravity**. A tier-4 explainer datapoint confirming the pattern's mainstream-saturation and its spread across agent substrates and note apps
tags: [creator, youtube, karpathy-llm-wiki, google-antigravity, antigravity, obsidian, apple-notes, zettelkasten, skills, beginner-tier, tier-4, note-taking, llm-wiki-implementer]
sources: 1
updated: 2026-06-27
---

# LearningToLearn

## What it is

A small YouTube channel that publishes accessible, beginner-oriented explainers on AI + note-taking. Surfaced in this vault for its [[karpathy-llm-wiki]] walkthrough, *How to Create a Karpathy LLM Wiki for your Notes* (332 views, 2026-06-08, 12:09), found via [[youtube-digest-apify-2026-06-27]] #3.

## Why it matters for this wiki

It extends the [[karpathy-llm-wiki]] adoption matrix in two genuinely new directions:

1. **Google Antigravity as the build substrate.** Where almost every tracked implementer uses [[claude-code]] (or [[hermes-agent]] / [[codex]]), LearningToLearn demos the pattern in **Google Antigravity** — the first Antigravity instantiation of the wiki pattern in this vault. (This vault's own `CLAUDE.md` / `AGENTS.md` schema explicitly notes Antigravity as a parallel agent.) He names **Claude Code or Google Antigravity** as the two tool choices for the build.

2. **Apple Notes as a wiki destination.** The first tracked implementation targeting **Apple Notes** (chapter 07:21, *Modifying queries for Apple Notes*) alongside **Obsidian** (the canonical frontend) — broadening the pattern past the Obsidian-markdown default to a mainstream consumer notes app.

It also adds a **zettelkasten** variant (chapter 09:23, *Modifying queries to make notes more like a zettelkasten*) and demos **skills in Antigravity** (chapter 10:08) — the cross-substrate confirmation that skills aren't Claude-Code-only.

## The video (chapter map)

| Time | Chapter |
|---|---|
| 00:00 | Intro |
| 00:06 | Who is Karpathy? |
| 00:23 | What an LLM Wiki is |
| 01:14 | Basic LLM setup |
| 02:14 | Callout: LLM Wikis for AI vs note-taking |
| 02:47 | Working example — generate markdown files using Google Antigravity |
| 07:21 | Modifying queries for Apple Notes |
| 09:23 | Modifying queries to make notes more like a zettelkasten |
| 10:08 | Example of skills in Antigravity |
| 10:47 | Final thoughts |

**The "AI vs note-taking" callout** (02:14) is the notable nuance: he distinguishes building an LLM Wiki *for an AI to read* from building one *as a human note-taking system* — the same write-time-knowledge fork the vault tracks, framed for a note-taking audience.

## Adoption-tier placement

A **tier-4 (tiny, sub-1K-view)** explainer — same funnel position as [[ai-academy]]'s 687-view explainer. Its value is not novelty of the core pattern (mainstream-saturated) but the **substrate + destination spread**: Antigravity build + Apple Notes/Obsidian/zettelkasten targets confirm the pattern is diffusing across both agent tools and consumer note apps.

## Open questions

- **Channel scale / focus** — broader subscriber count and whether note-taking + learning is the consistent beat.
- **Antigravity skill format** — does it match the Claude Code / Codex skill format the vault tracks, or diverge? (Worth diffing for the cross-substrate skill-portability question in [[open-skills]].)
- **Apple Notes mechanics** — how does Antigravity write into Apple Notes (AppleScript? an MCP? export)? The write path matters for porting.

## Related
- [[karpathy-llm-wiki]] — the pattern he implements (Antigravity build + Apple Notes target + zettelkasten variant)
- [[claude-code]] — the alternative build substrate he names alongside Antigravity
- [[open-skills]] — cross-substrate skill portability (his Antigravity skills demo is a datapoint)
- [[ai-academy]] — the other tier-4 wiki explainer
- [[andrej-karpathy]] — pattern originator
- [[youtube-digest-apify-2026-06-27]] — citation
