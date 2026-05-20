---
created: 2026-05-21
aliases:
  - "JPEG"
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
  - "ADSP_Write5/page_010.png"
---

# JPEG compression

JPEG pipeline 大致是：color transform/chroma subsampling -> 8x8 [[Discrete cosine transform]] -> [[Quantization]] -> [[Zigzag scanning]] -> [[Huffman coding]]。

Lossy 的主要來源是 chroma subsampling 與 quantization；lossless coding 則負責把剩下的符號更短地表示。

## 講義截圖

![JPEG compression pipeline](assets/adsp/ADSP_Write5_p010_jpeg_pipeline.png)

