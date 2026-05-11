---
title: OpenAI
category: entity
summary: AI lab behind ChatGPT and Codex; catalog-ads-only FB strategy triple-confirmed across three batches (2026-05-06 + 2026-05-10 + 2026-05-11) — 27 total carousel ads, all `{{product.name}}` / `{{product.brand}}` dynamic-creative placeholders, zero static narrative copy; new Apr 30 + May 8 campaign cluster confirms the pattern survives fresh launches (not a stale Apr campaign artifact); in 2026-05-11 also named as a six-vendor agent-security responder alongside Anthropic / SAP / Pinecone / Salesforce / ServiceNow following the McKinsey Lilly exploit
tags: [organization, ai-lab, openai, codex, chatgpt, competitor, ads, agent-security]
sources: 5
updated: 2026-05-11
---

# OpenAI

## What it is

AI lab. Maker of ChatGPT, GPT-x model family, [[codex|Codex CLI]], DALL-E, Sora. Founded 2015. The reference competitor to [[anthropic]] in the foundation-model + dev-platform space. Headquartered in San Francisco.

## Why it matters for this wiki

Two angles:

1. **Substrate competitor to Anthropic** — [[codex]] is the parallel coding-agent CLI to Claude Code, and [[nate-herk]]'s 1hr Codex full-course (covered in [[youtube-digest-apify-2026-05-06]]) confirmed Codex ships the same Skills / Plan Mode / weekly automations primitives. OpenAI's product moves directly affect the substrate the [[ai-consulting]] practice builds on.
2. **FB ads pattern signal** — OpenAI's 2026-05-06 batch creative is structurally distinct from DTC competitors (Hims). Worth tracking because what AI labs choose to advertise reveals what surface they're monetizing.

## FB ads pattern — catalog-only, triple-confirmed across three batches

### 2026-05-06 batch (21 ads)

From [[ads-digest-2026-05-06]]: 21 carousel ads, all `{{product.name}}` / `{{product.brand}}` placeholders. Started dates Apr 2 - Apr 21, 2026 — single campaign launch wave.

### 2026-05-10 batch (3 ads)

From [[ads-digest-2026-05-10]]: 3 more carousel ads, all placeholders. All started 2026-04-07 — same campaign launch cluster as the prior batch (the prior batch's dedup just hadn't caught these yet).

### 2026-05-11 batch (3 ads)

From [[ads-digest-2026-05-11]]: 3 more carousel ads, all placeholders. Started dates **2026-04-30 and 2026-05-08** — a **new campaign cluster outside the original Apr 2-21 launch wave**. IDs: `1337964444896096`, `1481884507069298`, `1638491670630932`.

The new cluster is the decisive evidence — if OpenAI were going to shift to narrative creative, a fresh campaign launch is the natural moment. They didn't. The template held.

### Confirmed pattern (triple-batch)

**27 total OpenAI ads tracked across three batches, 0 with teardown-able copy. Two distinct campaign clusters (Apr 2-21 + Apr 30 / May 8), identical template both times.**

| Batch | Date | Ads | Campaign cluster |
|---|---|---|---|
| 1 | 2026-05-06 | 21 | Apr 2-21 (initial wave) |
| 2 | 2026-05-10 | 3 | Apr 7 (subset of cluster 1) |
| 3 | 2026-05-11 | 3 | Apr 30 + May 8 (new cluster) |

This is **catalog ads** — product-feed-driven dynamic creative against the OpenAI product surface (API products / ChatGPT plan SKUs / ChatGPT-for-X verticals). Triple-batch consistency rules out single-campaign coincidence *and* stale-campaign drift; the new cluster proves the strategy is standing, not legacy.

> ⚠️ Pattern triple-confirmed: OpenAI runs only catalog-driven dynamic creative on FB (27 carousels). Anthropic appears to do the same (5 ads in 2026-05-06, 0 new since). Both AI labs ship zero static brand/narrative creative on FB in 2026-05. Hypothesis: AI labs lean on PR/launches for narrative work and reserve paid social for catalog re-targeting against existing intent (search visits, ChatGPT signups, API console traffic).

## Agent-security responder (per [[nate-b-jones]] #1 in [[youtube-digest-apify-2026-05-11]])

In the McKinsey "Lilly" agent-exploit aftermath ($20 SQL injection through 22 of 200 unauthenticated endpoints), OpenAI shipped a response in the same week as five other vendors — [[anthropic]], SAP, [[pinecone]], Salesforce, ServiceNow.

Likely response shape: agent-auth surface improvements on the Codex / API side. The buyer-side question all six are pitching to: **"does your platform know humans from agents?"** OpenAI's API key model (per-key scope + audit) is the closest existing surface to per-agent identity, but lacks the human-vs-agent distinction Nate B Jones names as the actual procurement-relevant differentiator. → See [[agent-security]].

Six-vendor convergence in one week confirms sub-month cadence is now normal for major architectural shifts (same shape as the [[knowledge-layer]] convergence — [[pinecone]] / Microsoft / Google in 4 weeks per [[youtube-digest-apify-2026-05-10]]).

> Open: specific OpenAI product / API change announced. Transcript pull on [[youtube-digest-apify-2026-05-11]] #1 would clarify.

## Substrate role (Codex)

Per [[concepts/codex]] and [[youtube-digest-apify-2026-05-06]]:

- Codex CLI is OpenAI's parallel substrate to Claude Code with overlapping primitives — Plan Mode, Skills, weekly automations, browser-use
- Nate Herk's 1hr Codex full course (the first major OpenAI Codex educational entry in this vault) confirms cross-vendor Skills as a real pattern
- OpenAI's substrate strategy mirrors Anthropic's: be the model + tool layer the next generation of AI-native apps build against

## Related

- [[anthropic]] — direct competitor; both run dynamic-creative-only FB ads in 2026-05-06 batch
- [[concepts/codex]] — OpenAI's coding-agent CLI
- [[concepts/claude-code]] — parallel substrate from Anthropic
- [[concepts/claude-skills]] — Skills also exist on Codex (cross-vendor primitive)
- [[ads-digest-2026-05-06]] — first ad-creative observation
- [[ads-digest-2026-05-11]] — third-batch catalog confirmation + new May 8 campaign cluster
- [[youtube-digest-apify-2026-05-06]] — Codex educational entry

## Appears in

- [[sources/ads-digest-2026-05-06]] — 21 catalog ads, all dynamic-creative-only
- [[sources/ads-digest-2026-05-10]] — 3 more catalog ads, same pattern (24 total tracked)
- [[sources/ads-digest-2026-05-11]] — 3 more carousel ads from a new Apr 30 + May 8 campaign cluster — pattern triple-confirmed (27 total)
- [[sources/youtube-digest-apify-2026-05-06]] — Nate Herk Codex full-course
- [[sources/youtube-digest-apify-2026-05-11]] — agent-security responder (six-vendor convergence)

## Open questions

- What product surface are the 21 carousel ads pointing to? (API console? ChatGPT Plus? ChatGPT for Business? Sora? Verticals?)
- Does OpenAI have a separate FB Page running narrative brand creative that the bare-"OpenAI" search misses?
- When OpenAI runs static narrative creative (e.g. for ChatGPT Plus / API launches), what's the messaging template?
