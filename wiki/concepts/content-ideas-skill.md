---
title: Content Ideas Skill (/content-ideas)
category: concept
summary: [[brad-bonanno]]'s free Claude skill (`/content-ideas`, GitHub `bradautomates/cont...`) credited with growing his channel 0→10K subs in 3 months including three 90K+ view videos — surfaced 2026-06-03 (*I Hit 10k Subs in 3 Months with Claude Code*, 8:20). Builds a custom **"For You page"** across YouTube/Instagram/X/TikTok, pulling only the highest-performing posts from tracked creators scored by an **outlier rating** (how far a post beat that creator's *own* average, normalizing for creator size); **reads the comments** on every analyzed post to mine angles the post itself didn't cover (*"the real edge"*); **scrapes your own channel** before every run for **anti-cannibalization** (knows what you've made + what your audience asks); uses **Claude auto-memory** so every thumbs-up/down trains it to your taste (self-improving via *encoded preference*, the subjective-taste cousin of [[self-improving-skills]]' binary-criteria loop). Cross-vendor (Claude Code / Chat / Cursor / Codex). A **content-ideation farmer** — same supply-chain shape as [[context-farming]] but the destination is a ranked idea list, not a wiki. Data source: **Scrape Creators** (`scrapecreators.com`)
tags: [content-ideas-skill, brad-bonanno, claude-skills, context-farming, self-improving-skills, auto-memory, encoded-preference, outlier-rating, anti-cannibalization, for-you-page, scrape-creators, cross-vendor, creator-growth, comment-mining, lead-magnet]
sources: 1
updated: 2026-06-03
---

# Content Ideas Skill (`/content-ideas`)

## What it is

A **free Claude skill** by [[brad-bonanno]] that generates personalized content ideas for a creator's channel. Brad credits it with growing **Brad | AI & Automation from 0 → 10,000 subscribers in 3 months**, including **three videos that each cleared 90K views**. He open-sourced it as the giveaway in the 2026-06-03 video *I Hit 10k Subs in 3 Months with Claude Code (steal this)* (174 views just-published, 8:20).

Install: free GitHub repo `github.com/bradautomates/cont...` (URL truncated in source). Runs in [[claude-code]], **Claude Chat, Cursor, and Codex** — cross-vendor by design.

## How it works — four mechanics

1. **Custom "For You page" across four platforms** — pulls posts from YouTube, Instagram, X, and TikTok, but only the **highest-performing** posts from the creators you choose to track.
2. **Outlier rating** — every candidate post is scored by *how far it beat that creator's own average*, not by absolute views. This **normalizes for creator size** — a 50K-view post from a small creator can outrank a 500K-view post from a mega-channel. The outlier score is the ranking signal.
3. **Comment mining** *(chapter 2:19 "How it finds angles")* — the skill **reads the comments** on every post it analyzes, "because that's where the angles the video itself didn't cover live." This is framed as the **real edge**: the winning idea is often in the audience reaction, not the post.
4. **Anti-cannibalization** *(chapter 3:13)* — it **scrapes your own channel before every run**, so it knows what you've already made and what your own audience is actively asking for. Ideas it surfaces don't repeat your back-catalog.

Plus a **taste layer**: it uses **Claude's auto-memory** so every 👍/👎 you leave trains it — "so the ideas it surfaces start to sound like you, not like an AI trend report."

Data source: **Scrape Creators** (`scrapecreators.com`) — the cross-platform scraping API behind the For You page.

Chapter map: 0:00 Results → 1:00 Demo running `/content-ideas` live → 2:19 How it finds angles → 3:13 Anti-cannibalization.

## Where it sits in the vault

### A content-ideation farmer
The skill is a **[[context-farming]] variant**. The supply-chain shape is identical — scheduled-or-on-demand pulls of fresh external context (creator posts + their comments + your own channel) compiled into a local artifact. The difference is the **destination**: context farming feeds a [[karpathy-llm-wiki]] vault; `/content-ideas` feeds a **ranked idea list**. Both depend on a scraping connector ([[mcp]]/CLI/Scrape Creators) and both dedup against prior state (here, your own back-catalog).

### A self-improving skill — via preference, not binary criteria
`/content-ideas` self-improves through **auto-memory + thumbs up/down**, which is **encoded preference** — the *subjective-taste* cousin of [[self-improving-skills]]' **binary-criteria overnight loop**. Two distinct self-improvement mechanisms:

| | [[self-improving-skills]] (Simon Scrapes) | `/content-ideas` (Brad Bonanno) |
|---|---|---|
| Signal | Binary criteria (pass/fail, objective) | 👍/👎 in auto-memory (subjective taste) |
| Loop | Autonomous overnight convergence | Per-run, human-in-the-loop ratings |
| Optimizes for | Contract satisfaction | The user's personal taste |
| "What good looks like" | Specified up front as code | Learned incrementally from feedback |

Together they map the two halves of skill self-improvement: **objective convergence** (binary) and **preference tuning** (auto-memory).

### Cross-vendor portability
Running in Claude Code / Chat / Cursor / Codex restates [[brad-bonanno]]'s execution-layer thesis that *the IP is portable* — the skill is the asset, the substrate is swappable. Same shape as the [[codex]] / [[free-sample-phase]] vendor-agnostic stance.

## Why it matters for 3Ps

- **Directly relevant to the user's own creator/content GTM** — this is a working, free, install-in-a-minute content-ideation engine from the creator whose patterns this vault already implements.
- **Lead-magnet template** — a free, high-utility skill that funnels to an AI Strategy Call (`cal.com/bradley-bonanno/ai-st...`) is the exact lead-magnet → call funnel shape the vault tracks across Brad's videos. The skill *is* the lead magnet.
- **Outlier rating is a reusable scoring primitive** — "beat the creator's own average" is a cleaner content-selection signal than absolute views, and worth porting into the vault's YouTube farmer (which currently dedups but does not score by outlier-vs-baseline).
- **Comment mining as the angle source** — a concrete technique: the differentiated idea lives in the audience reaction, not the post. Applicable to competitive-intel farming generally.

## Open questions

- Is the repo's scraping done via Scrape Creators API only, or also MCP/CLI? (Diff against the vault's Apify-based farmer.)
- How is the outlier rating computed — rolling average window? median? How many posts per creator does it baseline against?
- Does auto-memory taste-training transfer across substrates (Claude Code ↔ Chat ↔ Cursor ↔ Codex), or is the memory siloed per surface?
- Worth installing and diffing against the vault's `yt-search` / Apify farmer scoring logic.

## Related pages

- [[brad-bonanno]] — author; this is the creator-growth axis of his product trajectory
- [[context-farming]] — parent pattern; `/content-ideas` is a content-ideation farmer
- [[self-improving-skills]] — sister self-improvement mechanism (binary criteria vs auto-memory preference)
- [[claude-skills]] — packaging unit
- [[claude-code]] — primary substrate (also Chat / Cursor / Codex)
- [[codex]], [[free-sample-phase]] — cross-vendor portability
- [[karpathy-llm-wiki]] — the wiki-destination cousin of the idea-list destination
- [[youtube-digest-apify-2026-06-03]] — citation
