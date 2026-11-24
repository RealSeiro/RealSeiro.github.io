# realseiro.github.io

Personal site and blog — <https://realseiro.github.io>

Everything is plain Markdown. Push to `master` and the site rebuilds in about a minute.
You can do all of this from the GitHub website (Add file → Create new file).

## Add a project

Create `_projects/your-project.md`:

```markdown
---
title: "Project name"
description: One sentence on what it is.         # shown on the cards
date: 2026-12-15                                 # used for sorting (newest first)
period: Dec 2026                                 # shown as written, e.g. "Oct – Dec 2026"
role: Solo project                               # or "Team lead", "Backend lead", ...
status: In progress                              # optional; "In progress" adds a badge
featured: true                                   # optional; shows it on the home page
stack: [Python, PyTorch]
tags: [reinforcement learning]
links:
  - name: GitHub
    url: https://github.com/RealSeiro/...
---

## Overview
...
```

## Write a post

Copy `_drafts/example-post.md` into `_posts/` as `YYYY-MM-DD-some-title.md`.
That file shows everything a post can contain.

- **Table of contents**: built automatically from `##` and `###` headings.
- **Math**: `$$ ... $$`, inline or on its own lines (KaTeX).
- **Code**: fenced blocks with a language, e.g. ```` ```python ````.
- **Images**: put them in `assets/img/` and write `![caption](/assets/img/name.png)`.
- **Drafts**: files in `_drafts/` are never published.

## Edit the site

- Name, email, LinkedIn, Scholar links: `_config.yml`
- Home page intro: `index.html`
- About page: `about.md`
- Look: `assets/css/main.css`

## Preview locally

```sh
bundle install
bundle exec jekyll serve --drafts   # http://localhost:4000
```
