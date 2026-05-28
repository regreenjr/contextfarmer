---
title: YouTube Digest (Apify) — AI creators + Claude topics — 2026-05-28
category: source
summary: 5-video farm batch (32 fetched, 27 dedup-skipped) — (1) [[nate-b-jones]] (16.8K views) ships his **23rd framework** [[document-truth-layer]] (*"a prompt asks for output, a workflow defines trust"* — four-stage Office-file pipeline sources→structure→creation→verification + hostile-reviewer prompt + task risk gradient); (2) [[nate-b-jones]] (18.8K views) ships his **22nd framework** [[public-ai-work]] (Shopify's River agent only runs in public Slack channels; private AI chats widen an apprenticeship gap; Polanyi's paradox; make AI work visible); (3) [[mark-kashef]] (23.5K views, OLD 2024-06 video resurfaced) — 300-hours / 650-discovery-calls AI-consulting fundamentals + Prompt Advisers agency + "five personas in AI adoption" framework; (4) [[kevin-stratvert]] (new entity, 9.5K views) — first vault coverage of [[claude-skills]] running across **Chat + Cowork + Claude Code** surfaces (resolves the long-open "are skills Code-only?" question); (5) [[nate-herk]] (46.2K views) — *100 Hours Testing Claude Code vs ChatGPT Codex* head-to-head → new comparison [[claude-code-vs-codex]] (first performance shootout, not just architectural symmetry)
source_path: raw/youtube/digest-2026-05-28.md
source_date: 2026-05
authors: [Nate B Jones, Mark Kashef, Kevin Stratvert, David DeWinter, Nate Herk]
ingested: 2026-05-28
tags: [youtube, digest, apify, document-truth-layer, truth-layer, hostile-reviewer, task-risk-gradient, four-stage-workflow, office-files, public-ai-work, apprenticeship-gap, polanyi-paradox, tacit-knowledge, shopify, river-agent, slack-vs-teams, declared-spaces, mark-kashef, prompt-advisers, five-personas, ai-adoption-personas, kevin-stratvert, david-dewinter, claude-skills, chat-cowork-claude-code, thread-reply-skill, cross-surface-skills, claude-code-vs-codex, head-to-head, 100-hours, report-showdown, dashboard-battle]
sources: 1
updated: 2026-05-28
---

# YouTube Digest (Apify) — 2026-05-28

## Source meta

- **Farmer**: `ai-creators-youtube`
- **Fetcher**: Apify `streamers/youtube-scraper`
- **Total fetched**: 32 videos
- **Dedup-skipped**: 27 (already seen)
- **New videos**: 5
- **Creators**: [[nate-b-jones]] (2), [[mark-kashef]] (1), [[kevin-stratvert]] (1, new), [[nate-herk]] (1)

## Videos

| # | Title | Channel | Views | Date | Duration |
|---|---|---|---|---|---|
| 1 | I Built a Deck With AI, Then Made a Second AI Attack It. | AI News & Strategy Daily \| Nate B Jones | 16,780 | 2026-05-27 | 19:29 |
| 2 | Shopify CEO Reveals Their Secret AI Developer | AI News & Strategy Daily \| Nate B Jones | 18,802 | 2026-05-26 | 16:24 |
| 3 | 300 hours of AI consulting in 23 minutes | Mark Kashef | 23,464 | 2024-06-05 | 22:58 |
| 4 | Claude Skills Tutorial (2026): Chat, Cowork, and Claude Code | Kevin Stratvert | 9,514 | 2026-05-27 | 14:32 |
| 5 | 100 Hours Testing Claude Code vs ChatGPT Codex (honest results) | Nate Herk \| AI Automation | 46,178 | 2026-05-26 | 26:34 |

## Per-video highlights

### #1 Nate B Jones — *I Built a Deck With AI, Then Made a Second AI Attack It.* (23rd framework)

**16.8K views, 2026-05-27, 19:29. → New concept: [[document-truth-layer]]. Updates: [[nate-b-jones]] (23rd framework), [[claude-code]].**

The **document-reliability framework** for building Office files (PowerPoint, Excel, Word) with AI agents at the center. Core thesis: *"a prompt asks for output, but a workflow defines trust"* — a clean-looking deck with an undefendable number is **worse than no deck at all**. The title's "second AI attack it" is the **hostile reviewer prompt** — a separate adversarial pass whose only job is to find the undefendable claim.

**Substack monetization**: *"Full Post w/ Truth Layer Guide + Prompts"* — `natesnewsletter.substack.com/...` gates the operational checklist + prompt pack.

