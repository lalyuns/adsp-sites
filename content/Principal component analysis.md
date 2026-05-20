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

PCA 找資料變異最大的正交方向，常用於降維、影像壓縮與資料視覺化。講義流程是先把資料扣掉平均，形成矩陣 $A$，再用 [[Singular value decomposition]] 找 principal components。

第一主成分是最大 singular value 對應的方向。

## 講義截圖

![PCA flow](assets/adsp/ADSP_Write4_p029_pca_flow.png)

