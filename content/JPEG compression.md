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

JPEG pipeline 要按順序讀：color transform -> [[Chroma subsampling|chroma subsampling]] -> 8x8 block [[Discrete cosine transform|DCT]] -> [[Quantization|quantization]] -> zigzag -> run-length/Huffman。最主要失真來自 quantization。

連結：[[Compression math prerequisites]]、JPEG compression。


## 講義截圖
![JPEG compression pipeline](assets/adsp/ADSP_Write5_p010_jpeg_pipeline.png)
