---
title: Corey Ganim
category: entity
summary: Small-channel AI YouTuber (3.3K views on Hermes video); first creator in this vault to ship a focused [[karpathy-llm-wiki]]-on-[[hermes-agent]] implementation walkthrough; sells via Hostinger affiliate (COREY10) and a free "Hermes Second Brain Setup Guide" lead magnet
tags: [creator, youtube, hermes-agent, karpathy-llm-wiki, second-brain, hostinger, vps, telegram, openai-codex]
sources: 1
updated: 2026-05-10
---

# Corey Ganim

## What it is

Person + YouTube creator. Surfaced in this vault via [[youtube-digest-apify-2026-05-10]] #3 (*I Built the ULTIMATE AI Second Brain (Karpathy's LLM Wiki Setup Guide)*, 3.3K views, 18:41). Tier-3 / small-channel implementer of the [[karpathy-llm-wiki]] pattern.

## Why it matters for this wiki

Corey is the **first creator tracked here** to ship a dedicated [[hermes-agent]] + [[karpathy-llm-wiki]] walkthrough. His framing positions Hermes as superior to [[claude-code]] + Obsidian for the second-brain use case — a direct challenge to this vault's architecture. Worth tracking even at small-channel scale because the *specific architectural comparison* (VPS-hosted always-on agent vs local terminal session) is novel content for this vault.

## Key claims (from [[youtube-digest-apify-2026-05-10]] #3)

- **Hermes beats Claude Code, OpenClaw, and Obsidian** for the second-brain use case (his framing — see ⚠️ below)
- **Three-layer architecture**: raw sources, the wiki, the schema — same as Karpathy's gist and this vault
- **Division of labor**: human curates sources, agent summarizes/files/queries (matches CLAUDE.md in this vault)
- **Three core operations**: ingest, query, lint — *exactly* the operations defined in this vault's CLAUDE.md
- **VPS deployment** on Hostinger one-click; agent connects to OpenAI Codex + Telegram
- **MarkDownload Chrome extension** for source ingest (matches the Teacher's Tech / Web Clipper pattern from earlier digests)

## Distribution / business model

- **YouTube** (primary surface)
- **Hostinger affiliate** — discount code `COREY10` on `hostinger.com/corey10`; affiliate revenue is the apparent monetization
- **Free lead magnet**: "Hermes Second Brain Setup Guide" at `corey-ganim.kit.com/60fc0fe6d9` (ConvertKit form — matches [[brad-bonanno]]'s lead-magnet pattern)
- **No course, no community, no paid product visible** — early-stage solo creator

## Architectural significance

Corey's video is the **first concrete framing** that the [[karpathy-llm-wiki]] pattern can live outside the Claude Code + Obsidian stack. The implementation choices (VPS + Telegram + OpenAI Codex backend) are orthogonal to this vault's choices (local + Obsidian + Claude Code). Both run the same three-operation pattern.

⚠️ **Contradiction with this vault**: Corey claims "Hermes beats Claude Code and Obsidian for a second brain"; this vault is built on Claude Code + Obsidian and runs the same pattern with no apparent friction. Resolution probably hinges on use case — Hermes is always-on (cron-driven, Telegram-surfaced); Claude Code is session-driven. The two may be complementary substrates, not competitors. Worth a transcript pull to extract Corey's specific comparison criteria.

## Why track him for 3Ps

- **First-tier implementation evangelist** for [[hermes-agent]] — if Hermes becomes a category, Corey is an early voice
- **Lead-magnet pattern** is reproducible — free setup guide → email list → upsell (he hasn't monetized yet, but the funnel is built)
- **Hostinger affiliate** signals a creator-economy revenue path that doesn't require a product — useful pattern study for low-overhead 3Ps content
- **Comparison framing** (Hermes vs Claude Code vs Obsidian) is content this vault can reuse and pressure-test

## Open questions

- Channel sub count? (Views suggest small channel; sub count not in digest)
- Has he shipped earlier videos, or is the Hermes video his entry point?
- Does he have a Skool/community or X presence?
- Cross-platform (X, LinkedIn) — newsletter, podcast?
- Does he have an opinion on [[claude-code]]-on-VPS vs [[hermes-agent]] for the same use case? Or did he fork from Claude Code to Hermes for a specific reason?
- Hostinger seems to sponsor multiple creators in this vault ([[nate-herk]] uses code NATEHERK; Corey uses COREY10). Is Hostinger running an affiliate-driven creator program for VPS-AI-agent positioning specifically?

## Related pages

- [[hermes-agent]] — primary concept he covers
- [[karpathy-llm-wiki]] — the pattern he implements
- [[claude-code]] — what he claims to beat
- [[youtube-digest-apify-2026-05-10]] — primary citation
- [[brad-bonanno]] — sibling small/early-creator with similar lead-magnet pattern
- [[nate-herk]] — bigger-channel creator covering [[hermes-agent]] in the same week
