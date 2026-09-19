# SEO and Performance Baseline

## Public pages

Provide a unique title and description, canonical URL, robots policy, sitemap, Open Graph/Twitter metadata, accessible heading hierarchy and structured data where appropriate.

Authenticated tenant and admin routes must be excluded from indexing and must not leak tenant data through metadata, URLs or previews.

## Performance

Define and measure:

- Core Web Vitals for public pages
- initial JavaScript and CSS budgets
- largest contentful paint
- interaction latency
- API p50/p95 latency
- external dependency timeout/error rate
- database query and cache behavior

Use compressed assets, caching for public immutable assets, no-store for private responses and lazy loading for non-critical content.

## Evidence

Record the measurement command, environment, result, date and unresolved risks in EXECUTION-STATE.md before publication.
