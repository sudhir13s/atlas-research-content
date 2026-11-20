---
id: paper/denoising-diffusion-probabilistic-models-ddpm
type: paper
slug: denoising-diffusion-probabilistic-models-ddpm
schema_version: 1.0
title: Denoising Diffusion Probabilistic Models (DDPM)
aliases:
- DDPM
authors: Ho et al.
year: 2020
url: https://arxiv.org/abs/2006.11239
arxiv_id: '2006.11239'
topics:
- research-topic/diffusion
must_read:
  era: Scaling & Foundation Models (2020-2022)
  order: 17
is_high_impact: false
citation_signals:
  cited_by_count: 20791
  venue: arXiv (Cornell University)
  observed_at: '2026-11-20'
  source: https://openalex.org/W3036167779
summary: The foundational diffusion model paper. Showed that iteratively denoising random noise could generate high-quality images. This denoising approach replaced GANs as the dominant generation paradigm and led directly to Stable Diffusion, DALL-E, and Midjourney.
tags:
- paper
updated: '2026-11-20'
sources:
- url: https://arxiv.org/abs/2006.11239
  title: Denoising Diffusion Probabilistic Models (DDPM)
---

## Why It Matters

Showed that gradually denoising Gaussian noise, trained with a simple mean-squared-error loss, produces images rivaling GANs without adversarial training instability. The simplicity of the training objective is what made diffusion models practical for everyone. THE foundational paper for the entire diffusion-based generation revolution.
