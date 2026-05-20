---
created: 2026-05-21
aliases:
  - "differential cepstrum"
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
  - "ADSP_Write3/page_060.png"
---

# Differential cepstrum

Differential cepstrum 用 $X'(z)/X(z)$ 取代直接取 $\log X(z)$，可避開 phase ambiguity 與 delay 問題。若 $x[n]=x_1[n]*x_2[n]$，它仍保有加法分解性。

這是 cepstrum family 中更穩定的版本之一。

## 講義截圖

![Differential cepstrum](assets/adsp/ADSP_Write3_p060_differential_cepstrum.png)

