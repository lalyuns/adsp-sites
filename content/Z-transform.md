---
created: 2026-05-21
aliases:
  - "Z transform"
  - "Z 轉換"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Fourier analysis]]"
  - "[[Filter design]]"
tags:
  - "adsp"
  - "z-transform"
source:
  - "[[ADSP Write1 filter design and transforms]]"
pages:
  - "ADSP_Write1/page_036.png"
---

# Z-transform

Z-transform 把 sequence $g[n]$ 寫成

$$G(z)=\sum_{n=-\infty}^{\infty}g[n]z^{-n}.$$

把 $z=e^{j2\pi F}$ 代回去就得到 DTFT，因此 unit circle 上的 Z-transform 是 frequency response。Z-transform 也讓 [[IIR filter]] 的 recursion、pole/zero、stability 更好處理。

## 講義截圖

![Bilinear transform mapping](assets/adsp/ADSP_Write1_p036_bilinear_transform.png)

