# Change Log

## 2026-09-27

- Confirmed the live Room for Drama theme and custom plugins already live in `racheleliseanderson-ui/room-for-drama-woocommerce`.
- Confirmed WordPress.com deploys that repository's `main` branch automatically to `/wp-content`.
- Reclassified this repository as the site-control / architecture repository rather than a duplicate deployable codebase.
- Created remediation branch `fix/rfd-layout-consolidation-2026-09-27` in the production code repository.
- Removed two duplicate inline TOC/grid layout injections on that branch.
- Kept `assets/css/structure-toc.css` as the authoritative TOC layout stylesheet.
- Reduced the desktop TOC rail footprint and moved the single-column collapse breakpoint wider to protect article width.
