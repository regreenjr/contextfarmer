---
title: Voice Agents
category: concept
summary: Phone/voice-surfaced AI agents (lead capture, scheduling, support); 2026 inflection — building one is now a "describe in plain English to Claude Code" task with ElevenLabs as the runtime, replacing dashboard-clicking workflows
tags: [voice-agents, elevenlabs, claude-code, agentic, sales, scheduling, calcom]
sources: 1
updated: 2026-05-05
---

# Voice Agents

## Definition

AI agents that operate over a voice/phone surface — handling inbound calls, capturing leads, qualifying prospects, booking calls, or running outbound. Distinct from text chatbots in that the runtime constraints (latency, interruption handling, turn-taking, voice synthesis) require a specialized inference layer.

## 2026 inflection

Until late 2025, building a voice agent meant **clicking through ElevenLabs (or competitor) dashboards and wiring up API endpoints by hand** ([[nate-herk]] #6 framing in [[youtube-digest-apify-2026-05-05]]). As of mid-2026, the published pattern is:

> **Describe the agent in plain English to [[claude-code]] in Plan Mode. Claude writes the integration. ElevenLabs Agents API is the voice runtime. cal.com is the booking surface. Debug bugs through Claude rather than docs.**

This puts voice agents in the same "build by description" category as the rest of the [[claude-code]] surface — voice is no longer the holdout vertical that requires specialist tooling.

## Reference build ([[nate-herk]] #6 in [[youtube-digest-apify-2026-05-05]])

- **Use case**: voice agent embedded on a website, captures leads + books discovery calls
- **Stack**: Claude Code (Plan Mode build) + ElevenLabs Agents (runtime) + cal.com (booking)
- **Build narrative** (per chapters):
  - 0:00 Intro & demo
  - 3:00 How voice agents work
  - 5:42 Three ways to deploy (likely embed widget, phone number, API)
  - 6:43 Setting up Claude Code
  - 8:14 Plan Mode build
  - 14:03 Adding API keys
  - 17:11 First test & iteration
  - 22:50 Debugging the time zone bug
  - 26:55 Final booking demo
  - 29:14 Security & cost
  - 31:34 Final thoughts

The time-zone bug debugged via Claude (not docs) is the headline framing. Security & cost get a dedicated chapter, signaling commercial-deploy readiness.

## Stack components

- **ElevenLabs Agents** — current default voice runtime in this build pattern. Sponsorship in #6 — messaging is partly promotional but the build is real.
- **Claude Code** — orchestrator + integration writer
- **cal.com** — open-source scheduling surface; integrates cleanly via API
- **Three deployment modes** mentioned but not enumerated; presumed: embedded widget, dedicated phone number, programmatic API

## Why it matters for 3Ps

- **Net-new service line**: 3Ps client engagements can now include voice/phone surfaces without a specialist voice-AI vendor relationship — direct competitive lift over agencies still routing through dashboard ElevenLabs work.
- **Sales-funnel application**: discovery-call booking and lead qualification are the canonical use cases; both map directly to GTM service offerings.
- **Voice as a "multi-surface" play**: aligns with [[nate-b-jones]]'s framing that the right architecture is *many surfaces, one stack underneath* — voice is the next surface to plug into the same Claude-Code-substrate stack already covering text/email/Slack.

## Adjacent patterns

- **Creative agency on Claude** ([[nate-herk]] #3 — Higgsfield) — same "describe in English, Claude builds it" pattern but for image/video/ads
- **Marketing team on Claude** ([[grace-leung]]) — text-surface multi-agent build; voice is the missing surface in her stack until something like #6 plugs in
- **Skill-stack architectures** ([[claude-skills]]) — voice-agent skills (greeting, qualification, objection handling, booking) are publishable as a reusable skill stack

## Open questions

- Latency / quality of ElevenLabs Agents in production at scale?
- Cost-per-minute economics — is the 3Ps margin viable for a voice-agent line?
- Compliance / call-recording requirements by jurisdiction?
- Alternatives to ElevenLabs (Vapi, Retell, OpenAI Realtime) — what's the comparison?
- Do voice agents trigger the [[brad-bonanno]] MCP-vs-CLI cost optimization the same way other integrations do?
- Is there a "voice agent" skill bundle on `claude-plugins-official` or community marketplaces yet?
- Inbound vs outbound — outbound voice raises significantly more compliance concerns (TCPA in US); the #6 build is inbound-only

## Used in

- [[youtube-digest-apify-2026-05-05]] — [[nate-herk]] #6 (canonical reference build)
- [[claude-code]] — substrate
- [[nate-herk]] — currently the only creator with a published end-to-end build

## Related

- [[claude-code]] — substrate
- [[claude-skills]] — packaging unit for voice-agent behavior
- [[mcp]] — connector layer (cal.com integration likely via MCP)
- [[ai-consulting]] — service-line application
- [[gtm-2026]] — sales-funnel application
