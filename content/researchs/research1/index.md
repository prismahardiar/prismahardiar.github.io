---
title: "Mitigating Barren Plateaus in Quantum Neural Networks (QNNs) via a Hybrid Quantum–Classical Architecture with Layer-Wise Learning" 
date: 2026-01-07
tags: ["quantum machine learning","quantum neural networks","barren plateau","hybrid quantum-classical","layer-wise learning"]
author: ["Prismahardi Aji Riyantoko"]
description: "This research proposal investigates how to mitigate barren plateaus in deep Quantum Neural Networks by introducing a hybrid quantum–classical architecture trained with layer-wise learning."
summary: "This work proposes a layer-wise training strategy for hybrid QNNs to reduce gradient vanishing in deep circuits while maintaining expressivity for complex classification, evaluated on noise-free simulators using benchmark datasets and metrics such as loss, gradient variance, accuracy, and training time."
cover:
    image: ""
    alt: "Quantum Computing Research"
    relative: true
editPost:
    URL: "https://prismahardiar.github.io/"
    Text: "Quantum Computing Research"

---

---

##### Abstract
<div style="text-align: justify">
Training deep Quantum Neural Networks (QNNs) within the Noisy Intermediate-Scale Quantum (NISQ) era is severely hindered by the barren plateau phenomenon, where gradients vanish exponentially with circuit depth and optimization effectively breaks down. This project targets a key barrier to practical quantum machine learning developing a training strategy that avoids barren plateaus without sacrificing circuit expressivity for complex classification tasks relevant to innovation-driven applications aligned with SDG 9 (Industry, Innovation, and Infrastructure) and long-term advances for SDG 7 (Affordable and Clean Energy). We propose a hybrid quantum–classical QNN architecture trained via <strong>layer-wise learning</strong>: instead of end-to-end optimization, the quantum circuit is grown progressively, training one layer (or block) at a time to convergence while freezing previously learned parameters before adding the next layer. A classical neural network acts as an external optimizer to update quantum parameters during this sequential procedure. The approach will be evaluated on noise-free quantum simulators using standard reduced-dimensionality datasets (e.g., MNIST/Fashion-MNIST) and/or quantum-physics classification benchmarks (e.g., phase-of-matter classification), measuring loss, gradient variance (as a barren plateau indicator), classification accuracy, and training time across varying qubit counts and circuit depths. We hypothesize that layer-wise training yields polynomially smaller gradient variance and delivers materially higher test accuracy (≥10% improvement) than end-to-end training once circuit depth exceeds a threshold proportional to the number of qubits. While the study is limited to idealized noise-free simulation and may incur greedy suboptimality and longer wall-clock training, it aims to provide a scalable, practical pathway toward trainable deep QNNs—an essential step for unlocking future quantum-enabled applications.
</div>
---

##### Figure 1: Research Design

![](quantum-r.png)

---

##### Citation

Prismahardi Aji Riyantoko. “Mitigating Barren Plateaus in Quantum Neural Networks (QNNs) via a Hybrid Quantum–Classical Architecture with Layer-Wise Learning.”

```latex
@article{P.A.R-R1,
author = {Prismahardi Aji Riyantoko},
year = {},
title = {Mitigating Barren Plateaus in Quantum Neural Networks (QNNs) via a Hybrid Quantum--Classical Architecture with Layer-Wise Learning},
journal = {},
volume = {},
number = {},
pages = {},
url = {}}
```

---

##### Related material

+ [Proposal]()
+ [Presentation slides]()
+ [Key references]()
+ [Method overview]()
+ [Code repository]()
+ [Results summary]()
