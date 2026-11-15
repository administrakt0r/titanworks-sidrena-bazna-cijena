# Titanworks Bazna Cijena 2.0.48

* Storefront: the public price list now shows one clear empty state when a filter has no matches; open anchor tooltips stay positioned inside the viewport after resizing.
* Admin: Logs and Price History offer a Clear filters link. An unfiltered empty Logs page now says that no entries exist.
* Performance: public price-list generation releases the runtime object cache in batches on large catalogs, reducing measured peak memory from 249.1 MiB to 147.6 MiB on 5,216 items without changing the HTML.
* Cleanup: removed unused internal helpers, an orphan CI template and unused admin CSS selectors. No change to legal price calculations or stored history.

Package SHA-256: 83e2fb56dca5f95a843d2213940be3cfcaf853e23d813c607842a83c72cad27f
