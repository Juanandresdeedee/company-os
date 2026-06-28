---
owner: operator
status: template
last_updated: 2026-06-28
source_of_truth: company-os-starter-kit
load_policy: always
related:
  - /README.md
  - /AGENTS.md
---

# Content catalog

Use this file as the map of the Company OS. Update it when adding, moving, or retiring durable files.

## Root contracts

| File | purpose | owner | status | last updated | load policy |
| --- | --- | --- | --- | --- | --- |
| `README.md` | Company OS purpose, quick start, four-layer model, folder map | operator | template | 2026-06-28 | reference |
| `AGENTS.md` | Canonical model-agnostic agent guide | operator | template | 2026-06-27 | always |
| `CLAUDE.md` | Claude-specific entrypoint and compatibility notes | operator | template | 2026-06-27 | always |
| `ARCHITECTURE.md` | Systems of record, Company OS, read layer, operating surface | operator | template | 2026-06-27 | always |
| `GOVERNANCE.md` | PR workflow, ownership, harvest loop, guardrails | operator | template | 2026-06-27 | always |
| `INDEX.md` | Content catalog | operator | template | 2026-06-28 | always |
| `SKILLS.md` | Installation and authoring guide for repository-managed AI skills | operator | template | 2026-06-28 | reference |
| `CHANGELOG.md` | Human-reviewed notable changes for releases and project history | operator | template | 2026-06-28 | reference |
| `LICENSE` | MIT license terms for repository reuse | operator | template | 2026-06-28 | reference |
| `.gitignore` | Git ignore rules for local, editor, dependency, build, log, and cache files | operator | template | 2026-06-28 | reference |

## Folders

| Folder | purpose | owner | status | last updated | load policy |
| --- | --- | --- | --- | --- | --- |
| `company/` | Purpose, vision, values, structure, ICP, positioning, voice and market context | operator | template | 2026-06-27 | task |
| `strategy/` | Goal, today, analysis, thesis and tradeoffs | operator | template | 2026-06-27 | task |
| `run/` | Strategic processes, owners, cadence, metrics, systems of record | operator | template | 2026-06-27 | task |
| `change/` | Strategic projects, outcomes, owners, start and end dates, risks, and target operating changes | operator | template | 2026-06-27 | task |
| `wiki/` | SOPs, playbooks, onboarding, durable reference docs | operator | template | 2026-06-27 | reference |
| `clients/` | Per-client context and constraints | operator | template | 2026-06-27 | task |
| `clients/AGENTS.md` | Rules for client folder structure and context loading | operator | template | 2026-06-27 | always |
| `raw/` | Unprocessed source material | operator | template | 2026-06-27 | reference |
| `plugin/` | Agent commands, hooks, MCP setup, tool configs | operator | template | 2026-06-27 | reference |
| `workflows/` | Function-level operating guides | operator | template | 2026-06-27 | task |
| `decisions/` | ADR-style decisions | operator | template | 2026-06-27 | reference |
| `decisions/AGENTS.md` | Rules for creating and updating decisions | operator | template | 2026-06-27 | always |
| `output/` | Generated drafts, reports, briefs, bundles | operator | template | 2026-06-27 | reference |
| `archive/` | Retired material | operator | template | 2026-06-27 | archive |
| `.templates/` | Reusable document templates | operator | template | 2026-06-27 | reference |
| `.ai/skills/` | Company OS managed starter skills | operator | template | 2026-06-28 | task |

## Company context

| File | purpose | owner | status | last updated | load policy |
| --- | --- | --- | --- | --- | --- |
| `company/purpose.md` | Why the company exists | operator | draft | 2026-06-27 | task |
| `company/vision.md` | Future the company is trying to create | operator | draft | 2026-06-27 | task |
| `company/values.md` | Values that shape decisions | operator | draft | 2026-06-27 | task |
| `company/structure.md` | Company functions, ownership, communication routes and decision rights | operator | draft | 2026-06-27 | task |
| `company/icp.md` | Best-fit and bad-fit customers | operator | draft | 2026-06-27 | task |
| `company/positioning.md` | Category, promise, differentiation, alternatives | operator | draft | 2026-06-27 | task |
| `company/voice.md` | Tone, writing rules, banned phrases | operator | draft | 2026-06-27 | task |
| `company/terminology.md` | Canonical terms and definitions | operator | draft | 2026-06-27 | reference |
| `company/design-system.md` | Visual identity and design constraints | operator | draft | 2026-06-27 | reference |
| `company/market/README.md` | Guide for market context | operator | template | 2026-06-27 | reference |
| `company/market/intel.md` | Durable market context and buying signals | operator | draft | 2026-06-27 | reference |
| `company/market/competition.md` | Competitor categories and alternatives | operator | draft | 2026-06-27 | reference |

