---
title: Claude Fable 5 (The Doing Got Cheap)
category: concept
summary: Anthropic's **Fable 5** — *"the biggest model in the world"* — read through [[nate-b-jones]]' *The Doing Got Cheap. Now What?* (30.4K views, 2026-06-23): the real story isn't the benchmarks, it's that **the bottleneck moved from what the model can do to what you can imagine handing it**; his core reframe is **task imagination replaces prompt engineering as the new core skill** — *"the doing is getting cheap and the deciding is not"* — when one model can carry a whole job, the scarce skill becomes seeing the work that's big enough to hand over; five resets Fable 5 forces, the "model managers" framing of job risk; the latest rung above [[opus-4-8]] and the model the same-batch [[sakana-fugu|Fugu Ultra]] claimed to match
tags: [claude-fable-5, fable-5, anthropic, nate-b-jones, nate-herk, task-imagination, prompt-engineering-obsolete, the-doing-got-cheap, model-managers, opus-4-8, claude-mythos, ai-question-method, software-abundance-pm, work-primitive, whole-job, frontier-model, six-habits, effort-levels, model-handoff, fable-hands-off-to-opus, harness-over-model, free-sample-phase, token-economics, karpathy-llm-wiki, wiki-as-substrate, connected-second-brain]
sources: 3
updated: 2026-07-04
---

# Claude Fable 5

## What it is

**Fable 5** is Anthropic's newest and largest frontier model — billed in [[nate-b-jones]]' coverage as *"the biggest model in the world."* It sits above [[opus-4-8]] in the lineage and is the model the same-batch [[sakana-fugu|Sakana Fugu Ultra]] announcement claimed to match (alongside [[claude-mythos|Mythos]]). Read here through Jones's *The Doing Got Cheap. Now What? | Claude Fable 5 Changes Work* (30.4K views, 2026-06-23, 18:11) in [[youtube-digest-apify-2026-06-24]].

## The thesis — the bottleneck moved

Jones's framing claim:

> *"The common story is that it's just a smarter, faster model — but the real question is whether you can even see the work that's finally big enough to hand it."*

The model story isn't the benchmark; it's that **the bottleneck moved from what the model can do to what you can imagine handing it.** When one model can carry a whole job end-to-end, capability stops being the constraint and **task imagination** becomes the binding one.

### Task imagination replaces prompt engineering

The headline reset (chapter 06:29, *Task imagination, the new core skill*): the scarce skill is no longer crafting prompts — it's **seeing the whole job that's now hand-over-able.** This is the direct successor to his own [[ai-question-method]] ("Opus 4.7 and GPT-5.5 made your prompting style obsolete" → senior-partner questioning); Fable 5 pushes the same arc one step further — past *how you ask* to *what you're even able to imagine delegating.*

> *"The doing is getting cheap and the deciding is not — the people who learn to hand over whole jobs are the ones who win back time."*

## The five resets (per the video)

1. Why AI has felt *smaller* than the headlines for years
2. **Task imagination replaces prompt engineering** as the core skill (06:29)
3. What changes when **one model can carry a whole job**
4. Where the real **job risk** falls — and where it doesn't (12:10, *AI, jobs, and model managers*)
5. (Cold-open framing, 00:00 → 02:00, *Bigger, not just smarter*)

The **"model managers"** framing (12:10) is the labor-market read: the durable role becomes managing the whole-job handovers, not doing the constituent tasks — the human moves up to deciding-and-reviewing.

## The operator read — six habits for prompting Fable 5 ([[nate-herk]], 2026-07-01)

Where Jones gives the strategic read, [[nate-herk]]'s *How Anthropic Engineers Actually Prompt Fable 5* ([[youtube-digest-apify-2026-07-02]] #3, 30.1K views, 10:44) is the **operator read** — the recurring Herk (knobs/operations) vs Jones (thesis/strategy) lens split, now on Fable 5.

> *"Fable 5 is back, and it's the strongest model I've used. It's also **expensive and won't stay free** on your Claude plan for long, so this video breaks down the **six habits** I'm using to get the most out of it **without burning tokens**."*

The six rules are gated to the video (chapters Rule 1→6 at 2:25 / 3:33 / 5:01 / 6:44 / 7:42 / 8:29), but the description names the throughline: *"giving it the right context, to matching effort levels, to knowing when it quietly hands your task off to Opus."*

### Fable 5 hands off to Opus (chapter 9:22)

The load-bearing new fact: **Fable 5 quietly routes sub-tasks down to [[opus-4-8|Opus]]** ("When Fable Hands Off To Opus"). This is a **model-internal auto-router** — an orchestration layer *inside* a single Anthropic model — and confirms the **Fable-above-Opus lineage** from the vendor side. It's distinct from:
- **operator-controlled [[claude-subagents]]** (the human wires the delegates), and
- **[[sakana-fugu]]'s external cross-model router** (a separate product routing across Opus/GPT/Gemini).

Fable 5 does its own routing; the operator's job becomes *knowing when* the handoff happens (and what it costs), not wiring it.

