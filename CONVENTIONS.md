# CONVENTIONS.md — authoring rules

The rules every file follows. Humans and agents follow the identical process. The authoritative
cross-repo spec is the
[content-repo standard](https://github.com/sudhir13s/TheAIAtlas/blob/main/docs/content-repo-standard.md);
this file is the `research`-domain instance.

## Slugs and file names

- Slugs are **lowercase, hyphen-separated, ASCII** — no spaces, no underscores. Example:
  `attention-is-all-you-need`, `scaling-laws-for-neural-language-models`, `arxiv`.
- A paper's slug is its title in slug form, cut at a word boundary to about 60 characters; two
  papers that would share a slug get the year appended.
- A topic's slug is its short name (`transformers`), a resource's slug is the platform's short id
  (`semantic-scholar`), a direction's slug is its name in slug form.
- The file name is `<slug>.md` and **must equal** the `slug` frontmatter field.
- A file lives in the folder mapped to its `type` in `schema/registry.json`.

## IDs

- `id` = `<type>/<slug>` (e.g. `paper/attention-is-all-you-need`). Globally unique, **immutable**.
- All cross-references use IDs, never titles: `related`, and `topics` on a paper
  (`research-topic/<slug>`).
- Every referenced ID must resolve to an existing file. Dangling references fail validation.

## Frontmatter

Optional on every file: `aliases` — other names the record is written as — and `locked` — field
paths no job may change.

Base fields on **every** file: `id`, `type`, `slug`, `schema_version`, `title`, `tags`, `updated`,
`sources`. Optional base fields: `related`, `aliases`, `locked`. Each type adds its own fields —
see `schema/<type>.schema.json`.

- `tags`: lowercase, hyphen-separated.
- `updated`: ISO date (`YYYY-MM-DD`).
- `sources[]`: `{ url, title, trust }` — `trust` in `[0,1]`. A paper's source is its own link.
- `schema_version`: the `major.minor` the file was authored against (currently `1.1`).

## Body sections

- Prose lives under `##` headings. The **required sections** and their order per type are declared
  in `schema/registry.json → types.<type>.sections`; `optional_sections` may be absent and, when
  present, follow the required ones in that order.

## Per-type specifics

- **paper** — one record per distinct paper, however many lists it appears in. `authors` is the
  string as written, without the year; `year` is a number. `url` is the link as given (an arXiv
  abstract page, a publisher page, a PDF or a book); `arxiv_id` is present only for arXiv links.
  `topics` lists every topic the paper sits under (empty for none). `must_read` is
  `{era, order}` and present only for must-read papers. `is_high_impact` marks the few papers the
  page highlights. Body: `Why It Matters`, then optionally `Also Noted` (a second text from another
  topic's list). `summary` holds the short must-read text when a longer one fills `Why It Matters`.
  Other titles the paper is known by go in `aliases`. `citation_signals` is agent-owned: citation
  count, venue, the day it was read and the paper's OpenAlex address, copied by code for papers with
  an arXiv ID or DOI; never written by hand.
- **research-topic** — `icon`, `order`. No body.
- **research-direction** — `search_query` (words joined with `+`), `is_hot`, `order`. Body:
  `Why It Matters`.
- **research-resource** — `icon`, `links[]` (`{label, url}`, display order), `order`. Body:
  `Overview`.

## Sourcing

Open-source-first, zero plagiarism. Prefer open papers and official pages. Reference paywalled
material only as a cited pointer, never as copied text. Record everything in `sources[]`.
