---
created: 2026-05-21
aliases:
  - "radix-4"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Fast algorithms]]"
tags:
  - "adsp"
  - "fft"
source:
  - "[[ADSP Write6 fast algorithms]]"
pages:
  - "ADSP_Write6/page_027.png"
---

# Radix-4 FFT

Radix-4 FFT 在 $N=4^k$ 時把 $N$-point DFT 拆成四個 $N/4$-point DFT。相較 radix-2，每層拆得更大，常可進一步減少乘法數。

講義中估算 real multiplications 約為

$$\frac{9}{4}N\log_4 N-\frac{43}{12}N+\frac{16}{3}.$$

## 講義截圖

![Radix-4 algorithm](assets/adsp/ADSP_Write6_p027_radix4.png)

