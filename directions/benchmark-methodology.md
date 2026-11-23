---
id: research-direction/benchmark-methodology
type: research-direction
slug: benchmark-methodology
schema_version: 3.0
title: Benchmark Methodology
search_query: LLM+benchmark+contamination
order: 10
status: retired
origin:
  source: OpenAlex keyword
  keyword_ids:
  - benchmark-contamination
  keyword_names:
  - benchmark contamination
  first_seen: '2026-11-23'
selection:
  works_recent: 0
  works_previous: 0
  field_recent: 28087
  field_previous: 20431
  window_days: 90
  leave_after_runs: 2
  runs_below: 0
  observed_at: '2026-11-23'
activity:
  papers_recent: 42
  papers_previous: 72
  field_recent: 43623
  field_previous: 36684
  window_days: 90
  is_hot: false
  observed_at: '2026-11-22'
  source: https://export.arxiv.org/api/query?search_query=all%3ALLM+AND+all%3Abenchmark+AND+all%3Acontamination+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608170000+TO+202611150000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2501.14249
  title: Humanity's Last Exam
  trust: 0.9
---

## Why It Matters

Building benchmarks that still separate models as older ones saturate.

- The Humanity's Last Exam authors report that LLMs achieve over 90% accuracy on popular benchmarks such as MMLU, which limits informed measurement.
