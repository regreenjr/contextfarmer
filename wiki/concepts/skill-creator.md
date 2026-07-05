---
title: Skill Creator
category: concept
summary: Anthropic-published meta-skill for Claude Code that tests, benchmarks, and optimizes other skills using plain-language evals, blind A/B testing, and description-field optimization; resolves the authoring-evaluation gap in [[claude-skills]] and makes skills "testable software" rather than prose snippets; the two-types skill split (capability uplift vs encoded preference) named by [[chase-ai]] gives each skill type a clean eval target; **in 2026-05-23 [[simon-scrapes]]' [[self-improving-skills]]** (109.7K views, Karpathy-autoresearch-inspired autonomous loop + binary criteria) extends Skill Creator's single-shot eval into a **closed-loop overnight optimization** — together they form the complete authoring → evals → optimization pipeline
tags: [skill-creator, claude-skills, claude-code, anthropic, eval, meta-skill, ab-test, capability-uplift, encoded-preference, description-optimization, self-improving-skills, closed-loop, autonomous-loop, binary-criteria, karpathy-autoresearch, simon-scrapes, grill-me-skill, front-loading-context, context-extraction, nate-herk, skill-authoring-lessons, gotchas-section, stop-railroading, brock-mesarich, skill-forge, generation-first, alek]
sources: 5
updated: 2026-07-05
---

# Skill Creator

## What it is

[[anthropic]]-published **meta-skill** that lives inside [[claude-code]]. Distributed via `claude-plugins-official` (install: `/plugin install skill-creator@claude-plugins-official`).

Its job: take an existing skill (or scaffold a new one) and **test, benchmark, and optimize it** — using plain-language eval specs, blind A/B testing against unskilled baselines, and automated description-field iteration to improve invocation accuracy.

Surfaced canonically in this vault via [[chase-ai]]'s [[youtube-digest-apify-2026-05-11]] #2 — the first end-to-end first-hand walkthrough.

## Why it matters

Pre-Skill-Creator, [[claude-skills]] had a structural problem: **skills were prose, not software**. Authors wrote skill markdown, eyeballed outputs, and shipped. There was no standard way to ask "is my skill actually better than no skill?" The discourse around skill quality was vibes-based.

Skill Creator changes the shape:
- **Skills become testable software** — same shift unit tests created for source code
- **The description field is now an optimizable surface** — small wording changes affect invocation rate; Skill Creator automates the optimization
- **Cross-author quality comparisons become possible** — same eval framework applied to two competing skills produces a comparable signal
- **Authoring loops shorten** — write → eval → iterate replaces write → ship → hope

## How it works (per [[chase-ai]] #2 in [[youtube-digest-apify-2026-05-11]])

Three primary capabilities:

### 1. Plain-language evals

The user describes the eval criteria in plain English ("the output should follow our brand voice", "the skill should successfully convert markdown tables to CSV"). Skill Creator generates the test scaffolding from the description — no test harness boilerplate required.

This is a **lowered floor** — authors who couldn't (or wouldn't) write a Python test suite for their skill can still run benchmarked evaluations.

### 2. Blind A/B testing

Same input fed to:
- **Skilled run** — Claude with the skill loaded
- **Unskilled baseline** — Claude without the skill

Outputs are compared without revealing which is which. The comparison answers: **does the skill actually change behavior in the desired direction?**

This is the **falsifiable test** for skill value. A skill that produces identical or worse output vs unskilled baseline fails the eval — regardless of how clever the markdown reads.

### 3. Description-field optimization

The skill's `description` field is what Claude uses at runtime to decide *whether to invoke* the skill. Skill Creator iterates the description wording, runs invocation tests, and converges on a description that improves invocation accuracy on relevant prompts (and reduces false-positive invocations).

This is **the highest-leverage optimization** for skill authors — a perfectly-built skill that Claude rarely invokes is functionally useless, and description tuning is non-obvious by hand.

## The two-types skill split (from [[chase-ai]] #2)

The eval framework branches by skill type:

