<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/barazo-forum/.github/main/assets/logo-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/barazo-forum/.github/main/assets/logo-light.svg">
  <img alt="Barazo Logo" src="https://raw.githubusercontent.com/barazo-forum/.github/main/assets/logo-dark.svg" width="120">
</picture>

# barazo-website

**Marketing + documentation site for Barazo**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Next.js](https://img.shields.io/badge/Next.js-16-black)](https://nextjs.org/)

</div>

---

## 🚧 Status: Planned (Q2 2026)

The marketing and documentation website at barazo.forum.

**Current phase:** Repository will be created in Phase 1

---

## What is this?

The barazo-website hosts:

**Marketing pages (`/`):**
- Homepage - Hero, key benefits, CTAs
- Features - What Barazo does
- Pricing - Managed hosting tiers
- Comparisons - vs Discourse, Flarum, Circle, etc.
- Blog - Technical posts, community stories
- About - Who, why, open source commitment

**Documentation (`/docs`):**
- Self-hosting guides
- Admin tutorials
- Plugin development
- Concepts (portable identity, cross-forum reputation)
- API integration guides

**Note:** API reference docs are served separately by barazo-api at `/docs` (auto-generated from code).

---

## Tech Stack

| Component | Technology |
|-----------|-----------|
| Framework | Next.js 16, React 19 |
| Styling | TailwindCSS, Radix Colors, Flexoki |
| Content | MDX (blog + docs) |
| SEO | JSON-LD, OpenGraph, sitemaps |
| Analytics | Plausible (privacy-focused, optional) |
| Deployment | Vercel or self-hosted |

---

## Pages Structure

```
/                    Homepage
/features            Feature overview
/pricing             Managed hosting tiers
/vs/discourse        Comparison pages
/vs/flarum
/vs/circle
/blog                Blog listing
/blog/[slug]         Blog posts (MDX)
/docs                Documentation home
/docs/[...slug]      Documentation pages (MDX)
/about               About Barazo
```

---

## Development

**Prerequisites:**
- Node.js 24 LTS
- pnpm

**Setup:**
```bash
git clone https://github.com/barazo-forum/barazo-website.git
cd barazo-website
pnpm install
```

**Run development server:**
```bash
pnpm dev
```

**Run tests:**
```bash
pnpm test
pnpm lint
pnpm typecheck
```

---

## Content

**Blog posts:** `content/blog/*.mdx`
**Documentation:** `content/docs/**/*.mdx`

Both support:
- Frontmatter metadata
- MDX components
- Syntax highlighting (Shiki + Flexoki)
- Table of contents

---

## SEO

**Requirements:**
- Server-side rendering (SSR)
- JSON-LD structured data
- OpenGraph + Twitter Cards
- Sitemap generation
- robots.txt
- Fast page loads (Lighthouse > 90)

---

## Deployment

**Production:** Deployed to barazo.forum

**Method:**
- Vercel (recommended) - auto-deploy on push to `main`
- Or self-hosted via Docker

---

## License

**MIT** - Marketing and docs should be freely usable.

---

## Related Repositories

- **[barazo-api](https://github.com/barazo-forum/barazo-api)** - API reference docs (served at /docs)
- **[Organization](https://github.com/barazo-forum)** - All repos

---

## Community

- 🌐 **Website:** [barazo.forum](https://barazo.forum)
- 💬 **Discussions:** [GitHub Discussions](https://github.com/orgs/barazo-forum/discussions)
- 🐛 **Issues:** [Report bugs](https://github.com/barazo-forum/barazo-website/issues)

---

© 2026 Barazo. Licensed under MIT.
