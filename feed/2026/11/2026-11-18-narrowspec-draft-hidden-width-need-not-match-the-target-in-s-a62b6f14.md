---
id: feed-item/2026-11-18-narrowspec-draft-hidden-width-need-not-match-the-target-in-s-a62b6f14
type: feed-item
slug: 2026-11-18-narrowspec-draft-hidden-width-need-not-match-the-target-in-s-a62b6f14
schema_version: 2.0
title: 'NarrowSpec: Draft Hidden Width Need Not Match the Target in Speculative Decoding'
kind: paper
url: https://arxiv.org/abs/2611.23835
source: arXiv
source_tool: arxiv
published_at: '2026-11-18T04:40:10+00:00'
relevance: 8
quote: We show that the draft's whole residual stream can run at half or a quarter of that width while largely preserving acceptance.
credit: Metadata from the arXiv API; thank you to arXiv for use of its open access interoperability.
fields:
  arxiv_id: '2611.23835'
  version: 1
  authors:
  - Alagappan Valliappan
  - Ankit More
  - Dheevatsa Mudigere
  - Jatin Mitra
  categories:
  - cs.CL
  - cs.LG
  - cs.PF
  primary_category: cs.CL
  pdf_url: https://arxiv.org/pdf/2611.23835v1
  comment: 29 pages, 6 figures, 33 tables
  updated: '2026-11-18T04:40:10Z'
review:
  score: 10.0
  reviewed_by:
    provider: nvidia-gemma-4-31b
    model: nvidia_nim/google/gemma-4-31b-it
  prompt_versions:
    writer: 2.1.0
    critic: 1.1.0
generated_by:
  job: news-digest
  run_id: 4
  provider: gemini-flash-lite
  model: gemini/gemini-3.5-flash-lite
  prompt_version: 2.1.0
tags:
- research
- models
updated: '2026-11-19'
sources:
- url: https://arxiv.org/abs/2611.23835
  title: 'NarrowSpec: Draft Hidden Width Need Not Match the Target in Speculative Decoding'
---

## Summary

This work demonstrates that draft models in speculative decoding can operate at half or a quarter of the target model's hidden width while preserving token acceptance. The authors test DFlash and EAGLE-3 on targets like Qwen3-8B (NVFP4) and GPT-OSS-20B (MXFP4), showing that narrowing the draft model speeds up end-to-end decoding across various batch sizes on B200 and GB10 hardware.

## Why It Matters

unknown
