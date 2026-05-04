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
