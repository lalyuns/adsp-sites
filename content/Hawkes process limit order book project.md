---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Advanced digital signal processing]]"
tags:
  - "adsp"
  - "project-report"
  - "hawkes-process"
  - "limit-order-book"
---

# Hawkes process limit order book project

這個題目適合寫成：

**Hawkes process models for limit order book event streams: interpretable kernels, marked dynamics, and neural mark distributions.**

報告核心論點：LOB 不是規則時間取樣的 signal，而是 asynchronous event stream。ADSP 的角色在這裡不是 FFT，而是 stochastic signal/event modeling：用 intensity、kernel、marks 描述 event dependence，並比較可解釋模型與 neural model。

## Unified Notation

- event sequence：$\mathcal{H}_t=\{(t_n,k_n,v_n):t_n<t\}$。
- $t_n$：event time。
- $k_n\in\{1,\ldots,K\}$：event type，例如 limit order、market order、cancel，bid/ask side。
- $v_n$：mark，例如 order size/volume。
- $N_i(t)$：type $i$ 的 counting process。
- $\lambda_i(t)$：type $i$ 的 conditional intensity。

## Method Chain

1. [[Hawkes process]]：單變量 self-excitation。
2. [[Multivariate Hawkes process]]：event types 之間的 cross-excitation。
3. [[Hawkes kernel matrix]]：用 $\phi_{ij}(t)$ 解釋 type $j$ 對 type $i$ 的影響。
4. [[Nonparametric Hawkes estimation]]：用 second-order statistics 反推 kernel shape。
5. [[Marked Hawkes process]] / [[Compound Hawkes process]]：把 order size 加進 event model。
6. [[Neural marked Hawkes process]]：用 history embedding 讓 mark distribution conditioned on past events。

## Report Structure Suggestion

1. Abstract：LOB as event stream; compare classical, compound, and neural marked Hawkes.
2. Introduction：為什麼 LOB dynamics 可用 point process，而不是 regular time-series。
3. Hawkes process background：使用 [[Hawkes project notation]]。
4. Nonparametric kernel estimation：Bacry and Muzy 的 second-order statistics。
5. Compound Hawkes for LOB：order size and simulator stylized facts。
6. Neural marked Hawkes：history-dependent volume distribution。
7. Discussion：interpretability vs flexibility。
8. Conclusion and references。

核心 paper notes：[[Bacry Muzy 2015 Hawkes second-order statistics]]、[[Compound Hawkes process for LOB order size modeling]]、[[Neural marked Hawkes process for LOB]]。

## Figures For Report

![Multivariate Hawkes intensity and kernel matrix notation](assets/adsp/projects/hawkes_multivariate_definition_cropped.png)

![Calibrated excitation and inhibition kernels for LOB event types](assets/adsp/projects/hawkes_compound_calibrated_kernels_cropped.png)

![Neural marked Hawkes architecture with history-conditioned mark distributions](assets/adsp/projects/hawkes_neural_marked_architecture_cropped.png)
