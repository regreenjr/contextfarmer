# Log — Wiki

> Append-only timeline. Every LLM operation leaves an entry here.
>
> Format: `## [YYYY-MM-DD] <op> | <title>` followed by an optional detail line.
> Valid ops: `ingest`, `query`, `lint`, `create`, `update`, `delete`, `note`.
>
> Grep the last 10 entries: `grep "^## \[" log.md | tail -10`

## [2026-05-03] note | Vault initialized
Topic: **3Ps AI consulting + GTM playbook + AI creator landscape + competitive intel**. Layers created: `raw/`, `wiki/{entities,concepts,sources,comparisons,synthesis}`.
Schema loader: `CLAUDE.md` + `AGENTS.md` + `.cursorrules`.

## [2026-05-03] ingest | YouTube Digest — Claude Code AI Automation — 2026-05-03

Created: sources/youtube-digest-2026-05-03, entities/{nate-herk,greg-isenberg,jack-roberts,grace-leung}, concepts/{claude-code,claude-skills}

## [2026-05-03] note | farm: ai-creators-youtube

yt-search query='Claude Code AI automation skill', 7 videos found, saved digest to raw/youtube/digest-2026-05-03.md, ingest triggered

## [2026-05-03] ingest | YouTube Digest (Apify) — AI creators + Claude topics — 2026-05-03

28-video Apify digest. New: sources/youtube-digest-apify-2026-05-03; entities/{andrej-karpathy,nate-b-jones,anthropic,brad-bonanno,nick-saraev,mark-kashef,code-with-beto,tonbi-onchain-ai-garage}; concepts/{karpathy-llm-wiki,ai-consulting,context-farming,mcp,agent-substrate,agentic-commerce,claude-design,vibe-coding}; comparisons/karpathy-wiki-vs-openbrain. Updated: concepts/{claude-code,claude-skills}; entities/{nate-herk,grace-leung}.

## [2026-05-03] ingest | YouTube Digest (Apify, batch 3) — AI creators + Claude topics — 2026-05-03

5-video batch 3 digest. Created: sources/youtube-digest-2026-05-03-r3, entities/{tommy-chryst, jeanne-dewitt-grosser, lenny-rachitsky}, concepts/gtm-2026. Updated: entities/{grace-leung, nick-saraev, brad-bonanno}; concepts/{claude-code, ai-consulting, claude-design, claude-skills, karpathy-llm-wiki}; index regenerated to 30 pages.

## [2026-05-04] ingest | YouTube Digest (Apify) — AI creators + Claude topics — 2026-05-04

2-video batch (30 dedup-skipped). Created: sources/youtube-digest-apify-2026-05-04, entities/{brock-mesarich, y-combinator}. Updated: concepts/{claude-skills, claude-code, gtm-2026, ai-consulting}; index regenerated to 33 pages.

## [2026-05-05] ingest | YouTube Digest (Apify) — AI creators + Claude topics — 2026-05-05

