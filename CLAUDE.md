---
owner: operator
status: template
last_updated: 2026-06-27
source_of_truth: company-os-starter-kit
load_policy: always
related:
  - /AGENTS.md
  - /plugin/README.md
  - /SKILLS.md
  - /.ai/skills/company-purpose/SKILL.md
---

# Claude Code entry point

Claude-specific guidance lives here. The canonical agent rules are in `AGENTS.md`; read that file first and treat it as authoritative.

## Claude Code conventions

- Use `AGENTS.md` for navigation, hard rules, source of truth boundaries, and task-specific context loading.
- Use `SKILLS.md` for installing and updating Company OS managed skills, and `.ai/skills/` for the skill source files.
- Use `plugin/` for Claude Code commands, hooks, MCP setup notes, and safety guardrails.
- Do not add product code or app code to this repository.
- When producing drafts, briefs, or reports, write them to `output/` unless the user explicitly asks to update canonical context.

## Skills

Start with:

- `SKILLS.md`: install and update instructions for repository-managed skills.
- `.ai/skills/company-purpose/SKILL.md`: guided interview for purpose, vision, values, principles, strategic ambition and a 12 to 36 month goal.

## Safety

Ask for approval before external sends, deletes, deploys, money movement, credential changes, or client-confidential sharing. If a hook or command policy conflicts with `AGENTS.md`, follow `AGENTS.md` and propose a governance update.
