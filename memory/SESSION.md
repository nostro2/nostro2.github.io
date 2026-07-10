---
last_updated: 2026-07-10
status: active
---

# Session — nostro2.github.io

## Current Focus

ATS-safe resume: site is the resume source; PDF made via header download button (`window.print()`).

## Exact Stop Point

Committed and pushed b3104a8 (Projects section, below Experience) after c67cf92 (skills/experience/summary expansion); config grep for personal info = 0 hits before each push. GitHub Pages rebuilding.

## What Was Just Done

- Skills section reformatted: comma list → backtick-wrapped items (same pill style as Education modules). YAML validated, uncommitted.
- Trading bot project: new bullet, runs unattended on Hetzner cloud server (chosen over AWS for cost + multi-provider breadth). Uncommitted.
- Purged all em dashes from _config.yml (user rule: no em dashes anywhere on resume; see also commit 3291e8e "remove dashes"). Lines 164/165 split to sentences, line 225 to colon. Grep = 0 hits.
- Audited `resume/memory/` (user_skills.md, interview_matrixx.md) for content missing from site.
- `_config.yml` (uncommitted): Skills line gained Docker, Bash, EKS, then Ansible, Docker Compose, TypeScript, Cloudflare Workers, Observability, LLM Infrastructure; Matrixx gained four bullets (Docker image ownership, EKS CloudWatch build dashboard, customer Helm delivery, EKS LLM/RAG cluster). YAML validated.
- New user facts saved to resume memory: Ansible (EveryCity + KCOM, bullets added to both), Matrixx EKS LLM/RAG cluster (Ollama, Lambda-scaled GPU nodes, pre-warm tradeoff — expanded bullet + interview story).
- Skipped deliberately: Maven/Java (flagged weak in resume memory — don't advertise), wifi-pentest/network-gremlin projects.

## Next Action

User to review new Skills/Matrixx wording, then commit + push. Detailed CV PDF: run `bin/build-cv` (needs `.env` with CV_FULL_NAME/CV_EMAIL). Site download button = anonymous version; print via Chrome, not Firefox.

## Working Context

- Theme `sproogen/resume-theme` (remote). `.layout` is flex-row; print single-column needs `flex-direction: column`, width overrides alone don't work.
- Theme loads Roboto with `font-feature-settings: "kern","liga","pnum"` — cause of ligature corruption; print CSS forces Arial + ligatures off.
- Certs expired (DevOps Pro Oct 2023, SA Assoc Dec 2020) — summary reworded to "AWS DevOps specialist"; user may want to recertify.

## Carry-over to Other Files

None.
