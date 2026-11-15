# Titanworks Bazna Cijena 2.0.47

* Fix: the anchor-price tooltip now closes with Esc or a second tap or Enter even while the pointer or focus is still on it (it previously stayed visible).
* Performance: the cart/checkout block script and its WooCommerce checkout dependencies load only when cart and checkout reference lines are turned on, removing about 43 scripts from every storefront page by default.
* Admin: every logged event (including generation warnings, catch-up runs and file integrity checks) now has a translated label and can be selected in the Logs and Audit filters.
* Code: removed unused internal methods. No change to price history, exports or legal display rules.

Package SHA-256: c31986fc7853c27bebc5a826a9ee2b11b00b1f37ac596c4bf54c9d04c13e0941
