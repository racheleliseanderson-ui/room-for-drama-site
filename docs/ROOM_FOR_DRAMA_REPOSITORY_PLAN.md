# Room for Drama Repository Plan

## Decision

Do **not** duplicate the production theme and plugins into this repository.

A forensic check on 2026-09-27 confirmed that the live code already has a canonical private source repository:

`racheleliseanderson-ui/room-for-drama-woocommerce`

That repository contains the active classic theme `room-for-drama-approved-lovable` and the Room for Drama custom WordPress plugins, and WordPress.com already deploys its `main` branch automatically to `/wp-content`.

Creating a second deployable copy here would introduce two sources of truth.

## Role of this repository

`room-for-drama-site` is the site-control repository. It owns:

- architecture and repository mapping;
- production deployment documentation;
- current remediation / migration status;
- cross-repository handoff notes;
- change log and operational decisions.

It does not own deployable WordPress code.

## Canonical repository map

- Publication governance and editorial source: `racheleliseanderson-ui/room-for-drama`
- Production WordPress theme/plugins: `racheleliseanderson-ui/room-for-drama-woocommerce`
- Room Lab: `racheleliseanderson-ui/room-lab`
- Outside, Actually / Exposure Atlas: `racheleliseanderson-ui/exposure-atlas`
- Site-level control map: `racheleliseanderson-ui/room-for-drama-site`

## Production workflow

```
feature/fix branch
      |
      v
review + verification
      |
      v
merge to room-for-drama-woocommerce/main
      |
      v
WordPress.com GitHub Deployment
      |
      v
/wp-content
      |
      v
dramaroom.blog
```

Production deployment is automatic after a push to `main`. Do not merge unfinished code.

## Current remediation branch

`fix/rfd-layout-consolidation-2026-09-27`

Initial scope:

1. remove duplicate TOC/grid CSS injection from `template-parts/head.php`;
2. remove the duplicate late inline TOC/grid injection from `inc/structure-toc.php`;
3. leave `assets/css/structure-toc.css` as the authority;
4. reduce the desktop rail width and gap;
5. collapse the rail at a wider breakpoint so medium-width layouts do not squeeze article content;
6. continue homepage duplication and visual-density cleanup after layout consolidation is verified.
