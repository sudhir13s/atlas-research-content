---
id: paper/imagenet-classification-with-deep-cnns-alexnet
type: paper
slug: imagenet-classification-with-deep-cnns-alexnet
schema_version: 1.0
title: ImageNet Classification with Deep Convolutional Neural Networks
aliases:
- AlexNet
authors: Krizhevsky, Sutskever & Hinton
year: 2012
url: https://doi.org/10.1145/3065386
topics:
- research-topic/neural-networks
must_read:
  era: Deep Learning Revolution (2012-2015)
  order: 27
is_high_impact: false
citation_signals:
  cited_by_count: 118435
  venue: NeurIPS 2012
  observed_at: '2026-11-23'
  source: https://openalex.org/W2163605009
summary: Trains a large, deep convolutional neural network to classify the 1.3 million high-resolution images of the ImageNet LSVRC-2010 training set into 1000 classes.
tags:
- paper
updated: '2026-11-23'
sources:
- url: https://doi.org/10.1145/3065386
  title: ImageNet Classification with Deep Convolutional Neural Networks
- url: https://proceedings.neurips.cc/paper_files/paper/2012/hash/c399862d3b9d6b76c8436e924a68c45b-Abstract.html
  title: ImageNet Classification with Deep Convolutional Neural Networks
locked:
- citation_signals.venue
---

## Why It Matters

On the test data the authors report top-1 and top-5 error rates of 39.7% and 18.9%, considerably better than the previous state of the art.

- The network has 60 million parameters and 500,000 neurons: five convolutional layers, some followed by max-pooling, and two globally connected layers with a 1000-way softmax.
- Non-saturating neurons and an efficient GPU implementation sped up training; a new regularization method reduced overfitting.
