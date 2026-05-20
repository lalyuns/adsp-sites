---
created: 2026-05-21
aliases:
  - "4:2:2"
  - "4:2:0"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Data compression]]"
tags:
  - "adsp"
  - "compression"
  - "jpeg"
source:
  - "[[ADSP Write5 data compression]]"
pages:
  - "ADSP_Write5/page_013.png"
---

# Chroma subsampling

Chroma subsampling 把 RGB 轉到 luminance/chrominance 空間後，保留較多亮度 $Y$，少存色度 $C_b,C_r$。4:2:2 與 4:2:0 都利用人眼對亮度較敏感、對色度較不敏感的特性。

這是 JPEG/MPEG 常見的 lossy step。

## 講義截圖

![4:2:2 and 4:2:0 chroma subsampling](assets/adsp/ADSP_Write5_p013_chroma_subsampling.png)

