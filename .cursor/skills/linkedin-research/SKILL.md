---
name: linkedin-research
description: Researches LinkedIn topics that demonstrate Tanmoy Roy's expertise in SLMs, on-prem healthcare AI, medical ASR, and evaluation. Use when preparing the next LinkedIn post, scanning papers, or refreshing the content calendar.
disable-model-invocation: true
---

# LinkedIn research

Read `linkedin_ops/pillars.md` and the next 2 rows in `linkedin_ops/calendar.yml`.

## Scan (every time)

1. Anchor against P0 thesis: measurable confidence, white-box SLM, on-prem, specialist vs generic LLM.
2. Pull 2–4 **primary** sources from the last 90 days: arXiv, NVIDIA/Google/MS research blogs, HIM/AHIMA/CHIA practitioner writing. No listicles as claims.
3. Map each candidate to a pillar: `slm-agents` | `healthcare-speech` | `evaluation` | `craft`.
4. For each: Tanmoy's unique angle (DeliverHealth public work, PhD endpoints/SER, Siemens-to-research path). Drop anything he cannot speak to from lived work.
5. Flag IP risk. If a claim needs an unpublished number, replace with a qualitative bar or skip.

## Default corpus (already used)

- Belcak et al., arXiv:2506.02153, Section 6 conversion algorithm
- NVIDIA blog: SLMs as workers, LLMs as consultants
- NVIDIA on-prem / NIM ASR for HIPAA audio (cite as industry architecture, not as "we use this")
- Andrew Ng laptop/on-prem quote; Karpathy on model size coming down

## Output

Write `linkedin_ops/research/YYYY-MM-DD.md`:

- 3 topic options ranked
- Sources with URLs
- Recommended calendar id (P#) or a swap proposal
- Hashtag triplet from `hashtags.md`
- What **not** to say

Do not draft the post here. Hand off to `linkedin-draft`.
