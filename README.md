# Aayush Shah — Portfolio

Personal portfolio + writing. Built with [Astro](https://astro.build), deployed on Cloudflare Pages.

## Develop

```bash
npm install
npm run dev        # local preview at http://localhost:4321
```

## Build

```bash
npm run build      # outputs static site to ./dist
npm run preview    # preview the production build
```

## Adding a blog post

Drop a Markdown file in `src/content/blog/`. Frontmatter:

```yaml
---
title: "Post title"
description: "One-line summary."
date: 2026-06-13
draft: false   # optional; true hides it from the list
---
```

## Deploy (Cloudflare Pages)

Connect this GitHub repo in the Cloudflare dashboard:

- **Framework preset:** Astro
- **Build command:** `npm run build`
- **Output directory:** `dist`

Every push to `main` auto-builds and deploys. A custom domain can be attached
later under Pages → Custom domains (no rebuild needed).

## Structure

```
src/
  layouts/Base.astro        shared shell (head, nav, footer, scroll-reveal)
  pages/index.astro         homepage
  pages/blog/               blog list + post template
  content/blog/             Markdown posts
  styles/global.css         the whole design system
public/                     static assets (favicon, future resume.pdf)
```
