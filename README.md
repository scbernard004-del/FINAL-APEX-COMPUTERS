# Apex Computers — Simple GitHub package v2.3.0

This is the simplified GitHub/Vercel build.

## Folder structure
Only five folders are used:
- `api` — order, Gmail notification and catalogue API files
- `media-01`
- `media-02`
- `media-03`
- `media-04`

Everything else required by the storefront is in the project root.

## Latest stock refresh — 25 September 2026
- HP Elite Dragonfly 13.5-inch G3 updated with supplied stock photos, Core i7-1265U, 16GB/32GB DDR5 variants, 256GB SSD, touchscreen, backlit keyboard, fingerprint scanner and Intel Iris Xe graphics. Prices: TSh 1,580,000 / TSh 1,780,000.
- HP ZBook Firefly 16 G9 updated with supplied stock photos, Core i7-1265U, 16GB RAM, 512GB SSD, backlit keyboard and fingerprint scanner. Current supplied price: TSh 1,550,000.
- Existing catalogue records were updated in place so these models are not duplicated.

## Contact
- WhatsApp orders: +255 746 584 214
- Notification Gmail: scbernard004@gmail.com

## Vercel
Framework preset: `Other`
No build command. No output directory.

Gmail SMTP credentials belong only in Vercel Environment Variables. Never commit a Gmail App Password to GitHub.


## v2.2.5 storefront QA update

- Header now uses a robust fixed commerce shell, so it remains visible on desktop, tablet and mobile while the page scrolls.
- The announcement bar collapses after scrolling, while navigation and search stay available.
- HP Pro x360 Fortis 11 G10 refreshed with the latest supplied stock photos and the official 11.6-inch touchscreen specification.
- HP EliteDisplay E273m 27-inch monitor added at TSh 650,000 with supplied stock photos, clean enhanced product media, webcam/speaker details and HDMI/DisplayPort/VGA connectivity.
- Product/media references and simplified GitHub folder limits were rechecked.


## v2.3.0 header QA
- Rebuilt the header breakpoints to prevent the Apex wordmark, navigation, Instagram and language control from overlapping.
- Medium desktops now keep the logo, navigation and controls in one compact row; narrower layouts switch to the menu button.
- The sticky header remains fixed while scrolling, and header-height measurement no longer grows permanently after opening the mobile menu or resizing.
- Cache-busting asset versions were updated so GitHub/Vercel browsers load the new CSS/JS immediately.

### v2.3.0 final cleanup
- Apex header wordmark is now a compact icon + stacked `APEX / COMPUTERS` lockup with no tagline squeezed into navigation.
- The hidden accessibility label for Language/Lugha is correctly screen-reader-only and no longer consumes header space.
- Full navigation uses one compact row down to 1161px and switches to the menu button at 1160px and below, eliminating the large empty header band.
- On phones, the announcement strip is removed to preserve screen space; search and the sticky header remain available.
- Dark/light mode remains available on small phones through the mobile menu.
- Removed unused legacy `app.js`, `shop-simple.css`, and `mobile-polish.css` so future edits cannot accidentally revive obsolete header rules.


## v2.3.0 compact scroll header
- Replaced the heavy black selection/bag button with a clean circular cart button and small item-count badge.
- Added a smooth compact-on-scroll header: announcement and full search fold away, brand/navigation/controls reduce in size, and a search icon appears so search remains one tap away.
- Opening compact search temporarily restores the search bar; opening the mobile menu closes compact search to avoid collisions.
- Respects reduced-motion accessibility settings.


## v2.3.0 header space correction
- Removed the large unused center band visible around 1280px-wide laptop screens.
- From 1161–1360px, logo, navigation and action controls now share one balanced row.
- From 1101–1160px, the site switches to the collision-safe menu layout instead of creating an empty second header row.
- The compact-on-scroll animation and one-tap search remain unchanged.

## v2.3.0 product-identity audit

- Removed the separate HP EliteBook 835 G10 card from the public shop because the supplied stock source grouped 835/845 G10 and no independent exact-unit 835 photo/model record was available.
- Kept HP EliteBook 845 G10 as the source-backed 14-inch Ryzen 5 / 16GB / 256GB listing at the latest supplied TSh 1,100,000 price; exact CPU SKU remains a before-payment confirmation item.
- Kept HP EliteBook 845 G8 with its supplied actual-unit photos, but removed the guessed exact processor from the customer card because the older processor text conflicts with the G8 generation.
- Removed Lenovo IdeaPad D330 from the public shop because the prior mapping from “IdeaPad 300 Detachable” to D330 was an inference rather than a confirmed model code.
- Public catalogue policy: if exact model identity cannot be tied to a supplied photo/model record, hold it from the shop instead of publishing a look-alike.


Update v2.3.0: Added HP EliteBook 840 G6 supplied photos, HP E22 G4 supplied monitor video + stills, and Dell OptiPlex 7020 tower references.


Update v2.3.1:
- Confirmed all recently uploaded product sets are included in the website data.
- Upload-backed products covered: HP Elite Dragonfly G3, HP ZBook Firefly 16 G9, HP Pro x360 Fortis 11 G10, HP EliteDisplay E273m, HP EliteBook 840 G6, HP E22 G4 monitor with video, and Dell OptiPlex 7020.


## v2.4.0 SEO + conversion + performance
- Dynamic `/sitemap.xml` and `/robots.txt` work automatically on the deployed Vercel domain/custom domain.
- Product pages receive dynamic canonical tags, Open Graph/Twitter metadata and Product/Offer structured data through `seo.js`.
- `catalogue-index.html` provides a fast crawlable product index and internal links.
- Homepage/product cards have stronger WhatsApp conversion copy without fake reviews or ratings.
- Product videos use `preload=none`; videos were recompressed and duplicate unused PNG render files were trimmed.
- Run `npm test` before every deployment.

After deployment: submit `https://YOUR-DOMAIN/sitemap.xml` to Google Search Console and Bing Webmaster Tools. For faster Bing/participating-search-engine updates, enable IndexNow in Bing Webmaster Tools.
