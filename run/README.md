---
owner: operator
status: template
last_updated: 2026-06-27
source_of_truth: company-os-starter-kit
load_policy: task
related:
  - /strategy/README.md
  - /change/README.md
  - /workflows/README.md
---

# Run

`run/` describes how the current business operates. It contains strategic processes derived from the thesis, with owners, cadence, review rituals, metrics and systems of record.

## What belongs here

- recurring strategic processes
- process owners and decision rights
- cadence and review rituals
- metrics inside each process definition
- systems-of-record references
- escalation paths and failure signals

## What does not belong here

- one-time transformation projects
- task lists
- generated meeting notes
- live dashboards copied into markdown
- raw operational exports

## Recommended files

- `processes.md`
- `cycles.md`
- `review-rituals.md`
- `systems-of-record.md`

## Process standard

Each process should answer:

- What thesis or challenge does this process serve?
- Who owns it?
- What system of record stores live state?
- What cadence keeps it alive?
- What will we do?
- How will we know we do it well?
- What outcome should it create?
- What failure signal requires escalation?

## Metric types

Define metrics inside each process.

Use 3 metric types:

- activity metrics: what we will do
- quality metrics: how we will know we do it right
- outcome metrics: what outcome the process should create

## Prompts for operators

- What must happen every week, month, quarter, and year?
- Which processes turn strategy into operating rhythm?
- Which metrics show whether the company is healthy?
- What decisions should be made from this process?
