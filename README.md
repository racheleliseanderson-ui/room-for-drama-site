# Room for Drama — Site Control

Canonical site: https://dramaroom.blog

This repository is the control and operations map for the Room for Drama production site. It does **not** duplicate the live theme or plugins.

## Source of truth

| Surface | Canonical repository |
| --- | --- |
| dramaroom.blog theme + WordPress custom plugins | `racheleliseanderson-ui/room-for-drama-woocommerce` |
| Editorial source, governance, brand and publication records | `racheleliseanderson-ui/room-for-drama` |
| Room Lab | `racheleliseanderson-ui/room-lab` |
| Outside, Actually / Exposure Atlas | `racheleliseanderson-ui/exposure-atlas` |
| Site-level architecture, deployment map and operational handoff | **this repository** |

## Production deployment

WordPress.com Hosting is already connected to `racheleliseanderson-ui/room-for-drama-woocommerce`, branch `main`, destination `/wp-content`.

A merge/push to `main` deploys automatically to production. Work must therefore happen on a branch and be reviewed before merge.

The production code repository contains:

- `themes/room-for-drama-approved-lovable/`
- `plugins/room-for-drama-core/`
- `plugins/room-for-drama-store-core/`
- `plugins/room-for-drama-tools/`
- shared pinned plugins and MU plugins used by the site

## Important rule

Do not create a second copy of the live theme/plugins in this repository. Two deployable copies would create configuration drift and make rollback ambiguous.

Use this repository to answer: **what controls the site, where does it live, how is it deployed, and what work is currently in flight?**

See:

- `docs/architecture.md`
- `docs/deployment.md`
- `docs/change-log.md`
- `docs/ROOM_FOR_DRAMA_REPOSITORY_PLAN.md`
