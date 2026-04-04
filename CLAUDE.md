# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is Logan Schexnaydre's personal academic website, built with the [Academic Pages](https://academicpages.github.io/) Jekyll template and hosted on GitHub Pages.

## Commands

**Run locally (native):**
```bash
bundle install
bundle exec jekyll serve -l -H localhost
```
Site serves at `http://localhost:4000`.

**Run locally (Docker):**
```bash
docker compose up
```

**Restart required** after editing `_config.yml` — live reload does not pick up config changes.

## Site Structure

Content lives in these Jekyll collections and directories:

- `_pages/` — static pages (about, cv, projects, etc.)
- `_portfolio/` — portfolio/project entries
- `_publications/` — publication entries
- `_posts/` — blog posts
- `_talks/` — talk entries
- `_teaching/` — teaching entries
- `files/` — uploaded files (PDFs, etc.), served at `/files/<filename>`
- `images/` — images referenced by pages
- `_data/` — structured data (navigation, etc.)

## Key Config

- **`_config.yml`** — site-wide settings: author info, social links, analytics, collections
- **`_config_docker.yml`** — Docker-specific overrides
- **`_sass/`** — SCSS styles
- **`_includes/`** — reusable Liquid partials (author-profile, head, footer, etc.)
- **`_layouts/`** — page layout templates (single, archive, talk, splash, etc.)

## Content Conventions

Each content file uses YAML front matter. Key fields:
- `layout`: typically `single` (auto-applied via `_config.yml` defaults for most collections)
- `permalink`: controls the URL path
- `author_profile: false` hides the sidebar (used on the projects page for full-width layout)

The CV (`_pages/cv.md`) is hand-authored HTML/Markdown directly in the page — not generated from a data file.
