---
id: research-direction/small-language-models
type: research-direction
slug: small-language-models
schema_version: 2.2
title: Small Language Models
search_query: '"small+language+model"'
order: 4
status: active
origin:
  source: OpenAlex keyword
  keyword_ids:
  - small-language-models
  keyword_names:
  - small language models
  first_seen: '2026-11-23'
selection:
  works_recent: 130
  works_previous: 125
  field_recent: 28087
  field_previous: 20431
  window_days: 90
  min_recent_papers: 250
  max_field_share: 0.08
  max_directions: 25
  leave_below_ratio: 0.7
  leave_after_runs: 2
  runs_below: 1
  observed_at: '2026-11-23'
activity:
  papers_recent: 177
  papers_previous: 170
  field_recent: 43411
  field_previous: 36532
  window_days: 90
  min_papers_high_volume: 400
  min_papers: 100
  min_growth_vs_field: 1.05
  is_hot: false
  observed_at: '2026-11-23'
  source: https://export.arxiv.org/api/query?search_query=all%3A%22small+language+model%22+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608180000+TO+202611160000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2404.14219
  title: 'Phi-3 Technical Report: A Highly Capable Language Model Locally on Your Phone'
  trust: 0.9
---

## Why It Matters

Language models small enough to run on limited hardware.

- The Phi-3 authors report that phi-3-mini, a 3.8-billion-parameter model small enough to deploy on a phone, rivals Mixtral 8x7B and GPT-3.5 on academic benchmarks and internal testing.
