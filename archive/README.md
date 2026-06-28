---
owner: operator
status: template
last_updated: 2026-06-27
source_of_truth: company-os-starter-kit
load_policy: archive
related:
  - /GOVERNANCE.md
---

# Archive

`archive/` contains retired material excluded from default agent loading.

## What belongs here

- old strategies
- superseded playbooks
- completed projects kept for reference
- retired client or operating context that should not guide current work

## What does not belong here

- active company context
- current strategy
- live processes
- generated drafts that belong in `output/`

## Rules

- Mark archived files with `load_policy: archive`.
- Link to the replacement file when one exists.
- Do not delete history if future agents may need the reason it changed.

## Prompts for operators

- Why is this archived?
- What replaced it?
- Should agents ever load it by default?
