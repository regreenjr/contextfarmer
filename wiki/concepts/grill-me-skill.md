---
title: Grill Me Skill (Context Extraction Front-End)
category: concept
summary: [[nate-herk]]'s free [[claude-skills]] skill (2026-06-04, 36.8K views) that inverts the usual prompting direction — instead of you prompting Claude, **the skill relentlessly interviews *you* about a process and writes the answers back to a knowledge doc** so nothing gets lost; the thesis *"the hardest part of building a good AI system isn't the prompts, it's getting everything out of your head and into the system"*; **checkpoints after every answer** (no progress lost in a long extraction); produces **brainstorm files** as working artifacts; payoff claim: front-loading context this way gets a downstream skill to **~90% quality on the first try instead of grinding through 30 iterations**; the **context-extraction primitive** the vault has circled — the front-loading-context complement to [[skill-creator]] (which iterates *after* authoring), the individual-scale solution to [[public-ai-work]]'s tacit-knowledge/apprenticeship gap, and the inverse of [[ai-question-method]] (there Claude questions to do work; here the skill questions you to capture knowledge); instantiates [[ai-operating-system]]'s "context is king" and feeds the [[karpathy-llm-wiki]] knowledge-doc pattern
tags: [grill-me-skill, nate-herk, claude-skills, claude-code, context-extraction, front-loading-context, knowledge-doc, checkpointing, brainstorm-files, tacit-knowledge, ai-operating-system, context-is-king, skill-creator, ai-question-method, public-ai-work, karpathy-llm-wiki, free-skill, skool]
sources: 1
updated: 2026-06-05
---

# Grill Me Skill

## What it is

A free [[claude-skills]] skill by [[nate-herk]], introduced in *The Skill That 10x'd My Claude Code Projects* (36.8K views, 2026-06-04, 7:24) in [[youtube-digest-apify-2026-06-05]]. It **inverts the usual prompting direction**: instead of you prompting Claude, the skill *"relentlessly interviews you about a process and writes it all back to a knowledge doc so nothing gets lost."* Claude interrogates *you*.

## The thesis

> *"The hardest part of building a good AI system isn't the prompts, it's getting everything out of your head and into the system."*

The bottleneck in agentic systems is not model capability or prompt craft — it's **extraction**: most of the process knowledge that makes a system good lives only in the operator's head, never written down. Grill Me is a skill whose entire job is to **pull that tacit knowledge out** and durably record it before any downstream skill is built.

## How it works (chapter map)

| Chapter | Mechanic |
|---|---|
| 0:00 | **The Hardest Part Is Extraction** — the framing thesis |
| 1:03 | **What The Grill Me Skill Does** — drives a structured Q&A about a process, writes answers back to a single knowledge doc |
| 2:11 | **Checkpointing** — saves state after *every* answer, so a long extraction session never loses progress |
| 3:00 | **Brainstorm Files In Action** — working artifacts captured during the interview, shown live |
| 4:00 | **Why It's Worth It** — front-loading context pays for itself in fewer downstream iterations |
| 5:22 | **Get it FREE** — via his Skool *AI OS Course* |
| 7:05 | Final Thoughts |

**Checkpointing** is the most transferable mechanic — it mirrors the vault's append-only `log.md` and the `/wiki-ingest` checkpoint discipline: never lose accumulated context to a crash or a long session.

## The payoff claim

> Front-loading context this way gets a downstream skill to **~90% quality on the first try instead of grinding through 30 iterations.**

The core economic argument: **extraction up front replaces iteration later.** Spending one focused interview to capture context cleanly is cheaper than 30 build-test-fix cycles where the model is guessing at context you never wrote down. This is the **front-loading-context complement** to [[skill-creator]] — Skill Creator iterates a skill against evals *after* you author it; Grill Me reduces the iteration count by getting the context right *before* you author it.

## Where it sits in the vault

| Concept | Relationship to Grill Me |
|---|---|
| **[[ai-question-method]]** ([[nate-b-jones]]) | The **inverse**. There, Claude asks sharp questions to *do work* (flashlight intent / ask what good looks like / wrestle). Here, the skill asks *you* sharp questions to *capture knowledge*. Same "questioning beats prompting" instinct, opposite direction. |
| **[[ai-operating-system]]** ([[nate-herk]]) | The **instantiation of "context is king."** The Four C's put context first; Grill Me is the tool that fills the context layer. |
| **[[karpathy-llm-wiki]]** | The **destination.** Grill Me produces a knowledge doc; the wiki is the canonical place that doc compounds. "One source of truth" ([[ai-operating-system]]) restated as an extraction workflow. |
| **[[skill-creator]]** | The **other half of the pipeline.** Grill Me (extract context) → author skill → Skill Creator (eval + optimize). Front-load context, then close the loop. |
| **[[public-ai-work]]** ([[nate-b-jones]]) | The **individual-scale solution** to the apprenticeship gap / Polanyi's paradox (tacit knowledge that never gets written down). Public AI Work is the org-scale version (make AI work visible); Grill Me is the personal version (make *your* process visible). |
| **[[content-ideas-skill]]** ([[brad-bonanno]]) | A **sibling free-skill giveaway** as creator lead magnet, one batch prior. Both are free skills credited with outsized leverage, distributed as the top-of-funnel offer. |

## Why it matters for 3Ps

- **The context-extraction front-end the vault needs.** `farmer/` setup, wiki-source authoring, and client onboarding all begin with "get the operator's process out of their head." Grill Me is a candidate to **port into the vault** — a structured interview that feeds `/wiki-ingest` or a new farmer config, with checkpointing so a long discovery session is never lost.
- **Reframes the onboarding deliverable.** A 3Ps client engagement's first artifact shouldn't be a prompt or a skill — it should be a **knowledge doc extracted by interview**. "We grill you for an hour, you get a context base your AI system runs on" is a cleaner first-deliverable than "we'll write you some skills."
- **Quantifies the front-loading argument.** "90% on the first try vs 30 iterations" is a billable talking point: extraction is not overhead, it's the thing that makes everything downstream cheap.

## Open questions

- **Is the skill file public** (GitHub) or Skool-gated only? (Brad's [[content-ideas-skill]] shipped a free GitHub repo; this one is framed as a Skool-course freebie.)
- **What's the interview structure** — fixed question tree, adaptive follow-ups, or model-driven? How does it decide when extraction is "done"?
- **How does the checkpoint format work** — one growing markdown doc, or per-answer files? Diffable against `/wiki-ingest`?
- **Does it dedup / reconcile contradictions** in the operator's answers (the way the wiki flags `> ⚠️ Contradiction:`), or just transcribe?

## Used in

- [[sources/youtube-digest-apify-2026-06-05]] — vault entry point
- [[nate-herk]] — author
- [[claude-skills]] — the skill category
- [[skill-creator]] — front-loading context = fewer eval iterations
- [[ai-operating-system]] — "context is king" instantiated

## Related

- [[ai-question-method]] — the inverse (Claude questions to do work vs the skill questions you to capture knowledge)
- [[karpathy-llm-wiki]] — the knowledge-doc destination
- [[public-ai-work]] — org-scale tacit-knowledge problem; Grill Me is the individual-scale answer
- [[content-ideas-skill]] — sibling free-skill creator lead magnet
- [[nate-herk]] — author; see his [[ai-operating-system]] build framework
