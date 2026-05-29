---
title: Agent Analytics (Product Analytics for AI Agents)
category: concept
summary: [[nate-b-jones]]'s **24th framework** (2026-05-28) — product analytics for AI agents must start from the **agent run, not the click**; most agent failures are *product-analytics* failures hiding inside the run, not engineering incidents. Core moves — the **agent run replaces the session** as the unit of product behavior; **chat logs and engineering traces are not product analytics**; the **completion-vs-acceptance gap** measures trust; **the correction is your most valuable signal**; **Salesforce's Agent Work Units** name the delegated work; **three events to ship first**; *"product analytics is the rudder on your agents."* The observability/product-side complement to [[agent-security]] (action-boundary judge), [[long-running-benchmarks]] (eval-side), and the [[agent-metering]] work-unit (pricing-side)
tags: [agent-analytics, product-analytics, agent-run, session-replacement, completion-acceptance-gap, correction-signal, salesforce-agent-work-units, work-units, delegated-work, observability, cursor-database-wipe, three-events, nate-b-jones, framework, agent-security, long-running-benchmarks, agent-metering]
sources: 1
updated: 2026-05-29
---

# Agent Analytics

## Definition

[[nate-b-jones]]'s **24th named framework**, introduced in [[youtube-digest-apify-2026-05-29]] #1 — *A Cursor Agent Wiped a Database in 9 Seconds. Agent Analytics Would Have Seen It Coming.* (14.3K views, 2026-05-28, 11:51).

The **product-analytics-side framework** for the agent era. Core reframe:

> **Most agent failures are product-analytics failures hiding inside the agent run — not engineering incidents.** Your product dashboard cannot see what's really happening inside an agent run, and that blindness is where trust and failure both live.

The discipline: **product analytics for agents must start from the *run*, not the *click*.** Click/session analytics was built for human-driven product behavior; it cannot see delegated work an agent performs on a user's behalf.

## The framing claim

> *"What's really happening inside an AI agent run that your product dashboard cannot see? The common story is that agent failures are engineering incidents — but the reality is that most of them are product analytics failures hiding inside the agent run."*

The signature [[nate-b-jones]] structure — "the common framing is X, but the reality is Y" — applied to the analytics layer.

## Chapter map

- 00:00 The agent era changes product analytics
- 00:46 Ten billion tokens of agent code in production
- 01:34 A Cursor agent deletes a database in nine seconds
- 02:25 Why most dashboards miss the actual failure
- 03:09 **Delegated work is the new unit of product behavior**
- 04:08 **Chat logs are not enough**
- 05:02 **Engineering traces are not product analytics**
- 05:59 **Salesforce Agent Work Units name the work**
- 07:01 **The correction is your most valuable signal**
- 08:21 **The completion vs acceptance gap**
- 09:42 **Three events to ship first**
- 10:38 Product analytics is the rudder on your agents

## Core claims

- **The agent run replaces the session as the unit of product behavior** (chapter 03:09) — delegated work is the new primitive. A run (not a click, not a session) is what you measure, because the agent acts on the user's behalf across many steps.
- **Chat logs are not product analytics** (chapter 04:08) — a transcript records what was said, not whether the delegated work succeeded or was trusted.
- **Engineering traces are not product analytics** (chapter 05:02) — observability/APM traces tell you the *system* ran; they don't tell you whether the *product behavior* was the right one. The two are routinely confused, which is why dashboards miss the actual failure (chapter 02:25).
- **The completion-vs-acceptance gap is the trust signal** (chapter 08:21) — an agent can *complete* a run while the user *rejects* the output. The gap between completion rate and acceptance rate measures trust, and it is invisible to both chat logs and engineering traces.
- **The correction is your most valuable signal** (chapter 07:01) — when a user edits, undoes, or overrides what the agent did, that correction is the highest-information event in the whole run. Instrument corrections first.
- **Salesforce Agent Work Units name the work** (chapter 05:59) — Salesforce's Agent Work Unit is the productized instance of "delegated work as a measurable unit." It is the same primitive the [[agent-metering]] framework sees from the *pricing* side (Flex Credits / per-task billing), here seen from the *analytics* side.
- **The rudder thesis** (chapter 10:38) — *"product analytics is the rudder on your agents."* Without run-level analytics in place before agents run at full speed in production, there is no steering — only after-the-fact incident response.

## The unlock event — the Cursor database wipe

