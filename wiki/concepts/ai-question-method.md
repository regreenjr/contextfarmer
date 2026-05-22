---
title: AI Question Method
category: concept
summary: [[nate-b-jones]]' 15th named framework — the **questioning-discipline replacement for prompt engineering** in the Opus 4.7 / GPT 5.5 era; three principles (**flashlight intent** = convey perspective + edges of investigation; **ask what good looks like** = specify artifact success criteria before generation; **wrestle with data and opinions** = force AI to take positions and defend them); canonical reframe is **AI as senior partner, not junior teammate** — junior-teammate prompting wastes 2026-era agent capability; concrete examples are the **Prime Video PRFAQ** and **MRR / product-led growth** wrestle cases; pairs with [[prompt-caching]] (mechanics-side complement) and [[karpathy-llm-wiki]] / memory layers (where senior-partner relationships accumulate context); confirms [[free-sample-phase]] economics — when models commoditize, **questioning skill is the differentiator**, not model access
tags: [nate-b-jones, framework, ai-question-method, prompt-engineering, questioning, senior-partner, flashlight-intent, good-looks-like, wrestle, opinions, prfaq, prime-video, mrr, plg, opus-4.7, gpt-5.5, free-sample-phase, claude-code, karpathy-llm-wiki]
sources: 1
updated: 2026-05-22
---

# AI Question Method

## What it is

[[nate-b-jones]]' **15th named framework**, from *Opus 4.7 and OpenAI 5.5 Made Your Prompting Style Obsolete.* (52.7K views, 2026-05-21, 25:03) in [[youtube-digest-apify-2026-05-22]]. The **questioning-discipline replacement** for prompt engineering in the Opus 4.7 / GPT 5.5 frontier-model era.

**The framing claim**: *"Prompt engineering is dead, you can just ask AI for what you want — except no. The reality is more complicated. Anyone running heavy knowledge work with weak questions gets shallow output from powerful agents. Operators who learn to ask sharp, layered questions unlock real leverage."*

## The three principles

| Principle | What it is | Example | Failure mode |
|---|---|---|---|
| **1. Flashlight intent** | Convey perspective + edges of what you're investigating, not just the question | "I'm trying to understand X **because I'm deciding Y**" | Asking "what is X?" without saying why |
| **2. Ask what good looks like** | Specify the artifact's success criteria before generation | Prime Video PRFAQ (chapter 16:20) | Asking for an artifact without defining "good" |
| **3. Wrestle with data and opinions** | Force AI to take positions and defend them, not just summarize | MRR / PLG example (chapter 21:30) | Asking for a "balanced summary" — gets aggregated, useless output |

## Principle 1 — Flashlight Intent (chapter 10:05)

Don't ask the question alone — **convey perspective + edges**. The "flashlight" metaphor: you're shining a light on a specific area of investigation. The agent needs to know **what you're investigating, why, and where the edges of relevance lie**.

Concrete framing: *"I'm trying to understand X **because I'm deciding Y**. What I already know is Z. What I'm uncertain about is W."*

This converts the prompt from a **single question** into a **scoped investigation**. The agent now knows what counts as a useful answer (relevant to the decision Y) vs an unuseful one (general background on X).

**Conveying perspective and edges in your questions** (chapter 12:30) — the canonical anti-pattern is "tell me about X" (no perspective, no edges). The right pattern is "tell me about X **from the perspective of someone deciding Y**, **bounded by these constraints W**."

## Principle 2 — Ask What Good Looks Like (chapter 14:45)

**Specify the artifact's success criteria before generation.** The model is going to generate something; you choose whether you've defined what counts as a successful artifact before it generates, or you discover the criteria afterward by being unhappy with the output.

### The Prime Video PRFAQ example (chapter 16:20)

The canonical case study:

| Weak prompt | Strong prompt |
|---|---|
| "Write a PRFAQ for X" | "If you were the PM at Prime Video deciding to ship X, what's the PRFAQ you'd write — **and what are the three places it would be wrong**?" |
| → Gets a generic, balanced, on-rails PRFAQ | → Gets a defensible artifact with **named risk surface** |

The "what are the three places it would be wrong" addition is the **success criterion** — a strong PRFAQ is one that exposes its own weak points. By specifying the criterion, you steer the model toward producing the kind of artifact you actually want.

## Principle 3 — Wrestle with Data and Opinions (chapter 19:10)

**Force the AI to take positions and defend them, not just summarize.** Frontier models default to balanced summaries because that's the lowest-risk output. The valuable output is **opinionated, defensible, and disagreement-tolerant**.

### The MRR / Product-Led Growth example (chapter 21:30)

| Weak prompt | Strong prompt |
|---|---|
| "How do I grow MRR?" | "Wrestle with the trade-off between PLG conversion velocity and ACV — where do most B2B PLG companies misallocate?" |
| → Gets surface-level advice | → Gets an opinionated, actionable artifact with named misallocation patterns |

The "wrestle with" framing **forces position-taking**. The "where do most companies misallocate" framing **forces specific defensible claims** with named failure modes. The combination produces operator-grade output.

