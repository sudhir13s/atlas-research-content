---
id: research-direction/efficient-inference
type: research-direction
slug: efficient-inference
schema_version: 2.1
title: Efficient Inference
search_query: efficient+inference+quantization+LLM
order: 12
activity:
  papers_recent: 45
  papers_previous: 51
  field_recent: 43623
  field_previous: 36684
  window_days: 90
  min_papers_high_volume: 400
  min_papers: 100
  min_growth_vs_field: 1.05
  is_hot: false
  observed_at: '2026-11-22'
  source: https://export.arxiv.org/api/query?search_query=all%3Aefficient+AND+all%3Ainference+AND+all%3Aquantization+AND+all%3ALLM+AND+%28cat%3Acs.AI+OR+cat%3Acs.CL+OR+cat%3Acs.LG+OR+cat%3Acs.CV+OR+cat%3Acs.SE+OR+cat%3Acs.CR%29+AND+submittedDate%3A%5B202608170000+TO+202611150000%5D&max_results=1
tags:
- research-direction
updated: '2026-11-22'
sources:
- url: https://arxiv.org/abs/2210.17323
  title: 'GPTQ: Accurate Post-Training Quantization for Generative Pre-trained Transformers'
  trust: 0.9
- url: https://arxiv.org/abs/2211.17192
  title: Fast Inference from Transformers via Speculative Decoding
  trust: 0.9
---

## Why It Matters

Reducing the hardware and time needed to run a trained model.

- GPTQ quantizes 175-billion-parameter models to 3 or 4 bits per weight with negligible accuracy loss, its authors report.
- Speculative decoding produces identical outputs 2 to 3 times faster on T5-XXL, its authors report.
