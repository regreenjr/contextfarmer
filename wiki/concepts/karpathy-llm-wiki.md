---
title: Karpathy LLM Wiki
category: concept
summary: Pattern of having an LLM ingest sources once into structured, interlinked markdown — knowledge compiled at write time vs RAG's re-derive at query time
tags: [karpathy-llm-wiki, knowledge-management, second-brain, obsidian, claude-code, write-time-knowledge]
sources: 2
updated: 2026-05-03
---

# Karpathy LLM Wiki

## Definition
A pattern (originated by [[andrej-karpathy]] in an April 2026 [GitHub gist](https://gist.github.com/karpathy/442a37bf3a7be1f29bda3def33b2a3eb)) where an LLM ingests sources *once* into a structured, interlinked, plain-markdown knowledge base — entity pages, concept pages, source summaries, cross-references, contradictions — instead of re-deriving understanding from raw chunks every query (the RAG default).

**This vault is a direct implementation of the pattern.** The CLAUDE.md / AGENTS.md schema, the `raw/` → `wiki/` separation, the `/wiki-ingest`, `/wiki-query`, `/wiki-lint` commands all instantiate Karpathy's gist.

## Origin
- **April 2026**: [[andrej-karpathy]] publishes the gist
- **41,000 bookmarks in a week** ([[nate-b-jones]] in [[youtube-digest-apify-2026-05-03]] #24)
- **5+ derivative YouTube videos** within the following month, each implementing the pattern slightly differently

## Key claims (from [[youtube-digest-apify-2026-05-03]])

- **Knowledge compiled at write time beats query-time re-derivation** — the canonical fork ([[nate-herk]] #10, [[nate-b-jones]] #24)
- **Files as the universal interface** — markdown is the substrate; LLMs and humans both read/write it natively ([[tonbi-onchain-ai-garage]] #11)
- **Cross-references + contradiction flagging are first-class operations** — not bolted on after-the-fact (this vault's `> ⚠️ Contradiction:` callouts)
- **Obsidian as a graph-view frontend** — the user opens the vault while the LLM edits; graph view shows structural compounding ([[nate-herk]] #10, Teacher's Tech #20)
- **Linting matters** — orphans, stale claims, broken links accumulate without periodic cleanup ([[teachers-tech]] #20 explicitly covers linting in beginner setup)
- **Beats RAG for "what does the wiki say about X" questions** — but loses to RAG when you need exhaustive recall over millions of chunks

## Implementation patterns observed

| Source | Vault location | Key choices |
|---|---|---|
| [[nate-herk]] #10 | Personal second brain + YouTube transcripts | Two separate vaults, Obsidian frontend, ~5min setup demo |
| [[tonbi-onchain-ai-garage]] #11 | Trading-strategy wiki | Custom LLM backend, web search integration |
| Teacher's Tech #20 | Beginner generic | Obsidian Web Clipper for ingest, lint step explicit |
| **This vault** | 3Ps consulting + GTM playbook | Claude Code skills (`farmer`, `wiki-ingest`, `wiki-query`, `wiki-lint`), per-source farmer configs |
| [[brad-bonanno]] #23 | Company brain | Slack + Fireflies MCP feed via [[context-farming]] |
| [[tommy-chryst]] #1 (r3) | "PhD-level research" generic vault | Tier-3 small-channel walkthrough; positioned as ChatGPT deep-research alternative; signals pattern past tip-of-funnel |

## Contrasts with
- **[[openbrain]]** (OpenAI's memory product) — see [[karpathy-wiki-vs-openbrain]] for the full comparison; OpenBrain synthesizes at query time, LLM Wiki compiles at write time
- **Traditional RAG** — RAG embeds chunks and retrieves on query; LLM Wiki compiles into structured pages on ingest
- **Notion AI / Mem.ai** — proprietary, query-time, opaque storage

## Open questions / disagreements

- **Editorial errors get baked in** ([[nate-b-jones]] #24) — if the LLM mis-synthesizes during ingest, the error compounds across cross-references. RAG re-derives every time so a model upgrade fixes prior errors automatically; LLM Wiki needs explicit re-ingest.
- **Graph DB hybrid** ([[nate-b-jones]] #24) — is the future a graph DB *over* structured wiki pages? Mentioned but not yet built canonically.
- **Scale ceiling** — how many sources before the wiki becomes too dense for an LLM to navigate efficiently? No data yet.
- ⚠️ Contradiction: [[nate-herk]] #10 frames LLM Wiki as superior to RAG with no caveats; [[nate-b-jones]] #24 explicitly argues both have failure modes and a hybrid is likely correct. The wiki community is split on whether write-time fully replaces query-time or merely complements it.

## Why it matters for 3Ps

The user's entire knowledge architecture *is* this pattern. Implications:
1. **Validation**: 41K bookmarks + 5 implementer videos = the user is on a mainstream wave
2. **Differentiation risk**: as more people adopt the pattern, "I have a wiki" stops being a differentiator — the *quality of the wiki* (and the farmers feeding it) becomes the moat
3. **Productization opportunity**: a "3Ps Wiki Starter Kit" (this repo, generalized) could be a lead magnet or paid product
4. **Content angle**: the user can credibly publish wiki implementation content (vault structure, farmer configs, lint scripts) to creators currently watching [[nate-herk]] / [[teachers-tech]]

## Adoption-tier signal

Implementations now span all creator tiers:

| Tier | Subs/views range | Example | Date |
|---|---|---|---|
| Tier 1 (mainstream) | 100K+ subs | [[nate-herk]] (708K subs, 459K views) | April 2026 |
| Tier 2 (educator) | 200K-1M | Teacher's Tech (259K views) | April 2026 |
| Tier 3 (small) | sub-15K views | [[tommy-chryst]] (14.6K views) | April 2026 |
| Vertical | n/a | [[tonbi-onchain-ai-garage]] (trading) | April 2026 |
| Operator | n/a | [[brad-bonanno]] (company brain) | April 2026 |

Conclusion: the pattern is past the early-adopter trough; "I built an LLM Wiki" is no longer differentiating. Differentiation now lives in **what's in the wiki and how well the farmers feed it**, not in having one at all.

## Used in
- [[youtube-digest-apify-2026-05-03]] — primary citation
- [[youtube-digest-2026-05-03-r3]] — Tommy Chryst's tier-3 walkthrough
- [[karpathy-wiki-vs-openbrain]] — direct comparison page
- [[andrej-karpathy]] — author
- [[context-farming]] — the upstream feeder pattern
- [[tommy-chryst]] — small-channel implementer
- This vault's `CLAUDE.md` — the schema definition
