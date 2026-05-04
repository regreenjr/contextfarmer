---
name: x-trends
description: Daily X/Twitter scan of AI + marketing accounts and keywords; scored tweets become wiki signals
fetcher_skill: x-monitor
fetcher_args:
  authors:
    - "karpathy"
    - "swyx"
    - "alexalbert__"          # Anthropic dev rel
    - "natfriedman"
    - "GergelyOrosz"          # tech leadership
    - "AlexHormozi"           # GTM/marketing
    - "ShaanVP"               # business + marketing
  keywords:
    - "Claude Code"
    - "claude skill"
    - "managed agent"
    - "context farming"
    - "GTM engineering"       # for 3Ps positioning
    - "AI consulting"
  min_score: 0.65             # softmax threshold for inclusion
  since: "{{ last_run }}"
raw_path: raw/twitter/{date}.md
ingest: auto
dedup_by: report-date         # one report per day; never two
last_run: 2026-05-03
schedule_cron: "30 6 * * *"
auto_commit: true
---

# X / Twitter Trends Farmer

## Purpose
Catch high-signal tweets the day they're posted, not three weeks later. Scored
by velocity + authority + topical relevance. The wiki gets a daily report; the
report links into entity pages (people I track) and concept pages (topics).

The `x-monitor` skill already handles dedup via Supabase, so this farmer just
captures the **markdown report it produces** and saves it as the wiki source.
Each daily report becomes one source page; the ingestor builds entity/concept
pages from the people and topics referenced.

## What I'm looking for
- **Anthropic platform changes** — managed agents, skills marketplace, MCP updates
- **GTM/marketing patterns** — what's working for solopreneurs and consultants
- **Karpathy-style thinking** — frameworks for working with LLMs that compound
- **Competitor signals** — when names in my space (Brad, etc.) drop something new

## Notes
- Daily report is enough; don't run hourly (X dedup costs)
- Score threshold 0.65 keeps the noise out — tune up if too much, down if too little
- Reports older than 30 days lose ingest priority — the wiki has the entity/concept
  layer by then; new tweets only matter if they update an existing claim
