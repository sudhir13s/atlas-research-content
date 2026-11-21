---
id: paper/chain-of-thought-prompting-elicits-reasoning
type: paper
slug: chain-of-thought-prompting-elicits-reasoning
schema_version: 1.0
title: Chain-of-Thought Prompting Elicits Reasoning in Large Language Models
aliases:
- Chain-of-Thought Prompting
authors: Wei et al.
year: 2022
url: https://arxiv.org/abs/2201.11903
arxiv_id: '2201.11903'
topics:
- research-topic/llm
must_read:
  era: LLM Era & Agents (2022-Present)
  order: 12
is_high_impact: true
citation_signals:
  cited_by_count: 38349
  venue: NeurIPS 2022
  observed_at: '2026-11-20'
  source: https://openalex.org/W7133224126
summary: 'Introduces chain-of-thought prompting: a large language model is given a few exemplars that show a series of intermediate reasoning steps before the answer.'
tags:
- paper
updated: '2026-11-21'
sources:
- url: https://arxiv.org/abs/2201.11903
  title: Chain-of-Thought Prompting Elicits Reasoning in Large Language Models
- url: https://proceedings.neurips.cc/paper_files/paper/2022/hash/9d5609613524ecf4f15af0f7b31abca4-Abstract-Conference.html
  title: Chain-of-Thought Prompting Elicits Reasoning in Large Language Models
locked:
- citation_signals.venue
---

## Why It Matters

Across three large language models the authors report better performance on arithmetic, commonsense and symbolic reasoning tasks.

- They describe the ability as emerging naturally in sufficiently large models.
- A 540B-parameter model prompted with eight chain-of-thought exemplars reached state-of-the-art accuracy on the GSM8K benchmark of math word problems, surpassing fine-tuned GPT-3 with a verifier.
