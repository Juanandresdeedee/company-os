---
owner: operator
status: template
last_updated: 2026-06-27
source_of_truth: company-os-starter-kit
load_policy: task
related:
  - /strategy/README.md
  - /.ai/skills/company-purpose/SKILL.md
---

# Company

`company/` is the company context layer. It explains why the company exists, who it serves, how it is positioned, how it is structured and how it speaks.

## What belongs here

- purpose, vision, values, and principles
- company structure and ownership context
- ICP, positioning, category, offers, and terminology
- voice, tone, writing rules, and brand constraints
- design system and visual identity notes
- market context in `market/`

## What does not belong here

- live pipeline or account state
- generated marketing drafts
- temporary strategy notes
- client-confidential raw material
- product code or app code

## Recommended files

- `purpose.md`
- `vision.md`
- `values.md`
- `structure.md`
- `icp.md`
- `positioning.md`
- `voice.md`
- `terminology.md`
- `design-system.md`
- `market/README.md`
- `market/intel.md`
- `market/competition.md`

## Prompts for operators

- Why does this company deserve to exist beyond making money?
- What future are we trying to create?
- What values create real tradeoffs in decisions?
- Who do we serve best, and who should we avoid?
- What language should agents use or avoid?
- What would make generated output feel obviously off-brand?

## Metadata

Use durable-doc frontmatter on every non-README file:

```yaml
owner:
status:
last_updated:
source_of_truth:
load_policy: task
related:
```
