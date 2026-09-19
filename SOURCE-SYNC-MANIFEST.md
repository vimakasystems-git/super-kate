# Source Synchronization Manifest — Super Kate

Base44 application ID: 6aaae4c2df5420e03590b602
Product model: SaaS/source-available
Repository: vimakasystems-git/super-kate

## Expected synchronization

Export or synchronize the complete application source into this repository before implementation:

- frontend pages/components/assets
- entities and schema definitions
- backend functions and integrations
- authentication/authorization configuration
- environment templates without secrets
- dependency manifests and lockfiles
- tests and deployment configuration

## Rules

- Never commit Base44 secrets, OAuth secrets, API keys, session secrets or production data.
- Preserve the current Git execution plans and state files.
- Record the source commit, export date and Base44 app version after synchronization.
- Run inventory, security, performance, SEO, support and function baselines before changing behavior.
- For SaaS products, verify tenant_id and RBAC boundaries before exposing /API/vimaka.
- For ExploraSAMPA, keep consumer-app scope and do not add SaaS/Tenant billing.
