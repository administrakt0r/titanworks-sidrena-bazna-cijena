# Titanworks Bazna Cijena 2.1.0

* Compliance: price lists follow NN 132/2026-1584. They use the new goods column order (adds neto_kolicina and ean_barkod; drops vrsta, datum_sidrene_cijene and dostupnost), and services go in a separate list.
* Compliance: filenames start with the merchant OIB and include ROBA/USLUGE, YYYYMMDD, and ZA_SVA_PRODAJNA_MJESTA when one list covers all locations. A missing OIB blocks generation.
* Compliance: the 11:00 deadline applies, any price change republishes within minutes, and replaced lists stay public for 15 days after replacement.
* Compliance: the label defaults to "Bazna cijena" and legacy labels and tooltip are migrated. Variable products show the base-price range before a variation is chosen. Sale prices are never captured as the base price.
* Fix: SKUs are no longer copied into the barcode column, and WooCommerce's GTIN field is read. Missing prices export as empty instead of 0,00.
* Fix: the public feeds disable LiteSpeed/CDN page caching and are purged after each publication.
* Fix: the base-price range on variable products no longer disappears on page load or after a variation is cleared.
* Fix: settings migrate on cron and WP-CLI too, so the first scheduled run after updating already uses the new rules. XML records always carry every field in the statutory order.
* Import: the plugin's own NN 132/2026 goods list can be re-imported. A file without a reference-date column keeps each item's existing base-price date; new items need a date. Standalone and WooCommerce products get a net quantity field.
* Fix: an identical list republishes after it was superseded or when the OIB or list scope changes, and other locations' lists are retired only after the shared list publishes.

Package SHA-256: 19ee3f1aa2f3fad296e7fb9cc7d167aae0c4e90d2f58d4ca7e8ba08c64d7e8cb
