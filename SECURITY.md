# Security Policy — Super Kate

## Reporting

Report suspected vulnerabilities privately to vimakasystems@gmail.com. Do not publish credentials, tokens, personal data or exploit details in a public issue.

Include:

- affected repository and commit
- affected route/component
- reproduction steps or safe proof
- impact assessment
- proposed mitigation if known

## Response

The maintainers will triage the report, restrict access to sensitive evidence, record the decision in Git and coordinate remediation. Production secrets must be revoked and rotated immediately if exposure is suspected.

## Scope

Authentication, authorization, tenant isolation where applicable, secret handling, API boundaries, dependency vulnerabilities, injection, SSRF, path traversal, data exposure and privacy/LGPD failures are in scope.

SaaS systems must also report cross-tenant access, RBAC escalation and /API/vimaka authorization failures.
