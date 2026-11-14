# Titanworks Bazna Cijena 2.0.44

* Naming: removed the legacy "sidrena" code identifiers. PHP namespace is now Titanworks\BaznaCijena, CSS classes and custom properties use bazna-* (for example .bazna-cijena and --bazna-size), and script handles, admin page slugs and REST headers follow the same naming. Themes or custom CSS that targeted .sidrena-cijena* selectors must switch to .bazna-cijena*.
* Data: plugin tables are renamed in place to the twbce_ prefix with RENAME TABLE on upgrade, so the append-only price history keeps every row.
* Public URLs: feeds now live at /bazna-cijena.xml and /bazna-cijena.csv, the price list at /bazna-cijena-cjenik/ and the archive at /arhiva-bazne-cijene/. The old addresses answer with permanent 301 redirects. The REST namespace is now bazna-cijena/v1 and WP-CLI commands are wp bazna-cijena <command>; the old sidrena-cijena/v1 namespace, wp sidrena-cijena commands and theme template overrides in a sidrena-cijena/ folder keep working.
* Unchanged: the statutory "Sidrena cijena" label wording and the sidrena_cijena / datum_sidrene_cijene fields of the published price-list format.

Package SHA-256: 5574b25452a8339e088c98e2273dc7d1911e43be37cd28b72de87384daa23eac
