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

# Hawkes report ADSP course alignment

這篇是 Hawkes/LOB 報告和 ADSP 課程的對齊筆記。它的用途是避免報告看起來像純金融數學或純隨機過程，而是明確寫成 advanced signal processing。

## Core Thesis

Hawkes process is relevant to ADSP because it models an irregularly sampled event signal by estimating history-dependent conditional intensity and event-response kernels.

換成中文：Hawkes process 把「事件何時發生」當成訊號本體，用 conditional intensity 表示目前 activity level，用 kernels 表示歷史事件對未來事件的 response。

## ADSP Course Connections

1. Signal representation：從 waveform $x[n]$ 轉到 event stream $\{(t_n,k_n,v_n)\}$，連到 [[Limit order book event stream]]。
2. Filtering / memory：kernel $\phi_{ij}(t)$ 是 event-domain response，連到 [[Convolution]]。
3. Multichannel systems：不同 event type 形成 multivariate process，連到 [[Hawkes kernel matrix]] 和 MIMO-style cross-channel coupling。
4. Random signal processing：conditional intensity、covariance、second-order statistics 連到 [[Probability for random signals]] 與 [[Covariance matrix]]。
5. Stability：branching matrix 的 spectral radius 連到 [[Eigenvalues and eigenvectors]]。
6. Estimation：kernel estimation 連到 system identification / inverse problem，Bacry-Muzy 也連到 [[Wiener filter]] 的 second-order thinking。

## Mathematical Statistics Connections

Hawkes process 也需要數理統計，但這些連結是輔助，不是報告主線：

- [[Conditional expectation]]：conditioning on event history。
- [[Conditional distribution]]：marked Hawkes 的 mark distribution。
- [[Likelihood function]]：point-process likelihood。
- [[Maximum likelihood estimator]]：parametric kernel fitting。
- [[Expectation]]：intensity 和 branching ratio 的平均解釋。

## Report Framing

不要把題目寫成「Hawkes Process in Finance」。比較適合的題目是：

**Limit Order Book Event Streams as Advanced Signal Processing: Conditional Intensity, Event-Response Kernels, and Marked Hawkes Models**

這樣題目會明確表達：金融資料只是 application，ADSP 主體是 event-stream signal modeling。

## Links

- [[Hawkes process limit order book project]]
- [[Hawkes process as event-domain filtering]]
- [[Hawkes project notation]]
- [[Hawkes model comparison]]
- [[Probability for random signals]]
- [[Convolution]]
- [[Wiener filter]]
- [[Conditional expectation]]
- [[Likelihood function]]
