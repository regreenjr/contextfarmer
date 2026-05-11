---
title: YouTube Digest (Apify) — AI creators + Claude topics — 2026-05-11
category: source
summary: Small 2-video farm batch — [[nate-b-jones]] reframes the McKinsey Lilly "22 unauthenticated endpoints" incident as a procurement-sequence failure (not a security hygiene failure) and surfaces a new substrate question — "does your platform know humans from agents"; [[chase-ai]] (new entity) ships the canonical walkthrough of Anthropic's brand-new Skill Creator (evals + blind A/B + description optimization) and names the two-types skill split (capability-uplift vs encoded-preference)
tags: [youtube, digest, claude-code, claude-skills, skill-creator, agent-security, procurement, work-primitive, anthropic, openai, sap, pinecone, salesforce, servicenow, mckinsey, chase-ai]
sources: 1
source_path: raw/youtube/digest-2026-05-11.md
source_date: 2026-05
authors: [farmer-ai-creators-youtube, apify-yt-scraper]
ingested: 2026-05-11
updated: 2026-05-11
---

# YouTube Digest (Apify) — 2026-05-11

Eighth batch from the [[ai-creators-youtube]] farm. **2 new videos, 30 dedup-skipped** — a thin batch immediately following the dense 2026-05-10 batch (expected post-spike behavior). Both videos are high-signal, though: one introduces a net-new strategic frame and a new product-surface question; the other is the canonical walkthrough of an Anthropic skill-authoring product that this vault's [[claude-skills]] page has been referencing without first-hand coverage.

## TL;DR

Two orthogonal additions:

