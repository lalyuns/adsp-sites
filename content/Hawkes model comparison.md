---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Hawkes process limit order book project]]"
tags:
  - "adsp"
  - "hawkes-process"
  - "method-comparison"
  - "project-report"
---

# Hawkes model comparison

這篇是 Hawkes 報告 discussion 的骨架。

| Model | What it explains | Mathematical object | Strength | Weakness |
|---|---|---|---|---|
| Poisson baseline | independent event arrivals | constant or time-varying rate | simple baseline | no self/cross excitation |
| Multivariate Hawkes | event clustering and cross-excitation | kernel matrix $\phi_{ij}(t)$ | interpretable dependence | kernel form/estimation matters |
| Nonparametric Hawkes | empirical kernel shapes | Wiener-Hopf inversion | avoids fixed exponential kernels | estimation and regularization complexity |
| Compound Hawkes | event time/type + size | jumps with random marks/sizes | closer LOB simulator | size distribution may still be stylized |
| Neural marked Hawkes | history-dependent marks | neural embedding + conditional density | flexible multimodal volumes | less interpretable; training-dependent |

報告論點可以寫成：classical Hawkes gives interpretable excitation kernels; compound Hawkes adds economically meaningful order sizes; neural marked Hawkes increases mark-distribution flexibility at the cost of interpretability.

連結：[[Bacry Muzy 2015 Hawkes second-order statistics]]、[[Compound Hawkes process for LOB order size modeling]]、[[Neural marked Hawkes process for LOB]]。
