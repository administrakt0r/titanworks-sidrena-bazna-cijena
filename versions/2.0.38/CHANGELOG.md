# Titanworks Bazna Cijena 2.0.38

* Cart and Checkout Block styling & layout: added clean divider line and structured badge presentation for reference prices on /cart and /checkout.
* React VDOM text node preservation: preserved React-owned text node in WooCommerce Block Cart/Checkout ProductPrice component, collapsing raw text visually while maintaining characterData observer for dynamic recalculations (e.g., tax and shipping changes).
* Accessibility & screen reader optimization: marked structured badge presentation with aria-hidden="true", ensuring assistive technologies read clean semantic text without duplication.
* Dynamic lifecycle cleanup: automated badge removal when Store API refreshes cart items and reference suffixes disappear (e.g., promo expiration).
* Responsive slider typography: replaced fixed pixel sizing with responsive clamp scaling honoring --sidrena-size user settings.
* Quality gates: 804 unit tests (3,119 assertions) passing 100%; Croatian translation catalog 100% complete (931 translated / 0 untranslated strings); PHPCS and PHPStan Level 6 clean (0 errors).

Package SHA-256: b26768697d733293e5b509bd7fdf26342537be256c0ccf3e30087322d8441405
