---
id: P0
status: published
url: https://lnkd.in/p/d43WkBWg
canonical: https://www.linkedin.com/posts/tanmoy-roy-328b592b_smalllanguagemodels-slm-agenticai-share-7494834075690766337-01cZ
impressions: 713
reactions: 9
comments: 3
hashtags: [SmallLanguageModels, SLM, AgenticAI, ResponsibleAI, HealthcareAI, OnPremiseAI]
---

# Not more fluent. More honest. (anchor)

The AI industry is quietly shifting its obsession from brute-force scale to small language models (SLMs). The reason that mattered for us was not fluency. It was confidence you can measure.

“Why do I need to send all my data to a cloud provider when a small language model can do it just fine on my laptop?"- Andrew Ng

"Small language models are sufficiently powerful, inherently more suitable, and necessarily more economical for many invocations in agentic systems." - Peter Belcak et al., NVIDIA Research

"What the models have done in size is they’ve gone up and now they’ve come down. State-of-the-art models are smaller.” - Andrej Karpathy

We run an SLM on a single GPU, ensuring sensitive data never leaves our environment. Because it’s a white-box model, we get direct access to token probabilities and hidden states - not just a verbal “I’m sure.” It’s cheap enough to score multiple options per case rather than relying on a single guess.

That is the leverage: a confidence meter that went from near coin-flip (AUROC ~0.60) to actually useful (~0.90) at telling right from wrong. On this specific task, our setup with a specialized small models significantly outperformed a generic LLM (Gemini) based solution. Also, owning the SLMs is what let us know when to trust it.

Not just a smaller chatbot. A model small enough to inspect and honest enough to defer.

That’s the bar. Not more fluent. More honest.

[Quote sources in the first comment]

DeliverHealth

#SmallLanguageModels #SLM #AgenticAI #ResponsibleAI #HealthcareAI #OnPremiseAI

## First comment (already live)

Sources:
Andrew Ng — https://erictopol.substack.com/p/andrew-ng-on-openais-stormy-times
Peter Belcak et al. — https://arxiv.org/abs/2506.02153
Andrej Karpathy — https://www.dwarkesh.com/p/andrej-karpathy
