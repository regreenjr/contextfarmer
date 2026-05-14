---
title: Retrieval Contract
category: concept
summary: [[nate-b-jones]]'s 2026-05-13 builder-side framework — what an agent needs to declare *before* picking a database — entities, relationship structure, freshness, access controls; named via [[pinecone]] Nexus' "NoQL" primitive (chapter 7:00); the missing developer-facing primitive above NoQL/PageIndex/GraphRAG/tabular-memory; *"builders who write down what their agent needs before picking a database will ship reliable systems — the ones who shop vendor-first will keep paying for rediscovery on every run"*; the architectural decision point above the [[knowledge-layer]] convergence
tags: [retrieval-contract, knowledge-layer, pinecone-nexus, noql, pageindex, graphrag, tabular-memory, agent-retrieval, builder-framework, nate-b-jones]
sources: 1
updated: 2026-05-14
---

# Retrieval Contract

## Definition

A **retrieval contract** is the explicit declaration of what an agent needs to retrieve, *before* the agent's builder selects a database / index / knowledge store. The contract specifies:

- **Entities** — what kinds of things the agent needs to find
- **Relationship structure** — how those entities link (graph? hierarchy? table rows?)
- **Freshness** — how stale is acceptable
- **Access controls** — who/what can read what

Named by [[nate-b-jones]] in *Pinecone Just Demoted Vector Search. Here's the Knowledge Layer.* (38.5K views, 2026-05-13, 20:08, [[youtube-digest-apify-2026-05-14]] #2). Specifically introduced via [[pinecone]] Nexus' **NoQL** primitive at chapter 7:00.

## The architectural claim

> "Builders who write down what their agent needs before picking a database will ship reliable systems — the ones who shop vendor-first will keep paying for rediscovery on every run." — [[nate-b-jones]] #2

The contract inversion:

| Old pattern | New pattern |
|---|---|
| Pick a DB → fit your agent's needs to its query model | Spec the contract → pick the DB that matches |
| Vector search first, then figure out what fits | Declare retrieval needs first, then pick from {vector, graph, page, tabular} |
| Pay rediscovery cost forever | Pay compile cost once |

## Why it matters: the rediscovery problem

[[nate-b-jones]] frames the existing failure mode (chapter 1:15, *The rediscovery problem eating agent compute*):

- Agents make many tool calls per task
- Each call re-derives the same connections that prior calls already established
- Classic RAG was built for *one-shot chatbot retrieval*, not *iterative agent retrieval*
- 85% of agent effort goes to retrieval, only 15% to reasoning ([[pinecone]] framing post)

The retrieval contract is the answer: **declare the structure once, retrieve cheaply many times.**

## The four-shape attack on the problem (chapters 7:00-14:30)

[[nate-b-jones]] maps four vendor camps to four problem shapes. The retrieval contract is what tells you which shape applies:

| Shape | Vendor / pattern | Best for | Where it breaks |
|---|---|---|---|
| **Compiled knowledge + NoQL retrieval contract** | [[pinecone]] Nexus | General agent retrieval over docs | Compile cost high; fast-changing data |
| **Don't-chunk-this** | PageIndex | Long-form docs where structure is non-local (legal contracts, long papers) | Chunking-based search ineffective |
| **Tabular memory** | SAP / Dremio / Prior Labs | Structured business data (orders, customers, transactions) | Doesn't help with prose |
| **Relational knowledge** | Microsoft GraphRAG | Cross-document reasoning, entity-graph traversal | Setup cost; ontology overhead |

**The decision point** is the contract — once you've declared what your agent needs, the shape (and thus the vendor) follows. Skipping the contract step locks you into whatever shape your default vendor (usually vector search) handles.

## What goes in a retrieval contract

[[nate-b-jones]] doesn't ship an explicit schema, but the framework implies the contract carries at least:

