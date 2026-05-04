---
title: YouTube Digest (Apify, batch 3) — AI creators + Claude topics — 2026-05-03
category: source
summary: Third 2026-05-03 farm batch — 5 new videos covering Tommy Chryst's Karpathy LLM Wiki walkthrough, Brad Bonanno's OpenClaw-killer Claude Code features, Nick Saraev's 2026 AI consulting blueprint, and Jeanne DeWitt Grosser on world-class GTM
tags: [youtube, digest, claude-code, karpathy-llm-wiki, ai-consulting, gtm, claude-design]
sources: 1
source_path: raw/youtube/digest-2026-05-03.md
source_date: 2026-05
authors: [farmer-ai-creators-youtube, apify-yt-scraper]
ingested: 2026-05-03
updated: 2026-05-03
---

# YouTube Digest (Apify, batch 3) — 2026-05-03

Third farm run for [[ai-creators-youtube]] on 2026-05-03 (after [[youtube-digest-2026-05-03]] yt-search and [[youtube-digest-apify-2026-05-03]] 28-video Apify). Dedup state advanced; this batch fetched 32 videos and surfaced **5 new** ones.

## TL;DR
A small but high-signal batch. Three threads worth tracking:
1. **Karpathy LLM Wiki has crossed into the "small-channel beginner walkthrough" tier** — Tommy Chryst (sub-15K-view channel) shipping a 13-minute setup guide. Confirms the [[karpathy-llm-wiki]] pattern is no longer just 200K-creator territory.
2. **Anthropic shipped three Claude Code features that obsolete OpenClaw** ([[brad-bonanno]] #4) — **Channels** (Telegram-native bot), **Scheduled Tasks** (cron via `/loop`), and **Auto Memory**. Replaces sketchy open-source wrappers with first-party primitives. This vault already uses two of them (`/loop`, `/telegram`).
3. **GTM as the decisive layer in the AI era** — Lenny's podcast with Jeanne DeWitt Grosser (Vercel COO, ex-Stripe, ex-Google) is the canonical "what world-class GTM looks like in 2026" reference. Introduces the **GTM engineer** role, frames build-vs-buy in the AI era, and argues most customers buy to **avoid pain**, not gain upside.

## Videos

| # | Title | Channel | Views | Date | URL |
|---|---|---|---|---|---|
| 1 | How To Do PHD-Level Research with AI (Karpathy's LLM Wiki) | [[tommy-chryst]] | 14.6K | 2026-04-05 | [link](https://www.youtube.com/watch?v=FR9USL0yj3I) |
| 2 | Claude Design + Claude Skills: Automate Your Marketing | [[grace-leung]] | 29.0K | 2026-04-25 | [link](https://www.youtube.com/watch?v=Ph-maUAiSU8) |
| 3 | How I Would Start AI Consulting in 2026 (If I could start over) | [[nick-saraev]] | 49.4K | 2025-10-01 | [link](https://www.youtube.com/watch?v=bMmlCPLDk1c) |
| 4 | These 3 Claude Code Features Just Killed OpenClaw (Setup Guide) | [[brad-bonanno]] | 1.4K | 2026-03-25 | [link](https://www.youtube.com/watch?v=iG5D0RUZX2s) |
| 5 | What world-class GTM looks like in 2026 \| Jeanne DeWitt Grosser | [[lenny-rachitsky]] | 80.7K | 2025-11-30 | [link](https://www.youtube.com/watch?v=RmnWHz8HD74) |

## Per-video synthesis

### 1. Tommy Chryst — *How To Do PHD-Level Research with AI* (LLM Wiki)
- 14.6K-view channel; 12:53 video; positioning is "AI for research / ChatGPT deep research alternative"
- Three-act structure: (0:00) what + why, (4:52) setup walkthrough, (8:49) using + maintaining
- Pitched explicitly as **fix for LLM limits in complex analysis** — frames LLM Wiki as the answer to context-rotation and shallow-RAG problems
- Operator stack: arose.ai voice automation + AA Academy (Skool community)
- Signal: small-channel implementations of [[karpathy-llm-wiki]] are now happening; pattern is past tip-of-the-funnel adoption

### 2. Grace Leung — *Claude Design + Claude Skills: Automate Your Marketing*
- **Already covered in [[youtube-digest-2026-05-03]]**; this batch re-surfaces it. New synthesis from the timestamps:
- **Skills stack** explicitly named: Brand Voice → Brand Design System → Campaign Planning → Carousel Design → Animated Motion. Plus a **Campaign Manager Agent** that orchestrates between them.
- The opening section "Design Your Claude Skills Stack" (00:21) is a reusable framework — not just a tutorial pattern, but an **architectural template** for vertical skill libraries
- "Extracting Your Design System with Claude Design" (02:36) is the canonical [[claude-design]] → [[claude-skills]] handoff: Design generates the system, Skills replay it across asset types
- HubSpot sponsorship continues — confirms her audience overlap with HubSpot's marketer persona
- Resource link: `claude.ai/design`

### 3. Nick Saraev — *How I Would Start AI Consulting in 2026 (If I could start over)*
- **Different video** from Saraev #7 (*Four Key AI Consulting Basics*) already in the wiki. This one is the **complete blueprint** version — 29:43, 49.4K views, 2025-10-01
- Five-pillar customer-journey framework: **marketing → sales → onboarding → fulfillment → retention**
- Claims pattern that has scaled agencies to **$25K/month and beyond**
- Bundled toolkit: Upwork profiles, cold email formulas, sales call scripts, automation templates, "full workflow library"
- Operator stack: **Instantly + Anymailfinder + Apify (30NICKSARAEV code) + n8n** — affiliate kickbacks disclosed
- Pitches **Maker School ("get customer #1 guaranteed")** as the community on-ramp
- Cross-references his 4 free multi-hour courses: Claude Code (4hr), Antigravity Vibe Coding (6hr), Agentic Workflows (6hr), N8N (6hr / 890K+ views)
- Signal: this is the **operator playbook** counterpart to his earlier framework-first video. Together they bracket "how to think" + "how to execute" for AI consulting

### 4. Brad Bonanno — *These 3 Claude Code Features Just Killed OpenClaw*
- 1.4K-view video (early/small) but **architecturally important** — names three first-party Anthropic features that obsolete OpenClaude (the open-source Telegram-Claude bridge):
  1. **Claude Code Channels** — first-party Telegram bot, no exposed ports / leaked API keys / sketchy OSS code
  2. **Scheduled Tasks** — cron jobs via the `/loop` command (this vault uses it for farm scheduling)
  3. **Auto Memory** — persistent context across sessions (this vault uses it via `~/.claude/projects/.../memory/` per CLAUDE.md)
- His full setup: Telegram message → Claude reads files → runs SEO workflow → sends report attachments back → schedules follow-up cron jobs. **No VPS, no Docker, no third-party wrappers.**
- Includes a **Claude.md tuned for Telegram**: shorter mobile-friendly responses, progress updates so user is "never left on read", auto memory checks before every task, guardrails around `--dangerously-skip-permissions`
- Free download: `brad-b.kit.com/be466ba5df`
- Signal: the **substrate this vault runs on** is now first-party. The /telegram skill in this vault, the /loop skill, and the auto-memory CLAUDE.md instruction are all codifications of the same shift.

### 5. Lenny Rachitsky × Jeanne DeWitt Grosser — *What world-class GTM looks like in 2026*
- 1:26:02 podcast; 80.7K views
- Guest: [[jeanne-dewitt-grosser]] — Vercel COO; built GTM at Stripe (early sales org from scratch), Google, Vercel; GTM advisor to founders
- Six explicit topics:
  1. Why GTM is becoming **more** strategically important in the AI era (not less)
  2. **The rise of the GTM engineer** — the new role that fuses sales/marketing ops with engineering
  3. A primer on **segmentation**
  4. How to build a sales org that engineers and product teams **respect**
  5. **Build vs buy** for GTM tools in the AI era
  6. **Pain > upside** — most customers buy to avoid pain rather than gain upside
- Sponsors: Datadog (Eppo experimentation), Lovable (chat-to-app), Stripe
- Lenny references his paid newsletter with "biggest takeaways"; transcript link at lennysnewsletter.com
- Signal: this is the canonical **2026 GTM frame** worth quoting in any 3Ps GTM playbook content

## Themes (this batch)

- **[[karpathy-llm-wiki]]** — 1 video, but signals tier-3 mainstream creator adoption
- **[[claude-code]]** — substrate of every video except #5; new sub-features: Channels, Scheduled Tasks, Auto Memory
- **[[claude-design]]** + **[[claude-skills]]** — Grace Leung's stack (re-surfaced)
- **[[ai-consulting]]** — Nick Saraev full blueprint (5 pillars: marketing/sales/onboarding/fulfillment/retention)
- **[[gtm-2026]]** — new concept page from Jeanne DeWitt Grosser interview
- **Telegram + scheduled work + auto-memory** — convergence around mobile-first, persistent, autonomous Claude Code

## Connections

- Extends: [[claude-code]], [[claude-skills]], [[claude-design]], [[ai-consulting]], [[karpathy-llm-wiki]]
- Establishes: [[tommy-chryst]], [[jeanne-dewitt-grosser]], [[lenny-rachitsky]], [[gtm-2026]]
- Updates: [[grace-leung]], [[nick-saraev]], [[brad-bonanno]]
- Builds on prior 2026-05-03 digests: [[youtube-digest-2026-05-03]], [[youtube-digest-apify-2026-05-03]]

## Why this matters for 3Ps

1. **The Lenny × Jeanne podcast is the highest-leverage GTM source surfaced so far.** Quotable, recent, top-of-funnel for the marketer-buyer persona. Should anchor any 3Ps GTM-playbook content.
2. **Brad's "OpenClaw is dead" framing validates the vault's architecture.** The /telegram, /loop, and auto-memory primitives are now first-party — content riffing on "why first-party beats wrapper" is a natural angle.
3. **Nick Saraev's 5-pillar blueprint maps cleanly to a 3Ps services menu.** Marketing / sales / onboarding / fulfillment / retention is exactly the org-design framework a 3Ps engagement would deliver against.
4. **Tommy Chryst is a watch-list creator** — same vertical (LLM Wiki), much smaller channel; useful as a "what does this look like at sub-15K subs" reference for content style and audience reaction.

## Notes
- Fetched via Apify `streamers/youtube-scraper` actor
- Dedup state: 27 videos already seen, 5 new
- Original digest at `raw/youtube/digest-2026-05-03.md` (overwritten by this batch — prior batches' source files preserve their content)
- For deeper ingest of any single video, drop transcript at `raw/youtube/<channel>/<slug>.md` and re-run `/wiki-ingest`
