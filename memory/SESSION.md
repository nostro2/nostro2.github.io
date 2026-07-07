---
last_updated: 2026-07-07 15:10
status: active
---

# Session — nostro2.github.io

## Current Focus

ATS-safe resume: site is the resume source; PDF made via header download button (`window.print()`).

## Exact Stop Point

ATS fixes done + personal details moved to gitignored `.env`; public site stays "Dan R." with no email, so pushing is now safe. NOT yet committed/pushed.

## What Was Just Done

- Diagnosed old resume PDF ATS failure (Firefox print: left column missing from text layer, fi/digit ligatures → �, no contact info).
- Fixed `_config.yml`, `_includes/header.html`, `assets/main.scss` (see CHANGELOG).
- Verified with headless Chromium print + pdftotext: clean single-column text layer, 0 corrupted glyphs.
- Verified PDF copied to `~/Downloads/Daniel Robertson - Cloud Solutions Consultant.pdf`.

## Next Action

Commit + push when user asks (public build verified anonymous). Detailed CV PDF: run `bin/build-cv` (needs `.env` with CV_FULL_NAME/CV_EMAIL). Site download button = anonymous version; print via Chrome, not Firefox.

## Working Context

- Theme `sproogen/resume-theme` (remote). `.layout` is flex-row; print single-column needs `flex-direction: column`, width overrides alone don't work.
- Theme loads Roboto with `font-feature-settings: "kern","liga","pnum"` — cause of ligature corruption; print CSS forces Arial + ligatures off.
- Certs expired (DevOps Pro Oct 2023, SA Assoc Dec 2020) — summary reworded to "AWS DevOps specialist"; user may want to recertify.

## Carry-over to Other Files

None.