> ⚠️ Contradiction: Nate Herk's habit **"match effort levels"** (applied here to Fable 5) restates the same effort-control posture that [[nate-b-jones]]'s testing found **unpredictable** on [[opus-4-8]] — the Vending-Bench **effort-level trap**, where `max` effort can make long-running work *worse*. Herk treats effort-matching as a clean lever; Jones treats the effort knob as unreliable and non-monotonic. Both reads are in the vault, now spanning Opus 4.8 *and* Fable 5. → See [[harness-over-model]] and the callout on [[opus-4-8]].

### Token-economics / free-window signal

*"Expensive and won't stay free on your Claude plan for long"* is a [[free-sample-phase]] datapoint: Fable 5 is currently accessible on the Claude plan, but Herk expects the free access to close — consistent with the substrate-economics retention pattern around [[opus-4-8]] and the Claude Code rate-limit moves.

## Fable 5 as the reasoning layer over an LLM wiki ([[nate-herk]], 2026-07-03)

In *Fable 5 + Karpathy's LLM Wiki is Basically Cheating* (23.1K views, [[sources/youtube-digest-apify-2026-07-04]] #1), [[nate-herk]] pairs Fable 5 with a [[karpathy-llm-wiki|Karpathy LLM wiki]] built in ~5 minutes on [[claude-code|Claude Code]] + Obsidian. The *"basically cheating"* claim: pointing Anthropic's largest model at a **compiled, cross-linked knowledge base** lets it *"reason over"* the whole corpus at once — *"a connected second brain that my AI OS can actually reason over."* Chapter 1:13 (*What Fable Does With the Data*) is the load-bearing beat.

This is the **"doing got cheap" thesis applied to your own knowledge**: the scarce input becomes the *quality of the compiled substrate* you hand the model, not the prompt. It's the first time the vault has a creator explicitly pairing the **frontier model + LLM-wiki substrate** as one combined move (vs treating Fable 5 as a standalone chat model). See [[karpathy-llm-wiki]] for the build details (multiple topic-scoped wikis, flat-vs-structured schema fork, routing rules).

## Where it sits in the vault

- **Successor to [[opus-4-8]]'s "don't run it like 4.7"** — where [[nate-herk]] framed 4.8 as a workflow re-tuning and Jones countered with [[harness-over-model]] (it's a checkpoint), Fable 5 is framed by Jones as a *genuine step-change* — but on the **dimension of job-size you can hand over**, not raw score. Consistent with his standing skepticism of benchmark-first reads.
- **The capability floor under [[software-abundance-pm]]** — his 25th framework argued "the artifact arrives before the request" and PM becomes market-judgment; Fable 5 is the model that makes whole-job handover real, deepening that thesis.
- **Extends the [[work-primitive]] / [[ai-question-method]] line** — access/meaning/authority + senior-partner questioning + now *task imagination* form a three-stage progression of the human's job as the model climbs.
- **The same-batch Fugu foil** — [[sakana-fugu|Fugu Ultra]] claimed to match Fable; [[nate-herk]]'s 38-task test ([[sakana-fugu]]) is the empirical companion to Jones's interpretive read.

## Why it matters for 3Ps

- **"Task imagination" is a teachable, billable skill** — most operators are still optimizing prompts; the next consulting wedge is helping clients *find the whole jobs worth handing over.*
- **"The deciding is not getting cheap"** is the durable-value message for any client deck — judgment/decision work is where human time relocates, not disappears.
- **A diagnostic exercise** — "list the jobs you could hand over whole if the model never made a careless mistake" surfaces the latent automation backlog before any tooling is bought.

## Open questions

- **Fable 5's actual capabilities / benchmarks** — Jones deliberately downplays them; the spec is gated to his Substack (*Work Spec + Benchmarks*).
- **Relationship to [[claude-mythos|Mythos]]** — both are post-Opus-4.8 Anthropic frontier names; how the Fable / Mythos lineage splits is unresolved (see [[claude-mythos]]).
- **Pricing / availability** — undisclosed in the digest.

## Used in

- [[youtube-digest-apify-2026-06-24]] — vault entry point (Nate B Jones #11)
- [[youtube-digest-apify-2026-07-02]] — operator read + Opus handoff ([[nate-herk]] #3, 30.1K)
- [[nate-b-jones]] — strategic interpreter (task-imagination read)
- [[nate-herk]] — operator interpreter (six prompting habits)
- [[sources/youtube-digest-apify-2026-07-03]] — [[nate-b-jones]]' [[model-routing]] picker reserves Fable for *"Fable-style problems that need the strongest model"* (the hardest 20%)
- [[sources/youtube-digest-apify-2026-07-04]] — [[nate-herk]] pairs Fable 5 with a Karpathy LLM wiki as the reasoning layer over a connected second brain (#1, 23.1K)

## Related

- [[opus-4-8]] — the prior rung; reframed as a checkpoint by the same creator
- [[claude-mythos]] — sibling post-4.8 Anthropic frontier name
- [[sakana-fugu]] — same-batch orchestrator that claimed to match Fable
- [[ai-question-method]] — the prompting-obsolete predecessor; task imagination is its successor
- [[software-abundance-pm]] — the artifact-before-request framework Fable 5 deepens
- [[work-primitive]] — access/meaning/authority; the job-decomposition substrate
- [[anthropic]] — vendor
