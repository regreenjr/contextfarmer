---
title: YouTube Digest (Apify) — AI creators + Claude topics — 2026-06-03
category: source
summary: 2-video farm batch (32 fetched, 30 dedup-skipped — 93.75% dedup) — (1) [[brad-bonanno]] (174 views just-published, 8:20) gives away the free `/content-ideas` Claude skill credited with growing his channel **0→10K subs in 3 months including three 90K+ view videos** → new concept [[content-ideas-skill]] (a custom **"For You page"** across YouTube/IG/X/TikTok scored by an **outlier rating** = how far a post beat that creator's *own* average; **comment mining** for angles the post didn't cover = *"the real edge"*; **anti-cannibalization** by scraping your own channel each run; **Claude auto-memory** thumbs-up/down trains it to your taste; cross-vendor Claude Code/Chat/Cursor/Codex; data via **Scrape Creators**) — a **content-ideation farmer** and the **preference-tuned cousin** of [[self-improving-skills]]; (2) [[nate-herk]] (6.8K views, 17:22) ships *100 Years of Artificial Intelligence Explained* — an **AI-history explainer** (Turing/Enigma → Dartmouth naming → symbolic-vs-connectionist → two AI winters → the dead-end approach that won → AlphaGo "world champion walks away" → two missing pieces → "what just happened" → "who wins now"), a **content-format pivot** away from his Claude-tooling cadence into evergreen history-explainer territory. A **light, low-new-signal batch** — both repeat creators, one new skill + one format experiment, no new vendors
source_path: raw/youtube/digest-2026-06-03.md
source_date: 2026-06
authors: [Brad Bonanno, Nate Herk]
ingested: 2026-06-03
tags: [youtube, digest, apify, brad-bonanno, nate-herk, content-ideas-skill, for-you-page, outlier-rating, comment-mining, anti-cannibalization, auto-memory, scrape-creators, cross-vendor, context-farming, self-improving-skills, ai-history, explainer, content-format-pivot]
sources: 1
updated: 2026-06-03
---

# YouTube Digest (Apify) — 2026-06-03

## Source meta

- **Farmer**: `ai-creators-youtube`
- **Fetcher**: Apify `streamers/youtube-scraper`
- **Total fetched**: 32 videos
- **Dedup-skipped**: 30 (already seen)
- **New videos**: 2
- **Creators**: [[brad-bonanno]] (1), [[nate-herk]] (1)

## Videos

| # | Title | Channel | Views | Date | Duration |
|---|---|---|---|---|---|
| 1 | I Hit 10k Subs in 3 Months with Claude Code (steal this) | Brad \| AI & Automation | 174 | 2026-06-03 | 08:20 |
| 2 | 100 Years of Artificial Intelligence Explained | Nate Herk \| AI Automation | 6,825 | 2026-06-02 | 17:22 |

## Per-video highlights

### #1 Brad Bonanno — *I Hit 10k Subs in 3 Months with Claude Code (steal this)*

**174 views (just-published), 2026-06-03, 8:20. → New concept: [[content-ideas-skill]]. Updates: [[brad-bonanno]] (creator-growth axis), [[context-farming]] (content-ideation variant), [[self-improving-skills]] (preference-tuned cousin).**

Brad gives away the free `/content-ideas` Claude skill he credits with growing **Brad | AI & Automation from 0 → 10,000 subscribers in 3 months**, including **three videos that each cleared 90K views**. Install: free GitHub repo `github.com/bradautomates/cont...`. Runs in [[claude-code]], **Claude Chat, Cursor, and Codex**.

**Four mechanics**:

1. **Custom "For You page"** across YouTube / Instagram / X / TikTok — only the **highest-performing** posts from creators you track.
2. **Outlier rating** — scores each post by *how far it beat that creator's own average*, not absolute views (normalizes for creator size).
3. **Comment mining** (2:19 *How it finds angles*) — reads the comments on every analyzed post, "because that's where the angles the video itself didn't cover live." Framed as **the real edge**.
4. **Anti-cannibalization** (3:13) — scrapes **your own channel** before every run, so it knows what you've made and what your audience is asking for.

Plus a **taste layer**: **Claude auto-memory** + 👍/👎 trains it so "the ideas start to sound like you, not like an AI trend report."

**Data source**: Scrape Creators (`scrapecreators.com`). **Funnel**: AI Strategy Call (`cal.com/bradley-bonanno/ai-st...`). Chapters: 0:00 Results → 1:00 Demo → 2:19 How it finds angles → 3:13 Anti-cannibalization.

