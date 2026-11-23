---
id: paper/qlora-efficient-finetuning-of-quantized-language-models
type: paper
slug: qlora-efficient-finetuning-of-quantized-language-models
schema_version: 3.0
title: 'QLoRA: Efficient Finetuning of Quantized Language Models'
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
summary: Fine-tune a 65B model on a single 48GB GPU via 4-bit quantization + low-rank adaptation. Democratized LLM customization for individual researchers and small teams.
tags:
- paper
updated: '2026-11-19'
sources:
- url: https://arxiv.org/abs/2305.14314
  title: 'QLoRA: Efficient Finetuning of Quantized Language Models'
---

## Why It Matters

Combined 4-bit NormalFloat quantization with LoRA adapters to enable fine-tuning a 65B model on a single 48GB GPU without quality degradation. Introduced double quantization and paged optimizers to push memory efficiency further. Democratized LLM fine-tuning — anyone with a consumer GPU can now customize a frontier-scale model.
