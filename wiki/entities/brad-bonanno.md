---
title: Brad Bonanno
category: entity
summary: AI & Automation YouTuber; coined/popularized "context farming" pattern that this vault uses; Skills marketplace builder; canonical "OpenClaw is dead, first-party Claude Code wins" voice on Telegram + Scheduled Tasks + Auto Memory; in 2026-05 ships the canonical 13-product "Learn Claude From Scratch" tour — the most comprehensive Anthropic product-surface inventory tracked here
tags: [creator, youtube, claude-code, context-farming, second-brain, skills-marketplace, telegram, scheduled-tasks, auto-memory, claude-product-tour]
sources: 3
updated: 2026-05-10
---

# Brad Bonanno

## What it is
Person + YouTube channel **Brad | AI & Automation**. Builder of the "AI Second Brain" / "Company Brain" / "context farming" pattern that this vault directly implements via the [[context-farming]] skill (`farmer/` configs in this repo).

## Why it matters for this wiki
**The user's vault uses Brad's pattern.** The `farmer` skill, the per-source farmer markdown configs, the auto-ingest into raw/ → wiki are direct instantiations of his Slack/Fireflies-fed Obsidian second brain. Tracking him = tracking the upstream evolution of the architecture this vault runs on.

## Key videos in [[youtube-digest-apify-2026-05-03]]

- #19 *I Stopped Hitting Claude Code Usage Limits (Here's How)* — 106K views, 2026-04-10. Releases free **Context Audit skill** that scans Claude Code setup, scores token bloat, recommends cuts. Canonical fix: replace MCP servers with CLIs, optimize CLAUDE.md, cut skill bloat, tune settings.json.
- #23 *I Turned My Second Brain Into a Company Brain (Now it reads Slack for me)* — 2.4K views (early), 2026-04-01. Shows full context-farming setup: Slack MCP + Fireflies + Obsidian + scheduled Claude Code routines. Includes a `/create-farmer` skill that builds and schedules new farmers automatically. **Free GitHub repo at `bradautomates/second...`** (truncated in source).

## Key video in [[youtube-digest-apify-2026-05-10]]

- #2 *How I'd Learn Claude From Scratch in 2026* — 3.5K views (early), 2026-05-07, 11:29. **Canonical 13-product tour** of Anthropic's surface area — the most comprehensive product inventory in this vault. Walks every product end-to-end:
  1. Claude Chat + artifacts
  2. Connectors + MCP (Gmail, Drive, Notion, Calendar, Slack)
  3. Projects (work organization)
  4. Claude Desktop + Cowork + Live Artifacts (local file read/edit)
  5. **Skills** ("the one feature that makes everything else dramatically better")
  6. Dispatch (mobile-to-desktop handoff)
  7. Word add-in
  8. PowerPoint add-in
  9. Excel add-in
  10. Chrome (browser automation)
  11. Design ([[claude-design]])
  12. Code ([[claude-code]] — "the most powerful version of all of it")
  13. Routines (scheduled recurring work)
- **Thesis**: paying users use ~2% of what Claude exposes. Most never touch Skills, Connectors, Cowork, Routines.
- **Skills as the unlock** — same framing [[ben-ai]] uses; Brad confirms it from the operator side, [[ben-ai]] from the authoring side
- **Skills Marketplace waitlist** at `brad-b.kit.com/f9a7349a1c` — same waitlist Brad has been driving since the earlier #19/#23 videos; he's been at it for months
- Useful as the **canonical Anthropic product surface inventory** for this vault — supplements the [[anthropic]] entity page

## Key video in [[youtube-digest-2026-05-03-r3]]

- #4 *These 3 Claude Code Features Just Killed OpenClaw (Setup Guide)* — 1.4K views (early), 2026-03-25, 20:48. Architecturally important — names three first-party Anthropic features that obsolete the OpenClaude open-source Telegram-Claude bridge:
  1. **Claude Code Channels** — first-party Telegram bot, no exposed ports / leaked API keys / sketchy OSS code on the host machine
  2. **Scheduled Tasks** — cron jobs via the `/loop` command (this vault uses it for farm scheduling — see `farmers/`)
  3. **Auto Memory** — persistent context across sessions (this vault uses it via `~/.claude/projects/.../memory/`, baked into root CLAUDE.md)
- Full setup demoed end-to-end: Telegram message → Claude reads files → runs SEO workflow → sends report attachments back → schedules cron jobs. **No VPS, no Docker, no third-party wrappers.**
- **Telegram-tuned Claude.md** — shorter mobile-friendly responses, progress-update prompts so user is "never left on read", auto memory checks before every task, guardrails around `--dangerously-skip-permissions`. Free download: `brad-b.kit.com/be466ba5df`
- AI Strategy Call funnel: `cal.com/bradley-bonanno/ai-st...`

## Pattern artifacts to harvest

1. **Context Audit skill** (free download, video #19) — worth installing and running on this vault
2. **`/create-farmer` skill** (video #23) — directly comparable to the user's existing `farmer` skill
3. **Skills marketplace waitlist** — `brad-b.kit.com/f9a7349a1c` — he's building a verified-skills marketplace; competitive/complementary product to study
4. **Full second-brain repo** at `github.com/bradautomates/seco...` — likely worth cloning and diffing against this vault's `farmer/` skill
5. **Telegram-tuned Claude.md** (free, video #4) — `brad-b.kit.com/be466ba5df` — diff against the user's `/telegram` skill setup for ergonomics improvements

## Architecture co-evolution

Brad's three videos surfaced so far (#19, #23, #4) collectively describe the **architecture this vault runs on**:

| Brad video | Concept | Vault implementation |
|---|---|---|
| #19 (Context Audit) | Token-cost optimization | (TODO: install Context Audit skill) |
| #23 (Company Brain) | [[context-farming]] | `farmers/`, `/wiki-ingest`, scheduled routines |
| #4 (OpenClaw is dead) | Telegram + `/loop` + Auto Memory | `/telegram` skill, `/loop`, `~/.claude/projects/.../memory/` |

This makes him the **highest-priority creator-watch** for vault architecture evolution. New Brad videos likely → new vault primitives.

## Related
- [[context-farming]] — the canonical concept page
- [[karpathy-llm-wiki]] — the architecture his pattern implements
- [[claude-code]] — substrate
- [[claude-skills]] — packaging unit
- [[mcp]] — his pattern depends on MCP for Slack/Fireflies access

## Appears in
- [[youtube-digest-apify-2026-05-03]] — 2 high-signal videos (#19, #23)
- [[youtube-digest-2026-05-03-r3]] — video #4 (OpenClaw-killer features)
- [[youtube-digest-apify-2026-05-10]] — video #2 (Learn Claude From Scratch 13-product tour)
- [[context-farming]] — primary citation
- [[claude-code]] — primary citation for Channels / Scheduled Tasks / Auto Memory features
- [[anthropic]] — most comprehensive product-surface tour

## Why track him for 3Ps
- **Direct architectural influence** on this vault — anything he ships likely belongs here
- **Skills marketplace** is a strategic move worth watching; could become competitor or partner for any 3Ps skill product
- **His audience** = practitioners adopting context-farming patterns; same persona as 3Ps target customer

## Open questions
- What does his Skills marketplace actually offer? (Join waitlist for visibility)
- Is the `/create-farmer` skill open-source? Worth diffing against the user's existing implementation
- His business model — newsletter + AI strategy calls (`cal.com/bradley-bonanno/ai-st...`) — what's he selling?
- Cross-platform presence — X handle?
