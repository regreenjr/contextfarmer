---
title: Claude Subagents (Cheap Specialist Delegation)
category: concept
summary: The [[claude-code]] primitive that delegates work to **cheap specialist agents** while one smart model runs the show — keeping the main context clean and saving money. First given dedicated coverage in this vault via [[nate-herk]]'s *How to Build Claude Subagents Better Than 99% of People* (14.5K views, 2026-06-09, 26:42). Core teaching: a subagent is a **scoped delegate with its own context window**, invoked automatically off its **description** (progressive disclosure); **built-in vs custom** agents; **Skills vs Subagents** (knowledge unit vs worker unit); **project vs global** scope; **subagents as specialists** + **read-only / cheaper-model** assignment for cost control; and a **when-to-use-one** gate. Rung 2 of the [[dynamic-workflows]] complexity ladder (skills → **subagents** → teams → workflows)
tags: [claude-subagents, subagents, claude-code, nate-herk, progressive-disclosure, context-management, specialist-agents, read-only, cheaper-model, skills-vs-subagents, project-vs-global, complexity-ladder, dynamic-workflows, multi-agent, agent-design, cost-control, opus-4-8]
sources: 1
updated: 2026-06-09
---

# Claude Subagents

## What it is

**Subagents** are a [[claude-code]] primitive: scoped delegate agents that the main session spawns to do a bounded piece of work, each with **its own context window**. The pitch [[nate-herk]] lands in *How to Build Claude Subagents Better Than 99% of People* ([[youtube-digest-apify-2026-06-09]] #1, 14.5K views, 2026-06-09, 26:42): *"delegate work to a team of cheap specialist agents while one smart model runs the show, saving you money and getting better results."*

His framing is that **most people barely scratch the surface** of subagents even though they're "one of the most powerful features in Claude Code." The video is a build-from-scratch explainer: what a subagent is, when you actually need one (and when you don't), and how to build custom agents that get invoked automatically.

This is the **first dedicated subagents page** in the vault. Subagents had appeared only as **rung 2** of [[dynamic-workflows]]' complexity ladder (skills → subagents → teams → workflows) and as a line item in [[claude-code]]'s primitive list. Nate's video promotes the rung to its own subject.

## The two jobs a subagent does (chapters 1:24, 20:38)

1. **Keeps the main context clean** — the subagent's work (file reads, search, intermediate reasoning) happens in *its* context window, not the orchestrator's. The smart "manager" model never has to hold the mess; it gets back only the result. This is the context-hygiene argument — the same "one source of truth / don't pollute the canvas" instinct behind [[ai-operating-system]]'s "context is king" and [[project-room-workflow]]'s files-as-canvas.
2. **Saves money** — a subagent can run on a **cheaper model** and/or be scoped **read-only**, so the expensive frontier model is reserved for the orchestration that actually needs judgment. *"A team of cheap specialist agents while one smart model runs the show."*

## Chapter map (the teaching arc)

| Time | Chapter | What it teaches |
|---|---|---|
| 0:00 | Intro | |
| 1:24 | **What Is a Subagent** | scoped delegate with its own context window |
| 3:31 | **Built-In vs Custom Agents** | Claude Code ships some; you author your own |
| 5:39 | **Descriptions & Progressive Disclosure** | the agent is auto-invoked off its description; load detail only when needed |
| 8:40 | **Skills vs Subagents** | knowledge unit vs worker unit |
| 9:31 | **Project vs Global** | scope a subagent to one project or to `~/.claude` |
| 10:51 | **Building One Live** | the hands-on demo |
| 18:11 | **Subagents as Specialists** | one job each, narrow + deep |
| 20:38 | **Saving Money & Read-Only** | cheaper model + read-only scope as cost levers |
| 22:11 | **When to Use a Subagent** | the gate question |
| 23:46 | **Dynamic Workflows** | hands off to [[dynamic-workflows]] (rung 4) |

## Descriptions & progressive disclosure (chapter 5:39)

The load-bearing build detail: a custom subagent is **invoked automatically off its description**. Claude reads the short description to decide *when* to delegate to that agent — the full agent instructions are loaded only once it's actually called. This is **progressive disclosure** applied to agent selection: the orchestrator's context only ever holds the thin description until a delegation actually fires, the same mechanism [[claude-skills]] use for skill selection. Writing a sharp, trigger-rich description is therefore the highest-leverage part of authoring a good subagent.

## Skills vs Subagents (chapter 8:40)

