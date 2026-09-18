---
layout: page
title: Curriculum Vitae
subtitle: Download my CV in the format that best suits your needs.
permalink: /pages/cv/
---

I maintain multiple versions of my CV tailored for different audiences. All versions are auto-built from a single LaTeX source using GitHub Actions.

<div class="cv-grid">

  <div class="cv-card">
    <h3>Detailed (Full)</h3>
    <p>Complete academic and industry CV with all experience, research, publications, teaching, and references.</p>
    <a href="{{ '/cv_builds/cv_detailed.pdf' | relative_url }}" class="btn btn-primary" target="_blank">Download PDF</a>
  </div>

  <div class="cv-card">
    <h3>Industry</h3>
    <p>Focused on industry experience and technical skills. Research and post-doctoral roles appear in condensed form to keep the timeline complete; publications and teaching details are omitted.</p>
    <a href="{{ '/cv_builds/cv_industry.pdf' | relative_url }}" class="btn btn-primary" target="_blank">Download PDF</a>
  </div>

  <div class="cv-card">
    <h3>Brief</h3>
    <p>Concise 1&ndash;2 page version with condensed project and research descriptions covering the full 2007&ndash;present timeline. Ideal for quick screening.</p>
    <a href="{{ '/cv_builds/cv_brief.pdf' | relative_url }}" class="btn btn-primary" target="_blank">Download PDF</a>
  </div>

  <div class="cv-card">
    <h3>Detailed (No Research)</h3>
    <p>Full project descriptions for all industry roles. Academic roles are listed in condensed form so the timeline stays continuous, without the research, training, and publication sections.</p>
    <a href="{{ '/cv_builds/cv_noresearch.pdf' | relative_url }}" class="btn btn-primary" target="_blank">Download PDF</a>
  </div>

</div>

---

### How it works

The CV source lives in a single LaTeX file (`cv_detailed.tex`) with conditional compilation flags. Each version is a thin driver file that sets one flag and compiles the same source, ensuring all versions stay in sync. A GitHub Actions workflow automatically rebuilds all PDFs whenever the LaTeX source is updated.
