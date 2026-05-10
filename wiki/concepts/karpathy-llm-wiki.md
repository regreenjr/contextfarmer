---
title: Karpathy LLM Wiki
category: concept
summary: Pattern of having an LLM ingest sources once into structured, interlinked markdown — knowledge compiled at write time vs RAG's re-derive at query time; in 2026-05 commercially shipped by [[pinecone]] Nexus + Microsoft Fabric IQ + Google Knowledge Catalog within ~four weeks (the [[knowledge-layer]] convergence); a sibling Karpathy project (autoresearch) surfaces in mainstream curation
tags: [karpathy-llm-wiki, knowledge-management, second-brain, obsidian, claude-code, write-time-knowledge, autoresearch, knowledge-layer, pinecone, hermes-agent]
sources: 4
updated: 2026-05-10
---

# Karpathy LLM Wiki

## Definition
A pattern (originated by [[andrej-karpathy]] in an April 2026 [GitHub gist](https://gist.github.com/karpathy/442a37bf3a7be1f29bda3def33b2a3eb)) where an LLM ingests sources *once* into a structured, interlinked, plain-markdown knowledge base — entity pages, concept pages, source summaries, cross-references, contradictions — instead of re-deriving understanding from raw chunks every query (the RAG default).

**This vault is a direct implementation of the pattern.** The CLAUDE.md / AGENTS.md schema, the `raw/` → `wiki/` separation, the `/wiki-ingest`, `/wiki-query`, `/wiki-lint` commands all instantiate Karpathy's gist.

## Origin
- **April 2026**: [[andrej-karpathy]] publishes the gist
- **41,000 bookmarks in a week** ([[nate-b-jones]] in [[youtube-digest-apify-2026-05-03]] #24)
- **5+ derivative YouTube videos** within the following month, each implementing the pattern slightly differently
- **2026-05**: `karpathy/autoresearch` surfaces in [[dubibubii]]'s 33-tool curation ([[youtube-digest-apify-2026-05-05]] #5) — a separately-published Karpathy skill, **distinct from the LLM Wiki gist**. Open question whether autoresearch is the production form of this pattern or a sibling research-agent skill with different mechanics.
- **2026-05-10**: pattern is **commercially shipped** — [[pinecone]] Nexus + Microsoft Fabric IQ + Google Knowledge Catalog all ship the same architecture in ~4 weeks (per [[the-ai-automators]] #4 in [[youtube-digest-apify-2026-05-10]]). Pinecone's framing post: *"~85% of an agent's effort goes to retrieval rather than reasoning"* — admission that agentic RAG has fundamental architectural problems. Pinecone Nexus's three components (Context Compiler, Composable Retriever, KnowQL) explicitly map onto Karpathy wiki primitives. → [[knowledge-layer]] is the category page for the convergence.
- **2026-05-10**: tier-4 awareness saturation — [[ai-academy]]'s 687-view explainer in [[youtube-digest-apify-2026-05-10]] #6 marks the bottom of the creator funnel; the pattern is now mainstream-explainer-saturated.

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
| [[corey-ganim]] #3 | Hermes-on-Hostinger second brain | VPS + Telegram + OpenAI Codex backend; explicit fork from Claude Code + Obsidian — pattern runs on [[hermes-agent]] substrate too |
| [[ai-academy]] #6 | Tier-4 generic explainer | Bottom of the creator funnel; pattern at full mainstream-awareness saturation |
| **[[pinecone]] Nexus** | **Commercial enterprise software** | **Three-component architecture (Context Compiler / Composable Retriever / KnowQL) mapping onto wiki primitives** |
| **Microsoft Fabric IQ** | **Compiled Ontology layer** | **Inside Fabric data platform** |
| **Google Knowledge Catalog** | **Google Cloud platform layer** | **Cloud Next launch** |

## Contrasts with
- **[[openbrain]]** (OpenAI's memory product) — see [[karpathy-wiki-vs-openbrain]] for the full comparison; OpenBrain synthesizes at query time, LLM Wiki compiles at write time
- **Traditional RAG** — RAG embeds chunks and retrieves on query; LLM Wiki compiles into structured pages on ingest
- **Notion AI / Mem.ai** — proprietary, query-time, opaque storage

## Open questions / disagreements

- **Editorial errors get baked in** ([[nate-b-jones]] #24) — if the LLM mis-synthesizes during ingest, the error compounds across cross-references. RAG re-derives every time so a model upgrade fixes prior errors automatically; LLM Wiki needs explicit re-ingest.
- **Graph DB hybrid** ([[nate-b-jones]] #24) — is the future a graph DB *over* structured wiki pages? Mentioned but not yet built canonically.
- **Scale ceiling** — how many sources before the wiki becomes too dense for an LLM to navigate efficiently? No data yet.
- ⚠️ Contradiction: [[nate-herk]] #10 frames LLM Wiki as superior to RAG with no caveats; [[nate-b-jones]] #24 explicitly argues both have failure modes and a hybrid is likely correct. The wiki community is split on whether write-time fully replaces query-time or merely complements it.
- **`karpathy/autoresearch` vs the LLM Wiki gist** ([[dubibubii]] #5 in [[youtube-digest-apify-2026-05-05]]) — is autoresearch the canonical production-grade implementation of this pattern, a sibling research-agent skill, or a successor with a different memory model? **High-priority follow-up** before any next vault-architecture iteration; could moot or extend the entire current architecture.

## Why it matters for 3Ps

The user's entire knowledge architecture *is* this pattern. Implications:
1. **Validation**: 41K bookmarks + 5 implementer videos = the user is on a mainstream wave
2. **Differentiation risk**: as more people adopt the pattern, "I have a wiki" stops being a differentiator — the *quality of the wiki* (and the farmers feeding it) becomes the moat
3. **Productization opportunity**: a "3Ps Wiki Starter Kit" (this repo, generalized) could be a lead magnet or paid product
4. **Content angle**: the user can credibly publish wiki implementation content (vault structure, farmer configs, lint scripts) to creators currently watching [[nate-herk]] / [[teachers-tech]]

## Adoption-tier signal

Implementations now span all creator tiers + commercial software:

| Tier | Subs/views range | Example | Date |
|---|---|---|---|
| **Commercial vendor** | n/a | **[[pinecone]] Nexus, Microsoft Fabric IQ, Google Knowledge Catalog** | **2026-05** |
| Tier 1 (mainstream) | 100K+ subs | [[nate-herk]] (708K subs, 459K views) | April 2026 |
| Tier 2 (educator) | 200K-1M | Teacher's Tech (259K views) | April 2026 |
| Tier 3 (small) | sub-15K views | [[tommy-chryst]] (14.6K views), [[corey-ganim]] (3.3K) | April-May 2026 |
| **Tier 4 (tiny)** | sub-1K views | **[[ai-academy]] (687 views)** | 2026-04-29 |
| Vertical | n/a | [[tonbi-onchain-ai-garage]] (trading) | April 2026 |
| Operator | n/a | [[brad-bonanno]] (company brain) | April 2026 |
| **Substrate fork** | n/a | **[[corey-ganim]] on [[hermes-agent]]** | 2026-05-08 |

Conclusion: the pattern is **past the early-adopter trough AND has been validated by enterprise software**. "I built an LLM Wiki" is no longer differentiating; even tier-4 channels ship explainer videos for it. Differentiation now lives in **what's in the wiki and how well the farmers feed it**, not in having one at all.

The 2026-05 commercial-shipping shift changes the strategic frame: the user's vault is now an **early-mover artifact for an emerging enterprise category**, which is more sellable than "I built a hobbyist tool."

## Used in
- [[youtube-digest-apify-2026-05-03]] — primary citation
- [[youtube-digest-2026-05-03-r3]] — Tommy Chryst's tier-3 walkthrough
- [[youtube-digest-apify-2026-05-05]] — `karpathy/autoresearch` surfacing via [[dubibubii]] #5
- [[youtube-digest-apify-2026-05-10]] — commercial-shipping convergence ([[the-ai-automators]] #4) + tier-4 saturation ([[ai-academy]] #6) + [[hermes-agent]] fork ([[corey-ganim]] #3)
- [[karpathy-wiki-vs-openbrain]] — direct comparison page
- [[knowledge-layer]] — commercial-category page for the convergence
- [[pinecone]] — commercial-vendor-of-record
- [[andrej-karpathy]] — author
- [[context-farming]] — the upstream feeder pattern
- [[tommy-chryst]], [[corey-ganim]], [[ai-academy]], [[the-ai-automators]] — implementer/explainer creators
- [[claude-skills]] — `autoresearch` is published as a Claude Skill
- [[hermes-agent]] — alternative substrate for running the pattern (per [[corey-ganim]])
- This vault's `CLAUDE.md` — the schema definition
