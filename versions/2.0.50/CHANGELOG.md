# Titanworks Bazna Cijena 2.0.50

* Theme Compatibility: templates now use semantic HTML5 root <span> elements with display: block instead of <div>, preventing browser DOM splitting inside <p class="price"> and <span class="price"> wrappers.
* Variations: added MutationObserver and variation handler in frontend.js for themes with custom selected price summaries (e.g. .growshophr-selected-price), dynamically syncing anchor prices and 30-day lowest prices on card/pill selection.
* Tooltips: stored legal tooltip text in data-tooltip-text to prevent server-side tag stripping (e.g. search indexes, RSS feeds, recently viewed widgets) from concatenating legal explanation paragraphs into plain-text prices, with seamless CSS/JS hydration.
* Layout: standardized full-width flexbox wrapping (.price > .bazna-cijena) in modern catalog product grids to prevent staggered card heights and button misalignment.
* Tooltip Clipping: un-clipped tooltip popups on hover and active states (.product-card:has(...)) to prevent overflow: hidden card bounds from cropping tooltips.
* Mobile & Checkout: hidden compliance badges on 48px mobile sticky purchase bars to protect touch targets; added responsive wrapping for reference pricing in classic checkout order review tables.
* Extensibility: added filterable archive hooks (twbce_cijena_archive_hooks) supporting custom theme loop hooks such as growshophr_product_card_content.

Package SHA-256: 37dbd2ecffb7c82b1a68c46a60288ff91d7d73016fe58fddd88229a2fca1107f
