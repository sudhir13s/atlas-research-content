---
id: feed-item/2026-11-18-jeveration-system-one-models-now-generate-8c5914db
type: feed-item
slug: 2026-11-18-jeveration-system-one-models-now-generate-8c5914db
schema_version: 2.0
title: 'Jeveration: System One Models Now Generate'
kind: paper
url: https://arxiv.org/abs/2611.24738
source: Hugging Face Papers
source_tool: huggingface-papers
published_at: '2026-11-18T00:00:00+00:00'
relevance: 8
quote: In this paper, we introduce Jeveration, showing that the same decision paradigm can also generate high-quality images in a single forward pass.
credit: Paper list and upvotes from Hugging Face Papers (huggingface.co/papers); each paper is on arXiv under its own licence, thank you to arXiv for use of its open access interoperability.
fields:
  arxiv_id: '2611.24738'
  authors:
  - Yuhe Liu
  - Qi Li
  - Shihua Zhang
  - Xinchao Wang
  upvotes: 137
  comments: 4
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
- models
- research
updated: '2026-11-21'
sources:
- url: https://arxiv.org/abs/2611.24738
  title: 'Jeveration: System One Models Now Generate'
---

## Summary

The paper introduces Jeveration, a system that enables System One models to generate high-quality images in a single forward pass by building on a frozen vision-language model. Jeveration conditions parallel predictions on a shared random state and uses a distribution over discrete image codes to achieve global consistency. A single checkpoint also supports text-to-image generation, image-to-image generation, and dense prediction.

## Why It Matters

Experiments show that Jeveration generates a 512x512 image in 78 ms, up to 122x faster than existing unified models, while maintaining competitive image quality and dense prediction performance.
