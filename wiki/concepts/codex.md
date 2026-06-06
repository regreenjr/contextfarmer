---
title: Codex (OpenAI Codex CLI)
category: concept
summary: OpenAI's coding-agent CLI; parallel substrate to Claude Code with overlapping primitives (Plan Mode, Skills, scheduled automations, browser-use); 2026-05-13 ships Codex free for 2 months as retention play after Anthropic adoption flip; **2026-05-18 [[nate-herk]] publishes the 3-layer cross-substrate mental model** — Claude Code's `CLAUDE.md` ↔ Codex's `AGENTS.md` (instructions), skills directory (same format), agents directory (mostly compatible) — confirming cross-substrate symmetry at the *project filesystem* level, not just per-primitive; the conversion-prompt for migrating an entire project from Claude Code → Codex (or vice-versa) is now published — extends the substrate-portability playbook + makes the [[free-sample-phase]] retention war exploitable as a defensive strategy; **in 2026-05-28 [[nate-herk]]'s 100-hour [[claude-code-vs-codex]] shootout** ships the first *performance* comparison (vs prior architectural-symmetry coverage) — report/landing-page/dashboard scored head-to-head, "Codex fights back" arc implies Codex overperformed Claude-default priors (verdict gated to transcript)
tags: [codex, openai, coding-agent, cli, claude-code, claude-skills, plan-mode, browser-use, cross-vendor, retention-promo, free-sample-phase, business-adoption, codex-enterprise, agents-md, cross-substrate-3-layer, instructions-layer, project-portability, claude-code-vs-codex, head-to-head, performance-shootout, 100-hours, report-showdown, dashboard-battle, pricing-pain, harness-over-model, codex-harness, routing-guide, nate-b-jones, gpt-5-5, token-burn-dashboard, 800-million-tokens, self-instrumentation, feedback-loop, tufte, multi-agent]
sources: 6
updated: 2026-06-06
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

## 2026-05-13 retention promo: Codex free for 2 months (per [[nate-herk]] #5 in [[youtube-digest-apify-2026-05-14]])

Major behavioral break for OpenAI's Codex monetization stance:

- **Trigger event**: per a Ramp / EconLab article, [[anthropic]] passed [[openai]] in business adoption for the first time on 2026-05-13
- **Within hours**: OpenAI ships **Codex free for 2 months**, gated via the Codex Enterprise application form (`openai.com/form/codex-enterpr...`)
- **Symmetric move from Anthropic**: [[claude-code]] rate limits +50%

### Why this matters for Codex specifically

1. **First OpenAI retention promo tracked here** — prior to 2026-05-13, OpenAI's Codex stance was strict (paid tiers, metered API, no major free promos). The 2-months-free move is a meaningful behavioral break.
2. **Cost differential for cross-vendor experimentation drops to near-zero** during the 2-month window. Operators who would otherwise default to [[claude-code]] now have a free path to test Codex's Skills / Plan Mode / weekly automations / browser-use stack.
3. **Codex Enterprise gating** suggests the promo targets *business buyers* — same persona as the lost adoption lead. Not a broad consumer move.
4. **Educational on-ramp arbitrage** — [[nate-herk]]'s prior 1hr Codex course (9.5K views in [[youtube-digest-apify-2026-05-06]]) lands at a moment when free-tier Codex is suddenly cheap to follow along with. Expect Codex tutorial views to spike in the 2026-06 / 2026-07 timeframe.
5. **The dethroned-leader play** in [[nate-herk]]'s [[free-sample-phase]] framing — when adoption flips, the trailing vendor's first move is a free-tier promo to capture switching costs before they consolidate

### Strategic implications

- **Cross-vendor Skills experimentation just got cheaper** — operators can verify the Anthropic-Codex Skills format compatibility / API differences with 2 months of free Codex usage
- **Anthropic-ecosystem creators may add Codex coverage opportunistically** — if [[brock-mesarich]] / [[grace-leung]] / [[nick-saraev]] follow [[nate-herk]] in covering Codex during the free window, Codex graduates from "alternative substrate" to "tracked second substrate" for the whole vault
- **Pricing model differences become testable** — operators can compare Codex's metered API model vs Claude Code's flat-fee Pro/Max economically for 2 months, generating reusable benchmark data
- **Open question**: does the 2-months-free conversion sticky? Empirical resolution by 2026-08