1. **Agent security is a procurement/org-design problem, not a tech-hygiene problem** ([[nate-b-jones]] #1, 53.6K views — the highest-views entry in this batch). The McKinsey "Lilly" platform exploit ($20 SQL injection through 22 of 200 unauthenticated endpoints) is the unlock event. Common framing: "they forgot to lock down their endpoints." [[nate-b-jones]]' reframe: **traditional SaaS procurement breaks when the buyer can't tell humans apart from agents.** Vendor responses cited: Anthropic, OpenAI, SAP, Pinecone, Salesforce, ServiceNow — all pitching answers to the same underlying authentication question. The strategic move: **bring developers to the table before signing**, because implementation IS the strategy in the agent era. → New concept: [[agent-security]]. Updates: [[nate-b-jones]] (7th framework), [[work-primitive]] (the "knows humans from agents" question is a new authority-layer diagnostic), [[anthropic]] / [[openai]] / [[pinecone]] (each now positioned in the agent-security vendor response).
2. **The Skill Creator finally has first-hand coverage in this vault** ([[chase-ai]] #2, 107K views, 12 minutes). [[anthropic]]'s Skill Creator (referenced in [[claude-skills]] via [[code-with-beto]] #6 in [[youtube-digest-apify-2026-05-03]]) is **a meta-skill that tests, benchmarks, and optimizes other skills using plain language + evals + blind A/B testing + description optimization**. [[chase-ai]] (new entity, ~150K-sub-tier; Skool community at `skool.com/chase-ai`) introduces the **two-types skill split**:
   - **Capability uplift** skills — add ability the model didn't have
   - **Encoded preference** skills — bend the model to your house style

   Each type evals differently (capability = task-pass-rate; preference = output-distribution match). → New entity: [[chase-ai]]. New concept: [[skill-creator]]. Updates: [[claude-skills]] (Skill Creator now has first-hand walkthrough citation + two-types framing), [[anthropic]] (Skill Creator as named product surface).

## Videos

| # | Title | Channel | Views | Date | Duration |
|---|---|---|---|---|---|
| 1 | Anthropic And OpenAI Just Admitted The Model Isn't Enough. | [[nate-b-jones]] | 53.6K | 2026-05-10 | 20:48 |
| 2 | Claude Code Skills Just Got a MASSIVE Upgrade | [[chase-ai]] | 107.3K | 2026-03-04 | 12:19 |

URLs: `youtube.com/watch?v=` + `EpJ0CjTJSag` (#1), `UxfeF4bSBYI` (#2).

> Note: #2's date (2026-03-04) is older than #1; it surfaces here because of dedup-state drift in the farm — neither video had been ingested before. The 107K views figure suggests it's been live for ~9 weeks, putting it among [[chase-ai]]'s top-performing skill content.

## Key claims (synthesized)

### #1 [[nate-b-jones]] — *Anthropic And OpenAI Just Admitted The Model Isn't Enough*

The **procurement-side** framework. Adds a seventh named diagnostic to [[nate-b-jones]]' framework stack.

**The unlock event**:
- **McKinsey's "Lilly" AI platform** was exploited via **$20 SQL injection** — an attack mostly extinct from 2026's standard SaaS attack surface
- The attacker reached one entry point, then escalated through **22 of 200 endpoints that were left unauthenticated**
- Common narrative: "carelessness — they forgot auth"
- [[nate-b-jones]]' reframe: **22 unauthenticated endpoints out of 200 is a pattern, not a mistake** — it signals a culture/process gap, not a one-off oversight

**The procurement-sequence claim** (chapter 6:10, *Why agents break the old procurement sequence*):
- **Traditional SaaS procurement**: legal → security → IT → eventually-implementation. Implementation is *downstream* of strategy.
- **Agent procurement breaks this** because a single agent run *touches* multiple downstream systems (chapter 8:45). The implementation surface becomes the security surface.
- **Implementation IS the strategy in the agent era** (chapter 10:30) — this is the punchline. The cheapest move for buyers is bringing developers to the procurement table *before* signing, not after.

**Vendor responses** (chapter 12:15, *Anthropic, OpenAI, SAP, Pinecone, Salesforce, ServiceNow respond*):
- All six vendors pitched their answer to the same underlying problem in the same week
- This is **the "Pinecone admits RAG is broken" shape** from [[knowledge-layer]] — when category leaders all ship the same product in the same week, that's a category, not coincidence

**The new substrate question** (chapter 15:20, *Does your platform know humans from agents*):
- The procurement-side equivalent of [[work-primitive]]'s authority layer
- Most current platforms treat agent traffic as if it were human user traffic — same auth tokens, same session model, same audit trail
- The actual buyer question for any agent-touching product: **"can your platform distinguish a human action from an agent action, and apply different policies?"**

**Strategic significance**: this is a **new diagnostic layer above [[work-primitive]]** — Work Primitive asks *can the agent reach + understand + commit?*; Agent Security asks *can the platform tell when it's an agent doing it, and act differently?* Pairs with the existing authority layer.

→ New concept: [[agent-security]]. Updates: [[nate-b-jones]] (now 7 named frameworks), [[work-primitive]] (authority layer gains the "humans-vs-agents" sub-diagnostic), [[anthropic]] / [[openai]] / [[pinecone]] (now positioned as agent-security responders).

> Note: this is [[nate-b-jones]]' **first procurement-focused framework**. Prior frameworks (T/C/L/D worker, anticipation-gap user, work-primitive substrate, plugins builder, code-comprehensibility codebase, OpenClaw stack) all targeted post-buy diagnostics. This one targets the *buy* itself.

### #2 [[chase-ai]] — *Claude Code Skills Just Got a MASSIVE Upgrade*

The **canonical first-hand walkthrough** of [[skill-creator]] in this vault. Prior coverage ([[code-with-beto]] #6 in [[youtube-digest-apify-2026-05-03]], [[anthropic]] #4 same digest) referenced Skill Creator existed; this is the first end-to-end demo + framework.

**The two-types skill split** (chapter 2:47, *Skill Types & Evals*):
- **Capability uplift** — skills that add an ability the model couldn't do well otherwise (e.g., a new domain reasoning template, a tool-orchestration pattern). Eval target: **task pass rate** — does the skilled model succeed where the unskilled model fails?
- **Encoded preference** — skills that bend the model toward a specific style or convention the model could already approximate (e.g., "write in our brand voice", "format outputs to our spec"). Eval target: **output distribution match** — does the skilled output look more like the target than the unskilled output?

This is **the missing eval framework** for the [[claude-skills]] discourse — prior framings (Ben AI's "3 Types", Anthropic's authoring guide) named categories without specifying how to evaluate each.

**What Skill Creator buys you** (chapter 7:27, *The Tests*):
- **Evals in plain language** — no test harness scaffolding required
- **Blind A/B testing** — skilled vs unskilled run on same input, output compared without revealing which is which
- **Description optimization** — Skill Creator iterates on the skill's *description field* (used by Claude to decide whether to invoke the skill) to improve invocation accuracy
- The output: a benchmarked, A/B-tested, invocation-tuned skill — not just "I wrote a skill that seems to work"

**The workflow demo** (chapter 8:59, *Using Skill-Creator in Claude Code*): build-a-skill-from-scratch + run-an-eval walkthrough. Concrete artifact.

**Why this matters for [[claude-skills]]**:
- Resolves the **authoring-evaluation gap** — prior to Skill Creator, skill authors had no standard way to benchmark their work
- **Skills become testable software**, not prose snippets — same shift unit tests created for code in the 2000s
- The **description field is now an optimizable surface** — small wording changes affect invocation rate; Skill Creator automates this

**Distribution context**: [[chase-ai]] is a new tracked entity. Sub-tier ~150K (inferred from 107K view + Skool community sizing). Operates `skool.com/chase-ai` (paid "Master Claude Code, Build Your Agency, Land Your First Client") + `skool.com/chase-ai-community` (free) + `chaseai.io` (consult booking) — classic AI-creator three-tier funnel (audience → community → service). Closest analog in this vault: [[brock-mesarich]] (non-technical curator) or [[nate-herk]] (skill-builder tutorials), but [[chase-ai]] is **more agency-oriented** ("Build Your Agency, Land Your First Client" framing).

→ New entity: [[chase-ai]]. New concept: [[skill-creator]]. Updates: [[claude-skills]] (Skill Creator first-hand citation, two-types eval framework), [[anthropic]] (Skill Creator as named product surface), [[claude-code]] (Skill Creator workflow integration).

## Themes

- **[[claude-skills]]** — moves from "skills exist + many are useless" curation discourse to "skills are testable software" evaluation discourse. [[skill-creator]] is the inflection-point tool.
- **[[claude-code]]** — primary substrate retains position; [[skill-creator]] runs inside it as a meta-skill
- **[[anthropic]]** — Skill Creator joins SpaceX deal (2026-05-10) and Mythos (2026-05-10) as new product-surface entries in this 4-day window. Skill Creator and Mythos are both **AI-built-for-AI-builders** tools — Anthropic is increasingly shipping infrastructure for the people building on its substrate.
- **Agent security** — first appearance as a top-line theme. [[agent-security]] is the procurement-side complement to [[work-primitive]]'s post-buy substrate diagnostic.
- **[[nate-b-jones]] framework velocity** — 7th named framework in this vault; he's now contributing roughly one named diagnostic per video. The cadence makes him the single highest-density framework producer.

## Surprises / contradictions

- **The McKinsey incident framing is genuinely new for this vault** — security has been an ambient concern (mentioned in [[code-comprehensibility]] for codebase-side) but [[agent-security]] is the first **buyer-side** security frame here.
- **"Implementation is the strategy"** is a strong reframe — it implies the existing [[ai-consulting]] practice positioning ("we help you adopt AI tools") should sharpen toward **"we sit at your procurement table"**. Direct portability into 3Ps engagement scoping.
- **The two-types skill eval split** is a quiet but important resolution. The [[claude-skills]] page's "authoring vs composition vs curation" stack didn't have a *quality* dimension. [[chase-ai]]'s capability-uplift / encoded-preference split provides it.
- **Six-vendor convergence on agent security in one week** — Anthropic, OpenAI, SAP, Pinecone, Salesforce, ServiceNow all pitching the same week is the same shape as Pinecone/Microsoft/Google all shipping [[knowledge-layer]] products in four weeks ([[youtube-digest-apify-2026-05-10]] #4). Convergence cadence is now sub-month for major architectural shifts.
- **Why didn't [[chase-ai]] appear earlier?** Video is from 2026-03-04 (9 weeks old) with 107K views — should have been in the dedup state already. Likely the farmer's keyword set wasn't matching "Chase AI" until recently, or the video resurfaced via algorithm. Worth a periodic check of which top creators the farm is *missing*.

## Filtered out as noise

- None. Both videos are on-topic and contribute either net-new concepts/entities or framework reinforcement.
- 30 dedup-skipped — consistent with mature dedup state (~94% dedup hit rate this batch, up from ~63% in 2026-05-10).

## Connections

- **New entities**: [[chase-ai]]
- **New concepts**: [[agent-security]], [[skill-creator]]
- **Updated entities**: [[nate-b-jones]] (#1 — agent security framework), [[anthropic]] (Skill Creator surface, agent-security responder), [[openai]] (agent-security responder), [[pinecone]] (agent-security responder)
- **Updated concepts**: [[claude-skills]] (Skill Creator first-hand walkthrough, two-types eval framework), [[claude-code]] (Skill Creator workflow), [[work-primitive]] (authority layer + humans-vs-agents sub-diagnostic)
- **Builds on**: [[youtube-digest-apify-2026-05-03]] (Skill Creator was referenced via [[code-with-beto]] #6 + [[anthropic]] #4 without first-hand demo; [[chase-ai]] now provides it), [[youtube-digest-apify-2026-05-10]] (agent-security extends [[work-primitive]]'s authority layer)
- **Open follow-up**:
  - Transcript ingest for #1 (the full six-vendor response detail; the McKinsey postmortem specifics)
  - Transcript ingest for #2 (the actual eval-output examples for capability-uplift vs encoded-preference)
  - Check whether McKinsey publicly responded to the Lilly framing
  - Are there other [[chase-ai]] videos the farmer is missing? Cross-check his channel
  - Does [[skill-creator]] have known limitations (e.g., on Skills that depend on external tools)?

## Why this matters for 3Ps

1. **[[agent-security]] is the cleanest procurement-conversation entry point yet.** The "does your platform know humans from agents" question is a single sentence that turns any AI vendor-evaluation conversation into a scoping exercise. Direct alternative to vague "AI readiness" conversations.
2. **"Implementation is the strategy"** sharpens [[ai-consulting]] positioning. The 3Ps offering can claim a seat at *procurement* discussions, not just post-buy implementation — that's a higher-margin engagement scope.
3. **[[skill-creator]] resolves the skill-quality question.** Prior to this video, "how do I know my skill is good?" was a vibes-based answer. Now there's a tool. For 3Ps client deliverables shipping as skills, this becomes the **acceptance test** — "we ran Skill Creator evals, here are the pass rates."
4. **The two-types eval split is a deliverable-categorization tool.** When scoping a client engagement, label each proposed skill as capability-uplift or encoded-preference up front — sets the eval target, sets the acceptance criteria, sets the demo plan. Different success metrics flow from different categories.
5. **[[chase-ai]]'s funnel pattern is a 3Ps reference architecture.** Free YouTube → free Skool → paid Skool → consult. Same shape applicable to a 3Ps content/community/consult ladder.
6. **Six-vendor agent-security convergence is a content angle.** "Why Anthropic, OpenAI, SAP, Pinecone, Salesforce, and ServiceNow all shipped agent-security responses in the same week" is publishable thought leadership.

## Where it's cited in this wiki

- [[entities/chase-ai]] (new)
- [[concepts/agent-security]] (new)
- [[concepts/skill-creator]] (new)
- [[entities/nate-b-jones]] (updated — 7th framework)
- [[entities/anthropic]] (updated — Skill Creator surface, agent-security responder)
- [[entities/openai]] (updated — agent-security responder)
- [[entities/pinecone]] (updated — agent-security responder)
- [[concepts/claude-skills]] (updated — Skill Creator first-hand citation, two-types framework)
- [[concepts/claude-code]] (updated — Skill Creator workflow)
- [[concepts/work-primitive]] (updated — humans-vs-agents authority sub-diagnostic)

## Notes

- Fetched via Apify `streamers/youtube-scraper`
- Dedup state: 30 videos already seen, 2 new (mature dedup; ~94% hit rate this batch)
- Original digest at `raw/youtube/digest-2026-05-11.md`
- For deeper ingest: drop transcripts at `raw/youtube/<channel>/<slug>.md` and re-run `/wiki-ingest`. Highest-value transcript candidates: #1 (six-vendor agent-security response detail, McKinsey Lilly postmortem specifics) and #2 (Skill Creator eval-output examples for both skill types)
