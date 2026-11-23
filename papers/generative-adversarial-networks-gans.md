---
id: paper/generative-adversarial-networks-gans
type: paper
slug: generative-adversarial-networks-gans
schema_version: 3.0
title: Generative Adversarial Networks (GANs)
aliases:
- GANs
authors: Goodfellow et al.
year: 2014
url: https://arxiv.org/abs/1406.2661
topics:
- research-topic/neural-networks
- research-topic/diffusion
must_read:
  era: Deep Learning Revolution (2012-2015)
  order: 23
is_high_impact: false
summary: Generator vs discriminator competition produced the first photorealistic image generation. Spawned StyleGAN, CycleGAN, and thousands of variants. The dominant generative paradigm before diffusion models took over in 2022.
tags:
- paper
updated: '2026-11-19'
sources:
- url: https://arxiv.org/abs/1406.2661
  title: Generative Adversarial Networks (GANs)
---

## Why It Matters

A generator creates fake data while a discriminator tries to catch it — training both makes the generator produce increasingly realistic output. Launched the entire field of neural image generation and inspired thousands of variants before diffusion models took over.

## Also Noted

Introduced the adversarial training framework where a generator and discriminator compete, producing increasingly realistic outputs. Dominated neural image generation for seven years before diffusion models took over. Understanding GANs is essential context for why diffusion models were such a breakthrough — they solved GAN training instability.
