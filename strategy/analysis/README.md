---
owner: operator
status: template
last_updated: 2026-06-27
source_of_truth: company-os-starter-kit
load_policy: task
related:
  - /strategy/README.md
  - /strategy/today.md
  - /strategy/thesis.md
---

# Strategy analysis

`strategy/analysis/` contains focused analysis documents.

Use one file per question. Name files with the date and a short title:

```text
YYYYMMDD-title.md
```

For example:

```text
20260627-pricing-model-limits.md
```

## What belongs here

- analysis that starts from an observation
- a clear question
- current data
- diagnosis
- options and tradeoffs
- next action or recommendation

## What does not belong here

- live dashboards copied into markdown
- raw research dumps
- project task lists
- final strategy without supporting reasoning

## Use George Pólya's problem-solving method

Follow this order:

1. Understand the problem.
2. Make a plan.
3. Carry out the plan.
4. Look back.

In this folder, that means:

- define the observation and question before you analyse
- list current data and limits
- explain the diagnosis
- show the reasoning
- state what should change in `today.md`, `thesis.md`, `tradeoffs.md`, `run/` or `change/`

## Required structure

Each analysis must start with:

1. Context and observation.
2. Question.
3. Current data.
4. Diagnosis.

Then add:

- reasoning
- options
- recommendation
- what to update
