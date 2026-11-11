# Titanworks Bazna Cijena 2.0.30

* Publisher corruption recovery: added disk integrity validation for existing price list publications (existence, readability, non-zero file size, recorded size match, and SHA-256 checksum) so truncated or corrupt files automatically trigger clean re-generation.
* Migration and upgrade persistence: ensured default settings, rule configurations, and default webshop location are automatically seeded and preserved when updating via WordPress background or zip update routines.
* Product editor robustness: added fallback to children variations when variable products are unpublished or in draft, preventing empty state lockouts and preserving special sales persistence during normal product updates.
* Form clarity and helper text: added source-of-truth guidance across setup, sales locations (registered business seat for online stores), anchor price reference dates, and special sales.
* Multibyte CSV header normalization: fixed uppercase Croatian diacritic transliteration in CSV import column mapping.
* Empty catalog clarity: improved bulk anchor entry screen to distinguish between an empty store catalog and a fully anchored catalog.
* Quality gates: 735 unit tests (2,866 assertions) passing 100%; Croatian translation catalog 100% complete with 0 untranslated strings.

Package SHA-256: 2b8ce80adbe7404aa09383b85f489b76c62637d9ac5a83231a48f77d7fa15fd1
