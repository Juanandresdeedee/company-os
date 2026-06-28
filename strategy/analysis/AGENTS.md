---
owner: operator
status: template
last_updated: 2026-06-27
source_of_truth: company-os-starter-kit
load_policy: always
related:
  - /strategy/analysis/README.md
  - /strategy/today.md
  - /strategy/thesis.md
---

# Strategy analysis agent guide

Follow this guide for every file in `strategy/analysis/`.

## Rules

1. Use one file per strategic question.
2. Name files `YYYYMMDD-title.md`.
3. Start with context and observation, question, current data, and diagnosis.
4. Use George Pólya's method: understand the problem, make a plan, carry out the plan, then look back.
5. Separate facts from interpretation.
6. State uncertainty and data limits.
7. Link any proposed change to `strategy/today.md`, `strategy/thesis.md`, `strategy/tradeoffs.md`, `run/` or `change/`.

## Do not

- turn raw notes into strategy without analysis
- hide weak evidence
- copy live dashboards into markdown
- add project tasks here
- create broad analysis files that answer several unrelated questions

## Output standard

Each analysis should help the operator decide whether to update:

- `strategy/today.md`
- `strategy/thesis.md`
- `strategy/tradeoffs.md`
- `run/`
- `change/`
