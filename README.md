# realseiro.github.io

Personal research blog — <https://realseiro.github.io>

## Write a post

Add a file to `_posts/` named `YYYY-MM-DD-some-title.md`:

```markdown
---
title: "Post title"
subtitle: Optional one-line summary   # shown under the title and on the home page
tags: [rl, alignment]                 # optional
---

Text in Markdown.
```

Commit and push to `master`; the site rebuilds in about a minute.
You can do this straight from the GitHub website (Add file → Create new file).

- **Math**: `$$ ... $$` inline or on its own lines (KaTeX).
- **Code**: fenced blocks with a language, e.g. ```` ```python ````.
- **Images**: put them in `assets/img/` and write `![caption](/assets/img/name.png)`.
- **Draft**: add `published: false` to the front matter.

## Edit the site

- Name, tagline, links: `_config.yml`
- About page: `about.md`
- Look: `assets/css/main.css`

## Preview locally

```sh
bundle install
bundle exec jekyll serve   # http://localhost:4000
```
