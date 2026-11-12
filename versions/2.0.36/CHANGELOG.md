# Titanworks Bazna Cijena 2.0.36

* Product card anchor price sizing & layout: fixed critical visual defect where anchor prices rendered oversized (22px) and trapped inside WooCommerce Block theme price badges (#f2f2f2).
* Style preset options cascade: removed hardcoded font-size on subtle style preset that overrode card display size settings, ensuring admin sliders smoothly control card typography between 11px and 15px.
* Block theme component isolation: filter_price_block() now extracts and relocates anchor markup outside wc-block-components-product-price so price background pills only enclose the product price itself.
* 30-day lowest price card context: render_thirty_day() and thirty-day-price.php now support card context, card style presets, and card_display_size.
* Codified agent guidelines: added AGENTS.md § 7 requiring mandatory headless Chromium computed style audits and visual screenshot verification for all frontend changes.
* Quality gates: 798 unit tests (3,100 assertions) passing 100%; Croatian translation catalog 100% complete (932 translated / 0 untranslated strings); PHPCS and PHPStan Level 6 clean (0 errors).

Package SHA-256: d3684620af17aed8e0383eaaccb9b608b8285230f292b04900c0675bac465d11
