# Wiki — LLM Wiki

> **Topic:** 3Ps AI consulting + GTM playbook + AI creator landscape + competitive intel
> **Initialized:** 2026-05-03
> **Tool:** Claude Code (this file). A parallel `AGENTS.md` exists for Codex/Cursor/Antigravity.

You are the maintainer of this wiki. You read from `raw/`, you write to `wiki/`. You never edit `raw/`.

## The three layers

```
raw/     → sources (articles, papers, notes). IMMUTABLE. You only read.
wiki/    → the knowledge base. You own this. Create, update, cross-reference.
CLAUDE.md / AGENTS.md → schema (this file). Co-evolved with the user.
```

## Vault structure

```
raw/
├── <sources>              # articles, papers, notes — IMMUTABLE
└── assets/                # downloaded images from clipped articles

wiki/
├── index.md               # THIN root index (stats + TOC) — regenerate, never hand-edit
├── index/                 # per-category catalog shards: concepts.md, entities.md, sources.md, …
├── log.md                 # append-only timeline
├── entities/              # people, orgs, places, products
├── concepts/              # ideas, theories, frameworks
├── sources/               # one summary page per ingested source
├── comparisons/           # cross-source analysis
├── synthesis/             # high-level overviews and theses
└── .templates/            # page templates (reference only)
```

## Scripts path (absolute — this vault has no local `scripts/` dir)

All helper scripts live at **`/Users/robbgreenpro/.claude/skills/llm-wiki/scripts/`**.
Always invoke them by that absolute path, e.g.
`python3 /Users/robbgreenpro/.claude/skills/llm-wiki/scripts/update_index.py --vault .`

## Editing rules (read before you edit)

1. **ALWAYS Read the file immediately before any Edit.** For files >20KB, Read with
   `offset`/`limit` windows. Never Edit from remembered or assumed content — that is
   what causes "String to replace not found" / "File has not been read yet".
2. **To add a `[[wikilink]]` to a link-list section** (e.g. `## Appears in`,
   `## Where it's cited`, `## Used in`, `## Related`), do NOT hand-Edit the list. Use:
   `python3 /Users/robbgreenpro/.claude/skills/llm-wiki/scripts/append_wikilink.py --file <page> --section "## <Heading>" --link "<target>" --bump-updated`
   It reads the live file, is idempotent (a no-op if the link is already there), and
   appends one bullet safely.
3. **Pages >100KB** (see the **Large pages** list in `index.md`) must be read via
   `Grep` or windowed `Read` (offset/limit) — **never** whole-file (they exceed the
   Read cap). Fix how they're accessed; do not split them.
4. **Never hand-edit `index.md` or `index/*.md`.** They are generated —
   run `update_index.py` to regenerate the thin root + shards.

## Page frontmatter (required on every wiki page)

```yaml
---
title: <Title>
category: entity | concept | source | comparison | synthesis
summary: <one-line summary>
tags: [tag1, tag2]
sources: <count of sources referencing this page>
updated: YYYY-MM-DD
---
```

For `source` pages, also include:
```yaml
source_path: raw/<path>
source_date: YYYY-MM (original publication)
authors: [author1, author2]
ingested: YYYY-MM-DD
```

## The three operations

### Ingest (`/wiki-ingest <path>`)

1. Run `python3 /Users/robbgreenpro/.claude/skills/llm-wiki/scripts/ingest_source.py --vault . --source <path> --json` to get the brief
2. Read the source directly
3. **Discuss with the user first** — TL;DR, key claims, which pages will be touched, contradictions
4. Wait for confirmation
5. Create or merge the summary page at `wiki/sources/<slug>.md`
6. Update every relevant entity and concept page (typically 5-15 pages). **Read each page (offset/limit for big ones) immediately before editing it.** For link-list bullets (`## Appears in` / `## Where it's cited` / `## Used in` / `## Related`) use `append_wikilink.py` instead of hand-editing.
7. Flag contradictions with `> ⚠️ Contradiction:` callouts on both sides
8. Regenerate the index: `python3 /Users/robbgreenpro/.claude/skills/llm-wiki/scripts/update_index.py --vault .` (rebuilds the thin `index.md` + `index/` shards). Never hand-edit the index.
9. Run `python3 /Users/robbgreenpro/.claude/skills/llm-wiki/scripts/append_log.py --vault . --op ingest --title "<title>" --detail "<touched pages>"`
10. Report back with a bulleted list of touched pages

