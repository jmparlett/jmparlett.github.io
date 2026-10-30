# How this site works

## Hosting / publishing

This is a **GitHub Pages user site** (`jmparlett/jmparlett.github.io`). There is no CI
workflow and no build step you run yourself: GitHub builds the Jekyll site server-side
whenever you push to `main`, and serves the result at <https://jmparlett.github.io/>.

**To publish a change: edit, commit, push to `main`.** That is the whole deploy process.
Ruby is only needed if you want to preview locally before pushing.

## Local preview (optional)

The system Ruby that ships with macOS (2.6) is too old for the `github-pages` gem, so
this uses a Homebrew Ruby that is kept separate from the system one:

```
brew install ruby@3.3
export PATH="/opt/homebrew/opt/ruby@3.3/bin:$PATH"
gem install bundler -v 2.5.10
bundle config set --local path vendor/bundle
bundle install
bundle exec jekyll serve --livereload
```

Then open <http://localhost:4000>. `vendor/` and `_site/` are gitignored.

In later shells you only need the `export PATH=...` line plus `bundle exec jekyll serve`.

## Layout

| Path | What it is |
| --- | --- |
| `_config.yml` | Site settings. **Not** reloaded by `jekyll serve` — restart after editing. |
| `_pages/` | The actual pages: `index.html` (home), `research.markdown`, `blog.html`, `about.markdown`. Each sets its own `permalink` and `id`. |
| `_layouts/default.html` | Shared shell: nav bar, MathJax, CSS. The nav links are hardcoded here. |
| `_assets/css/` | `index.css` (home page only), `main.css` (everything else), `syntax_highlight.css`. |
| `_data/documents/` | PDFs served directly — CV, posters, slides, handouts. |
| `_data/img/`, `_data/home_data/` | Images. The home page photo is `falls_2026.jpg`; the size in the `<img>` tag in `_pages/index.html` must match the file's real 3:4 dimensions. |
| `_data/publications.yml` | Only feeds the 2023 loop on the research page; newer entries are hardcoded in `research.markdown`. |
| `_posts/` | Blog posts. The blog is currently unlinked from the nav. |

There is no theme (`theme: null`); all styling is hand-written in `_assets/css`.

Note that `include: [_pages,_assets,_data,_includes]` in `_config.yml` is what makes
Jekyll serve the underscore-prefixed directories, which is why PDF links look like
`/_data/documents/....pdf`.

## The CV

The CV on the site is the compiled PDF at `_data/documents/curriculum_vitae.pdf`.

**The LaTeX source is not in this repo** — it lives in Overleaf (`main.tex` plus the
custom `resume.cls`). To update the CV: edit in Overleaf, download the PDF, overwrite
`_data/documents/curriculum_vitae.pdf`, commit, push.

If you have the source locally, it builds with `pdflatex main.tex` (run twice so the
cross-references settle); MacTeX is already installed.
