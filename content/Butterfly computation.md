---
created: 2026-05-21
aliases:
  - "butterfly"
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
  - "ADSP_Write6/page_021.png"
---

# Butterfly computation

Butterfly computation 是 FFT 圖中的基本資料流，把兩個 input 經由加減與 twiddle factor 組合成兩個 output。2-point DFT 的 butterfly 是最小單位：

$$G[0]=g[0]+g[1],\qquad G[1]=g[0]-g[1].$$

大 FFT 透過很多 butterfly 疊起來。

## 講義截圖

![Two-point DFT butterfly](assets/adsp/ADSP_Write6_p021_butterfly.png)

