# Titanworks Bazna Cijena 2.0.32

* Currency parser tolerance: added European thousands-separator and currency-symbol support to price normalization (`Currency::to_storage()`), accepting values such as "1.234,56 €" and "1,234.56 EUR" with robust float fallback.
* Product editor save workflows: resolved item mapping for draft, pending, and standalone products by falling back to direct item resolution and variation lookups when catalog manager queries return empty for non-published products.
* Barcode meta persistence: automatically saved barcode identifiers (`_twbce_barcode`) during standard WooCommerce product updates and standalone post saves.
* Export publication auditability: recorded failed publication attempts in `wp_sidrena_publications` and passed structured validation findings to the `twbce_cijena_publication_failed` action hook.
* Form clarity and statutory format hints: added helper text across standalone product editing (SKU, price, reference date, and reason) and sales location editing (OIB and registered business seat).
* Quality gates: 750 unit tests (2,922 assertions) passing 100%; Croatian translation catalog 100% complete with 0 untranslated strings.

Package SHA-256: e4131c3cb9392fbcda0a1afc119fd4a3ca3041805d3e2a6cfc06968fa1632c2d
