---
id: paper/qlora-efficient-finetuning-of-quantized-language-models
type: paper
slug: qlora-efficient-finetuning-of-quantized-language-models
schema_version: 3.0
title: 'QLoRA: Efficient Finetuning of Quantized LLMs'
aliases:
- QLoRA
authors: Dettmers et al.
year: 2023
url: https://arxiv.org/abs/2305.14314
topics:
- research-topic/efficiency
must_read:
  era: LLM Era & Agents (2022-Present)
  order: 7
is_high_impact: false
citation_signals:
  cited_by_count: 7575
  venue: NeurIPS 2023
  observed_at: '2026-11-23'
  source: https://openalex.org/W7133233472
summary: Introduces QLoRA, a fine-tuning approach that backpropagates gradients through a frozen, 4-bit quantized pretrained language model into Low Rank Adapters (LoRA).
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2305.14314
  title: 'QLoRA: Efficient Finetuning of Quantized LLMs'
- url: https://proceedings.neurips.cc/paper_files/paper/2023/hash/1feb87871436031bdc0f2beaa62a049b-Abstract-Conference.html
  title: 'QLoRA: Efficient Finetuning of Quantized LLMs'
locked:
- citation_signals.venue
---

## Why It Matters

It cuts memory enough to fine-tune a 65B-parameter model on a single 48GB GPU while preserving full 16-bit fine-tuning task performance. It introduces:

- 4-bit NormalFloat (NF4), a data type the authors call information theoretically optimal for normally distributed weights;
- double quantization, which quantizes the quantization constants;
- paged optimizers to manage memory spikes.

The authors’ Guanaco models reach 99.3% of ChatGPT’s performance level on the Vicuna benchmark after 24 hours of fine-tuning on a single GPU.
