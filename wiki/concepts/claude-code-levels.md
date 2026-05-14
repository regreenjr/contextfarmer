---
title: Claude Code Levels (Five-Level Mastery Framework)
category: concept
summary: [[nate-herk]]'s 2026-05-12 five-level Claude Code mastery framework (73K views, 21:42) — "every level of Claude Code explained in 21 minutes"; positions Claude Code adoption as a *progression* rather than a flat primitive inventory; Level 1 = entry use, Level 2 = hidden artifacts + Office takeover (Word/PowerPoint/Excel add-ins), Level 3 = "Figma killer" ([[claude-design]]), Level 4 = Shift Tab Twice + /rewind (advanced session control), Level 5 = "five parallel sessions while they sleep" (multi-agent + Routines + Channels); credibility anchor "400 hours inside Claude"; the depth-tour companion to [[brad-bonanno]]'s 13-product breadth-tour
tags: [claude-code, mastery, framework, levels, nate-herk, agent-view, goal-command, claude-design, office-add-ins, slash-rewind, plan-mode, multi-agent, parallel-sessions]
sources: 1
updated: 2026-05-14
---

# Claude Code Levels

## Definition

A five-level mastery progression for [[claude-code]] users, ranging from entry-level CLI use (Level 1) to "running five parallel sessions while they sleep" (Level 5). Named by [[nate-herk]] in *Every Level of Claude Explained in 21 Minutes* (despite the title, the video is **specifically about Claude Code** — clarified in the description). 73.4K views in days; his most-viewed video in [[youtube-digest-apify-2026-05-14]].

## Origin

[[nate-herk]] frames it as a personal credibility claim: **"I've spent over 400 hours inside Claude, and I'm breaking down exactly what separates someone stuck on level 1 from someone running five parallel sessions while they sleep."**

Same shape as his earlier course-gated frameworks (Three Ms, Four Cs of an AIOS) — credibility anchor + named progression + course/community as the path to higher levels.

## The five levels (from chapter timestamps)

| Level | Chapter | Likely contents | Maps to |
|---|---|---|---|
| **1** | 0:12 | Entry-level Claude Code CLI use | Basic prompts + file edits |
| **2** | 1:03 → 2:13 "Hidden artifacts" → 3:35 "Office takeover" | Artifacts + Word/PowerPoint/Excel add-ins | [[brad-bonanno]]'s 13-product tour (#7-#9) |
| **3** | 4:54 → 7:21 "Figma killer?" | [[claude-design]] | "Figma killer" framing is strongest yet for Claude Design |
| **4** | 9:24 → 10:40 "Shift tab twice" → 13:54 "Slash rewind" | Advanced session control: Plan Mode toggle, `/rewind` for session state | Plan Mode + session memory |
| **5** | 15:56 | "Five parallel sessions while they sleep" | Agent View + `/goal` + Routines + Channels |

## Level-by-level interpretation

### Level 1 (0:12) — Entry-level

Basic Claude Code CLI usage: open Claude Code, ask a question, edit a file, run a command. The floor most operators stop at if they treat Claude Code as a "smart REPL."

### Level 2 (1:03) — Artifacts + Office takeover

Two distinct sub-skills:

