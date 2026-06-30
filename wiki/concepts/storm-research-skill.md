---
title: STORM Research Skill (Stanford's Five-Perspective Method as a Claude Skill)
category: concept
summary: A free [[claude-skills|Claude skill]] from [[nate-herk]] (*Stanford's Method Turns Claude Into a PhD-Level Research Team*, 24.1K views, 2026-06-29) that packages Stanford's **STORM** research method — running a topic through **five expert perspectives** (practitioner, academic, skeptic, economist, historian) instead of a single prompt — **maps where they disagree, verifies every source, and outputs a clean HTML briefing**; pitched head-to-head against [[claude-code]]'s built-in Deep Research; the thesis is *"five perspectives beat one — the blind spots one angle misses get caught by another"*; a multi-perspective research **harness** (reliability via disagreement-mapping + source-verification), the research-synthesis cousin of [[project-room-workflow]], [[agent-council]], and [[directing-agents]]
tags: [storm-research-skill, stanford-storm, nate-herk, claude-skills, claude-code, deep-research, multi-perspective, five-perspectives, source-verification, disagreement-mapping, research-synthesis, harness-over-model, subagents, agent-teams, html-briefing, free-skill]
sources: 1
updated: 2026-06-30
---

# STORM Research Skill

## What it is

A free [[claude-skills|Claude skill]] built by [[nate-herk]] that adapts **Stanford's STORM** research method into Claude. Instead of asking one prompt one way, it **spins up five expert lenses** on the same topic, **maps where they disagree**, **verifies every source**, and hands back a **clean HTML briefing**. Surfaced in [[youtube-digest-apify-2026-06-30]] (#3, *Stanford's Method Turns Claude Into a PhD-Level Research Team*, 24.1K views, 12:05).

## The five perspectives

| Lens | Catches |
|---|---|
| **Practitioner** | What actually works in the field |
| **Academic** | The theory, the literature, the rigor |
| **Skeptic** | The holes, the counter-evidence |
| **Economist** | Incentives, costs, second-order effects |
| **Historian** | Precedent, prior cycles, what's been tried |

Core thesis (00:42): **"Why five perspectives beat one"** — *"the blind spots one angle misses get caught by another."* The disagreement between lenses is the signal: the skill **maps where they conflict** rather than averaging them into mush.

## The pipeline

1. Run the topic through the **five lenses** (each a perspective prompt).
2. **Map disagreement** across the lenses.
3. **Verify every source** before it's used (a reliability gate).
4. Output a **clean HTML briefing**.

The video walks **the four prompts behind it** (04:36), how to **install it** (06:06), a **live run on Voice AI Agents** (07:26), and **subagents vs agent teams** (08:34) as the implementation substrate.

## Why it matters for this wiki

- **A research-grade reliability harness.** Source-verification + disagreement-mapping are an explicit reliability layer — [[harness-over-model]] applied to *research synthesis*. The output's trustworthiness comes from the harness (multiple lenses + source checks), not from a single model call.
- **The research-synthesis member of the vault's "structured-artifact-before-output" family** — alongside [[project-room-workflow]] (source-inventory / conflict-log / missing-context-list), [[agent-council]] (a panel pressure-tests an idea *before* you build), and [[directing-agents]] (plan-and-verify). All four front-load structure to make the model's output more reliable. STORM's **conflict-map** is the direct analog of Project Room's **conflict log**.
- **A first-party-vs-skill benchmark.** It's pitched **head-to-head against [[claude-code]]'s built-in Deep Research** (01:28) — a creator-built skill competing with Anthropic's native `/deep-research`, the same "skill beats default" framing as [[nate-herk]]'s prior feature tier-lists.
- **Implemented on [[claude-subagents]] / agent teams** — the "subagents vs agent teams" segment (08:34) makes the five lenses concrete as scoped delegates, a new application of his own complexity-ladder coverage.

## Open questions

- The verdict of the **STORM-vs-Deep-Research** head-to-head (gated to the video) — when does the multi-lens skill beat the native tool, and when is `/deep-research` enough?
- Are the **five lenses fixed or tunable per domain** (he mentions "tweak the lenses for your own work")?
- Does it ship via his Skool AI OS course (free) like his other skills?

## Related pages

- [[nate-herk]] — built and released the skill
- [[claude-skills]] — the packaging primitive
- [[claude-code]] — Deep Research is the head-to-head benchmark
- [[claude-subagents]] — the five lenses as scoped delegates; "subagents vs agent teams"
- [[project-room-workflow]] — the conflict-log / structured-artifact cousin
- [[agent-council]] — a panel that pressure-tests before building (idea-validation analog)
- [[directing-agents]] — plan-and-verify / harness engineering
- [[harness-over-model]] — reliability comes from the harness, not the raw model
- [[grill-me-skill]] — sibling free context/research skill from the same creator
