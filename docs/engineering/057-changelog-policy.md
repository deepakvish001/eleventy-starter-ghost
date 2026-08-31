# Changelog Policy

## Purpose

Define the changelog policy standard for Ghostleaf so Ghost content is transformed into predictable, accessible, and deployable Eleventy output.

## Current baseline

Ghostleaf uses the Ghost Content API, Eleventy, Nunjucks, Markdown, local-image processing, HTML minification, and Netlify-compatible static output. This guide distinguishes existing behavior from planned work.

## Acceptance criteria

- The changelog policy requirement is observable at build time or in generated output.
- Ghost API failure and missing-content behavior are covered.
- Accessibility, security, and static-hosting impact are considered.
- Environment and credential requirements are explicit.
- Rollback or fallback behavior is documented.

## Verification checklist

- [ ] Run `yarn lint`.
- [ ] Run `yarn test`.
- [ ] Inspect relevant files in `dist`.
- [ ] Check a representative post, page, author, and tag route.
- [ ] Confirm no real credentials or generated secrets are committed.

## Review guidance

Keep implementation work focused on one changelog policy outcome and record unrelated template or content-model changes separately.