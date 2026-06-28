---
owner: operator
status: template
last_updated: 2026-06-27
source_of_truth: company-os-starter-kit
load_policy: task
related:
  - /run/README.md
  - /.templates/workflow.md
---

# Workflows

`workflows/` contains function-level operating guides for sales, marketing/GTM, product, delivery, operations, and finance.

## What belongs here

- function mandates
- read first context for each function
- systems of record
- cadence and recurring outputs
- connector/tool expectations
- function-specific guardrails

## What does not belong here

- individual task lists
- generated reports
- live CRM or analytics data copied into markdown
- company-wide strategy that belongs in `strategy/`

## Recommended files

- `sales.md`
- `marketing.md`
- `product.md`
- `delivery.md`
- `operations.md`
- `finance.md`

## Prompts for operators

- What is this function accountable for?
- What context must agents read before acting?
- What system of record owns the live state?
- What outputs happen weekly or monthly?
