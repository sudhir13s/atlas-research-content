# Standard: Portable Content Repos (`atlas-<domain>-content`)

> The canonical contract for every `atlas-<domain>-content` knowledge repository and for every
> project or AI agent that consumes one. These repos hold **content only** — Markdown + JSON
> Schema + docs, **zero code** — so they can be vendored into any project and navigated by a
> human or an agent with no external context. This document is the single source of truth; a repo
> that diverges from it is non-conformant.

## 1. Purpose and principles

`atlas-<domain>-content` repos exist to hold **durable, reusable AI reference knowledge** (models,
hardware, evaluation, licenses, frameworks) as portable data. The library is authored once and
reused across many projects; TheAIAtlas is only the first consumer.

Five principles, non-negotiable:

1. **Content only, zero code.** No `.js`, `.ts`, `.mjs`, no `package.json`, no build scripts, no
   CI code inside the repo. Only Markdown, JSON Schema (`.json`), SVG assets, and Markdown docs.
   All executable tooling lives in the *consuming* project (for TheAIAtlas: `packages/atlas-content`).
2. **Self-describing.** Two machine entrypoints (`meta.json`, `schema/registry.json`) plus human
   docs let any reader — person or agent — discover, understand, validate, and extend the repo
   from the repo alone.
3. **Dual-audience.** Every convention serves a human author *and* an automated agent identically.
   Structure is predictable, IDs are stable, relationships are explicit and resolvable.
4. **Portable and versioned.** `schema_version` per file + repo semver tags + `CHANGELOG` + `LICENSE`.
   A consumer pins a tag and vendors the repo; nothing couples it to a specific consumer.
5. **Source-of-truth is the Markdown.** Any JSON a consumer builds from these files is derived
   state, rebuildable from the Markdown alone. The repo never contains derived/compiled output.

## 2. Repository skeleton

Every `atlas-<domain>-content` repo has the identical top-level shape. `<type>` folders and file
names vary per domain; everything else is fixed.

```
atlas-<domain>-content/
├── README.md              # HUMAN entrypoint: what it is, structure map, quick start, contributing
├── AGENTS.md              # AGENT entrypoint: how to discover / read / validate / extend programmatically
├── CONVENTIONS.md         # BOTH: the rules — slugs, frontmatter, body sections, IDs, relationships
├── CHANGELOG.md           # human-readable change log, grouped by schema_version / release
├── LICENSE                # reuse terms (so other projects can legally vendor the content)
├── meta.json              # MACHINE ENTRYPOINT 1 — repo descriptor
├── schema/                # declarative JSON Schema (draft 2020-12) — NOT code
│   ├── registry.json      # MACHINE ENTRYPOINT 2 — type → {folder, schema, id_prefix, sections}
│   ├── _shared.schema.json# shared $defs (source, provenance, enums)
│   └── <type>.schema.json # one per content type
├── templates/             # copy-to-author: one template per type
│   └── <type>.template.md
├── <type-folder>/         # one folder per content type; files are <slug>.md
│   └── <slug>.md          # a `dated` type adds <year>/<month>/ folders, see section 3.3
└── assets/                # SVG diagrams referenced by frontmatter *_url fields
    └── <...>.svg
```

## 3. The two machine entrypoints

An agent reads these two files first and then knows how to handle the whole repo.

### 3.1 `meta.json` — repo descriptor

Small, stable, non-drifting (no counts). Declares what the repo is and where its contract lives.

```json
{
  "name": "atlas-models-content",
  "domain": "models",
  "title": "AI Models — reference knowledge",
  "schema_version": "1.0",
  "description": "Portable reference knowledge for AI models: catalog cards, architecture eras, parameters, hyperparameters, fine-tuning methods, licenses.",
  "entrypoints": {
    "human": "README.md",
    "agent": "AGENTS.md",
    "conventions": "CONVENTIONS.md",
    "registry": "schema/registry.json"
  },
  "types": ["model", "architecture-era", "parameter", "parameter-calculator", "hyperparameter", "fine-tuning-method", "license", "task-group", "task"],
  "license": "CC-BY-4.0"
}
```

### 3.2 `schema/registry.json` — type map

Maps every content `type` to its folder, its schema, its ID prefix, and its **required body
sections**. One read gives an agent the complete authoring/validation contract.

```json
{
  "schema_version": "1.0",
  "shared": "schema/_shared.schema.json",
  "types": {
    "hyperparameter": {
      "folder": "hyperparameters",
      "schema": "schema/hyperparameter.schema.json",
      "id_prefix": "hyperparameter/",
      "sections": ["Definition", "What to look for", "Calculation", "Example"]
    }
  }
}
```

### 3.3 Folder layout of a type: flat or dated

Each registry entry may carry an optional `layout`. Without it the layout is flat.

| Layout | Where a file lives | Used for |
|---|---|---|
| flat (default) | `<folder>/<slug>.md` | Reference records that stay few and are looked up by name |
| `dated` | `<folder>/<year>/<month>/<slug>.md` | Records that accumulate without end, such as the feed |

- **A dated type** has the year and month taken from the record's own date (for a feed item, its UTC publication day), never from the day it was written, so a record's place never changes on a rerun.
- **A record with no date** is filed under `<folder>/undated/<slug>.md`.
- **The slug stays unique across the whole type,** whatever the folders; the ID is still `<type>/<slug>` and does not contain the date folders.
- **Example:** `atlas-news-content` declares the `feed-item` type with `"folder": "feed"` and `"layout": "dated"`, so an item is stored at `feed/2026/11/<slug>.md`. Its slug is the publication date, the title words and 8 hex characters of the URL's hash, so the same item always maps to the same file.

