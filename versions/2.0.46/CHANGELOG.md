# Titanworks Bazna Cijena 2.0.46

* Performance: daily price-list generation no longer runs per-product queries for barcodes, categories and variations. On a 4,800-item catalog this cuts queries from about 10,600 to about 600 and halves run time. Published CSV/XML output is unchanged.
* Performance: generation peak memory no longer grows with the catalog (290 MiB to 158 MiB on 4,800 items), keeping large shops under a 256M memory limit. It can be turned off with the twbce_cijena_generation_release_object_cache filter.
* Packaging: the development-only seed-test-data WP-CLI command is no longer included in the release package.

Package SHA-256: aaba23746ef201282a61a0c5f55ce20f375be341dbdce0b68c853dfafee9ea9c