The disambiguation the ecosystem keeps needing (cf. [[dynamic-workflows]]' whole premise):

| | [[claude-skills]] | Subagent |
|---|---|---|
| **Unit type** | **Knowledge** — reusable procedural instructions | **Worker** — a delegated agent with its own context |
| **Context** | Loaded into the *current* agent's context | Runs in a *separate* context window |
| **Use when** | You want the current agent to *know how* to do something | You want to *hand the whole job off* and keep your context clean |

A skill teaches the agent you're already talking to; a subagent is a different agent you send away to work. They compose — a subagent can itself use skills.

## Built-in vs custom; project vs global (chapters 3:31, 9:31)

- **Built-in** agents ship with Claude Code; **custom** agents are authored by the user (the video builds one live, 10:51).
- **Project** scope lives with one repo; **global** scope lives at `~/.claude` and is available everywhere — the same project-vs-global split that governs [[claude-skills]] and `CLAUDE.md` instructions.

## Cost control: read-only + cheaper models (chapter 20:38)

The substrate-economics core. Two assignment levers make subagents a *cost* play, not just an architecture play:

- **Read-only scope** — a research/lookup subagent that can't write is both safer and cheaper to let run autonomously (echoes [[agent-security]]'s read action-class, where the cost of a false-allow is low).
- **Cheaper model** — the specialist doesn't need the frontier model; reserve [[opus-4-8]] for the orchestration. This is the operator-side discipline that pairs with [[prompt-caching]] habits and [[dynamic-workflows]]' token-cost warning.

## When to use one — and when not (chapter 22:11)

Nate's gate mirrors his [[dynamic-workflows]] gate: don't reach for a subagent by default. Use one when the work is **separable, specialist, and context-heavy** (you'd otherwise pollute the main context) or when you want to **run it cheap/read-only**. For a quick in-context task, a skill or a plain prompt is lighter. The hand-off at 23:46 to [[dynamic-workflows]] places subagents as the building block that workflows orchestrate deterministically.

## Where it sits on the complexity ladder

From [[dynamic-workflows]]:

| Rung | Primitive | Token cost |
|---|---|---|
| 1 | [[claude-skills]] | Lowest |
| 2 | **Subagents** ← *this page* | Low–moderate |
| 3 | Agent teams | Moderate–high |
| 4 | [[dynamic-workflows]] | Highest |

Subagents are the **delegation unit** that teams coordinate and workflows script. Understanding rung 2 well is the prerequisite for using rungs 3–4 without torching a token budget.

## Strategic significance

1. **Confirms [[nate-herk]]'s "every primitive gets its own explainer" cadence** — after [[claude-code-levels]] (mastery progression), [[dynamic-workflows]] (top rung), and the [[grill-me-skill]] (a skill), he now isolates rung 2. The complexity ladder is being unpacked rung by rung for a mainstream audience.
2. **Context hygiene is the headline benefit, cost is the kicker** — the framing leads with "keeps your main context clean" and closes with "saves you money," matching the vault's standing thesis that the binding constraints in 2026 are context and tokens, not raw model intelligence (cf. [[harness-over-model]]).
3. **A clean 3Ps deliverable** — "build a team of read-only specialist subagents on a cheaper model, orchestrated by one frontier model" is a concrete, billable cost-optimization pattern for client Claude Code setups. Pairs with [[dynamic-workflows]]' "is this worth a workflow?" gate.
4. **Lower-view, evergreen-tooling content** — 14.5K views is below his news-interpreter range (100K+) and on par with his other deep-tooling explainers; his audience rewards news spikes but these how-to videos are the durable reference library.

## Open questions

- **Authoring format** — is a custom subagent a markdown file with frontmatter (skill-like) under `.claude/agents/`? The digest doesn't name the file path; transcript/docs would confirm.
- **Auto-invocation precision** — how does Claude arbitrate when several subagent descriptions match? Is there a priority/precedence model?
- **Model assignment mechanics** — how is the "cheaper model" set per-subagent (frontmatter field? runtime flag?)?
- **Relationship to agent teams** — exactly where rung 2 ends and rung 3 begins (same open question [[dynamic-workflows]] flags).

## Related pages

- [[dynamic-workflows]] — rung 4; subagents are the unit it orchestrates; same author, same complexity-ladder framing
- [[claude-skills]] — rung 1; the knowledge-unit counterpart (chapter 8:40 disambiguation)
- [[claude-code]] — the substrate that hosts subagents
- [[opus-4-8]] — the orchestrator model the cheap specialists report to
- [[agent-security]] — read action-class rationale behind read-only subagents
- [[prompt-caching]], [[free-sample-phase]] — substrate-economics context for the cost-control framing
- [[ai-operating-system]] — "context is king"; subagents keep the main context clean
- [[nate-herk]] — primary author; mainstream Claude Code explainer
- [[youtube-digest-apify-2026-06-09]] — primary citation

## Used in

- [[youtube-digest-apify-2026-06-09]] — primary citation ([[nate-herk]] #1)
- [[claude-code]] — primitive unpacked
- [[nate-herk]] — primary author
