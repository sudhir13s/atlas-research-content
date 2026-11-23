---
id: paper/bert-pre-training-of-deep-bidirectional-transformers
type: paper
slug: bert-pre-training-of-deep-bidirectional-transformers
schema_version: 1.0
title: 'BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding'
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
citation_signals:
  cited_by_count: 83666
  venue: NAACL 2019
  observed_at: '2026-11-23'
  source: https://openalex.org/W2896457183
summary: Introduces BERT (Bidirectional Encoder Representations from Transformers), a language representation model pre-trained on unlabeled text by conditioning on both left and right context in all layers.
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://arxiv.org/abs/1810.04805
  title: 'BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding'
- url: https://aclanthology.org/N19-1423/
  title: 'BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding'
locked:
- citation_signals.venue
---

## Why It Matters

The pre-trained model is fine-tuned with just one additional output layer for tasks such as question answering and language inference.

- No substantial task-specific architecture changes are needed.
- The authors report new state-of-the-art results on eleven natural language processing tasks, including a GLUE (General Language Understanding Evaluation) score of 80.5% and a SQuAD v1.1 question answering test F1 of 93.2.
