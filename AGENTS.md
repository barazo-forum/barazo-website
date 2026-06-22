# Barazo Website -- Marketing Site

<!-- Auto-generated from barazo-workspace. To propose changes, edit the source:
     https://github.com/singi-labs/barazo-workspace/tree/main/agents-md -->

MIT | Part of [github.com/singi-labs](https://github.com/singi-labs)

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

- **Organization:** [github.com/singi-labs](https://github.com/singi-labs)
- **License:** AGPL-3.0 (backend) / MIT (frontend, lexicons, deploy) / CC BY-SA 4.0 + MIT (docs) / Proprietary (website)
- **Contributing:** See [CONTRIBUTING.md](https://github.com/singi-labs/.github/blob/main/CONTRIBUTING.md)

### Coding Standards

1. **Test-Driven Development** -- write tests before implementation (Vitest).
2. **Strict TypeScript** -- `strict: true`, no `any`, no `@ts-ignore`.
3. **Conventional commits** -- `type(scope): description`.
4. **CI must pass** -- lint, typecheck, tests, security scan on every PR.
5. **Input validation** -- Zod schemas on all API inputs and firehose records.
6. **Output sanitization** -- DOMPurify on all user-generated content.
7. **No raw SQL** -- Drizzle ORM with parameterized queries only.
8. **Structured logging** -- Pino logger, never `console.log`.

### Before Starting Any Issue

**Always check for existing work before implementing anything:**

1. Search for open PRs that may already address the issue: `gh pr list --repo singi-labs/barazo-website --state open`
2. Search for related branches: `gh api repos/singi-labs/barazo-website/branches --paginate`
3. Scan the codebase for partial implementations of the feature
4. Check closed PRs for previously attempted work

The GitHub board may lag behind actual implementation state. Partial or complete implementations may exist without being reflected in issue status. Never duplicate work -- always verify first.

### Git Workflow

All changes go through Pull Requests -- never commit directly to `main`. Branch naming: `type/short-description` (e.g., `feat/add-reactions`, `fix/xss-sanitization`).

**Use git worktrees for all feature work.** Each branch must get its own working directory. This prevents multiple agents from stepping on each other's files and allows parallel work without stashing.

```bash
# Create a worktree for your branch
git worktree add /tmp/barazo-website-<branch-name> -b <branch-name> origin/main

# Work in the worktree
cd /tmp/barazo-website-<branch-name>

# When done, remove the worktree
git worktree remove /tmp/barazo-website-<branch-name>
```

Never work directly in the main checkout (`/singi-labs/repos/barazo-website/`). Always create a worktree per issue. Clean up the worktree after the PR is merged.

### AT Protocol Context

- Users own their data (stored on their Personal Data Server)
- The AppView (barazo-api) indexes data from the AT Protocol firehose
- Lexicons (`forum.barazo.*`) define the data schema contract
- Identity is portable via DIDs -- no vendor lock-in
- All record types are validated against lexicon schemas
