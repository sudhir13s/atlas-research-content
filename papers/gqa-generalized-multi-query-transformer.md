---
id: paper/gqa-generalized-multi-query-transformer
type: paper
slug: gqa-generalized-multi-query-transformer
schema_version: 3.0
title: 'GQA: Generalized Multi-Query Transformer'
authors: Ainslie et al.
year: 2023
url: https://arxiv.org/abs/2305.13245
topics:
- research-topic/transformers
is_high_impact: false
citation_signals:
  cited_by_count: 2415
  venue: Conference on Empirical Methods in Natural Language Processing (EMNLP)
  observed_at: '2026-11-23'
  source: https://openalex.org/W4389518760
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2305.13245
  title: 'GQA: Generalized Multi-Query Transformer'
---

## Why It Matters

Multiple query heads share fewer key-value heads, reducing KV cache memory by 2-8x with minimal quality loss. Now the default attention mechanism in Llama, Mistral, Qwen, and most modern LLMs. The sweet spot between MHA quality and MQA efficiency.
