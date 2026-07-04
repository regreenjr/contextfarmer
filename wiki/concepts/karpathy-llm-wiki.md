---
title: Karpathy LLM Wiki
category: concept
summary: Pattern of having an LLM ingest sources once into structured, interlinked markdown — knowledge compiled at write time vs RAG's re-derive at query time; in 2026-05 commercially shipped by [[pinecone]] Nexus + Microsoft Fabric IQ + Google Knowledge Catalog within ~four weeks (the [[knowledge-layer]] convergence); **2026-05-19 [[andrej-karpathy]] joins [[anthropic]]** — pattern becomes about-to-be-first-party-Anthropic-architecture, with [[nate-herk]] (105K views) framing **"the wiki is your data moat"**; **2026-05-20 [[eric-tech]] ships a `/wiki` skill** that automates the pattern; **in 2026-05-23 batch the autoresearch lineage continues** — [[simon-scrapes]]' [[self-improving-skills]] (109.7K views) is the **skill-tier instantiation of Karpathy `autoresearch`** (autonomous loop + binary criteria + overnight convergence), and [[nate-b-jones]]' [[project-room-workflow]] (22.3K views) is the **per-task instantiation** of the wiki architecture (source inventory + conflict log + missing context list = same shape as `raw/` → `wiki/` + contradiction-callouts at the per-deliverable scale)
tags: [karpathy-llm-wiki, knowledge-management, second-brain, obsidian, apple-notes, zettelkasten, google-antigravity, claude-code, write-time-knowledge, autoresearch, knowledge-layer, pinecone, hermes-agent, karpathy-anthropic, eric-tech, wiki-skill, farmer-subagents, cron, data-moat, anthropic-internal-future, context-marketplace, self-improving-skills, project-room-workflow, simon-scrapes, autoresearch-lineage, per-task-canvas, opus-4-7, learning-to-learn, nate-herk, claude-fable-5, multiple-wikis, routing-rules, flat-vs-structured]
sources: 11
updated: 2026-07-04
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
- **2026-05-19**: **[[andrej-karpathy]] joins [[anthropic]]** (per [[nate-herk]] 105K-view coverage in [[youtube-digest-apify-2026-05-22]]). Major implications: (1) the LLM Wiki gist and `karpathy/autoresearch` are no longer external-creator artifacts — they're **about-to-be-first-party Anthropic architecture**; (2) [[nate-herk]]'s "**LLM Wiki and Your Data Moat**" framing (chapter 6:25) makes the wiki **the explicit competitive moat** in a commoditized-model era; (3) the predictions (chapter 12:01) align with [[brad-bonanno]]'s [[execution-layer]] and [[alex-mcfarland]]'s [[plugin-marketplace]] — three creators converging on **context-marketplace + education-layer + unified-context-substrate** as the 2026-Q3 Anthropic roadmap.
- **2026-05-20**: **[[eric-tech]] ships a `/wiki` skill** that automates the entire workflow on a cron — pulling from YouTube/Gmail/Slack/any-MCP-source into an Obsidian vault. **Same primitive triple as this vault** (skill + farmer subagents + cron scheduling). Convergent evolution = strong correctness signal; the pattern is now creator-shipped-skill territory.
- **2026-05-22 (per [[youtube-digest-apify-2026-05-23]])**: **[[simon-scrapes]] ships [[self-improving-skills]]** (109.7K views) — explicit Karpathy-`autoresearch`-inspired autonomous overnight loop for Claude Code skills with binary criteria + convergence. Skill-tier instantiation of the autoresearch primitive; predates Karpathy-Anthropic hire but confirms the pattern survives the transition. Also: **[[nate-b-jones]] ships [[project-room-workflow]]** (22.3K views, 2026-05-22) — the per-task instantiation of the wiki architecture (`raw/` → `wiki/` + contradiction-callouts) named explicitly as **source inventory + conflict log + missing context list**. The vault implements project-room-workflow at the wiki scale; Nate's framework names the per-deliverable instantiation.