### For 3Ps

This is a **2-month consulting opportunity** — 3Ps clients who want to evaluate Codex vs Claude Code can do so during the free window with no incremental cost. A "cross-vendor substrate evaluation" engagement is more attractive now than at any prior point. The same architectural patterns (Skills, Plan Mode, [[skill-systems]], [[execution-layer]], [[retrieval-contract]]) port across both substrates per the vendor-agnostic positioning thesis.

→ See [[free-sample-phase]] for the broader substrate-economics framing.

## 3-Layer cross-substrate mental model ([[nate-herk]] in [[youtube-digest-apify-2026-05-22]])

[[nate-herk]]'s 2026-05-18 *How to Use Your Claude Code Projects in Codex in 5 Mins* (24.6K views, 8:39) ships the canonical **3-layer mental model** for cross-substrate work:

| Layer | Claude Code artifact | Codex artifact | Compatible? |
|---|---|---|---|
| **Instructions** | `CLAUDE.md` | `AGENTS.md` | Yes — same content, different filename |
| **Skills** | `skills/` directory | `skills/` directory | Yes — same format |
| **Agents** | `agents/` directory | `agents/` directory | Mostly compatible — minor schema deltas |

**Cross-substrate symmetry now confirmed at the *project filesystem* level**, not just per-primitive. Entire projects copy-paste between substrates with the conversion prompt Nate publishes in the video.

**Chapter map**:
- 0:00 Intro
- 0:29 Claude vs Codex File Structure
- 3:05 Skills & Agents Compared
- 4:17 **The 3-Layer Mental Model**
- 5:13 Convert Any Project Fast
- 6:23 Using Both Together
- 8:11 Final Thoughts

**Strategic significance**:

1. **Confirms [[free-sample-phase]] thesis in concrete portability terms** — "use both at once" is the canonical defensive strategy
2. **The 3-layer model is a portable architectural primitive** — applies symmetrically to [[hermes-agent]] / [[claude-code]] / [[codex]]
3. **First conversion prompt published** for Claude Code ↔ Codex auto-migration — extends substrate-portability playbook
4. **This vault's `CLAUDE.md` + `AGENTS.md`** parallel files are the architectural artifact this video formalizes — the vault was already running the pattern; Nate names it

## 100-hour performance shootout ([[nate-herk]] in [[youtube-digest-apify-2026-05-28]])

[[nate-herk]]'s 2026-05-26 *100 Hours Testing Claude Code vs ChatGPT Codex (honest results)* (46.2K views, 26:34) is the **first performance comparison** of the two substrates in this vault. Prior coverage on this page was **architectural symmetry** (do the primitives match? — yes, via the 3-layer cross-substrate model). This video answers the *different* question: **which one wins on real builds?**

Three deliverable types scored head-to-head: **report showdown** (12:48), **landing page** (15:10), **dashboard battle** (16:32) — plus **pricing pain** (10:22, the flat-fee-vs-metered axis with real usage data, resolving a standing open question on this page) and a "sketchy loophole" (09:13). The chapter arc ("Biggest comeback?" → "Claude's edge" → "Codex fights back" → "Honest verdict") implies **Codex overperformed the Claude-default audience's priors**, but the verdict (21:02) is gated to transcript.

Strategic significance: confirms the [[free-sample-phase]] thesis is now *empirically testable* (a 100-hour comparison is only feasible because of the near-zero-cost Codex free window) and strengthens vendor-agnostic positioning — same deliverables ship on both, so the choice is performance/pricing, not architecture. → See [[claude-code-vs-codex]] for the full comparison.

## "The Codex harness outperformed raw model intelligence" ([[nate-b-jones]] in [[youtube-digest-apify-2026-06-05]])

[[nate-b-jones]]'s *Opus 4.8 Scored 81. Your Workflow Doesn't Care.* (34.3K views, 2026-06-03) gives Codex its **strongest competitive endorsement** in the vault — not on architecture (the 3-layer symmetry above) or a scored deliverable shootout (the 100-hour comparison above), but on the **harness**:

