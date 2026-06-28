---
owner: operator
status: template
last_updated: 2026-06-27
source_of_truth: company-os-starter-kit
load_policy: task
related:
  - /.templates/client-context.md
  - /AGENTS.md
  - /clients/AGENTS.md
---

# Clients

`clients/` holds per-client context so agents do not mix voices, ICPs, campaigns, constraints, or confidential assumptions.

## What belongs here

- client overview and engagement context
- client-specific voice, people involved, constraints, and preferences
- agreed scope and boundaries
- approved reusable client knowledge

## What does not belong here

- full raw client exports unless explicitly approved
- private credentials
- unreviewed transcripts
- another client's assumptions
- generated drafts that should live in `output/`

## Required shape

Create one folder per client directly under `clients/`. Do not create shared client context files at the root of `clients/` except `README.md` and `AGENTS.md`.

Each client folder should use a stable lowercase slug:

```text
clients/acme/
├── README.md
├── engagement.md
├── voice.md
└── constraints.md
```

Use `.templates/client-context.md` for the first client `README.md` unless a more specific approved template exists.

## Prompts for operators

- What must agents know before working for this client?
- What is confidential?
- What language, tone, or constraints are client-specific?
- What is the source of truth for project execution?
