# Tanmoy Roy — Profile & CV

Personal profile site and multi-format CV system, hosted on GitHub Pages.

**Live site:** [https://tan-res-space.github.io/my-profile](https://tan-res-space.github.io/my-profile)

## Structure

```
my-profile/
├── .github/workflows/    GitHub Actions (auto-build CVs)
├── _layouts/             Jekyll HTML templates
├── _includes/            Header, footer components
├── _posts/               Blog posts
├── assets/css/           Stylesheet
├── cv_source/            LaTeX source files
├── cv_builds/            Auto-generated CV PDFs
├── pages/                Site pages (CV, Research, Blog, Contact)
└── index.md              Home page
```

## CV System

The CV is maintained as a single LaTeX file (`cv_source/cv_detailed.tex`) with conditional compilation flags (via `etoolbox`). Four versions are generated from this single source:

| Version | Driver File | Description |
|---------|------------|-------------|
| **Detailed** | `cv_detailed.tex` | Full CV with all sections |
| **Industry** | `cv_industry.tex` | Industry-focused; keeps PhD/PostDoc in Experience; omits research/teaching/publications |
| **Brief** | `cv_brief.tex` | Concise 1-2 page version; PhD/PostDoc remain in Experience |
| **No Research** | `cv_noresearch.tex` | Detailed industry roles plus UJ fellowships; no research/training sections |

PDFs are **automatically rebuilt** via GitHub Actions whenever files in `cv_source/` are modified. You can also trigger a manual build from the Actions tab.

## Local Development

### Site preview (requires Ruby + Jekyll)
```bash
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
- **CV content:** Edit `cv_source/cv_detailed.tex` — all versions rebuild automatically on push
- **Blog posts:** Add new `.md` files to `_posts/` with the format `YYYY-MM-DD-title.md`
- **Styling:** Edit `assets/css/style.css`

## License

Content is copyright Tanmoy Roy. The Jekyll template structure is open for reuse.
