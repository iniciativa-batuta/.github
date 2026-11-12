# Repository baseline

Every repository must be understandable and operable by someone who did not create it.

## Required files

| File | Required for | Notes |
| --- | --- | --- |
| `README.md` | All repositories | What it is, why it exists, how to use it, status, license, links. |
| `LICENSE` | All repositories | A repository-local license file. Defaults cannot provide a license. |
| `.gitignore` | All repositories | Ignore build output, local state, secrets, and editor files. |
| `AGENTS.md` | Code repositories | Short, durable instructions for AI coding agents. Not a copy of the README. |
| `docs/ROADMAP.md` | Product repositories | Phased plan with exit criteria. |
| `docs/architecture/overview.md` | Product repositories | Components, boundaries, flows, non-goals. |
| `docs/architecture/decisions.md` | Product repositories | Relevant decisions, alternatives, trade-offs. |
| `docs/issues/` | Planning phase | Markdown issue breakdown until work is published as GitHub issues. |
| `CONTRIBUTING.md` | Organization default | Inherited from `.github` unless a repository needs different rules. |
| `SECURITY.md` | Organization default | Inherited from `.github`. |
| `CODE_OF_CONDUCT.md` | Organization default | Inherited from `.github`. |
| `SUPPORT.md` | Organization default | Inherited from `.github`. |

A repository may override a community file. Do not override it just to duplicate the
default text.

## Repository metadata

- **Name:** lowercase kebab-case. Use a product prefix when the name would otherwise be
  ambiguous.
- **Description:** one sentence explaining what the repository is, not a slogan.
- **Topics:** only meaningful, searchable topics. Avoid a wall of generic tags.
- **Default branch:** `main`.
- **License:** AGPL-3.0 for Batuta software unless a specific component has a documented
  reason to use another OSI-approved license.
- **Visibility:** public by default for documentation and standards. Private only for
  sensitive material that cannot be published.

## Recommended GitHub settings

- Enable private vulnerability reporting.
- Enable Dependabot alerts and security updates.
- Protect the default branch:
  - Require a pull request before merging.
  - Require status checks when CI exists.
  - Require conversation resolution.
  - Disallow force pushes and branch deletion.
  - Do not require a second reviewer while the organization has only one maintainer; use
    the pull request checklist and self-review instead. Add the requirement when a second
    maintainer exists.
- Allow squash merge only, and delete the branch after merge.
- Keep the issue tracker enabled. Disable unused features instead of leaving empty pages.

## Code repository expectations

- Build, test, vet, and format commands are documented and work from a clean checkout.
- CI runs the same commands, not a different set.
- The module or package path matches the repository URL.
- Secrets are never committed. Provide an example configuration with placeholders.
- Generated files are either reproducible through a documented command or excluded.
- `AGENTS.md` contains durable engineering rules, not a chronological plan.

## Documentation repository expectations

- The README explains how the repository is consumed and who it serves.
- Standards are normative and have a change process.
- Templates are valid and do not reference labels that do not exist.
- Examples are consistent with the actual tools.

## Checklist

Use this checklist when creating or reviewing a repository:

- [ ] README explains purpose, status, usage, and license.
- [ ] LICENSE exists in the repository.
- [ ] Description and topics are set.
- [ ] Default branch is `main`.
- [ ] Branch protection and merge settings are configured.
- [ ] Private vulnerability reporting is enabled.
- [ ] Required documentation exists and is linked from the README.
- [ ] `AGENTS.md` exists for code repositories.
- [ ] Issue and PR templates resolve from the organization defaults.
- [ ] Labels used by templates exist.
- [ ] No secrets, local paths, or generated artifacts are committed.
- [ ] CI, when present, runs the documented checks.
