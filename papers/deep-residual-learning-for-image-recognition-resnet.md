---
id: paper/deep-residual-learning-for-image-recognition-resnet
type: paper
slug: deep-residual-learning-for-image-recognition-resnet
schema_version: 3.0
title: Deep Residual Learning for Image Recognition
aliases:
- ResNet
authors: He et al.
year: 2015
url: https://arxiv.org/abs/1512.03385
topics:
- research-topic/neural-networks
must_read:
  era: Deep Learning Revolution (2012-2015)
  order: 22
is_high_impact: false
citation_signals:
  cited_by_count: 18258
  venue: CVPR 2016
  observed_at: '2026-11-23'
  source: https://openalex.org/W2949650786
summary: 'Introduces residual learning: layers learn residual functions with reference to their inputs, which eases the training of networks substantially deeper than those used before.'
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/1512.03385
  title: Deep Residual Learning for Image Recognition
- url: https://openaccess.thecvf.com/content_cvpr_2016/html/He_Deep_Residual_Learning_CVPR_2016_paper.html
  title: Deep Residual Learning for Image Recognition
locked:
- citation_signals.venue
---

## Why It Matters

The authors report:

- residual networks are easier to optimize and gain accuracy from considerably increased depth;
- on ImageNet, nets of up to 152 layers, 8 times deeper than VGG nets with lower complexity; an ensemble reached 3.57% test error and won first place in the ILSVRC (ImageNet Large Scale Visual Recognition Challenge) 2015 classification task;
- a 28% relative improvement on COCO object detection, and first places in ImageNet detection and localization and COCO detection and segmentation in 2015.