**Chapter map**:
- 00:00 The Excel and Office files conversation
- 01:30 Past individual-asset territory: eight documents at once
- 03:00 Agents at the heart of the new workflow
- 05:25 How to build documents reliably in a pipeline
- 07:00 The board deck that blended actuals and plan data
- 08:40 Models are goal-oriented and will guess without sources
- 10:07 The task risk gradient: where AI is highest and lowest risk
- 11:20 File creation in [truncated in source]

**The four stages** (chapter 05:25): **sources → structure → creation → verification**. The verification stage is where the hostile-reviewer pass lives.

**Two named diagnostics**:
- **The task risk gradient** (chapter 10:07) — maps where AI is highest-risk vs lowest-risk on a document task. High risk: blended actuals + plan data presented as one number (the board-deck failure at chapter 07:00). Low risk: structure, formatting, first-draft prose.
- **Models guess without sources** (chapter 08:40) — frontier models are goal-oriented and will fabricate a plausible number to "finish the deck" if the source isn't pinned. The truth layer exists to make that impossible.

**Why it matters**: the **document-creation-side complement** to [[project-room-workflow]] (canvas-before-prompt for *writing*) and a sibling to [[agent-security]]'s LLM-as-judge (the hostile reviewer is a judge at the document boundary). The "verification stage" + "hostile reviewer" is the same shape as the separate-judge pattern, applied to deliverable trust rather than action safety. → New concept: [[document-truth-layer]].

### #2 Nate B Jones — *Shopify CEO Reveals Their Secret AI Developer* (22nd framework)

**18.8K views, 2026-05-26, 16:24. → New concept: [[public-ai-work]]. Updates: [[nate-b-jones]] (22nd framework).**

The **organizational-learning framework**: AI adoption is **not a tooling problem you solve by buying licenses** — your most valuable AI work is *invisible*, and that invisibility is widening an **apprenticeship gap**. Unlock event: **Shopify's "River" agent only runs in public Slack channels** (deliberately, so the work is watchable).

**The framing claim**:

> *"What's really happening inside companies that are actually getting smarter with AI, not just faster? The common story is that AI adoption is a tooling problem you solve by buying licenses, but the reality is more complicated."*

**Chapter map**:
- 00:00 The substrate for AI collaboration
- 01:30 Slack versus Teams and Copilot
- 03:29 Why AI is coming to your company
- 04:45 Tooling choices are frontier choices
- 05:46 The apprenticeship gap
- 07:30 Polanyi's paradox and tacit knowledge
- 09:03 What public AI work looks like
- 11:00 Why a prompt library isn't enough
- 13:28 Building a public AI workflow
- 15:00 Privacy, declared spaces, and senior people

**Core claims**:
- **Private AI chats widen an apprenticeship gap** (chapter 05:46) — when senior people do their best AI work in private DMs, juniors can't watch and learn. The tacit knowledge never transmits.
- **Polanyi's paradox** (chapter 07:30) — "we know more than we can tell"; the way an expert *uses* AI is tacit knowledge that only transmits by observation, not by a prompt library (chapter 11:00 — *"why a prompt library isn't enough"*).
- **Four parts of AI work to make visible** — the actionable core (specifics gated to transcript).
- **Tooling choices are frontier choices** (chapter 04:45) — Slack (public-channel-native) vs Teams/Copilot (DM-native) materially shapes whether AI work is observable. Substrate choice = organizational-learning choice.
- **Declared spaces + senior people** (chapter 15:00) — regulated teams can still expose work safely via declared/sanctioned channels; the unlock is **senior people willing to run real work where everyone can watch**.

**Why it matters**: the **org-design-side complement** to his worker-side T/C/L/D and the [[agent-substrate]] thesis (Slack-as-substrate). It reframes [[context-farming]] / [[karpathy-llm-wiki]] as *organizational* apprenticeship infrastructure — a public, watchable record of how the org actually uses AI. → New concept: [[public-ai-work]].

### #3 Mark Kashef — *300 hours of AI consulting in 23 minutes* (resurfaced 2024-06 video)

**23.5K views, published 2024-06-05 (OLD), 22:58. → Updates: [[mark-kashef]], [[ai-consulting]].**

An **older foundational AI-consulting video** the Apify scraper surfaced fresh — Mark's most-viewed video in this farm to date (23.5K), and notably **~2 years older** than every other video in the digest. Distills 300 hours of client work + **650 discovery calls** into an implementation primer. First-person credential: *"Data Science Manager by day, AI automation agency owner by night, a decade in the AI space, founder of Prompt Advisers."*

