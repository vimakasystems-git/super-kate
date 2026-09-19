# Rollback Plan — Super Kate

## Rollback triggers

- authentication or authorization regression
- tenant isolation or privacy failure
- elevated 5xx/latency/timeouts
- exposed secret or dependency compromise
- broken support, payment or webhook behavior
- failed health/readiness or critical smoke test

## Procedure

1. Freeze publication and record UTC time, commit, deployment ID and correlation IDs.
2. Revert to the last verified Git commit or Cloudflare deployment.
3. Revoke/rotate affected credentials when exposure is possible.
4. Verify health, readiness, authentication, protected routes and public entry points.
5. Monitor errors and dependency behavior.
6. Record cause, impact, rollback evidence and follow-up regression test.

## Data safety

Do not roll back destructive data migrations without a reviewed restore plan. SaaS systems must preserve tenant isolation and audit events during rollback. ExploraSAMPA remains a consumer application.
