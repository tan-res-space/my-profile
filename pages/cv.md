---
layout: page
title: Curriculum Vitae
subtitle: Download my CV in the format that best suits your needs.
permalink: /pages/cv/
---

I maintain multiple versions of my CV tailored for different audiences. Content is stored in YAML and typeset with LaTeX; GitHub Actions rebuilds every PDF from that single source.

<div class="cv-grid">

  <div class="cv-card">
    <h3>Detailed (Full)</h3>
    <p>Complete academic and industry CV with all experience, research, publications, teaching, and references.</p>
    <a href="{{ '/cv_builds/cv_detailed.pdf' | relative_url }}" class="btn btn-primary" target="_blank">Download PDF</a>
  </div>

  <div class="cv-card">
    <h3>Industry</h3>
    <p>Focused on industry experience and technical skills. Omits academic research sections, publications, and teaching details.</p>
    <a href="{{ '/cv_builds/cv_industry.pdf' | relative_url }}" class="btn btn-primary" target="_blank">Download PDF</a>
  </div>

  <div class="cv-card">
    <h3>Brief</h3>
    <p>Concise 1&ndash;2 page version with condensed project descriptions. Ideal for quick screening.</p>
    <a href="{{ '/cv_builds/cv_brief.pdf' | relative_url }}" class="btn btn-primary" target="_blank">Download PDF</a>
  </div>

  <div class="cv-card">
    <h3>Detailed (No Research)</h3>
    <p>Full project descriptions for all industry roles, but without research, training, and academic sections.</p>
    <a href="{{ '/cv_builds/cv_noresearch.pdf' | relative_url }}" class="btn btn-primary" target="_blank">Download PDF</a>
  </div>

</div>

---

### How it works

The CV source lives in `cv_source/cv.yaml`. Each named profile under `profiles` (detailed, industry, brief, noresearch) selects which tagged sections and which summary to include. A small Python renderer writes a complete `.tex` file per profile; GitHub Actions compiles those files to PDF so layout stays in LaTeX.
