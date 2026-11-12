# Contributing to Iniciativa Batuta

Thank you for taking the time to contribute. This document applies to every repository in
the organization. Repositories may add specific instructions, but they must not weaken
the rules here without a documented reason.

## Before you start

- Read the repository `README.md` and, for code repositories, `AGENTS.md`.
- Read the [organization standards](docs/standards/README.md).
- Follow the [Code of Conduct](CODE_OF_CONDUCT.md).
- For security issues, follow the [security policy](SECURITY.md). Do not open a public
  issue.

## Workflow

1. **Find or open an issue.** Search first. Use the issue form that matches the work.
   Small, well-scoped issues are merged faster than large ones.
2. **Agree on the approach** when the change is architectural, changes a public
   interface, or has more than one reasonable design. Open a research or design issue
   before writing a large implementation.
3. **Create a branch** using `type/short-slug`, for example `feat/worker-snapshot`.
4. **Make focused commits** following the [commit standard](docs/standards/commits.md).
5. **Update tests and documentation** in the same change.
6. **Open a pull request** using the template. Link the issue and list the commands you
   actually ran.
7. **Address review comments** and keep the branch current with the default branch.
8. **Squash merge** after required checks pass.

## Language

- Source code, identifiers, filenames, branches, commits, issues, pull requests, and
  technical documentation: English.
- User-facing product copy: the language required by its context. The public
  organization profile currently uses Portuguese.
- One language per document. Do not mix languages in the same section.

## Definition of done

A change is done when:

- The behavior is implemented and covered by tests.
- Failure paths, cancellation, timeouts, and invalid input are handled explicitly.
- Documentation and examples match the behavior.
- The validation commands were run and their results are reported.
- No secrets, local paths, generated artifacts, or unrelated changes are included.
- Known limitations are documented.

## Code expectations

- Prefer the simplest design that satisfies a demonstrated requirement.
- Keep domain rules independent of transport, storage, and specific executors.
- Do not add a dependency without a clear justification.
- Do not add speculative abstractions, configuration options, or extension points.
- Bound inputs, outputs, durations, and resource use.
- Never interpolate untrusted input into a shell command.
- Do not store secrets in source, task definitions, logs, or snapshots.

## Issues and pull requests

- Use the templates. Do not delete required sections.
- One concern per pull request.
- Do not claim a check passed unless it was executed.
- Do not force-push the default branch.
- Do not commit generated files unless the repository requires them.

## Questions

Use the `question` issue label. Include the repository, version, what you tried, and the
relevant error with secrets redacted. See [SUPPORT.md](SUPPORT.md).

## License

By contributing, you agree that your contribution is licensed under the repository's
license. Batuta software is licensed under AGPL-3.0 unless a repository states otherwise.
