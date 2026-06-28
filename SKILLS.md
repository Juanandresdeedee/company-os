---
owner: operator
status: template
last_updated: 2026-06-28
source_of_truth: company-os-starter-kit
load_policy: reference
related:
  - /.ai/skills/README.md
  - /.ai/skills/board-of-directors/SKILL.md
  - /.ai/skills/company-purpose/SKILL.md
  - /AGENTS.md
  - /CLAUDE.md
---

# Skills

This repository keeps Company OS managed starter skills in `.ai/skills/`.

Skills are authored here as durable company assets. Local AI tools may need a copy or symlink in their own skills directory before they can discover and run them.

## Available skills

| Skill | source | purpose |
| --- | --- | --- |
| `board-of-directors` | `.ai/skills/board-of-directors/SKILL.md` | Board-style review for high-stakes founder/operator decisions, strategy, finance, risk, governance, customer, and operations tradeoffs. |
| `company-purpose` | `.ai/skills/company-purpose/SKILL.md` | Guided interview for purpose, vision, values, principles, strategic ambition, and a 12 to 36 month goal. |

## Suggested external skills

These skills are not stored in this repository, but they pair well with Company OS work:

| Skill | source | use when |
| --- | --- | --- |
| `llm-council` | `tenfoldmarc/llm-council-skill` | You need to pressure-test a meaningful strategy, positioning, prioritization, or operating decision from multiple angles. |

## Install for Codex

Install all repository-managed skills into the local Codex skills directory:

```sh
mkdir -p "$HOME/.codex/skills"

for skill in .ai/skills/*; do
  [ -d "$skill" ] || continue
  [ -f "$skill/SKILL.md" ] || continue

  name="$(basename "$skill")"
  dest="$HOME/.codex/skills/$name"

  if [ -e "$dest" ]; then
    echo "skip $name: already installed at $dest"
  else
    cp -R "$skill" "$dest"
    echo "installed $name to $dest"
  fi
done
```

Restart Codex after installing or updating skills so the app reloads available skill metadata.

To install only one skill:

```sh
mkdir -p "$HOME/.codex/skills"

name="board-of-directors"

if [ -e "$HOME/.codex/skills/$name" ]; then
  echo "skip $name: already installed"
else
  cp -R ".ai/skills/$name" "$HOME/.codex/skills/$name"
fi
```

To install the suggested external LLM Council skill:

```sh
python3 "$HOME/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py" \
  --repo tenfoldmarc/llm-council-skill \
  --path . \
  --name llm-council-skill
```

## Update installed skills

Treat `.ai/skills/` as the source of truth. When a skill changes in this repository, reinstall it into the tool-specific skills directory or replace the installed copy after reviewing local changes.

If you customize a skill for personal use, keep the customized copy outside this repository or propose the durable improvement through the harvest loop in `AGENTS.md`.

## Authoring rules

- Each skill lives in `.ai/skills/<skill-name>/`.
- Each skill folder must contain `SKILL.md`.
- Use frontmatter with `name`, `description`, `version`, `category`, `managed_by`, `owner`, `status`, `last_updated`, `source_of_truth`, `load_policy`, and `related`.
- Keep skills blueprint-owned and reusable; do not store client-confidential material, secrets, generated drafts, or one-off personal prompts in managed skills.
- When adding, moving, or retiring skills, update this file, `.ai/skills/README.md`, and `INDEX.md`.
