# Barazo Website -- Marketing Site

<!-- Auto-generated from barazo-workspace. To propose changes, edit the source:
     https://github.com/barazo-forum/barazo-workspace/tree/main/agents-md -->

MIT | Part of [github.com/barazo-forum](https://github.com/barazo-forum)

Marketing site for Barazo at barazo.forum. Built with Astro. Documentation lives in barazo-docs (docs.barazo.forum).

## What This Repo Does

- Public-facing marketing pages (homepage, features, pricing, comparison pages)
- Blog
- SEO landing pages and conversion funnels
- Redirects /docs/* to docs.barazo.forum

## Website-Specific Standards

- Strict TypeScript -- `strict: true`, no `any`, no `@ts-ignore`
- Accessibility -- WCAG 2.2 AA, semantic HTML
- SEO -- meta tags, OpenGraph, sitemaps, canonical URLs
- Search -- Orama (self-hosted, shared index with docs.barazo.forum)
- Static-first -- Astro islands architecture, zero JS by default

---

## Project-Wide Standards

### About Barazo

Open-source forum software built on the [AT Protocol](https://atproto.com/). Portable identity, member-owned data, no lock-in.

- **Organization:** [github.com/barazo-forum](https://github.com/barazo-forum)
- **License:** AGPL-3.0 (backend) / MIT (frontend, lexicons, deploy, website)
- **Contributing:** See [CONTRIBUTING.md](https://github.com/barazo-forum/.github/blob/main/CONTRIBUTING.md)

### Coding Standards

1. **Test-Driven Development** -- write tests before implementation (Vitest).
2. **Strict TypeScript** -- `strict: true`, no `any`, no `@ts-ignore`.
3. **Conventional commits** -- `type(scope): description`.
4. **CI must pass** -- lint, typecheck, tests, security scan on every PR.
5. **Input validation** -- Zod schemas on all API inputs and firehose records.
6. **Output sanitization** -- DOMPurify on all user-generated content.
7. **No raw SQL** -- Drizzle ORM with parameterized queries only.
8. **Structured logging** -- Pino logger, never `console.log`.

### Git Workflow

All changes go through Pull Requests -- never commit directly to `main`. Branch naming: `type/short-description` (e.g., `feat/add-reactions`, `fix/xss-sanitization`).

### AT Protocol Context

- Users own their data (stored on their Personal Data Server)
- The AppView (barazo-api) indexes data from the AT Protocol firehose
- Lexicons (`forum.barazo.*`) define the data schema contract
- Identity is portable via DIDs -- no vendor lock-in
- All record types are validated against lexicon schemas
