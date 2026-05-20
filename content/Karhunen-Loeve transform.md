---
created: 2026-05-21
aliases:
  - "KLT"
  - "Karhunen-Loeve Transform"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Data compression]]"
  - "[[Linear algebra]]"
tags:
  - "adsp"
  - "compression"
  - "linear-algebra"
source:
  - "[[ADSP Write5 data compression]]"
pages:
  - "ADSP_Write5/page_017.png"
---

# Karhunen-Loeve transform

KLT 是讓 transform coefficients decorrelate 的 optimal transform，本質上與 [[Principal component analysis]] 相同。若 covariance matrix 是 $C$，KLT matrix 的 rows/columns 由 $C$ 的 eigenvectors 組成。

它能給最佳 energy compaction，但缺點是 dependent on input，需要根據資料估 covariance。

## 講義截圖

![Karhunen-Loeve transform](assets/adsp/ADSP_Write5_p017_klt.png)

