---
layout: home
---

<section class="hero">
  <p class="eyebrow">AI researcher &amp; engineer &middot; PhD</p>
  <h1 class="hero-name">Tanmoy Roy</h1>
  <p class="hero-lede">I build AI that knows when it might be wrong.</p>
  <div class="hero-links">
    <a class="btn btn-primary" href="{{ '/pages/cv/' | relative_url }}">View CV</a>
    <a class="btn btn-ghost" href="{{ site.author.linkedin }}" target="_blank" rel="noopener">LinkedIn</a>
    <a class="btn btn-ghost" href="{{ site.author.scholar }}" target="_blank" rel="noopener">Google Scholar</a>
    <a class="btn btn-ghost" href="{{ site.author.github }}" target="_blank" rel="noopener">GitHub</a>
  </div>
</section>

<section class="section about" aria-labelledby="about-title" markdown="1">
<h2 id="about-title" class="section-title">About</h2>

I design and build on-prem language models for medical coding, clinical notes and speech recognition. Every answer carries a calibrated confidence score, so we know when to trust the model and when to hand the work to a person.

- Medical coding: a fine-tuned model reads a full patient chart and matches human coders on 92.1% of E/M levels, up from 83.0%. Confidence AUROC is 0.89, with 96%-coverage candidate sets.
- Medical speech recognition: a fine-tuned engine at 12% word error rate, with no audio sent to a public cloud.
- Retrieval-based correction of speech drafts and automated clinical note generation.
{: .highlights}

As a consultant, I design agentic AI systems:

- AI-driven data delivery: from discovery to reviewed mappings to a deployed cloud pipeline, built for a US healthcare provider.
- Plan-and-execute agents: a cloud planner that checks the work, and an on-prem agent that runs only human-approved plans.
{: .highlights}

My route here was not straight: 8+ years at Siemens building telecom and EV-charging billing systems, then a PhD and post-doc in speech emotion recognition at the University of Johannesburg, and seven peer-reviewed publications. The engineer in me wants it to run on the hardware we have. The researcher in me wants the evaluation written down before the result comes in.

Focus areas: small language models, fine-tuning and compression, confidence calibration, medical ASR, RAG and agentic AI.
{: .focus}

Models small enough to inspect and honest enough to defer. Not more fluent. More honest.
{: .closing}
</section>

<section class="section" aria-labelledby="explore-title">
  <h2 id="explore-title" class="section-title">Explore</h2>
  <div class="card-grid">
    <a class="card" href="{{ '/pages/cv/' | relative_url }}">
      <span class="card-kicker">CV</span>
      <span class="card-title">Experience, education &amp; skills</span>
      <span class="card-text">19+ years across healthcare AI, finance, telecom and academic research.</span>
    </a>
    <a class="card" href="{{ '/pages/research/' | relative_url }}">
      <span class="card-kicker">Research</span>
      <span class="card-title">Publications</span>
      <span class="card-text">Speech emotion recognition, speech endpoint detection, computer vision and NLP.</span>
    </a>
    <a class="card" href="{{ '/pages/contact/' | relative_url }}">
      <span class="card-kicker">Contact</span>
      <span class="card-title">Get in touch</span>
      <span class="card-text">Consulting, research collaborations, training and conversations about AI/ML.</span>
    </a>
  </div>
</section>
