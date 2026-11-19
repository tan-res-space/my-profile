# Tanmoy Roy — Profile & CV

Personal profile site and multi-format CV system, hosted on GitHub Pages.

**Live site:** [https://tan-res-space.github.io/my-profile](https://tan-res-space.github.io/my-profile)

## Structure

```
my-profile/
├── .github/workflows/    GitHub Actions (deploy site to Pages, auto-build CVs)
├── _layouts/             Jekyll HTML templates
├── _includes/            Header, footer components
├── _posts/               Blog posts
├── assets/css/           Stylesheet
├── cv_source/            LaTeX source files
├── cv_builds/            Auto-generated CV PDFs
├── pages/                Site pages (CV, Research, Blog, Contact)
└── index.md              Home page
```

## Publishing

The site is built with Jekyll and deployed by `.github/workflows/pages.yml`
(GitHub Actions) on every push to `main`. Pull requests get a build-only check.
Repository setting needed once: **Settings > Pages > Build and deployment >
Source: GitHub Actions**.

Not published on the site (see `exclude` in `_config.yml`): `cv_source/`,
`cv_builds/`, `linkedin_ops/`, `.agents/`, `.cursor/`. The CV PDFs contain phone
numbers and referee details, so the site shows a web CV (`pages/cv.md`) with a
"Save as PDF" button instead of linking the PDFs. The workflow fails the build if
any phone number or private employer/project name shows up in `_site/`.

## CV System

The CV is maintained as a single LaTeX file (`cv_source/cv_detailed.tex`) with conditional compilation flags (via `etoolbox`). Four versions are generated from this single source:

| Version | Driver File | Description |
|---------|------------|-------------|
| **Detailed** | `cv_detailed.tex` | Full CV with all sections |
| **Industry** | `cv_industry.tex` | Industry-focused; keeps PhD/PostDoc in Experience; omits research/teaching/publications |
| **Brief** | `cv_brief.tex` | Concise 1-2 page version; PhD/PostDoc remain in Experience |
| **No Research** | `cv_noresearch.tex` | Detailed industry roles plus UJ fellowships; no research/training sections |
| **Mercor** | `cv_mercor.tex` | Standalone; targets Mercor AI-training/evaluation roles; facts only from the detailed CV; no references |

PDFs are **automatically rebuilt** via GitHub Actions whenever files in `cv_source/` are modified. You can also trigger a manual build from the Actions tab.

## Local Development

### Site preview (requires Ruby + Jekyll)
```bash
bundle config set --local path vendor/bundle
bundle install
bundle exec jekyll serve
# Visit http://localhost:4000/my-profile
```

### CV compilation (requires TeX Live)
```bash
cd cv_source
make all        # Build all versions
make industry   # Build one version
make clean      # Remove build artifacts
```

## Updating Content

- **Profile/pages:** Edit markdown files in `pages/` or `index.md`
- **CV content:** Edit `cv_source/cv_detailed.tex` — all PDF versions rebuild automatically on push. The web CV on the site is `pages/cv.md` and is edited separately.
- **Blog posts:** Add new `.md` files to `_posts/` with the format `YYYY-MM-DD-title.md`
- **Styling:** Edit `assets/css/style.css`

## License

Content is copyright Tanmoy Roy. The Jekyll template structure is open for reuse.
