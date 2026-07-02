---
title: Open Knowledge Format (OKF)
category: concept
summary: **Google's open standard (shipped ~2026-07, surfaced via [[cole-medin]] in [[youtube-digest-apify-2026-07-02]]) that formalizes [[andrej-karpathy]]'s LLM-wiki pattern into plain markdown any AI can read with zero integration** — *"no plugin, RAG pipeline, or vector DB; you point your agent at a folder and ask it anything as long as it knows OKF."* Published under **GoogleCloudPlatform** on GitHub with a `SPEC.md` and a `cloud.google.com/blog` launch post. Converts [[karpathy-llm-wiki]] from a *convention* (a viral April-2026 gist) into a *cross-vendor spec*, and is the **open-standard answer** to the [[knowledge-layer]] open question "will an open spec emerge, or proprietary lock-in?" — notably shipped by the same player (Google) that shipped the proprietary Knowledge Catalog. Direct validation *and* a differentiation-risk signal for this vault, which is itself a Karpathy LLM wiki
tags: [open-knowledge-format, okf, google, open-standard, spec, markdown, karpathy-llm-wiki, knowledge-layer, andrej-karpathy, cole-medin, portability, cross-vendor, zero-integration, second-brain, data-moat, agent-interop]
sources: 1
updated: 2026-07-02
---

# Open Knowledge Format (OKF)

## Definition

**OKF** is an **open standard from Google** that formalizes [[andrej-karpathy]]'s LLM-wiki pattern ([[karpathy-llm-wiki]]) into **plain markdown that any AI can read with zero integration**. Per [[cole-medin]]'s coverage (*Finally, an Open Standard for the Karpathy LLM Wiki is HERE*, [[youtube-digest-apify-2026-07-02]] #2):

> *"Google just quietly shipped the Open Knowledge Format (OKF): an open standard that formalizes Andrej Karpathy's LLM wiki pattern into plain markdown any AI can read with zero integration. No plugin, RAG pipeline, or vector DB. You point your agent at a folder and ask it anything as long as it knows OKF."*

Artifacts named in the coverage:
- A **`SPEC.md`** — the format specification
- A repo under **`GoogleCloudPlatform`** on GitHub
- A **launch blog** on `cloud.google.com/blog`
- [[cole-medin]]'s **open-source OKF bundle** (`github.com/coleam00`) — a clonable demonstration ("clone this and point your AI at it") that lets any agent search his YouTube content

*(Exact URLs are truncated in the digest; transcript / the blog post would resolve the canonical links and the SPEC contents.)*

## The problem it solves — the missing shared format

Cole's framing: you already have a personal agent, search that works, and *"some version of a second brain."* Yet *"it's still basically impossible to hand your knowledge to someone else's AI and have it just work. The answer is we never agreed on a format."* OKF is the **interop layer** — the agreed-upon file format that makes a knowledge base **portable across any AI**, the way a shared file format (not a plugin) is what makes documents portable.

This is the **portability corollary** to [[nate-b-jones]]'s same-batch *own the memory, rent the intelligence* thesis (#1 in the same digest): if you own your memory, OKF is what lets you carry it to whatever intelligence you rent.

## Why it matters for this vault (and 3Ps)

**This vault is a Karpathy LLM wiki, so OKF is a standard for the vault's own architecture.** Three consequences:

1. **Validation, one tier deeper than [[knowledge-layer]].** The commercial convergence ([[pinecone]] Nexus, Microsoft Fabric IQ, Google Knowledge Catalog) proved *vendors* would build products on the pattern. OKF proves the pattern is worth **standardizing as an open spec** — the strongest possible signal that `raw/` → `wiki/` markdown-with-cross-references is a durable architecture, not a hobbyist convention.
2. **Answers a standing open question.** [[knowledge-layer]] asked: *"will KnowQL or an open spec emerge as the cross-vendor layer, or proprietary lock-in across the three vendors?"* OKF is the **open-spec answer** — and, pointedly, it's **Google** shipping the *open, portable* standard rather than doubling down on its proprietary Knowledge Catalog. Interop over lock-in, at least at the format layer.
3. **Differentiation-risk signal.** As [[karpathy-llm-wiki]] already noted, "I have a wiki" stopped being a differentiator once the pattern went mainstream. A *named open standard* accelerates that: soon "my wiki is OKF-compliant" is table stakes. Differentiation moves further toward **what's in the wiki and how well the farmers feed it** — and possibly toward **being OKF-native early** (a "3Ps OKF-compliant vault starter" is a sharper lead-magnet than a generic wiki).

**Concrete follow-up:** clone Cole's bundle + read the `SPEC.md`, then diff OKF's required structure against this vault's `CLAUDE.md` schema (frontmatter fields, `entities/`/`concepts/`/`sources/` layout, `> ⚠️ Contradiction:` callouts, `log.md`). If OKF is close, adopting it makes the vault portable to any OKF-aware agent for near-zero cost; if it diverges, the gap is itself a content/positioning angle.

## Where it sits relative to other vault concepts

| Concept | Layer | Relationship to OKF |
|---|---|---|
| [[karpathy-llm-wiki]] | The *pattern* (a gist / convention) | OKF is the **formal spec** of this pattern — convention → standard |
| [[knowledge-layer]] | The *commercial category* (Nexus / Fabric IQ / Knowledge Catalog) | OKF is the **open-standard / interop** answer to that category's proprietary products |
| [[karpathy-wiki-vs-openbrain]] | The *write-time vs query-time* fork | OKF standardizes the **write-time (wiki) side**; it's a format for compiled markdown, not a query-time memory service |
| [[open-engine]] / [[open-skills]] | Cross-vendor *work* / *procedure* portability | OKF is the cross-vendor *knowledge* portability sibling — the third "make it travel between agents" primitive |
| own the memory, rent the intelligence ([[nate-b-jones]], same batch) | The *ownership* thesis | OKF makes owned memory **portable** across rented intelligence |

## Open questions

- **What's actually in the `SPEC.md`?** Required frontmatter, page types, link syntax, contradiction/versioning conventions — all gated to the spec + transcript.
- **How does OKF differ from this vault's `CLAUDE.md` schema?** (Compatible enough to adopt? A superset? A different link/frontmatter convention?)
- **Who else adopts it?** A Google spec is only an interop win if Anthropic / OpenAI agents honor it. Does it get cross-vendor uptake, or stay a Google-Cloud artifact? (Watch whether [[andrej-karpathy]] — now at [[anthropic]] — or Anthropic tooling references OKF.)
- **Relationship to [[knowledge-layer]] products** — is OKF the *export/interchange* format the proprietary knowledge-layer engines compile *to* / read *from*, or a competing free alternative?
- **Does it specify a query contract** (like [[retrieval-contract]] / KnowQL), or only the storage format? Cole frames it as a *read* format ("point your agent at a folder"), suggesting storage-side only.

## Used in

- [[youtube-digest-apify-2026-07-02]] — vault entry point ([[cole-medin]] #2)
- [[cole-medin]] — the creator who surfaced it

## Related

- [[karpathy-llm-wiki]] — the pattern OKF formalizes (this vault's architecture)
- [[andrej-karpathy]] — originator of the pattern; now at [[anthropic]]
- [[knowledge-layer]] — the commercial category; OKF is its open-standard counterpart
- [[cole-medin]] — surfacing creator; ships the open-source OKF bundle
- [[karpathy-wiki-vs-openbrain]] — the write-time side OKF standardizes
- [[open-engine]], [[open-skills]] — sibling cross-vendor portability primitives
- [[nate-b-jones]] — same-batch "own the memory, rent the intelligence" ownership thesis OKF makes portable