1. **Entity types** — what categories of thing the agent retrieves (documents? rows? entities? sections?)
2. **Cardinality** — how many of each per query (one-shot? top-k? exhaustive?)
3. **Relationship requirements** — does the agent need linked entities (graph traversal)?
4. **Freshness requirements** — real-time? hourly? compiled-once-then-cached?
5. **Structure requirements** — chunked OK or must read whole doc (PageIndex case)?
6. **Access controls** — what's the auth surface? (Pairs with [[agent-security]]'s "platform knows humans from agents")
7. **Failure modes** — what happens when the shape doesn't match (graceful degrade? error? human escalation?)

This is **an analog of an API contract** for retrieval. The same engineering discipline that produced OpenAPI specs is now being applied to agent retrieval.

## Why bigger context windows don't fix this (chapter 15:45)

Tempting alternative: just stuff everything in a million-token context window. [[nate-b-jones]]'s rebuttal:

- **Cost scales linearly with context** — every token is paid; agent loops compound
- **Recall degrades in the middle** (lost-in-the-middle) — long context is unreliable
- **No compilation** — the work isn't structured, just stuffed; agents pay rediscovery cost inside the context window

The retrieval contract still applies — agents need declared structure, not just access to more raw text.

## Three steps if you're building an agent today (chapter 17:00)

(Specifics gated to transcript — likely:

1. **Write the contract** before picking a DB
2. **Pick the matching shape** from the four-vendor camp
3. **Set up the compile pipeline** — one-time per source, cheap to query)

Transcript pull needed for the precise steps.

## How the wiki implements (partially) the retrieval-contract pattern

This vault is a hand-rolled implementation of compiled-knowledge retrieval. The implicit retrieval contract:

| Contract dimension | This vault's spec |
|---|---|
| Entity types | entities, concepts, sources, comparisons, synthesis |
| Cardinality | top-k via [[wikilinks]] + index.md catalog |
| Relationship | wikilinks (manually authored), implicit category hierarchy |
| Freshness | manual `updated:` frontmatter; not enforced |
| Structure | mostly chunked (paragraphs), some not-chunked (whole entity/concept pages) |
| Access | filesystem (no auth) |
| Failure mode | "claim has citation" rule + lint check |

The wiki **doesn't yet have a formal contract spec** — the contract is implicit in CLAUDE.md / AGENTS.md and the frontmatter schema. A `retrieval-contract.yaml` at vault root could make it explicit. Worth adding when the vault hits multi-tenant / cross-vault use cases.

## Strategic significance for the vault

### Confirms the "compile once" thesis at builder layer

[[nate-b-jones]]'s prior [[knowledge-layer]] coverage was vendor-side (Pinecone/Microsoft/Google shipping the layer). This video adds the **builder-side decision** — operators now have an explicit framework for *when to use which knowledge-layer product*. The decision sits at the contract layer, above the product layer.

For the vault: the wiki architecture sits in the **compiled knowledge + NoQL retrieval contract** quadrant ([[pinecone]] Nexus shape). The other three shapes (PageIndex, tabular, GraphRAG) suggest **adjacent capabilities the vault could add**:

- **PageIndex shape** — useful for long-form sources (Karpathy 3.5hr deep dive; full transcripts) that shouldn't be chunked into entity pages
- **Tabular shape** — useful for the competitor-ads-farm batches (each ad is a row; structured query is natural)
- **GraphRAG shape** — the wiki's wikilink structure is *almost* GraphRAG; an explicit graph layer (the planned KnowQL analog) would make this complete

### Names the missing primitive layer above [[knowledge-layer]]

| Layer | What it is | Status |
|---|---|---|
| **Retrieval contract** | What the agent needs (declarative) | NEW — [[nate-b-jones]] 2026-05-13 |
| Knowledge layer (compiled) | How it's structured ([[pinecone]] Nexus, Fabric IQ, Knowledge Catalog) | [[knowledge-layer]] |
| Vector DB / graph DB / table DB | Where it lives | [[pinecone]] (vector), Microsoft Fabric (lake), etc. |

The retrieval contract is **the developer-facing API** to the knowledge layer. Same shape as REST/GraphQL being the developer API above HTTP transport.

