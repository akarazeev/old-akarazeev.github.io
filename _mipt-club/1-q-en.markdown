---
title: MIPT Quantum Club \#1
redirect_from: "/1-q"
lang: en
ref: 1q
date: 2018-03-03 03:00:01 +03:00
tags:
- Neural Network
- MIPT Q Club
- RBM
- Quantum State Tomography
header:
  teaser: "/images/mipt-club/q1.jpg"
---

_Anton Karazeev_ on application of neural networks (Restricted Boltzmann Machines, RBM) for quantum state tomography qst

Tomography of quantum states is labour-intensive process which demands a huge number of measurements to achieve good precision. [The paper](https://www.nature.com/articles/s41567-018-0048-5) was published recently in Nature Physics - authors propose a method which uses neural networks (RBM) and allows to achieve good results of quantum state tomography using much smaller number of measurements.

Training process of Restricted Boltzmann Machines (based on Contrastive Divergence) and sampling from already trained RBM based on Gibbs Sampling were considered (it’s also called "daydreaming" phase of an RBM).

Additional links:
- [More on quantum state tomography](http://research.physics.illinois.edu/QI/Photonics/Tomography/)
- [Tutorial for RBM](http://deeplearning.net/tutorial/rbm.html)
- [A Practical Guide to Training RBM by Hinton](https://www.cs.toronto.edu/~hinton/absps/guideTR.pdf)

{% include video id="bCD3rRgc5Oc" provider="youtube" %}
