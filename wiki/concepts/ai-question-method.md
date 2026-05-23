---
title: AI Question Method
category: concept
summary: [[nate-b-jones]]' 15th named framework — the **questioning-discipline replacement for prompt engineering** in the Opus 4.7 / GPT 5.5 era; three principles (**flashlight intent** + **ask what good looks like** + **wrestle with data and opinions**); canonical reframe is **AI as senior partner, not junior teammate**; **in 2026-05-23 [[nate-b-jones]] ships the artifact-side complement** — [[project-room-workflow]] (his 18th framework, 22.3K views) — names the **canvas artifacts** that pair with the questioning discipline (source inventory + conflict log + missing context list); together Question Method + Project Room form the **complete pre-prompt workflow** above any frontier model; Principle 2 (*ask what good looks like*) is also operationalized at the skill-eval tier by [[simon-scrapes]]' [[self-improving-skills]] (binary criteria = success criteria as code)
tags: [nate-b-jones, framework, ai-question-method, prompt-engineering, questioning, senior-partner, flashlight-intent, good-looks-like, wrestle, opinions, prfaq, prime-video, mrr, plg, opus-4.7, gpt-5.5, free-sample-phase, claude-code, karpathy-llm-wiki, project-room-workflow, self-improving-skills, pre-prompt-workflow, canvas-shaping, artifact-discipline]
sources: 2
updated: 2026-05-23
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

## The artifact-side complement (2026-05-23): [[project-room-workflow]]

[[nate-b-jones]] shipped his **18th framework** ([[project-room-workflow]]) one day after AI Question Method. The two are designed as **complementary pre-prompt disciplines**:

| Framework | Discipline | Pre-prompt requirement | Output |
|---|---|---|---|
| **AI Question Method (this)** | **Questioning** | Flashlight intent + ask what good looks like + wrestle | Sharp question |
| **[[project-room-workflow]]** | **Artifacts** | Source inventory + conflict log + missing context list | Curated canvas |

Both target the same gap: **junior-teammate prompting wastes Opus-4.7-era frontier capability**. Question Method shapes *what you ask*; Project Room shapes *the canvas the agent works in*. Together they form the **complete pre-prompt workflow** above any frontier model.

The **Sullivan & Cromwell hallucination unlock event** in Project Room Workflow (federal-court motions with AI hallucinations despite frontier-model access) is the canonical "good questions cannot save bad canvas" case. Even perfect application of AI Question Method principles cannot rescue an output if the canvas is duplicate-poisoned and gap-blind.

## Principle 2 operationalized at the skill-eval tier: [[self-improving-skills]]

[[simon-scrapes]]'s 2026-05-23 [[self-improving-skills]] (109.7K views) operationalizes **Principle 2 (*ask what good looks like*) at the machine practice tier**. Where AI Question Method asks a human to specify success criteria before generation, self-improving skills encodes those success criteria as **binary criteria** that an autonomous loop optimizes against. Same principle, two levels:

- Human practice (this) → ask what good looks like before prompting
- Machine practice (self-improving skills) → encode binary criteria; autonomous loop converges

The convergence-via-binary-criteria pattern confirms Principle 2 has portable validity across human-tier and machine-tier applications.

## Related

- [[nate-b-jones]] — author; 15th + 18th frameworks
- [[project-room-workflow]] — artifact-side complement (his 18th framework, 2026-05-22)
- [[self-improving-skills]] — Principle 2 operationalized at skill-eval tier ([[simon-scrapes]] 2026-05-23)
- [[prompt-caching]] — mechanics-side complement (Nate Herk #9)
- [[karpathy-llm-wiki]] — memory-layer complement
- [[prove-it-economy]] — "opinions matter" parallel (Principle 3 ↔ chapter 20:30)
- [[free-sample-phase]] — questioning-skill is the differentiator in commoditized-model era
- [[claude-code]] — primary substrate
- [[anticipation-gap]] — permission-ladder calibrates question depth to autonomy level
- [[skill-creator]] — sister evals voice

## Used in

- [[youtube-digest-apify-2026-05-22]] — primary citation ([[nate-b-jones]] #11)
- [[youtube-digest-apify-2026-05-23]] — artifact-side complement via [[project-room-workflow]] ([[nate-b-jones]] #4); machine-tier operationalization via [[self-improving-skills]] ([[simon-scrapes]] #3)

## Open questions

- **The PRFAQ at Prime Video example** — is there a published "good" output Nate references, or is it conceptual?
- **Application to agentic pipelines** vs single-agent sessions — concrete pipeline-gate questioning patterns
- **Habit-unlearning playbook** — how do operators actually unlearn 2025-era prompt engineering?
- **Question-quality as a measurable metric** — can question-quality be evaluated independently of output-quality?
- **Cross-model portability** — does AI Question Method work the same on Opus 4.7 vs GPT 5.5 vs Gemini-equivalent?
- **Memory + question-method compounding** — does long-running memory change which question patterns work? (Important for [[karpathy-llm-wiki]] vault users)
