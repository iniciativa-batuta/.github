# Governance

## Current model

Iniciativa Batuta is maintainer-led. The current interim organization admin and
maintainer is [`@ShiMigui`](https://github.com/ShiMigui). As the project grows, additional
maintainers may be added.

## Decisions

- **Product and architecture:** documented in the affected repository's
  `docs/architecture/decisions.md`. A decision records the recommendation, alternatives,
  trade-offs, MVP impact, and whether it can be deferred.
- **Organization standards:** documented in this repository under
  `docs/standards/`. Changes require a pull request and maintainer approval.
- **Security:** handled privately through GitHub Security Advisories. See
  [SECURITY.md](SECURITY.md).
- **Day-to-day work:** tracked as issues and pull requests. Small, explicit changes are
  preferred over large, ambiguous ones.

When maintainers disagree, the decision is made by consensus. If consensus is not
possible, the maintainer responsible for the affected area decides and records the
rationale. Do not leave a decision implicit.

## Maintainers

Maintainers can:

- Triage issues and pull requests.
- Merge changes.
- Manage repository settings and releases.
- Approve organization standards changes.
- Handle security reports.

A contributor may be invited as a maintainer after sustained, high-quality
contributions, demonstrated care with security and review, and agreement with the
project's standards. With one maintainer, invitations are at that maintainer's
discretion. With multiple maintainers, a new maintainer requires approval from the
existing maintainers and no sustained objection.

Maintainers may step down at any time. Access should be removed when a maintainer is
inactive for an extended period or leaves the project.

## Releases

Releases follow the [release standard](docs/standards/releases.md). Only maintainers
publish releases, create tags, or change organization settings.

## Conflicts of interest

Maintainers must disclose a conflict of interest when reviewing a change that benefits
them financially or personally. If necessary, another maintainer should review the
change. With a single maintainer, the conflict must be documented in the pull request.

## Changes to this document

Open a pull request in this repository. Explain the problem and the proposed change.
Governance changes take effect after maintainer approval and merge.
