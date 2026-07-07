---
title: Fable Mode Skill (Make Opus Think Like Fable)
category: concept
summary: [[nate-herk]]'s [[claude-skills|Claude skill]] (*How I Make Opus Think Like Fable (5 easy steps)*, 20.2K views, 2026-07-07) that **transplants [[claude-fable-5|Fable 5]]'s process into [[opus-4-8|Opus 4.8]]** — because *"Fable is going back behind subscriptions,"* Nate keeps its **process, not its intelligence**: reverse-engineer a **leaked Fable system prompt** into a skill that makes Opus *"feel elevated,"* drive **effort levels** deliberately, and wire a **[[model-routing|model routing table]]** so cheaper models handle what they can; the thesis is the chapter-0 title **"the model isn't the moat"** — the operator-side capture of the vault's own-the-durable-layer cluster ([[harness-over-model]], [[context-wars]], [[model-routing]]); also a [[free-sample-phase]] datapoint (the Fable free window closing)
tags: [fable-mode-skill, nate-herk, claude-skills, claude-fable-5, fable-5, opus-4-8, leaked-system-prompt, effort-levels, model-routing, the-model-isnt-the-moat, harness-over-model, context-wars, free-sample-phase, process-not-intelligence, claude-code, prompt-transplant]
sources: 1
updated: 2026-07-07
---

# Fable Mode Skill

## What it is

A [[claude-skills|Claude skill]] built by [[nate-herk]] in *How I Make Opus Think Like Fable (5 easy steps)* ([[youtube-digest-apify-2026-07-07]] #4, 20.2K views, 2026-07-07, 9:59) that **makes [[opus-4-8|Opus 4.8]] behave like [[claude-fable-5|Fable 5]]**. The premise:

> *"Fable 5 is going back behind subscriptions at some point, so I've been focused on keeping its **process** instead of its **intelligence**."*

The skill is the vehicle for that capture: extract *the way Fable works* — reverse-engineered from a **leaked Fable system prompt** — into a reusable skill, so a cheaper, still-accessible model (Opus 4.8) *"feels elevated"* even after the frontier model's free access closes.

## The five steps (chapter map)

| Chapter | Step |
|---|---|
| **The Model Isn't the Moat** (0:00) | The thesis: process/harness is durable, model *access* is rented and revocable |
| **Turning Opus Into Fable** (1:15) | The goal state — Opus running Fable's process |
| **Leaked Fable System Prompt** (2:33) | The raw material the skill is reverse-engineered from |
| **Effort Levels** (3:18) | How to actually drive the effort knob deliberately |
| **Building the Fable Mode Skill** (4:25) | Packaging the extracted process as a [[claude-skills|Claude skill]] |
| **Model Routing Table** (7:30) | A simple table so cheaper models handle the work they're capable of → [[model-routing]] |

## The load-bearing move — capture *process* when *access* closes

The distinctive contribution vs the vault's other "the model is disappearing" responses:

- **[[model-routing]]** ([[nate-b-jones]]) — *route around* the model: send each job to the right tier, keep context portable.
- **[[karpathy-llm-wiki]] + [[claude-fable-5|Fable]]** ([[nate-herk]], 2026-07-03) — *pair* the model with a compiled knowledge substrate.
- **Fable Mode skill** (this page) — **transplant the vanishing model's behavior into a cheaper one** via a skill built from its leaked system prompt. It doesn't route or pair; it *clones the process*.

This is [[harness-over-model]] taken to its literal conclusion: if the harness (process, prompt, effort discipline) is what actually does the work, then you can lift a frontier model's harness off it and run that harness on a commodity model. *"The model isn't the moat"* is Nate's operator-phrasing of the same own-the-durable-layer thesis behind [[context-wars]] and [[model-routing]]'s *keep your context portable*.

## The effort-levels caveat (standing contradiction)

Nate again treats **effort levels** as a clean, deliberate lever (chapter 3:18) — consistent with his [[opus-4-8]] and Fable-5 six-habits coverage.

> ⚠️ Contradiction: [[nate-b-jones]]' testing found the effort knob **unpredictable and non-monotonic** on [[opus-4-8]] (the Vending-Bench *effort-level trap*, where `max` effort can make long-running work *worse*). Herk builds a skill around driving effort levels as if they're reliable; Jones treats them as a knob you can't trust. Both reads are in the vault — see [[harness-over-model]] and the callout on [[claude-fable-5]].

## Free-window signal

*"Fable going back behind subscriptions at some point"* is a [[free-sample-phase]] datapoint — the free access window closing, exactly the outcome Herk predicted in his six-habits video (*"won't stay free on your Claude plan for long,"* [[youtube-digest-apify-2026-07-02]]). The Fable Mode skill is his **hedge against the free window closing**: keep the process locally even when the model goes back behind the paywall.

## Why it matters for 3Ps

- **A packageable, billable artifact** — "we captured your best model's process into a skill so your cheaper daily-driver runs it" is a concrete deliverable, not a thesis.
- **Vendor-churn insurance** — the literal answer to "what happens when the model we standardized on disappears / gets priced up": you kept its process, not its access.
- **Teaches the durable-layer lesson concretely** — most operators chase model access; the skill demonstrates that *process is the transferable asset*.

## Open questions

- **How faithfully does a leaked-system-prompt transplant reproduce Fable's behavior on Opus?** A system prompt captures *instructions*, not *weights* — the ceiling of this technique is unclear.
- **Is the leaked Fable system prompt legitimate / stable?** Reverse-engineering from a leak is brittle if Anthropic rotates it.
- **How does the routing table interact with the skill** — does Fable Mode become one row in a broader [[model-routing]] table, or the default wrapper?
- **Does this survive a Fable API change** the way [[karpathy-llm-wiki]]-pairing (which is model-agnostic) would?

## Used in

- [[youtube-digest-apify-2026-07-07]] — vault entry point ([[nate-herk]] #4)

## Related

- [[nate-herk]] — author
- [[claude-fable-5]] — the model whose process is being captured
- [[opus-4-8]] — the model the process is transplanted *into*
- [[model-routing]] — the routing table step; the route-around sibling response
- [[harness-over-model]] — the thesis this literalizes (lift the harness off the model)
- [[context-wars]] — *"the model isn't the moat"* is its operator phrasing
- [[free-sample-phase]] — the closing free-window this hedges against
- [[claude-skills]] — the packaging unit
- [[karpathy-llm-wiki]] — the pair-with-a-substrate sibling response (also Nate Herk)
