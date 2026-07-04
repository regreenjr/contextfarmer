---
title: Reusable Agent Skeleton (One Nine-Step Agent for High-Trust Paperwork)
category: concept
summary: [[nate-b-jones]]' 36th named framework (*Every AI Agent Demo Stops at Email. I Pointed Mine at the Bills That Cost You Money.*, 11.6K views, 2026-07-03, 15:44) — the reusability thesis for agents: instead of rebuilding an agent per job, **build one nine-step skeleton, learn it on low-stakes email/calendar (the "101"), then point the same skeleton at the high-trust paperwork that actually costs money** — insurance appeals, tax prep, and beyond; the human-approval gate stays **locked** at the end of every build (*"as long as the last decision stays yours"*); *"the real question is what you build once and point at everything else"*
tags: [reusable-agent-skeleton, nate-b-jones, nine-step-skeleton, build-once, high-trust-paperwork, insurance-appeals, tax-prep, email-101, human-approval-gate, cited-appeal-packet, clean-data, model-choice, agent-security, agent-ownership, document-truth-layer, open-skills, model-routing, anticipation-gap, claude-code]
sources: 1
updated: 2026-07-04
---

# Reusable Agent Skeleton (One Nine-Step Agent for High-Trust Paperwork)

## Definition
[[nate-b-jones]]' framework (his **36th named**) that most agents are wastefully **rebuilt from scratch for every job**, when the better move is to build **one reusable skeleton** — a nine-step pattern — that you first learn on cheap, low-stakes work (email/calendar) and then **point at the messy, high-trust paperwork that actually costs money** (insurance appeals, tax prep). *"The real question is what you build once and point at everything else."* Surfaced via *Every AI Agent Demo Stops at Email. I Pointed Mine at the Bills That Cost You Money.* (11.6K views, 2026-07-03, 15:44) in [[sources/youtube-digest-apify-2026-07-04]].

## Origin
- **2026-07-03**, [[nate-b-jones]] (*AI News & Strategy Daily*). Description: *"AI agents usually get rebuilt from scratch for every new job. Here's how to build one reusable AI agent for messy, high-trust paperwork — insurance appeals, tax prep, and beyond… Learn the pattern on low-stakes email, and the paperwork that actually costs you money gets cheaper to face, as long as the last decision stays yours."*
- Chapter map: *Cold open: email is the 101* (0:00) → *The paperwork frame* (0:59) → **Same skeleton: nine steps** (2:25) → *Run plan* (3:08) → **Build 1: email/calendar** (3:38) → *The bridge from 101 to 201* (5:55) → **Build 2: insurance appeal packet** (6:55) → **Build 3: tax prep packet** (10:49) → *Payoff: three builds, same gate* (12:27) → *Clean data and model choice* (13:09) → *Rules* (13:46).

## Key claims
- **Email/calendar is the 101 where mistakes stay cheap** (cold open) — you learn the pattern on low-stakes work before pointing it at paperwork that costs money. The wedge is deliberately boring so the skeleton is proven before the stakes rise. *(from [[sources/youtube-digest-apify-2026-07-04]])*
- **One nine-step skeleton carries unchanged across three builds** (chapter 2:25) — email/calendar → **denied insurance claim** → **tax-prep packet**, same nine steps. The reusability thesis: *build once, point at everything*, the opposite of rebuild-per-job. *(from [[sources/youtube-digest-apify-2026-07-04]])*
- **A cited appeal packet must do specific things — and never promise** (Build 2) — the high-stakes artifact is grounded in citations/evidence and is explicitly forbidden from over-claiming. The [[document-truth-layer]] discipline applied to a regulated document.
- **The human-approval gate stays locked at the end of every build** (chapter 12:27, *three builds, same gate*) — *"the human approval gate stays locked, from email to taxes"*; the payoff is *"as long as the last decision stays yours."* The [[agent-security]] / [[agent-ownership]] permission boundary made non-negotiable.
- **Clean data + model choice** (chapter 13:09) — a data-quality precondition plus a callback to his [[model-routing]] picker; the two operational levers that make the skeleton reliable enough for high-trust work.

## Contrasts with
- **[[open-skills]]** — Jones's *"skills don't travel / own portable procedures"* framework; the reusable skeleton is that portable procedure **made concrete** for one agent across three jobs.
- **Per-job custom agents** — the industry default the framework argues against (*"rebuilt from scratch for every new job"*); the skeleton trades bespoke fit for reuse + a proven approval gate.
- **[[reusable-agent-skeleton]] vs [[loop-of-loops]]** — loops are the *scheduling/recurrence* frame; the skeleton is the *portable build pattern* inside a single agent. Complementary, not competing.

## Open questions / disagreements
- **What are the nine steps?** Gated to the video (chapter 2:25); the load-bearing content isn't in the vault yet. High-priority transcript follow-up.
- **How much really transfers unchanged?** The claim that the *same* skeleton carries from email to a denied insurance claim to taxes is strong; the per-domain glue (data sources, citation rules, gate copy) is where reusability usually leaks — unverified here.
- **Where exactly does the gate sit?** "Locked at the end of every build" implies a single terminal approval; whether high-trust paperwork needs *intermediate* gates (per the [[agent-security]] action-risk classes) is unresolved.

## Used in
- [[sources/youtube-digest-apify-2026-07-04]] — vault entry point (Nate B Jones #3)
- [[nate-b-jones]] — author (36th named framework)
- [[agent-security]] — the locked human-approval gate
- [[agent-ownership]] — the last decision stays yours / who owns the agent
- [[document-truth-layer]] — the cited-packet, never-promise discipline
- [[open-skills]] — portable procedure the skeleton instantiates
- [[model-routing]] — the "model choice" lever
- [[anticipation-gap]] — "start with one repeated part of your life" wedge, here email/calendar
</content>
