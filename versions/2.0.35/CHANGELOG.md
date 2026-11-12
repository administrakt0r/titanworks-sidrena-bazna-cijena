# Titanworks Bazna Cijena 2.0.35

* Bulk anchor entry and save date validation: AnchorMetaBox, SpecialSaleMetaBox, and BulkAnchorEntryPage now preserve explicitly invalid reference and end date strings when submitting forms, ensuring domain services return actionable invalid_reference_date and invalid_sale_end_date errors rather than silently falling back to category dates or open-ended promotions.
* Product editor nonce cleanliness: eliminated duplicate _wp_http_referer hidden inputs in AnchorMetaBox by setting referer argument to false on wp_nonce_field, aligning with SpecialSaleMetaBox and keeping the native WooCommerce product editor form clean.
* Dedicated bulk anchor entry test suite: added comprehensive unit suite for BulkAnchorEntryPage (8 tests, 28 assertions) covering permission denials, completion banners, missing-items tables, row selection, failure counts, and bulk setup from current prices.
* Dedicated core model test suites: added unit test suites for CatalogItem (5 tests, 35 assertions) and Finding (5 tests, 10 assertions) covering key generation, price resolution hierarchy, severity fallback, and serialization.
* Quality gates: 794 unit tests (3,092 assertions) passing 100%; Croatian translation catalog 100% complete (932 translated / 0 untranslated strings); PHPCS and PHPStan clean (0 errors).

Package SHA-256: 582dfd2affabe73817041fd5a0d6faf8df18d5c39d1a4b02a049e80269bee025
