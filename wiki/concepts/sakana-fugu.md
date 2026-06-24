---
title: Sakana Fugu (Fugu Ultra — Orchestration, Not a Model)
category: concept
summary: Sakana's **Fugu Ultra** went viral claiming to match [[claude-fable-5|Fable]] and [[claude-mythos|Mythos]] — but [[nate-herk]]'s *I Battle Tested Sakana Fugu's Fable Killer* (74.8K views, 2026-06-23) clarifies it **isn't a new model**: it's **one API that orchestrates and routes tasks across frontier models** (Opus, GPT, Gemini), *"kind of like Claude Code spinning up sub-agents, just automatic"*; Nate ran Fugu Ultra against **Claude [[opus-4-8|Opus 4.8]] across 38 tasks** on quality/speed/cost and **isn't switching off his Claude Code + Codex subscriptions yet**; a concrete datapoint on the **orchestration spectrum** (automatic-router vs operator-controlled subagents) and the model-router cousin of [[harness-over-model]] and [[claude-subagents]]
tags: [sakana-fugu, fugu-ultra, sakana, orchestration, model-router, multi-model, openrouter, fusion-api, nate-herk, opus-4-8, claude-fable-5, claude-mythos, claude-subagents, harness-over-model, codex, 38-task-test, orchestration-spectrum]
sources: 1
updated: 2026-06-24
---

# Sakana Fugu (Fugu Ultra)

## What it is

**Fugu Ultra** is a release from **Sakana** whose viral announcement claimed it *matches [[claude-fable-5|Fable]] and [[claude-mythos|Mythos]]* — positioning it as a "Fable killer." [[nate-herk]]'s *I Battle Tested Sakana Fugu's Fable Killer* (74.8K views, 2026-06-23, 12:15) in [[youtube-digest-apify-2026-06-24]] punctures the framing:

> **"Fugu isn't a new model. It's one API that orchestrates and routes tasks across frontier models like Opus, GPT, and Gemini — kind of like Claude Code spinning up sub-agents, just automatic."**

So the "Fable killer" comparison is a category error: Fugu isn't competing *as* a frontier model — it's an **orchestration/routing layer that calls** frontier models. The benchmark-matching claim is about the orchestrated output, not a single model's intelligence.

## The 38-task battle test

Nate ran **Fugu Ultra against Claude [[opus-4-8|Opus 4.8]] across 38 tasks**, scoring **quality, speed, and cost** (chapter 6:28, *The 38-Task Test*). His verdict (10:27): **he's not switching off his Claude Code and Codex subscriptions yet** — the orchestration didn't clearly beat running a single strong model in a good harness.

Chapter map:
- 1:00 How Fugu Actually Works
- 2:32 Running Fugu In Claude Code
- 3:30 **The Orchestration Spectrum**
- 5:07 vs OpenRouter Fusion API
- 5:39 Speed And Cost Reality
- 6:28 **The 38-Task Test**
- 10:27 Final Takeaway

## The orchestration spectrum

The reusable idea (chapter 3:30): agentic systems sit on a spectrum from **fully automatic routing** (Fugu decides which model handles each task, invisibly) to **operator-controlled delegation** ([[claude-subagents]], where *you* assign the cheap-specialist delegates and the cheaper-model/read-only scopes). Fugu sits at the automatic end; the **OpenRouter Fusion API** (5:07) is a named neighbor on the same axis.

This is the **automatic-router foil to [[claude-subagents]]**: same underlying move (route work across models to optimize quality/cost), but Fugu hides the control Nate's subagent content hands to the operator.

## Where it sits in the vault

- **A test of [[harness-over-model]] at the routing layer** — Jones argued the harness beats raw model intelligence; Fugu asks whether an *automatic multi-model router* beats a single strong model in a good harness. Nate's "not switching yet" is a datapoint that, for now, **a well-driven single-model harness still wins** over black-box auto-orchestration.
- **The automatic cousin of [[claude-subagents]] / [[dynamic-workflows]]** — Nate explicitly analogizes Fugu to Claude Code spinning up subagents "just automatic," tying it to his own complexity-ladder content.
- **A hype-deflation video** — like his [[claude-mythos|Mythos]] "a leak isn't a launch" read, this is a "the viral claim is miscategorized" debunk: Fugu is real but it's *not* a Fable-class model. Continues the **deflate-the-hype thread** he and [[nate-b-jones]] both run.
- **Cross-references the Fable/Mythos frontier** — Sakana's marketing pegged Fugu to [[claude-fable-5]] and [[claude-mythos]], making this the batch's third Fable-adjacent video alongside Jones's Fable read and the talent-war coverage.

## Why it matters for 3Ps

- **"Orchestration isn't free magic"** — a client tempted by an auto-router should weigh it against a single strong model in a disciplined harness; Nate's 38-task test is the kind of head-to-head a 3Ps engagement would run before recommending a switch.
- **The orchestration spectrum is a decision frame** — automatic-router vs operator-controlled-subagents is a real architectural choice with cost/control/observability tradeoffs.
- **Marketing-claim hygiene** — "matches Fable" needs the question "as a model, or as an orchestrated pipeline?" — a portable due-diligence reflex.

## Open questions

- **The actual 38-task results** — where Fugu won/lost on quality/speed/cost (gated to the video beyond the "not switching yet" headline).
- **Is Sakana's Fugu the same Sakana** known for evolutionary/model-merging research? Lineage not confirmed in the digest.
- **Does automatic routing ever win** — at what task mix or scale would Nate flip? Unresolved.

## Used in

- [[youtube-digest-apify-2026-06-24]] — vault entry point (Nate Herk #13)
- [[nate-herk]] — author / tester

## Related

- [[claude-subagents]] — operator-controlled delegation; the manual cousin of Fugu's auto-routing
- [[harness-over-model]] — single-strong-model-in-good-harness vs auto-orchestration
- [[opus-4-8]] — the model Fugu was benchmarked against
- [[claude-fable-5]], [[claude-mythos]] — the frontier names Sakana's marketing pegged Fugu to
- [[dynamic-workflows]] — fanned-out orchestration on the same spectrum
- [[codex]] — the other subscription Nate keeps despite Fugu
