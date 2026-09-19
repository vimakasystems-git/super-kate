# Incident Response — Super Kate

## Trigger

Use this procedure for suspected credential exposure, unauthorized access, cross-tenant access, data leak, dependency compromise, payment/webhook abuse or service outage.

## Immediate actions

1. Record UTC time, service, commit, correlation IDs and evidence without copying secrets or personal data.
2. Revoke and rotate affected credentials.
3. Disable compromised routes or integrations when necessary.
4. Preserve redacted logs and deployment metadata.
5. Open a private incident record for the maintainers.

## Assessment

Classify confidentiality, integrity, availability and LGPD impact. For SaaS systems, identify affected tenant IDs. For ExploraSAMPA, identify affected user/app data without adding tenant semantics.

## Recovery

Patch the root cause, add a regression test, deploy through reviewed Git changes, verify health/readiness and monitor errors. Keep a rollback target.

## Communication

Notify affected stakeholders according to the incident and privacy policy. Do not disclose exploit details or credentials in public issues.

## Closure

Record cause, timeline, affected scope, rotations, tests, deployment commit, follow-up actions and retention/deletion decisions.
