---
title: Deployment Framework (Three Methods)
category: concept
summary: [[nate-herk]]'s 2026-05-15 three-method classifier for where Claude Code automations should run — Method 1 `/loop` (in-session), Method 2 Routines/Scheduled Tasks (Anthropic-hosted cloud cron), Method 3 Modal / Trigger.dev (external serverless runtime); plus two higher-tier primitives — the **Claude Agent SDK** for packaged-product agents outside the CLI, and **Managed Agents & Hooks** for Anthropic-hosted always-on agents with event triggers; decision axis is "where it runs" + "how agentic it needs to be"; pairs with [[skill-systems]] (composition) / [[plugin-marketplace]] (distribution) / [[execution-layer]] (team-operational) / [[plugins]] (scaffolding-taxonomy) as the fifth operational-stack framework in the vault
tags: [deployment, claude-agent-sdk, managed-agents, hooks, modal, trigger-dev, loop, routines, scheduled-tasks, claude-code, nate-herk, runtime, operational-stack]
sources: 1
updated: 2026-05-16
---

# Deployment Framework (Three Methods)

## Definition

A three-method classifier for **where** Claude Code automations should run, plus two higher-tier primitives that sit above the three methods. Named by [[nate-herk]] in *I Tested 3 Ways to Deploy Claude Agents (Here's When to Use Each)* ([[youtube-digest-apify-2026-05-16]] #1, 2026-05-15, 16.6K views, 21:48).

The decision axis is **"where it runs" + "how agentic it needs to be"**.

## The three methods

| Method | Where it runs | Best for | Failure mode | Chapter |
|---|---|---|---|---|
| **1. `/loop` command** | Inside Claude Code session | Dead-simple recurring tasks while you work | Doesn't survive session close | 1:22 |
| **2. Routines / Scheduled Tasks** | Anthropic-hosted cloud cron | Repeating jobs that run while you sleep | Limited to Claude Code primitives | 8:29 |
| **3. Modal / Trigger.dev** | External serverless runtime | Skills that need long-running, non-Claude-Code execution (custom Python, GPUs, queues) | Setup overhead; pay-per-run | 13:00 |

The methods scale **upward in deployment effort and capability**:

- Method 1 is **free** and available immediately — the dead-simple starting point
- Method 2 is **subscription-included** but limited to Claude Code primitives
- Method 3 requires **external runtime account + setup** but unlocks arbitrary code execution

## The two higher-tier primitives

Above the three methods are two further primitives — the first surfacing of either in the vault:

### Claude Agent SDK (chapter 15:52)

The SDK that lets you build Claude agents **outside the Claude Code CLI**:

- **The unlock for packaged-product agents** — Claude as a library, not a tool
- The substrate for **third-party products built on Claude** (vs the CLI's interactive use case)
- Referenced in [[nate-herk]]'s description ("Theo's video on SDK pricing") — suggests an active developer-tier pricing debate
- Pairs with [[codex]]' SDK pricing as cross-vendor SDK-tier convergence

Strategic implication: the SDK is **Anthropic's deployment-tier API** for *packaged products*. Same shape as [[agentic-implementation-layer]] axis-1 (frontier labs going down the stack into deployment) — the SDK is the developer-facing primitive for axis-1.

### Managed Agents & Hooks (chapter 19:18)

Anthropic-hosted always-on agents with event-triggered hooks:

- The **deployment-tier equivalent of `claude-plugins-official`** for running agents (not just installing skills)
- Closes the gap between Routines (scheduled) and external runtime (event-driven)
- Hooks here refer to **deployment-tier event triggers**, not the same as the Claude Code settings.json hooks for tool-call events
- Specifics gated to transcript pull

Likely positioning: this is Anthropic's answer to "what if I want a Cloud-hosted always-on Claude agent with event triggers" — closing the gap that Modal/Trigger.dev currently fills.

## Why this framework matters

### It completes the operational-stack inventory

Combined with the four prior operational-layer frameworks named in this vault, the deployment framework completes the operational stack for Claude Code work:

| Layer | Framework | Author |
|---|---|---|
| Unit | [[claude-skills]] | [[anthropic]] |
| Authoring | (Skill Creator + 3 Types of Skills) | [[anthropic]] + [[ben-ai]] |
| **Composition** | [[skill-systems]] | [[simon-scrapes]] |
| **Scaffolding taxonomy** | [[plugins]] (6 layers) | [[nate-b-jones]] |
| **Distribution** | [[plugin-marketplace]] | [[alex-mcfarland]] |
| **Team deployment** | [[execution-layer]] | [[brad-bonanno]] |
| **Runtime deployment** | **[[deployment-framework]] (this concept)** | **[[nate-herk]]** |
| Eval / meta | [[skill-creator]] | [[anthropic]] + [[chase-ai]] |

Seven named operational layers now exist. The deployment-framework is the **runtime-selection layer** — the last layer before code actually runs.

### It maps to the [[agentic-implementation-layer]] axes

| Method | Maps to [[agentic-implementation-layer]] axis |
|---|---|
| Method 1 (`/loop`) | Axis 1 (Anthropic-hosted, lab-owned) |
| Method 2 (Routines) | Axis 1 (Anthropic-hosted, deployment-tier) |
| Method 3 (Modal / Trigger.dev) | (Outside the four axes — third-party runtime category) |
| Claude Agent SDK | Axis 1 (developer-facing axis-1 primitive) |
| Managed Agents & Hooks | Axis 1 (deployment-tier always-on) |

Three of the five primitives are axis-1 Anthropic deployment-tier. Modal / Trigger.dev are **outside the four-axis squeeze** — they're third-party runtimes that don't fit any axis. This may be a fifth axis that [[nate-b-jones]]' framework didn't name (or a temporary gap before axis-1 absorbs the use case via Managed Agents).

### It is a buy-up funnel

The three methods form an **Anthropic monetization funnel**:

- Method 1 captures the user (free, in-session)
- Method 2 retains the user (subscription-included)
- Method 3 is happy to lose (still pays for inference via external runtime)

Pairs with [[free-sample-phase]] economics — the substrate captures users at low-effort tiers and is happy to lose them to specialized runtimes at the top because inference billing still accrues regardless of where the orchestration runs.

## Decision rules ([[nate-herk]]'s framing)

The deployment choice depends on two axes:

| If your automation... | Use |
|---|---|
| Runs only while you're working | Method 1 (`/loop`) |
| Needs to run on a schedule while you sleep | Method 2 (Routines / Scheduled Tasks) |
| Needs long-running execution (>5min) | Method 3 (Modal / Trigger.dev) |
| Needs GPUs / custom Python / specialized libs | Method 3 |
| Is a packaged product for other developers | Claude Agent SDK |
| Needs event-driven always-on hosting | Managed Agents & Hooks |

## Why it matters for 3Ps

1. **Client-engagement sequencing** — most clients should start at Method 1 / Method 2 before paying for Method 3 setup overhead. The 3Ps consulting offer can include the deployment-method-selection diagnostic.
2. **Cost-structure clarity** — Methods 1-2 are subscription-included; Method 3 is pay-per-run. The buy-up funnel maps cleanly to client tier (small biz at Method 2, mid-market at Method 3).
3. **The SDK is the productization unlock** — for any 3Ps client wanting to *sell* their AI workflow as a product, the Claude Agent SDK is the relevant primitive (not the Claude Code CLI).
4. **Modal + Trigger.dev are tracking candidates** — both surface for the first time in this vault. Worth establishing as 3Ps-supported external runtime options for client work that exceeds Claude Code's session limits.

## Contrasts with

- **[[skill-systems]]** — composition discipline *inside* a workflow; this concept is about *where the workflow runs*
- **[[execution-layer]]** — team-operational deployment ("how does my team install this"); this concept is about runtime selection ("where does this execute")
- **[[plugin-marketplace]]** — distribution layer ("how does this get to other machines"); this concept is about runtime layer ("where it ticks")
- **[[plugins]] taxonomy** — categorical "what scaffolding type is this"; this concept is the deployment counterpart to that taxonomy
- **[[hermes-agent]]** — competitor substrate that bundles all three methods + always-on as a single VPS topology; [[deployment-framework]] decomposes Hermes' single-bundle into a three-tier funnel within Claude Code

## Cross-substrate portability

- Methods 1-2 are **Claude Code-specific** (Anthropic-hosted primitives)
- Method 3 is **substrate-agnostic** — Modal / Trigger.dev work with [[codex]], [[hermes-agent]], or any LLM SDK
- The Claude Agent SDK is **Anthropic-specific** but has [[codex]]-side equivalents (referenced via the "Theo's video on SDK pricing" cross-link)

The framework itself (the three-method shape + the SDK + Managed Agents tier above) likely **ports across substrates** — Codex and Hermes have parallel deployment tiers. [[nate-herk]] hasn't explicitly drawn this cross-substrate parallel yet, but the shape is symmetric.

## Open questions

- **Pricing of Managed Agents** — Anthropic hasn't been confirmed shipping this as a paid product yet; transcript pull would resolve
- **What Theo's video on SDK pricing says** — referenced in [[nate-herk]]'s description but not summarized; may surface cross-vendor SDK pricing comparison worth tracking
- **Modal vs Trigger.dev choice criteria** — both surface together but [[nate-herk]] doesn't explicitly compare them; future video likely
- **Cross-substrate parity** — does [[codex]] have direct equivalents for `/loop` / Routines / Modal / SDK / Managed Agents? Likely yes; needs verification
- **Hooks semantics** — the chapter title "Managed Agents & Hooks" conflates two primitives; are they always bundled, or can you have Managed Agents without Hooks?

## Used in

- [[youtube-digest-apify-2026-05-16]] — primary citation ([[nate-herk]] #1)
- [[nate-herk]] — primary author (third operational framework in his cadence)
- [[claude-code]] — substrate; new primitives surfaced (Agent SDK, Managed Agents, Hooks)
- [[agentic-implementation-layer]] — three of the five primitives are axis-1 Anthropic deployment-tier
- [[free-sample-phase]] — economics-layer that the three-method funnel maps to
- [[execution-layer]] — sibling team-deployment framework
- [[plugin-marketplace]] — sibling distribution framework
- [[skill-systems]] — sibling composition framework
- [[plugins]] — sibling scaffolding-taxonomy framework

## Related pages

- [[nate-herk]], [[claude-code]], [[anthropic]]
- [[execution-layer]], [[plugin-marketplace]], [[skill-systems]], [[plugins]], [[skill-creator]] — sibling operational-stack frameworks
- [[codex]], [[hermes-agent]] — cross-substrate equivalents
- [[free-sample-phase]] — economics counterpart
- [[agentic-implementation-layer]] — strategic counterpart (axis-1 mapping)
