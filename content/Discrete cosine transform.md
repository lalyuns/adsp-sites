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

DCT 在 Write5 是 compression tool，在 Write6 則是 fast algorithm 的對象。它把 image block 表成 cosine basis coefficients；自然影像通常能量集中在低頻係數，所以 JPEG 會保留低頻、粗量化高頻。

2-D DCT 常寫成 separable transform：先對 rows 做 1-D DCT，再對 columns 做 1-D DCT。這讓 8x8 block 的計算可以拆成多個小問題，也讓 fast DCT 有空間利用 symmetry 和 matrix factorization。

和 [[Karhunen-Loeve transform]] 的關係：KLT 對資料 covariance 最佳，但 depends on input；DCT 固定、real-valued、接近自然影像的 KLT，而且容易快速實作。

連結路徑：[[JPEG compression]] -> [[Quantization]] -> [[Zigzag scanning]]；演算法路徑則是 [[Matrix multiplication complexity]] -> [[Fast algorithm design]]。


## 講義截圖
![Discrete cosine transform](assets/adsp/ADSP_Write5_p021_dct.png)