8-video farm batch (24 dedup-skipped). Created: sources/youtube-digest-apify-2026-05-05; entities/{dan-martell, dubibubii, ben-ai}; concepts/voice-agents. Updated: entities/{nate-herk, nate-b-jones, andrej-karpathy, nick-saraev}; concepts/{claude-code, claude-skills, mcp, ai-consulting, karpathy-llm-wiki}; index regenerated to 38 pages. New patterns: voice-agents-as-Claude-Code-build (Nate Herk #6), creative-agency-on-Claude (Nate Herk #3 Higgsfield), T/C/L/D knowledge-work hollowing framework (Nate B Jones #1), karpathy/autoresearch surfacing (Dubibubii #5).

## [2026-05-06] ingest | YouTube Digest (Apify) — AI creators + Claude topics — 2026-05-06

3-video farm batch (29 dedup-skipped). Created: sources/youtube-digest-apify-2026-05-06; entities/simon-scrapes; concepts/{anticipation-gap, codex, skill-systems}. Updated: entities/{nate-b-jones, nate-herk}; concepts/{claude-skills, claude-code, ai-consulting}; index regenerated to 43 pages. New patterns: anticipation-gap + permission-ladder (Nate B Jones #1), Codex as parallel substrate with Skills/Plan-Mode/automations (Nate Herk #2 — first major OpenAI Codex educational entry), Skill Systems composition discipline (Simon Scrapes #3 — the missing rung between authoring and curation).

## [2026-05-06] ingest | FB Ads Digest — Competitor brands — 2026-05-06

183-ad first competitor-ads farm batch (4 dedup-skipped). Created: sources/ads-digest-2026-05-06; entities/{hims, ro, henry-meds, openai, hampton-founders}; concepts/{compounded-drug-disclaimer, dtc-telehealth-ad-template, competitor-ads-farm}. Updated: entities/anthropic. Index regenerated to 52 pages. Key findings: Hims 45 ads across 3 wedges (GLP-1/hair/Sex Rx) with canonical compounded-drug-disclaimer template; OpenAI (21) + Anthropic (5) ship dynamic-creative-only carousels, no static narrative; Hampton Founders runs 'M+ founder peer group' community pitch; ~65% of digest is brand-name-substring noise — flagged farm tuning action item.

## [2026-05-10] ingest | YouTube Digest (Apify) — AI creators + Claude topics — 2026-05-10

12-video farm batch (20 dedup-skipped). Created: sources/youtube-digest-apify-2026-05-10; entities/{corey-ganim, the-ai-automators, ai-academy, pinecone, mozilla}; concepts/{hermes-agent, knowledge-layer, printing-press, work-primitive, plugins, code-comprehensibility}. Updated: entities/{nate-herk, nate-b-jones, brad-bonanno, anthropic, andrej-karpathy}; concepts/{claude-code, claude-skills, mcp, karpathy-llm-wiki}. Index regenerated to 64 pages. Key signals: Hermes Agent crosses to mainstream-creator awareness (Nate Herk 1hr course + Corey Ganim LLM Wiki walkthrough); Karpathy LLM Wiki commercially shipped (Pinecone Nexus + Microsoft Fabric IQ + Google Knowledge Catalog converge in 4 weeks — knowledge-layer is now an enterprise category); Printing Press packages CLI-vs-MCP optimization; Nate B Jones ships 3 new frameworks in one batch (work-primitive, plugins-as-mech-suit, code-comprehensibility) plus an OpenClaw runtime reframe — now 6 named frameworks total in the vault; Anthropic-SpaceX deal doubles Claude Code session limits; Anthropic Mythos enters vault via Mozilla 271-vulnerabilities cycle.

## [2026-05-10] ingest | FB Ads Digest — Competitor brands — 2026-05-10

22-ad second competitor-ads farm batch (168 dedup-skipped from 190 fetched). Created: sources/ads-digest-2026-05-10. Updated: entities/{hims, ro, openai}; concepts/{compounded-drug-disclaimer, dtc-telehealth-ad-template, competitor-ads-farm}. Index regenerated to 65 pages. Key findings: Hims ships new Hard Mints SKU (chewable compounded ED for non-responders) — first 4-bullet variant of the DTC telehealth template; OpenAI catalog-ads-only pattern confirmed across two batches (24 total ads, 0 narrative); Ro placeholder-only pattern persists (3 total Ro ads, 0 with copy); brand-name substring filter still untuned — noise worsened from 65% to 82% as dedup removed real creative but kept fresh noise pages (KaRoL G, Uproot Clean, BaBylissPRO, Hampton by Hilton/VA/RV/Univ-Cancer, Hill Chiropractic).

## [2026-05-11] ingest | YouTube Digest (Apify) — AI creators + Claude topics — 2026-05-11

Thin 2-video batch (30 dedup-skipped). Created: [[sources/youtube-digest-apify-2026-05-11]], [[entities/chase-ai]], [[concepts/skill-creator]], [[concepts/agent-security]]. Updated: [[entities/nate-b-jones]] (7th framework — agent-security procurement-side), [[entities/anthropic]] (Skill Creator surface + agent-security responder), [[entities/openai]] (agent-security responder), [[entities/pinecone]] (agent-security responder, second sub-month convergence), [[concepts/claude-skills]] (Skill Creator first-hand walkthrough + two-types eval split capability-uplift vs encoded-preference), [[concepts/claude-code]] (Skill Creator workflow + agent-security responder set), [[concepts/work-primitive]] (humans-vs-agents authority sub-diagnostic). Index regenerated to 69 pages.

## [2026-05-11] ingest | FB Ads Digest — Competitor brands — 2026-05-11

6-ad third competitor-ads farm batch (190 dedup-skipped from 196 fetched — 97% dedup, steady state reached). Created: sources/ads-digest-2026-05-11. Updated: entities/{openai, hims, ro}; concepts/competitor-ads-farm. Index regenerated to 70 pages. Key findings: OpenAI catalog-ads-only TRIPLE-confirmed across 3 batches (27 total ads, 0 narrative) via new Apr 30 + May 8 campaign cluster — fresh-launch evidence rules out stale-campaign artifact; every other tracked brand (Hims/Ro/Anthropic/Henry Meds/Hampton Founders/DealMachine) 0 new ads (fully dedup-cached); new Adobe Acrobat noise has no substring match to any tracked brand — confirms Apify actor returns unsolicited adjacent brands, not just substrings, meaning page-ID allow-listing is the only structurally-safe filter; brand-name filter untuned across all 3 batches now.

## [2026-05-12] ingest | YouTube Digest (Apify) — AI creators + Claude topics — 2026-05-12

Small 4-video farm batch (28 dedup-skipped, ~87% hit). Created: [[sources/youtube-digest-apify-2026-05-12]], [[entities/mert-yerlikaya]], [[entities/zinho-automates]], [[entities/lindy]]. Updated: [[entities/nate-b-jones]] (judge-architecture extension of agent-security framework — 6th source), [[entities/nate-herk]] (Agent View + /goal walkthrough — 6th source), [[concepts/agent-security]] (architectural pattern section + LLM-as-judge at action boundary + four action-risk classes + Lindy case study + permission-ladder×action-class 2D matrix), [[concepts/claude-code]] (Agent View + /goal as new core primitives — multi-agent orchestration first-party), [[concepts/claude-skills]] (daily-driver curation sub-format added as 4th curation philosophy), [[concepts/ai-consulting]] (offer-language layer added as new dimension; operator-voices table grew from 6 to 7). Index regenerated to 74 pages. Key signals: agent-security extends from procurement diagnostic to complete framework (procurement + architecture + four-class taxonomy + Lindy case); Claude Code ships first-party multi-agent orchestration via Agent View; daily-driver curation joins best-of-N/essentials-bundle/mixed-stack as 4th curation pattern; offer-language is the under-covered AI-consulting dimension (Monk AI / Mert Yerlikaya).

## [2026-05-12] ingest | FB Ads Digest — Competitor brands — 2026-05-12

16-ad fourth competitor-ads farm batch (191 dedup-skipped from 207 fetched — 92% dedup, steady state continues). Created: sources/ads-digest-2026-05-12. Updated: entities/{openai, hims, ro}; concepts/{competitor-ads-farm, dtc-telehealth-ad-template}. Index regenerated to 75 pages. Key findings: OpenAI catalog-ads-only QUADRUPLE-confirmed across 4 batches (31 total ads, 0 narrative) — the May 8 launch cluster expanded from 2 → 6 ads across batches 3+4 evidencing the campaign is still rolling out; Hims re-launches the canonical Wegovy GLP-1 three-bullet template VERBATIM in a fresh 2026-05-07 ad (first Hims ad since 2026-05-10) — confirms the template is the standing creative and inside-structure A/B testing dominates over template variation; second non-substring-match noise event (Romance miniseries, 3 ads, "I rise from scavenger to king with alien tech") in two consecutive batches after Adobe Acrobat — rules out fluke hypothesis, the Apify actor returns unsolicited adjacent brands at non-zero rate with multi-ad volume per page; Lauren Brooks long-form pet-allergy direct-response (4 ads, "Brooks" contains "ro") filed as a copy-pattern contrast to the Hims three-bullet template; bare-"Ro" filter now demonstrably net-negative across 4 batches.
