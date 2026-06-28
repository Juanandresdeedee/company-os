---
owner: operator
status: template
last_updated: 2026-06-27
source_of_truth: company-os-starter-kit
load_policy: reference
related:
  - /decisions/AGENTS.md
  - /.templates/decision.md
  - /GOVERNANCE.md
---

# Decisions

`decisions/` contains ADR-style records: context, decision, consequences, and supersession notes. Use it to preserve why the Company OS works this way.

Agents should read `decisions/AGENTS.md` before creating or changing decision records.

## What belongs here

- strategic and operating decisions
- architecture decisions for the OS
- tool and system-of-record choices
- decisions that affect processes, skills, or governance

## What does not belong here

- informal brainstorms
- generated drafts
- task lists
- decisions without context or consequences

## Naming

Use numbered files:

```text
001-use-github-as-company-os.md
002-separate-run-and-change.md
```

## Prompts for operators

- What changed?
- What alternatives were considered?
- Why was this decision made?
- What consequences should future agents understand?