## The canonical reframe: senior partner, not junior teammate (chapter 4:05)

**Junior teammate prompting** (give instructions, expect compliance):
- "Here's the task. Do it."
- "Use this format."
- "Don't include X."

**Senior partner questioning** (frame the problem, request judgment):
- "Here's what I'm trying to decide. How would you approach it?"
- "What's your strongest critique of this approach?"
- "Where would you push back on the framing?"

The 2026-era frontier models (Opus 4.7, GPT 5.5) **have the capability of a senior partner**. Treating them as junior teammates wastes the capability. Treating them as senior partners unlocks the leverage.

## "Why most people are still prompting like it's 2025" (chapter 6:20)

The pattern is a **habit lag** — operators learned 2025-era prompt engineering (clear instructions + examples + formatting + constraints) and the habit persists into 2026. The Opus 4.7 capability jump means:

- Constraints often **suppress useful output** instead of focusing it
- Examples often **anchor** the model to the example shape, missing better artifact shapes
- Format specification often **prevents** the model from suggesting better formats
- Junior-teammate framing **wastes** the senior-partner capability

The unlearning is harder than the learning. Operators who **don't unlearn** stay stuck producing 2025-quality output with 2026-quality models.

## "Defining agents vs agentic pipelines" (chapter 8:10)

A side-distinction Nate makes in this video:
- **Agents** — autonomous decision-makers (Claude Code agent, ChatGPT agent mode)
- **Agentic pipelines** — orchestrated workflows of multiple agent calls

The AI Question Method applies to **both**, but with different cadences:
- Agents: front-load the questioning (you ask once, the agent works for hours)
- Agentic pipelines: questioning is **at each pipeline gate** (between stages, you ask: did this produce what good looks like?)

## "Why memory and quick-start guides matter" (chapter 23:45)

The **vault-side complement**. Once you ask sharp questions, the answers need a place to compound. Memory layers — Claude Auto Memory, [[karpathy-llm-wiki]], wiki vaults — are how the senior-partner relationship **accumulates context across sessions**.

Without memory: every session restarts the senior-partner relationship from scratch. With memory: the partner has seen prior questions, prior answers, prior decisions — and can question back more sharply.

The AI Question Method + [[karpathy-llm-wiki]] + [[prompt-caching]] form a **complete senior-partner-workflow stack**:
- **Question method** = how you converse
- **Wiki/memory** = where the conversation accumulates
- **Prompt caching** = the economics of long-running conversation

## Strategic significance

1. **15th [[nate-b-jones]] framework** — extends framework cadence to 15-in-18-days (T/C/L/D 2026-05-04 → AI Question Method 2026-05-21)
2. **"Senior partner, not junior teammate" reframe is portable to 3Ps client positioning** — same shift consultants need to make with AI-augmented clients. Don't manage AI-augmented clients as junior teammates; treat them as senior partners with new capability.
3. **The three principles are diagnostic-ready** — like Nate's prior frameworks, the AI Question Method has 3 questions that double as an audit (flashlight intent specified? success criteria explicit? wrestling required?)
4. **Pairs with [[karpathy-llm-wiki]] + [[prompt-caching]]** — questioning skill (Nate) + memory layer (Karpathy) + cache economics (Nate Herk #9) form a complete senior-partner stack across this batch alone
5. **Confirms [[free-sample-phase]] economics** — Opus 4.7 / GPT 5.5 capability jump means **questioning skill is the differentiator**, not model access. Free-sample-phase doesn't matter if questions stay weak.
6. **"Opinions matter more"** ([[prove-it-economy]] #10 chapter 20:30 same batch) — same shape as Principle 3. Two [[nate-b-jones]] frameworks in one batch reinforce each other at different layers (brand-positioning + questioning-skill).

## Related

- [[nate-b-jones]] — author; 15th framework
- [[prompt-caching]] — mechanics-side complement (Nate Herk #9 same batch)
- [[karpathy-llm-wiki]] — memory-layer complement
- [[prove-it-economy]] — "opinions matter" parallel (Principle 3 ↔ chapter 20:30)
- [[free-sample-phase]] — questioning-skill is the differentiator in commoditized-model era
- [[claude-code]] — primary substrate
- [[anticipation-gap]] — permission-ladder framework names the agent autonomy levels that AI Question Method calibrates the questioning to

## Used in

- [[youtube-digest-apify-2026-05-22]] — primary citation ([[nate-b-jones]] #11)

## Open questions

- **The PRFAQ at Prime Video example** — is there a published "good" output Nate references, or is it conceptual?
- **Application to agentic pipelines** vs single-agent sessions — concrete pipeline-gate questioning patterns
- **Habit-unlearning playbook** — how do operators actually unlearn 2025-era prompt engineering?
- **Question-quality as a measurable metric** — can question-quality be evaluated independently of output-quality?
- **Cross-model portability** — does AI Question Method work the same on Opus 4.7 vs GPT 5.5 vs Gemini-equivalent?
- **Memory + question-method compounding** — does long-running memory change which question patterns work? (Important for [[karpathy-llm-wiki]] vault users)
