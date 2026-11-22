---
id: research-direction/long-context
type: research-direction
slug: long-context
schema_version: 2.0
title: Long Context
search_query: long+context+window+language+model
order: 14
activity:
  papers_recent: 116
  papers_previous: 108
  field_recent: 43623
  field_previous: 36684
  window_days: 90
  min_papers: 100
  min_growth_vs_field: 1.05
  is_hot: false
  observed_at: '2026-11-22'
  source: https://export.arxiv.org/api/query?search_query=all%3Along+AND+all%3Acontext+AND+all%3Awindow+AND+all%3Alanguage+AND+all%3Amodel+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608170000+TO+202611150000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-22'
sources:
- url: https://arxiv.org/abs/2306.15595
  title: Extending Context Window of Large Language Models via Positional Interpolation
  trust: 0.9
---

## Why It Matters

Extending how many tokens a language model can take as input.

- Position Interpolation extends the context window of RoPE-based LLaMA models to up to 32,768 tokens with minimal fine-tuning, its authors report.
