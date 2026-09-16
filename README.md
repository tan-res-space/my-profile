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
├── cv_source/            YAML content + LaTeX layout
├── cv_builds/            Auto-generated CV PDFs
├── pages/                Site pages (CV, Research, Blog, Contact)
└── index.md              Home page
```

## CV System

CV **content** lives in `cv_source/cv.yaml`. Layout stays in LaTeX (`structure.tex` plus a generated `.tex` file per version) so PDF quality is unchanged. `render_cv.py` turns the YAML into complete LaTeX files; GitHub Actions compiles them to PDF.

Four versions ship by default, plus a teacher/educationist profile. Add another by copying an entry under `profiles:` in `cv.yaml` and running `python3 render_cv.py`.

| Version | Profile id | Description |
|---------|------------|-------------|
| **Detailed** | `detailed` | Full CV with all sections |
| **Industry** | `industry` | Industry-focused, no academic sections |
| **Brief** | `brief` | Concise 1-2 page version |
| **No Research** | `noresearch` | Detailed industry roles, no research/training |
| **Educationist** | `educationist` | Teaching, training, and research supervision first |

PDFs are **automatically rebuilt** via GitHub Actions whenever files in `cv_source/` are modified. You can also trigger a manual build from the Actions tab.

## Local Development

### Site preview (requires Ruby + Jekyll)
```bash
bundle install
bundle exec jekyll serve
# Visit http://localhost:4000/my-profile
```

### CV compilation (requires Python 3 + PyYAML + TeX Live)
```bash
pip install -r cv_source/requirements.txt
cd cv_source
make test       # Validate YAML profiles
make all        # Render LaTeX and build all PDFs
make industry   # Build one version (run make generate first if needed)
make clean      # Remove build artifacts
```

## Updating Content

- **Profile/pages:** Edit markdown files in `pages/` or `index.md`
- **CV content:** Edit `cv_source/cv.yaml` — all versions rebuild automatically on push
- **CV layout:** Edit `cv_source/structure.tex` or `cv_source/render_cv.py`
- **Blog posts:** Add new `.md` files to `_posts/` with the format `YYYY-MM-DD-title.md`
- **Styling:** Edit `assets/css/style.css`

## License

Content is copyright Tanmoy Roy. The Jekyll template structure is open for reuse.
