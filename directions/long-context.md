---
id: research-direction/long-context
type: research-direction
slug: long-context
schema_version: 3.0
title: Long Context
search_query: long+context+window+language+model
order: 14
status: active
origin:
  source: OpenAlex keyword
  keyword_ids:
  - long-context-modeling
  - long-context-reasoning
  keyword_names:
  - long-context modeling
  - long-context reasoning
  first_seen: '2026-11-23'
selection:
  works_recent: 0
  works_previous: 0
  field_recent: 28087
  field_previous: 20431
  window_days: 90
  leave_after_runs: 2
  runs_below: 1
  observed_at: '2026-11-23'
activity:
  papers_recent: 115
  papers_previous: 109
  field_recent: 43411
  field_previous: 36532
  window_days: 90
  is_hot: false
  observed_at: '2026-11-23'
  source: https://export.arxiv.org/api/query?search_query=all%3Along+AND+all%3Acontext+AND+all%3Awindow+AND+all%3Alanguage+AND+all%3Amodel+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608180000+TO+202611160000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2306.15595
  title: Extending Context Window of Large Language Models via Positional Interpolation
  trust: 0.9
---

## Why It Matters

Extending how many tokens a language model can take as input.

- Position Interpolation extends the context window of RoPE-based LLaMA models to up to 32,768 tokens with minimal fine-tuning, its authors report.
