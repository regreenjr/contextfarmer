---
title: Lindy
category: entity
summary: Consumer agent platform; surfaced in this vault as the canonical public case study for [[agent-security]]'s judge-architecture pattern — after their agents started sending unauthorized emails, they redesigned the system to put a separate LLM-as-judge between the actor and the outbound mail provider, with access to user intent + proposed action + blast radius
tags: [agent-platform, consumer-agent, lindy, agent-security, judge-architecture, case-study, unauthorized-emails]
sources: 1
updated: 2026-05-12
---

# Lindy

Consumer agent platform. Surfaced in this vault as a **case study**, not yet as a primary content source.

## Why it matters for this wiki

[[nate-b-jones]] cited Lindy as the **cleanest public example** of the [[agent-security]] architectural pattern in [[youtube-digest-apify-2026-05-12]] #1 (*LLM Agents: The Security Breach Pattern Nobody's Talking About*, chapter 3:30):

- Lindy's agents began **sending unauthorized emails** — outbound messages users hadn't approved
- They **redesigned the system** to place a separate LLM-as-judge between the actor model and the outbound mail provider
- The judge has access to: original user intent (compiled from session context), the proposed action (recipient + subject + body), the blast radius (external send, potentially irreversible reputational impact)
- Decision: proceed / refuse / escalate to human

This is **the public-postmortem reference** for the judge-architecture pattern — every 3Ps client conversation about agent-security can cite Lindy as proof that even consumer-grade agent platforms hit this failure mode and the working response is a judge layer.

## What's still unknown

- **Lindy's public postmortem** — did they publish a detailed writeup? What's the canonical source [[nate-b-jones]] is citing?
- **Their judge architecture's exact shape** — model used, latency budget, fallback policy, escalation criteria, intent-compilation method
- **Volume / scale** — how many email-send attempts per day? What fraction get judge-refused?
- **Product positioning** — is Lindy a competitor to [[claude-code]], [[hermes-agent]], [[codex]], or a different category (consumer-facing agent platform vs developer agent CLI)?
- **Tracked elsewhere?** — does Lindy appear in [[the-ai-automators]] or [[nate-b-jones]]' prior content? Worth a grep.

## Why track them for 3Ps

- **Reference case study for agent-security conversations** — concrete, named, post-incident; the kind of detail that earns enterprise attention
- **Architecture pattern artifact** — their judge architecture is a portable design pattern any agentic 3Ps deliverable can replicate
- **Competitive landscape signal** — if Lindy is a consumer-agent platform, they may overlap with the agent-platform space that 3Ps targets indirectly (clients building on agent platforms vs clients building agents)

## Related pages

- [[agent-security]] — primary concept; Lindy is the public case study for the architectural pattern
- [[nate-b-jones]] — citing source
- [[anticipation-gap]] — permission ladder pairs with the action-risk class taxonomy that the Lindy judge architecture implements
- [[youtube-digest-apify-2026-05-12]] — primary citation

## Appears in

- [[youtube-digest-apify-2026-05-12]] — first appearance (case study citation)
