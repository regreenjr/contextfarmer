---
title: Brad Bonanno
category: entity
summary: AI & Automation YouTuber; coined/popularized "context farming" pattern that this vault uses; Skills marketplace builder
tags: [creator, youtube, claude-code, context-farming, second-brain, skills-marketplace]
sources: 1
updated: 2026-05-03
---

# Brad Bonanno

## What it is
Person + YouTube channel **Brad | AI & Automation**. Builder of the "AI Second Brain" / "Company Brain" / "context farming" pattern that this vault directly implements via the [[context-farming]] skill (`farmer/` configs in this repo).

## Why it matters for this wiki
**The user's vault uses Brad's pattern.** The `farmer` skill, the per-source farmer markdown configs, the auto-ingest into raw/ → wiki are direct instantiations of his Slack/Fireflies-fed Obsidian second brain. Tracking him = tracking the upstream evolution of the architecture this vault runs on.

## Key videos in [[youtube-digest-apify-2026-05-03]]

- #19 *I Stopped Hitting Claude Code Usage Limits (Here's How)* — 106K views, 2026-04-10. Releases free **Context Audit skill** that scans Claude Code setup, scores token bloat, recommends cuts. Canonical fix: replace MCP servers with CLIs, optimize CLAUDE.md, cut skill bloat, tune settings.json.
- #23 *I Turned My Second Brain Into a Company Brain (Now it reads Slack for me)* — 2.4K views (early), 2026-04-01. Shows full context-farming setup: Slack MCP + Fireflies + Obsidian + scheduled Claude Code routines. Includes a `/create-farmer` skill that builds and schedules new farmers automatically. **Free GitHub repo at `bradautomates/second...`** (truncated in source).

## Pattern artifacts to harvest

1. **Context Audit skill** (free download, video #19) — worth installing and running on this vault
2. **`/create-farmer` skill** (video #23) — directly comparable to the user's existing `farmer` skill
3. **Skills marketplace waitlist** — `brad-b.kit.com/f9a7349a1c` — he's building a verified-skills marketplace; competitive/complementary product to study
4. **Full second-brain repo** at `github.com/bradautomates/seco...` — likely worth cloning and diffing against this vault's `farmer/` skill

## Related
- [[context-farming]] — the canonical concept page
- [[karpathy-llm-wiki]] — the architecture his pattern implements
- [[claude-code]] — substrate
- [[claude-skills]] — packaging unit
- [[mcp]] — his pattern depends on MCP for Slack/Fireflies access

## Appears in
- [[youtube-digest-apify-2026-05-03]] — 2 high-signal videos
- [[context-farming]] — primary citation

## Why track him for 3Ps
- **Direct architectural influence** on this vault — anything he ships likely belongs here
- **Skills marketplace** is a strategic move worth watching; could become competitor or partner for any 3Ps skill product
- **His audience** = practitioners adopting context-farming patterns; same persona as 3Ps target customer

## Open questions
- What does his Skills marketplace actually offer? (Join waitlist for visibility)
- Is the `/create-farmer` skill open-source? Worth diffing against the user's existing implementation
- His business model — newsletter + AI strategy calls (`cal.com/bradley-bonanno/ai-st...`) — what's he selling?
- Cross-platform presence — X handle?
