---
created: 2026-05-21
aliases:
  - "資料壓縮"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Data compression]]"
tags:
  - "adsp"
  - "compression"
source:
  - "[[ADSP Write5 data compression]]"
pages:
  - "ADSP_Write5/page_002.png"
---

# Data compression

Data compression 利用資料的一致性、規律性、可預測性，把 original signal 表成 compact representation 加 residual information。資料越一致、越集中、entropy 越小，通常越容易壓縮。

壓縮分成 lossy 與 lossless：JPEG 同時使用 transform、quantization、zigzag、Huffman coding。

## 講義截圖

![Compression philosophy](assets/adsp/ADSP_Write5_p002_compression_philosophy.png)

