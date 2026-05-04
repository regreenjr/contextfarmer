# contextfarmer

Self-updating Karpathy-style LLM wiki for AI consulting + GTM playbook + competitive intel. Sources are fetched daily by scheduled "context farmers" running on Claude Code; the wiki maintains itself.

## What this repo holds

- `farmers/` — declarative configs, one per source. Each is ~30 lines of YAML + markdown.
- `raw/` — immutable source data dumped by farmers (transcripts, ad copy, tweet reports). Wiki layer never modifies these.
- `wiki/` — LLM-maintained knowledge base: entities, concepts, sources, comparisons, synthesis. The compounding output.
- `CLAUDE.md` — schema + conventions read by Claude Code on every operation.
- `SETUP.md` — operating guide.

## How it works

```
fetcher (Apify YouTube / X / FB Ad Library / etc.)
   ↓
raw/<source-type>/<slug>.md
   ↓
/wiki-ingest <path>            (the wiki-ingestor sub-agent)
   ↓
wiki/sources/, entities/, concepts/   ← cross-referenced markdown
   ↓
git auto-commit + push  ← cloud routines pull, run, commit, push
   ↓
Obsidian Git plugin pulls locally
```

## Pattern

[Karpathy's LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f), but with the manual-update problem solved by separating selection (taste) from fetching (cron).

## Skills required

- [`alirezarezvani/claude-skills/engineering/llm-wiki`](https://github.com/alirezarezvani/claude-skills/tree/main/engineering/llm-wiki) — wiki maintenance, sub-agents, slash commands
- `farmer` (custom, in `~/.claude/skills/farmer/`) — orchestrator that wraps fetchers + calls /wiki-ingest

## License

Private.
