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

Zigzag 把 8x8 DCT coefficients 從低頻掃到高頻，使量化後的零聚集成長 run，方便 run-length 和 Huffman coding。

連結：[[Compression math prerequisites]]、[[JPEG compression]]。


## 講義截圖
![Zigzag scanning](assets/adsp/ADSP_Write5_p039_zigzag_scan.png)
