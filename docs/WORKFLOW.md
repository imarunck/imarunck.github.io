# Blog Workflow (Chirpy + GitHub Pages)

This document describes the workflow for maintaining `blog.arunck.com`.

## Stack

* GitHub Pages
* Jekyll
* Chirpy Starter
* Ruby 3.1.x
* Bundler
* Git

---

# First-Time Setup (New Machine)

Clone the repository:

```bash
git clone https://github.com/imarunck/imarunck.github.io.git
cd imarunck.github.io
```

Verify Ruby:

```bash
ruby -v
```

Expected:

```text
ruby 3.1.x
```

Install dependencies:

```bash
bundle install
```

Run locally:

```bash
bundle exec jekyll serve
```

Open:

```text
http://127.0.0.1:4000
```

---

# Creating a New Post

Create a file inside `_posts`.

Example:

```text
_posts/English/2026/2026-02-20-my-post.md
```

Example front matter:

```yaml
---
title: My Post
date: 2026-02-20 10:00:00 +0530
categories: [Blog]
tags: [thoughts]
author: arun
---
```

Author information is defined in:

```text
_data/authors.yml
```

---

# Local Testing

Always test before publishing:

```bash
bundle exec jekyll serve
```

Open:

```text
http://127.0.0.1:4000
```

Verify:

* Posts render correctly
* Images load correctly
* Links work
* No build errors

---

# Publish Changes

Commit and push:

```bash
git add .
git commit -m "Add new post"
git push
```

GitHub Pages will deploy automatically.

---

# Daily Workflow

Normal content updates:

```bash
git add .
git commit -m "Update content"
git push
```

---

# Chirpy Theme Updates

Check current remotes:

```bash
git remote -v
```

Expected:

```text
origin   https://github.com/imarunck/imarunck.github.io.git
upstream https://github.com/cotes2020/chirpy-starter.git
```

Fetch latest Chirpy updates:

```bash
git fetch upstream
git merge upstream/main
bundle install
```

If conflicts occur:

1. Resolve conflicts manually
2. Test locally

Then:

```bash
git add .
git commit -m "Merge upstream Chirpy updates"
git push
```

---

# Custom Domain

Domain:

```text
blog.arunck.com
```

Repository must contain:

```text
CNAME
```

Contents:

```text
blog.arunck.com
```

---

# Useful Commands

Run local server:

```bash
bundle exec jekyll serve
```

Clean build:

```bash
bundle exec jekyll clean
```

Install dependencies:

```bash
bundle install
```

Check remotes:

```bash
git remote -v
```

Check branch status:

```bash
git branch -vv
```

---

# Notes

* Use Ruby 3.1.x.
* Do not upgrade to Ruby 4.x until Chirpy officially supports it.
* Always test locally before pushing.
* Pull Chirpy updates from `upstream`.
* Push website changes to `origin`.
