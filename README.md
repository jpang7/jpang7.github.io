# Jekyll Site

The jekyll stuff is all from cursor.

This is a Jekyll-powered personal site organized into sections (collections):
Apps, Math, and Progress.

## Setup

1. Install Ruby and Bundler (if not already installed)
2. Install dependencies:
   ```bash
   bundle install
   ```

## Running Locally

To preview your site locally:

```bash
bundle exec jekyll serve
```

Then visit `http://localhost:4000` in your browser.

Note: changes to `_config.yml` (e.g. adding a new collection) require
restarting the server — they are not picked up by the live reload.

## Sections

Each section is a Jekyll collection with its own folder and index page:

| Section  | Content folder | Index page      | Layout                 |
|----------|----------------|-----------------|------------------------|
| Apps     | `_apps/`       | `apps.html`     | `_layouts/app.html`    |
| Math     | `_math/`       | `math.html`     | `_layouts/math.html`   |
| Progress | `_progress/`   | `progress.html` | `_layouts/progress.html` |

## Adding a Page to a Section

Create a new Markdown file in the section's folder (e.g. `_math/my-topic.md`).

**Front matter** (the layout is applied automatically per section):

```markdown
---
title: "Your Title"
date: 2026-01-01
---
```

Then write your content in Markdown below the front matter. The page will
automatically appear on that section's index.

## Adding a New Section

1. Register a collection in `_config.yml` (under `collections:`) with
   `output: true` and a `permalink`, plus a `defaults` entry mapping its type
   to a layout.
2. Create the content folder `_<section>/`.
3. Create an index page `<section>.html` (copy an existing one and swap
   `site.<section>`).
4. Create `_layouts/<section>.html` (copy an existing one).
5. Add a nav link in `_layouts/default.html`.

## GitHub Pages

Since this is a `*.github.io` repository, GitHub Pages will automatically build
and deploy your Jekyll site when you push to the `main` (or `master`) branch.
