---
title: Andrej Karpathy
category: entity
summary: Co-founder of OpenAI, ex-Tesla AI head, founder of Eureka Labs; author of the LLM Wiki gist (now commercially shipped by [[pinecone]] Nexus + Microsoft Fabric IQ + Google Knowledge Catalog within four weeks), "autoresearch" skill, and "vibe coding" / "Software 3.0" / "agentic engineering" framings; his 3.5hr "Deep Dive into LLMs" (6.27M views) is the canonical mainstream LLM explainer
tags: [person, ai-researcher, openai, eureka-labs, karpathy, llm-wiki, autoresearch, vibe-coding, knowledge-layer, pinecone]
sources: 3
updated: 2026-05-10
---

# Andrej Karpathy

## What it is
Person. Co-founder of OpenAI, former head of AI at Tesla, founder of [Eureka Labs](https://eurekalabs.ai). One of the most-followed AI educators and an originator of multiple framings ("vibe coding," "Software 3.0," "agentic engineering," "LLM Wiki") that the AI-creator ecosystem reuses heavily.

## Why it matters for this wiki
This vault *literally implements* his [LLM Wiki gist](https://gist.github.com/karpathy/442a37bf3a7be1f29bda3def33b2a3eb). His framings shape how the AI-creator ecosystem talks about agents, knowledge, and engineering practice. Tracking what he posts = tracking the next mainstream wave 6-12 weeks out.

## Key claims attributed to him in [[youtube-digest-apify-2026-05-03]]

- **LLM Wiki paradigm** ([[karpathy-llm-wiki]]) — knowledge compiled at write time into structured markdown beats RAG's re-derive-at-query-time. Cited in 5 videos this digest. Per [[nate-b-jones]] #24: 41,000 bookmarks in a week.
- **"Vibe coding" → "agentic engineering"** (Sequoia AI Ascent 2026, video #13) — vibe coding was the casual on-ramp; agentic engineering is the serious discipline now taking shape on top.
- **"LLMs are ghosts, not animals"** (Sequoia #13) — jagged, statistical, summoned entities requiring new taste and judgment to direct. Pushes back against animal/AGI framings.
- **Software 3.0** (Sequoia #13) — the era where natural language is the programming surface and agents are the installer/runtime.
- **"You can outsource your thinking but never your understanding"** (Sequoia #13) — caveat against full automation of cognitive work.

## Recent activity tracked

- 2026-04-29: *From Vibe Coding to Agentic Engineering* talk at Sequoia AI Ascent 2026 — 549K views, the largest single video in [[youtube-digest-apify-2026-05-03]]
- 2026-04: LLM Wiki gist drops, then goes viral (41K bookmarks per [[nate-b-jones]] #24)
- Triggered downstream content from [[nate-herk]] (#10), [[tonbi-onchain-ai-garage]] (#11), Teacher's Tech (#20), [[nate-b-jones]] (#24)
- **2025-02-05** *Deep Dive into LLMs like ChatGPT* (3:31:23, **6.27M views**) — surfaced in [[youtube-digest-apify-2026-05-05]] #8. Evergreen general-audience curriculum: pretraining → tokenization → NN internals → inference → GPT-2 / Llama 3.1 → post-training → RLHF, plus key framings: **"models need tokens to think"**, **"jagged intelligence"**, hallucinations / tool use / working memory, knowledge of self, tokenization-and-spelling failure modes
- **`karpathy/autoresearch`** — surfaced via [[dubibubii]] curation in [[youtube-digest-apify-2026-05-05]] #5; a published Karpathy skill distinct from the LLM Wiki gist. **Open question**: is this the production form of the [[karpathy-llm-wiki]] pattern? Worth investigating before next vault-architecture iteration.
- **2026-05: LLM Wiki gist commercially shipped** — surfaced in [[youtube-digest-apify-2026-05-10]] via [[the-ai-automators]] #4. [[pinecone]] Nexus + Microsoft Fabric IQ + Google Knowledge Catalog all ship the same architecture in roughly four weeks. The gist is now a **category** ([[knowledge-layer]]), not a curiosity. Pinecone explicitly frames their Nexus three components (Context Compiler, Composable Retriever, KnowQL) as mapping onto Karpathy's wiki primitives. Major validation of the pattern's correctness; Karpathy's gist is now a foundational document for an enterprise software category.
- **2026-05: AI Academy tier-4 explainer** — [[ai-academy]]'s 687-view *Inside the LLM Wiki* video in [[youtube-digest-apify-2026-05-10]] #6 marks the LLM Wiki pattern reaching the bottom of the creator funnel — full mainstream-awareness saturation.

## Related
- [[karpathy-llm-wiki]] — the pattern this vault uses
- [[vibe-coding]] — term he coined
- [[agentic-engineering]] — his successor framing
- [[claude-code]] — the substrate his wiki pattern runs on
- Eureka Labs — his current company (educational AI)

## Appears in
- [[youtube-digest-apify-2026-05-03]] — Sequoia talk + 4 derivative wiki videos
- [[youtube-digest-apify-2026-05-05]] — *Deep Dive into LLMs* (#8, evergreen) + `karpathy/autoresearch` surfacing (#5)
- [[youtube-digest-apify-2026-05-10]] — LLM Wiki commercially shipped via [[the-ai-automators]] #4 + [[ai-academy]] #6 tier-4 explainer
- (Future) [[youtube-digest-2026-05-03]] — covered by [[nate-herk]] in earlier yt-search digest

## Related (additions from this digest)
- [[knowledge-layer]] — the commercial category his gist seeded
- [[pinecone]] — the company-of-record shipping his pattern
- [[the-ai-automators]] — primary creator-channel covering the convergence

## Open questions
- What does Eureka Labs actually ship? Education-focused, but specifics?
- Is the LLM Wiki gist his stable position, or has `karpathy/autoresearch` superseded it as the production form? (High-priority follow-up)
- His follow-up posts on agentic engineering — is there a canonical write-up beyond the talk?
- Does `autoresearch` use the same write-time-compile architecture as the LLM Wiki gist, or a different memory model?
- Has Karpathy commented publicly on Pinecone Nexus / Microsoft Fabric IQ / Google Knowledge Catalog shipping his gist's architecture? (Worth searching X)
