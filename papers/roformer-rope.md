---
id: paper/roformer-rope
type: paper
slug: roformer-rope
schema_version: 3.0
title: RoFormer (RoPE)
authors: Su et al.
year: 2021
url: https://arxiv.org/abs/2104.09864
topics:
- research-topic/transformers
is_high_impact: false
tags:
- paper
updated: '2026-11-19'
sources:
- url: https://arxiv.org/abs/2104.09864
  title: RoFormer (RoPE)
---

## Why It Matters

Encodes position by rotating query and key vectors, naturally capturing relative distance. The dominant positional encoding in modern LLMs because it enables context length extension — you can scale rope_theta to handle longer sequences than the model was trained on.
