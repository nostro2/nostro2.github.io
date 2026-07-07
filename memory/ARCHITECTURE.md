---
last_updated: 2026-05-20
---

# Architecture — nostro2.github.io

## Overview

Personal Jekyll site hosted on GitHub Pages. Custom layouts and includes. Content in Markdown. Bundle manages gem dependencies.

## Stack

| Layer | Technology | Notes |
|-------|------------|-------|
| Framework | Jekyll | Ruby/Bundler |
| Hosting | GitHub Pages | Auto-builds on push |

## Structure

```
nostro2.github.io/
├── _config.yml     — site config
├── _layouts/       — page templates
├── _includes/      — partials (header.html etc.)
├── index.md        — homepage
├── assets/         — CSS, JS
├── images/         — image assets (favicon etc.)
├── Gemfile
└── vendor/bundle/  — bundled gems (not committed)
```
