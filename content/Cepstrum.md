---
created: 2026-05-21
aliases:
  - "倒頻譜"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Homomorphic processing]]"
tags:
  - "adsp"
  - "cepstrum"
source:
  - "[[ADSP Write3 filters and homomorphic processing]]"
pages:
  - "ADSP_Write3/page_042.png"
---

# Cepstrum

Cepstrum 是把 spectrum 取 log 後再 inverse transform 的結果。若 $y[n]=x[n]*h[n]$，在 cepstrum domain 可近似分離成 source 與 filter 的加總。

常見詞彙：cepstrum 對應 spectrum，quefrency 對應 frequency，lifter 對應 filter。

## 講義截圖

![Cepstrum process](assets/adsp/ADSP_Write3_p042_cepstrum_process.png)

