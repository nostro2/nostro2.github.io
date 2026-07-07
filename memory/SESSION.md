---
last_updated: 2026-07-07 16:15
status: active
---

# Session — nostro2.github.io

## Current Focus

ATS-safe resume: site is the resume source; PDF made via header download button (`window.print()`).

## Exact Stop Point

Committed (c5edd77, rebased onto remote "full-time" wording edit) and pushed; live site verified anonymous ("Dan R.", 0 personal-info hits) on 2026-07-07.

## What Was Just Done

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
