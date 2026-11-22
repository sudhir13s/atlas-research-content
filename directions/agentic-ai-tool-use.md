---
id: research-direction/agentic-ai-tool-use
type: research-direction
slug: agentic-ai-tool-use
schema_version: 2.1
title: Agentic AI & Tool Use
search_query: agent+"tool+use"
order: 6
activity:
  papers_recent: 596
  papers_previous: 471
  field_recent: 43623
  field_previous: 36684
  window_days: 90
  min_papers_high_volume: 400
  min_papers: 100
  min_growth_vs_field: 1.05
  is_hot: true
  observed_at: '2026-11-22'
  source: https://export.arxiv.org/api/query?search_query=all%3Aagent+AND+all%3A%22tool+use%22+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608170000+TO+202611150000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-22'
sources:
- url: https://arxiv.org/abs/2210.03629
  title: 'ReAct: Synergizing Reasoning and Acting in Language Models'
  trust: 0.9
- url: https://arxiv.org/abs/2302.04761
  title: 'Toolformer: Language Models Can Teach Themselves to Use Tools'
  trust: 0.9
---

## Why It Matters

Language models that plan and act, for example by calling tools and APIs.

- ReAct interleaves reasoning traces with task actions.
- Toolformer is trained to decide which APIs to call, when to call them and what arguments to pass.