### Makes the 3Ps positioning sharper

3Ps consulting deliverables can now lead with **"let's write your retrieval contract"** as Phase 0 of a knowledge-layer engagement. This is:

- A small, billable artifact (could be a half-day workshop output)
- Vendor-neutral (doesn't lock the client to a specific knowledge-layer product)
- The forcing function that surfaces the right shape (graph? page? tabular? compiled docs?)

Pairs with [[execution-layer]] (output-side productization) for a complete client-engagement arc:

| Phase | Artifact | Concept |
|---|---|---|
| Phase 0 | Retrieval contract | [[retrieval-contract]] |
| Phase 1 | Context layer (second brain) | [[karpathy-llm-wiki]] / [[context-farming]] |
| Phase 2 | Execution layer | [[execution-layer]] |
| Phase 3 | PR-back loop | [[execution-layer]] |

## Open questions

- **Is there an emerging open-spec for retrieval contracts?** — KnowQL is Pinecone-specific; is there an OpenAPI-style multi-vendor spec brewing?
- **PageIndex** — new candidate entity stub. Who ships it? Standalone product or [[pinecone]] sub-feature?
- **GraphRAG** — Microsoft Research published; is it now in Fabric IQ, or still research-stage?
- **Tabular memory** — SAP / Dremio / Prior Labs each have different shapes; which converges?
- **Compile cost benchmarks** — no public numbers on [[pinecone]] Nexus compile times for representative source bases
- **Contract evolution** — how does a contract change as the agent's task scope grows? Versioning?
- **Cost model** — does Pinecone bill per-NoQL-query or per-compiled-page?

## Contrasts with

- **[[knowledge-layer]]** — the *implementation* layer (vendor-shipped); retrieval contract is the *spec* layer above it
- **[[karpathy-llm-wiki]]** — the *pattern* (write-time vs query-time); contract is *what you declare* to operate the pattern
- **[[plugins]]** taxonomy ([[nate-b-jones]] #11 in 2026-05-10) — six-layer agentic-scaffolding map; retrieval contract sits **above** the plugins layer at the meta-architecture decision tier
- **Classic RAG retrieval** — implicit contract ("top-k similar chunks"); retrieval contract makes the implicit explicit and adds the shape question

## Why it matters for 3Ps

### Diagnostic deliverable

A 3Ps engagement can ship a **retrieval contract audit** as a half-day workshop:

1. List the agent's actual retrieval needs per workflow
2. Categorize each retrieval into a shape (compiled / page / tabular / graph)
3. Map shapes to vendors / patterns
4. Identify mismatch (e.g., using vector search for tabular needs)
5. Output: a 2-page retrieval contract document + a recommended migration path

### Forcing function for [[knowledge-layer]] conversations

Most clients with vector DB stacks don't know they have a retrieval mismatch — they just know "RAG is brittle." The contract framing **forces the mismatch to surface** without requiring a vendor pitch.

### Reusable framework asset

[[nate-b-jones]] gives the names but not the spec. 3Ps content can ship the **first open retrieval-contract spec** (YAML or JSON schema), filling the same gap [[brad-bonanno]] filled for execution layer (free GitHub template).

## Related pages

- [[knowledge-layer]] — primary parent concept (this is the spec layer above it)
- [[pinecone]] — NoQL is their primitive; Nexus is the implementation
- [[karpathy-llm-wiki]] — the conceptual antecedent; retrieval contract makes the wiki's implicit contract explicit
- [[nate-b-jones]] — primary author; eighth named framework
- [[plugins]] — sibling architectural framework
- [[execution-layer]] — companion productization concept
- [[ai-consulting]] — engagement artifact (Phase 0)
- [[youtube-digest-apify-2026-05-14]] — primary citation

## Used in

- [[youtube-digest-apify-2026-05-14]] — primary citation ([[nate-b-jones]] #2)
- [[knowledge-layer]] — spec-layer companion
- [[nate-b-jones]] — primary author
