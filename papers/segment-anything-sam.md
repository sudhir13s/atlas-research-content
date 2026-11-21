---
id: paper/segment-anything-sam
type: paper
slug: segment-anything-sam
schema_version: 1.0
title: Segment Anything
aliases:
- Segment Anything Model (SAM)
- SAM
authors: Kirillov et al.
year: 2023
url: https://arxiv.org/abs/2304.02643
arxiv_id: '2304.02643'
topics:
- research-topic/vision
must_read:
  era: LLM Era & Agents (2022-Present)
  order: 4
is_high_impact: false
citation_signals:
  cited_by_count: 19456
  venue: ICCV 2023
  observed_at: '2026-11-20'
  source: https://openalex.org/W4390874575
summary: 'Introduces the Segment Anything project: a new task, model and dataset for image segmentation, with a model designed and trained to be promptable.'
tags:
- paper
updated: '2026-11-21'
sources:
- url: https://arxiv.org/abs/2304.02643
  title: Segment Anything
- url: https://openaccess.thecvf.com/content/ICCV2023/html/Kirillov_Segment_Anything_ICCV_2023_paper.html
  title: Segment Anything
locked:
- citation_signals.venue
---

## Why It Matters

Using the model in a data collection loop, the authors built SA-1B: over 1 billion masks on 11 million licensed and privacy-respecting images.

- The model transfers zero-shot to new image distributions and tasks, often competitive with or superior to prior fully supervised results, the authors report.
- The Segment Anything Model (SAM) and SA-1B were released.
