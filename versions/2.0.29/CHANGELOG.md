# Titanworks Bazna Cijena 2.0.29

* Fixed duplicate plugin header: removed Author URI matching Plugin URI to ensure compliance with WordPress.org Plugin Check and directory upload guidelines.
* Unit test coverage expansion: authored dedicated test suites for PublicArchiveSitemapProvider (sitemap provider identity, canonical archive URL generation, bounds clamping, subtype ignorance), Cli\ImportCommand (CLI arguments, --confirm-overwrite, dry-run previews, rollback on failure, JSON and table output formatting), and Cli\SeedTestDataCommand (scenario parameters, confirmation cancellation, standalone product and taxonomy seeding, multi-scenario batch execution).
* Robust unit stubs: isolated WP_CLI_Command and WP_Sitemaps_Provider into separate guards, added wp_insert_post() test stub with failure injection, and enhanced get_posts() with post_status any and meta query filtering.
* Quality gates: 703 unit tests (2,673 assertions) passing 100%; Croatian translation catalog complete with 0 untranslated strings.

Package SHA-256: 3b98e3017ec69c5e90263461e6daff4c3c2cc26c60898148d4ed4e06578039ce
