---
layout: post
title:  "Building GPT from scratch: overview"
date:   2026-06-21 17:10:00 +0530
categories: AI Infrastructure
---
Before going deeper into AI infrastructure, I wanted to refresh my mental model of a neural network by building a transformer from scratch. 

The video by Andrej Karpathy [Let's Build GPT: from scratch, in code, spelled out](https://www.youtube.com/watch?v=kCc8FmEb1nY) is what I worked through. My implementation: [github.com/vinayak-g-bhat/gpt](https://github.com/vinayak-g-bhat/gpt).
The video implements paper on which GPT and many modern LLMs are based: [Attention Is All You Need](https://arxiv.org/abs/1706.03762).

## Program structure
* Download the corpus [TinyShakespeare](https://raw.githubusercontent.com/karpathy/char-rnn/master/data/tinyshakespeare/input.txt)
* Split the text into two parts. One for training and one for evaluation.
* Implement tokenization routines: build vocabulary, encode and decode methods
* Implement method for  getting a batch of data, either for training or evaluation.
* Choose a block size, and reason about what it means semantically
* Build deep learning layers, most importantly self-attention.
* Add other layers like residual layer, normalization layers and dropouts.
* Training loop and evaluting loss.
* Generate tokens from prompt.

## Side-quests
* Tensor memory management in PyTorch, including strides.
* How Pytorch autograd works under the hood.
* Measuring memory consumed during the training and evaluation.
* Comparing MPS (MacBook GPU) runs and CPU runs against Karpathy's reported numbers.
* Loss comparison between Karpathy's runs and mine on a local Macbook.
* The math behind loss functions.

## What's next
This post is the summary I want to be able to come back to. Each of the side-quests above is more interesting than the high-level walkthrough, so I'll write each up as its own post over the coming days.