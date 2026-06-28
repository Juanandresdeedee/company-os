---
owner: operator
status: template
last_updated: 2026-06-27
source_of_truth: company-os-starter-kit
load_policy: always
related:
  - /AGENTS.md
  - /clients/README.md
  - /.templates/client-context.md
---

# Client context rules

These rules apply to everything under `clients/`.

## Structure

1. Keep one direct child folder per client.
2. Use stable lowercase folder slugs, with hyphens when needed: `clients/acme-health/`.
3. Do not put durable client context files directly in `clients/` except `README.md` and this file.
4. Start each client folder with a `README.md` based on `.templates/client-context.md`.
5. Put client-specific engagement, voice, constraints, stakeholders, and reusable approved knowledge inside that client's folder.

## Loading

- For client-specific work, read `clients/README.md`, this file, and exactly one client folder before acting.
- Do not load multiple client folders unless the user explicitly asks for comparison or cross-client synthesis.
- If the target client is unclear, ask before loading client context.

## Boundaries

- Do not generalize client-confidential information into company, wiki, workflow, or public playbook files unless it is anonymized and approved.
- Keep raw exports, unreviewed transcripts, credentials, and sensitive source material out of canonical client context.
- Generated client drafts belong in `output/` until reviewed and harvested.
