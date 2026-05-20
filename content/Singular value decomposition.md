---
created: 2026-05-21
aliases:
  - "SVD"
  - "奇異值分解"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Linear algebra]]"
tags:
  - "adsp"
  - "linear-algebra"
source:
  - "[[ADSP Write4 acoustics speech PCA SVD]]"
pages:
  - "ADSP_Write4/page_027.png"
---

# Singular value decomposition

SVD 把任意矩陣拆成 $U\Sigma V^T$，可理解為 rotate -> scale -> rotate。它比 eigen-decomposition 更泛用，常用於 low-rank approximation、denoising、PCA。

連結：[[Matrix diagonalization for transforms]]、[[Linear algebra for DSP]]。


## 講義截圖
![SVD flow](assets/adsp/ADSP_Write4_p027_svd_flow.png)
