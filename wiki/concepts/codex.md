---
title: Codex (OpenAI Codex CLI)
category: concept
summary: OpenAI's coding-agent CLI; parallel substrate to Claude Code with overlapping primitives (Plan Mode, Skills, scheduled automations, browser-use); Nate Herk's 1hr full course is the first major educational entry tracked here — confirms Skills, Plan Mode, and weekly automations are cross-vendor patterns, not Anthropic-only
tags: [codex, openai, coding-agent, cli, claude-code, claude-skills, plan-mode, browser-use, cross-vendor]
sources: 1
updated: 2026-05-06
---

# Codex (OpenAI Codex CLI)

## Definition

**Codex** in 2026 refers to OpenAI's coding-agent CLI — the OpenAI counterpart to [[claude-code]]. Not the original 2021 Codex model (which is deprecated); the modern Codex is a full agentic CLI with Plan Mode, Skills, scheduled automations, browser automation, and standard ship loops (GitHub + Vercel deploy).

It is the **second tracked substrate** in this vault for AI coding agents and the first non-Anthropic one. Architectural concepts ([[claude-skills]], plan modes, [[mcp]]-equivalent connectors) appear in parallel form on both sides.

## Origin

Re-introduced by OpenAI as a coding-agent CLI in the 2025-2026 cycle. Distinct from the original 2021 Codex (the GPT-3-era code model). First major educational entry in this vault: [[nate-herk]] *Master 97% of Codex in 1 Hour (full course)* in [[youtube-digest-apify-2026-05-06]] #2.

## Key claims (from [[nate-herk]] #2 in [[youtube-digest-apify-2026-05-06]])

The 1hr course chapter list is the canonical primitive list for Codex as of 2026-05:

- **Plan Mode** (12:36) — planning step before execution; analogous to [[claude-code]] Plan Mode
- **API Setup** — paid OpenAI API integration (vs Claude Code's flat-fee Pro/Max plans)
- **Reusable Skills** (26:44) — *Codex has Skills* — the procedural-knowledge primitive that this vault has tracked as a [[claude-skills]] concept is now cross-vendor
- **Dashboard generation** (32:46) — UI surface output
- **GitHub + Vercel deploy** (38:50) — same ship loop as Claude Code
- **Weekly automations** (44:23) — scheduled execution analog to [[claude-code]] Routines / Scheduled Tasks
- **Browser Use & QA** (48:25) — browser automation, parallel to Claude Code + Playwright

Demo project in the course: a **YouTube comment intelligence system** built end-to-end. Same shape as the AIOS / vertical-stack patterns Nate Herk teaches on Claude Code.

## Cross-vendor primitive map

The architectural concepts this vault tracks port between substrates:

| Concept | [[claude-code]] | [[codex]] |
|---|---|---|
| Procedural knowledge units | Skills | Skills (per Nate Herk #2) |
| Pre-execution planning | Plan Mode | Plan Mode |
| Scheduled execution | Routines / Scheduled Tasks | Weekly Automations |
| External-tool connector | MCP / CLI | API Setup (likely OpenAI Function Calling + future MCP) |
| Browser automation | Playwright integration | Browser Use |
| Project-wide context | CLAUDE.md | (TBD — likely an analog) |
| Memory | Auto Memory | (TBD) |

**Open**: how much of the symmetry is real vs naming-borrowing. Some primitives (Skills) may be a re-implementation; others may be functionally different despite shared naming. Transcript ingest of the Nate Herk course would resolve.

## Contrasts with

- **[[claude-code]]** — the closer-cousin substrate; this vault's primary focus. Codex is currently the alternative for OpenAI-leaning operators.
- **Cursor / Antigravity / etc.** — IDE-hosted coding tools; Codex (like Claude Code) is a CLI that *can* run inside an IDE but isn't IDE-bound. [[nick-saraev]]'s recommendation of Antigravity (Gemini IDE) as Claude Code host is an analog of "use the best IDE shell for the agent CLI you prefer" — Codex would have a similar IDE pairing question.
- **Function calling / Assistants API** — Codex CLI sits *above* these as an integrated agentic stack, not just a model+API.

## Why it matters for this wiki

- **Vendor-agnostic 3Ps positioning** — clients running on OpenAI rather than Anthropic can still consume the same architectural patterns ([[claude-skills]], [[skill-systems]], [[karpathy-llm-wiki]], [[context-farming]]). The IP is portable.
- **Tracking cross-vendor primitive convergence** — when "Skills" appears in two competing CLIs, it's a strong signal that the abstraction is settling. The vault should track which concept names converge vs diverge.
- **Educational tier signal** — first 1hr Codex course from a top-tier creator (708K-sub Nate Herk) at 9.5K views is *much* lower than his Claude Code content at the same length. Codex is the lower-mainstream-attention substrate as of 2026-05; useful for tracking creator ecosystem positioning.

## Open questions / disagreements

- **Skill format compatibility** — are Codex Skills file-format-compatible with Claude Skills, or just conceptually parallel? (If compatible, the marketplace dynamic is very different.)
- **MCP support in Codex** — [[mcp]] is Anthropic-published but open. Codex adoption of MCP would be a major signal; non-adoption would be a vendor-lock signal.
- **Plan Mode semantics** — same UX, same internal mechanism, or just same word?
- **Pricing model** — flat-fee Claude Pro/Max vs metered OpenAI API is a real differentiator. Operator economics differ at scale. (See [[brad-bonanno]]'s context-bloat / cost-optimization work — applies to both vendors but mechanisms differ.)
- **Will Anthropic-ecosystem creators add Codex coverage as a hedge?** — [[nate-herk]] is the first; if [[brock-mesarich]], [[grace-leung]], [[nick-saraev]] follow, Codex graduates from "alternative" to "tracked second substrate" for the whole vault.

## Why it matters for 3Ps

- **Service offering**: 3Ps should be substrate-agnostic at the spec level. Skill Systems, context-farming, wiki patterns translate across [[claude-code]] and [[codex]] — quote in vendor-neutral terms.
- **Client choice doesn't gate the deliverable** — if a client is locked into OpenAI, the same architectural patterns ship; the 3Ps offering doesn't break.
- **Educational content angle** — Codex is currently underserved by the creator-economy compared to Claude Code; "Codex for AI consultants" content has runway if 3Ps wants the cross-vendor positioning.
- **Watch for primitive drift** — when one substrate ships a primitive the other doesn't (memory, channels, etc.), that's where the vendor-tied lock-in returns.

## Used in

- [[youtube-digest-apify-2026-05-06]] — primary source ([[nate-herk]] #2 *Master 97% of Codex in 1 Hour*)
- [[nate-herk]] — primary educator in this vault for Codex
- [[claude-code]] — sibling substrate; the cross-vendor primitive symmetry is the main connection
- [[claude-skills]] — Skills as cross-vendor primitive
- [[anticipation-gap]] — coding agents (both Codex and Claude Code) are the canonical proof that anticipation-gap-closing requires clean verification, which both have
- [[ai-consulting]] — vendor-agnostic positioning enables OpenAI-shop clients
