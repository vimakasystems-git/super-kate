# Release Test Matrix — Super Kate

Every applicable row must have a command, CI result or reproducible evidence before publication.

| Area | Required evidence |
|---|---|
| Build | clean install/build with pinned or reviewed dependencies |
| Functions | happy path, invalid input, auth failure, dependency failure and idempotency where relevant |
| Security | secret scan, dependency audit, auth/RBAC, secure headers, rate limits and abuse cases |
| Data isolation | tenant A/B negative tests for SaaS; user/session isolation for consumer apps |
| Observability | health, readiness, version, correlation ID, structured error and latency evidence |
| LGPD | privacy notice, access/export/correction/deletion and redacted logs |
| Performance | bundle, API latency, timeout behavior and mobile/web budget |
| SEO | title, description, canonical, robots, sitemap, social metadata and headings for public pages |
| Support | ticket/contact creation, status, escalation, audit and redaction |
| API | /API/vimaka server-only authentication, replay rejection, idempotency and schema validation |
| Cloudflare | TLS, WAF, rate limits, secrets, health probe and rollback smoke test |

## Publication gate

Mark each row pass or record a concrete blocker in EXECUTION-STATE.md. Do not publish with unknown status.
