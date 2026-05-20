---
created: 2026-05-21
aliases:
  - "homomorphism"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Homomorphic processing]]"
tags:
  - "adsp"
  - "homomorphic"
source:
  - "[[ADSP Write3 filters and homomorphic processing]]"
pages:
  - "ADSP_Write3/page_041.png"
---

# Homomorphic signal processing

Homomorphic processing 的目標是把難處理的運算搬到另一個代數系統。例如 convolution 在 Fourier domain 變 multiplication，再取 log 變 addition：

$$x*h \xrightarrow{FT} XH \xrightarrow{\log} \log X+\log H.$$

這是 [[Cepstrum]]、echo removal、speech analysis 的核心。

## 講義截圖

![Homomorphic signal processing](assets/adsp/ADSP_Write3_p041_homomorphism.png)

