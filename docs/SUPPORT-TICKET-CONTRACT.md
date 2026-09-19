# Support Ticket Contract

## Ticket fields

- id
- tenant_id
- requester_id
- subject and bounded description
- severity: low | medium | high | critical
- status: open | triaged | in_progress | waiting_customer | resolved | closed
- assigned_to
- created_at, updated_at, resolved_at
- correlation_id
- redacted attachments

## Rules

Tickets are tenant-scoped. A tenant member can view only tickets permitted by role. Support operators use time-limited audited access. Superusers can escalate and review all tickets.

Critical tickets trigger an operational alert and escalation to the CerebroBrasil control plane. Never include API keys, passwords, session cookies or unnecessary personal data in ticket text or attachments.

## SLA and audit

Define response and resolution targets per severity. Every status, assignment, escalation and export creates an immutable audit event. Closed tickets remain retained according to the LGPD policy.
