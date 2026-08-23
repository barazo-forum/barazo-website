<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/singi-labs/.github/main/assets/logo-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/singi-labs/.github/main/assets/logo-light.svg">
  <img alt="Barazo Logo" src="https://raw.githubusercontent.com/singi-labs/.github/main/assets/logo-dark.svg" width="120">
</picture>

# Barazo Website

**Marketing and documentation site for [barazo.forum](https://barazo.forum).**

[![Status: Alpha](https://img.shields.io/badge/status-alpha-orange)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

</div>

---

## Overview

The public-facing site for the Barazo project. Will host marketing pages, comparisons, blog, and user/admin documentation. API reference documentation is served separately by [barazo-api](https://github.com/singi-labs/barazo-api) at its `/docs` endpoint (auto-generated from code).

**Status:** This repository is scaffolded but not yet implemented. It contains repository configuration files (`.gitignore`, PR template, security policy, CLA workflow) but no application code. Implementation is planned for a later phase.

---

## Planned Content

**Marketing pages:**

- Homepage with key benefits and calls to action
- Feature overview
- Comparison pages (vs Discourse, Flarum, Circle, etc.)
- Blog (technical posts, community stories)
- About page

**Documentation (`/docs`):**

- Self-hosting guides
- Admin tutorials
- Plugin development
- AT Protocol concepts (portable identity, cross-forum reputation)
- API integration guides

---

## Planned Tech Stack

| Component | Technology |
|-----------|-----------|
| Framework | Next.js 16, React 19 |
| Styling | TailwindCSS, Radix Colors, Flexoki |
| Typography | Source Sans 3, Source Code Pro (self-hosted via next/font) |
| Icons | Phosphor Icons |
| Content | MDX (blog + docs) |
| Syntax highlighting | Shiki + Flexoki theme |
| SEO | JSON-LD, OpenGraph, sitemaps, SSR |
| Analytics | Umami (self-hosted) |
| Testing | Vitest, vitest-axe, @axe-core/playwright |
| Deployment | Docker or Vercel |

---

## Related Repositories

| Repository | Description | License |
|------------|-------------|---------|
| [barazo-api](https://github.com/singi-labs/barazo-api) | AppView backend (Fastify, firehose, REST API) | AGPL-3.0 |
| [barazo-web](https://github.com/singi-labs/barazo-web) | Forum frontend (Next.js, Tailwind) | MIT |
| [barazo-lexicons](https://github.com/singi-labs/barazo-lexicons) | AT Protocol lexicon schemas + generated types | MIT |
| [barazo-deploy](https://github.com/singi-labs/barazo-deploy) | Docker Compose deployment templates | MIT |

---

## Community

- **Website:** [barazo.forum](https://barazo.forum)
- **Discussions:** [GitHub Discussions](https://github.com/orgs/singi-labs/discussions)
- **Issues:** [Report bugs](https://github.com/singi-labs/barazo-website/issues)

---

## License

**Proprietary** -- All rights reserved.

See [LICENSE](LICENSE) for full terms.

---

Made with ♥ in 🇪🇺 by [Singi Labs](https://singi.dev)
