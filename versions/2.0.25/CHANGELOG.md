# Titanworks Bazna Cijena 2.0.25

* Faster large-catalog generation: share one compliance validation and catalog mapping across CSV/XML, stream documents to disk, and calculate fingerprints and published checksums incrementally.
* Leaner publication and cleanup queries: allocate the next location sequence without hydrating the full location row, batch expired-publication updates, and avoid redundant publication reads.
* Faster repeated price-list downloads and storefront sale displays through cached serialized documents and one request-wide sale-period batch.
* Safer cache generation initialization when concurrent requests invalidate anchor-price caches.
* Directory-review hardening: public page and archive shortcodes now use the unique `twbce_cjenik` and `twbce_arhiva` tags; replace legacy `sidrena-cjenik` and `sidrena-arhiva` tags in page content.
* Quality gates: 640 unit tests (2,419 assertions); integration suite 103 tests / 488 assertions (1 skipped); 42 Chromium E2E tests; packaged Plugin Check reported no errors.

Package SHA-256: a73fc2343c197449fdeb2c26f79e66c27c75c3a4f5e8d75c9cf40e525ed9cc0d
