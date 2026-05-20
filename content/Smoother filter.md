---
created: 2026-05-21
aliases:
  - "weighted average filter"
  - "moving average"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Popular filters]]"
tags:
  - "adsp"
  - "filters"
source:
  - "[[ADSP Write3 filters and homomorphic processing]]"
pages:
  - "ADSP_Write3/page_003.png"
---

# Smoother filter

Smoother filter 是 lowpass filter 的一種，用加權平均降低高頻 noise。最簡單的 moving average 是

$$y[n]=\frac{1}{2L+1}\sum_{r=-L}^{L}x[n+r].$$

更一般地，只要 $h[n]$ 是 nonnegative、even、總和為 1，通常就能作為 smoother。

## 講義截圖

![Smoother as weighted average](assets/adsp/ADSP_Write3_p003_smoother_weighted_average.png)

