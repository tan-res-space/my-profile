---
name: linkedin-ops
description: Orchestrates Tanmoy Roy's LinkedIn content system — calendar, cadence, hashtags, drafting, engagement, and weekly review. Use when the user mentions LinkedIn posts, scheduling, content calendar, hashtags, reach, or deploying the LinkedIn agents.
---

# LinkedIn ops

Read `linkedin_ops/README.md` and `linkedin_ops/calendar.yml` first. Then `voice.md`, `hashtags.md`, `pillars.md`.

## Route

| User wants | Load skill |
|---|---|
| Topics, papers, what to post next | `.cursor/skills/linkedin-research/SKILL.md` |
| Write / rewrite a post | `.cursor/skills/linkedin-draft/SKILL.md` |
| Comments, first hour, daily 3 | `.cursor/skills/linkedin-engage/SKILL.md` |
| Analytics, slot A vs B, change cadence | `.cursor/skills/linkedin-review/SKILL.md` |

Do the work in `linkedin_ops/`. Update `calendar.yml` status (`outlined` → `drafted` → `scheduled` → `published`). Append `metrics.md` after publish.

## Cadence (do not improvise)

- Slot A: Wednesday 08:00 IST
- Slot B: Thursday 19:00 IST
- 2 posts/week unless review says otherwise
- Exactly 3 hashtags
- Links in first comment only
- No unofficial LinkedIn posting bots. User publishes or uses native scheduler.

## Before P1

If P0 still has unreplied comments, say so and draft the reply before any new post.
