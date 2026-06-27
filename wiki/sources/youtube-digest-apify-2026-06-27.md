---
title: YouTube Digest (Apify) — AI creators + Claude topics — 2026-06-27
category: source
summary: A **3-video farm batch** (32 fetched, 29 dedup-skipped) spanning all three vault-tracked axes. **(1)** [[nate-b-jones]] *I Was The Only Thing Connecting Claude, ChatGPT, and Codex. So I Built My Replacement.* (17.9K views) → new concept [[open-engine]] (his **34th framework**) — the **handoff between agents, not the model, is the bottleneck**; you're the *"human glue"* / *"hallway"*; the fix is a **shared task queue both people and agents read** that hands off work, carries the sources, and leaves a receipt (*prompt mode → work mode*). **(2)** [[brad-bonanno]] *I Automated Pre-Call Research with Claude Code (FULL BUILD)* (249 views, 49:08 live build) → new concept [[event-driven-routines]] — an event-triggered pre-call sales-research agent ("Sally") that fires on a **cal.com webhook → make.com → Claude cloud routine**, scrapes the prospect (Apify + Firecrawl), and writes/attaches a doc via Google Drive + Calendar MCPs; load-bearing lesson is **local routine vs cloud routine vs managed agent**. **(3)** [[learning-to-learn]] (new entity) *How to Create a Karpathy LLM Wiki for your Notes* (332 views) → deepens [[karpathy-llm-wiki]] with the first **Google Antigravity** build substrate + first **Apple Notes** destination + a zettelkasten variant. Two new concepts, one new entity.
source_path: raw/youtube/digest-2026-06-27.md
source_date: 2026-06
authors: [Nate B Jones, Brad Bonanno, LearningToLearn]
ingested: 2026-06-27
tags: [youtube, digest, apify, nate-b-jones, brad-bonanno, learning-to-learn, open-engine, agent-handoff, shared-task-queue, human-glue, loop-managers, prompt-mode, work-mode, event-driven-routines, cloud-routine, cal-com, make-com, sally, pre-call-research, apify, firecrawl, google-drive-mcp, google-calendar-mcp, karpathy-llm-wiki, google-antigravity, apple-notes, obsidian, zettelkasten, three-video-batch]
sources: 1
updated: 2026-06-27
---

# YouTube Digest (Apify) — 2026-06-27

## Source meta

- **Farmer**: `ai-creators-youtube`
- **Fetcher**: Apify `streamers/youtube-scraper`
- **Total fetched**: 32 videos
- **Dedup-skipped**: 29 (already seen)
- **New videos**: 3
- **Creators**: [[nate-b-jones]] (1), [[brad-bonanno]] (1), [[learning-to-learn]] (1)

A **3-video batch** that lands one video on each of the vault's three core axes — the **analyst** (Nate B Jones, agent coordination), the **operator-builder** (Brad Bonanno, event-driven automation), and the **wiki-pattern implementer** (LearningToLearn, Karpathy LLM Wiki). Two new concepts ([[open-engine]], [[event-driven-routines]]) and one new entity ([[learning-to-learn]]).

## Videos

| # | Title | Channel | Views | Date | Duration |
|---|---|---|---|---|---|
| 1 | I Was The Only Thing Connecting Claude, ChatGPT, and Codex. So I Built My Replacement. | AI News & Strategy Daily \| Nate B Jones | 17,892 | 2026-06-26 | 22:04 |
| 2 | I Automated Pre-Call Research with Claude Code (FULL BUILD) | Brad \| AI & Automation | 249 | 2026-06-26 | 49:08 |
| 3 | How to Create a Karpathy LLM Wiki for your Notes | LearningToLearn | 332 | 2026-06-08 | 12:09 |

## Per-video highlights

### #1 Nate B Jones — *I Was The Only Thing Connecting Claude, ChatGPT, and Codex. So I Built My Replacement.*

**17.9K views, 2026-06-26, 22:04. → New concept: [[open-engine]] (his 34th framework).**

The framing: *"Your AI agents don't talk to each other, so you have become the human glue moving work between Claude, Codex, and ChatGPT."* The common story is agents go autonomous; the reality is **the handoff between agents is the bottleneck** — context, sources, and review keep falling back on the human. **Open Engine** is a **shared task queue both people and agents read** that lets agents **hand off work, carry the sources, and leave a receipt** without a human in the middle.

Chapter spine:
- **00:00** How to make your AI agents work as one system
- **01:06** A friend juggling five AI tools
- **04:48** *Agents are loop managers and you are the hallway*
- **06:32** *The fix is a shared queue both people and agents read*

The behavioral ask: move from **prompt mode** (one request at a time, human shuttles output) to **work mode** (agents pull/push a shared queue as one system). *"The agents are finally capable enough to do the work, and the win now is building the queue that moves it between them before you become the bottleneck."* How-to gated to his Substack.

