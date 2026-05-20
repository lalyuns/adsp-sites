---
created: 2026-05-21
aliases:
  - "template matching"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Popular filters]]"
tags:
  - "adsp"
  - "filters"
  - "correlation"
source:
  - "[[ADSP Write3 filters and homomorphic processing]]"
pages:
  - "ADSP_Write3/page_016.png"
---

# Matched filter

Matched filter 用 time-reversed conjugate $h^*[-n]$ 和 input 做 correlation，常用於 demodulation、pattern recognition、similarity measurement。

若 template 出現在訊號中，matched filter output 會在對齊位置產生 peak。實作時常需要 normalization，避免 amplitude 大小主導相似度。

## 講義截圖

![Matched filter](assets/adsp/ADSP_Write3_p016_matched_filter.png)

