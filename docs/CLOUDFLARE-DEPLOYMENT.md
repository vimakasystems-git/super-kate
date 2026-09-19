# Cloudflare Deployment Contract — Super Kate

Status: deployment design only; no Cloudflare resources provisioned

## Required edge controls

- TLS-only public traffic
- WAF managed rules enabled
- per-route rate limits
- request size and timeout limits
- security headers and controlled CORS
- bot and abuse protection appropriate to the product
- health and readiness probes
- structured request logs with correlation ID
- deploy version visible through a non-sensitive version endpoint

## Routing

Public application traffic uses the system hostname. Private /API/vimaka traffic uses server-to-server routing and is never exposed as a browser credential or unrestricted proxy.

Each system has separate staging and production routes, service identities and secrets. Do not share signing keys between systems.

## Secrets

Store API signing keys, provider credentials and deployment tokens in Cloudflare secrets or the approved secret manager. Never commit them, render them in HTML, send them to browsers or include them in logs.

## Data and state

Use the smallest suitable Cloudflare primitive after schema review:

- Workers for routing and edge logic
- KV only for non-sensitive cache/configuration
- D1 only after migration, backup and tenant-isolation review
- R2 for controlled artifacts
- Queues for asynchronous work
- Durable Objects only where coordination or locking is required

## Observability and rollback

Record deployment ID, commit, environment, route, status and latency. Every deployment must have a rollback target and a smoke test for public health, protected authentication and private API rejection from browsers.

## Release gate

Provision only after Git tests pass, secrets are configured, tenant or consumer privacy requirements are verified, WAF/rate limits are reviewed and rollback evidence exists.
