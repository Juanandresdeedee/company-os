---
owner: operator
status: template
last_updated: 2026-06-27
source_of_truth: company-os-starter-kit
load_policy: reference
related:
  - /output/README.md
  - /.templates/raw-ingestion-summary.md
---

# Raw

`raw/` stores unprocessed source material: transcripts, research dumps, exports, notes, and other inputs that may later become curated context.

## What belongs here

- meeting transcripts
- research dumps
- CSV or markdown exports
- pasted notes
- unprocessed source documents

## What does not belong here

- canonical company rules
- reviewed playbooks
- generated final drafts
- secrets or credentials
- sensitive raw material without clear access rules

## Processing rule

Raw material is not canonical context. Convert it into:

- `output/` for generated summaries
- `decisions/` for accepted choices
- `strategy/` for reviewed strategic insights
- `wiki/` for reusable playbooks
- `.ai/skills/` for repeatable procedures

## Prompts for operators

- What source produced this material?
- What is the timestamp?
- What can be safely harvested?
- What should remain private or temporary?
