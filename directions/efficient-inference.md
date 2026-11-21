---
id: research-direction/efficient-inference
type: research-direction
slug: efficient-inference
schema_version: 1.0
title: Efficient Inference
search_query: efficient+inference+quantization+LLM
is_hot: false
order: 12
tags:
- research-direction
updated: '2026-11-21'
sources:
- url: https://arxiv.org/abs/2210.17323
  title: 'GPTQ: Accurate Post-Training Quantization for Generative Pre-trained Transformers'
  trust: 0.9
- url: https://arxiv.org/abs/2211.17192
  title: Fast Inference from Transformers via Speculative Decoding
  trust: 0.9
---

## Why It Matters

Reducing the hardware and time needed to run a trained model.

- GPTQ quantizes 175-billion-parameter models to 3 or 4 bits per weight with negligible accuracy loss, its authors report.
- Speculative decoding produces identical outputs 2 to 3 times faster on T5-XXL, its authors report.
