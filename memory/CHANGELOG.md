---
last_updated: 2026-07-07
---

# Changelog — nostro2.github.io

## [Unreleased] (local, not yet committed/pushed)

- Skills/experience additions from `resume/memory/` audit (2026-07-07):
  - Skills line: added Docker, Bash, EKS (Docker was flagged strongest area in [[user_skills]] yet absent from site).
  - Matrixx section: three new bullets — Docker image/build-pipeline ownership for C++/Java services, EKS build cluster CloudWatch dashboard (queue depth/CPU/memory/disk/network → instance right-sizing), customer-facing Helm chart delivery. Sourced from `resume/memory/interview_matrixx.md`.
- Second round from user input (2026-07-07, Dan OK'd diluting AWS focus):
  - Skills line: added Ansible, Docker Compose, TypeScript, Cloudflare Workers, LLM Infrastructure (EKS, Ollama, RAG); "Infrastructure Monitoring" → "Observability & Monitoring".
  - Matrixx: new bullet — EKS cluster running self-hosted LLMs for dev team RAG pipeline.
  - New facts persisted to `resume/memory/user_skills.md` and `interview_matrixx.md`.
- Third round (2026-07-07): Ansible confirmed at EveryCity + KCOM — bullet added to each; Matrixx RAG bullet expanded (Ollama, Lambda-driven GPU node scaling, cold-start vs pre-warm tradeoff). Resume memory updated to match.
- Summary rewritten (2026-07-07): now covers CI/CD platform ownership, Jenkins on EKS, Docker pipelines, cost optimisation, LLM infra, one-week MVP. Interests gained home-lab sentence (local LLM stack, Docker Compose, monitoring).

## c5edd77 (committed 2026-07-07)

- ATS overhaul of resume print output (2026-07-07):
  - `_config.yml`: name → Daniel Robertson (full name), email set, "About Me" → "Summary", cert claim in summary reworded (certs expired), new Skills keyword section, Snippets section removed and GIS contract folded into Experience as "April 2026 - Present", cert captions now "(expired …)", "A Little More About Me" → "Interests".
  - `_includes/header.html`: print-only text contact block (LinkedIn/GitHub URLs).
  - `assets/main.scss`: `@media print` block — Arial system font + ligatures disabled (fixes � glyph corruption in extracted text layer), single-column via `.layout { flex-direction: column }`, black-on-white print colors, cert tiles flattened.
- Verified: headless Chromium print → `pdftotext` extracts name, contact, all employers/titles/dates, 0 corrupted glyphs. Old Firefox-printed PDF had missing left column + � glyphs.
- Personal details split out of public site (2026-07-07): `_config.yml` back to "Dan R." / no email; full name + aliased email live in gitignored `.env` (`CV_FULL_NAME`, `CV_EMAIL`); new `bin/build-cv` script overlays them via temp `_config.local.yml`, prints detailed PDF via headless Chromium, then restores anonymous `_site`. Added `.gitignore`.

## 2026-05-20

- Bootstrapped memory files
