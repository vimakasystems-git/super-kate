# Super Kate Observability and LGPD Contract

Status: design contract; runtime implementation pending source synchronization

## Observability

Provide /api/health, /api/readiness and /api/version. Structured events include timestamp, service, environment, release, correlation_id, route, status, duration_ms and tenant_id when known. Never log secrets or unnecessary personal data.

Track request/error rates, latency, auth failures, rate limits, dependency failures, tenant usage and support failures. Alert on sustained 5xx, latency spikes and missing health signals.

## LGPD

Provide privacy notice, controller/processor mapping, purpose and lawful-basis records, data inventory, minimization, retention, export, correction, deletion, legal hold, incident response and audit trails. Redact personal data from logs and telemetry.
