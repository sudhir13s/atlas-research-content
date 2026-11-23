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
└── assets/                # SVG diagrams referenced by frontmatter `figures[].asset` fields
    └── <...>.svg
```

### Which repository holds a record

- **One repository per top tab:** models, evaluation, frameworks, hardware (Compute), research, news.
- **A record lives in the repository of the tab that shows it,** whatever job writes it: Research → Recent Papers reads `feed-item` records of kind `paper` from the research repo, News → Headlines reads kind `news` from the news repo.
- **A new record type goes into the repository of its tab;** the same type may be registered in more than one repo (`feed-item` is), as long as record IDs stay unique.
- **A new repository is created only for a new top tab.**

## 3. The two machine entrypoints

An agent reads these two files first and then knows how to handle the whole repo.

### 3.1 `meta.json` — repo descriptor

Small, stable, non-drifting (no counts). Declares what the repo is and where its contract lives.

```json
{
  "name": "atlas-models-content",
  "domain": "models",
  "title": "AI Models — reference knowledge",
  "schema_version": "3.1",
  "description": "Portable reference knowledge for AI models: catalog cards, architecture eras, parameters, hyperparameters, fine-tuning methods, licenses.",
  "entrypoints": {
    "human": "README.md",
    "agent": "AGENTS.md",
    "conventions": "CONVENTIONS.md",
    "registry": "schema/registry.json"
  },
  "types": ["model", "organization", "architecture-era", "parameter", "parameter-calculator", "hyperparameter", "fine-tuning-method", "license", "task-group", "task", "concept", "milestone", "quantization-topic"],
  "license": "CC-BY-4.0"
}
```

### 3.2 `schema/registry.json` — type map

Maps every content `type` to its folder, its schema, its ID prefix, and its **required body
sections**. One read gives an agent the complete authoring/validation contract.

```json
{
  "schema_version": "3.1",
  "shared": "schema/_shared.schema.json",
  "types": {
    "hyperparameter": {
      "folder": "hyperparameters",
      "schema": "schema/hyperparameter.schema.json",
      "id_prefix": "hyperparameter/",
      "sections": ["Definition"],
      "optional_sections": ["How It Works", "Calculation", "Worked Example", "What To Watch"]
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
schema_version: 3.1                  # the one value the type's schema allows; any other is refused
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

**Optional sections** (`optional_sections`) may be absent; those present keep their declared place
after the required ones. The `model` type is the example of a record whose whole body is optional
(models schema 3.0):

- **Five passages, each a frontmatter field only.** `summary`, `intended_use`, `what_sets_it_apart`,
  `running_it` and `limitations` live in the frontmatter; the body never repeats them.
- **Hand-written long form stays in the body.** A record a person wrote may keep the sections
  Summary, Why It Matters and Notes; no job writes them.
- **A passage the model card cannot support is absent.** It has no field; the word `unknown` is
  never stored.
- **`quotes` keeps the evidence.** It maps each written passage's field name to the one span of the
  model card the passage rests on.
- **`model_category` and `model_kind` are two fields.** The first says what the model is for (nine
  values), the second how it is built (nine kinds: `transformer-language`, `transformer-vision`,
  `multimodal`, `convolutional`, `diffusion`, `audio-speech`, `embedding`, `tabular-time-series`,
  `control-policy`). The kind decides which architecture blocks the schema allows: a
  `transformer-language` record states a `fingerprint` unless its repository is gated; a
  `convolutional` record has a `pipeline` and no `fingerprint`, `moe_config` or
  `context_window_tokens`; only an `embedding` record has `embedding_dimension`; only an
  `audio-speech` record has `fingerprint.input_stem`.
- **Mixture of experts is one stored statement,** `filters.is_moe`; `moe_config` exists only when it
  is true.
- **Each fact is stored once.** The context window and active parameters are top-level fields, the
  attention type is in `fingerprint` only, and the release year and month are read from
  `release_date`.

#### A record of lists with one optional passage: the `atlas-weekly-issue` type (added in news schema 1.2)

- **Structured lists in frontmatter.** `sections` holds `{title, total, items}`; each item is a title
  and a `url` (outside page) or a `record` (`<type>/<slug>`, a library record that may live in another
  repository), plus an optional `source`, `note` and `group`. Code copies every list from the stores.
- **The only body section is `## Introduction`, and it is optional** (`"sections": []`,
  `"optional_sections": ["Introduction"]`). It is absent when no model text passed review, and
  `generated_by` then names the job and run only.
- **One record per ISO week:** the flat file `issues/<YYYY>-w<WW>.md`; a week is written once.

#### A record whose fields follow who wrote it: the `feed-item` type (schema 2.0)

One news item, newsletter issue or recent paper. The news and research repos both register the
type from one shared definition (`feed_item` in each repo's `_shared.schema.json`).

- **On every item:** `kind`, `url`, `source`, `source_tool`, `published_at`, `credit`, `fields`
  and `generated_by`.
- **Only a model's score is stored.** An item a model wrote states `relevance` (0 to 10), `quote`
  and `review`. An item code copied (a newsletter issue, a paper copied by code) states none of the
  three, and its `generated_by` names the job and run only.
- **`fields` has one closed shape per `source_tool`:** `rss` (`categories`, and `author` when the
  feed names one), `huggingface-papers` (`arxiv_id`, `authors`, `upvotes`, `comments`) and `arxiv`.
  A value the source did not state is absent, never an empty text.
- **A newsletter issue names its source:** `newsletter_source` (a `newsletter-source/<slug>` ID),
  with `series` and `series_issue` when its title matches a series of that source.

#### Values read by code instead of stored: the research types (schema 3.0)

- **`paper` stores `url` and no `arxiv_id`.** For an arXiv paper the address is
  `https://arxiv.org/abs/<arXiv ID>`, so a reader takes the ID from it; a recent paper in the feed
  is matched to a `paper` by that address.
- **`research-direction` stores counts, not thresholds.** `selection` and `activity` keep what was
  counted and the verdict; the rule's thresholds live in the consumer's configuration.
- **`quotes` is the one home of a direction's evidence:** one span per sentence of a model-written
  text, with `review` and `generated_by`, all three or none. There is no single `quote`.

#### An enum with a note beside it: `newsletter-source.cadence` (news schema 2.0)

- **`cadence`** is `daily`, `weekly` or `monthly`, stated only when the publisher states it.
- **`cadence_note`** holds a rhythm one word does not say, in the publisher's own terms.

#### One block of a page: the `guide` type

A `guide` record is one block of the GPU Buying Guide page, so the page prints it without reshaping:

- **Placement.** `page_section` (`quick-decision`, `background`, `power`, `further-reading`) names
  the page section that shows the record; `order` sorts the blocks of one section. `title` is the
  heading shown.
- **Text.** The body sections Overview and Takeaway are the lead-in and the closing rule. Rows of
  strings live in the frontmatter: `decisions` (`scenario`, `recommendation`, optional `section`, the
  id of the page section that explains the row), `mistakes`, `points` (`name`, `text`) and one
  `table` (`columns`, `rows`). A `further-reading` record keeps its outside links in `sources`.
- **Figures the page computes are not stored.** Memory by model size, running cost and prices come
  from the `gpu` records, so a guide record carries none of them.

#### A record that drives computed figures: the `hyperparameter` type

A `hyperparameter` record carries what its page draws, so the site holds no page-specific code:

- **Visual-first page order.** `controls` (one plain sentence) → the effect scale from `effects`
  (`decrease[]`, `increase[]`) and `scale` (`min`, `max`, `typical_min`, `typical_max`, `spacing`) →
  Definition → How It Works with the `visual` figure → `typical_values[]` (`setting`, `value`,
  `source`) → Calculation → Worked Example → `mistakes[]` (`mistake`, `why`, `fix`) → What To Watch.
- **`visual` holds parameters, never a drawing.** `kind: schedule` (`peak`, `warmup_steps`,
  `total_steps`, `curves`, `marks`), `kind: distribution` (`tokens`, `logits`, `temperatures`) or
  `kind: beams`; the site computes every point (`components/figures`). An example value is named as
  one in `caption`.
- **Only Definition is a required section;** the others are optional. `related` (the base field)
  lists the settings a record interacts with, and the page prints them under "Interacts with".

#### A rule a consumer derives from: the `framework-support` type

A `framework-support` record says which compute platforms one framework officially supports, so a
GPU's support is derived instead of stored per GPU:

- **One record per framework, no body.** `platforms[]` holds `platform` (a `gpu` record's
  `compute_platform`), `supported`, the `source` page and, where that page narrows it,
  `min_compute_capability` or `gpus[]` (`gpu/<slug>` IDs, checked as references) and a `note`.
  `checked` is the day the pages were read.
- **Unknown is not unsupported.** `supported: false` only where the page says so; a platform,
  product or compute capability the page does not name derives to null.
- **`framework` links the framework record** (optional): the `framework/<slug>` ID of the same
  project in the frameworks repo, resolved like any reference when both repos are read. The
  framework's page shows these platforms with their sources; a `framework` record carries no GPU
  support.

#### A record made of facts alone: the `framework` type

A `framework` record states its origin in `status`:

- **`curated`:** a person wrote it. `subcategory`, `description`, `best_for`, `key_features`,
  `use_cases` and `pros` are then required.
- **`discovered`:** a job (framework discovery) copied it from GitHub, so it carries facts and no
  prose; none of those fields is required.
- **`kind` is optional.** No GitHub fact says whether a project is a framework, a library or a
  tool, so a record without one has not been judged. The site shows no kind for it and the kind
  filter lists only kinds some record carries.
- **`framework-category/other` holds what no topic maps to.** A repository whose GitHub topics match
  no category is filed there instead of being guessed into one. A person moves it later.
- **A framework has no body section;** `description` is the one home of its text.

#### Where a category sits in the stack: the `framework-category` type

A `framework-category` record carries a required `layer`, one of `build`, `train`, `data`, `run`,
`operate`, `domain` or `other` (in that order on the site). The Categories page groups the records by
it; `order` sorts within a layer. Every record is listed: one with no `defacto` shows no default
pick. The layer titles and one-line notes are interface text in the site's `labels.ts`, because the
loader reads no `meta.json` field beyond the repo's name and domain.

#### A goal and its building blocks: the `use-case` type

A `use-case` record answers "I want to build X: what do I need?". It is a reference, not a how-to:
no install commands, no day plans. Frontmatter carries, besides `label`, `order` and `goal`:

- **`stages[]`** (2 to 4, in order): the lanes of the system map. Each has `id`, `name` and a
  one-sentence `note` on when that part of the system runs.
- **`blocks[]`**, ordered by where they sit in the system: `id` (unique in the record), `stage` (one
  of `stages[].id`), `name`, `purpose`, `options[]` (1 to 5), `how_to_choose[]` (1 to 4 bullets) and an
  optional `browse` (`label`, `record`: a `framework-category/`, `task-group/` or `task/` ID).
- **An option** is an Atlas record (`record`: a `framework/`, `model/`, `benchmark/` or `fine-tuning-method/` ID) or, until
  the Atlas has one, `name` + `url`; never both. `choice` is `default` or `alternative`, and `when`
  says why it is the default or when to pick it. The first option is the default, and each block has
  exactly one.
- **Checks.** JSON Schema covers the shapes. The loader (`atlas_content.use_case_checks`) adds what a
  schema cannot say: the stage exists, one default per block, unique block ids. Every `record` and
  `browse.record` is an ordinary reference (`atlas_content.references`), so a dangling one is reported
  against the file that holds it. The use-case body has one section, Overview.

The site reads the title, page and category of each referenced record
(`lib/content/use-case-references.ts`): a model from the models API, any other record from the
records API. The frameworks API lists a framework's use cases through the `blocks.options.record`
link relation.

#### Authored figures: `diagram_svg`

An `architecture-era` record may carry a hand-authored SVG figure in the `diagram_svg` frontmatter
field, a YAML block scalar holding one `<svg>` element. The page draws, in order of preference:
`diagram_svg`, the block diagram of a catalog model, then the Mermaid `diagram`.
`diagram_caption` captions all of them. The site sanitises the markup, styles it
from the `d-*` classes and opens it in the shared enlarged view.

Rules for the markup:

- **One root:** `<svg class="atlas-figure" viewBox="0 0 W H" role="img" aria-label="...">`, with no
  `width` or `height` attribute.
- **Forbidden:** `<style>`, `<script>`, `<foreignObject>` and colours in attributes (`fill`,
  `stroke`, `style`). Colour comes only from the classes below, so both themes work.
- **Text:** 10 to 12 px in figure units; the classes set the size, so draw the viewBox to match.

Classes (a role class colours a shape and combines with `d-box` or `d-node`):

| Kind | Classes |
| --- | --- |
| Text | `d-title` (12 px, bold), `d-label` (11 px), `d-note` (10 px, dimmed), `d-math` (11 px, italic) |
| Shapes | `d-box` (block), `d-node` (circle neuron), `d-frame` (dashed group outline), `d-fill-soft` (feature maps, bands) |
| Roles | `d-role-input`, `d-role-embedding`, `d-role-position`, `d-role-attention`, `d-role-feedforward`, `d-role-router`, `d-role-output`, `d-role-vision`, `d-role-audio`, `d-role-projector` |
| Lines | `d-line`, `d-line-strong`, `d-line-accent`, `d-line-back` (dashed: backward pass, skip or feedback paths) |
| Arrow heads (marker shapes) | `d-arrow`, `d-arrow-accent`, `d-arrow-strong` |

### 4.3 IDs and relationships

- **`id` is `<type>/<slug>` and is immutable.** Renaming a file changes the `slug`/`id`; treat that
  as a breaking change (add a redirect note in `CHANGELOG`, update referrers).
- **All cross-references use IDs, never titles** (`related`, and any domain-specific link fields
  such as `led_to`, `influenced_by`, `architecture_id`, `notable_models[].model`,
  `learn_first[].id`, `gpu_id`). This keeps the graph resolvable and lets the consumer detect
  dangling references.
- **A name with no record is named text, not a guessed ID.** Where a product or model has no
  record, the field beside the ID takes the name (`license_note`, `gpu_name`,
  `notable_models[].name`); a record sets one of the two, never both.
- **A reference may point into another content repo** (a task's `benchmarks` are
  `benchmark/<slug>` IDs from the evaluation repo); the consumer resolves IDs across every mounted
  repo.
- **No reverse link is stored.** A record names what it points at; the list of what points at it
  (the models under a licence, the architectures after one) is read from those links by the
  consumer, never written into the target.

## 5. Validation

- The **JSON Schema lives in the repo** (`schema/`), so the contract travels with the content and
  any consumer validates against the same source.
- **Validation runs in the consumer**, not the repo (the repo has no code). For TheAIAtlas, the
  loader in `packages/atlas-content` validates every file's frontmatter against its type schema and
  checks that every relationship ID resolves, on every load and before every automatic commit.
- A file that fails schema validation or has a dangling reference fails the load, and the error
  names the file.
- **Records are strict.** The consumer rejects a top-level field its type's schema does not
  declare, and each schema closes the blocks of fixed shape too (`sources[]`, `fingerprint`,
  `permissions`, `notable_models[]`). The schema fixes `schema_version` as a constant of the type,
  so a record with any other value is refused, in all six repos.
- **Every fact is stored once.** A value another field states is derived by the reader, never
  copied into a second field, and no record stores a reverse link.

## 6. Consumption and git-submodule mechanics

- Each repo is mounted in a consumer as a **git submodule** (TheAIAtlas: `content/atlas-<domain>-content/`),
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

- **`schema_version`** is per file, fixed as a constant by the type's schema, and mirrored in
  `meta.json`/`registry.json`. Bump the minor for additive fields, the major for breaking changes;
  a bump changes the constant and converts every record in the same change. Record both in
  `CHANGELOG.md`.
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
