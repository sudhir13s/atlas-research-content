---
id: paper/an-image-is-worth-16x16-words-vit
type: paper
slug: an-image-is-worth-16x16-words-vit
schema_version: 1.0
title: 'An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale'
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
citation_signals:
  cited_by_count: 72289
  venue: ICLR 2021
  observed_at: '2026-11-23'
  source: https://openalex.org/W3094502228
summary: 'Introduces the Vision Transformer (ViT): a standard Transformer applied directly to sequences of image patches, with no reliance on convolutional neural networks (CNNs).'
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2010.11929
  title: 'An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale'
- url: https://iclr.cc/virtual/2021/oral/3458
  title: 'An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale'
locked:
- citation_signals.venue
---

## Why It Matters

The authors show that a pure transformer on image patches can perform very well on image classification.

- Pre-trained on large amounts of data and transferred to mid-sized or small benchmarks (ImageNet, CIFAR-100, VTAB), ViT attains excellent results compared with state-of-the-art convolutional networks.
- It needs substantially fewer computational resources to train.
