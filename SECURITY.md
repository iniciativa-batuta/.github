# Security policy

## Reporting a vulnerability

Do not open a public issue, discussion, or pull request with exploit details.

Use GitHub private vulnerability reporting in the affected repository, or open a draft
security advisory. If the repository does not expose that option, contact the
organization maintainers through the organization profile and ask for a private channel.

Please include:

- The affected repository, version, or commit.
- A description of the issue and its impact.
- Reproduction steps or a proof of concept, shared privately.
- Whether the issue is already public.
- Any suggested mitigation.

## Supported versions

Batuta is pre-alpha. Only the latest commit on the default branch is supported until the
first tagged release. After that, the supported versions will be listed here or in the
repository release notes.

## Scope

In scope:

- Authentication and authorization bypass.
- Credential or secret exposure.
- Remote code execution, command injection, or sandbox escape.
- Path traversal and arbitrary file access.
- Snapshot, protocol, or state-integrity violations.
- Denial of service caused by unbounded input or resource use.
- Supply-chain compromise.

Out of scope:

- Issues in unsupported versions or local modifications.
- Social engineering.
- Physical access attacks.
- Vulnerabilities in dependencies that are already publicly known and not exploitable in
  the supported configuration. Report them anyway if the project's usage is affected.

## Handling

1. Acknowledge the report privately.
2. Reproduce and assess the impact.
3. Prepare a fix in a private branch or advisory.
4. Add a regression test.
5. Release a patch and publish an advisory with affected versions, fixed version, impact,
   and mitigation.
6. Credit the reporter if they agree.

There is no bug bounty program unless a repository explicitly states otherwise. Do not
promise a response time that the organization cannot meet.

## Safe contribution practices

- Never commit tokens, passwords, private keys, or production configuration.
- Use placeholders in examples.
- Redact secrets from logs, issues, and pull requests.
- Report a leaked secret immediately and rotate it.
- Enable Dependabot alerts and private vulnerability reporting in every repository.

## Security standards

See the [security standard](docs/standards/security.md) for repository expectations and
the pull request security checklist.
