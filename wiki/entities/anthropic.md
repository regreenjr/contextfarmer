---
title: Anthropic
category: entity
summary: AI lab behind Claude / Claude Code / Claude Skills / MCP; 2026 strategy is layering Claude into other vendors' apps + rumored Atlassian acquisition; 2026-05-06 FB ads batch shows Anthropic running 5 catalog-driven dynamic-creative carousels with zero static narrative copy — same pattern as OpenAI
tags: [organization, ai-lab, anthropic, claude, claude-code, enterprise, ads]
sources: 2
updated: 2026-05-06
---

# Anthropic

## What it is
AI lab. Maker of the Claude model family, [[claude-code]], [[claude-skills]], and the [[mcp]] standard. Founded 2021 by ex-OpenAI researchers (Dario & Daniela Amodei et al). Headquartered in San Francisco.

## Why it matters for this wiki
The user's entire stack runs on Anthropic primitives: Claude Code (this vault), Claude Skills, MCP servers, sub-agents, Routines. Anthropic's product/strategy moves directly determine the substrate the 3Ps offering builds on. 2026 is shaping up as the year Anthropic transitions from "best coding model" to "enterprise infrastructure provider."

## 2026 strategy signals (from [[youtube-digest-apify-2026-05-03]])

### Layering inside other vendors' apps
- **Microsoft is testing Claude against its own Copilot** ([[nate-b-jones]] #16) — implies Microsoft sees Claude as competitive enough on coding tasks to evaluate as a Copilot backend
- **Salesforce Headless 360** ([[nate-b-jones]] #2) — Claude showing up inside Salesforce flows
- **Perplexity Personal Computer** — another surface

The framing per [[nate-b-jones]]: Anthropic's strategy is *layering* (be the model inside other vendors' UX) more than *destination* (own the chat surface).

### Acquisition rumor
- **Anthropic might buy Atlassian for $40B** ([[nate-b-jones]] #8, 2026-05-02) — would put Anthropic on top of Jira/Confluence, the canonical enterprise issue-tracker substrate that's becoming [[agent-substrate]]
- Strategic logic: agents need durable state, ownership, permissions, history — exactly what issue trackers were built for

### Product surface area
- **[[claude-code]]** — CLI/agent tool; the dominant developer-facing surface
- **[[claude-skills]]** — reusable procedural-knowledge units; "Agent Skills Explained" (#4) is the official explainer (201K views)
- **[[mcp]]** — the open standard for tool/data integration
- **[[claude-design]]** — Anthropic's design tool (covered in [[nate-herk]] #18)
- Skill marketplace — Anthropic-distributed via `claude-plugins-official`

## 2026-05-06 FB ads pattern

From [[ads-digest-2026-05-06]] — 5 active Anthropic ads, all carousel format with `{{product.name}}` headlines and `{{product.brand}}` body text. **Zero static narrative copy.** Started Mar 16 - Apr 8, 2026.

Same pattern as [[openai]] in the same batch (21 ads, all dynamic-creative-only). Both AI labs in 2026-05-06 ship **only catalog/product-feed-driven dynamic creative** — opposite of DTC competitors like [[hims]] who pair catalog ads with static narrative wedges. Hypothesis: AI labs treat narrative work as PR/launches, and reserve paid social for catalog re-targeting against existing intent.

Open: which surface are the 5 ads pointing to? (claude.ai? Claude API? Claude Code? Claude for Enterprise?)

## Official channel activity

- 2025-11-26: *Claude Agent Skills Explained* (201K views) — canonical 3-minute explainer for Skills vs CLAUDE.md vs MCP vs sub-agents
- (Anthropic's official YouTube cadence appears low; high impact when they post)

## Related
- [[claude-code]], [[claude-skills]], [[mcp]], [[claude-design]] — products
- [[andrej-karpathy]] — not at Anthropic but his frameworks (LLM Wiki, agentic engineering) shape the ecosystem Anthropic ships into
- [[agent-substrate]] — the strategic frame that explains the Atlassian rumor
- [[agentic-commerce]] — Anthropic likely a player here too

## Appears in
- [[youtube-digest-apify-2026-05-03]] — official Skills explainer + 4 derivative analyst videos
- [[ads-digest-2026-05-06]] — 5 catalog-driven carousel ads (no static narrative)
- [[claude-code]], [[claude-skills]] — concept pages

## Open questions
- Is the Atlassian rumor priced into Anthropic strategy, or speculative? (Watch for confirmation/denial)
- What does the next official Anthropic YouTube post cover? (Cadence is low but each post is high-signal)
- Are Skills going to ship in non-Code surfaces (Claude.ai, mobile)? (Currently Code-only)
- Is there an official Skills marketplace coming, or will GitHub-distributed remain canonical?
