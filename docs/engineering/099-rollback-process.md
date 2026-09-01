# Rollback Process

## Purpose

Define the rollback process standard for Ghostleaf so Ghost content is transformed into predictable, accessible, and deployable Eleventy output.

## Current baseline

Ghostleaf uses the Ghost Content API, Eleventy, Nunjucks, Markdown, local-image processing, HTML minification, and Netlify-compatible static output.

## Acceptance criteria

- The rollback process requirement is observable at build time or in generated output.
- Ghost API failure and missing-content behavior are covered.
- Accessibility, security, and static-hosting impact are considered.
- Environment and credential requirements are explicit.
- Rollback or fallback behavior is documented.

## Verification checklist

- [ ] Run `yarn lint`.
- [ ] Run `yarn test`.
- [ ] Inspect relevant files in `dist`.
- [ ] Check a representative post, page, author, and tag route.
- [ ] Confirm no real credentials are committed.