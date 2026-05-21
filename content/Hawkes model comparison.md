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
| Compound Hawkes | event time/type + size | jumps with random marks/sizes | closer [[Limit order book event stream|LOB]] simulator | size distribution may still be stylized |
| Neural marked Hawkes | history-dependent marks | neural embedding + conditional density | flexible multimodal volumes | less interpretable; training-dependent |

## ADSP Course Connection

這張比較表要服務 ADSP 報告，不是金融模型排行榜。比較角度應放在 signal representation、kernel response、random signal estimation、stability、以及 interpretability vs flexibility。

## Mathematical Statistics Connection

Poisson baseline 連到 independent increments；Hawkes model 連到 [[Conditional intensity]]；marked/neural models 連到 [[Conditional distribution]]；估計方法連到 [[Likelihood function]] 與 [[Maximum likelihood estimator]]。

## Links

- [[Hawkes process limit order book project]]
- [[Hawkes report ADSP course alignment]]
- [[Hawkes process]]
- [[Multivariate Hawkes process]]
- [[Hawkes kernel matrix]]
- [[Nonparametric Hawkes estimation]]
- [[Compound Hawkes process]]
- [[Marked Hawkes process]]
- [[Neural marked Hawkes process]]
- [[Conditional intensity]]
- [[Conditional distribution]]
- [[Likelihood function]]
- [[Maximum likelihood estimator]]
