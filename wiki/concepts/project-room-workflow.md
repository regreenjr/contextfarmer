---
title: Project Room Workflow (Canvas Before Prompt)
category: concept
summary: [[nate-b-jones]]' 18th named framework (2026-05-22, 22.3K views) — the **canvas-shaping discipline** that makes AI hallucinations *structurally unlikely* in high-stakes knowledge work; unlock event is **prestigious law firms (Sullivan & Cromwell) filing federal-court motions full of AI hallucinations** despite frontier-model access; counter-claim to "better prompts prevent hallucinations" — the real fix is **shaping the canvas before the writing starts**; three first-prompt artifacts (**source inventory table** + **conflict log** + **missing context list**) build the canvas the agent works in, after which the writing prompt itself becomes short; enabled by **Opus 4.7 + GPT-5.5 capability jump** (agents now walk folder trees and compare files cleanly); the **artifact-side complement** to [[ai-question-method]] (his 15th framework) — Question Method = questioning discipline (flashlight / good / wrestle); Project Room = artifact discipline (inventory / conflicts / gaps); pairs with [[self-improving-skills]] (Simon Scrapes in same batch) as **"before-the-work artifact"** sibling frameworks; confirms [[karpathy-llm-wiki]] / vault architecture (`raw/` → `wiki/` + `> ⚠️ Contradiction:` callouts) as canonical at the per-task scale
tags: [project-room-workflow, canvas-shaping, agentic-engineering, sullivan-cromwell, hallucination, source-inventory, conflict-log, missing-context-list, opus-4-7, gpt-5-5, folder-tree-walking, files-as-canvas, knowledge-work, ai-question-method-complement, nate-b-jones, framework-17, pre-prompt-artifact, duplicate-reasoning, writing-prompt, knowledge-quality-infrastructure]
sources: 1
updated: 2026-05-23
---

# Project Room Workflow

## What it is

[[nate-b-jones]]' 18th named framework — a **canvas-shaping discipline** for high-stakes knowledge work with AI agents. Instead of going from "messy sources" directly to "write the thing," operators build a **project room** (a working filesystem with explicit canvas artifacts) **before** issuing the writing prompt. The discipline makes hallucinations *structurally unlikely* because the agent's available context is curated, deduplicated, and gap-named.

Source: [[nate-b-jones]] *The One AI Writing Hack Nobody Talks About.* (22.3K views, 2026-05-22, 21:50), surfaced via [[youtube-digest-apify-2026-05-23]].

## The framing claim

*"What's really happening when prestigious law firms file motions full of AI hallucinations? The common story is that better prompts prevent hallucinations — but the reality is that operators doing high-stakes knowledge work with AI agents need to shape the canvas before the writing starts, or they ship the same soft spots that landed Sullivan and Cromwell in front of a federal judge."*

## The Sullivan & Cromwell unlock event

The unlock event for the framework: **Sullivan & Cromwell** (top-tier US law firm) filed federal-court motions containing AI hallucinations — invented citations, misattributed case law, made-up factual claims. The firm has frontier-model access. Their prompts are presumably well-crafted. Yet they shipped soft spots that landed them in front of a federal judge.

Nate's diagnosis: **the failure is upstream of the prompt**. No prompt could have fixed the failure mode because the agent's available context contained the messy source material that *caused* the hallucinations.

Pairs with the vault's other named-firm AI-failure unlock events:

