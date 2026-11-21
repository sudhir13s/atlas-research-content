---
id: feed-item/2026-11-19-posterior-matching-distillation-78d21f09
type: feed-item
slug: 2026-11-19-posterior-matching-distillation-78d21f09
schema_version: 1.1
title: Posterior Matching Distillation
kind: paper
url: https://arxiv.org/abs/2611.26629
source: Hugging Face Papers
source_tool: huggingface-papers
published_at: '2026-11-19T00:00:00+00:00'
relevance: 7
quote: Experiments on SDXL and FLUX.2 [klein] 4B demonstrate that PMD achieves the best FID among 4-step methods on both models, while maintaining competitive or leading performance across prompt-alignment and perceptual-quality metrics.
credit: Paper list and upvotes from Hugging Face Papers (huggingface.co/papers); each paper is on arXiv under its own licence, thank you to arXiv for use of its open access interoperability.
fields:
  arxiv_id: '2611.26629'
  authors:
  - Hidir Yesiltepe
  - Julius Berner
  - Arash Vahdat
  - Pinar Yanardag
  upvotes: 29
  comments: 2
review:
  score: 10.0
  reviewed_by:
    provider: cloudflare-llama-3-3-70b
    model: openai/@cf/meta/llama-3.3-70b-instruct-fp8-fast
  prompt_versions:
    writer: 2.2.0
    critic: 1.2.0
generated_by:
  job: news-digest
  run_id: 26
  provider: gemini-flash-lite
  model: gemini/gemini-3.5-flash-lite
  prompt_version: 2.2.0
tags:
- research
- models
updated: '2026-11-21'
sources:
- url: https://arxiv.org/abs/2611.26629
  title: Posterior Matching Distillation
---

## Summary

The authors introduce Posterior Matching Distillation (PMD), a diffusion distillation method combining mode-covering posterior sampling with any-step generation. PMD matches exponentially reweighted averages of student samples to corresponding teacher posterior means, recovering the teacher's full posterior at each trained noise level. Experiments on SDXL and FLUX.2 [klein] 4B show that PMD achieves the best FID among 4-step methods on both models.

## Why It Matters

PMD achieves the best FID among 4-step methods on both models while maintaining competitive or leading performance across prompt-alignment and perceptual-quality metrics.
