---
id: paper/denoising-diffusion-probabilistic-models-ddpm
type: paper
slug: denoising-diffusion-probabilistic-models-ddpm
schema_version: 3.0
title: Denoising Diffusion Probabilistic Models
aliases:
- DDPM
authors: Ho et al.
year: 2020
url: https://arxiv.org/abs/2006.11239
topics:
- research-topic/diffusion
must_read:
  era: Scaling & Foundation Models (2020-2022)
  order: 17
is_high_impact: false
citation_signals:
  cited_by_count: 21081
  venue: NeurIPS 2020
  observed_at: '2026-11-23'
  source: https://openalex.org/W3036167779
summary: Synthesizes images with diffusion probabilistic models, latent variable models inspired by nonequilibrium thermodynamics, trained on a weighted variational bound linked to denoising score matching with Langevin dynamics.
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2006.11239
  title: Denoising Diffusion Probabilistic Models
- url: https://proceedings.neurips.cc/paper_files/paper/2020/hash/4c5bcfec8584af0d967f1ab10179ca4b-Abstract.html
  title: Denoising Diffusion Probabilistic Models
- url: https://arxiv.org/abs/2112.10752
  title: High-Resolution Image Synthesis with Latent Diffusion Models
locked:
- citation_signals.venue
---

## Why It Matters

The authors report an Inception score of 9.46 and a state-of-the-art FID (Fréchet Inception Distance) of 3.17 on unconditional CIFAR10, and sample quality similar to ProgressiveGAN on 256x256 LSUN.

In 2021 the latent diffusion paper described diffusion models as achieving state-of-the-art synthesis results on image data.