| Type | Definition | Eval metric | Example |
|---|---|---|---|
| **Capability uplift** | Adds an ability the model couldn't do well | Task pass rate (skilled vs unskilled) | New domain reasoning template, tool-orchestration pattern |
| **Encoded preference** | Bends the model toward a style/convention the model could already approximate | Output distribution match (skilled output looks more like target) | Brand voice, format spec, house style |

This is the **missing eval rung** in the [[claude-skills]] discourse. Authoring frameworks (Ben AI's "3 Types") named *categories*; composition frameworks (Simon Scrapes' Skill Systems) named *chaining*; this split names **how you decide whether a skill works**.

For 3Ps deliverables: every shipped skill should be **labeled with its type at authoring time** — the eval target and acceptance criteria flow from the label.

## Where it fits in the [[claude-skills]] stack

Updated stack with Skill Creator's place:

| Layer | Question | Voices / tools |
|---|---|---|
| Taxonomy | What types of scaffolding exist? | [[nate-b-jones]] ([[plugins]]) |
| Authoring | How do I write *one* skill well? | [[code-with-beto]], [[anthropic]] authoring guide |
| Authoring framework | What categories of skills exist? | [[ben-ai]] (3 Types), [[chase-ai]] (capability vs preference) |
| **Evaluation (single-shot)** | **Does my skill actually work?** | **[[skill-creator]] (this)** |
| **Optimization (closed-loop)** | **Can my skill be converged to as-good-as-possible?** | **[[self-improving-skills]] ([[simon-scrapes]] 2026-05-23)** |
| Composition | How do skills chain into automations? | [[simon-scrapes]] ([[skill-systems]]) |
| Curation | Which skills to install? | [[nate-herk]], [[brock-mesarich]], [[dubibubii]] |

Skill Creator sits between authoring and composition — it's the **acceptance test** before a skill is fit to compose with other skills.

## Extension: [[self-improving-skills]] closed-loop (2026-05-23)

[[simon-scrapes]]'s 2026-05-23 109.7K-view video ships [[self-improving-skills]] — the **closed-loop optimization layer** above Skill Creator's single-shot acceptance test.

The relationship:

| | [[skill-creator]] (this) | [[self-improving-skills]] |
|---|---|---|
| **Loop shape** | Single run | Convergent autonomous loop |
| **Eval format** | Plain-language criteria + blind A/B | Binary criteria (pass/fail per criterion) |
| **Output** | Pass/fail signal | Improved skill |
| **Time horizon** | One run | Overnight — N iterations |
| **Use case** | "Does my skill work?" | "Can my skill be made to work better?" |

Skill Creator + Self-Improving Skills form the **complete pre-ship pipeline**:
1. Skill Creator runs the acceptance test (does the skill change behavior in the right direction?)
2. Self-Improving Skills converges the skill against binary criteria (until plateau or budget exhausted)
3. Shippable skill emerges with both acceptance + optimization evidence

Self-improving skills is **the closed-loop extension** of Skill Creator's three core capabilities — particularly extending blind A/B testing into a **convergent revision loop**. Likely path: Anthropic ships an integrated `/skill-improve` command that wraps both into one workflow.

## Front-end: [[grill-me-skill]] — front-load context to cut the iteration count (2026-06-04)