**Why it matters**: a **content-ideation farmer** — same supply-chain shape as [[context-farming]] but the destination is a ranked idea list, not a wiki. Self-improves via **encoded preference** (auto-memory thumbs), the *subjective-taste* cousin of [[self-improving-skills]]' *objective* binary-criteria loop. The skill *is* the lead magnet — directly relevant to the user's own creator/content GTM, and the **outlier rating** is a reusable content-selection primitive worth porting into the vault's YouTube farmer (which dedups but doesn't score by outlier-vs-baseline). → New concept: [[content-ideas-skill]].

### #2 Nate Herk — *100 Years of Artificial Intelligence Explained*

**6.8K views, 2026-06-02, 17:22. → Updates: [[nate-herk]] (content-format pivot).**

An **AI-history explainer** — a clear departure from [[nate-herk]]'s usual Claude-tooling / build-tutorial cadence into **evergreen history-explainer** content. Walks the field's full arc:

- **Bedroom side project / unbreakable code** (0:00–0:24) — Turing-era origins, "a code that took an entire war to crack" (Enigma)
- **Naming the field** (3:01) — the 1956 Dartmouth workshop
- **Logic or brain?** (3:44) — the symbolic-vs-connectionist split
- **Boom then bust** (6:48) — the **two AI winters** that "nearly killed the field"
- **Two missing pieces** (9:48) — "the approach everyone wrote off as a dead end" (neural nets / connectionism) + what it lacked (compute + data)
- **What just happened?** (12:55) — the modern deep-learning / transformer breakthrough; "the single move that made a world champion walk away" (AlphaGo / Lee Sedol)
- **Who wins now?** (13:51) — the present-day frontier-lab race

**Sponsor/affiliate stack**: Skool free AI OS course + paid community, podcast (`podcast.nateherk.com`), Uppit AI (`uppitai.com`), Glaido (voice-to-text, `get.glaido.com/nate`), Hostinger VPS (`NATEHERK`).

**Why it matters**: this is a **content-format pivot** — Nate's catalog in this vault has been Claude-tooling tutorials, framework videos, news interpretation, and one long-form interview. A 17-minute narrative AI-history explainer is a new format bet (evergreen/educational rather than news-cycle-pegged). It introduces **no new vault concept** on the GTM/Claude axis, but is a notable signal about his content diversification — testing evergreen explainer reach against his usual same-day-news cadence. At 6.8K views it underperformed his recent news/framework videos (which run 50K–105K), an early datapoint that his audience still rewards Claude-tooling content over general AI education.

## Cross-video signals

**A light, low-new-signal batch.** 93.75% dedup (30/32), both anchors repeat creators ([[brad-bonanno]] + [[nate-herk]]), no new vendors. The new signal is **one new skill** ([[content-ideas-skill]]) + **one content-format experiment** (Nate's history explainer).

**The two videos are opposite bets on creator growth.** Brad ships a **tool** for finding what to make next (`/content-ideas` — data-driven, outlier-scored, taste-tuned ideation). Nate ships an **evergreen explainer** — a bet on durable educational reach over news-cycle timeliness. Both are creator-growth strategies; Brad's is systematized/repeatable, Nate's is a format experiment. Brad's 174-view just-published number vs Nate's 6.8K reflects publish recency, not reach — Brad's channel is the one that 10x'd in 3 months *using the skill he's giving away*.

## Notes

- Both surfaced through the `ai-creators-youtube` farmer's Apify run on 2026-06-03
- For deeper ingest: clone Brad's `/content-ideas` repo (`github.com/bradautomates/cont...`) and diff its scoring/scraping logic against the vault's `yt-search` + Apify farmer; pull video #1's transcript for the exact outlier-rating computation and the live demo
- Nate's history-explainer transcript would resolve the specific people/dates beyond the chapter map, but introduces no vault-tracked concept

## Related

- [[content-ideas-skill]] — new concept ([[brad-bonanno]]'s free content-ideation skill)
- [[brad-bonanno]] — creator-growth axis of his product trajectory
- [[nate-herk]] — content-format pivot to AI-history explainer
- [[context-farming]] — `/content-ideas` is a content-ideation farmer
- [[self-improving-skills]] — auto-memory preference is the subjective cousin of binary criteria
- [[claude-code]], [[codex]] — cross-vendor substrates the skill runs on
- [[free-sample-phase]] — cross-vendor portability stance
