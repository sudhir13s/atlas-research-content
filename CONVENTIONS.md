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
- `schema_version`: the `major.minor` the file was authored against (currently `2.3`).

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
- **research-direction** — `search_query`, `order`. Body: `Why It Matters`.
  - **Which directions exist is decided by rule, not by hand.** A direction stands for one or
    more OpenAlex keywords; the `research-curation` job counts the arXiv-primary works of every
    keyword each month and applies the rule in `config/jobs.yaml` of TheAIAtlas.
  - `origin` is agent-owned and written once: `source` (`OpenAlex keyword`), `keyword_ids` (short
    OpenAlex IDs, the naming keyword first), `keyword_names` and `first_seen`. A direction the
    job adds takes its title from the first keyword's name in title case, its slug from the
    title, and its `search_query` from that name as one phrase.
  - `status` is agent-owned: `active` (listed) or `retired` (kept with its text, not listed).
    A record without it is active. A direction is retired after `leave_after_runs` runs in a
    row below the leave bar and becomes active again when its keywords pass the entry bar.
  - `selection` is agent-owned and never written by hand: the keyword works in the latest
    window and the one before (`works_recent`, `works_previous`), the same counts for every
    work counted (`field_recent`, `field_previous`), the rule's numbers (`window_days`,
    `min_recent_papers`, `max_field_share`, `max_directions`, `leave_below_ratio`,
    `leave_after_runs`), `runs_below` and the day read.
    - Entry: `works_recent >= min_recent_papers` and
      `works_recent <= max_field_share * field_recent`, while fewer than `max_directions` are
      active; the fastest-growing keywords enter first.
    - Leave bar: `leave_below_ratio * min_recent_papers`.
  - The text of a direction the job adds is written by a model from the abstracts of the
    keyword's most cited recent arXiv papers and reviewed before it is stored. Such a record
    lists those papers in `sources` and carries `quotes` (one abstract span per sentence of the
    text, in sentence order; a record written before 2.3 has a single `quote`), `review` and
    `generated_by`. A hand-written record has none of them.
  - `search_query` is words joined with `+`; a phrase goes inside double quotes
    (`"mixture+of+experts"`, `agent+"tool+use"`). A paper must contain every word and phrase. The
    same query opens the arXiv search and is counted through the arXiv API, so it holds no field
    prefix and no `OR`.
  - `activity` is agent-owned and never written by hand; a template has none. It holds the arXiv
    paper counts for the query in the latest window and the one before (`papers_recent`,
    `papers_previous`), the same two counts for every paper of the counted arXiv categories
    (`field_recent`, `field_previous`), the rule the counts were judged by (`window_days`,
    `min_papers_high_volume`, `min_papers`, `min_growth_vs_field`), the verdict `is_hot`, the day
    read and the API address that gave `papers_recent`.
  - A direction is hot for either of two reasons. High volume:
    `papers_recent >= min_papers_high_volume`. Rising: `papers_recent >= min_papers` and
    `papers_recent / papers_previous >= min_growth_vs_field * field_recent / field_previous`, enough
    papers and faster growth than the field. A record without `activity` is not marked.
- **research-resource** — `icon`, `links[]` (`{label, url}`, display order), `order`. Body:
  `Overview`.

- **feed-item** — a recent paper the community is reading, kept apart from the landmark `paper`
  records. Its slug is `<YYYY-MM-DD>-<title-words>-<8 hex>`: the UTC day the source published it
  (`undated` when it gave no date), the title as lowercase ASCII words cut to 60 characters, and the
  first 8 hex characters of the SHA-256 of its `url`. The file is `feed/<year>/<month>/<slug>.md`
  (`feed/undated/` without a date) and its name equals `slug`. `kind` is always `paper`; `url` is
  unique across the repo; `source` names the `config/sources.yaml` entry and `source_tool` the fetch
  tool (`arxiv`, `huggingface-papers`). A paper copied by code has a `generated_by` that names the
  job and run only: `fields` holds what the source gave (`arxiv_id`, `authors`, counts), `relevance`
  is `0`, `tags` is empty, the `Summary` is the abstract as the source gives it, and it has no
  `quote`, `review` or `Why It Matters`. A paper a model wrote names `provider`, `model` and
  `prompt_version` in `generated_by` and carries `quote`, `review` and both sections.

## Sourcing

Open-source-first, zero plagiarism. Prefer open papers and official pages. Reference paywalled
material only as a cited pointer, never as copied text. Record everything in `sources[]`.
