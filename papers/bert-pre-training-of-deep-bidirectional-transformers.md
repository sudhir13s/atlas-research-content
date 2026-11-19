---
id: paper/bert-pre-training-of-deep-bidirectional-transformers
type: paper
slug: bert-pre-training-of-deep-bidirectional-transformers
schema_version: 1.0
title: 'BERT: Pre-training of Deep Bidirectional Transformers'
aliases:
- BERT
authors: Devlin et al.
year: 2018
url: https://arxiv.org/abs/1810.04805
arxiv_id: '1810.04805'
topics:
- research-topic/llm
must_read:
  era: Attention & Transformers (2016-2019)
  order: 19
is_high_impact: true
summary: Introduced pretrain-then-finetune for NLP. A single pretrained model adapted to dozens of tasks with just a simple output layer. Masked language modeling became the standard pretraining objective. Dominated NLP from 2018 to 2022.
tags:
- paper
updated: '2026-11-19'
sources:
- url: https://arxiv.org/abs/1810.04805
  title: 'BERT: Pre-training of Deep Bidirectional Transformers'
---

## Why It Matters

Introduced bidirectional pretraining via masked language modeling, then fine-tuning on downstream tasks. Crushed every NLP benchmark overnight and made transfer learning the default approach. BERT single-handedly ended the era of task-specific architectures and started the pretrain-then-fine-tune paradigm.
