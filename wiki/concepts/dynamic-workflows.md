---
title: Dynamic Workflows (Claude Code Orchestration Capstone)
category: concept
summary: The [[opus-4-8]]-era [[claude-code]] primitive that scripts how multiple subagents run (deterministic fan-out / pipeline / verify) — the **top rung of the orchestration complexity ladder** above skills → subagents → agent teams. First covered in this vault via [[nate-herk]]'s *Claude Code Dynamic Workflows Clearly Explained* (57.6K views, 2026-05-30, 16:31). Core disambiguations: the **complexity ladder** (skills → subagents → teams → workflows), **/goal vs workflow = depth vs width** (one deep long-running agent vs many fanned-out agents synthesized), and the **token-cost warning** (*"one prompt burned through half my $200 monthly plan"*) — workflows are the most expensive primitive, so a single gate question decides whether a job is even worth one. First vault surfacing of **ultracode mode** and **/deep-research**
tags: [dynamic-workflows, claude-code, opus-4-8, orchestration, complexity-ladder, skills, subagents, agent-teams, goal-command, depth-vs-width, token-cost, ultracode, deep-research, nate-herk, fan-out, pipeline, multi-agent, harness-over-model, nate-b-jones, workflows-command, agent-design]
sources: 2
updated: 2026-06-05
---

# Dynamic Workflows

## What it is

**Dynamic workflows** are a [[claude-code]] primitive added in the [[opus-4-8]] era — a **deterministic orchestration layer** that scripts how multiple subagents run (fan-out, pipeline through stages, verify, synthesize) rather than letting the model decide orchestration on the fly. They sit at the **top of the orchestration complexity ladder**: the most powerful and the most token-expensive way to coordinate agentic work.

First covered in this vault via [[nate-herk]]'s *Claude Code Dynamic Workflows Clearly Explained* ([[youtube-digest-apify-2026-06-02]] #3, 57.6K views, 2026-05-30, 16:31).

**The framing problem Nate sets up**: *"Opus 4.8 added dynamic workflows to Claude Code, and they look a lot like skills, subagents, agent teams, and the /goal feature, so it's easy to get confused about when you'd actually reach for one."* The whole video is **disambiguation** — when do you reach for a workflow vs everything else on the ladder.

## The complexity ladder (chapter 5:47)

| Rung | Primitive | What it adds | Token cost |
|---|---|---|---|
| 1 | **[[claude-skills]]** | Reusable procedural knowledge, one agent | Lowest |
| 2 | **Subagents** | Delegated specialized agents | Low–moderate |
| 3 | **Agent teams** | Multiple coordinating agents | Moderate–high |
| 4 | **Dynamic workflows** | Scripted, deterministic multi-agent orchestration (fan-out / pipeline / verify) | **Highest** |

The strategic lesson: **don't climb to the top rung by default.** Each rung up adds orchestration power *and* token cost. Most jobs are solved cheaper and more reliably lower on the ladder. A dynamic workflow is the right tool only when the job genuinely needs many agents coordinated deterministically.

## /goal vs workflow = depth vs width (chapter 8:39)

The clearest disambiguation in the video — the two long-running primitives differ on **shape**:

| Primitive | Shape | Use when |
|---|---|---|
| **`/goal`** | **Depth** — one long-running agent pursuing a single goal over many cycles | The work is a deep, sequential pursuit (keep going until X is done) |
| **Dynamic workflow** | **Width** — many agents fanned out and synthesized | The work decomposes into parallel pieces that combine into one answer |

`/goal` goes *deep on one thread*; a workflow goes *wide across many*. This is the question to ask first: is my job depth-shaped or width-shaped?

## The token-cost question (chapter 10:13)

The cautionary core of the video: **workflows are the most expensive primitive.** Nate's anchor: *"one prompt burned through half my $200 monthly plan."* Because a workflow can spawn dozens of agents, a single invocation can consume a large fraction of a session/plan budget.

This makes dynamic workflows the substrate-economics frontier of [[claude-code]] — the operator-side discipline of [[prompt-caching]] (per-session economy), [[agent-metering]] (renewal-side pricing), and [[free-sample-phase]] (macro substrate war) now extends to **"is this job worth a workflow at all?"**

## When you actually need it (chapter 11:18)

Nate's gate: a **simple question asked before deciding if a job is even worth a workflow.** The framing inverts the default — instead of "could a workflow do this?" (almost anything could), the question is "does this job *require* the width + determinism a workflow buys, enough to justify the token cost?" If not, drop down the ladder.

## Hidden modes: ultracode + /deep-research

- **Ultracode mode** (chapter 14:08) — **first vault surfacing.** A higher-power Claude Code mode flagged as a session-limit risk; Nate covers it so viewers "don't accidentally torch your session limit." (Exact mechanics gated to transcript — appears to escalate effort/orchestration aggressiveness.)
- **/deep-research** (wrap, 15:25) — **first vault surfacing.** A research-oriented mode in the same high-cost category. (Likely the Claude Code analog of the deep-research harness pattern; specifics gated to transcript.)

