---
name: company-purpose
description: Guided interview and drafting workflow for company purpose, vision, values, principles, strategic ambition, and an initial 12 to 36 month goal.
version: 0.1.0
category: company-os
managed_by: company-os-starter-kit
owner: operator
status: template
last_updated: 2026-06-27
source_of_truth: company-os-starter-kit
load_policy: task
related:
  - /company/README.md
  - /company/purpose.md
  - /company/vision.md
  - /company/values.md
  - /company/positioning.md
  - /strategy/goal.md
---

# Company purpose skill

Use this skill when an operator wants to clarify the identity layer of the Company OS:

- company purpose
- vision
- values
- operating principles
- strategic ambition
- initial 12 to 36 month goal

The goal is not to write a polished slogan. The goal is to produce durable context that helps humans and agents make better decisions.

## Read first

Before starting, read:

1. `/AGENTS.md`
2. `/company/README.md`
3. `/strategy/README.md`
4. Existing files in `/company/` if present
5. Existing `/strategy/goal.md` if present

## When to use

Use this skill when the user asks to:

- define company purpose
- clarify why the company exists
- write mission, vision, values, or principles
- align strategy around a company goal
- make agent context more durable
- start filling the Company OS

## Operating rules

- Interview first, draft second.
- Separate identity from marketing copy.
- Prefer concrete beliefs and decision rules over inspiring language.
- Challenge generic statements politely.
- Preserve uncertainty where answers are not settled.
- Do not invent company facts.
- Do not over-optimize for polish before the logic is clear.

## Interview flow

### Purpose interview

Ask:

- What problem does the company feel responsible for?
- Who would be worse off if the company disappeared?
- What do you believe about the market, people, technology, or work that others underweight?
- Why is this problem worth years of effort?

Draft:

- one plain-language purpose statement
- supporting explanation
- decision test: what this purpose should change

### Vision interview

Ask:

- What future should exist because this company succeeds?
- What should customers or users be able to do differently?
- What category, behavior, or market structure should change?
- What is the long-term time horizon?

Draft:

- future-state narrative
- 3 to 5 observable signs that the vision is becoming real

### Values interview

Ask:

- What behavior should be rewarded even when inconvenient?
- What behavior should be rejected even when profitable?
- What principles should agents preserve when optimizing?
- What has the company learned the hard way?

Draft values only if they create tradeoffs.

For each value, include:

- value name
- what it means
- what it rules out
- example decision it should affect

### Principles interview

Ask:

- When speed and quality conflict, what wins?
- When a customer request conflicts with strategy, what wins?
- When short-term revenue conflicts with long-term positioning, what wins?
- What should never be optimized away?

Draft principles as action rules, not slogans.

### Ambition interview

Ask:

- What level of company are you trying to build?
- What must become true in 12 to 36 months?
- What will be materially different about the operating system?
- What would make this chapter successful?

Draft:

- strategic ambition paragraph
- boundaries and non-goals

### Goal interview

Ask:

- What is the next measurable milestone?
- What primary metric proves progress?
- What supporting metrics reduce ambiguity?
- What is the deadline?

Draft a goal suitable for `/strategy/goal.md`.

## Output format

Produce a concise package with these sections:

```markdown
# Company purpose package

## Purpose
[Draft for /company/purpose.md]

## Vision
[Draft for /company/vision.md]

## Values
[Draft for /company/values.md]

## Operating principles
[Draft for /company/values.md]

## Strategic ambition
[Draft for /company/positioning.md or strategy context]

## 12 to 36 month goal
[Draft for /strategy/goal.md]

## Open questions
[Unresolved questions that need operator judgment]

## File updates
[List files to update]
```

## Quality checklist

The package is ready when:

- purpose is specific enough to guide tradeoffs
- vision describes a future state, not an activity list
- values change decisions
- principles are actionable
- goal has a measurable deadline
- language is plain and durable
- uncertainty is explicit
- no unsupported facts were invented

## Things to avoid

Avoid:

- "We help companies succeed" without a specific theory
- values that every company would claim
- mission statements that are only marketing copy
- vision written as internal growth targets only
- principles that do not constrain decisions
- goals without metrics or deadlines
- copying live operating state into durable identity docs

## Files to update

- `/company/purpose.md`
- `/company/vision.md`
- `/company/values.md`
- `/company/positioning.md`
- `/strategy/goal.md`

## Harvest guidance

If the interview reveals durable strategic choices, propose follow-up updates to:

- `/strategy/thesis.md`
- `/strategy/tradeoffs.md`
- `/strategy/today.md`
- `/decisions/`
