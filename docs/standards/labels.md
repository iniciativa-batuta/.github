# Label standard

Labels are a classification system, not decoration. Use a small, consistent vocabulary.

## Rules

- Every issue has exactly one `type:*` label.
- Use `area:*` only for the parts actually affected. More than two areas usually means
  the issue should be split.
- Every issue has one `priority:*` label.
- Use `status:*` only when true. Clear it when the condition no longer applies.
- Templates may set a default label. The author must change it if it is wrong.
- A label referenced by a template must exist in this repository and in every repository
  where the template is used.

## Types

| Label | Color | Use for |
| --- | --- | --- |
| `type:feature` | `#1d76db` | New user-visible or architectural capability. |
| `type:bug` | `#d73a4a` | Incorrect behavior or a regression. |
| `type:docs` | `#0075ca` | Documentation, examples, standards, or comments. |
| `type:chore` | `#c5def5` | Maintenance, tooling, build, or repository hygiene. |
| `type:security` | `#b60205` | Security hardening, authentication, authorization, or secrets. |
| `type:research` | `#5319e7` | A question that must be answered before an implementation issue. |

## Areas

| Label | Color | Scope |
| --- | --- | --- |
| `area:core` | `#0052cc` | Domain, application orchestration, cross-cutting behavior. |
| `area:storage` | `#006b75` | SQLite, repositories, migrations, artifacts storage. |
| `area:api` | `#0e8a16` | Central HTTP API. |
| `area:cli` | `#1d76db` | Command-line interface. |
| `area:worker` | `#fbca04` | Worker runtime, local state, heartbeats. |
| `area:protocol` | `#5319e7` | Wire contracts, versioning, snapshots, channel. |
| `area:execution` | `#d93f0b` | Step runner, executors, continuity, timeouts. |
| `area:scheduler` | `#bfd4f2` | Assignment, priority, capabilities, dependencies. |
| `area:security` | `#b60205` | Auth, TLS, secrets, audit, threat boundaries. |
| `area:web` | `#c2e0c6` | Optional web interface. |
| `area:integrations` | `#f9d0c4` | Git, OpenCode, Docker, and other adapters. |

## Priority

| Label | Color | Meaning |
| --- | --- | --- |
| `priority:p0` | `#b60205` | Blocks safe use or the MVP; drop other work. |
| `priority:p1` | `#d93f0b` | Required for the current milestone. |
| `priority:p2` | `#fbca04` | Valuable, not required for the current milestone. |

## Status

| Label | Color | Meaning |
| --- | --- | --- |
| `status:blocked` | `#e99695` | Cannot proceed until a dependency or decision is resolved. |
| `status:needs-design` | `#d4c5f9` | The problem is known; the approach is not. |

## Other

| Label | Color | Meaning |
| --- | --- | --- |
| `dependencies` | `#0366d6` | Dependency update. |
| `good first issue` | `#7057ff` | Scoped, documented, and suitable for a newcomer. |
| `help wanted` | `#008672` | Maintainers want external help. |
| `question` | `#d876e3` | A question, not a defect or a planned change. |
| `duplicate` | `#cfd3d7` | Already tracked elsewhere. |
| `invalid` | `#e4e669` | Not a valid issue or not reproducible. |
| `wontfix` | `#ffffff` | Deliberately not planned. |

Do not add a new label for every nuance. Add a label only when it changes how work is
triaged or filtered.
