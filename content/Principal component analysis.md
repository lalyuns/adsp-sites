---
created: 2026-05-21
aliases:
  - "PCA"
  - "主成分分析"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Linear algebra]]"
  - "[[Data compression]]"
tags:
  - "adsp"
  - "linear-algebra"
  - "pca"
source:
  - "[[ADSP Write4 acoustics speech PCA SVD]]"
pages:
  - "ADSP_Write4/page_029.png"
---

# Principal component analysis

PCA 找最大 variance 的方向，讓資料投影後保留最多能量。它可看成 covariance matrix 的 eigen-decomposition，也可由 SVD 實作。

連結：[[Matrix diagonalization for transforms]]、[[Linear algebra for DSP]]。


## 講義截圖
![PCA flow](assets/adsp/ADSP_Write4_p029_pca_flow.png)
