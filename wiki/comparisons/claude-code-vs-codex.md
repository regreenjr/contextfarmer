---
title: Claude Code vs Codex — 100-Hour Head-to-Head (Nate Herk)
category: comparison
summary: [[nate-herk]]'s 2026-05-26 100-hour same-prompts-same-builds shootout (46.2K views) — the **first explicit performance comparison** of [[claude-code]] vs [[codex]] in this vault, complementing the existing [[codex]] page (architectural-symmetry-focused). Scores three concrete deliverables side by side — **report generation, landing page, dashboard** — plus pricing and a "sketchy loophole." The framing ("Biggest comeback?" + "Codex fights back") implies Codex outperformed the Claude-default audience's priors, but the verdict (chapter 21:02) is gated to transcript. Confirms the [[free-sample-phase]] thesis is now *empirically testable* and strengthens vendor-agnostic 3Ps positioning
tags: [comparison, claude-code, codex, head-to-head, performance-shootout, 100-hours, report-showdown, landing-page, dashboard-battle, pricing, free-sample-phase, nate-herk, vendor-agnostic, substrate-choice]
sources: 1
updated: 2026-05-28
---

# Claude Code vs Codex — 100-Hour Head-to-Head (Nate Herk)

> Source: [[nate-herk]] *100 Hours Testing Claude Code vs ChatGPT Codex (honest results)* ([[youtube-digest-apify-2026-05-28]] #5, 46.2K views, 2026-05-26, 26:34)

## Why this comparison is different

The existing [[codex]] page maps **architectural symmetry** — same `CLAUDE.md` ↔ `AGENTS.md` instructions, same `skills/` format, mostly-compatible `agents/` directory (the [[nate-herk]] 3-layer cross-substrate model). That answers *"do the primitives match?"* (yes).

This video answers a **different** question: *"which one actually wins on real builds?"* — same prompts, same builds, both tools side by side for 100 hours. It is the **first performance shootout** (not architecture mapping) in the vault, and from a 708K-sub Claude-ecosystem creator whose default audience leans Claude.

## The framing

> *"Same prompts, same builds, both tools side by side, and one of them hit way harder than I expected."*

The chapter titles tell a momentum story: **"Biggest comeback?"** (00:00) → **"Claude's edge"** (04:04) → **"Codex fights back"** (06:19) → **"Honest verdict"** (21:02). The arc implies **Codex outperformed the Claude-default audience's priors** — but whether the final verdict favors Codex or names a "comeback" for Claude is **gated to the transcript**.

## The head-to-head categories

Three concrete deliverable types scored side by side:

| Category | Chapter | What it tests |
|---|---|---|
| **Report showdown** | 12:48 | Structured analytical output / document generation |
| **Landing page** | 15:10 | Frontend build quality (design + code) |
| **Dashboard battle** | 16:32 | Data-UI generation, multi-component app |
| **The numbers** | 17:25 | Quantified results across the builds |

Plus two non-build axes:

- **Pricing pain** (10:22) — the flat-fee Claude Pro/Max vs metered OpenAI-API cost difference (the long-standing [[codex]] open question, now with real usage data behind it)
- **Sketchy loophole** (09:13) — an unspecified exploit/workaround (gated to transcript; possibly a pricing or rate-limit loophole)

## What's settled vs open

**Settled (from this video + prior vault coverage):**
- The primitives match — both ship Skills, Plan Mode, scheduled automation, browser-use; projects port between them ([[codex]] 3-layer model).
- Both can produce all three deliverable types (report, landing page, dashboard) — the question is *quality/speed/cost*, not *capability*.
- Pricing models genuinely differ (flat-fee vs metered) — a real operator-economics axis, not a wash.

**Open (gated to transcript):**
- ⚠️ **The actual verdict** (chapter 21:02) — who won, and by how much. The chapter arc hints at Codex overperforming but is not conclusive.
- **Per-category winners** — does one tool win reports while the other wins frontend? (The most useful output for substrate selection.)
- **The "sketchy loophole"** — what it is and which tool it applies to.
- **Reproducibility** — single-operator, single-100-hour run; no public methodology/scoring rubric.

## Relationship to [[free-sample-phase]]

This video is the **empirical payoff** of the [[free-sample-phase]] thesis. [[nate-herk]] named the substrate-economics moment (Anthropic passes OpenAI → both labs ship retention promos: Codex 2 months free + Claude +50% limits) on 2026-05-13. The recommended play was *"use both like crazy while building swap-flexible projects."* A 100-hour head-to-head is exactly that play executed — and the near-zero cost of the Codex free window is what makes a 100-hour comparison economically feasible. Expect more such shootouts through the 2026-06/07 free-tier window.

## Why it matters for 3Ps

- **Vendor-agnostic positioning, now evidence-backed** — the same deliverables (report, landing page, dashboard) ship on both substrates. The substrate choice reduces to **performance + pricing**, not architecture lock-in. 3Ps can quote engagements in vendor-neutral terms and let the client pick.
- **A "cross-vendor substrate evaluation" is a billable engagement** — replicate the head-to-head on the client's *actual* workload during the free window; deliver a scored report + pricing model. Same shape as the [[codex]] page's "2-month consulting opportunity."
- **Pricing-model advisory** — the flat-fee vs metered axis is a real cost-structure decision at scale; the "pricing pain" chapter is the data point for client cost modeling.
- **Watch for primitive drift** — when one substrate ships a primitive the other lacks (memory, Channels, etc.), that's where vendor lock-in re-enters and the head-to-head stops being apples-to-apples.

## Sources & related

- [[youtube-digest-apify-2026-05-28]] — primary source
- [[nate-herk]] — author of the shootout; the vault's primary Codex educator
- [[claude-code]] — substrate A
- [[codex]] — substrate B; architectural-symmetry page (this comparison adds the performance dimension)
- [[free-sample-phase]] — the substrate-economics thesis this video empirically tests
- [[claude-code-levels]] — Nate Herk's Claude-side mastery framework (depth-tour companion)
- [[ai-consulting]] — vendor-agnostic deliverable positioning