**A Cursor agent deleted a database in nine seconds** (chapter 01:34). The framing: this reads as an *engineering incident*, but the deeper failure is that **no product-analytics layer existed to see the run heading toward an irreversible action** before it executed. "Agent analytics would have seen it coming."

This is the same shape as [[nate-b-jones]]'s prior named-firm unlock events (McKinsey-Lilly → [[agent-security]], Mozilla-271 → [[code-comprehensibility]], Sullivan & Cromwell → [[project-room-workflow]], Shopify-River → [[public-ai-work]]): a public failure becomes the entry point for the structural lesson. **"Ten billion tokens of agent code in production"** (chapter 00:46) is the scale claim that makes the analytics gap urgent.

## Three events to ship first

Chapter 09:42 names a starter instrumentation set — the minimum events to put in before agents run at scale. The video frames three (specifics gated to transcript / Substack), but the shape follows from the core claims:

1. **Run start/end with outcome** — the run as the unit, not the click.
2. **Correction / override events** — the highest-signal event (chapter 07:01).
3. **Acceptance vs completion** — the trust gap (chapter 08:21).

**Substack monetization**: *"Full Post w/ Prompts"* — `natesnewsletter.substack.com/...` gates the operational event spec + prompt pack, the same pattern as his prior framework videos.

## Where it sits in the [[nate-b-jones]] stack

Agent Analytics is the **production-observability / product-side** complement to four prior frameworks:

| Framework | Boundary | What it governs |
|---|---|---|
| [[agent-security]] | Action boundary (pre-execution) | A separate LLM-as-judge decides *should this action proceed?* |
| **Agent Analytics** | **Run boundary (during + post-execution)** | **Did the delegated work succeed, and was it trusted?** |
| [[long-running-benchmarks]] | Eval boundary (pre-deployment) | Does the agent behave well over a long trajectory? |
| [[infrastructure-control-layer]] | Observability control point | What did the agent technically *do*? |

The four chain cleanly: the judge ([[agent-security]]) gates the action, **agent analytics measures whether the run delivered trusted product behavior**, long-running benchmarks test trajectory behavior before deploy, and infra observability records the technical trace beneath it all. Agent Analytics' key move is insisting the **product** layer (acceptance, correction, trust) is *distinct from* the **engineering** layer (traces) — the same distinction [[agent-metering]] draws between work-units and tokens.

## Why it matters for 3Ps

1. **A concrete pre-production deliverable** — "instrument run-level analytics before your agents ship" is a one-engagement scope: define the run, instrument corrections + the completion-vs-acceptance gap, build the dashboard. Same consulting shape as the [[agent-metering]] pre-renewal review and the [[work-primitive]] readiness audit.
2. **Names the metric clients are missing** — most teams shipping agents track engineering traces (Datadog-tier) and chat logs, and believe they have "agent analytics." This framework gives the language to show them the gap.
3. **The correction-signal instrumentation is directly portable** — corrections are the highest-information event and are usually uninstrumented; a fast, high-value first deliverable.
4. **Pairs with this vault's own log discipline** — `wiki/log.md` is a run-level (not click-level) record of what the maintaining agent did; the same instinct, at the personal-knowledge-base scale.

## Open questions

- What are the **three named events** (chapter 09:42)? (Transcript / Substack would resolve.)
- Is "Agent Analytics" the durable name, or does it converge with vendor terms (Salesforce Agent Work Units, PostHog/Amplitude "agent analytics" SKUs)?
- Does the completion-vs-acceptance gap have a canonical metric definition, or is it per-product?
- Which analytics vendors are building run-first (vs click-first) products? (Net-new entity stubs likely in a future digest.)

## Related pages

- [[nate-b-jones]] — author (his 24th framework in 25 days)
- [[agent-security]] — action-boundary judge; pre-execution complement to run-boundary analytics
- [[long-running-benchmarks]] — eval-side complement (trajectory behavior before deploy)
- [[agent-metering]] — sees the *same* delegated-work unit (Salesforce Agent Work Units) from the pricing side
- [[infrastructure-control-layer]] — the "observability" control point that agent analytics sits *above* (product vs engineering observability)
- [[work-primitive]] — "delegated work as the unit" is the analytics instantiation of the access/meaning/authority substrate
- [[claude-code]] — coding agents (Cursor, Claude Code) are the proof case where runs already produce rich, correctable signal
- [[youtube-digest-apify-2026-05-29]] — primary citation
