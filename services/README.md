# Service Asset Conventions

Each folder is named after the `slug` defined in the application’s `services.ts` data file. Add imagery as follows:

- `hero/` – 1 landscape image (~1600×900) that can serve as the top banner for the service page.
- `gallery/` – 2–3 lifestyle or in-treatment images to illustrate the guest experience.
- `detail/` – Close-ups, product shots, or results imagery to support the copy.

Recommended basenames:

```
hero/
  01-hero.jpg
  01-hero@2x.jpg
gallery/
  01-experience.jpg
  02-experience.jpg
  03-experience.jpg
detail/
  01-detail.jpg
```

Feel free to include both `.jpg` and `.webp` variants. Keep filenames lowercase, hyphenated, and descriptive for SEO. Update the web project to point to the CDN URL that mirrors this path structure.
