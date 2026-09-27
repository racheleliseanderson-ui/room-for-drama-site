# Change Log

## 2026-09-27

- Confirmed the live Room for Drama theme and custom plugins already live in `racheleliseanderson-ui/room-for-drama-woocommerce`.
- Confirmed WordPress.com deploys that repository's `main` branch automatically to `/wp-content`.
- Reclassified this repository as the site-control / architecture repository rather than a duplicate deployable codebase.
- Created remediation branch `fix/rfd-layout-consolidation-2026-09-27` in the production code repository.
- Removed two duplicate inline TOC/grid layout injections on that branch.
- Kept `assets/css/structure-toc.css` as the authoritative TOC layout stylesheet.
- Reduced the desktop TOC rail footprint and moved the single-column collapse breakpoint wider to protect article width.

- Simplified the homepage branch to seven major visible bands: hero, problem routes, reinventions, current article, room exploration, Outside Actually, and closing.
- Removed the homepage-only Reading/Pulse, Room Record, six-stage Lab sequence, and Room Cases bands; the underlying systems and dedicated pages remain intact.
- Removed the duplicate final outdoor image and redundant secondary outdoor route.
- Added theme validation workflow to the production-code branch.
- Opened draft PR #28 in `room-for-drama-woocommerce`: `Clean Room for Drama layout and homepage density`.

- PR #28 in `room-for-drama-woocommerce` passed Theme validate and Store Core validation and was squash-merged to `main` as `ad3f446b83835215eec8d635fd9c36ad6a9724d5`.
- Live data cleanup: orphaned WordPress Navigation record #16 was moved to Trash after confirming zero exact references; this removed the retired `/field-kits/` navigation entry.
- Taxonomy verification: zero published posts are missing category, room, or trouble assignments.
- Deployment verification remains open: immediately after the merge, the public rendered homepage still reflected the pre-merge theme and WordPress.com activity showed no deployment event. Treat the GitHub-to-WordPress.com handoff as unverified until the live theme reflects commit `ad3f446b83835215eec8d635fd9c36ad6a9724d5`.
