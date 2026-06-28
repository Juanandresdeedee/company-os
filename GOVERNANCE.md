---
owner: operator
status: template
last_updated: 2026-06-27
source_of_truth: company-os-starter-kit
load_policy: always
related:
  - /AGENTS.md
  - /decisions/README.md
  - /output/README.md
---

# Governance

Governance keeps the Company OS reliable enough for agents to use.

## Change workflow

Use branch, review, merge for durable changes.

1. Propose a change in a branch.
2. Keep changes focused and linked to the relevant owner.
3. Review for accuracy, sensitivity, and source of truth boundaries.
4. Merge only when the owner accepts the change.

Do not silently rewrite strategy, governance, skills, client context, or operating rules.

## Ownership

Every durable file should identify an owner in frontmatter. Ownership means the person or function responsible for accuracy, review, and updates.

## Context and output

Context is what agents read to act. Output is what agents produce.

- Canonical context belongs in `company/`, `strategy/`, `run/`, `change/`, `wiki/`, `workflows/`, `clients/`, `decisions/`, `.ai/skills/`, and selected `plugin/` docs.
- Generated output belongs in `output/`.
- Raw inputs belong in `raw/`.
- Retired context belongs in `archive/`.

Do not place generated campaign drafts, reports, or briefs next to canonical operating rules unless they have been reviewed and harvested.

## Harvest loop

Human corrections, repeated successful outputs, and project learnings should become durable improvements when they generalize.

Harvest into:

- `wiki/` for playbooks and SOPs
- `.ai/skills/` for repeatable agent procedures
- `run/` for recurring operating processes
- `change/` for transformation project learnings
- `decisions/` for choices that explain why the OS works this way

## Approval rules

Require explicit human approval for:

- external sends or publishing
- deleting records or files outside normal draft cleanup
- deployments or production changes
- money movement or contractual commitments
- credential or permission changes
- sharing client-confidential material
- loading files marked `load_policy: never`

## What not to add

Do not add product code, app code, Storybook, package manifests, generated software, private credentials, or runtime build artifacts. Tool configuration for agents is allowed when it belongs in `plugin/` or `.ai/`.
