---
created: 2026-05-21
aliases:
  - "ADSP Write5"
  - "Write5"
categories:
  - "[[Evergreen]]"
  - "[[Indexes]]"
topics:
  - "[[Advanced digital signal processing]]"
  - "[[Data compression]]"
type:
  - "[[MOCs]]"
status:
  - "[[Active]]"
tags:
  - "adsp"
  - "compression"
  - "jpeg"
pages:
  - "ADSP_Write5/page_001.png-page_056.png"
---

# ADSP Write5 data compression

Write5 是 ADSP 工具的整合案例：transform、perception、quantization、entropy coding 都會在 JPEG 裡合起來。

主線是：

1. [[Data compression]] / [[Image compression]]：先分 lossless 和 lossy，再問 redundancy 來自哪裡。
2. [[Chroma subsampling]]：利用人眼對色度較不敏感，降低 Cb/Cr resolution；4:2:2 和 4:2:0 是 [[Sampling and aliasing|sampling]] layout。
3. [[Karhunen-Loeve transform]] -> [[Discrete cosine transform]]：KLT 理論上 optimal 但 depends on data，DCT 固定且接近自然影像的 energy compaction。
4. [[JPEG compression]]：color transform、8x8 DCT、[[Quantization]]、[[Zigzag scanning]]、run-length/Huffman。
5. [[Huffman coding]] / [[Entropy coding length]]：利用 symbol probability 降低平均碼長。
6. [[Structural similarity index]]：品質評估不只看 MSE，也要看 luminance、contrast、structure。

讀圖時要標出每一步是 reversible 還是 lossy。JPEG 的主要失真在 quantization；Huffman coding 只是 lossless 地重寫符號，不會再丟資訊。

前置補洞：[[Compression math prerequisites]]、[[Matrix diagonalization for transforms]]、[[Discrete cosine transform]]。


## 講義截圖
![Compression philosophy](assets/adsp/ADSP_Write5_p002_compression_philosophy.png)

![JPEG compression pipeline](assets/adsp/ADSP_Write5_p010_jpeg_pipeline.png)

![Discrete cosine transform](assets/adsp/ADSP_Write5_p021_dct.png)

![Structural similarity formula](assets/adsp/ADSP_Write5_p030_ssim_formula.png)

![Huffman coding principle](assets/adsp/ADSP_Write5_p041_huffman_principle.png)