- **Hidden artifacts** (2:13) — likely the artifact panel / live editing surface that ships with Claude Code's full UI
- **Office takeover** (3:35) — Word add-in (#7 in [[brad-bonanno]]'s 13-product tour) + PowerPoint add-in (#8) + Excel add-in (#9). This is the "Claude Code edits your Office docs" use case.

Implication: most users don't know the Office add-ins exist. Level 2 is "unlock the surface you didn't know was there."

### Level 3 (4:54) — "Figma killer?"

[[claude-design]] gets the strongest competitive-substitute framing seen in this vault. Earlier coverage ([[nate-herk]]'s #18 in [[youtube-digest-apify-2026-05-03]] — *Claude Design 2 HOUR COURSE*) framed it as a standalone tool. Here he frames it as the **Figma replacement**.

This is significant for [[claude-design]]'s positioning trajectory:
- 2026-05-03: "Claude Design is a tool, learn it"
- 2026-05-12: "Claude Design is the Figma killer, switch"

Same creator (Nate Herk), increasing aggression in framing over six weeks.

### Level 4 (9:24) — Shift Tab Twice + /rewind

Two advanced primitives:

- **Shift Tab Twice** (10:40) — likely Plan Mode toggle or alternate UI mode. Not previously documented in this vault. Possibly: first Shift+Tab opens Plan Mode, second Shift+Tab opens an alternate planner/explorer surface.
- **Slash Rewind** (13:54) — likely `/rewind` for session state. Pairs with [[claude-code]]'s Auto Memory primitive (persistent file-based memory) — `/rewind` is the rollback companion to Auto Memory's forward-persistence.

Level 4 is **advanced session control** — the user has graduated from individual interactions to managing the *state of a session* over time. Same shape as a developer graduating from "I write code" to "I manage the codebase."

### Level 5 (15:56) — Five parallel sessions

The capstone. Likely uses:

- **Agent View** (the 2026-05-12 multi-session-per-terminal-tab primitive, covered by [[nate-herk]] #2 in [[youtube-digest-apify-2026-05-12]])
- **`/goal` command** (the long-running-agent primitive that ships with Agent View)
- **Routines** (cloud-scheduled work)
- **Channels** (Telegram surface, so the user can check progress remotely)

The "while they sleep" framing implies **autonomous parallel execution** — the agents work in parallel without per-action approval. The architectural pattern requires:
- A trustworthy verification path (probably tests/checks per [[anticipation-gap]]'s clean-verification claim for coding agents)
- An action-risk strategy (likely matches [[agent-security]]'s four-class taxonomy: high-stakes actions still confirmed, write actions delegated)
- A judge layer for unsafe actions ([[agent-security]] architectural pattern)

## Strategic significance

### First mastery framework for Claude Code in this vault

Existing [[claude-code]] coverage documents *primitives* (Skills, MCP, Routines, etc.) and *frameworks* (Three Ms, Four Cs, plugins taxonomy, work primitive). This is the first **user-progression framework** — what to learn first, second, third.

Useful for any onboarding deliverable (3Ps consulting or user-self-onboarding).

### Pairs with [[brad-bonanno]]'s 13-product breadth-tour

| Dimension | [[brad-bonanno]] #2 in [[youtube-digest-apify-2026-05-10]] | [[nate-herk]] #6 in [[youtube-digest-apify-2026-05-14]] |
|---|---|---|
| Axis | **Breadth** (13 products) | **Depth** (5 mastery levels) |
| Goal | Inventory awareness | Progression path |
| Audience | "What does Anthropic actually ship?" | "Where am I stuck and what's next?" |

**Together they form the canonical Claude Code onboarding kit** — Brad answers *"what is there?"*, Nate Herk answers *"how do I level up?"*.

### "Figma killer" is the cleanest [[claude-design]] positioning yet

Earlier Claude Design coverage was tool-focused. The "Figma killer?" framing is **category-attack framing** — Figma is the dominant design tool, calling Claude Design its killer is a direct competitive claim. Worth tracking whether other creators adopt the framing.

### Level 5 implicitly confirms [[agent-view]] / [[goal-command]] adoption trajectory

"Five parallel sessions while they sleep" is precisely the use case [[nate-herk]]'s 2026-05-12 Agent View walkthrough enabled. Two videos in three days — first showing the primitive, then framing it as the Level 5 mastery target. Tight feedback loop between primitive shipping and creator-mastery positioning.

## Open questions / things to verify from transcript

- **Shift Tab Twice** — what exactly does this do? Plan Mode? An alternate explorer? A different keystroke shortcut?
- **`/rewind`** — when did this ship? It's not in this vault's existing Claude Code primitive list. New 2026-05 primitive?
- **Level 5 specifics** — does he actually demo five parallel agent sessions, or is that a marketing flourish?
- **"Hidden artifacts"** at Level 2 (2:13) — what's "hidden" about them? Is this the new Live Artifacts surface from Brad's Phase 2 tour?
- **Level progression assumes Claude Code Plus/Pro?** — Level 5 (parallel sessions) likely requires the higher tier
- **Does level 5 include sub-agents or stay at top-level agent multiplicity?**

## Why it matters for 3Ps

### Direct onboarding artifact

The five levels are **a ready-made client onboarding rubric**. A 3Ps engagement can map any client to a level, identify the next-level skills, and design the gap-closing program. This is **faster intake** than starting from scratch.

### Content gap to fill

[[nate-herk]]'s framework is **broad** but **gated** — the 21-minute video is the high-level overview; specifics live in his Skool community. 3Ps content can:
- Document the specific primitives at each level (filling the transcript-pull gap)
- Add the consulting-relevant level overlays (e.g., Level 5 + multi-client orchestration)
- Build the **migration guide** from each level to the next (specifically the Level 3→4 and Level 4→5 jumps — where Plan Mode + `/rewind` + Agent View live)

## Related pages

- [[claude-code]] — primary substrate
- [[claude-design]] — Level 3 ("Figma killer")
- [[nate-herk]] — primary author; this is his ninth+ Claude Code framework
- [[brad-bonanno]] — 13-product breadth-tour companion
- [[anticipation-gap]] — Level 5 ("while they sleep") requires anticipation-gap-closing for autonomous operation
- [[agent-security]] — Level 5 autonomous operation requires action-risk management
- [[youtube-digest-apify-2026-05-14]] — primary citation
- [[youtube-digest-apify-2026-05-12]] — Agent View + `/goal` primitives (Level 5 enablers)

## Used in

- [[youtube-digest-apify-2026-05-14]] — primary citation ([[nate-herk]] #6)
- [[claude-code]] — onboarding/mastery framework
- [[nate-herk]] — primary author
