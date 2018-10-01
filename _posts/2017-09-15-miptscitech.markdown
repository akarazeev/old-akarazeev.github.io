---
title: MIPT SciTech Club
date: 2017-09-15 03:00:01 +03:00
tags:
- MIPT
- Deep Learning
- Clubs
- Quantum
- Bioinformatics
layout: post
---

**MIPT SciTech Club** at [Facebook](https://www.facebook.com/scitechmipt/)

---

**MIPT Bioinf Club #1**

_Daria Romanovskaia_ about Nature paper "Predicting the sequence specificities of DNA- and RNA-binding proteins by deep learning" (https://www.nature.com/articles/nbt.3300)

Authors of this paper proposed new method based on Deep Learning (DL) to predict binding sites of RNA- and DNA-binding proteins that are regulators of gene expression.

Method is based on Convolutional Neural Networks (CNN) that help to assign affinity score to every sequence.

As a result - proposed method is very accurate and it works much better than already existent programs for searching of biological motifs in DNA and RNA. A useful add-on is the visualization of maps of potentially pathogenic mutations.

{% include video id="_NagRpo_Eww" provider="youtube" %}

_Michael Chertkov_ about "Science Application Informed Machine Learning" [#ML in Physics, application of #GANs to the problem of turbulence, controlling of energy networks in USA, etc.]

Abstract: Thanks to IT industry push, Machine Learning (ML) capabilities are in a phase of tremendous growth, and there is great opportunity to point these practically powerful tools toward modeling specific to applications, e.g. in natural and engineering sciences. The challenge is to incorporate domain expertise from traditional scientific discovery into next-generation ML models. We propose to develop new theoretical and algorithmic methodology that extends cutting-edge ML tools and merge them with application-specific knowledge stated in the form of constraints, symmetries, conservation laws, phenomenological assumptions and other examples of domain expertise regarding relevant degrees of freedom.

The emerging methodology is illustrated on the following four enabling examples:
1. Topology and Parameter Estimation in Power Grids [IEEE CONES 2018/ https://arxiv.org/abs/1710.10727]
2. Acceleration of Computational Fluid Dynamics with Deep Learning [APS/DFD2017 abstract + work in progress]
3. Learning Graphical Models [Science 2018/ https://arxiv.org/abs/1612.05024] and #NIPS2016/ https://arxiv.org/abs/1605.07252]
4. Renormalization of Tensor Networks (Graphical Models) [AISTATS 2018/ https://arxiv.org/abs/1801.01649 and #ICML 2018/ https://arxiv.org/abs/1803.05104]

{% include video id="r1EImGv0NxE" provider="youtube" %}

**MIPT Q Club #2**

_Anton Karazeev_ about optical setups that can mimic the functionality of artificial neural networks (Optical Neural Networks) - paper [1], Nature, 2017.

The linear (and some nonlinear) transformations can be applied at the speed of light in optical setups. It's well known from physics that a lens performs Fourier transform without any energy consumption and consequently some matrix operations can be performed optically without consumption of energy.

These advantages in speed and energy consumption make optical neural networks (ONNs) fairly prospective field of research.

Authors [1] implemented nanophotonic circuit and classified spoken vowels with it (they "trained" Mach-Zender interferometer by changing the phase shifts of laser beam). According to the paper, the nonlinearity wasn't implemented optically but was calculated on classical computer. Perhaps the training phase and nonlinearity will be implemented inside the optical circuit in next versions.

- [1] Deep learning with coherent nanophotonic circuits (https://www.nature.com/articles/nphoton.2017.93)
- [2] Mach–Zehnder interferometer (https://en.wikipedia.org/wiki/Mach–Zehnder_interferometer)
- [3] Computing by Means of Physics-Based Optical Neural Networks (https://arxiv.org/abs/1006.1434)
- \*OIU - Optical Interference Unit

{% include video id="bpkuyGXvbEU" provider="youtube" %}

**MIPT DL Club #13**

_Taras Khakhulin_ about "Breaking the Softmax Bottleneck: A High-Rank RNN Language Model" (https://arxiv.org/abs/1711.03953)

The problem of constructing the Language model was considered as a factorization of matrix. Authors showed that Softmax has a bottleneck which affects the expressive power of the model. Also they proposed to solve such a problem using the Mixture of Softmax.

Results mentioned in the paper are impressive. A lot of experiments were conducted and state-of-the-art results were achieved on a big number of datasets.

To conclude, even very strong RNN Language model's expressive power will be restricted because of a high rank representation of natural language.

{% include video id="IXI5EkCyVnA" provider="youtube" %}

**MIPT DL Club #12**

_Anton Karazeev_ on classical methods of keyphrases extraction from [biomedical] texts: statistical (TF-IDF) and graphical (TextRank).

Besides them, newly proposed methods were discussed: based on Information Theory (Kullback-Leibler divergence) using word2gauss algorithm.

- word2gauss (https://github.com/seomoz/word2gauss)
- [2015, ICLR] Word Representations via Gaussian Embedding (https://arxiv.org/abs/1412.6623)
- [2017] Multimodal Word Distributions (https://arxiv.org/abs/1704.08424)
- [2018] EmbedRank: Unsupervised Keyphrase Extraction using Sentence Embeddings (https://arxiv.org/abs/1801.04470)
- [2010] Keyword Extraction Using Word Co-occurrence (https://www.researchgate.net/publication/224179686_Ke)

{% include video id="D9nzI0EO9ok" provider="youtube" %}

**MIPT Q Club #1**

_Anton Karazeev_ on application of neural networks (Restricted Boltzmann Machines, #RBM) for quantum state tomography #qst

Tomography of quantum states is labour-intensive process which demands a huge number of measurements to achieve good precision. The paper https://www.nature.com/articles/s41567-018-0048-5 was published recently in Nature Physics - authors propose a method which uses neural networks (RBM) and allows to achieve good results of quantum state tomography using much smaller number of measurements.

Training process of Restricted Boltzmann Machines (based on Contrastive Divergence) and sampling from already trained RBM based on Gibbs Sampling were considered (it’s also called “daydreaming” phase of an RBM).

Additional links:
- More on quantum state tomography - http://research.physics.illinois.edu/…/Photonics/Tomography/
- Tutorial for RBM - http://deeplearning.net/tutorial/rbm.html
- A Practical Guide to Training RBM by Hinton - https://www.cs.toronto.edu/~hinton/absps/guideTR.pdf

{% include video id="bCD3rRgc5Oc" provider="youtube" %}

**MIPT DL Club #11**

_Danil Lykov_ on applications of attention-mechanisms

Besides well-known paper "Show, Attend and Tell" by Bengio et al. (https://arxiv.org/abs/1502.03044), a new paper about "AttnGAN" (https://arxiv.org/abs/1711.10485) by Microsoft was mentioned - it’s a generative network which allows to generate image given text description (caption -> image)

{% include video id="ZH77RI5ERLw" provider="youtube" %}

**MIPT DL Club #10**

_Danil Lykov_ about Hinton's paper on "Dynamic Routing Between Capsules" (https://arxiv.org/abs/1710.09829)

New method of information transmitting from different areas of image is proposed (in convolutional networks the Pooling-layer is responsible for that).

Proposed method allows to recognise overlapped objects more effectively and better process ambiguous images.

Moreover the authors of this paper use interesting method of regularisation - divergence of recovered vector from low dimensional space between the original one.

Useful video: https://www.youtube.com/watch?v=pPN8d0E3900

Hinton's comment on Reddit: https://www.reddit.com/r/MachineLearning/comments/7ew7ba/d_capsule_networks_capsnets_tutorial/dq8yc9p/

{% include video id="8R3gXmh1F0c" provider="youtube" %}

**MIPT DL Club #9**

_Emil Zakirov_ about “Outrageously Large Neural Networks: The Sparsely-Gated Mixture-of-Experts Layer” (https://arxiv.org/abs/1701.06538)

Authors studied conditional computation layer called Mixture of Experts (MoE) with different parts activated for different samples. Due to this fact the number of parameters can be increased by 1000 while preserving amount of time per one sample.

One of the reason for such a good paper's result is the huge size of dataset with about 1 billion of different languages sentences. Authors beat SOTA methods in tasks of language modelling and multilingual translation - that's not very surprising because of researchers from Google Translators who are mentioned as the authors.

{% include video id="nNZceFX2tQU" provider="youtube" %}

**MIPT DL Club #8**

"Improving the Realism of Synthetic Images" - _Anton Karazeev_ about paper by Apple (Machine Learning Journal: https://machinelearning.apple.com/2017/07/07/GAN.html, full paper's text: https://arxiv.org/pdf/1612.07828.pdf)

The key novelty here is using the generator's history to improve discriminator (and performance of the proposed refiner model)

Thanks to _Valentin Malykh_ for help in understanding the paper

- MPIIGaze dataset (for appearance-based gaze estimation): https://www.mpi-inf.mpg.de/departments/computer-vision-and-multimodal-computing/research/gaze-based-human-computer-interaction/appearance-based-gaze-estimation-in-the-wild-mpiigaze/
- "Gaze estimation from synthesised images" (with some physics): https://pdfs.semanticscholar.org/c17a/332e59f03b77921942d487b4b102b1ee73b6.pdf
- Post on GANs: https://blog.statsbot.co/generative-adversarial-networks-gans-engine-and-applications-f96291965b47

{% include video id="ukt_F1FTNBA" provider="youtube" %}

**MIPT DL Club #7**

System for face recognition - _Danil Lykov_ about "DeepFace" by Facebook

Paper: https://research.fb.com/publications/deepface-closing-the-gap-to-human-level-performance-in-face-verification/

{% include video id="gCaRBYQKfbU" provider="youtube" %}

**MIPT Deep Learning Club #6**

https://vk.com/dlmipt

Synthesis of human speech from text - _Emil Zakirov_ about generative model “WaveNet” by google

- [September, 2016] WaveNet: https://deepmind.com/blog/wavenet-generative-model-raw-audio/
- [April, 2017] Tacotron: https://arxiv.org/pdf/1703.10135.pdf

{% include video id="gUdyQ5Ocr0g" provider="youtube" %}
