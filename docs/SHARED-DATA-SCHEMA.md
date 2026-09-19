# Shared SaaS Data Schema

Status: implementation contract; adapt to the system's persistence layer

## Tenant

Required fields:

- id: opaque server-generated identifier
- name: bounded display name
- status: provisioning | active | suspended | archived | deletion_requested | deleted
- created_at, updated_at
- retention_until
- legal_hold: boolean

## Membership

Required fields:

- id
- tenant_id
- subject_id
- role: tenant_owner | tenant_admin | member
- status: active | suspended | revoked
- created_at, updated_at
- granted_by

Rules: unique subject per tenant, server-side tenant filtering, no client-selected role elevation.

## AuditEvent

Required fields:

- id
- occurred_at
- tenant_id when applicable
- actor_subject_id
- actor_role
- action
- resource_type
- resource_id
- correlation_id
- outcome
- metadata with secrets and unnecessary personal data removed

Audit events are append-only, access-controlled and retained according to the LGPD/legal policy.

## ServiceRequest

Required fields:

- idempotency_key
- service_identity
- tenant_id when applicable
- timestamp
- nonce
- correlation_id
- schema_version
- action
- outcome

Replay, stale timestamps and revoked identities must be rejected.
