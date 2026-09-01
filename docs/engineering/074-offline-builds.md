# Offline Builds

## Purpose

Define the offline builds standard for Ghostleaf and its Ghost-to-Eleventy build flow.

## Acceptance criteria

- The offline builds requirement is observable.
- Ghost API failures and static-build behavior are considered.
- Environment and security impact is documented.
- Verification and rollback steps are repeatable.

## Verification

- [ ] Run `yarn lint`.
- [ ] Run `yarn test`.
- [ ] Inspect relevant output in `dist`.
- [ ] Confirm no real credentials are committed.