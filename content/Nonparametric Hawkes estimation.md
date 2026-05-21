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

在 [[Bacry Muzy 2015 Hawkes second-order statistics]] 中，核心想法是用 second-order statistics 建立和 kernel 有關的 integral equations。這個 note 要連到兩個問題：如何從 event data 估計 [[Conditional intensity]]，以及估計出的 kernel 是否能解釋 [[Limit order book event stream]] 的 interaction。
