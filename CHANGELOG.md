# Changelog

All notable changes to `atlas-research-content`. Grouped by schema version / release. Follows
[Keep a Changelog](https://keepachangelog.com/) conventions.

## [Unreleased]

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
