---
last_updated: 2026-07-07
---

# Changelog — nostro2.github.io

## [Unreleased] (local, not yet committed/pushed)

- ATS overhaul of resume print output (2026-07-07):
  - `_config.yml`: name → Daniel Robertson (full name), email set, "About Me" → "Summary", cert claim in summary reworded (certs expired), new Skills keyword section, Snippets section removed and GIS contract folded into Experience as "April 2026 - Present", cert captions now "(expired …)", "A Little More About Me" → "Interests".
  - `_includes/header.html`: print-only text contact block (LinkedIn/GitHub URLs).
  - `assets/main.scss`: `@media print` block — Arial system font + ligatures disabled (fixes � glyph corruption in extracted text layer), single-column via `.layout { flex-direction: column }`, black-on-white print colors, cert tiles flattened.
- Verified: headless Chromium print → `pdftotext` extracts name, contact, all employers/titles/dates, 0 corrupted glyphs. Old Firefox-printed PDF had missing left column + � glyphs.
- Personal details split out of public site (2026-07-07): `_config.yml` back to "Dan R." / no email; full name + aliased email live in gitignored `.env` (`CV_FULL_NAME`, `CV_EMAIL`); new `bin/build-cv` script overlays them via temp `_config.local.yml`, prints detailed PDF via headless Chromium, then restores anonymous `_site`. Added `.gitignore`.

## 2026-05-20

- Bootstrapped memory files