→ New concept: [[open-engine]]. Updates: [[nate-b-jones]] (34th framework), [[agent-protocol-stack]] (build-side instantiation of A2A), [[open-skills]] (work-side cousin of procedures-don't-travel), [[loop-of-loops]] (multi-agent extension).

### #2 Brad Bonanno — *I Automated Pre-Call Research with Claude Code (FULL BUILD)*

**249 views (just-published), 2026-06-26, 49:08 unedited live build. → New concept: [[event-driven-routines]].**

For months Brad ran a sales-research skill **by hand** on every booked call; the problem was remembering to type the slash command. This build **takes him out of the loop**: research fires the instant a booking is made and notes land on the calendar invite before he opens his laptop — the concrete operator-side close of [[nate-b-jones]]' [[anticipation-gap]].

The agent ("**Sally**") pulls the prospect's LinkedIn, work history, company size, recent news, open roles, and buying signals via **Apify** (LinkedIn + Google search) and **Firecrawl** (website + web search), then writes a private research doc with the **Google Drive MCP** and attaches it to the invite with the **Google Calendar MCP** ([[mcp]]).

The load-bearing architecture decision: **why a local routine isn't event-based enough, and when to reach for a Claude cloud routine vs a managed agent.** The trigger chain is `cal.com webhook → make.com (enriches the booking) → Claude cloud routine`. He lets Claude configure the cloud routine straight from the **Git-tracked AIOS repo** and sets **least-access permissions**.

→ New concept: [[event-driven-routines]]. Updates: [[brad-bonanno]], [[ai-operating-system]] (cadence/connections made event-driven), [[claude-code]] (cloud routines + event triggers), [[mcp]] (Drive + Calendar write surface), [[anticipation-gap]] (concrete fix).

### #3 LearningToLearn — *How to Create a Karpathy LLM Wiki for your Notes*

**332 views, 2026-06-08, 12:09. → New entity: [[learning-to-learn]]. Deepens [[karpathy-llm-wiki]].**

A beginner-tier, multi-tool walkthrough of the [[karpathy-llm-wiki]] pattern that adds two genuinely new cells to the vault's implementer matrix: it builds the wiki with **Google Antigravity** (naming Claude Code as the alternative) and targets **Apple Notes** *and* Obsidian, plus a **zettelkasten** variant. A clean **"LLM Wikis for AI vs note-taking"** callout (02:14) distinguishes building for an AI reader vs a human note system. Also demos **skills in Antigravity** (10:08) — cross-substrate confirmation that skills aren't Claude-Code-only.

→ New entity: [[learning-to-learn]]. Updates: [[karpathy-llm-wiki]] (first Antigravity substrate + first Apple Notes destination + zettelkasten variant), [[open-skills]] (Antigravity skills datapoint).

## Cross-batch signals

- **Two same-day videos (06-26) circle the same theme from opposite ends: the human as the bottleneck between agents.** [[nate-b-jones]]' [[open-engine]] is the *queue/coordination* side (move work *between* agents), [[brad-bonanno]]' [[event-driven-routines]] is the *trigger* side (remove the human from *invoking* the agent). Together they sketch the full "take yourself out of the loop" surface — coordination + triggering — that the vault's cron-only farmers don't yet cover.
- **Nate B Jones's cross-vendor-coordination run continues.** open-skills (30th) → loop-of-loops (33rd) → **open-engine (34th)** are three frameworks circling the same insight: the scarce missing piece in a multi-tool 2026 workflow is the **layer between agents**, not the agents. **34 named frameworks in ~54 days.**
- **The Karpathy LLM Wiki pattern keeps diffusing across substrates.** After Claude Code / Codex / Hermes implementations, LearningToLearn adds **Google Antigravity** + **Apple Notes** — the pattern is now substrate- and destination-agnostic, reinforcing the vault's standing read that *having* a wiki no longer differentiates; *what's in it and how the farmers feed it* does.

## Notes

- Surfaced through the `ai-creators-youtube` farmer's Apify run on 2026-06-27.
- Deeper-ingest targets worth a transcript pull: the **exact Open Engine queue implementation** (file? service? MCP both tools mount?) and its receipt format; Brad's **make.com scenario** (middleware enrichment vs in-routine work) and how the **cloud routine authenticates MCPs** in Anthropic's cloud; and LearningToLearn's **Antigravity → Apple Notes write path**.

## Related
- [[open-engine]] — new concept (shared task queue for agent handoff)
- [[event-driven-routines]] — new concept (webhook → cloud routine automation)
- [[learning-to-learn]] — new entity (Antigravity + Apple Notes wiki implementer)
- [[nate-b-jones]] — author #1 (34th framework)
- [[brad-bonanno]] — author #2 (pre-call research build)
- [[karpathy-llm-wiki]] — deepened by #3
- [[anticipation-gap]] — the human-in-the-loop tax both #1 and #2 attack
- [[agent-protocol-stack]] — A2A is the protocol-layer abstraction of Open Engine
- [[ai-operating-system]] — the AIOS Brad's event-driven build extends
- [[mcp]] — Google Drive + Calendar MCPs in #2
- [[claude-code]], [[codex]] — substrates being coordinated