### Query (`/wiki-query <question>`)

1. Read the thin `wiki/index.md`, then open the relevant `wiki/index/<category>.md` shard(s) to pick pages
2. Pick 3-10 relevant pages across categories (synthesis + concepts + sources + entities)
3. Read them in full (pages >100KB in the index's **Large pages** list: use Grep / windowed Read, never whole-file)
4. Follow wikilinks opportunistically
5. Fall back to `python3 /Users/robbgreenpro/.claude/skills/llm-wiki/scripts/wiki_search.py --vault . --query <terms>` if the index doesn't surface the answer
6. Synthesize: direct answer (1-3 sentences) → supporting detail → inline `[[sources/xxx]]` citations → "Related pages" section
7. **Offer to file the answer back** as a new page in `comparisons/` or `synthesis/`

### Lint (`/wiki-lint`)

1. Run `python3 /Users/robbgreenpro/.claude/skills/llm-wiki/scripts/lint_wiki.py --vault .` for mechanical checks (orphans, broken links, stale, missing frontmatter, **large pages >100KB**, log gap)
2. Run `python3 /Users/robbgreenpro/.claude/skills/llm-wiki/scripts/graph_analyzer.py --vault .` for structural stats
3. Semantic checks: look for contradictions, stale claims, concepts mentioned without their own page, cross-reference gaps
4. Present findings as a markdown report with suggested actions
5. Append a `lint` entry to `log.md`

## Iron rules

1. **`raw/` is immutable.** You read from it; you never write to it.
2. **All writes go to `wiki/`.** No exceptions.
3. **Every wiki page has YAML frontmatter** with `title`, `category`, `summary`, `updated`.
4. **Every ingest touches ≥5 files.** The source summary, 2-4 entity/concept pages, `index.md`, `log.md`.
5. **Every claim has a citation.** Link back to the `sources/<slug>` page.
6. **Contradictions get flagged inline.** Both pages get the callout.
7. **Good answers get filed back.** Explorations compound.

## Log format

```
## [YYYY-MM-DD] <op> | <title>
<optional detail — which pages touched, what changed>
```

Valid ops: `ingest`, `query`, `lint`, `create`, `update`, `delete`, `note`.

Grep the log: `grep "^## \[" wiki/log.md | tail -10`

## Tools

All scripts live at the absolute path **`/Users/robbgreenpro/.claude/skills/llm-wiki/scripts/`** (this vault has no local `scripts/` dir — always use the absolute path). Standard library only.

- `init_vault.py` — bootstrap a vault
- `ingest_source.py` — prep a source for ingest (metadata + preview)
- `update_index.py` — regenerate the thin `wiki/index.md` + per-category `index/` shards from page frontmatter
- `append_wikilink.py` — idempotently append one `[[wikilink]]` bullet to a page's link-list section (use instead of hand-editing growing lists)
- `append_log.py` — append a standardized log entry
- `wiki_search.py` — BM25 search fallback
- `lint_wiki.py` — mechanical health check (incl. large-page >100KB warnings)
- `graph_analyzer.py` — link graph stats
- `export_marp.py` — render a page as a Marp slide deck

## Obsidian

The user opens this vault in Obsidian. They watch the graph view while you edit. Useful plugins: Graph view, Backlinks, Dataview, Marp, Templates, Git.

## Style

- Be concise. Wiki pages are read, not generated.
- Prefer short paragraphs. Bulleted lists where appropriate.
- Cite aggressively with `[[wikilinks]]`.
- When you're not sure, say so in the page. Don't invent content.
- Update `updated:` frontmatter whenever you touch a page.
