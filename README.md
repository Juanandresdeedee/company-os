---
owner: operator
status: template
last_updated: 2026-06-27
source_of_truth: company-os-starter-kit
load_policy: reference
related:
  - /AGENTS.md
  - /ARCHITECTURE.md
  - /GOVERNANCE.md
  - /SKILLS.md
---

# Company OS starter kit

This repository is a blueprint for an AI-first Company OS. It gives people and agents durable company context they can read, maintain and improve through version control.

Use markdown and config only. Do not add product code, app code, generated software, package manifests, Storybook files or runtime code unless the file only configures agent tools.

## What this is

A Company OS is the authored operating context of the business:

- who the company is
- why it exists
- what it believes
- how it makes strategic choices
- how it runs the current business
- how it changes the business
- how agents should safely use company context

The OS owns intent and operating rules. Live state belongs in systems of record such as CRM, Linear, GitHub Issues, accounting, analytics, calendar, Slack, or other operational tools.

## Four-layer model

1. Systems of record hold live operational state in purpose-built tools.
2. Company OS holds durable authored intent, governance, playbooks, skills, strategy and context in this repo.
3. The knowledge graph or read layer joins this repo with systems of record for search, retrieval and reasoning.
4. The operating surface is where AI tools, agents, Claude Code, assistants and human workflows act through approved systems.

## Start here

1. Read `AGENTS.md` to understand how agents should navigate this repo.
2. Fill `company/README.md` prompts first, especially purpose, vision, values, structure, ICP, positioning, market and voice.
3. Fill `strategy/README.md` next: goal, today, analysis, thesis and tradeoffs.
4. Define current operating processes in `run/`.
5. Define transformation projects in `change/`.
6. Use `.ai/skills/company-purpose/SKILL.md` to guide the first company-purpose interview.
7. Read `SKILLS.md` to install or update repository-managed skills in local AI tools.
8. Keep generated drafts in `output/` until they are explicitly harvested into canonical context.

## Folder map

| Folder | purpose |
| --- | --- |
| `company/` | Purpose, vision, values, structure, ICP, positioning, voice, terminology, design system and market context. |
| `strategy/` | Goal, today, analysis, thesis and tradeoffs. |
| `run/` | Strategic processes derived from the thesis, with owners, cadence, metrics, review rituals, and systems of record. |
| `change/` | Strategic projects derived from the thesis, each with outcome, owner, deadline, metric, and target operating change. |
| `wiki/` | SOPs, playbooks, onboarding, recurring processes, and durable reference docs. |
| `clients/` | One folder per client, with per-client context templates so agents do not mix voices, ICPs, campaigns, constraints, or confidential assumptions. |
| `raw/` | Transcripts, research dumps, exports, notes, and other unprocessed source material. |
| `plugin/` | Agent commands, hooks, safety rules, MCP setup notes, and tool integration configs. |
| `workflows/` | Function-level operating guides for sales, marketing/GTM, product, delivery, ops, and finance. |
| `decisions/` | ADR-style context, decision, consequences, and supersession records. |
| `output/` | Generated drafts, reports, briefs, and bundles; never canonical context. |
| `archive/` | Retired material excluded from default agent loading. |
| `.templates/` | Reusable templates for all major document types. |
| `.ai/skills/` | Company OS managed starter skills for operators and future CLI tooling. |

## Metadata

Durable markdown files should use this frontmatter:

```yaml
owner:
status:
last_updated:
source_of_truth:
load_policy:
related:
```

Allowed `load_policy` values:

- `always`: load before most work.
- `task`: load when the task matches this area.
- `reference`: load only when needed.
- `archive`: do not load by default.
- `never`: never load into agent context without explicit human approval.

## Operating rule

If an agent learns something durable, do not leave it only in chat memory. Propose an update to the relevant company, strategy, run, change, wiki, skill, or decision file.
