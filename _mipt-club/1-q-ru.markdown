---
title: MIPT Quantum Club \#1
lang: ru
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

_Anton Karazeev_ про применение нейронных сетей (Ограниченных машин Больцмана, RBM) для томографии квантовых состояний

Томография квантовых состояний - дело трудоёмкое, требует большого числа измерений для достижения хорошей точности.
В Nature Physics была недавно [опубликована статья](https://www.nature.com/articles/s41567-018-0048-5), в которой предлагается метод, использующий нейронные сети (RBM) и позволяющий за меньшее (на порядки) число измерений достигать хороших результатов в томографии квантовых состояний.

Был рассмотрен механизм обучения Restricted Boltzmann Machines (RBM) - на основе Contrastive Divergence, а также сэмплирования из обученной RBM - на основе метода Gibbs Sampling.

Дополнительные ссылки:
- [Подробнее про томографию квантовых состояний](http://research.physics.illinois.edu/QI/Photonics/Tomography/)
- [Tutorial for RBM](http://deeplearning.net/tutorial/rbm.html)
- [A Practical Guide to Training RBM by Hinton](https://www.cs.toronto.edu/~hinton/absps/guideTR.pdf)

{% include video id="bCD3rRgc5Oc" provider="youtube" %}
