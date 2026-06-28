---
owner: operator
status: template
last_updated: 2026-06-27
source_of_truth: company-os-starter-kit
load_policy: reference
related:
  - /CLAUDE.md
  - /GOVERNANCE.md
---

# Plugin

`plugin/` contains agent commands, hooks, safety rules, MCP setup notes, and tool integration configs. It is for agent tooling configuration only.

## What belongs here

- command definitions
- hook documentation
- safety policies
- MCP setup notes
- tool integration config docs

## What does not belong here

- product code
- app code
- runtime package manifests
- private credentials
- generated software

## Prompts for operators

- What tools may agents read from?
- What tools may agents write to?
- Which actions require approval?
- Which hooks protect against unsafe behavior?