## 4. File contract

### 4.1 Base frontmatter (every file, every domain)

```yaml
---
id: hyperparameter/learning-rate     # STABLE, globally unique = "<type>/<slug>". Never changes.
type: hyperparameter                 # the discriminator; must be a key in registry.json → types
slug: learning-rate                  # lowercase, hyphen-separated, ASCII; == filename (without .md)
schema_version: 1.0                  # the schema major.minor this file was authored against
title: "Learning Rate"               # human-readable
tags: [training, optimization]       # lowercase, hyphen-separated
updated: 2026-07-16                  # ISO date of last edit
sources:                             # provenance; open-source-first, cite don't copy
  - url: https://arxiv.org/abs/2001.08361
    title: "Scaling Laws for Neural Language Models"
    trust: 0.9
related: [hyperparameter/effective-batch-size]   # OPTIONAL; resolvable IDs, never titles
---
```

**Mandatory base fields:** `id`, `type`, `slug`, `schema_version`, `title`, `tags`, `updated`,
`sources`. **Optional:** `related`. Each `type` extends this base with its own required fields
(defined in `schema/<type>.schema.json`).

### 4.2 Body sections

Prose lives in the Markdown body under `##` headings. The **required sections per type** are
declared in `registry.json` and enforced by the consumer's validator. Sections appear in the
declared order. Reference-heavy structured data (arrays, matrices, config) lives in **frontmatter**,
not prose, so it stays machine-parseable; the body carries explanation, formulas, and worked
examples.

### 4.3 IDs and relationships

- **`id` is `<type>/<slug>` and is immutable.** Renaming a file changes the `slug`/`id`; treat that
  as a breaking change (add a redirect note in `CHANGELOG`, update referrers).
- **All cross-references use IDs, never titles** (`related`, and any domain-specific link fields
  such as `led_to`, `influenced_by`, `models_using`). This keeps the graph resolvable and lets the
  consumer detect dangling references.
- **A reference may point into another content repo** (a task's `benchmarks` are
  `benchmark/<slug>` IDs from the evaluation repo); the consumer resolves IDs across every mounted
  repo.

## 5. Validation

- The **JSON Schema lives in the repo** (`schema/`), so the contract travels with the content and
  any consumer validates against the same source.
- **Validation runs in the consumer**, not the repo (the repo has no code). For TheAIAtlas, the
  loader in `packages/atlas-content` validates every file's frontmatter against its type schema and
  checks that every relationship ID resolves, on every load and before every automatic commit.
- A file that fails schema validation or has a dangling reference fails the load, and the error
  names the file.

## 6. Consumption and git-submodule mechanics

- Each repo is mounted in a consumer as a **git submodule** (TheAIAtlas: `content/<domain>-src/`),
  **pinned by commit SHA** — never branch-tracked at build time (reproducible builds).
- **Two kinds of change reach a content repo:**
  - **By hand:** author in the content repo, validate, commit. Fields written by hand are marked
    locked, and automated writers never overwrite them.
  - **By a scheduled job:** the consumer's job works in its own clone of the repo (for TheAIAtlas,
    `runtime/content/<repo>`), never inside the submodule checkout. It validates each record before
    writing, writes only files that differ, never deletes, and commits once per run. Each commit
    records the job, the run, the models and the prompt versions that produced it, so it can be
    traced and rolled back. The push is never forced.
- **Where the database is rebuilt from:** the consumer's loader reads either the pinned submodules
  or the jobs' clones. Because jobs push to the repo's main branch and the pin moves only at
  release, the clones are the current state and the pins are the reproducible one.
- **Pin bumps** in the consumer are ordinary changes to the consumer. `git show --stat` on a pin
  bump must show exactly one `Subproject commit` line.

## 7. Versioning and reuse

- **`schema_version`** is per file and mirrored in `meta.json`/`registry.json`. Bump the minor for
  additive fields, the major for breaking changes; record both in `CHANGELOG.md`.
- **Repo semver tags** mark releases; a consumer pins a tag/SHA and vendors the repo.
- **`LICENSE`** governs reuse. Content is open-source-first and citation-based (see the global
  open-source-first rule); the default content license is `CC-BY-4.0` unless a repo states otherwise.

## 8. Authoring workflow (human or agent)

1. Read `meta.json` → `schema/registry.json` to learn the types, folders, and section contracts.
2. Copy `templates/<type>.template.md`.
3. Fill the frontmatter (base + type-specific) and the required body sections; use IDs for links.
4. Validate against `schema/<type>.schema.json` (the consumer's validator, or any JSON Schema runner).
5. Ensure every referenced ID resolves to an existing file.
6. Commit to the content repo; the consumer then bumps its submodule pin.

## 9. Conformance checklist

- [ ] Only Markdown, JSON Schema, SVG, and Markdown docs — no code files.
- [ ] `meta.json` and `schema/registry.json` present and mutually consistent.
- [ ] Every content file carries the full base frontmatter with a stable `<type>/<slug>` `id`.
- [ ] Every `type` has a schema, a template, and declared required sections.
- [ ] All relationships use resolvable IDs; no dangling references.
- [ ] `README.md`, `AGENTS.md`, `CONVENTIONS.md`, `CHANGELOG.md`, `LICENSE` present.
