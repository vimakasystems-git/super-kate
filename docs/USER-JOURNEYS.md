# User Journeys

## Visitor

Understand the product, privacy notice and support contact; sign in without receiving tenant data before authentication.

## Tenant owner

Create or accept a tenant, complete settings, invite members, assign allowed roles, configure integrations, review usage, open support tickets, export data and request deletion.

## Tenant admin

Manage members, settings, operational data and support within the tenant. Cannot grant superuser or access another tenant.

## Member

Use product features allowed by membership, see clear loading/empty/error states and manage personal session/privacy settings.

## Support operator

Access only the assigned tenant through time-limited, explicitly logged support access. Cannot silently impersonate or export unrelated tenants.

## Superuser

Only vimakasystems@gmail.com and dougcardoso07@gmail.com. Review system health, tenants, audit events, security findings, support escalation, deployment status and integrations. Every privileged action is audited.

## Failure and recovery

Every journey must explain authentication failure, permission denial, dependency outage, rate limit, retry behavior and data deletion state without exposing secrets or cross-tenant information.
