---
id: paper/lora
type: paper
slug: lora
schema_version: 3.0
title: LoRA
authors: Hu et al.
year: 2021
url: https://arxiv.org/abs/2106.09685
topics:
- research-topic/efficiency
is_high_impact: false
citation_signals:
  cited_by_count: 24655
  venue: arXiv (Cornell University)
  observed_at: '2026-11-23'
  source: https://openalex.org/W3168867926
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2106.09685
  title: LoRA
---

## Why It Matters

Freezes the pretrained model and injects trainable low-rank decomposition matrices into each transformer layer, reducing trainable parameters by 10,000x while matching full fine-tuning quality. No added inference latency because the adapters merge into the base weights. The dominant fine-tuning method — used in virtually every LLM customization workflow from enterprise to hobbyist.
