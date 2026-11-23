---
id: feed-item/<YYYY-MM-DD>-<title-words>-<8-hex-of-url-hash>
type: feed-item
slug: <YYYY-MM-DD>-<title-words>-<8-hex-of-url-hash>
schema_version: 2.0               # the schema's current version; the schema refuses any other
title: "<Title of the paper as the source published it>"
kind: paper
url: "<canonical address>"
source: "<name from config/sources.yaml>"
source_tool: huggingface-papers   # the fetch tool that read it (arxiv | huggingface-papers); it decides the shape of `fields`
published_at: "<YYYY-MM-DDTHH:MM:SS+00:00>"   # UTC; null when the source gave no date
relevance: 7                      # 0 to 10, a model's score; only on a paper a model wrote
quote: "<the passage of the source the summary rests on, word for word>"   # only on a paper a model wrote
credit: "<licence or credit line the source requires>"
fields:                           # what the tool read; this is the huggingface-papers shape, the schema states the arxiv one
  arxiv_id: "<NNNN.NNNNN>"
  authors: ["<author>"]
  upvotes: 0
  comments: 0
review:                           # only on a paper a model wrote
  score: 10.0                     # the Critic's score, 0 to 10
  reviewed_by: { provider: "<provider>", model: "<model>" }
  prompt_versions: { writer: "<version>", critic: "<version>" }
generated_by:
  job: papers-sync
  run_id: 1
  provider: "<provider>"          # provider, model and prompt_version are all left out when code wrote the record
  model: "<model>"
  prompt_version: "<version>"
tags: []
updated: <YYYY-MM-DD>
sources:
  - { url: "<canonical address>", title: "<title>" }
---

## Summary
<The abstract as the source gives it, when code copied the paper; otherwise what the paper says, in one or two sentences, every claim supported by the quote.>

## Why It Matters
<Only on a paper a model wrote: why a reader of the AI ecosystem should care, in one or two sentences.>
