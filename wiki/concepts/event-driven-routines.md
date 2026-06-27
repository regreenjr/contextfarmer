---
title: Event-Driven Routines (Webhook → Cloud Routine Automation)
category: concept
summary: [[brad-bonanno]]'s build pattern for taking the **operator out of the loop** — turning a manually-invoked Claude skill into an **event-triggered automation** that fires the instant an external event happens, not when the operator remembers to type a slash command. Surfaced via *I Automated Pre-Call Research with Claude Code (FULL BUILD)* (249 views, 2026-06-26, 49:08) — an unedited live build of a pre-call sales-research agent ("Sally") that fires on a **cal.com booking webhook**, enriched through **make.com middleware**, which triggers a **Claude cloud routine** that scrapes the prospect (Apify for LinkedIn + Google search, Firecrawl for website/web search) and writes a private research doc via the **Google Drive MCP**, then attaches it to the calendar invite via the **Google Calendar MCP** — all before the operator opens their laptop. The video's load-bearing architecture decision: **a local routine isn't event-based enough; reach for a Claude cloud routine (vs a managed agent) when the trigger is an external event.** The concrete, build-it-today instantiation of closing [[nate-b-jones]]' [[anticipation-gap]] — the agent knows *when* to act because an event tells it — and the cadence/connections layer of the [[ai-operating-system]] made event-driven
tags: [event-driven-routines, cloud-routine, local-routine, managed-agent, webhook, cal-com, make-com, middleware, sally, pre-call-research, sales-research, apify, firecrawl, google-drive-mcp, google-calendar-mcp, least-access-permissions, git-tracked-aios, take-yourself-out-of-the-loop, anticipation-gap, brad-bonanno, claude-code, mcp]
sources: 1
updated: 2026-06-27
---

# Event-Driven Routines (Webhook → Cloud Routine Automation)

## Definition

The pattern of converting a **manually-invoked skill** into an **event-triggered automation** — the agent fires *the instant an external event occurs* rather than when the operator remembers to invoke it. Named in practice by [[brad-bonanno]] in *I Automated Pre-Call Research with Claude Code (FULL BUILD)* (249 views, 2026-06-26, 49:08), an unedited live build.

Source: [[youtube-digest-apify-2026-06-27]] #2. Skill download: `brad-b.kit.com/0b31eb2b33`.

## The problem it solves

Brad had been running a sales-research skill **by hand** every time a call booked — *"I have to remember to type slash research every single time, and on a busy morning I forget."* The build **takes the operator completely out of the loop**: the research fires the instant a booking is made and the notes land on the calendar invite before he's opened his laptop. This is the concrete operator-side fix for [[nate-b-jones]]' [[anticipation-gap]] — the agent now knows *when* to act because an **event** tells it, not because the human decided to invoke it.

## The agent — "Sally"

Brad maps out exactly what the agent (he calls her **Sally**) needs to find and which tools get it there. Sally pulls the prospect's **LinkedIn, work history, company size, recent news, open roles, and buying signals** so he walks into every call prepared. Tools:

| Job | Tool |
|---|---|
| LinkedIn scraping + Google search | **Apify** |
| Website + web search | **Firecrawl** |
| Write a private research doc | **Google Drive MCP** ([[mcp]]) |
| Attach the doc to the invite | **Google Calendar MCP** ([[mcp]]) |

## The architecture decision — local vs cloud routine vs managed agent

The video's most transferable lesson (chapter ~midpoint): **why a local routine isn't event-based enough, and when to reach for a Claude cloud routine versus a managed agent.**

- **Local routine** — runs on a schedule on your machine; *not* event-based, and dead when the laptop is closed. Wrong tool for "fire the moment a booking happens."
- **Claude cloud routine** — runs in Anthropic's cloud, can be triggered by an external event, survives a closed laptop. The right reach for **event-driven** work.
- **Managed agent** — the heavier option; the video positions the cloud routine as the right middle tier for this job.

The trigger chain:

```
cal.com booking  →  webhook  →  make.com (middleware: enriches the booking)  →  Claude cloud routine (Sally runs)
```

**make.com** sits in the middle as the middleware that **enriches the booking** before firing the routine — the glue between the SaaS event and the agent.

## The build discipline

- **Configured straight from the Git-tracked AIOS repo** — Brad lets Claude configure the cloud routine for him from his version-controlled [[ai-operating-system]] repo (infrastructure-as-context).
- **Least-access permissions** — he sets the routine's access scope tight (the operator-side echo of [[agent-security]]'s action-risk discipline and the [[ai-operating-system]] "bike method" graduated-autonomy idea).
- **Unedited live build, "bugs and all"** — a real-architecture walkthrough rather than a polished demo.

## Where it sits

| Concept | Relationship |
|---|---|
| [[anticipation-gap]] | Event-driven routines are the **concrete fix** — the agent acts unprompted because an event triggers it, closing the "agent doesn't know *when* to act" gap |
| [[ai-operating-system]] | This is the **cadence + connections** layer of Brad's AIOS made *event-driven* rather than scheduled — the execution-layer payoff of his Phases 1-4 |
| [[claude-code]] | Cloud routines are a [[claude-code]] primitive; this extends the vault's routines coverage from *scheduled* (cron / `/loop`) to *event-triggered* (webhook) |
| [[mcp]] | Google Drive + Google Calendar MCPs are the write surface (doc + invite attachment) |
| [[agent-security]] | Least-access permissions on the routine = the operator-grade version of action-boundary discipline |

## Why it matters for 3Ps / this vault

1. **Event triggers are a missing primitive in this vault.** The vault's farmers run on **cron** ([[context-farming]]); Brad's pattern adds the **event-driven** trigger (webhook → middleware → cloud routine). A booking-triggered or email-triggered farmer would be a direct port.
2. **Pre-call research is a canonical sellable skill** — the same shape as [[claude-for-small-business]]' "call list" and the persona/lead-research skills, but **automated end-to-end** rather than invoked.
3. **The cloud-routine-vs-managed-agent decision is a consulting artifact** — a plain-language "which trigger tier for which job" guide for clients building event-driven automations.

## Open questions

- **Exact make.com scenario** — what enrichment happens in middleware vs in the routine? (Gated to the build.)
- **How does the cloud routine authenticate the MCPs** in Anthropic's cloud (vs a local routine with local creds)?
- **Cost/latency** of a cloud routine per booking vs a managed agent.
- **Is the cal.com → make.com → cloud-routine chain replaceable** by a direct webhook into a cloud routine once Claude routines accept native event triggers?

## Related
- [[brad-bonanno]] — author (pre-call research / "Sally" build)
- [[anticipation-gap]] — the gap this closes (agent knows *when* to act)
- [[ai-operating-system]] — the cadence/connections layer this makes event-driven
- [[claude-code]] — cloud routines as a primitive
- [[mcp]] — Google Drive + Calendar MCPs as the write surface
- [[agent-security]] — least-access permissions discipline
- [[context-farming]] — the cron-scheduled cousin; event triggers are the missing complement
- [[open-engine]] — [[nate-b-jones]]' same-batch agent-coordination framework (queue-side vs trigger-side)
- [[youtube-digest-apify-2026-06-27]] — citation
