---
id: paper/gqa-generalized-multi-query-transformer
type: paper
slug: gqa-generalized-multi-query-transformer
schema_version: 1.0
title: 'GQA: Generalized Multi-Query Transformer'
authors: Ainslie et al.
year: 2023
url: https://arxiv.org/abs/2305.13245
arxiv_id: '2305.13245'
topics:
- research-topic/transformers
is_high_impact: false
tags:
- paper
updated: '2026-11-19'
sources:
- url: https://arxiv.org/abs/2305.13245
  title: 'GQA: Generalized Multi-Query Transformer'
---

## Why It Matters

Multiple query heads share fewer key-value heads, reducing KV cache memory by 2-8x with minimal quality loss. Now the default attention mechanism in Llama, Mistral, Qwen, and most modern LLMs. The sweet spot between MHA quality and MQA efficiency.
