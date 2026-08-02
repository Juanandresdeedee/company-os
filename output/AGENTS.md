---
owner: operator
status: accepted
last_updated: 2026-08-02
source_of_truth: company-os-starter-kit
load_policy: always
related:
  - /AGENTS.md
  - /output/README.md
---

# Output naming and structure rules

These rules apply to everything under `output/`.

## File naming

1. Name every generated file `YYYYMMDD-{topic}.md`, for example `20260708-weekly-report.md`.
2. Use the creation date as the `YYYYMMDD` stamp so any file's origin date is readable from its name.
3. Use a short, lowercase, hyphenated `{topic}` slug: `20260708-shugyo-landing-copy.md`.
4. The stamp is the date the artifact was created; do not restamp on later edits.

## Placement

- Write new dated files directly in `output/` as single files or dated bundles (a lead file plus an artifacts directory).
- Do not create category or working subfolders for new output.
- `README.md` files are exempt from the date stamp.

## Single file vs bundle

- A small, single-artifact output stays a single dated file.
- When an output has more than one part (an artifact plus appendices, review notes, or harvest candidates), create a bundle: a dated lead file plus an artifacts directory.

## Bundle structure

Separate the request and inputs from the generated output. A bundle is two things, side by side:

```text
output/
|-- YYYYMMDD-{topic}.md      # lead file: meta, no generated content
`-- YYYYMMDD-{topic}/        # artifacts directory: generated content only
    |-- {artifact}.md
    `-- {appendix}.md
```

The lead file `YYYYMMDD-{topic}.md` contains, in this order:

| Section | Content |
| --- | --- |
| Artifacts | A table linking every file in the artifacts directory with a one-line description. |
| Request | What was asked. |
| Inputs | Sources used (Company OS files, transcripts, external references, role models). |
| Review notes | What needs human review before publishing or harvesting. |
| Harvest candidates | What may be promoted into canonical context (`company/`, `strategy/`, `wiki/`, `run/`, `decisions/`). |

The artifacts directory `YYYYMMDD-{topic}/` contains only generated artifacts: one artifact per file, short lowercase-hyphenated names without a date stamp (the directory carries the stamp).

Rules:

1. The lead file carries all meta; artifact files carry only generated content. Never mix the two.
2. The lead file must reference the artifacts directory and list every artifact in it.
3. Cross-reference with relative links: lead to artifact `[card](YYYYMMDD-{topic}/card.md)`, artifact to artifact `[appendix](appendix.md)`.
4. Each file keeps its own frontmatter (`owner`, `status`, `last_updated`, `source_of_truth`, `load_policy`, `related`).
5. When an output grows from a single file into a bundle, keep the original date stamp: the single file becomes the lead file and the generated content moves into the artifacts directory.
