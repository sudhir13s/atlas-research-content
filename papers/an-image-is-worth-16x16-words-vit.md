---
id: paper/an-image-is-worth-16x16-words-vit
type: paper
slug: an-image-is-worth-16x16-words-vit
schema_version: 1.0
title: An Image is Worth 16x16 Words (ViT)
aliases:
- Vision Transformer (ViT)
- ViT
authors: Dosovitskiy et al.
year: 2020
url: https://arxiv.org/abs/2010.11929
arxiv_id: '2010.11929'
topics:
- research-topic/transformers
- research-topic/vision
must_read:
  era: Scaling & Foundation Models (2020-2022)
  order: 14
is_high_impact: true
summary: Split images into 16x16 patches and processed them with a standard transformer. Proved the transformer is not language-specific. With sufficient data, ViT matches or exceeds CNNs on vision tasks. Launched the entire Vision Transformer field.
tags:
- paper
updated: '2026-11-19'
sources:
- url: https://arxiv.org/abs/2010.11929
  title: An Image is Worth 16x16 Words (ViT)
---

## Why It Matters

Split images into 16x16 patches, treat each patch as a token, and run a standard transformer. Proved that the transformer architecture is not language-specific — it works equally well for vision. Launched the entire Vision Transformer field.

## Also Noted

Proved that a pure transformer applied directly to image patches, with no convolutional layers whatsoever, matches or exceeds CNNs when pretrained on sufficient data. Shattered the assumption that inductive biases like locality and translation invariance are necessary for vision. Launched the entire ViT ecosystem.
