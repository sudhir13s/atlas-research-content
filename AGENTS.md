# AGENTS.md — machine navigation guide

This repository is designed to be read and extended by AI agents with **no external context**.
Follow these steps.

## 1. Orient

1. Read [`meta.json`](meta.json) — the repo descriptor. It gives `domain`, `schema_version`, the
   list of content `types`, and pointers to the human/agent/convention docs and the registry.
2. Read [`schema/registry.json`](schema/registry.json) — the type map. For each `type` it gives:
   - `folder` — where files of that type live
   - `schema` — the JSON Schema that validates that type's frontmatter
   - `id_prefix` — the stable-ID namespace (`<type>/`)
   - `sections` — the required Markdown body sections, in order
   - `optional_sections` — body sections that may be absent

After these two reads you know every type, where it lives, how to validate it, and how it must be
structured.

## 2. Discover content

Two equivalent ways to enumerate the library:

- **Glob**: read every `**/*.md`, parse its YAML frontmatter, key on `id` / `type`.
- **By type**: for a known `type`, list its `folder` from the registry and read each `<slug>.md`.
  A `dated` type (`feed-item`) files its records at `feed/<year>/<month>/<slug>.md`.

Every file self-identifies via frontmatter (`id`, `type`, `slug`, `title`, `tags`, ...), so no
separate index is needed and none can fall out of sync.

## 3. Read a file

- **Frontmatter** carries the structured data (all fields the schema defines). Parse it as YAML.
- **Body** carries prose under `##` headings matching the type's `sections`.
- **Links** are **IDs** of the form `<type>/<slug>`. Resolve them to files by matching `id`.
  Cross-reference fields in this domain: `topics` on a paper (→ `research-topic/<slug>`) and
  `related`. `url`, `links[].url` and `sources[].url` are web addresses, not cross-references.
- **Lists** (the must-read list, a topic's papers) are not stored: filter papers by `must_read`
  and sort by `must_read.order`, or filter by `topics`.

## 4. Validate

- Load the type's schema from `schema/<type>.schema.json` (shared `$defs` in `schema/_shared.schema.json`).
- Validate the file's frontmatter against it (any JSON-Schema draft-2020-12 validator, e.g. `ajv`).
- Check that every referenced ID resolves to an existing file (no dangling references).

## 5. Add or edit content

1. Pick the `type`; copy `templates/<type>.template.md`.
2. Set `id` = `<type>/<slug>`, `slug` = filename, `schema_version` to the constant the type's
   schema states (`3.0`, as in `meta.json`; `2.0` for `feed-item`), and `updated` to today's date.
3. Fill the type-specific frontmatter fields (schema `required` first) and every required body
   section in order.
4. Use IDs for all cross-references; create or reference the target files so nothing dangles.
5. Validate (step 4 above). Do not introduce code files — this repo is content-only.
6. Follow open-source-first sourcing: cite sources in `sources[]`; never copy paywalled text.

## 6. Invariants (do not violate)

- `id` is immutable; renaming a slug is a breaking change (note it in `CHANGELOG.md`).
- No `.js` / `.ts` / `.mjs` / `package.json` / build scripts anywhere.
- All links are IDs, never titles.
- One record per distinct paper: a paper listed under several topics is one file with several `topics`.
- Frontmatter must pass the type schema before a change is complete.
