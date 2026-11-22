# Changelog

All notable changes to `atlas-research-content`. Grouped by schema version / release. Follows
[Keep a Changelog](https://keepachangelog.com/) conventions.

## [Unreleased]

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
