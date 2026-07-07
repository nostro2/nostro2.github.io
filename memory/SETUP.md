---
last_updated: 2026-07-07
---

# Setup — nostro2.github.io

## Prerequisites

- Ruby + Bundler
- Chromium + python3 (for `bin/build-cv` PDF generation)
- `.env` in repo root (gitignored): `CV_FULL_NAME`, `CV_EMAIL` — personal details for detailed CV builds; public site stays anonymous

## Install

```bash
bundle install
```

## Dev Commands

| Command | What it does |
|---------|--------------|
| `bundle exec jekyll serve` | Start local dev server |
| `bundle exec jekyll build` | Build anonymous public site to _site/ |
| `bin/build-cv [out.pdf]` | Build detailed CV PDF (full name + email from .env) to ~/Downloads |

## Notes

- Push to main/master triggers GitHub Pages auto-build.
