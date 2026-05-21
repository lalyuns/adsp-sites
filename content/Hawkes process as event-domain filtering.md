---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Hawkes process limit order book project]]"
  - "[[Advanced digital signal processing]]"
tags:
  - "adsp"
  - "hawkes-process"
  - "course-connection"
  - "project-report"
---

# Hawkes process as event-domain filtering

Hawkes process 和 ADSP 的核心連結是：它把 irregular event stream 當成 signal，並用 kernels 描述 past events 對 future event intensity 的 response。

在 regular DSP 裡，LTI system 常寫成

$$
y(t)=h*x(t).
$$

在 multivariate Hawkes 裡，可以把 event history 寫成 counting-process impulses $dN_j(t)$，再由 kernel $\phi_{ij}$ 濾到 conditional intensity：

$$
\lambda_i(t)=\mu_i+\sum_j \phi_{ij} * dN_j(t).
$$

這裡 $\phi_{ij}$ 的角色很像 event-domain impulse response：type $j$ event 發生後，type $i$ 的 future rate 如何隨 lag decay。這不是傳統 waveform filter，但概念上仍是「memory + convolution + response」。

## ADSP Course Connection

- [[Convolution]]：Hawkes intensity 可看成 event impulses 與 kernels 的 convolution-like accumulation。
- [[Probability for random signals]]：regular waveform 的 randomness 變成 point process 的 randomness。
- [[Wiener filter]]：兩者都使用 second-order statistics；Bacry-Muzy 的 Wiener-Hopf equation 可視為 random signal estimation 思想的 event-stream 版本。
- [[Matrix diagonalization for transforms]]：multivariate Hawkes 的 stability 由 kernel integral matrix 的 spectral radius 控制。

## Mathematical Statistics Connection

- [[Conditional expectation]]：conditional intensity 是 conditioning on history 的 instantaneous rate。
- [[Likelihood function]]：Hawkes model 常用 point-process log-likelihood fitting。
- [[Maximum likelihood estimator]]：parametric Hawkes estimation 可用 MLE；nonparametric estimation 則更像 inverse problem。

## Links

- [[Hawkes process]]
- [[Conditional intensity]]
- [[Hawkes kernel matrix]]
- [[Multivariate Hawkes process]]
- [[Convolution]]
- [[Probability for random signals]]
- [[Conditional expectation]]
- [[Likelihood function]]
- [[Maximum likelihood estimator]]
