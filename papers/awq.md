---
id: paper/awq
type: paper
slug: awq
schema_version: 1.0
title: AWQ
authors: Lin et al.
year: 2023
url: https://arxiv.org/abs/2306.00978
arxiv_id: '2306.00978'
topics:
- research-topic/efficiency
is_high_impact: false
tags:
- paper
updated: '2026-11-19'
sources:
- url: https://arxiv.org/abs/2306.00978
  title: AWQ
---

## Why It Matters

Identified that protecting just 1% of salient weight channels (those corresponding to large activations) preserves model quality during INT4 quantization. Achieves better quality than GPTQ at the same bitwidth with a simpler method. The go-to quantization technique for deploying LLMs on consumer hardware because it is fast, accurate, and widely supported by inference engines.
