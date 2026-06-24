---
title: Agent Loops (Loop Engineering)
category: concept
summary: [[nate-herk]]'s plain-English explainer of **loop engineering** (*Finally. Agent Loops Clearly Explained.*, 83.8K views, 2026-06-19) — an agent loop is **reason → act → observe → repeat**, and the load-bearing part is not the architecture but the **verification step + a "done" criteria the agent can actually check**; the deflationary thesis is *"loops are about getting you closer on the first try, not perfect output"* and *"you're not behind because you're not running five agents at once"*; three ways to build loops, demoed on thumbnail-scoring, a three.js plane, and an Abbey Road recreation; the mainstream-creator restatement of [[simon-scrapes]]' [[self-improving-skills]] overnight-convergence loop and the runtime cousin of [[nate-b-jones]]' [[harness-over-model]] thesis
tags: [agent-loops, loop-engineering, nate-herk, claude-code, reason-act-observe, verification, done-criteria, self-improving-skills, harness-over-model, dynamic-workflows, first-try, deflate-the-hype]
sources: 1
updated: 2026-06-24
---

# Agent Loops (Loop Engineering)

## Definition

From [[nate-herk]]'s *Finally. Agent Loops Clearly Explained.* (83.8K views — his highest-view explainer in the [[youtube-digest-apify-2026-06-24]] batch, 2026-06-19, 14:33). An **agent loop** is the basic control structure under all agentic work: **reason → act → observe → repeat.** "Loop engineering" is the discipline of shaping that cycle so the agent converges toward a goal instead of wandering.

His core move is **deflationary**: the hype frames loop engineering as something only "hardcore coders running fleets of agents around the clock" do. Nate's reframe — *"if you have been feeling behind because you are not running five agents at once, this one is for you"* — pulls the primitive down to a single, ordinary loop anyone can run.

## The load-bearing claim

> **The verification step matters more than the architecture.**

What makes a loop *work* is not the orchestration topology — it's a **"done" criteria the agent can actually check itself against** (chapter 10:42, *What Makes a Loop Work*). Without a checkable done-state, the loop has no gradient to climb; with one, even a simple loop gets meaningfully closer each pass.

The companion reframe (chapter 12:40, *Does This Apply to You?*): **loops are about getting you closer on the first try, not perfect output.** The value is compressing iteration count, not achieving autonomy.

## Chapter map

- 0:31 What Loop Engineering Means
- 2:23 How an Agent Loop Works (reason / act / observe / repeat)
- 5:29 **Three Ways to Build Loops**
- 6:13 Demo: Thumbnail Scoring
- 8:12 Demo: Three.js Plane
- 9:08 Demo: Abbey Road Recreation
- 10:42 **What Makes a Loop Work** (the done-criteria claim)
- 12:40 Does This Apply to You?

The three demos are deliberately non-coding-flavored (thumbnail scoring is a taste/marketing task), reinforcing his standing thesis that **the agentic mindset applies whether or not you write code**.

## Where it sits in the vault

- **The mainstream restatement of [[self-improving-skills]]** — [[simon-scrapes]]' autonomous overnight loop (binary criteria + convergence) is the same primitive at skill-authoring scale; Nate strips it to its core cycle for a general audience. Both descend from Karpathy's `autoresearch` lineage (see [[karpathy-llm-wiki]]).
- **The runtime cousin of [[harness-over-model]]** — [[nate-b-jones]] argues the harness, not the model, does the heavy lifting; the verification-as-the-real-work claim is the same instinct at the loop level.
- **Rung-zero of [[dynamic-workflows]]** — below subagents, teams, and scripted workflows sits the single loop. His own complexity ladder ([[claude-subagents]] → [[dynamic-workflows]]) builds up from exactly this.
- **The "done" criteria echoes [[ai-question-method]]'s "ask what good looks like"** — success criteria specified before generation, here specified so the *agent* (not the human) can check them.
- **Same-batch sibling to [[directing-agents]]** — Nate's other 06-24 video ("make the agent prove its work") is the human-direction side of the same verification discipline.

## Why it matters for 3Ps

- **A clean client-explainer primitive** — "reason/act/observe/repeat + a checkable done-state" is the simplest correct mental model for agentic work; usable verbatim in onboarding.
- **Verification-first is the billable discipline** — most operators over-invest in orchestration and under-invest in done-criteria; this names the correction.
- **The thumbnail-scoring demo is a portable pattern** — an LLM-as-judge loop over creative output, directly reusable in the vault's content + ads farms.

## Open questions

- What are the **three ways to build loops** (chapter 5:29)? Names gated to the video.
- How does he encode a "done" criteria in practice — a rubric file, a test, a judge prompt? Transcript would resolve.

## Used in

- [[youtube-digest-apify-2026-06-24]] — vault entry point (Nate Herk #2)
- [[nate-herk]] — author

## Related

- [[self-improving-skills]] — the skill-authoring-scale version of the same loop
- [[harness-over-model]] — verification/harness > model intelligence
- [[dynamic-workflows]] — the complexity ladder this sits beneath
- [[directing-agents]] — same-batch sibling; "make the agent prove its work"
- [[ai-question-method]] — "ask what good looks like" = the human-side of done-criteria
- [[claude-code]] — substrate
