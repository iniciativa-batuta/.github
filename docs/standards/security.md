# Security standard

## Reporting a vulnerability

Do not open a public issue, discussion, or pull request with exploit details.

Use GitHub private vulnerability reporting or a draft security advisory in the affected
repository. If that is unavailable, contact the organization maintainers through the
organization profile and ask for a private channel.

Include:

- Affected repository and version or commit.
- A description of the vulnerability and its impact.
- Reproduction steps or a proof of concept, shared privately.
- Whether the issue is already public.
- Any suggested mitigation.

There is no bug bounty program unless a repository explicitly states otherwise. Do not
promise a response time the organization cannot meet.

## Scope

Security reports are relevant for:

- Authentication and authorization bypass.
- Credential or secret exposure.
- Remote code execution or command injection.
- Path traversal or sandbox escape.
- Snapshot, protocol, or state-integrity violations.
- Denial of service caused by unbounded input.
- Supply-chain compromise.

## Handling

1. Acknowledge the report privately.
2. Reproduce and assess impact.
3. Contain the issue and prepare a fix in a private branch or advisory.
4. Add a regression test.
5. Release a patch.
6. Publish an advisory with affected versions, fixed version, impact, and mitigation.
7. Credit the reporter if they agree.

Do not rewrite public history to hide a vulnerability. Do not publish details before a
fix is available unless users are at immediate risk and disclosure is coordinated.

## Secrets

- Never commit tokens, passwords, private keys, or production configuration.
- Use environment variables or files with restrictive permissions for local
  development.
- Example configuration uses placeholders, never real values.
- Logs, errors, audit metadata, and snapshots must redact credentials and secret values.
- Rotate a secret immediately if it is exposed, even if the commit is removed.
- Do not paste real secrets into issues or pull requests.

## Dependencies

- Enable Dependabot alerts and security updates.
- Review new dependencies for maintenance, license, and attack surface.
- Prefer the standard library when it solves the problem.
- Pin versions where reproducibility matters.
- Do not add a dependency for a trivial helper.

## Secure defaults

- Authentication is required outside loopback.
- TLS is required for non-loopback transport unless an explicit development mode is
  enabled and clearly warned.
- The shell executor is disabled by default.
- Working directories are restricted to configured roots.
- Input, output, payload, and execution duration are bounded.
- Secrets are referenced from worker-local sources, not stored centrally.
- A worker can only access its own assignments and executions.

## Pull request security checklist

- [ ] No secrets or credentials in code, tests, fixtures, or examples.
- [ ] New input is validated and bounded.
- [ ] Authorization is checked on every new endpoint or command.
- [ ] Errors do not leak sensitive values.
- [ ] Logs redact credentials and request bodies.
- [ ] Process execution does not introduce shell interpolation.
- [ ] File paths are resolved and constrained to allowed roots.
- [ ] Dependencies are justified and reviewed.
- [ ] A security-relevant behavior change has a test.
