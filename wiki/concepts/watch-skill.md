---
title: Watch Skill (/watch — Give Claude Code Eyes on Any Video)
category: concept
summary: [[brad-bonanno]]'s free, open-source [[claude-skills|Claude skill]] (`/watch`, on GitHub) that closes a real [[claude-code]] capability gap — video comprehension; *"Claude Code can't watch videos — until you give it the `/watch` skill. Paste a link and Claude pulls the **frames and the transcript together**, so it understands what happens on screen and when."* Works across **1,600+ sites** (YouTube, Zoom recordings, Looms, TikToks, local files) and *"demolished a 2-hour interview in seconds."* Surfaced via *This Skill Can INSTANTLY Watch any Video For Free* (1.2K views, 2026-07-02). **v2** is a token-economics rewrite — **smart scene selection**, **deictic targeting** (find the exact frame a speaker points at), **token-burner mode**, **efficient keyframe extraction** (**40× faster** — pulls keyframes from the file instead of rebuilding every frame), and **frame deduplication** (stop paying tokens for near-identical talking-head frames) — plus a first-run mode picker across four modes.
tags: [brad-bonanno, watch-skill, watch, claude-skills, claude-code, video-understanding, multimodal, frames-plus-transcript, smart-scene-selection, deictic-targeting, token-burner-mode, keyframe-mode, frame-deduplication, token-costs, substrate-economics, free-github-skill, lead-magnet, context-farming]
sources: 1
updated: 2026-07-03
---

# Watch Skill (/watch)

## What it is

`/watch` is a **free, open-source [[claude-skills|Claude skill]]** (hosted on GitHub) from [[brad-bonanno]] that gives [[claude-code]] the ability to **watch video** — a capability Claude Code otherwise lacks. Surfaced via *This Skill Can INSTANTLY Watch any Video For Free - Here's How* (1.2K views, 2026-07-02, 08:31) in [[sources/youtube-digest-apify-2026-07-03]].

The mechanism: *"Paste a link and Claude pulls the **frames and the transcript together**, so it understands what happens on screen and when."* Frames + transcript, aligned in time — not just an audio transcription. It works across **over 1,600 sites** — YouTube, Zoom recordings, Looms, TikToks — plus local files, and per Brad *"demolished a 2-hour interview in seconds."*

## v2 — the token-economics rewrite

Brad frames v2 as *"the biggest upgrade since launch,"* and almost every headline feature is about **spending fewer tokens for the same understanding**:

| Feature | What it does |
|---|---|
| **Smart scene selection** (2:14) | Picks the frames that actually matter instead of sampling blindly. |
| **Deictic targeting** | When a speaker says *"look at this,"* Claude finds the **exact frame** they're pointing at. |
| **Token burner mode** | Takes the cap off entirely for maximum detail when you need it. |
| **Efficient keyframe mode** | Pulls keyframes **straight out of the video file** instead of rebuilding every frame — *"that's where the 40× comes from."* |
| **Frame deduplication** | Strips near-identical frames (a talking head barely changes) so *"you stop paying tokens for the same picture twice."* |

Brad is explicit that dedup is a direct response to user feedback: *"half the comments on v1 were about token costs, so this one's for you."* Install is *"two commands, two minutes,"* with a **first-run mode picker** so you know which of the four modes to choose.

## Key claims

- **Claude Code cannot natively watch video; `/watch` closes the gap** — cited from [[sources/youtube-digest-apify-2026-07-03]].
- **Frames + transcript are pulled together and time-aligned** — the skill understands *what happens on screen and when*, not just what is said.
- **1,600+ supported sites + local files** — YouTube / Zoom / Loom / TikTok and more.
- **v2 is ~40× faster** via keyframe extraction from the file rather than frame rebuilding.
- **Frame deduplication is the token-cost fix** for the #1 v1 complaint.

## Where it sits in the vault

- **Another free-skill-as-lead-magnet in [[brad-bonanno]]'s playbook** — sibling of his [[content-ideas-skill]]. But unlike content-ideas (a workflow tool), `/watch` closes a genuine **[[claude-code]] capability gap** (video comprehension).
- **Squarely in the 2026 substrate-economics cluster** — the v2 story is almost entirely token management (keyframe extraction, dedup, mode picker), the same "manage your tokens" consensus behind [[prompt-caching]], [[glm]], [[model-routing]], and [[token-burn-dashboard]] — here applied to **multimodal ingest**.
- **A primitive this vault can adopt** — the YouTube [[context-farming|farmer]] currently ingests **titles + descriptions + chapters only** (transcripts explicitly not pulled, per the digest notes). `/watch` is the primitive that could upgrade the farmer to **frame-level video understanding** of the videos it tracks.

## Why it matters for 3Ps

- **A deliverable-grade ingest primitive** — "point Claude at any client call recording / webinar / competitor video and get a time-aligned frame-plus-transcript summary" is a billable, repeatable service.
- **Token-cost transparency is the sell** — the four-mode picker (cheap keyframe → token burner) lets you tune cost-per-video to the job, the same routing instinct as [[model-routing]].

## Open questions

- **The exact GitHub repo** — named as free-on-GitHub; skill download gated to `brad-b.kit.com/5ca85f4a2a`, repo URL not captured in the digest.
- **Which of the four modes is the sensible default** for scheduled/unattended farmer use (where no human runs the first-run picker)?
- **How it handles very long inputs at scale** — v2 claims *"handles ultra-long videos,"* but the token cost of a full 2-hour ingest in token-burner mode is unstated.

## Used in

- [[sources/youtube-digest-apify-2026-07-03]] — vault entry point (Brad Bonanno #2)
- [[brad-bonanno]] — author

## Related

- [[claude-skills]] — the packaging unit `/watch` ships as
- [[claude-code]] — the harness whose video-comprehension gap it closes
- [[content-ideas-skill]] — Brad's other free-skill-as-lead-magnet
- [[context-farming]] — the farmer pattern this could upgrade to frame-level video ingest
- [[prompt-caching]], [[glm]], [[model-routing]], [[token-burn-dashboard]] — fellow substrate-economics / token-cost levers
