---
owner: operator
status: template
last_updated: 2026-06-27
source_of_truth: company-os-starter-kit
load_policy: always
related:
  - /decisions/README.md
  - /.templates/decision.md
  - /GOVERNANCE.md
---

# Decision agent guide

Use this guide when creating or updating decision records in `decisions/`.

Decision records explain why the Company OS works this way. They are not meeting notes, task lists or brainstorms.

## When to create a decision

Create a decision record when a choice changes:

- company strategy
- run processes
- change projects
- governance
- agent rules
- systems of record
- skills or playbooks
- client context boundaries

Do not create a decision record for small wording changes or temporary work.

## Naming

Use the next number in sequence:

```text
001-use-github-as-company-os.md
002-separate-run-and-change.md
```

Keep the title short. Use lowercase words separated by hyphens.

## Required structure

Use `.templates/decision.md`.

Every decision must include:

- context
- decision
- consequences
- alternatives considered
- supersedes, if it replaces an older decision

## Rules

1. State the decision in plain language.
2. Explain the context before the decision.
3. Separate the decision from the consequences.
4. Link affected files.
5. Do not hide tradeoffs.
6. Do not rewrite old accepted decisions to change history.
7. Supersede old decisions with a new record when the company changes its mind.
8. Keep live state in its system of record.

## Status values

Use one of these values in frontmatter:

- `proposed`
- `accepted`
- `superseded`
- `rejected`

## Review

Before a decision becomes `accepted`, the owner should check:

- the context is clear
- the decision is specific
- consequences are honest
- affected files are linked
- sensitive information is not exposed
- the decision does not conflict with `GOVERNANCE.md`

## What agents should do

When a user asks why something is set up a certain way, read `decisions/` before answering.

When a change creates a new rule, propose a decision record.

When a decision affects a process, skill, workflow or strategy file, update or link those files in the same change.