## Strategy, run, and change

| File | purpose | owner | status | last updated | load policy |
| --- | --- | --- | --- | --- | --- |
| `strategy/goal.md` | 12 to 36 month measurable milestone | operator | draft | 2026-06-27 | task |
| `strategy/today.md` | Honest diagnosis of where the company is now | operator | draft | 2026-06-27 | task |
| `strategy/analysis/` | Dated analysis documents for specific strategy questions | operator | template | 2026-06-27 | task |
| `strategy/analysis/README.md` | Guide for strategy analysis documents | operator | template | 2026-06-27 | task |
| `strategy/analysis/AGENTS.md` | Rules for strategy analysis files | operator | template | 2026-06-27 | always |
| `strategy/analysis/YYYYMMDD-title.md` | Template for dated analysis files | operator | template | 2026-06-27 | reference |
| `strategy/thesis.md` | Where we play, how we play, how we reach the goal | operator | draft | 2026-06-27 | task |
| `strategy/tradeoffs.md` | Deliberate compromises and rejected options | operator | draft | 2026-06-27 | task |
| `run/processes.md` | Strategic recurring processes with activity, quality and outcome metrics | operator | draft | 2026-06-27 | task |
| `run/cycles.md` | Long-term, annual, quarterly, monthly, weekly cycles | operator | draft | 2026-06-27 | task |
| `run/systems-of-record.md` | Systems that own live operational state | operator | draft | 2026-06-27 | reference |
| `change/projects.md` | Strategic change projects, portfolio status, project risks, dates, scope, resources, contributors, and milestones | operator | draft | 2026-06-27 | task |
| `change/lessons/` | Project reflections, lesson index, and harvest candidates linked to project records | operator | draft | 2026-06-27 | reference |
| `change/lessons/README.md` | Guide and index for project lessons and reflections | operator | draft | 2026-06-27 | reference |
| `change/lessons/YYYYMMDD-project-slug-reflection.md` | Template for a dated project reflection | operator | template | 2026-06-27 | reference |

## Templates and managed skills

| File | purpose | owner | status | last updated | load policy |
| --- | --- | --- | --- | --- | --- |
| `.templates/durable-doc.md` | Base durable document template | operator | template | 2026-06-27 | reference |
| `.templates/company-context.md` | Company context template | operator | template | 2026-06-27 | reference |
| `.templates/strategy.md` | Strategy template | operator | template | 2026-06-27 | reference |
| `.templates/process.md` | Run process template | operator | template | 2026-06-27 | reference |
| `.templates/project.md` | Change project template | operator | template | 2026-06-27 | reference |
| `.templates/playbook.md` | Wiki playbook template | operator | template | 2026-06-27 | reference |
| `.templates/workflow.md` | Function workflow template | operator | template | 2026-06-27 | reference |
| `.templates/client-context.md` | Client context template | operator | template | 2026-06-27 | reference |
| `.templates/decision.md` | ADR-style decision template | operator | template | 2026-06-27 | reference |
| `.templates/raw-ingestion-summary.md` | Raw source processing template | operator | template | 2026-06-27 | reference |
| `.templates/output-brief.md` | Generated output brief template | operator | template | 2026-06-27 | reference |
| `SKILLS.md` | Installation and authoring guide for repository-managed AI skills | operator | template | 2026-06-28 | reference |
| `.ai/skills/board-of-directors/SKILL.md` | Managed skill for board-style review of high-stakes company decisions and tradeoffs | operator | template | 2026-06-28 | task |
| `.ai/skills/company-purpose/SKILL.md` | Managed skill for company purpose interview and drafts | operator | template | 2026-06-27 | task |
