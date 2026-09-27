# Deployment

## Existing production path

WordPress.com Hosting → Deployments is connected to:

- Repository: `racheleliseanderson-ui/room-for-drama-woocommerce`
- Branch: `main`
- Destination: `/wp-content`
- Mode: **automatic on push to main**

There is no extra production publish button after merge. A merge to `main` is a production action.

## Safe change sequence

1. Create a feature/fix branch from current `main`.
2. Make the smallest coherent change.
3. Review the diff.
4. Run available checks and inspect affected templates/components.
5. Merge only when the branch is production-ready.
6. Verify the live effect after WordPress.com deployment.

## Do not

- develop directly in the WordPress theme editor;
- maintain a second deployable copy of the active theme;
- put credentials, salts, passwords or environment secrets in Git;
- merge experimental work directly to `main`;
- assume deleting a file from Git removes a previously deployed server file — deployment hygiene must handle server leftovers.

## Current branch

`fix/rfd-layout-consolidation-2026-09-27`

This branch is not live until merged to the production repository's `main` branch.
