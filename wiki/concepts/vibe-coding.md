---
title: Vibe Coding
category: concept
summary: Karpathy's term for casual, prompt-driven code generation; in 2026 he reframes it as the on-ramp to the more serious "agentic engineering" discipline
tags: [vibe-coding, andrej-karpathy, agentic-engineering, software-3-0, claude-code, directing-agents, nate-herk]
sources: 2
updated: 2026-06-24
---

# Vibe Coding

## Definition
Term coined by [[andrej-karpathy]] (~early 2025) for the casual, prompt-driven mode of writing code with an LLM — "vibing" with the model, accepting/rejecting suggestions, writing English instead of code. Distinguished from production-grade engineering by its informality and reliance on the model's judgment.

In 2026, Karpathy himself reframed the term: vibe coding was the **on-ramp**; **[[agentic-engineering]]** is the more serious discipline now taking shape on top.

## Origin
[[andrej-karpathy]] coined the term ~early 2025 (X/Twitter). Reframed at Sequoia AI Ascent 2026 in *From Vibe Coding to Agentic Engineering* ([[youtube-digest-apify-2026-05-03]] #13, 549K views — largest video in this digest).

## Key claims (from Sequoia talk #13)

- **"I've never felt more behind as a programmer"** — Karpathy's framing for the speed of change
- **Vibe coding → agentic engineering** is the maturation path
- **Software 3.0** — natural language is the programming surface; agents are the installer/runtime
- **Agents as the installer** — the new layer that sits between human intent and running code
- **Menu Gen vs Raw Prompts** — structure matters as you scale beyond toy prompts
- **LLMs are ghosts, not animals** — jagged, statistical, summoned entities; new taste/judgment required to direct them
- **Verifiability and jagged skills** — LLMs' capability profile is uneven; verifiability is the constraint
- **"You can outsource your thinking but never your understanding"** — caveat against fully delegated cognition

## Contrasts with

- **[[agentic-engineering]]** — the serious successor discipline; structured, verifiable, agent-orchestrated
- **Traditional software engineering** — typed, tested, reviewed; vibe coding skips these
- **No-code / low-code** — pre-LLM precursor; vibe coding does in English what no-code did in visual blocks

## Open questions / disagreements

- **Where's the line between vibe and agentic?** — Karpathy gestures at it but no canonical taxonomy exists
- **Production fitness** — vibe coding for prototypes is established; vibe coding for production is contested
- ⚠️ **Karpathy's reframe** vs the term's continuing use as an aesthetic — many creators still use "vibe coding" without the maturation framing; the term may bifurcate

## Why it matters for 3Ps

- **Client conversation framing** — "vibe coding got you here; agentic engineering is what your team needs next" is a credible upsell narrative
- **Skill positioning** — 3Ps skill library should be marketed as "agentic engineering primitives," not "vibe coding shortcuts"
- **Karpathy reference is high-status** — citing his 2026 Sequoia talk in any client deck adds credibility cheaply

## Operator instantiation (2026-06-24)

[[nate-herk]]'s *How to Build Effective Claude Code Agents in 2026* (39.7K views, w/ Cole) gives the vibe→agentic transition a concrete operator playbook — **[[directing-agents]]**. Its load-bearing chapter is literally *"Stop Vibe Coding, Start Directing"*: plan more than you build, **make the agent prove its work**, route around the **"dumb zone,"** chain sessions, and treat the system as **harness engineering**. It's the clearest creator-side demonstration of Karpathy's "vibe coding was the on-ramp; agentic engineering is the discipline" reframe — and it lands on the same conclusion as [[harness-over-model]] (the system around the model is the leverage). → See [[directing-agents]].

## Used in
- [[youtube-digest-apify-2026-05-03]] — primary citation (Sequoia #13)
- [[youtube-digest-apify-2026-06-24]] — [[directing-agents]] (Nate Herk + Cole; the operator-grade vibe→agentic playbook)
- [[andrej-karpathy]] — author
- [[agentic-engineering]] — successor concept (page TBD)
- [[directing-agents]] — the 2026-06-24 operator instantiation of the maturation arc
- [[claude-code]] — primary substrate where both vibe and agentic engineering happen
