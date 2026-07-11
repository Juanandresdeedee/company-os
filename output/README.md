---
owner: operator
status: template
last_updated: 2026-07-11
source_of_truth: company-os-starter-kit
load_policy: reference
related:
  - /GOVERNANCE.md
  - /raw/README.md
  - /company/changelog.md
---

# Output

`output/` contains generated drafts, reports, briefs, bundles, and working artifacts. Output is not canonical context until reviewed and harvested.

## What belongs here

- generated drafts
- research briefs
- weekly reports
- campaign bundles
- meeting summaries pending review
- proposed updates before they become canonical context

## What does not belong here

- source of truth company rules
- final playbooks
- strategy decisions
- sensitive raw material

## Harvest rule

When output proves useful and repeatable, harvest it into:

- `wiki/` for playbooks and SOPs
- `.ai/skills/` for repeatable agent procedures
- `strategy/` for reviewed strategic insight
- `run/` for recurring operating processes
- `decisions/` for accepted choices

The owner's request to harvest is acceptance. Write harvested material as settled canonical statements, without `proposed` or `pending confirmation` hedges. Keep evidence-gathering notes where a claim genuinely still needs future data.

Complete every harvest by:

1. Setting the source draft's frontmatter to `status: read` and leaving it at `output/YYYYMMDD-topic.md`.
2. Adding a dated, newest-first entry to `company/changelog.md` that summarizes what was harvested and names its canonical destinations.

Place new output drafts directly in `output/` using `YYYYMMDD-topic.md`. Do not create nested draft folders.

## Prompts for operators

- Is this draft or canonical context?
- What parts should be harvested?
- Who needs to review it?
