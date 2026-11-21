---
id: paper/sora-video-generation-models-as-world-simulators
type: paper
slug: sora-video-generation-models-as-world-simulators
schema_version: 1.0
title: Video generation models as world simulators
aliases:
- Sora (World Simulators)
authors: Brooks et al.
year: 2024
url: https://openai.com/index/video-generation-models-as-world-simulators/
topics:
- research-topic/video
must_read:
  era: LLM Era & Agents (2022-Present)
  order: 2
is_high_impact: false
summary: An OpenAI technical report on training text-conditional diffusion models on videos and images of variable durations, resolutions and aspect ratios, using a transformer on spacetime patches of video and image latent codes.
tags:
- paper
updated: '2026-11-21'
sources:
- url: https://openai.com/index/video-generation-models-as-world-simulators/
  title: Video generation models as world simulators
---

## Why It Matters

The report states that its largest model, Sora, can generate a minute of high fidelity video; model and implementation details are not included.

- Diffusion transformers scale effectively as video models, with sample quality improving markedly as training compute increases.
- The authors report capabilities that emerge at scale, such as 3D consistency and, often though not always, long-range coherence and object permanence.
- They suggest scaling video generation models is a promising path towards general purpose simulators of the physical world.
