# Documentation standard

Documentation is part of the product. It must be accurate, scoped, and maintained with
the code it describes.

## Source of truth

- The repository is the source of truth for its own behavior.
- Link to another document instead of copying it.
- If two documents disagree, the more specific and more recent one wins, but the
  disagreement is a bug: fix or delete the stale copy.
- Do not publish the same decision in the README, an issue, and an architecture document
  with different wording. Summarize and link.

## Required structure for a product repository

```text
README.md
docs/
  ROADMAP.md
  architecture/
    overview.md
    domain-model.md
    worker-protocol.md
    execution-and-steps.md
    decisions.md
  examples/
  issues/            # while work is planned in Markdown
  guides/            # optional: operator and user guides
  reference/         # optional: CLI, API, configuration reference
  runbooks/          # optional: recovery and incident procedures
```

Create optional directories only when they contain real documents.

## What each document must answer

| Document | Questions it answers |
| --- | --- |
| `README.md` | What is this? Why does it exist? How do I start? What is the status? |
| `ROADMAP.md` | What are the phases, deliverables, dependencies, exit criteria, and risks? |
| `architecture/overview.md` | What are the components, boundaries, flows, topologies, and non-goals? |
| `architecture/domain-model.md` | What are the entities, states, invariants, and ownership rules? |
| `architecture/worker-protocol.md` | How do components communicate, authenticate, retry, and recover? |
| `architecture/execution-and-steps.md` | How does execution behave on success, failure, timeout, and cancellation? |
| `architecture/decisions.md` | Which decisions are accepted, provisional, or deferred, and why? |
| `docs/issues/` | What is the reviewable work breakdown? |
| `guides/` | How do users or operators perform a task? |
| `reference/` | What are the exact commands, fields, codes, and limits? |
| `runbooks/` | What do I do when a specific failure happens? |

## Writing rules

- Start with the purpose and audience. Do not open with a generic definition.
- Be explicit about what is implemented, planned, provisional, or out of scope.
- Prefer short paragraphs, tables, and concrete examples.
- Use RFC 3339 UTC timestamps in examples.
- Use Mermaid for diagrams so they are reviewable as text.
- Use fenced code blocks with a language. Commands must be copy-pasteable.
- Do not present illustrative output as verified output. Label examples as illustrative
  when IDs, timestamps, or responses are synthetic.
- Do not invent a percentage, metric, or guarantee that the system does not produce.
- Do not use "simply", "just", or "obviously" to skip a necessary explanation.
- Define acronyms on first use.
- Avoid marketing claims in technical documents.

## Docs as code

- Behavior changes and documentation changes belong in the same pull request.
- New configuration, commands, or protocol fields require reference documentation.
- Removed behavior must have its documentation removed or marked deprecated.
- Examples must be updated when the CLI or schemas change.
- A broken internal link is a defect.
- Architecture decisions that change the MVP scope update `decisions.md` and the
  roadmap.

## Issue documents

While work is planned in Markdown:

- One file per issue, prefixed with a stable number.
- The first heading is the issue title.
- Use the sections defined in the issue standard.
- Keep the Markdown and the published GitHub issue in sync.
- The index file is the entry point, not a duplicate of every issue body.

## Review checklist

- [ ] Purpose and audience are clear.
- [ ] Status (implemented, planned, provisional) is explicit.
- [ ] Examples match the actual commands and schemas.
- [ ] Links resolve.
- [ ] No duplicated source of truth.
- [ ] No secrets or private paths.
- [ ] Language follows the organization rule.
- [ ] Diagrams are text-based and render.
