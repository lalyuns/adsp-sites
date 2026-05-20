---
created: 2026-05-21
aliases:
  - "prime factor algorithm"
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
  - "ADSP_Write6/page_037.png"
---

# Prime factor FFT

Prime factor FFT 用在 $N=P_1^{k_1}P_2^{k_2}\cdots P_M^{k_M}$ 且 factors 互質時。它把 DFT 分解成多個較小長度的 DFT，可能比單純 radix-2 更省乘法。

注意 $P_i$ 不一定要是 prime number，但彼此要 coprime。

## 講義截圖

![Prime factor FFT](assets/adsp/ADSP_Write6_p037_prime_factor_fft.png)

