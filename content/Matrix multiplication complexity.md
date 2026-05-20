---
created: 2026-05-21
aliases:
  - "matrix-vector complexity"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Linear algebra]]"
  - "[[Fast algorithms]]"
tags:
  - "adsp"
  - "linear-algebra"
  - "complexity"
source:
  - "[[ADSP Write6 fast algorithms]]"
pages:
  - "ADSP_Write6/page_004.png"
---

# Matrix multiplication complexity

一般 $M\times N$ matrix-vector multiplication 需要 $MN$ multiplications 與 $M(N-1)$ additions。Fast algorithms 通常利用 zero、repeated coefficients、symmetry、outer-product decomposition 來少算。

這是理解 [[Fast Fourier transform]] 和 [[Discrete cosine transform]] fast implementation 的基礎。

## 講義截圖

![Matrix simplification for fast algorithms](assets/adsp/ADSP_Write6_p004_matrix_simplification.png)

