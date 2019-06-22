---
title: MIPT Deep Learning Club \#13
redirect_from: "/13-dl"
lang: en
ref: 13dl
date: 2018-03-30 03:00:01 +03:00

tags:
- MIPT DL Club
- NLP
- Softmax
- RNN
- Language Modeling
header:
  teaser: "/images/mipt-club/dl13.jpg"
---

_Taras Khakhulin_ about ["Breaking the Softmax Bottleneck: A High-Rank RNN Language Model"](https://arxiv.org/abs/1711.03953)

The problem of constructing the Language model was considered as a factorization of matrix. Authors showed that Softmax has a bottleneck which affects the expressive power of the model. Also they proposed to solve such a problem using the Mixture of Softmax.

Results mentioned in the paper are impressive. A lot of experiments were conducted and state-of-the-art results were achieved on a big number of datasets.

To conclude, even very strong RNN Language model's expressive power will be restricted because of a high rank representation of natural language.

{% include video id="IXI5EkCyVnA" provider="youtube" %}
