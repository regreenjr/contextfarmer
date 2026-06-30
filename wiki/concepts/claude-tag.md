---
title: Claude Tag (Anthropic's Slack-Resident Context Harness)
category: concept
summary: Anthropic's **Slack-native** product (surfaced by [[nate-b-jones]] across two 2026-06 videos) that lets Claude live *inside* a team's Slack and **turn that Slack context into a sticky harness** — *"Claude Tag turns your team's Slack context into a sticky harness"*; the named mechanism behind why companies don't switch to cheaper open models like [[glm]] even when those models win on raw work: the **last mile is context**, and Claude Tag captures it where work already happens; a concrete instance of the [[context-wars]] thesis (live where the user's context lives) and the **stickiness layer** that [[harness-over-model]] predicts will hold customers as intelligence commoditizes
tags: [claude-tag, anthropic, slack, context-harness, last-mile, context-wars, harness-over-model, glm, stickiness, switching-cost, nate-b-jones, context-moat]
sources: 1
updated: 2026-06-30
---

# Claude Tag

## What it is

**Claude Tag** is [[anthropic]]'s **Slack-resident** Claude product — Claude living *inside* a team's Slack, where it absorbs the team's working context (threads, decisions, history). Surfaced by [[nate-b-jones]] in [[youtube-digest-apify-2026-06-30]]:
- #4 (*GLM 5.2 Is Free And Beats Claude On Most Work…*, 83.5K) — *"Claude Tag turns your team's Slack context into a sticky harness."*
- #5 (*The Real Story Behind the Government GPT 5.6 Freeze*, 32.1K, chapter 5:44 *Anthropic launches Claude Tag inside Slack*).

> ⚠️ Detail status: sourced from video descriptions + chapter markers, not a transcript or an Anthropic announcement page. Exact feature scope, pricing, and GA status are unconfirmed in this vault.

## Why it matters

Claude Tag is the **named stickiness mechanism** in two of the vault's central 2026 theses:

1. **The answer to "why can't companies switch?"** ([[glm]] / #4). [[glm]] 5.2 is free and beats Claude on most everyday work, yet companies keep paying frontier prices. Jones' explanation: **switching a model means replacing a whole work system, not a call** — *"the real question is whether you can move your context."* Claude Tag is the thing that **traps the context inside Anthropic's harness**, so the cheaper model can't be dropped in. It is [[harness-over-model]]'s prediction made into a product: as intelligence commoditizes, the **harness + your own context** is the durable layer.

2. **A front in the [[context-wars]]** (#5). Alongside **Apple wiring Siri into your phone context** and **[[codex]] earning trust on sensitive work at OpenAI**, Claude Tag is Anthropic's move to **live where your work already is** (Slack). *"Whoever controls the context that makes any model useful — your files, your Slack, your phone — wins."*

The privacy hinge from #5 applies directly: putting Claude inside Slack *"quietly turns every convenience into a decision about what you are willing to hand over."*

## Related pages

- [[context-wars]] — the macro thesis Claude Tag is an instance of (live where the context lives)
- [[glm]] — the cheaper open model Claude Tag's stickiness defends against
- [[harness-over-model]] — the framework predicting harness + context > raw model
- [[anthropic]] — the vendor shipping it
- [[codex]] — OpenAI's parallel "earn trust where work happens" move
- [[open-engine]] — [[nate-b-jones]]' agent-handoff harness thesis (sibling context-layer framework)
- [[karpathy-llm-wiki]] — the "own your context / data moat" pattern from the user side
- [[nate-b-jones]] — the creator who surfaced it
