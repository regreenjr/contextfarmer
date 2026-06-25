---
title: Loop of Loops (Agents as Loop Managers)
category: concept
summary: [[nate-b-jones]]' **33rd named framework** (*I Stopped Prompting AI One Task At A Time. This Works Better.*, 22.2K views, 2026-06-24) — AI agents get useful when you **stop prompting one task at a time and start building loops**; a **loop** is *"a recurring job that remembers, notices what changed, and stops where your judgment matters"*, a **loop of loops** is the orchestrator that composes sub-loops which notice each other and hand off what changed (the *school-trip* example), and **agents are "loop managers"**; the discipline is **spotting which recurring jobs to hand to a loop, giving each clear boundaries, and deciding where the loop stops and asks for you**; the consumer/life-admin demand-side complement to [[nate-herk]]'s runtime [[agent-loops]] and the orchestration cousin of [[anticipation-gap]] (when to act unprompted) + [[agent-ownership]] (who owns the running agent)
tags: [loop-of-loops, nate-b-jones, loops, recurring-jobs, agents-as-loop-managers, anticipation-gap, agent-loops, agent-ownership, life-admin, stop-where-judgment-matters, hand-off-what-changed, prompt-vs-loop, harness-over-model]
sources: 1
updated: 2026-06-25
---

# Loop of Loops (Agents as Loop Managers)

## Definition

From [[nate-b-jones]]' *I Stopped Prompting AI One Task At A Time. This Works Better.* (22.2K views, 2026-06-24, 15:38) — his **33rd named framework**. The thesis: *"AI agents get useful when you stop prompting one task at a time and start building loops."*

- **A loop** = *"a recurring job that remembers, notices what changed, and stops where your judgment matters."* Three load-bearing properties: it **persists state** (remembers across runs), it is **change-driven** (notices what changed rather than re-running blind), and it has a **stop condition tied to human judgment**.
- **A loop of loops** = the orchestrator above several loops. Sub-loops **notice each other and hand off what changed**; the loop-of-loops handles a multi-part recurring job end to end (the canonical demo is **the school trip**, chapter 3:03).
- **Agents are "loop managers"** (chapter 2:17) — the right mental model for an agent is not "a thing that does one task" but "a thing that runs and supervises recurring loops."

The reframe in one line: *"the common story is that better prompting is the path to better AI — but the real question is which recurring jobs you can hand to a loop, and where that loop should stop."*

## The three-level ladder

> **prompt → loop → loop of loops** (chapter 1:31)

| Level | What it is | Unit of work |
|---|---|---|
| **Prompt** | A one-off task you trigger by hand | One task, no memory |
| **Loop** | A recurring job that remembers + notices change + stops for judgment | One recurring job |
| **Loop of loops** | An orchestrator whose sub-loops hand off what changed | A whole area of your life/work |

The argument is that most people are stuck at the **prompt** rung (prompting one task at a time) and that the leverage lives one or two rungs up.

## Why apps left the hard part to you

Chapter 4:06 (*Why apps left the hard part to you*) is the structural claim: conventional apps automate the easy, legible step and **push the recurring, judgment-laden orchestration back onto the human**. The week *"feels heavier than it should"* (chapter 0:00) precisely because you are personally acting as the loop-of-loops manager for dozens of recurring jobs. Handing those loops to an agent is what lifts the mental load.

## The discipline (where a loop should stop)

The framework is not "automate everything." Its guardrail is explicit: **loops only lift real load if you give each one clear boundaries and let it stop where your judgment still matters.** Spotting your **first** loop (chapter 5:04, *Spotting the loops in your own life*) and starting simple — **sales and research loops** (6:33), then the **boring loops** like kids' logistics (8:57) — is the on-ramp. The stop condition is the safety mechanism: a loop that never stops to ask is the failure mode.

## Chapter map

- 0:00 Why a week feels heavier than it should
- 1:31 **Prompt vs loop vs loop of loops**
- 2:17 **Agents are loop managers**
- 3:03 A loop of loops handles the school trip
- 4:06 Why apps left the hard part to you
- 5:04 Spotting the loops in your own life
- 6:33 Starting simple with sales and research loops
- 8:57 The boring loops: kids' logistics (…)

(Full post + questionnaire gated behind his Substack — `natesnewsletter.substack.com`.)

## Where it sits in the vault

- **Demand-side complement to [[agent-loops]]** — [[nate-herk]]'s same-month *Agent Loops Clearly Explained* names the **runtime control structure** (reason → act → observe → repeat + a checkable "done"); Jones names the **portfolio of life/work loops** an agent should manage and *where they stop for you*. Herk = how a single loop runs; Jones = which loops to build and how they compose. Two creators, two halves of the same "loops, not prompts" turn.
- **Orchestration cousin of [[anticipation-gap]]** — "where a loop should stop and ask for you" is exactly his earlier permission-ladder question (Read → Suggest → Draft → Act-with-confirmation → Autonomous). The loop-of-loops is the anticipation-gap framework applied to **recurring** jobs.
- **Pairs with [[agent-ownership]]** (his 32nd framework, same week) — agent-ownership names the human who **owns** a running agent; loop-of-loops names **what the agent does** (manages loops) and where it hands control back. Own the loop, name the owner.
- **A runtime instance of [[harness-over-model]]** — the leverage is in the loop structure (memory + change-detection + stop condition), not raw model intelligence. Same instinct as his harness thesis.
- **The "stops where your judgment matters" line echoes [[portable-judgment]]** — judgment is the durable human residue the loop is built around, not the thing it replaces.

## Why it matters for 3Ps

- **A client-legible automation ladder** — "prompt → loop → loop of loops" is a cleaner sell than "let's do AI"; it tells an operator exactly which rung they're on and what the next one is.
- **"Which recurring jobs?" is a billable discovery exercise** — the loop-spotting audit (chapter 5:04) is a one-session consulting deliverable, the recurring-work cousin of [[nate-b-jones]]' T/C/L/D week-tagging audit.
- **Stop-conditions are the safety story** — "where the loop stops and asks for you" is the governance answer buyers need before they trust an always-on agent; pairs with [[agent-security]]'s action-risk classes.

## Open questions

- What is the **questionnaire** in the gated Substack post — a structured loop-spotting worksheet? (Likely the productized artifact.)
- How does a loop *notice what changed* in practice — polling, event triggers, a diff against remembered state? Transcript/post would resolve.
- How does this relate to his [[deployment-framework|deployment]] surfaces (`/loop`, Routines, external cron) — is a "loop" here always a scheduled job, or any stateful recurring agent?

## Used in

- [[youtube-digest-apify-2026-06-25]] — vault entry point (Nate B Jones #2)
- [[nate-b-jones]] — author (33rd named framework)

## Related

- [[agent-loops]] — [[nate-herk]]'s runtime reason→act→observe→repeat loop (the how-one-loop-runs half)
- [[anticipation-gap]] — "when should the agent act unprompted" + the permission ladder
- [[agent-ownership]] — who owns the running agent (same-week sibling framework)
- [[harness-over-model]] — the leverage is the loop structure, not the model
- [[portable-judgment]] — the judgment the loop stops to protect
- [[deployment-framework]] — where loops actually run (`/loop` / Routines / external)
- [[claude-code]] — substrate
