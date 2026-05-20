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

Smoother 是 low-pass intuition：把鄰近 samples 平均，壓掉快速變動。要小心 smoothing 也會模糊 edge 或 transient。

連結：[[Frequency response]]、[[Probability for random signals]]。


## 講義截圖
![Smoother as weighted average](assets/adsp/ADSP_Write3_p003_smoother_weighted_average.png)
