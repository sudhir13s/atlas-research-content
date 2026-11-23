# Changelog

All notable changes to `atlas-research-content`. Grouped by schema version / release. Follows
[Keep a Changelog](https://keepachangelog.com/) conventions.

## [Unreleased]

### Schema 3.0, feed-item 2.0 (strict schemas, checked versions; breaking)

Every record was converted by the consumer's `atlas migrate research-restructure`. A step only
moved, renamed or deleted: no value was added, and `updated` did not move.

- **Changed** `schema_version` to a constant of each schema: `3.0` for `paper`,
  `research-topic`, `research-direction` and `research-resource`, `2.0` for `feed-item`. A
  record with any other value is refused. The records said `1.0`, `1.1`, `2.2` or `2.3`.
- **Changed** to strict: no unknown field at the top level of any type, in `sources[]`, or
  inside a block of fixed shape.
- **Removed** `paper.arxiv_id` (107 of 121 records). Breaking: the ID is read from `url`, which
  is `https://arxiv.org/abs/<arXiv ID>` on each of those records.
- **Removed** the copies of the rule's thresholds from every `research-direction` (26 records).
  Breaking: a reader takes them from the `research-curation` job in `config/jobs.yaml`.
  - `selection`: `min_recent_papers`, `max_field_share`, `max_directions`, `leave_below_ratio`.
  - `activity`: `min_papers_high_volume`, `min_papers`, `min_growth_vs_field`.
  - Kept: the counts, `window_days`, `runs_below`, `leave_after_runs`, `is_hot`, the days read.
- **Removed** `research-direction.quote`. Breaking: the 7 records that held it list the same
  text as the one entry of `quotes`. Their writer prompt version (`1.0.0`) says the span covers
  the whole text; from `2.0.0` there is one span per sentence.
- **Changed** `review` and `generated_by` to shared definitions in `_shared.schema.json`, with
  every property declared. On a `research-direction` they come with `quotes`, all three or none.
- **Changed** `feed-item.fields` from an open object to one shape per `source_tool` (`arxiv`,
  `huggingface-papers`). The shared part of the type is `feed_item` in `_shared.schema.json`,
  identical in `atlas-news-content`.
- **Removed** empty text standing for a missing value in `feed-item.fields`: `doi` and
  `journal_reference` (20 records each) and `comment` (6 records).
- **Changed** `feed-item`: a paper copied by code states no `relevance`, `quote` or `review`
  (it stated `relevance: 0`); a paper a model wrote states all three. No stored record changed
  for this: all 33 are model-written.
- **Kept** as written: `paper.authors` (one line of text; splitting `Bertasius et al.` would
  invent names) and `paper.summary` (optional prose, on 28 records).

### Schema 2.3 (one quote per sentence)

- **Added** the optional, agent-owned `quotes` on `research-direction`: one span of a source
  abstract for each sentence of a model-written text, in sentence order. Each sentence is checked
  against its own quote before the record is stored. The single `quote` stays on the records
  written before 2.3.

### Schema 2.2 (directions chosen by rule)

- **Added** `status` (`active` or `retired`), `origin` and `selection` on `research-direction`,
  all agent-owned and optional. A direction now stands for one or more OpenAlex keywords
  (`origin`); `selection` holds the keyword work counts, the rule and the runs spent below the
  leave bar. A record without `status` is active.
- **Added** the optional `quote`, `review` and `generated_by` on `research-direction`, present
  only on a record whose text a model wrote from paper abstracts.
- **Changed** the 15 `research-direction` records to 2.2: each names its keywords in `origin`
  and keeps its text. Thirteen are `active`. `multi-head-latent-attention` and
  `benchmark-methodology` are `retired`: their keywords are far below the entry bar.

### Schema 2.1 (hot by high volume)

- **Added** `activity.min_papers_high_volume` on `research-direction`: a direction with at least
  that many papers in the latest window is hot whatever its growth. The earlier rule (enough papers
  and faster growth than the field) still marks a direction as well. The 15 records were converted
  to 2.1 and judged again from their stored counts.
- **Changed** `search_query` of three `research-direction` records whose queries matched too few
  papers or papers off the direction: `hallucination-reduction`, `rlhf-alignment` and
  `benchmark-methodology`. Their counts were read again for the same two windows.

### Schema 2.0 (direction activity)

- **Removed** the hand-set `is_hot` field of `research-direction`. Breaking: a reader of the
  top-level `is_hot` now reads `activity.is_hot`.
- **Added** the optional, agent-owned `activity` block on `research-direction`: the arXiv paper
  counts for the record's `search_query` in the latest window and the one before, the same counts
  for the whole field, the rule they were judged by, the verdict `is_hot`, the day read and the API
  address used. Written by code only; absent until the first count.
- **Changed** `search_query` of `research-direction`: a phrase may be written inside double quotes.
  The 15 records were converted to 2.0, and the queries whose results were off the direction now
  name it by its phrase.

### Directions and resources checked against their primary sources

- **Changed** the 15 `research-direction` records: `Why It Matters` now describes the research
  area and the main approaches, each backed by a paper whose arXiv abstract states it and cited in
  `sources`. Market, adoption and prediction claims and numbers no paper states were removed.
- **Changed** the 13 `research-resource` records: overviews say only what each site states about
  itself, without rankings or unstated "free" claims. Links that no longer resolve or did not do
  what their label said were removed or relabelled, and `sources` lists the pages used.
- **Changed** the GPT-2 and chain-of-thought `paper` records move to `research-topic/llm`.

### Must-read papers checked against their primary pages

- **Changed** the 36 must-read `paper` records after checking each against its arXiv record,
  proceedings page or publisher page: exact titles (short names moved to `aliases`), authors and
  year where they differed, the venue in `citation_signals.venue` set from the page that states it
  and locked against the OpenAlex refresh, and `summary` and `Why It Matters` rewritten to what
  the abstract supports, without superlatives or unsourced influence claims.

### Schema 1.1 (citation signals)

- **Added** the optional, agent-owned `citation_signals` block on `paper`: `cited_by_count`,
  `venue` (optional), `observed_at` and `source` (the paper's OpenAlex address). Copied from
  OpenAlex by code, only for papers with an arXiv ID or DOI, matched by that identifier alone;
  absent until the first read.

### Schema 1.1 (recent papers)

- **Added** the `feed-item` type (folder `feed/<year>/<month>/`, kind `paper` only): one record per
  recent paper the community is reading, copied from Hugging Face Papers or arXiv. It moved here
  from `atlas-news-content`, because Research shows these papers; the files are unchanged.

### Added
- Repository scaffold to the content-repo standard: `meta.json`, `schema/registry.json`, the five
  JSON Schemas (`_shared`, `paper`, `research-topic`, `research-direction`, `research-resource`),
  templates, and docs (`README`, `AGENTS`, `CONVENTIONS`).
- Initial research library (schema version 1.0), moved over from the Research page's code:
  - **paper** — one record per distinct paper, with its topics, must-read era and order, and the
    reason it matters.
  - **research-topic** — the topics that group papers.
  - **research-direction** — research directions with a paper-search query.
  - **research-resource** — platforms for finding and reading papers, with their useful links.

## Schema versions

- **1.0** — initial schema for all four research content types.
- **1.1** — `paper.citation_signals`; the `feed-item` type for recent papers.
- **2.0** — `research-direction.is_hot` replaced by the agent-owned `research-direction.activity`.
- **2.1** — `research-direction.activity.min_papers_high_volume`: a second way to be hot.
- **2.2** — `research-direction.status`, `origin` and `selection`: directions chosen by rule from
  OpenAlex keywords; `quote`, `review` and `generated_by` on a model-written direction.
- **2.3** — `research-direction.quotes`: one quote per sentence of a model-written direction.
- **3.0** — strict schemas and a fixed version per type; `paper.arxiv_id`, the rule copies of
  `research-direction` and `research-direction.quote` removed. `feed-item` is at its own `2.0`:
  typed `fields` per `source_tool`, shared with `atlas-news-content`.
