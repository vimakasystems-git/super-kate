# Dependency Policy — Super Kate

- Commit lockfiles for every package manager used by the runtime.
- Prefer reproducible installs in CI.
- Review Dependabot updates before merge.
- Run high-severity dependency audits on every release workflow.
- Do not run package lifecycle scripts in inventory jobs unless explicitly required.
- Remove unused dependencies and pin or constrain risky transitive providers.
- Record exceptions, affected versions, mitigation and expiry date.
- Rotate secrets if a compromised dependency may have accessed them.
- Never auto-push dependency changes from CI without review.
