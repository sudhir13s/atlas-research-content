---
id: paper/clip-learning-transferable-visual-models
type: paper
slug: clip-learning-transferable-visual-models
schema_version: 1.0
title: 'CLIP: Learning Transferable Visual Models'
aliases:
- CLIP
authors: Radford et al.
year: 2021
url: https://arxiv.org/abs/2103.00020
arxiv_id: '2103.00020'
topics:
- research-topic/vision
- research-topic/multimodal
must_read:
  era: Scaling & Foundation Models (2020-2022)
  order: 13
is_high_impact: false
citation_signals:
  cited_by_count: 61476
  venue: arXiv (Cornell University)
  observed_at: '2026-11-20'
  source: https://openalex.org/W3135367836
summary: Trained on 400M image-text pairs from the internet, CLIP learned to connect vision and language. Enabled zero-shot image classification — describe any category in text and CLIP classifies images into it. The foundation of all vision-language models.
tags:
- paper
updated: '2026-11-20'
sources:
- url: https://arxiv.org/abs/2103.00020
  title: 'CLIP: Learning Transferable Visual Models'
---

## Why It Matters

Trained image and text encoders jointly on 400M image-text pairs from the internet, enabling zero-shot image classification by matching images to text descriptions. Eliminated the need for labeled datasets in many vision tasks. The vision-language alignment it pioneered underpins DALL-E, Stable Diffusion, and every modern VLM.

## Also Noted

Trained dual image-text encoders on 400M web pairs using contrastive learning, creating a shared embedding space where images and text are directly comparable. Enabled zero-shot classification, image search, and became the vision backbone for DALL-E, Stable Diffusion, and most VLMs. The foundational vision-language alignment method that the entire multimodal AI field is built upon.