- **The Codex harness outperformed raw model intelligence** — in his real-work tests, Codex's harness produced better outcomes than a higher-scoring model run in a weaker harness. → See [[harness-over-model]].
- **He still reaches for [[codex]]/5.5 daily *despite the lower benchmark score***. The clearest single instance of the harness-over-model thesis: model choice is a harness/workflow-fit decision, not a leaderboard lookup.
- **A published routing guide** (Substack-gated): when to use [[opus-4-8]] vs **Codex/5.5** vs GPT-5.5 for real work.

This reframes the prior [[claude-code-vs-codex]] performance shootout: it's not just that Codex ships comparable deliverables — its **harness can beat a higher-scoring Claude model on real work.** Strengthens the vendor-agnostic positioning *and* gives Codex a concrete "why you might prefer it" beyond price. → See [[harness-over-model]].

## Contrasts with

- **[[claude-code]]** — the closer-cousin substrate; this vault's primary focus. Codex is currently the alternative for OpenAI-leaning operators. Head-to-head performance now tracked in [[claude-code-vs-codex]].
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

## Heavy-usage substrate — 800M tokens/day + the token-burn dashboard ([[nate-b-jones]] in [[youtube-digest-apify-2026-06-06]])

[[nate-b-jones]]'s *My Codex Ran 800 Million Tokens in A Day. The Real Story Isn't Cost.* (14.5K views) uses **Codex as the substrate for a heavy-usage self-instrumentation experiment** → new concept [[token-burn-dashboard]]. He burned **~800 million tokens in a single day** on Codex and **built the token-burn dashboard itself in Codex** — computer-work building the tool that measures computer-work.

Two things this confirms about Codex specifically:

1. **Codex sustains extreme token throughput** — an 800M-token day (log-scale charting required) is a datapoint on Codex's heavy-multi-agent-usage ceiling, relevant to the metered-API cost model (vs Claude's flat-fee) the [[claude-code-vs-codex]] "pricing pain" segment flagged.
2. **The "Codex harness" thesis extends from quality to behavior** — where [[harness-over-model]] said *"the Codex harness outperformed raw model intelligence"* on output quality, the token-burn experiment says the harness also shapes *operator behavior* (multi-agent runs reveal real habits; assistant-work vs computer-work is a habit, not a model question). *"Being stuck on the wrong side has nothing to do with the model."*

→ See [[token-burn-dashboard]].

## Used in

- [[youtube-digest-apify-2026-05-06]] — primary source ([[nate-herk]] #2 *Master 97% of Codex in 1 Hour*)
- [[youtube-digest-apify-2026-05-14]] — secondary source: 2-months-free retention promo following the Anthropic adoption flip ([[nate-herk]] #5)
- [[youtube-digest-apify-2026-05-28]] — 100-hour Claude Code vs Codex performance shootout ([[nate-herk]] #5)
- [[youtube-digest-apify-2026-06-05]] — "the Codex harness outperformed raw model intelligence" ([[nate-b-jones]] #1)
- [[youtube-digest-apify-2026-06-06]] — 800M-token day + token-burn dashboard built in Codex ([[nate-b-jones]] #3)
- [[harness-over-model]] — the Codex-harness-beat-the-score thesis + routing guide
- [[token-burn-dashboard]] — 800M tokens/day on Codex; the dashboard was built in Codex
- [[claude-code-vs-codex]] — the head-to-head comparison page (performance dimension)
- [[nate-herk]] — primary educator in this vault for Codex
- [[openai]] — Codex vendor; retention-promo signal
- [[claude-code]] — sibling substrate; the cross-vendor primitive symmetry is the main connection
- [[claude-skills]] — Skills as cross-vendor primitive
- [[free-sample-phase]] — substrate-economics framing for the 2-months-free promo
- [[anticipation-gap]] — coding agents (both Codex and Claude Code) are the canonical proof that anticipation-gap-closing requires clean verification, which both have
- [[ai-consulting]] — vendor-agnostic positioning enables OpenAI-shop clients
- [[execution-layer]], [[retrieval-contract]], [[skill-systems]] — vendor-agnostic architectural patterns that port to Codex
