---
owner: operator
status: template
last_updated: 2026-07-11
source_of_truth: company-os-starter-kit
load_policy: reference
related:
  - /AGENTS.md
  - /ARCHITECTURE.md
  - /GOVERNANCE.md
  - /company/changelog.md
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

```text
company-os-starter-kit/
|-- company/                 # Purpose, vision, values, structure, ICP, positioning, voice, terminology and design system.
|   `-- market/              # Market context, buying signals, competitors and alternatives.
|-- strategy/                # Goal, today, thesis, tradeoffs and strategy analysis.
|   `-- analysis/            # Dated analysis documents for specific strategy questions.
|-- run/                     # Strategic processes with owners, cadence, metrics, rituals and systems of record.
|-- change/                  # Strategic projects, outcomes, risks, owners, dates and target operating changes.
|   `-- lessons/             # Project reflections, lesson index and harvest candidates.
|-- wiki/                    # SOPs, playbooks, onboarding and durable reference docs.
|-- clients/                 # One folder per client; keep context, constraints and confidential assumptions separated.
|-- workflows/               # Function-level guides for sales, marketing/GTM, product, delivery, ops and finance.
|-- decisions/               # ADR-style decision records, consequences and supersession history.
|-- raw/                     # Transcripts, research dumps, exports, notes and other unprocessed source material.
|-- output/                  # Generated drafts, reports, briefs and bundles; never canonical context.
|-- plugin/                  # Agent commands, hooks, safety rules, MCP setup notes and tool integration configs.
|-- .templates/              # Reusable templates for all major document types.
|-- .ai/
|   `-- skills/              # Company OS managed starter skills for operators and future CLI tooling.
`-- archive/                 # Retired material excluded from default agent loading.
```

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

This block is required on every canonical markdown file, including wiki and brand files. Convert legacy metadata to this format when harvesting migrated material.

Allowed `load_policy` values:

- `always`: load before most work.
- `task`: load when the task matches this area.
- `reference`: load only when needed.
- `archive`: do not load by default.
- `never`: never load into agent context without explicit human approval.

## Operating rule

If an agent learns something durable, do not leave it only in chat memory. Propose an update to the relevant company, strategy, run, change, wiki, skill, or decision file.

## Two changelogs

The root `CHANGELOG.md` records changes to the starter-kit repository itself, including structure, templates, skills, tooling, and releases. `company/changelog.md` records changes and refinements the company decided to make to its context. Formal decisions still belong in `decisions/`; the company changelog provides the readable timeline.
