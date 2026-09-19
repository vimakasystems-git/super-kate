# Super Kate SaaS Contract

Product model: SaaS/source-available
Status: design contract; runtime implementation pending source synchronization

## Required identity

Every protected request resolves tenant_id, authenticated subject, role and correlation_id. Client-supplied tenant identifiers are not trusted.

Roles: tenant_owner, tenant_admin, member, support_operator and superuser. Superuser access is limited to vimakasystems@gmail.com and dougcardoso07@gmail.com.

## Tenant controls

Tenant lifecycle: provisioning, active, suspended, archived, deletion-requested and deleted. Every tenant-owned read/write is authorized server-side. Cross-tenant access is non-disclosing. Suspended tenants cannot perform normal writes.

## Private integration

/API/vimaka is server-to-server. Requests require service identity, timestamp, nonce, correlation ID, signed body, replay protection and idempotency. Browser clients never receive service secrets.

## Priority risks

license compliance, tenant isolation, usage markers, secret leakage and commercial authorization

## Required tests

- tenant A cannot access tenant B
- tenant admins cannot grant superuser
- suspended/deleted tenants are blocked
- unsigned, replayed and revoked service requests fail
- privileged actions emit immutable audit events
