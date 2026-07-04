---
title: Document Truth Layer (Reliable AI-Built Office Files)
category: concept
summary: [[nate-b-jones]]' 23rd named framework (2026-05-27, 16.8K views) — the **document-reliability discipline** for building Office files (PowerPoint, Excel, Word) with AI agents at the center; core thesis *"a prompt asks for output, but a workflow defines trust"* (a clean-looking deck with an undefendable number is worse than no deck); four-stage pipeline **sources → structure → creation → verification**; the **hostile reviewer prompt** (a second adversarial AI pass whose only job is to find the undefendable claim) + the **task risk gradient** (where AI is highest vs lowest risk on a document task); models are goal-oriented and will *guess without sources*; the document-creation-side complement to [[project-room-workflow]] (canvas-before-prompt for writing) and the deliverable-boundary sibling of [[agent-security]]'s LLM-as-judge (action-boundary). Distinct from [[prove-it-economy]]'s marketing-side "truth layer"
tags: [document-truth-layer, truth-layer, hostile-reviewer, judge-architecture, task-risk-gradient, four-stage-workflow, sources-structure-creation-verification, office-files, powerpoint, excel, word, board-deck, goal-oriented-models, source-pinning, verification-stage, nate-b-jones, workflow-defines-trust, deliverable-trust]
sources: 1
updated: 2026-07-04
---

# Document Truth Layer (Reliable AI-Built Office Files)

[[nate-b-jones]]' **23rd named framework** — *I Built a Deck With AI, Then Made a Second AI Attack It.* ([[youtube-digest-apify-2026-05-28]] #1, 16.8K views, 2026-05-27, 19:29). The **document-reliability discipline** for building Office files with AI agents at the center of the workflow.

## The framing claim

> *"The common story is that ChatGPT, Claude, and Copilot can now build a polished PowerPoint or Excel model in minutes, so the work is basically solved. The reality is more complicated. The output looks finished long before it's actually trustworthy — and a clean-looking deck with an undefendable number is worse than no deck at all."*

The core distinction (chapter 03:00): **a prompt asks for output; a workflow defines trust.** A single prompt produces a finished-*looking* artifact. Only a workflow with a verification stage produces a *defendable* one.

The title's "second AI attack it" is the framework's headline mechanic — the **hostile reviewer prompt**.

## The four stages (chapter 05:25)

The reliable document pipeline runs in four ordered stages:

| Stage | What happens | Failure if skipped |
|---|---|---|
| **1. Sources** | Pin the authoritative inputs *first* — actuals, plan data, source files | Model guesses a plausible number to "finish" (chapter 08:40) |
| **2. Structure** | Define the document skeleton / outline / model shape before content | Content drifts; sections don't trace to a question |
| **3. Creation** | The agent fills the structure from the pinned sources | (low-risk stage per the task risk gradient) |
| **4. Verification** | The **hostile reviewer** pass attacks the artifact for undefendable claims | A clean deck ships with a wrong number nobody caught |

The discipline is that **trust is built in stage 4, not stage 3** — generation alone never produces trust.

## The hostile reviewer prompt

The signature primitive: after the document is built, run a **separate adversarial AI pass** whose *only* job is to find the weakest, least-defendable claim — *"what a hostile reviewer catches that proofreading never will."* It is not a proofread (grammar/format); it is an **adversarial audit of the numbers and assertions**.

This is the **deliverable-boundary instance** of the separate-judge pattern that [[agent-security]] names at the *action* boundary:

| Pattern | Boundary | Judge's job |
|---|---|---|
| [[agent-security]] LLM-as-judge | Action (send email, charge card) | Should this *action* proceed? |
| **Document truth layer hostile reviewer** | **Deliverable (deck, model)** | **Is this *claim* defendable?** |
| [[project-room-workflow]] conflict log | Source canvas (pre-write) | Do my *sources* contradict each other? |

A separate adversarial model invocation generalizes from action safety to **output trust**.

## The task risk gradient (chapter 10:07)

A diagnostic for **where AI is highest vs lowest risk** on a single document task — not every part of a deck carries the same risk:

| Risk | Document elements | Why |
|---|---|---|
| **Highest** | Blended actuals + plan data presented as one number; forward-looking claims; anything cited to memory not a source | The board-deck failure (chapter 07:00) — actuals and plan blended into one undefendable figure |
| **Medium** | Synthesized commentary, comparative framing | Interpretation can drift from the data |
| **Lowest** | Structure, formatting, first-draft prose, layout | Cheap to verify, low blast radius |

