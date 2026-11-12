# Organization standards

These standards apply to every repository in `iniciativa-batuta`. They are normative:
**must** means required, **should** means expected unless there is a documented reason,
and **may** means optional.

The goal is consistency without bureaucracy. A standard exists to prevent a concrete
failure mode, not to decorate a repository.

## Index

- [Repository baseline](repository-baseline.md)
- [Documentation](documentation.md)
- [Issues](issues.md)
- [Labels](labels.md)
- [Pull requests](pull-requests.md)
- [Commits and branches](commits.md)
- [Releases](releases.md)
- [Security](security.md)

## Changing a standard

1. Open a pull request against this repository.
2. Explain the problem, the proposed rule, the trade-off, and affected repositories.
3. Get maintainer approval.
4. Update affected repositories in the same change or a linked change.

Do not create a repository-specific exception by silently ignoring a rule. Document the
exception in the repository README or an architecture decision.

## Language

- Source code, identifiers, filenames, branches, commit messages, issues, pull requests,
  and technical documentation: **English**.
- User-facing product copy and the organization profile: the language required by the
  audience. The Batuta organization currently uses **Portuguese** for the public profile.
- One language per document. Do not mix languages in the same paragraph or list.
- Translate a document only when the translation will be maintained. A stale translation
  is worse than a link to the maintained version.
