# Titanworks Bazna Cijena 2.0.34

* WooCommerce availability input safety: WooCommerceDetector::product_exists() now guards against non-positive IDs, preventing unnecessary lookups on 0 or negative product identifiers.
* Frontend markup whitelist & charset guard: PriceDisplay::allowed_anchor_html() now whitelists data-sidrena-cijena-30-day on span elements, ensuring sanitize_markup() preserves statutory 30-day price markup, with a safe UTF-8 fallback in cart reference rendering.
* Actionable CSV import error handling: CsvParser::parse_file() reports a dedicated, translated import_encoding_unsupported error when file bytes cannot be converted to valid UTF-8, avoiding misleading missing-header messages.
* Expanded unit test suites: added dedicated PriceDisplayTest and WooCommerceDetectorTest suites and CSV encoding tests, expanding test suite to 773 tests (3,010 assertions) at 100% pass rate.
* Quality gates: complete Croatian translation catalog (932 translated / 0 untranslated strings); PHPCS and PHPStan Level 6 clean (0 errors).

Package SHA-256: 12c7c1ec9199e893d7d279c775c587d01e47096fa5b6fb0168e8ed431de1839c
