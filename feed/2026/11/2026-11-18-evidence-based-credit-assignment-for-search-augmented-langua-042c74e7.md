---
id: feed-item/2026-11-18-evidence-based-credit-assignment-for-search-augmented-langua-042c74e7
type: feed-item
slug: 2026-11-18-evidence-based-credit-assignment-for-search-augmented-langua-042c74e7
schema_version: 1.0
title: Evidence-Based Credit Assignment for Search-Augmented Language Models
kind: paper
url: https://arxiv.org/abs/2611.23824
source: arXiv
source_tool: arxiv
published_at: '2026-11-18T04:24:51+00:00'
relevance: 7
quote: We present Evidence-based Credit Assignment (ECA), which augments terminal outcome rewards with a training-only auxiliary signal measuring how retrieved documents improve the likelihood of a reference answer.
credit: Metadata from the arXiv API; thank you to arXiv for use of its open access interoperability.
fields:
  arxiv_id: '2611.23824'
  version: 1
  authors:
  - Wen Wang
  - Jindong Wang
  - Jiahua Bao
  - Tu Yongsiqi
  - Yihao Liu
  - Junwei He
  - Wenkui Fan
  categories:
  - cs.AI
  primary_category: cs.AI
  pdf_url: https://arxiv.org/pdf/2611.23824v1
  doi: ''
  journal_reference: ''
  comment: 16 pages, 4 figures. Includes supplementary material
  updated: '2026-11-18T04:24:51Z'
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
- url: https://arxiv.org/abs/2611.23824
  title: Evidence-Based Credit Assignment for Search-Augmented Language Models
---

## Summary

The paper introduces Evidence-based Credit Assignment (ECA), a training-only auxiliary signal that measures how retrieved documents improve the likelihood of a reference answer to address the limits of outcome supervision in search-augmented language models. It compares ECA-Step and ECA-Horizon return formulations paired with cross-fold group normalization, novelty gating, and search-local token assignment. Across seven Search QA benchmarks, ECA-Horizon improves strict macro exact match over an outcome-only GRPO baseline by 1.03 and 4.80 percentage points on Qwen2.5-3B- and 7B-Instruct, respectively.

## Why It Matters

unknown
