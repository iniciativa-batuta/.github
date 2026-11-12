# Iniciativa Batuta — organization defaults

This public `.github` repository holds the organization's shared community health files,
issue and pull request templates, and engineering standards. GitHub uses these files as
defaults for any repository in the organization that does not define its own.

The organization profile is rendered from [`profile/README.md`](profile/README.md).

## What is here

| Path | Purpose |
| --- | --- |
| [`profile/README.md`](profile/README.md) | Public organization profile. |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | Contribution workflow and definition of done. |
| [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) | Community behavior expectations. |
| [`SECURITY.md`](SECURITY.md) | Private vulnerability reporting and security expectations. |
| [`SUPPORT.md`](SUPPORT.md) | Where to ask for help. |
| [`GOVERNANCE.md`](GOVERNANCE.md) | Decision-making and maintainership. |
| [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE/) | Default issue forms. |
| [`.github/pull_request_template.md`](.github/pull_request_template.md) | Default pull request template. |
| [`docs/standards/`](docs/standards/) | Repository, documentation, issue, PR, commit, release, label, and security standards. |

## How defaults work

- The `.github` repository must be **public**.
- A repository that has its own file of a given type overrides the organization default.
- If a repository defines any valid issue template or issue template configuration, the
  organization's issue templates are not used for that repository.
- Labels referenced by templates must exist in this repository and in every repository
  where the templates are used. See [labels](docs/standards/labels.md).

## Repository baseline

Every repository should meet the [repository baseline](docs/standards/repository-baseline.md):
README, license, description and topics, branch protection, a documented architecture
or purpose, and the shared templates. Code repositories also need an `AGENTS.md` that is
short, durable, and actionable.

## Changing the standards

Open a pull request against this repository. A standards change is an organization
decision, not a personal preference. Explain the problem, the proposed rule, the
trade-off, and which repositories are affected. Update affected repository documents in
the same or a linked change.

## License

The standards and templates in this repository are published under AGPL-3.0. See
[LICENSE](LICENSE). Each repository still needs its own license file.
