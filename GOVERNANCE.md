---
owner: operator
status: template
last_updated: 2026-07-11
source_of_truth: company-os-starter-kit
load_policy: always
related:
  - /AGENTS.md
  - /company/changelog.md
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

## Durable metadata

Every canonical markdown file, including wiki and brand files, must carry the standard frontmatter fields: `owner`, `status`, `last_updated`, `source_of_truth`, `load_policy`, and `related`. Ownership means the person or function responsible for accuracy, review, and updates.

Convert legacy frontmatter to this standard as part of harvesting a migrated file. Do not preserve an incompatible legacy metadata format in canonical context.

Keep provenance out of canonical document bodies. Do not add inline attributions such as `(Source: 2026-07-10 meeting)`. Record provenance in `source_of_truth` and git history.

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

When the owner asks an agent to harvest, that request is acceptance. Write the harvested content as settled canonical statements without `proposed`, `pending confirmation`, or similar hedges. Evidence-gathering notes remain appropriate where future data is genuinely needed, for example `validate with customer interviews`.

Every harvest ends with these bookkeeping steps:

1. Set the source draft's frontmatter to `status: read` and leave it at the root of `output/`, named `YYYYMMDD-topic.md`. Do not create nested draft folders for new output files.
2. Add a dated, newest-first entry to `company/changelog.md` summarizing what was harvested and where it landed.

## Changelog boundary

The root `CHANGELOG.md` records repository housekeeping: structure, templates, skills, tooling, and releases. `company/changelog.md` records changes and refinements the company decided to make to its context. Formal rationale remains in `decisions/`; the company changelog is the readable timeline of how company thinking evolved.

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
