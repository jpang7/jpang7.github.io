# Jekyll Blog

The jekyll stuff is all from cursor.

This is a Jekyll-powered blog site that supports Markdown blog posts.

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

## Writing Blog Posts

Create new blog posts as Markdown files in the `_posts/` directory.

**File naming format**: `YYYY-MM-DD-post-title.md`

**Front matter** (required at the top of each post):

```markdown
---
layout: post
title: "Your Post Title"
date: 2025-01-01
---
```

Then write your content in Markdown below the front matter.

## Example

To create a new post for January 2, 2025:

1. Create `_posts/2025-01-02-my-new-post.md`
2. Add the front matter and content:

   ```markdown
   ---
   layout: post
   title: "My New Post"
   date: 2025-01-02
   ---

   This is my blog post content written in **Markdown**!
   ```

3. The post will automatically appear on your blog page.

## GitHub Pages

Since this is a `*.github.io` repository, GitHub Pages will automatically build
and deploy your Jekyll site when you push to the `main` (or `master`) branch.
