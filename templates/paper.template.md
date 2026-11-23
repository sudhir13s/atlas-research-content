---
id: paper/<slug>
type: paper
slug: <slug>
schema_version: 3.0                      # the schema's current version; the schema refuses any other
title: "<Full paper title>"
aliases: ["<shorter name the paper is also known by>"]   # optional
authors: "<First author et al.>"         # one line of text, not a list
year: <YYYY>
url: "<where to read it>"                # https://arxiv.org/abs/<NNNN.NNNNN> for an arXiv paper; the arXiv ID is read from it
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
