---
id: research-direction/code-generation
type: research-direction
slug: code-generation
schema_version: 2.2
title: Code Generation
search_query: '"code+generation"'
order: 8
status: active
origin:
  source: OpenAlex keyword
  keyword_ids:
  - code-generation
  keyword_names:
  - code generation
  first_seen: '2026-11-23'
selection:
  works_recent: 325
  works_previous: 243
  field_recent: 28087
  field_previous: 20431
  window_days: 90
  min_recent_papers: 250
  max_field_share: 0.08
  max_directions: 20
  leave_below_ratio: 0.7
  leave_after_runs: 2
  runs_below: 0
  observed_at: '2026-11-23'
activity:
  papers_recent: 466
  papers_previous: 433
  field_recent: 43411
  field_previous: 36532
  window_days: 90
  min_papers_high_volume: 400
  min_papers: 100
  min_growth_vs_field: 1.05
  is_hot: true
  observed_at: '2026-11-23'
  source: https://export.arxiv.org/api/query?search_query=all%3A%22code+generation%22+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608180000+TO+202611160000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2107.03374
  title: Evaluating Large Language Models Trained on Code
  trust: 0.9
---

## Why It Matters

Language models that write program code.

- Codex, a GPT model fine-tuned on public GitHub code, was introduced with HumanEval, which checks generated programs for functional correctness.
