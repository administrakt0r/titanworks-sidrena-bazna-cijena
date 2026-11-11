# Titanworks Bazna Cijena 2.0.31

* Product editor save workflows: eliminated form action shadowing and implicit submission hijacking so pressing Enter or saving product updates never submits to admin-post.php.
* Native product update persistence: anchor prices entered or updated in the product editor panel now persist automatically on standard WooCommerce "Update" and standalone post save.
* Legal evidence idempotency: skipped re-recording unchanged anchor prices and reference dates to prevent duplicate rows in the append-only price history table.
* Correction reason enforcement: required documented explanation when amending existing anchor records on product save.
* Import parser tolerance: enhanced CSV import parser to accept currency symbols (€, EUR) and flexible date formats with spaces, slashes, or trailing dots.
* Quality gates: 742 unit tests (2,887 assertions) passing 100%; Croatian translation catalog 100% complete with 0 untranslated strings.

Package SHA-256: a6e9668cbfe545bcfffa41d5206f16198c6b0e838537918db077a506cde59393
