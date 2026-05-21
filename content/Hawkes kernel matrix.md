---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Hawkes process limit order book project]]"
tags:
  - "adsp"
  - "project-concept"
  - "hawkes-process"
---

# Hawkes kernel matrix

Hawkes kernel matrix 的 entry $\phi_{ij}(t)$ 表示 type $j$ 的過去事件，對 type $i$ 未來 [[Conditional intensity]] 的影響。對角線是 self-excitation；非對角線是 cross-excitation。

在 [[Multivariate Hawkes process]] 中，kernel matrix 是可解釋性的主要來源：它告訴你哪一類 LOB event 會激發哪一類後續 event。

## ADSP Course Connection

如果 LTI filter 的 impulse response 是 $h(t)$，Hawkes kernel $\phi_{ij}(t)$ 就是 event-domain response。差別是輸入不是 regular sampled $x[n]$，而是 event impulses $dN_j(t)$。因此它自然連到 [[Convolution]]、multichannel systems、以及 [[Probability for random signals]]。

若把 kernel 對時間積分成 matrix $G$，就能用 eigenvalue/spectral radius 判斷 stability，連到 [[Eigenvalues and eigenvectors]]。

## Mathematical Statistics Connection

kernel matrix 是 dependence structure 的估計目標。它可用 likelihood-based methods 估，也可用 second-order statistics 估，連到 [[Covariance matrix]] 與 [[Maximum likelihood estimator]]。

## Links

- [[Conditional intensity]]
- [[Multivariate Hawkes process]]
- [[Hawkes branching ratio]]
- [[Nonparametric Hawkes estimation]]
- [[Convolution]]
- [[Probability for random signals]]
- [[Eigenvalues and eigenvectors]]
- [[Covariance matrix]]
- [[Maximum likelihood estimator]]
