---
id: paper/<slug>
type: paper
slug: <slug>
schema_version: 1.1
title: "<Full paper title>"
aliases: ["<shorter name the paper is also known by>"]   # optional
authors: "<First author et al.>"
year: <YYYY>
url: "<where to read it>"
arxiv_id: "<NNNN.NNNNN>"                 # only when the url is an arXiv link
topics: [research-topic/<slug>]          # every topic the paper is listed under; [] for none
must_read: { era: "<era heading>", order: 1 }   # only for must-read papers
is_high_impact: false
citation_signals:                        # agent-owned; absent until OpenAlex has been read
  cited_by_count: <N>
  venue: "<source OpenAlex names>"       # optional
  observed_at: "<YYYY-MM-DD>"
  source: "https://openalex.org/<W-id>"
summary: "<short text, only when a longer text fills the section>"   # optional
tags: [paper]
updated: <YYYY-MM-DD>
sources:
  - { url: "<url>", title: "<Full paper title>" }
---

## Why It Matters

<What the paper changed and why a reader should know it.>

## Also Noted

<Optional: a second angle on the paper from another topic's list.>
