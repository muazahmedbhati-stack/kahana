# Khan Restaurant website

A responsive, dependency-free static website designed specifically for Khan's printed-menu identity: oversized condensed lettering, Urdu typography, a mustard masthead, original menu photography, numbered cuisine links, and a typographic delivery section. Includes scroll reveals, subtle food-image motion, a reading-progress line, category filters, cross-category English/Urdu search, an accessible original-menu dialog, call links, and a map search embed.

## Deploy to Vercel

1. Extract the ZIP and upload this folder's contents to a GitHub repository. Keep `index.html` at the repository root.
2. In Vercel, choose **Add New → Project**, then import that repository.
3. The included `vercel.json` explicitly selects **Other**, runs `node build.cjs`, and serves the **public** output directory. No environment variables or dependencies are needed.
4. Click **Deploy**. The build copies only browser files into `public/`; the local preview server is not deployed.

If replacing an earlier failed deployment, replace the repository files with this version, ensure Vercel's Root Directory points to the folder containing `vercel.json`, then redeploy the new commit with the build cache disabled. If editing dashboard settings manually, use Framework **Other**, Build Command **node build.cjs**, and Output Directory **public**.

Alternatively, with the Vercel CLI installed, run `vercel` from this directory and follow its prompts; run `vercel --prod` for production.

## Preview locally

With Node.js installed, run `npm run dev`, then visit http://127.0.0.1:4173. Run `npm run check` to check JavaScript syntax.

## Edit content

- `app.js`: menu categories, English/Urdu names, and prices. Handi prices are half/full. Unclear printed items are omitted; the full original remains available.
- `index.html`: phone numbers, address, copy, map query, and structured data.
- `style.css`: design, responsive breakpoints, motion, and original-menu image viewport.
- `assets/menu.jpg`: original provided menu. The logo is extracted visually through an SVG viewport using this original image, preserving its artwork.

## Content notes before launch

The supplied menu is undated. Confirm current prices, the printed 5% dine-in service charge, and the four contact numbers. BBQ pricing was not provided, so the site offers a call enquiry. No opening hours, booking service, or online ordering are invented.

The Google Maps URL is a search using the supplied Plus Code and restaurant name, not a verified place-ID pin. Replace both the map iframe and directions link with the restaurant's exact shared Maps link when available.

All restaurant imagery and the logo now use the supplied menu; no stock food photography is used. The original image is low resolution, so a high-resolution logo and restaurant photos would improve sharpness. Google Fonts and Google Maps need internet access; local font fallbacks are present. For a fully self-hosted version, add local font files. The website has not been deployed to Vercel by this chat.
