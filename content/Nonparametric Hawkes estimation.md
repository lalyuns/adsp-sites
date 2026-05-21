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

# Nonparametric Hawkes estimation

Nonparametric Hawkes estimation 不先指定 kernel 必須是 exponential、power-law 或其他固定形狀，而是從資料估計 [[Hawkes kernel matrix]] 的 shape。

在 [[Bacry Muzy 2015 Hawkes second-order statistics]] 中，核心想法是用 second-order statistics 建立和 kernel 有關的 integral equations。

## ADSP Course Connection

這最像 ADSP 裡的 system identification / inverse problem：已知 observed signal，反推 system response。Bacry-Muzy 用 second-order statistics，和 [[Wiener filter]]、correlation-based random signal processing 的精神接近。

## Mathematical Statistics Connection

它用 empirical covariance/correlation 估 unknown function，連到 [[Covariance matrix]]、[[Expectation]]，也可和 likelihood-based [[Maximum likelihood estimator]] 形成對照。

## Links

- [[Bacry Muzy 2015 Hawkes second-order statistics]]
- [[Hawkes kernel matrix]]
- [[Conditional intensity]]
- [[Wiener filter]]
- [[Probability for random signals]]
- [[Covariance matrix]]
- [[Expectation]]
- [[Maximum likelihood estimator]]
