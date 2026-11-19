---
id: paper/llm-int8
type: paper
slug: llm-int8
schema_version: 1.0
title: LLM.int8()
authors: Dettmers et al.
year: 2022
url: https://arxiv.org/abs/2208.07339
arxiv_id: '2208.07339'
topics:
- research-topic/efficiency
is_high_impact: false
tags:
- paper
updated: '2026-11-19'
sources:
- url: https://arxiv.org/abs/2208.07339
  title: LLM.int8()
---

## Why It Matters

Discovered that LLM weights have emergent outlier features that break naive INT8 quantization, then solved it with mixed-precision decomposition — keeping outlier dimensions in FP16 while quantizing the rest to INT8. Made it possible to run a 175B model in half the GPU memory. The first practical method for quantizing billion-scale models without retraining.