**Surfaces two facts not previously in his entity page**:
- **Prompt Advisers** is his agency (distinct from the **Early AIdopters** community already tracked); specialization is **Natural Language Processing**.
- **650 discovery calls** is a hard credibility anchor — comparable in shape to [[nate-herk]]'s "$231K in 30 days" or [[brock-mesarich]]'s "$80K/month no employees."

**The "five personas in AI adoption" framework** (chapter 01:29) — a buyer-segmentation model for AI consultants:
1. **The Skeptic** (01:35)
2. **The Enthusiast** (01:58, truncated in source)
3-5. (gated to transcript)

This is a **net-new framework** for the [[ai-consulting]] wedge — a *buyer-psychology* segmentation, complementary to the existing macro-thesis / offer-language / business-model layers. Distinct from the "why now" three-pillars framework in his 2025-11 video. Goal of the video: *"create an AI strategy"* (chapter 01:20). Transcript ingest would resolve personas 3-5.

### #4 Kevin Stratvert — *Claude Skills Tutorial (2026): Chat, Cowork, and Claude Code* (new entity)

**9.5K views, 2026-05-27, 14:32. Host: David DeWinter. Sponsor: Intuit/QuickBooks. → New entity: [[kevin-stratvert]]. Updates: [[claude-skills]].**

The **first vault coverage of [[claude-skills]] running across the full surface set — Chat + Cowork + Claude Code** — and the first from a mainstream **office-productivity tutorial** channel (Kevin Stratvert; this video hosted by David DeWinter). Directly answers the long-standing open question on the [[claude-skills]] page: *"Skills are Code-only today; will they work in the Claude.ai chat surface?"* — **yes**, the same skill runs across all three surfaces.

**What the tutorial covers**:
- **What a Claude Skill is** + how Claude stores dozens of skills without slowing down (progressive-disclosure / load-on-trigger).
- **Build a "Thread Reply" skill from scratch** — replies to long missed email threads — *complete with test cases that grade the skill before you save it* (the [[skill-creator]] eval discipline, surfaced for a non-developer audience).
- **Skills against internal app data** to validate business rules.
- **Running the same skill inside Claude Cowork** on a local folder with more business context.
- **Claude Code handles skills differently** — skills live as folders on disk in `.claude/skills`.
- **Four ways to share a skill with a team** — including a **synced shared folder** so a sub-team runs the same skill *without a Team or Enterprise plan*.

**Chapter map** (truncated in source):
- 0:00 Skills in 2026
- 1:14 Create a Skill
- 3:05 [truncated]

**Why it matters**: extends the [[claude-skills]] explainer funnel into the **mainstream office-productivity tutorial tier** (QuickBooks-sponsored, business-operator audience) and is the canonical demonstration that **skills are surface-portable (Chat ↔ Cowork ↔ Code)**, not Claude-Code-bound. The "test cases that grade the skill before you save it" framing brings [[skill-creator]]-style eval discipline to a non-developer audience — same shape as [[tristen-obrien]]'s beginner-tier pizza-shop demo, but cross-surface. → New entity: [[kevin-stratvert]].

### #5 Nate Herk — *100 Hours Testing Claude Code vs ChatGPT Codex (honest results)*

**46.2K views, 2026-05-26, 26:34. → New comparison: [[claude-code-vs-codex]]. Updates: [[nate-herk]], [[claude-code]], [[codex]].**

[[nate-herk]]'s **100-hour head-to-head shootout** — same prompts, same builds, both tools side by side. The **first explicit performance comparison** of [[claude-code]] vs [[codex]] in this vault, complementing the existing [[codex]] page (which is architectural-symmetry-focused: same `CLAUDE.md`/`AGENTS.md`, same skills format). This video asks *which one actually wins on real builds*, not *which primitives match*.

**Chapter map**:
- 00:00 Biggest comeback?
- 00:30 Claude Code explained
- 01:28 Meet Codex
- 04:04 **Claude's edge**
- 06:19 **Codex fights back**
- 09:13 Sketchy loophole
- 10:22 **Pricing pain**
- 12:48 **Report showdown**
- 15:10 **Landing page**
- 16:32 **Dashboard battle**
- 17:25 The numbers
- 21:02 **Honest verdict**
- 24:46 Final mindset

