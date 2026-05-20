---
created: 2026-05-21
aliases:
  - "L2 and Linfinity norms"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Meta knowledge]]"
  - "[[Filter design]]"
tags:
  - "adsp"
  - "math-prerequisites"
  - "optimization"
---

# Optimization norm for filter design

Filter design 的 objective 取決於 norm。$L_2$ norm 對應 [[Least MSE FIR design]]，重視平均平方誤差；$L_\infty$ norm 對應 [[Minimax FIR design]]，重視最大誤差。

直覺：MSE 容許局部大誤差，只要平均小；minimax 會壓住最糟點。
