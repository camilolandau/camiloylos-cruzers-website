# Camilo y los Cruzers Website

Band website for Camilo y los Cruzers, built with [Hugo](https://gohugo.io/) and the [Blowfish](https://blowfish.page/) theme.

**Live site:** https://camiloyloscruzers.com

## Hosting

- **Domain registrar:** Cloudflare (~$10/year)
- **Hosting:** Cloudflare Pages (free)
- **Dashboard:** https://dash.cloudflare.com — go to Compute > Workers & Pages > camiloylos-cruzers-website

## Deploying

The site is **not** auto-deployed from GitHub. To deploy changes:

```bash
# 1. Build the site locally
hugo

# 2. Deploy to Cloudflare Pages
npx wrangler pages deploy public --project-name=camiloylos-cruzers-website
```

You need to be authenticated with wrangler. If prompted, run `npx wrangler login` first.

## Local Development

```bash
# Start the Hugo dev server
hugo server -D
```

Then visit http://localhost:1313

## Project Structure

- `content/` — Page content (markdown)
- `assets/css/custom.css` — Custom styles (background, fonts, forms, gallery)
- `assets/css/schemes/camilo.css` — Custom Blowfish color scheme
- `layouts/shortcodes/` — Custom shortcodes (kit-form, add-to-calendar)
- `layouts/partials/extend-head.html` — Google Fonts loading
- `static/` — Images, icons, PDF onesheet, favicons
- `static/images/bg-animation.svg` — Animated SVG background
- `config/_default/` — Hugo/Blowfish configuration
- `themes/blowfish/` — Blowfish theme (git submodule)

## Key Services

- **Email signup:** Kit (ConvertKit) — form ID 9180311
- **Contact form:** Formspree (needs setup — replace YOUR_FORM_ID in contact.md)
- **Label:** Round Whirled Records — roundwhirledrecords.bandcamp.com
