# Titanworks Bazna Cijena 2.0.28

* Expanded unit test coverage: dedicated suites for settings field renderers and first-offer evidence recording.
* Isolated the import-run test in its own PHP process so the WP_IMPORTING flag cannot leak between tests.
* Extended unit test stubs with guarded delete_post_meta, add_post_meta, get_post_status, get_the_date and wc_get_price_including_tax.
* Quality gates: 683 unit tests (2,568 assertions) passing 100%; Croatian translation catalog unchanged with 0 untranslated strings.

Package SHA-256: 47993727a837f192569371883915039090cc52ffeceb417eb7c317291e2060de
