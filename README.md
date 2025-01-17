# Developer Blog

A static, client-first blog built with Astro focusing on software development content.

## Architecture

### Core Principles
- Static site generation with Astro
- Client-side only functionality
- MDX-based content management
- Local search capabilities
- Automated cross-posting via GitHub Actions

### Technical Stack
- **Framework**: Astro
- **Content**: MDX files
- **Search**: Pagefind (client-side search index)
- **Deployment**: Vercel/Netlify
- **Cross-posting**: GitHub Actions

## Project Structure
```bash
blog
├── src/
│   ├── content/
│   │   └── posts/
│   │       ├── prompt-driven-development/
│   │       │   ├── index.mdx
│   │       │   └── images/
│   │       │       ├── definition.png
│   │       │       └── process.png
│   ├── components/
│   │   ├── PostCard.astro
│   │   ├── Search.astro
│   │   └── PostLayout.astro
│   ├── layouts/
│   │   └── BaseLayout.astro
│   ├── pages/
│   │   ├── index.astro
│   │   ├── posts/[...slug].astro
│   │   └── tags/[tag].astro
│   └── utils/
│       ├── search.ts
│       └── crossPost.ts
├── public/
│   ├── favicon.ico
│   └── robots.txt
├── scripts/
│   └── generate-search-index.ts
├── .github/
│   └── workflows/
│       ├── build.yml
│       └── cross-post.yml
├── astro.config.mjs
├── package.json
└── tsconfig.json
```

## Frontmatter schema


2. **Frontmatter Schema** (based on your content):

```yaml
---
title: Prompt-driven Development
date: 2024-03-20
tags: ['ai', 'development', 'methodology']
crossPost:
  linkedin: true
  dev: false
excerpt: >
  Software-Entwicklung wird aufgrund von KI nie mehr sein wie vor noch einem Jahr.
  Prompt-driven Development ist die aktuellste Umwälzung...
images:
  hero: ./images/hero.png
---
```