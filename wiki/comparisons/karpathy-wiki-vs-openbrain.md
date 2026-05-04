---
title: Karpathy LLM Wiki vs OpenBrain — Write-Time vs Query-Time Memory
category: comparison
summary: The deepest design fork in personal-AI memory architecture; LLM Wiki compiles understanding at write time, OpenBrain synthesizes at query time. Both have failure modes.
tags: [karpathy-llm-wiki, openbrain, memory-architecture, second-brain, comparison, write-time, query-time]
sources: 1
updated: 2026-05-03
---

# Karpathy LLM Wiki vs OpenBrain — Write-Time vs Query-Time Memory

> Source: [[nate-b-jones]] *Karpathy's Wiki vs. Open Brain. One Fails When You Need It Most.* ([[youtube-digest-apify-2026-05-03]] #24, 98K views, 2026-04-22)

## The fork

The two systems solve **the same problem** (AI amnesia / no compounding knowledge) from **opposite directions**:

| | [[karpathy-llm-wiki]] | OpenBrain |
|---|---|---|
| **When work happens** | At write time (ingest) | At query time |
| **Storage shape** | Structured markdown pages, cross-linked | Raw stored memory, indexed for retrieval |
| **What's stored** | Compiled understanding (entities, concepts, syntheses) | Source material + vectors |
| **What gets re-derived** | Nothing on query — it's all pre-computed | Everything on query |
| **Token cost per query** | Low (read pre-compiled pages) | High (re-synthesize from raw chunks) |
| **Token cost per ingest** | High (LLM does heavy synthesis once) | Low (just embed + store) |
| **Cognitive metaphor** | Study guide | Filing cabinet with a librarian |

## Where each fails

### Karpathy LLM Wiki failure mode
- **Editorial errors get baked in** — if the LLM mis-synthesizes during ingest, the error compounds across cross-references
- **Model upgrades don't auto-fix prior pages** — wiki re-ingest is required to benefit from a smarter model
- **Lossy compression** — anything not captured during ingest is gone; query-time can't recover what wasn't compiled
- **High-leverage but high-blast-radius** — one bad ingest poisons many pages

### OpenBrain failure mode
- **Token-burn per query** — every question pays for re-synthesis from raw
- **No compounding insight** — connections you've already made get re-derived, not stored
- **Failure at scale** — too many sources → too much context → query-time synthesis degrades
- **Library-of-everything problem** — high recall, low precision; you get all the relevant chunks but no curated answer
- **"Fails when you need it most"** ([[nate-b-jones]]'s headline) — heaviest queries are when you most need pre-compiled understanding, and that's exactly where query-time synthesis breaks

## The hybrid

[[nate-b-jones]] points to a graph database **over** structured wiki pages as the likely synthesis. Wiki provides write-time-compiled cognition; graph DB provides query-time relational lookup; both layers stay healthy.

This vault is currently pure write-time. A graph layer is on the open-questions list for [[karpathy-llm-wiki]] and [[context-farming]].

## Stakes for builders ([[nate-b-jones]]'s framing)

> Builders who pick a memory architecture without understanding this fork will either lose detail when they need precision (wiki-only) or burn tokens re-deriving connections they already made (OpenBrain-only).

## Where each makes sense

| Use case | Best fit | Why |
|---|---|---|
| Personal knowledge / second brain | Wiki | High-leverage on a small, curated source set; ingest cadence is manageable; editorial taste matters |
| Enterprise corpus search | OpenBrain (or RAG variant) | Volume too high to compile everything; recall over many docs is the win |
| Domain expert system (legal, medical) | Hybrid | Wiki for canonical understanding; raw retrieval for primary sources |
| Real-time data (logs, events) | Neither pure — needs streaming layer | Both assume slow-changing source material |
| Customer support knowledge | Wiki for curated answers; raw for escalation | Tiered |

## What's settled vs open

**Settled:**
- These are different design choices, not "one is better"
- Both have failure modes
- The user's choice depends on use-case characteristics (volume, change rate, editorial value, query patterns)

**Open:**
- ⚠️ **Editorial error rate in wiki ingest** — no public data on how often LLM-driven synthesis bakes in errors at scale
- **Hybrid architecture** — described conceptually ([[nate-b-jones]]), no canonical implementation yet
- **Re-ingest cost** — when a smarter model arrives, what's the operational cost of re-ingesting a 1,000-page wiki? Unmeasured.
- **Multi-LLM wiki** — does the same wiki ingested by Claude vs GPT vs Gemini produce different (better/worse?) cross-references?

## Why this matters for 3Ps

- **Architectural justification** for any client-facing knowledge-system deliverable
- **Educational content** — this comparison is itself a credible 3Ps content asset; very few creators frame the trade-off cleanly
- **The user's vault is wiki-architecture** — adopting the comparison lets the user articulate trade-offs honestly when pitching it
- **Productization angle** — a "hybrid wiki + lightweight RAG over raw/" template could be a differentiated offering

## Sources & related

- [[youtube-digest-apify-2026-05-03]] — primary source
- [[nate-b-jones]] — author of the comparison
- [[karpathy-llm-wiki]] — primary concept
- [[andrej-karpathy]] — wiki pattern author
- [[context-farming]] — feeds the wiki side
- [[mcp]] — could feed either architecture
