---
id: feed-item/2026-11-18-a-system-1-decision-model-for-medical-multiple-choice-questi-cef683fb
type: feed-item
slug: 2026-11-18-a-system-1-decision-model-for-medical-multiple-choice-questi-cef683fb
schema_version: 1.0
title: A System 1 Decision Model for Medical Multiple-Choice Questions Built on Frozen Language Models
kind: paper
url: https://arxiv.org/abs/2611.23832
source: arXiv
source_tool: arxiv
published_at: '2026-11-18T04:38:49+00:00'
relevance: 6
quote: We rebuilt the recipe from scratch for MedMCQA and trained only two projection heads and one temperature on top of frozen Qwen3.5-0.8B, Granite-4.2-3B and Qwen3-8B, using a contrastive loss with in-batch and hard negatives and a mask for repeated answers.
credit: Metadata from the arXiv API; thank you to arXiv for use of its open access interoperability.
fields:
  arxiv_id: '2611.23832'
  version: 1
  authors:
  - Pavan Kumar Mantha
  categories:
  - cs.AI
  - cs.CL
  primary_category: cs.AI
  pdf_url: https://arxiv.org/pdf/2611.23832v1
  doi: ''
  journal_reference: ''
  comment: 12 pages with 7 tabular explanations
  updated: '2026-11-18T04:38:49Z'
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
- models
- research
- evaluation
updated: '2026-11-19'
sources:
- url: https://arxiv.org/abs/2611.23832
  title: A System 1 Decision Model for Medical Multiple-Choice Questions Built on Frozen Language Models
---

## Summary

A System 1 decision model for medical multiple-choice questions is built using frozen language models, specifically Qwen3.5-0.8B, Granite-4.2-3B, and Qwen3-8B, with two small trained projection heads. The approach achieves 41.7% and 42.5% accuracy for the small encoders and 46.0% +-0.2 for Qwen3-8B on 3,842 held-out MedMCQA questions. The authors present this as a cheap and fast baseline rather than a competitive system.

## Why It Matters

unknown