- **2026-06-08 (surfaced 2026-06-27, per [[youtube-digest-apify-2026-06-27]])**: **[[learning-to-learn]] ships the first Google-Antigravity-built and first Apple-Notes-targeted implementation** (*How to Create a Karpathy LLM Wiki for your Notes*, 332 views). Two new cells in the matrix: (1) the wiki is built with **Google Antigravity** (he names Claude Code as the alternative) — the first non-Claude-Code/Codex/Hermes agent substrate tracked for the pattern; and (2) it targets **Apple Notes** alongside Obsidian, plus a **zettelkasten** variant — the first consumer-notes-app destination. A clean *"LLM Wikis for AI vs note-taking"* callout distinguishes building for an AI reader vs a human note system; he also demos **skills in Antigravity** (cross-substrate skill confirmation, a datapoint for [[open-skills]]). Tier-4 (sub-1K-view) explainer — confirms the pattern is now substrate- and destination-agnostic.

- **2026-04-06 (surfaced 2026-06-24, per [[youtube-digest-apify-2026-06-24]])**: **[[the-prediction-engineer]] uses the LLM Wiki as an autonomous agent's *self-edited working memory*** (*I Rebuilt My Ai's Brain Using the Karpathy Method*, 2.1K views). His crypto-trading agent was *"demented"* — no state between days — so he rebuilt its memory with the wiki pattern **instead of vector-DB RAG** (*"too slow and imprecise for coding tasks"*), gave the **agent autonomy to edit its own wiki files**, and ran a **start-of-day `daily_plan.md` / end-of-day lessons-learned** loop. A **new cell in the implementation matrix: wiki-as-agent-state** (the agent both reads *and writes* its own wiki), distinct from the human-facing knowledge-management uses; the closest external artifact to what this vault does, in a markets vertical. Raises the "errors get baked in" risk in its sharpest form (the *agent* is the editor).

- **~2026-07 (surfaced 2026-07-02, per [[youtube-digest-apify-2026-07-02]])**: **Google ships the [[open-knowledge-format]] (OKF) — the pattern's first named open standard.** Per [[cole-medin]] (*Finally, an Open Standard for the Karpathy LLM Wiki is HERE*, 15.6K views): *"an open standard that formalizes Andrej Karpathy's LLM wiki pattern into plain markdown any AI can read with zero integration. No plugin, RAG pipeline, or vector DB."* Published under **GoogleCloudPlatform** on GitHub (a `SPEC.md` + `cloud.google.com/blog` launch post); Cole ships an **open-source OKF bundle** (`github.com/coleam00`) so any agent can search his content. This is the **convention → spec** step: the pattern goes from a viral gist to a cross-vendor standard, and it's **Google** shipping the *open/portable* version rather than another proprietary product (contrast their own Knowledge Catalog in [[knowledge-layer]]). Directly answers the [[knowledge-layer]] open question *"will an open spec emerge, or proprietary lock-in?"* → New concept: [[open-knowledge-format]]. Same-batch pairing: [[nate-b-jones]]' *own the memory, rent the intelligence* (#1) is the ownership thesis OKF makes **portable**.

