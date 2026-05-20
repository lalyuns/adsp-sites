---
created: 2026-05-21
aliases:
  - "zigzag scan"
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
  - "ADSP_Write5/page_039.png"
---

# Zigzag scanning

Zigzag scanning 把 8x8 DCT coefficient 從低頻到高頻排成 1-D sequence。Quantization 後高頻常變成很多 0，zigzag 讓這些 0 聚在後段，方便 run-length coding 與 EOB。

它是 JPEG entropy coding 前的重要重排。

## 講義截圖

![Zigzag scanning](assets/adsp/ADSP_Write5_p039_zigzag_scan.png)

