---
title: Open Engine (Shared Task Queue for Agent Handoff)
category: concept
summary: [[nate-b-jones]]'s **34th named framework** (*I Was The Only Thing Connecting Claude, ChatGPT, and Codex. So I Built My Replacement.*, 17.9K views, 2026-06-26, 22:04) — names the real bottleneck of multi-tool agent work as the **handoff between agents, not the model**: because agents don't talk to each other, *"you have become the human glue moving work between Claude, Codex, and ChatGPT."* **Open Engine** is a **shared task queue both people and agents read** that lets agents **hand off work, carry the sources, and leave a receipt** without a human stuck in the middle. The thesis: *"agents are loop managers and you are the hallway"* — agents are finally capable enough to do the work, so the 2026 win is **building the queue that moves work between them before you become the bottleneck** (move from *prompt mode* to *work mode*). The build-side / coordination-layer instantiation of [[agent-protocol-stack]]'s A2A (agent-to-agent delegation), the work-side cousin of [[open-skills]] (procedures don't travel ⇄ here *work* doesn't travel), and the multi-agent extension of [[loop-of-loops]]
tags: [open-engine, agent-handoff, shared-task-queue, human-glue, agent-coordination, loop-managers, hallway, work-mode, prompt-mode, receipt, source-carrying, a2a, cross-vendor, claude-code, codex, chatgpt, nate-b-jones, 34th-framework]
sources: 1
updated: 2026-06-27
---

# Open Engine (Shared Task Queue for Agent Handoff)

## Definition

[[nate-b-jones]]'s **34th named framework**, from *I Was The Only Thing Connecting Claude, ChatGPT, and Codex. So I Built My Replacement.* (17.9K views, 2026-06-26, 22:04). **Open Engine** is a **shared task queue that both people and agents read**, designed to let agents **hand off work to each other, carry the sources along, and leave a receipt** — removing the human from the middle of every transfer.

Source: [[youtube-digest-apify-2026-06-27]] #1. How-to guide gated behind his Substack (`natesnewsletter.substack.com`).

## The framing claim — the handoff is the bottleneck, not the model

> *"Your AI agents don't talk to each other, so you have become the human glue moving work between Claude, Codex, and ChatGPT."*

The common story is that agents go autonomous and take work off your plate. Jones's reframe: **the real bottleneck is the handoff between agents** — where the context, the sources, and the review keep falling back on the human. The models are individually capable; what's missing is the **coordination layer** that moves work between them.

- **"Agents are loop managers and you are the hallway"** (chapter 04:48) — each agent competently manages its own loop, but the human is the corridor every piece of work has to walk through to get from one agent to the next.
- **"The fix is a shared queue both people and agents read"** (chapter 06:32) — a durable task queue that any agent (or person) can pull from, push to, and leave a record on.

## The three properties of the queue

A working Open Engine queue lets agents:

1. **Hand off work** — pass a task from one agent/tool to another without a human re-typing or re-pasting it.
2. **Carry the sources** — the context travels *with* the task, so the receiving agent isn't starting cold (the failure mode that forces the human back into the loop).
3. **Leave a receipt** — a record of what was done, so review and the next handoff don't depend on the human reconstructing state.

## Prompt mode → work mode

The behavioral shift the framework asks for (chapter 00:00, *How to make your AI agents work as one system*): stop operating each agent in **prompt mode** (one request at a time, human shuttles the output) and move to **work mode** (agents pull from and push to a shared queue as a single system). *"The agents are finally capable enough to do the work, and the win now is building the queue that moves it between them before you become the bottleneck."*

## Where it sits in Nate B Jones's stack

| Framework | What it names | Relationship to Open Engine |
|---|---|---|
| [[agent-protocol-stack]] (A2A) | agent-to-agent delegation protocol | Open Engine is the **build-side instantiation** of A2A — the practical "how do agents actually hand off" that the protocol layer abstracts |
| [[open-skills]] (30th) | *procedures* don't travel between tools | Open Engine is the work-side cousin — *work* doesn't travel between tools; both are cross-vendor portability problems |
| [[loop-of-loops]] (33rd) | compose recurring loops that hand off what changed | Open Engine is the **multi-agent / multi-tool** extension — loops handing off across *different agents*, not just sub-loops within one |
| [[work-primitive]] | access / meaning / authority under agent work | "prompt mode → work mode" is the same move at the operator scale |
| [[anticipation-gap]] | the burden of *when to invoke* falls on the human | Open Engine removes a different human burden — *moving work between* agents — but both shrink the human-in-the-middle tax |

This is his **third consecutive cross-vendor-coordination framework** (open-skills → loop-of-loops → open-engine), all circling the same insight: in a multi-tool 2026 workflow, the scarce missing piece is the **layer between agents**, not the agents.

## Why it matters for 3Ps / this vault

1. **Names the coordination tax directly.** Operators running Claude + Codex + ChatGPT feel the "human glue" problem acutely; a queue that carries sources + leaves receipts is a concrete, sellable deliverable.
2. **The vault is a partial Open Engine.** `raw/` → `wiki/` with the `log.md` receipt and farmer handoffs is a *write-time* shared store both humans and agents read — the same shape as Open Engine, but for knowledge rather than tasks. Worth diffing Jones's queue design against the vault's log + farmer pattern.
3. **Build-side complement to [[ai-operating-system]].** Where the AIOS is one operator's single-agent system, Open Engine is the **multi-agent coordination layer** above it.

## Open questions

- **What's the actual queue implementation?** (File-based? A service? An MCP server both tools mount? Gated to the Substack how-to.)
- **How is the "receipt" structured** — free text, schema, or a log like this vault's `log.md`?
- **Does it depend on A2A**, or is it a hand-rolled shared store that predates protocol adoption?
- **How does it carry sources across vendors** with different context formats?

## Related
- [[nate-b-jones]] — author (34th framework)
- [[agent-protocol-stack]] — A2A is the protocol-layer abstraction of this build
- [[open-skills]] — procedures-don't-travel; the cross-vendor cousin
- [[loop-of-loops]] — the single-tool recurring-loop predecessor (33rd framework)
- [[work-primitive]] — prompt-mode → work-mode at the substrate level
- [[anticipation-gap]] — the other human-in-the-middle tax
- [[ai-operating-system]] — single-operator AIOS that Open Engine coordinates across
- [[claude-code]], [[codex]] — two of the three agents being coordinated
- [[youtube-digest-apify-2026-06-27]] — citation
