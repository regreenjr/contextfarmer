---
title: Directing Agents (Stop Vibe Coding, Start Directing)
category: concept
summary: [[nate-herk]] + Cole's hour-long deep dive (*How to Build Effective Claude Code Agents in 2026*, 39.7K views, 2026-06-18) on **directing coding agents instead of prompting-and-praying** — the **planning + verification system** that separates real results from [[vibe-coding]]; *"make the agent prove its work"*; **you plan more than you build**; **the "dumb zone"** every model has where it starts missing obvious things; **chaining multiple agent sessions** so one big task doesn't fall apart halfway; treating **every bug as a permanent upgrade**; **harness engineering** as the frame — *"whether or not you write code, the mindset applies directly to using AI for real work"*; the agentic-engineering successor to [[vibe-coding]] and the human-direction side of [[agent-loops]]' verification thesis
tags: [directing-agents, nate-herk, cole, vibe-coding, agentic-engineering, planning, verification, prove-its-work, dumb-zone, session-chaining, harness-engineering, claude-code, agent-loops, claude-subagents, harness-over-model, execution-layer, bug-as-upgrade]
sources: 1
updated: 2026-06-24
---

# Directing Agents

## What it is

[[nate-herk]]'s longest video in the [[youtube-digest-apify-2026-06-24]] batch — *How to Build Effective Claude Code Agents in 2026* (39.7K views, 2026-06-18, **1:08:12**), a sit-down with **Cole**, who (with Nate) has *"logged thousands of hours working in tools like Claude Code."* The frame:

> *"How to actually **direct** your coding agents instead of just prompting and praying."*

The thesis applies past coding: *"whether or not you write code, the mindset applies directly to using AI for real work."*

## The system

### Stop vibe coding, start directing (7:41)

The pivot from [[vibe-coding]] (accept/reject suggestions, hope it works) to **direction** — a planning-and-verification discipline. This is the **agentic-engineering** maturation [[andrej-karpathy]] named, given an operator-grade walkthrough.

### Make the agent prove its work (13:17)

The verification half: don't trust output, **require evidence.** The human-direction counterpart to [[agent-loops]]' claim that the verification step (a checkable "done") is what makes a loop converge.

### You plan more than you build (19:46)

The planning half: the leverage is upstream. *"Why you plan more than you build"* — the build is cheap (cf. [[claude-fable-5]] "the doing got cheap"); the plan is where outcomes are decided.

### The dumb zone (27:01)

**Every model has a "dumb zone" where it starts missing obvious things.** A capability map, not a quality verdict — knowing *when* a model degrades lets you route around it (chain sessions, reset context, switch models). Sibling to [[harness-over-model]]'s "reasoning effort is unpredictable on 4.8."

### Session chaining + harness engineering (33:38)

**Chain multiple agent sessions** so one big task doesn't fall apart halfway through — the context-management discipline behind [[claude-subagents]] (keep the main context clean) and [[dynamic-workflows]]. Framed under **harness engineering**: the system around the model is where reliability is built.

### Security + every bug a permanent upgrade

Cole's security mindset, and the principle that **every bug fixed becomes a permanent upgrade** — the individual-discipline version of [[execution-layer]]'s PR-back loop ("every correction becomes a permanent upgrade across the whole company").

## Where it sits in the vault

- **The agentic-engineering successor to [[vibe-coding]]** — gives Karpathy's "vibe coding → agentic engineering" arc a concrete operator playbook (plan / prove / chain / harness).
- **The human-direction side of [[agent-loops]]** — Nate's same-batch loop video is the *mechanism* (reason/act/observe/repeat + done-criteria); this is the *operator posture* (direct, don't prompt-and-pray). Together they're his 06-24 "how to actually run agents" pair.
- **Lands on [[harness-over-model]]** — "harness engineering" + the "dumb zone" + session chaining all say the system around the model matters more than the model — [[nate-herk]] converging again with [[nate-b-jones]]' thesis (as he does in the same batch via [[glm]]).
- **"Every bug a permanent upgrade" = [[execution-layer]] at individual scale** — the PR-back-loop compounding principle, applied to one operator's practice rather than a team marketplace.

## Why it matters for 3Ps

- **The plan/prove/chain triad is the core operator curriculum** — directly teachable; the difference between "vibe coding" clients and ones who get reliable output.
- **"The dumb zone" is a portable diagnostic** — naming where a model degrades is exactly the kind of hard-won operator knowledge a 3Ps engagement encodes into routing rules (which model, which effort, when to reset).
- **Mindset-applies-without-coding** keeps the audience broad — the planning/verification discipline is sellable to non-technical operators, the vault's core persona.

## Open questions

- **Who is Cole?** The digest gives only a first name and "thousands of hours in Claude Code" — likely a known AI-coding creator; identity unconfirmed, so no dedicated entity page yet.
- **The specific planning/verification artifacts** — what files/prompts encode "prove its work" and the plan? Gated to the hour-long video.
- **How is the "dumb zone" detected** in practice — a heuristic, a benchmark, a feel? Unresolved.

## Used in

- [[youtube-digest-apify-2026-06-24]] — vault entry point (Nate Herk #1)
- [[nate-herk]] — co-host / author

## Related

- [[vibe-coding]] — the predecessor mode this matures past
- [[agent-loops]] — same-batch sibling; the loop mechanism behind "prove its work"
- [[harness-over-model]] — "harness engineering" + the dumb zone land here
- [[claude-subagents]], [[dynamic-workflows]] — session chaining / context management
- [[execution-layer]] — "every bug a permanent upgrade" = the PR-back loop at team scale
- [[claude-code]] — substrate