[[nate-herk]]'s *The Skill That 10x'd My Claude Code Projects* ([[youtube-digest-apify-2026-06-05]] #2, 36.8K views) ships the **front-loading-context complement** to Skill Creator's evaluation loop. → New concept: [[grill-me-skill]].

Where Skill Creator iterates a skill against evals **after** you author it, the [[grill-me-skill]] reduces the iteration count by getting the context right **before** you author it — a skill that *"relentlessly interviews you about a process and writes it back to a knowledge doc."* Nate's claim: front-loading context this way gets a skill to **~90% on the first try instead of grinding through 30 iterations.**

The two are the bookends of the authoring pipeline:

| Stage | Tool | Question |
|---|---|---|
| **Before authoring** | **[[grill-me-skill]]** | Have I extracted the context this skill needs? |
| Authoring | [[claude-skills]] practices | Is the skill well-written? |
| **Acceptance (single-shot)** | **[[skill-creator]] (this)** | Does the skill change behavior in the right direction? |
| Optimization (closed-loop) | [[self-improving-skills]] | Can it be converged to as-good-as-possible? |

Extraction up front (grill-me) and iteration after (Skill Creator / self-improving) are two ways to reach the same quality bar — the former trades a focused interview for fewer build-test-fix cycles.

## Sibling: generation-first meta-skill — [[skill-forge]] (2026-06-30)

[[alek]]'s *The BEST Claude Skill You've Never Seen Before* ([[youtube-digest-apify-2026-07-01]] #1, 4.3K views) surfaces **[[skill-forge]]** — a meta-skill pitched as *"the only skill you really need"* because it **builds any other skill from a described workflow**. It's Skill Creator's closest sibling (both operate *on* skills) but sits at the **opposite end of the pipeline**:

| | [[skill-forge]] ([[alek]]) | [[skill-creator]] (this) |
|---|---|---|
| Primary job | **Generate / scaffold** a skill from a workflow | **Evaluate / optimize** an existing skill |
| Pipeline stage | Author | Acceptance test |
| Positioning | "The one skill you need" | "The tool that proves your skill works" |

They're complementary, not competing: **generate with Skill Forge → prove with Skill Creator → converge with [[self-improving-skills]]**. Skill Forge also carries a **"one skill, not a curated shelf"** counter-thesis to the [[claude-skills]] curation debate — worth watching against Skill Creator's acceptance-test discipline, since on-demand-forged skills still need to pass an eval. → See [[skill-forge]].

## Strategic implications

### For [[anthropic]]
- Continues the **infrastructure-for-AI-builders** pattern — Skill Creator, [[anthropic]]'s Mythos (code review), and [[anthropic]]'s Skill Creator are all tools built for people building on the platform
- Locks in [[claude-skills]] as the canonical skill format — a meta-skill that benchmarks competing skill formats would be weird; Anthropic shipping the eval tool implicitly endorses its own format
- Creates a **quality floor** for the [[claude-skills]] marketplace — if Skill Creator becomes the standard acceptance test, low-quality marketplace skills face an explicit shame metric

### For [[claude-skills]] marketplace
- The [[dubibubii]] "500K skills, 95% useless" claim becomes testable — run Skill Creator against the marketplace, see what passes
- Creates a **distribution advantage** for authors who publish eval results alongside their skills — "Skill X passes Skill Creator eval Y at 0.83 vs unskilled 0.12" becomes a marketing claim

### For 3Ps
- **Acceptance criteria become standard** — every client-deliverable skill ships with a Skill Creator eval pass
- **The description field is a billable artifact** — description optimization is non-obvious; clients can't replicate it without the tool, which makes it a deliverable in its own right
- **The two-types split is a scoping framework** — when scoping a client engagement, label proposed skills as capability-uplift or encoded-preference up front (this sets the eval target, acceptance criteria, and demo plan)

## First-party confirmation — "write descriptions for the model" + "stop railroading" ([[skill-authoring-lessons]] 2026-06-06)

Anthropic's *Lessons from building Claude Skills* article (surfaced via [[brock-mesarich]], → [[skill-authoring-lessons]]) **first-party-validates Skill Creator's core mechanic**: it names the **`description` field as the highest-leverage field, written for the model not humans** — exactly the field Skill Creator's automated **description-field optimization** tunes. The article's **"stop railroading Claude"** lesson is the authoring-time complement to Skill Creator's eval-time discipline: don't over-constrain a capable model with rigid scripts; let the eval loop confirm the looser skill still passes. The pairing is clean — [[skill-authoring-lessons]] is the **human-readable how-to-author** companion to Skill Creator's **mechanical how-to-evaluate**.

## Beginner on-ramp — build-from-scratch ([[skill-leap-ai]] 2026-06-29)

[[skill-leap-ai]]'s *Ultimate Guide To Claude Skills* (29.5K views, [[youtube-digest-apify-2026-07-05]] #3) positions Skill Creator as the **non-technical on-ramp** — *"how to build a skill from scratch with the Claude skill creator"* — rather than an eval tool bolted on after hand-authoring. This is a distinct framing from [[chase-ai]]'s eval-mechanics walkthrough: for a beginner, Skill Creator is the *first* tool you touch (scaffold → build), not the last (test → optimize). Named example builds: a writing-style skill, a deep-research auditor, a CSV dashboard, a content engine, an on-brand presentation maker. The video also carries a **skill-safety / provenance** caveat (build your own + read the instructions before running internet skills) — the consumer-facing complement to Skill Creator's acceptance-test discipline. → See [[skill-leap-ai]].

## Open questions

- **External-tool dependencies** — Skill Creator's eval architecture is presumably designed for self-contained skills. How does it handle skills that depend on MCP tools, sub-agents, or [[printing-press]] CLIs? Test fixtures or stubs?
- **Multi-turn skills** — most evals demonstrated are single-turn. Skills used in long conversations may need a different eval shape.
- **Eval cost** — running blind A/B across many test cases uses Claude tokens. Is there budgeting / sampling guidance?
- **Cross-model eval** — [[code-with-beto]] #6's authoring guidance is "test different models." Does Skill Creator support cross-model eval, or is it Claude-only?
- **Description optimization convergence** — how does Skill Creator avoid local optima in description-field tuning?
- **Anthropic's own quality bar** — Anthropic ships `superpowers`, `frontend-design`, `skill-creator` itself, etc. Are Anthropic's official skills publicly benchmarked via Skill Creator? Could become a sales motion: "look at our pass rates."
- **Codex parity** — does [[codex]] ship a Skill Creator equivalent? If [[claude-skills]] is cross-vendor at the format level, evaluation may not yet be.

## Why this matters for 3Ps

1. **Acceptance test for client deliverables** — every shipped skill gets a Skill Creator eval. Resolves "is the deliverable done?" deterministically.
2. **Eval-pass-rate as a marketing claim** — quoting pass rates in 3Ps content is a credibility lever the rest of the consulting market doesn't yet use.
3. **Two-types scoping framework** — capability vs preference labeling at scoping time saves design iterations downstream.
4. **Description optimization is sellable** — clients can't easily do this themselves; it's a concrete, narrow, billable deliverable.
5. **First-mover lever** — most of the AI-creator economy doesn't yet ship eval-backed skills; 3Ps doing so by default is a differentiation play with a ~6-month window before becoming table stakes.

## Related pages

- [[claude-skills]] — primary parent concept
- [[claude-code]] — substrate
- [[anthropic]] — vendor / publisher
- [[chase-ai]] — first-hand walkthrough source
- [[skill-systems]] — composition layer that consumes Skill-Creator-passed skills
- [[self-improving-skills]] — closed-loop optimization extension (Simon Scrapes 2026-05-23)
- [[skill-forge]] — generation-first sibling meta-skill (Alek 2026-06-30); scaffolds any skill from a workflow, the "author" half to this page's "acceptance-test" half
- [[grill-me-skill]] — front-loading-context front-end (Nate Herk 2026-06-04); extract context before authoring
- [[skill-authoring-lessons]] — Anthropic's first-party authoring playbook (2026-06-05); confirms description-for-the-model + don't-railroad
- [[plugins]] — taxonomy parent
- [[ai-consulting]] — practice that ships eval-backed skills as deliverables
- [[youtube-digest-apify-2026-05-11]] — primary citation
- [[youtube-digest-apify-2026-05-23]] — self-improving-skills extension
- [[youtube-digest-apify-2026-06-05]] — grill-me-skill front-loading-context front-end
- [[skill-leap-ai]] — beginner build-from-scratch on-ramp + skill-safety/provenance ([[youtube-digest-apify-2026-07-05]])
- [[code-with-beto]], [[ben-ai]] — fellow authoring-discipline voices
- [[karpathy-llm-wiki]] — autoresearch lineage inherited via self-improving-skills
