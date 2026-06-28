---
owner: operator
status: template
last_updated: 2026-06-27
source_of_truth: company-os-starter-kit
load_policy: always
related:
  - /README.md
  - /AGENTS.md
  - /GOVERNANCE.md
---

# Architecture

The Company OS separates live state, durable intent, retrieval, and action. AI-first operations require all four layers to be explicit.

## Layer 1 systems of record

Systems of record hold mutable operational state:

- CRM owns contacts, accounts, pipeline, and sales activity.
- Linear or GitHub Issues owns task execution.
- Accounting owns financial state.
- Analytics owns product, funnel, and process metrics.
- Calendar, Slack, email, and support tools own communication history.

Do not duplicate live state into this repo unless the file is a snapshot or summary with a clear timestamp and source.

## Layer 2 Company OS

This repository owns durable authored intent:

- purpose, vision, values, principles
- structure, ICP, positioning, voice
- strategy, thesis, tradeoffs, goals
- run processes and change projects
- playbooks, SOPs, skills, workflows
- decisions and governance

The OS should explain why work matters, how the company chooses, and how agents should act.

## Layer 3 read layer

The read layer joins this repo with systems of record. It may be a future knowledge graph, search index, vector store, catalog, or retrieval service.

The read layer is not the source of truth. It is an access layer over sources that remain authoritative in their own domains.

## Layer 4 operating surface

The operating surface is where humans and agents work:

- Claude Code and other AI coding and agent tools
- assistants connected to CRM, docs, analytics, and Slack
- scheduled jobs, monitors, and workflow automations
- human review through branches and PRs

Agents should read this OS, retrieve live state from systems of record when allowed, act through approved tools, and propose durable updates through governance.

## Run and change

The OS distinguishes two operating modes:

- `run/`: how the current business operates, measured by processes, owners, cadence, and metrics.
- `change/`: how the business transforms, measured by project outcomes and target operating changes.

Every change project should either create, remove, or improve a run process. Every run process should be observable.