- **2026-07-03 (per [[sources/youtube-digest-apify-2026-07-04]])**: **[[nate-herk]] pairs the wiki with [[claude-fable-5|Fable 5]] and teaches a ~5-minute [[claude-code|Claude Code]] + Obsidian build** (*Fable 5 + Karpathy's LLM Wiki is Basically Cheating*, 23.1K views). *"I ingested all my YouTube videos into an LLM wiki and turned them into a connected second brain that my AI OS can actually reason over… build the same thing in about five minutes using Claude Code and Obsidian… routing rules so it can find anything fast."* Four vault-relevant additions: (1) **Fable 5 as the reasoning layer over the connected wiki** (chapter 1:13, *What Fable Does With the Data*) — the *"basically cheating"* claim is that the frontier model + a compiled cross-linked corpus lets it reason over everything at once (the [[claude-fable-5|"doing got cheap"]] thesis applied to *your own* knowledge); the first creator to explicitly pair **frontier-model + LLM-wiki substrate** as a combined move; (2) **multiple topic-scoped wikis federated under one [[ai-operating-system|AIOS]]** (chapter 2:58) — matches the vault's multi-farmer design; (3) **flat-vs-structured** as an explicit schema-design fork (chapter 7:59) — when to keep pages flat vs split into `entities/`/`concepts/`/`sources/`; (4) **routing is why it works** (chapter 12:38) — the load-bearing mechanism is the **routing rules** that place/find sources, exactly the role this vault's ingest/query schema plays. Closest a mainstream 708K-sub creator has come to teaching *this vault's* exact stack in five minutes — validation of the design and a sharpening of the differentiation-risk clock below.

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
| **[[the-prediction-engineer]] (2026-06-24)** | **Autonomous crypto-trading agent state store** | **Agent self-edits its own wiki as working memory; daily_plan.md + end-of-day lessons-learned loop; explicit anti-vector-DB for coding/state** |
| **[[learning-to-learn]] (2026-06-08)** | **Personal notes (Obsidian + Apple Notes)** | **First Google-Antigravity build substrate; first Apple-Notes destination; zettelkasten variant; "AI vs note-taking" callout; skills-in-Antigravity demo** |
| **[[nate-herk]] (2026-07-03)** | **YouTube-video second brain federated under his AIOS** | **First to pair [[claude-fable-5|Fable 5]] as the reasoning layer; multiple topic-scoped wikis; explicit flat-vs-structured schema fork; routing rules named as the load-bearing mechanism; ~5-min Claude Code + Obsidian build** |
| [[ai-academy]] #6 | Tier-4 generic explainer | Bottom of the creator funnel; pattern at full mainstream-awareness saturation |
| **[[eric-tech]] #8 (2026-05-22)** | **Skool-distributed `/wiki` skill** | **Same primitive triple as this vault** (skill + farmer subagents + cron); convergent-evolution from independent creator |
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
2. **Differentiation risk**: as more people adopt the pattern, "I have a wiki" stops being a differentiator — the *quality of the wiki* (and the farmers feeding it) becomes the moat. The 2026-07 [[open-knowledge-format]] (OKF) standard sharpens this: once "OKF-compliant" is a checkbox, differentiation moves entirely to content quality + farmer coverage — with a possible early-mover edge in being **OKF-native** (a "3Ps OKF-compliant vault starter" is a crisper lead-magnet than a generic wiki)
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
- [[youtube-digest-apify-2026-05-22]] — **Karpathy joins Anthropic** ([[nate-herk]] #3, 105K views) + **[[eric-tech]] ships /wiki skill** ([[eric-tech]] #8)
- [[youtube-digest-apify-2026-06-27]] — **[[learning-to-learn]]** Antigravity build + Apple Notes destination + zettelkasten variant (tier-4 explainer)
- [[youtube-digest-apify-2026-07-02]] — **[[cole-medin]]**: Google ships the [[open-knowledge-format]], the pattern's first named open standard
- [[sources/youtube-digest-apify-2026-07-04]] — **[[nate-herk]]** pairs the wiki with [[claude-fable-5|Fable 5]] + teaches a ~5-min Claude Code/Obsidian build (multiple wikis, flat-vs-structured, routing rules)
- [[open-knowledge-format]] — Google's open standard formalizing this pattern (2026-07)
- [[karpathy-wiki-vs-openbrain]] — direct comparison page
- [[knowledge-layer]] — commercial-category page for the convergence
- [[pinecone]] — commercial-vendor-of-record
- [[andrej-karpathy]] — author
- [[context-farming]] — the upstream feeder pattern
- [[tommy-chryst]], [[corey-ganim]], [[ai-academy]], [[the-ai-automators]] — implementer/explainer creators
- [[the-prediction-engineer]] — wiki-as-agent-state variant (crypto-trading agent self-edits its own wiki); [[youtube-digest-apify-2026-06-24]]
- [[learning-to-learn]] — Antigravity-built + Apple-Notes-targeted implementer; [[youtube-digest-apify-2026-06-27]]
- [[claude-skills]] — `autoresearch` is published as a Claude Skill
- [[hermes-agent]] — alternative substrate for running the pattern (per [[corey-ganim]])
- This vault's `CLAUDE.md` — the schema definition