> ⚠️ The exact API/UX of dynamic workflows, `ultracode`, and `/deep-research` — and the precise token-cost math — are **gated to the video transcript / Anthropic docs** and are not in the digest. Pull the transcript or release docs to fill these in.

## Strategic significance

1. **The orchestration-tier capstone above [[claude-code-levels]] Level 5** — Nate Herk's own five-level mastery framework topped out at "five parallel sessions while they sleep" (Agent View + `/goal` + Routines). Dynamic workflows are the *deterministic-scripting* layer above ad-hoc parallel sessions — a plausible **Level 6**.
2. **Confirms [[nate-herk]]'s mainstream-news-interpreter role for [[opus-4-8]]** — his second consecutive 4.8-centered video (after *Opus 4.8 Just Dropped*, 101K). First model adoption, then model-enabled primitive. Same fast release-barometer cadence as his Karpathy-hire (105K) and session-limits (87.7K) coverage.
3. **Names the disambiguation the whole ecosystem needs** — skills / subagents / teams / `/goal` / workflows now all coexist in Claude Code; the *which-do-I-reach-for* question is the new operator skill. The complexity ladder + depth-vs-width are reusable decision tools.
4. **The token-cost warning is a client guardrail** — "one prompt = half my plan" is the headline risk for any 3Ps engagement deploying workflows. The gate question ("is this worth a workflow?") belongs in any onboarding rubric.

## Why it matters for 3Ps

- **Decision framework for client work** — the complexity ladder + depth-vs-width + the gate question form a ready-made "when to use which Claude Code primitive" deliverable. Maps cleanly onto [[claude-code-levels]] and [[deployment-framework]] (where it runs) — this is *how complex the orchestration should be*.
- **Cost-control talking point** — workflows can blow a budget; the discipline of staying low on the ladder unless width+determinism are required is a billable cost-optimization insight (sibling to [[prompt-caching]] habits).
- **Capability frontier to teach** — dynamic workflows + `ultracode` + `/deep-research` are the newest, least-documented primitives; "Claude Code orchestration for operators" content has runway.

## Open questions

- **What is the actual scripting interface?** — is a dynamic workflow authored as a file (like a skill), defined inline, or generated by the model? How deterministic is "deterministic"?
- **How does it relate to agent teams?** — is a workflow a *scripted* agent team, or a distinct mechanism? Where exactly is the boundary on the ladder?
- **`ultracode` mechanics** — what does it change (effort level? auto-workflow authoring? orchestration aggressiveness)? How does it interact with [[opus-4-8]]'s effort levels and `/fast`?
- **`/deep-research`** — is this the Claude Code build of the deep-research harness? What does it cost relative to a workflow?
- **The token-cost math** — what configuration actually burned half a $200 plan in one prompt? Is that typical or a worst case?

## "/workflows reveals agent design" ([[nate-b-jones]] in [[youtube-digest-apify-2026-06-05]])

[[nate-b-jones]]'s *Opus 4.8 Scored 81. Your Workflow Doesn't Care.* (34.3K views, 2026-06-03) names the `/workflows` command as a **window into agent architecture**, not just a feature — *"what the /workflows command reveals about agent design."* In his [[harness-over-model]] framing, the orchestration layer dynamic workflows expose is precisely the **harness** that he argues matters more than the model score. Dynamic workflows are therefore evidence for his thesis: the place where agent design actually lives is the deterministic orchestration scaffold, not the underlying model. → See [[harness-over-model]].

This complements [[nate-herk]]'s how-to coverage (the primary citation below) with the **why-it-matters-strategically** read: workflows aren't just a new tool to learn, they're where the harness-as-strategic-primitive becomes visible.

## Related pages

- [[claude-code]] — the substrate that hosts dynamic workflows
- [[opus-4-8]] — the model generation that added them
- [[harness-over-model]] — "/workflows reveals agent design"; the harness is the strategic primitive
- [[claude-skills]] — rung 1 of the complexity ladder
- [[claude-code-levels]] — dynamic workflows sit above Level 5 (a plausible Level 6)
- [[prompt-caching]], [[agent-metering]], [[free-sample-phase]] — the substrate-economics context for the token-cost warning
- [[nate-herk]] — primary author; mainstream-news interpreter for Claude releases
- [[deployment-framework]] — *where* automations run (companion to *how complex* the orchestration is)
- [[nate-b-jones]] — "/workflows reveals agent design" ([[harness-over-model]])
- [[youtube-digest-apify-2026-06-02]] — primary citation
- [[youtube-digest-apify-2026-06-05]] — secondary citation ([[nate-b-jones]]: /workflows reveals agent design)

## Used in

- [[youtube-digest-apify-2026-06-02]] — primary citation ([[nate-herk]] #3)
- [[claude-code]] — new orchestration primitive
- [[opus-4-8]] — model-enabled capability
- [[nate-herk]] — primary author
