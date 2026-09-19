# Secrets Management — Super Kate

## Rules

- Secrets exist only in an approved secret manager or deployment secret store.
- Never commit secrets, production data or private keys.
- Never render service credentials in HTML, browser storage, URLs or client logs.
- Use separate staging and production values.
- Rotate after suspected exposure, staff/access changes or provider compromise.
- Record owner, purpose, environment, rotation date and revocation procedure without recording the secret value.
- CI uses read-only repository permissions unless a narrowly scoped deployment job requires otherwise.
- Logs and support tickets must redact authorization headers, cookies, API keys and personal data.

## Required inventory

Document each required secret by name, owner, environment, provider, rotation interval and failure behavior. Production must fail closed when a mandatory authentication or signing secret is absent.

## Inter-system API

/API/vimaka uses separate service identities and signing keys per system and environment. Revoked, stale, replayed or incorrectly signed requests are rejected.
