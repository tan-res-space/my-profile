---
id: P1
status: drafted
schedule: 2026-09-23 08:00 IST
slot: A
pillar: slm-agents
hashtags: [SmallLanguageModels, AgenticAI, HealthcareAI]
---

# Body (paste into LinkedIn)

NVIDIA Research did not just argue that small language models belong in agents. They published a conversion algorithm.

Most teams I talk to skip it. They jump to “which 7B should we fine-tune?” That is how you get a small model that is just as untrustworthy as the big one — only cheaper.

Belcak et al. start somewhere less glamorous. Log the actual agent calls. Not the chat. The repetitive jobs: extract, route, fill a schema, score a candidate. Strip PHI. Cluster those jobs. Then pick a specialist per cluster. Then fine-tune. Then iterate.

We ran a version of this in healthcare. The job was not “be a doctor.” It was “propose an answer, and tell us how sure you are.” Once we treated it as a specialist task, a single-GPU SLM beat a generic Gemini setup on that task. The AUROC on “is this answer right?” moved from ~0.60 to ~0.90.

The conversion is not a model swap. It is a task inventory.

If every subtask still hits one frontier API, you do not have an agent. You have a very expensive intern with a single tool.

That’s the next bar: not a smaller chatbot. A smaller job.

#SmallLanguageModels #AgenticAI #HealthcareAI

## First comment (post immediately after publish)

Sources:
Peter Belcak et al., “Small Language Models are the Future of Agentic AI,” NVIDIA Research — conversion algorithm is Section 6.
https://arxiv.org/abs/2506.02153

NVIDIA technical blog on SLMs in agentic systems:
https://developer.nvidia.com/blog/how-small-language-models-are-key-to-scalable-agentic-ai/

This continues last month’s post on measurable confidence vs fluency.

## First hour

Reply to every comment. If someone asks “which SLM?”, do not name an unreleased stack. Answer with the job: schema + calibration + on-prem logits.