**The head-to-head categories**: report generation (12:48), landing page (15:10), dashboard (16:32) — three concrete deliverable types scored side by side. The framing ("Biggest comeback?" + "Codex fights back") strongly implies **Codex outperformed expectations** / staged a comeback against the Claude-default audience's priors, but the verdict (chapter 21:02) is gated to transcript.

**Why it matters**: confirms the [[free-sample-phase]] thesis is now *empirically testable* — operators are running real 100-hour comparisons during the free-tier window. Strengthens the **vendor-agnostic 3Ps positioning**: the same deliverables ship on both substrates, so the choice is performance/pricing, not architecture. → New comparison: [[claude-code-vs-codex]].

## Cross-video signals

**Nate B Jones ships two more frameworks (22nd + 23rd)** — extends his cadence to **23 named frameworks in 24 days** (T/C/L/D 2026-05-04 → [[document-truth-layer]] 2026-05-27). Both are **trust/reliability frameworks**: [[document-truth-layer]] (deliverable trust) + [[public-ai-work]] (organizational-learning trust). After the 2026-05-26 interview-format experiment ([[platform-agent-asymmetry]]), he reverts to solo-monologue framework videos here.

**Two distinct "judge / hostile reviewer" patterns now in the vault** — [[agent-security]]'s LLM-as-judge (action boundary) + [[document-truth-layer]]'s hostile-reviewer pass (deliverable boundary). The separate-adversarial-model pattern generalizes from *action safety* to *output trust*.

**The "second 'truth layer'" naming collision** — [[prove-it-economy]] already uses "truth layer" (marketing-side: website/pricing/docs that LLMs read). [[document-truth-layer]] is a *different* truth layer (document-creation-side: pinned sources + verification pass). Both are Nate B Jones frameworks; the shared term is intentional brand consistency, not a contradiction. Flagged on both pages.

**Cross-surface skills resolve a standing open question** — [[kevin-stratvert]]'s tutorial shows the same skill on Chat + Cowork + Claude Code, answering the [[claude-skills]] "Code-only?" open question. The skills primitive is now confirmed surface-portable, not just vendor-portable ([[codex]]).

**Empirical substrate comparison goes mainstream** — [[nate-herk]]'s 100-hour Claude-vs-Codex shootout (46.2K views, the highest-view video in this batch) is the first real performance benchmark in the farm; prior [[codex]] coverage was symmetry-mapping only.

**Resurfaced old content** — [[mark-kashef]]'s #3 is a 2024-06 video (~2 years old), the oldest in any digest. The Apify scraper occasionally surfaces evergreen back-catalog content as "new"; useful for back-filling foundational frameworks (here: five-personas buyer segmentation) but the publish date must be read carefully.

## Notes

- All 5 videos surfaced through the `ai-creators-youtube` farmer's Apify run on 2026-05-28
- Dedup rate (84.4%, 27/32) is the *lowest* of recent batches (93.75% on 2026-05-26, 90.6% on 2026-05-25) — consistent with the larger 5-video new-signal count
- [[nate-b-jones]] + [[nate-herk]] both appear again — now ~13 of 14 YouTube digest batches since cold start
- Publish dates span ~2 years (2024-06 → 2026-05-27); read [[mark-kashef]] #3 as back-catalog, not fresh
- Substack ([[nate-b-jones]]) + Skool ([[nate-herk]], [[mark-kashef]]) monetization layers continue

## Related

- [[document-truth-layer]] — new concept (Nate B Jones #23, hostile-reviewer + four-stage Office-file pipeline)
- [[public-ai-work]] — new concept (Nate B Jones #22, Shopify River agent + apprenticeship gap + Polanyi's paradox)
- [[claude-code-vs-codex]] — new comparison (Nate Herk 100-hour head-to-head)
- [[kevin-stratvert]] — new entity (mainstream office-productivity tutorial channel)
- [[nate-b-jones]] — 22nd + 23rd frameworks
- [[nate-herk]] — first head-to-head substrate comparison
- [[mark-kashef]] — Prompt Advisers + 650 discovery calls + five-personas framework
- [[claude-skills]] — cross-surface (Chat/Cowork/Code) confirmation
- [[claude-code]], [[codex]] — head-to-head performance comparison
- [[ai-consulting]] — five-personas buyer segmentation added
- [[project-room-workflow]], [[agent-security]] — adjacent frameworks extended by [[document-truth-layer]]
- [[agent-substrate]], [[context-farming]], [[karpathy-llm-wiki]] — reframed as apprenticeship infrastructure by [[public-ai-work]]
