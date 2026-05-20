---
created: 2026-05-21
aliases:
  - "Discrete Hilbert transform"
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
  - "ADSP_Write3/page_008.png"
---

# Hilbert transform filter

Discrete Hilbert transform filter 近似把正頻率乘上 $-j$、負頻率乘上 $j$，用來產生 analytic signal、instantaneous frequency，也可用於 edge detection。

它是一種 odd symmetric filter，因此和 [[Four FIR filter symmetry types]] 的 Type 3/4 有關。

## 講義截圖

![Discrete Hilbert transform](assets/adsp/ADSP_Write3_p008_discrete_hilbert_transform.png)

