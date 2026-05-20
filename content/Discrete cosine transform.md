---
created: 2026-05-21
aliases:
  - "DCT"
  - "離散餘弦轉換"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Data compression]]"
  - "[[Fourier analysis]]"
tags:
  - "adsp"
  - "compression"
  - "dct"
source:
  - "[[ADSP Write5 data compression]]"
pages:
  - "ADSP_Write5/page_021.png"
  - "ADSP_Write6/page_013.png"
---

# Discrete cosine transform

DCT 用 cosine basis 表示有限區塊，JPEG 通常對 8x8 block 做 2-D DCT。相較 DFT，DCT 對自然影像有較好的 energy compaction，而且 output 為 real。

DCT 可視為 KLT 的 practical approximation：suboptimal, but independent of input。

## 講義截圖

![Discrete cosine transform](assets/adsp/ADSP_Write5_p021_dct.png)

