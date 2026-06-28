---
owner: operator
status: template
last_updated: 2026-06-27
source_of_truth: company-os-starter-kit
load_policy: task
related:
  - /company/README.md
  - /run/README.md
  - /change/README.md
---

# Strategy

`strategy/` contains the chain from current reality to choices.

Start with the company purpose and vision. Then define the goal, diagnose today, analyse important questions, write the thesis and state the tradeoffs.

## What belongs here

- 12 to 36 month goal and success measures
- today's honest diagnosis
- focused analysis in `analysis/`
- thesis: where we play, how we play, and how we reach the goal
- deliberate tradeoffs

## What does not belong here

- current task lists
- project implementation details
- recurring process checklists
- generated strategy drafts that have not been reviewed
- raw research dumps
- process metrics, which belong inside `run/processes.md`

## Recommended files

- `goal.md`
- `today.md`
- `analysis/`
- `thesis.md`
- `tradeoffs.md`

## Strategic chain

Work in this order:

1. Company purpose and goal.
2. Today: the honest diagnosis of where the company is.
3. Analysis: focused documents that answer specific strategy questions.
4. Thesis: where we play, how we play and how we reach the goal.
5. Tradeoffs: what the company accepts and rejects.
6. Run processes and change projects derived from the thesis.

## Analysis standard

Put each analysis in `strategy/analysis/`.

Name each file with the date and a short title:

```text
YYYYMMDD-title.md
```

Each analysis must start with:

- context and observation
- question
- current data
- diagnosis

Use George Polya's method from 'How to solve it':

1. Understand the problem.
2. Make a plan.
3. Carry out the plan.
4. Look back.

## Prompts for operators

- What is the next measurable milestone?
- What is true about the business today?
- What problems come from the current business model or operating system?
- What question needs focused analysis?
- What must be true for the thesis to work?
- What will we deliberately not do?