Apply the verification budget where the gradient is steepest — heavy scrutiny on high-risk numbers, light touch on formatting.

## Why models guess without sources (chapter 08:40)

The mechanism behind the whole framework: **frontier models are goal-oriented**. Given "finish the deck," a model will **fabricate a plausible number** rather than leave a gap — it optimizes for *looks finished*, not *is true*. The truth layer (pinned sources + verification) exists to make that fabrication structurally impossible rather than relying on the prompt to forbid it. Same root cause as [[project-room-workflow]]'s hallucination thesis (messy/missing context → confident fabrication).

## The payoff (per the source)

For operators and teams the upside is *"real and measured in weeks a year"* — but only realized if you **build a truth layer around the file** instead of dragging in messy sources and hoping the output holds. The framework is positioned as the eight-documents-at-once unlock (chapter 01:30): once verification is systematic, you can run many documents in parallel without trust collapsing.

## Where it sits in [[nate-b-jones]]' framework stack

- **Document-creation-side complement to [[project-room-workflow]]** (his 18th framework) — Project Room shapes the *source canvas* before *writing*; Document Truth Layer adds the *verification pass* after *building*. Together: canvas before → hostile review after, bracketing the AI work on both ends.
- **Deliverable-boundary sibling of [[agent-security]]** — the hostile reviewer is a judge for *output trust* the way the LLM-as-judge is a judge for *action safety*.
- **Trust/reliability pair with [[public-ai-work]]** (his 22nd framework, same batch) — both are about *trust*: Document Truth Layer = trust in the deliverable; Public AI Work = trust/learning in the organization.

## ⚠️ "Truth layer" naming — two distinct frameworks

[[nate-b-jones]] uses "truth layer" for **two different things**:

- [[prove-it-economy]] (14th framework) — the **marketing-side** truth layer: website + pricing pages + docs that LLMs read when recommending a brand.
- **This framework** — the **document-creation-side** truth layer: pinned sources + verification pass around an individual Office file.

Same brand term, different surface. Not a contradiction — flagged on both pages so future queries don't conflate them.

## Why it matters for 3Ps

- **Directly portable client deliverable** — a "document reliability pipeline" (four stages + hostile-reviewer prompt + risk-gradient checklist) is a one-day consulting artifact, same shape as the [[agent-metering]] four pre-renewal questions or the [[capital-allocation-framework]] five-lever audit.
- **The hostile-reviewer prompt is a packageable skill** — a [[claude-skills]]-shape adversarial-audit skill that runs the verification stage on any AI-built deck/model. Natural pairing with Anthropic's `pptx` / `xlsx` / `docx` skills (which generate the artifact) — this skill *audits* it.
- **High-stakes-document vertical** — finance (board decks, models), legal (filings — cf. the Sullivan & Cromwell unlock in [[project-room-workflow]]), consulting deliverables. The risk gradient tells clients exactly where to spend verification effort.

## Open questions

- **The four "make-visible parts" vs four "stages"** — distinct from [[public-ai-work]]'s "four parts of AI work to make visible"; confirm no overlap when transcripts land.
- **Hostile-reviewer prompt specifics** — gated to the Substack "Truth Layer Guide + Prompts"; transcript/newsletter ingest needed for the exact prompt.
- **Does the hostile reviewer need a frontier model?** — [[agent-security]] argues judges must be frontier-tier (cheap judges share the actor's failure correlation). Open whether the same holds for document review.

## Related pages

- [[nate-b-jones]] — framework author (23rd named framework)
- [[youtube-digest-apify-2026-05-28]] — primary source
- [[project-room-workflow]] — canvas-before-prompt sibling (source-side discipline)
- [[agent-security]] — LLM-as-judge at the action boundary (the hostile reviewer is the deliverable-boundary analog)
- [[public-ai-work]] — same-batch trust/reliability framework (organizational side)
- [[prove-it-economy]] — the *other* "truth layer" (marketing-side); naming-collision flagged
- [[claude-code]] — substrate; Anthropic `pptx`/`xlsx`/`docx` skills generate the artifacts this framework audits
- [[claude-skills]] — the hostile-reviewer pass is a packageable audit skill
- [[reusable-agent-skeleton]]
