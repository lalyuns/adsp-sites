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

SVD 把矩陣分解成

$$A=USV^H,$$

其中 $U,V$ 是 unitary/orthonormal basis，$S$ 的 singular values 依大小排序。SVD 讓任意矩陣可寫成多個 rank-one components 的加總，是 [[Principal component analysis]] 與低秩近似的核心。

若只保留前 $k$ 個 singular values，就得到最佳 low-rank approximation。

## 講義截圖

![SVD flow](assets/adsp/ADSP_Write4_p027_svd_flow.png)

