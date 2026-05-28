---
title: Kevin Stratvert
category: entity
summary: Mainstream office-productivity tutorial YouTuber; first **office-productivity tutorial tier** voice for [[claude-skills]] tracked in this vault — his 2026-05-27 *Claude Skills Tutorial* (9.5K views, hosted by David DeWinter, sponsored by Intuit/QuickBooks) is the **first vault coverage of skills running across the full surface set (Chat + Cowork + Claude Code)** and resolves the long-open "are skills Code-only?" question; demos a from-scratch "Thread Reply" skill *with test cases that grade it before saving* ([[skill-creator]] eval discipline for non-developers) + four ways to share a skill including a synced shared folder without a Team/Enterprise plan
tags: [creator, youtube, office-productivity, tutorial, claude-skills, chat-cowork-claude-code, cross-surface-skills, thread-reply-skill, david-dewinter, intuit, quickbooks, skill-sharing, shared-folder, non-developer, mainstream-tutorial, business-operator]
sources: 1
updated: 2026-05-28
---

# Kevin Stratvert

## What it is

YouTube channel **Kevin Stratvert** — a mainstream **office-productivity / software-tutorial** brand (Microsoft 365, Google Workspace, Windows, and increasingly AI tools). Known for clean, beginner-friendly, business-operator-facing walkthroughs. The 2026-05-27 Claude Skills video was **hosted by David DeWinter** (a presenter on the channel) and **sponsored by Intuit / QuickBooks Workforce** — a business-software sponsor consistent with the channel's office-operator audience.

## Why it matters for this wiki

Kevin Stratvert is the **first office-productivity-tutorial-tier** voice for [[claude-skills]] tracked in this vault — a different audience than every prior skills creator. The existing explainer funnel ran developer → operator → beginner; Stratvert adds the **business-software-tutorial** lane (the audience that watches "how to use a pivot table" content), reached through a QuickBooks sponsorship.

Two things make the video high-signal despite its modest 9.5K views:

1. **First cross-surface coverage** — the same skill demonstrated running across **Chat + Cowork + Claude Code**, not Claude-Code-only. This **resolves a standing open question** on the [[claude-skills]] page: *"Skills are Code-only today; will they work in the Claude.ai chat surface?"* → yes.
2. **Eval discipline for non-developers** — the "Thread Reply" skill is built *with test cases that grade it before you save it* — the [[skill-creator]] eval pattern, surfaced for an audience that has never written a unit test.

## The video — *Claude Skills Tutorial (2026): Chat, Cowork, and Claude Code*

**9.5K views, 2026-05-27, 14:32. Host: David DeWinter. Sponsor: Intuit / QuickBooks Workforce.**

What it covers:
- **What a Claude Skill is** + how Claude stores dozens of skills without slowing down (progressive disclosure / load-on-trigger).
- **Build a "Thread Reply" skill from scratch** — replies to long missed email threads — *complete with test cases that grade the skill before you save it*.
- **Skills against internal app data** to validate business rules.
- **Running the same skill inside Claude Cowork** on a local folder that holds more business context.
- **Claude Code handles skills differently** — skills live as folders on disk in `.claude/skills`.
- **Four ways to share a skill with a team** — including a **synced shared folder** so a sub-team runs the same skill *without a Team or Enterprise plan*.

Chapter map (truncated in source): 0:00 Skills in 2026 · 1:14 Create a Skill · 3:05 [truncated].

Resources cited: a Google-Doc resource guide (prompts + commands), `claude.ai` (Chat), `claude.com/download` (Desktop / Cowork).

## Strategic significance

1. **Skills are surface-portable, not Code-bound** — the canonical demonstration that the [[claude-skills]] primitive spans Chat ↔ Cowork ↔ Code. Combined with [[codex]] (vendor-portable), skills are now confirmed portable on **both** axes: surface and vendor.
2. **The "share without Team/Enterprise plan" mechanic** is a real distribution detail — a synced shared folder lets a sub-team run the same skill on a free/Pro tier. Lowers the team-distribution floor below [[plugin-marketplace]] (GitHub-hosted) and [[execution-layer]] (private team marketplace).
3. **QuickBooks sponsorship places skills in the SMB-accounting audience** — same buyer as [[claude-for-small-business]]' QuickBooks connector. The skills message is reaching business operators through their accounting-software content diet.
4. **Eval discipline goes mainstream-tutorial** — "test cases that grade the skill before you save it" brings [[skill-creator]]'s acceptance-test framing to non-developers, same democratization move as [[tristen-obrien]]'s beginner-tier pizza-shop demo, but cross-surface.

## Why track him for 3Ps

- **Audience-tier signal** — when a Microsoft-365-tutorial channel covers Claude Skills under a QuickBooks sponsor, the primitive has crossed into the mainstream business-operator content diet. Useful adoption-tier marker.
- **The cross-surface skill demo is a reusable client-onboarding asset** — "your skill runs in Chat, Cowork, and Code" is exactly the message a 3Ps client (non-developer operator) needs to hear.
- **Distribution-floor benchmark** — the synced-shared-folder sharing method is the lowest-friction team-distribution pattern tracked; relevant for clients without Team/Enterprise plans.

## Open questions

- **Channel sub count / Kevin Stratvert vs David DeWinter** — is DeWinter a recurring co-host or guest presenter? The brand is Kevin Stratvert; this video is DeWinter-hosted.
- **Is Claude Skills a one-off or a new content pillar** for the channel? If the office-productivity-tutorial tier sustains Claude coverage, it's a meaningful mainstreaming signal.
- **Skill-format parity across surfaces** — does the *same file* run unchanged on Chat/Cowork/Code, or are there per-surface adaptations? (Transcript would resolve.)

## Related

- [[claude-skills]] — primary concept; this video resolves the cross-surface open question
- [[skill-creator]] — eval discipline ("test cases that grade the skill before you save it")
- [[codex]] — skills are vendor-portable; this video shows they're also surface-portable
- [[claude-for-small-business]] — shares the QuickBooks/SMB-operator audience
- [[tristen-obrien]] — sibling beginner/non-developer skills explainer (single-surface)
- [[claude-code]] — `.claude/skills` folder-on-disk surface
- [[execution-layer]], [[plugin-marketplace]] — higher-friction team-distribution patterns vs the synced-shared-folder method

## Appears in

- [[youtube-digest-apify-2026-05-28]] — #4, Claude Skills cross-surface tutorial
