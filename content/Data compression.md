---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[ADSP Write5 data compression]]"
tags:
  - "adsp"
  - "compression"
---

# Data compression

Data compression 先分 lossless/lossy。Lossless 利用 statistical redundancy，例如 [[Huffman coding]]；lossy 進一步利用 perceptual redundancy 與任務容忍度，例如 [[JPEG compression]] 中的 transform coding、[[Quantization]]、以及 [[Chroma subsampling]]。

在 ADSP 裡，compression 不是單純檔案變小，而是「representation + approximation」問題：先用 [[Discrete cosine transform]] 或 [[Karhunen-Loeve transform]] 把能量集中，再決定哪些係數可粗略表示或丟棄。數學前置整理在 [[Compression math prerequisites]]。

![Compression philosophy](assets/adsp/ADSP_Write5_p002_compression_philosophy.png)
