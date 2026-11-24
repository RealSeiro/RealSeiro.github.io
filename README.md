# realseiro.github.io

Personal site and blog — <https://realseiro.github.io>

This folder is also an **Obsidian vault**: open it in Obsidian and write. Settings come preconfigured.

## Write a post

1. **Ctrl+N** — a new note opens in `_writing/`. Name it with the post's title.
2. The Templater plugin fills in the properties automatically (title, description, date, tags, published).
3. Write. Paste images with Ctrl+V; they're saved to `assets/img/` and work on the site.
4. Check **published** when it's ready. Unchecked posts stay private.
5. Click **Commit-and-sync** (Obsidian Git, left sidebar). The site updates in about a minute.

`_writing/How to Write a Post.md` shows everything a post can contain (math, code, tables, images).

## Add a project

Right-click `_projects` → **New note** and name it. The project properties fill in automatically.

| Property | Meaning |
|---|---|
| `description` | One sentence, shown on the cards |
| `date` | Used for sorting (newest first) |
| `period` | Shown as written, e.g. `Oct – Dec 2026` |
| `role` | e.g. `Solo project`, `Backend lead` |
| `status` | `In progress` adds a badge |
| `featured` | Checked → shown on the home page |
| `stack`, `tags` | Lists |
| `links` | Edit in source mode: `- name: GitHub` / `url: https://...` |

## Writing features

- **Table of contents**: built from `##` and `###` headings.
- **Math**: `$$ ... $$`, inline or on its own lines.
- **Code**: fenced blocks with a language, e.g. ```` ```python ````.

## Edit the site

- Name, email, LinkedIn, Scholar: `_config.yml`
- Home page intro: `index.html`
- About page: `about.md`
- Look: `assets/css/main.css`

## Preview locally (optional)

```sh
bundle install
bundle exec jekyll serve   # http://localhost:4000
```
