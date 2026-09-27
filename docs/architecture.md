# Architecture

## Production WordPress

**Site:** https://dramaroom.blog  
**Active theme:** `room-for-drama-approved-lovable`  
**Production code repository:** `racheleliseanderson-ui/room-for-drama-woocommerce`

The WordPress site should be treated as a deployment target, not the primary code editor.

## Repository responsibilities

### room-for-drama-woocommerce
Deployable WordPress code. Owns the active classic theme, custom plugins, MU plugins, deploy hygiene and the WordPress.com deployment contract.

### room-for-drama
Editorial source, governance, content records, brand authority and publication documentation. It intentionally contains no live site code.

### room-lab
Room Lab application and the Read the Room experience at `lab.dramaroom.blog`.

### exposure-atlas
Outside, Actually at `outsideactually.dramaroom.blog`.

### room-for-drama-site
Operational control map. Records where systems live, how they deploy, what is being remediated and which repository is authoritative.

## Configuration rule

Production constants such as `DISALLOW_FILE_EDIT` are not a reason to bypass source control. GitHub deployment writes to `/wp-content` independently of the WordPress dashboard file editor.

Theme/plugin changes should be made in the canonical GitHub repository, verified on a branch, then merged for deployment.
