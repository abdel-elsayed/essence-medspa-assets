# Essence Med Spa Assets

This repository stores public-facing imagery for the Essence Med Spa & Wellness Center web experience. Keeping media in a dedicated repo lets us serve optimized files from a CDN (e.g. jsDelivr) without bloating the application bundle.

## Structure Overview

```
site/
  home/
    hero/
services/
  <service-slug>/
    hero/
    gallery/
    detail/
shared/
  branding/
  textures/
gallery/
  studio-tour/
```

### site/
Global marketing assets reused across multiple pages. The `home/hero/` folder contains the main landing hero artwork.

### services/
Each service slug mirrors the slug defined in `src/data/services.ts` in the app repo. Drop 3–4 curated images per service:

- `hero/` – primary banner image for the service detail page.
- `gallery/` – supporting lifestyle or treatment imagery.
- `detail/` – close-up shots, equipment, or results-focused imagery.

Name files descriptively and consistently, e.g. `01-treatment-room.jpg`, `02-instruments.jpg`. Keep originals ≤ 3000px on the long edge, then export optimized JPG/WebP versions around 1200–1600px for production.

### gallery/
Collections used on the public gallery page. Organize by narrative (e.g. `studio-tour/`) and number sequentially to control display order.

### shared/
Brand elements, staff portraits, repeatable backgrounds, and any assets reused across services.

## CDN Access

Once this repo is public on GitHub, any file can be served via jsDelivr:

```
https://cdn.jsdelivr.net/gh/<org-or-user>/essence-medspa-assets/<path-to-file>
```

Update the Astro project to reference those CDN URLs (or build a helper that maps slugs to paths) after uploading final imagery.

## Workflow Tips

1. Commit high-quality masters to `main` and export web-ready variants alongside them.
2. Automate optimization with `sharp`, `squoosh-cli`, or similar before pushing.
3. Record photographer/prompt credits in the commit message or a `CREDITS.md` file when required.

