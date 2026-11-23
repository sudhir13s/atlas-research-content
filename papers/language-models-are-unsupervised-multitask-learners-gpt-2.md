---
id: paper/language-models-are-unsupervised-multitask-learners-gpt-2
type: paper
slug: language-models-are-unsupervised-multitask-learners-gpt-2
schema_version: 3.0
title: Language Models are Unsupervised Multitask Learners
aliases:
- GPT-2
authors: Radford et al.
year: 2019
url: https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf
topics:
- research-topic/llm
must_read:
  era: Attention & Transformers (2016-2019)
  order: 18
is_high_impact: false
summary: Shows that language models begin to learn tasks such as question answering, translation, reading comprehension and summarization without explicit supervision when trained on WebText, a new dataset of millions of webpages.
tags:
- paper
updated: '2026-11-21'
sources:
- url: https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf
  title: Language Models are Unsupervised Multitask Learners
---

## Why It Matters

The authors report:

- given a document plus questions, answers reach 55 F1 on the CoQA dataset, matching or exceeding 3 of 4 baseline systems without their 127,000+ training examples;
- model capacity is essential to zero-shot task transfer, and increasing it improves performance log-linearly across tasks;
- GPT-2, a 1.5B-parameter Transformer, achieves state-of-the-art results on 7 of 8 language modeling datasets zero-shot, while still underfitting WebText.
