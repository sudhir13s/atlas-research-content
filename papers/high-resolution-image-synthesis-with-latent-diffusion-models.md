---
id: paper/high-resolution-image-synthesis-with-latent-diffusion-models
type: paper
slug: high-resolution-image-synthesis-with-latent-diffusion-models
schema_version: 1.0
title: High-Resolution Image Synthesis with Latent Diffusion Models
aliases:
- Latent Diffusion Models (LDM)
authors: Rombach et al.
year: 2021
url: https://arxiv.org/abs/2112.10752
arxiv_id: '2112.10752'
topics:
- research-topic/diffusion
must_read:
  era: LLM Era & Agents (2022-Present)
  order: 11
is_high_impact: false
citation_signals:
  cited_by_count: 37689
  venue: CVPR 2022
  observed_at: '2026-11-23'
  source: https://openalex.org/W4312933868
summary: 'Introduces latent diffusion models (LDMs): diffusion models trained in the latent space of powerful pretrained autoencoders instead of pixel space, with cross-attention layers for conditioning on inputs such as text or bounding boxes.'
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/2112.10752
  title: High-Resolution Image Synthesis with Latent Diffusion Models
- url: https://openaccess.thecvf.com/content/CVPR2022/html/Rombach_High-Resolution_Image_Synthesis_With_Latent_Diffusion_Models_CVPR_2022_paper.html
  title: High-Resolution Image Synthesis with Latent Diffusion Models
locked:
- citation_signals.venue
---

## Why It Matters

The authors report:

- a new state of the art for image inpainting;
- highly competitive results on unconditional image generation, semantic scene synthesis and super-resolution;
- substantially lower computational requirements than pixel-based diffusion models.