| Failure | Firm | Framework |
|---|---|---|
| Hallucinated motions | Sullivan & Cromwell | **Project Room Workflow (this)** |
| SQL injection via 22 unauthenticated endpoints | McKinsey's Lilly platform | [[agent-security]] (procurement + judge architecture) |
| 271 vulnerabilities in Firefox | Mozilla (via Anthropic's Mythos) | [[code-comprehensibility]] |

Nate's pattern: **prestigious organization fails publicly → extract the structural lesson → build a framework around it**.

## Why better prompts cannot fix this (chapter 1:30)

Prompt engineering operates **inside** the agent's available context. If the available context is messy — duplicate sources, contradictory claims, gaps — no prompt-level adjustment can rescue the output. The hallucination is **a canvas-shape failure**, not a model failure or prompt failure.

The deeper claim: **hallucinations are downstream of source quality, and source quality is upstream of any prompt**.

## What changed with Opus 4.7 and GPT-5.5 (chapter 3:00)

The 2026-Q2 model capability jump enables the workflow:
- **Agents now walk folder trees and compare files cleanly** — pre-4.7, you had to feed the model curated chunks; post-4.7, the agent can navigate a project structure on its own
- **Multi-file reasoning is reliable** — the agent can build the source inventory, conflict log, and missing context list itself, given a folder of raw materials
- **Files become the canvas, not the prompt window** — the unit of work is the file, not the message

The capability shift is **the precondition** for the workflow. Pre-Opus-4.7, project-room-workflow would have required human file-curation labor that exceeded the labor saved.

## Three first-prompt artifacts

The Project Room Workflow has three canvas artifacts, built as outputs of the **first prompt** (before any writing prompt):

### 1. Source inventory table (chapter 12:00)

A structured table of every source in scope:

| Field | Purpose |
|---|---|
| Name | Source identifier |
| Path | File location in the project room |
| Type | Article / paper / transcript / brief / etc. |
| Date | Publication / creation date |
| Authoritativeness | First-party / second-party / community / unknown |

The inventory makes **scope visible**. Both the agent and the reviewer can see exactly what's in and what's not. If a source isn't in the inventory, the agent cannot rely on it.

### 2. Conflict log (chapter 14:00)

A list of **explicit contradictions across sources**:

> ⚠️ Source A (page 3) claims X. Source B (page 7) claims not-X. Both cited inline.

Conflicts are surfaced **before** the writing prompt. The agent can then either:
- Acknowledge the conflict in the deliverable (transparent uncertainty)
- Defer to the higher-authoritativeness source (explicit choice)
- Flag the conflict for human resolution

Same shape as this vault's `> ⚠️ Contradiction:` callouts on entity pages.

### 3. Missing context list (chapter 15:30)

Named **gaps**: what *should* be in scope but isn't. Examples:
- "No source covers regulatory exposure in EU jurisdictions"
- "No source published after [date]"
- "No first-party data on customer churn rate"

The list makes **what the agent doesn't know explicit**. The agent can then either:
- Note the gap in the deliverable ("EU exposure not assessed; would require [source type]")
- Refuse to make claims in the gap area
- Request the missing material before proceeding

## Why duplicates are a reasoning problem (chapter 17:00)

The deep claim. Duplicate sources don't just waste tokens; they **break the agent's reasoning**. The agent sees the same claim twice and treats it as **two independent confirmations** of the claim — increasing its weight. But the two sources are actually one source citing itself, which provides **zero additional evidence**.

Dedup discipline is therefore **information-quality infrastructure**, not just hygiene. The conflict log + dedup pass during canvas-shaping is **structural** — it shapes how the agent weighs evidence in the final output.

## Files as the canvas for agentic work (chapter 18:30)

The substrate claim: **the filesystem is the canvas**, not the prompt window. Implications:
- Files persist across agent runs (the canvas survives session restarts)
- Humans can inspect files independently (verifiability)
- Revisions happen at the file level, not the message level
- Diffs between revisions are tractable (git, file comparisons)
- The agent can reference specific files by path in deliverables

This is structurally identical to the [[karpathy-llm-wiki]] architecture — `raw/` for sources (immutable), `wiki/` for the agent's compiled understanding (canonical), source pages for citation, contradiction callouts for conflicts. **The vault implements project-room-workflow at the wiki-scale**; Nate's framework names the per-task instantiation.

## The short writing prompt that finally works (chapter 20:00)

The output of the workflow: **the writing prompt becomes short**. Because the canvas does the heavy lifting:
- The inventory tells the agent what sources to use
- The conflict log tells the agent how to handle disagreement
- The missing context list tells the agent what *not* to claim

The writing prompt itself becomes something like: *"Using the source inventory at X, the conflict log at Y, and the missing context list at Z, draft [deliverable]. Cite by source path. Flag any new conflicts in the conflict log."*

Short prompt + rich canvas = reliable output.

## Where to build your room across tools (chapter 10:30)

Tool-independent — the artifacts can be built in:

| Tool | Project room location |
|---|---|
| Claude Code | CLAUDE.md + `raw/` folder + `wiki/` folder (this vault's shape) |
| Cursor | `.cursor/` + workspace |
| ChatGPT Projects | Uploaded files + Project instructions |
| [[manus]] | Workspace + source ingest |
| [[notebooklm]] | Source list + notebook |
| [[codex]] | AGENTS.md + `raw/` folder |
| [[hermes-agent]] | VPS filesystem + GitHub backup |

The artifacts are **portable across substrates**. The Project Room Workflow is a substrate-independent discipline.

## Three takeaways for serious knowledge work (chapter 4:30)

Nate's diagnostic framing:
1. **Your first AI prompt should never be "do the thing"**
2. **Agents now walk folder trees and compare files cleanly** (post-Opus-4.7 capability)
3. **Artifacts make an agent's judgment visible and inspectable**

Each takeaway names a pre-prompt requirement. Together they form the **pre-prompt discipline** at the operational tier.

## Why your first prompt is never "do the thing" (chapter 6:00)

The canonical statement of the workflow. Most operators issue a single "do the thing" prompt and ship the soft spots. The Project Room Workflow inverts this — **the first prompt builds the canvas; the second prompt does the thing**. The discipline is the sequencing.

## Strategic positioning

### Complement to [[ai-question-method]]

Nate B Jones shipped [[ai-question-method]] (15th framework, 2026-05-21) and Project Room Workflow (18th framework, 2026-05-22) on consecutive days. The two are **complementary disciplines** above the prompt:

| Framework | Discipline | Pre-prompt requirement |
|---|---|---|
| [[ai-question-method]] | **Questioning** | Flashlight intent + ask what good looks like + wrestle with data |
| **Project Room Workflow (this)** | **Artifacts** | Source inventory + conflict log + missing context list |

Both target the same gap: **junior-teammate prompting wastes Opus-4.7-era agent capability**. Question Method shapes *what you ask*; Project Room shapes *the canvas the agent works in*. Together they form the **complete pre-prompt workflow**.

### Sibling framework to [[self-improving-skills]]

[[simon-scrapes]] shipped [[self-improving-skills]] in the same 2026-05-23 batch. The two are **"before-the-work artifact" sibling frameworks**:

| Framework | Pre-work artifact | Domain |
|---|---|---|
| **[[self-improving-skills]]** | Binary criteria (per-skill) | Skill authoring |
| **Project Room Workflow (this)** | Source inventory + conflict log + missing context (per-task) | Writing / knowledge work |

Both reject the "just prompt better" frame. Both name **what the agent needs *before* doing the work**. Both encode the success criteria / canvas explicitly so the agent's run becomes reliable.

### Builds on [[karpathy-llm-wiki]]

The Project Room Workflow is structurally identical to the LLM Wiki architecture at the per-task scale:

| Wiki architecture | Project Room equivalent |
|---|---|
| `raw/` (immutable sources) | Source folder in the project room |
| Source pages (one per source) | Source inventory table row |
| `> ⚠️ Contradiction:` callouts | Conflict log entry |
| Open questions / "we don't know" notes | Missing context list entry |
| Wiki linting | Pre-prompt canvas review |
| Wiki query | Writing prompt with canvas references |

The vault implements project-room-workflow at the **wiki scale** (durable, multi-task knowledge base); Nate's framework names the **task scale** (per-deliverable canvas).

### Validates the [[capital-allocation-framework]] failure mode

The capital-allocation framework named *"Do not automate what you cannot describe"* (chapter 31:52 of #5 in 2026-05-22 batch). Project Room Workflow operationalizes the inverse: **before automating, build the description** (source inventory + conflict log + missing context list). The canvas *is* the description.

## Strategic significance

1. **18th [[nate-b-jones]] framework** — extends framework cadence to **18 in 20 days** (T/C/L/D 2026-05-04 → project-room-workflow 2026-05-22)
2. **Confirms [[karpathy-llm-wiki]] architecture as canonical** — at the per-task scale, the vault's `raw/` → `wiki/` + contradiction-callouts shape is what Nate is naming
3. **The Sullivan & Cromwell unlock joins McKinsey-Lilly + Mozilla-271** as the third **named-firm 2026 AI-failure unlock event** in this vault — pattern of high-stakes failures driving framework production continues
4. **Files-as-canvas is portable across substrates** — applies to [[claude-code]] / [[codex]] / [[cursor]] / [[manus]] / [[notebooklm]] / [[hermes-agent]]
5. **Substack monetization** — *"Full Post w/ Prompt Pack: natesnewsletter.substack.com/..."* — Nate's standing distribution pattern (paywall the operational checklist behind newsletter signup)
6. **Audience-tier signal**: 22.3K views on a workflow video is mid-range for him — process content underperforms framework content even from the same creator (same pattern as [[nate-herk]]'s [[deployment-framework]] underperforming [[claude-code-levels]])

## Open questions

- **Automation tier** — can the first-prompt artifact generation be itself automated via a Claude Code skill / [[self-improving-skills]] loop?
- **Skill-creator integration** — could a `/project-room-init` skill ship as part of [[claude-skills]]?
- **Cross-task reuse** — should source inventories / conflict logs persist across tasks (wiki-scale) or be task-scoped?
- **Conflict log maintenance** — who updates the log when new sources arrive mid-project?
- **Authoritativeness scoring** — how does the agent score authoritativeness without explicit human input?
- **Integration with [[ai-question-method]]** — is there a unified "pre-prompt workflow" that combines questioning + canvas-shaping into one practice?
- **Prompt Pack contents** — what's in the Substack paywalled prompt pack? Worth tracking as competitive product analysis.
- **Cursor / Codex parity** — does Nate's workflow assume Claude Code, or does he name multi-substrate implementations?

## Related pages

- [[nate-b-jones]] — creator (18th framework)
- [[ai-question-method]] — sister framework (questioning discipline complement)
- [[self-improving-skills]] — sibling framework in same batch (before-the-work artifact pattern)
- [[karpathy-llm-wiki]] — canonical wiki-scale instantiation of the same primitives
- [[claude-code]] — substrate (Opus 4.7 folder-tree-walking enables this)
- [[capital-allocation-framework]] — "do not automate what you cannot describe" failure mode operationalized
- [[agent-security]] — companion "named-firm AI failure" unlock event (McKinsey-Lilly)
- [[code-comprehensibility]] — companion "named-firm AI failure" unlock event (Mozilla 271)
- [[anticipation-gap]] — sister discipline (proactive supervision before action)
- [[skill-creator]] / [[self-improving-skills]] — eval-tier complements
- [[manus]] / [[notebooklm]] / [[claude-for-small-business]] — substrate alternatives that can host the workflow
- [[youtube-digest-apify-2026-05-23]] — citation
