# Titanworks Bazna Cijena 2.0.33

* Direct indexed seeking and memoization in price history: PriceHistoryRepository::latest() now queries the composite index directly with request-level memoization, eliminating broad 10-clause generic scans and executing repeat or batch-hydrated lookups in 0 DB queries.
* Publications index COUNT(*) bypass: PublicationRepository::index() now bypasses the unbounded COUNT(*) query on page 1 when retrieved row count is under the limit, eliminating unnecessary queries on admin dashboard and publications views.
* Standalone catalog cache batch priming: StandaloneCatalogProvider::get_items() now batch-primes postmeta and taxonomy term caches, eliminating up to 3*N term queries and N meta queries in standalone mode.
* Optimized sale-period map lookups: PriceHistoryRepository::active_sale_period_map() now uses O(1) hash map membership checks instead of linear array scans.
* Quality gates: 758 unit tests (2,973 assertions) passing 100%; complete Croatian translation catalog with 0 untranslated strings.

Package SHA-256: b8eb3c33d1e483279032b3157802567055befaefc54e2678ac24674fd023973d
