---
created: 2026-05-21
aliases:
  - "霍夫曼編碼"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Data compression]]"
tags:
  - "adsp"
  - "compression"
  - "coding"
source:
  - "[[ADSP Write5 data compression]]"
pages:
  - "ADSP_Write5/page_041.png"
---

# Huffman coding

Huffman coding 是 lossless coding 的 greedy algorithm。機率越高的 symbol 應該有越短 codeword；建樹時反覆合併最低機率的兩個 node。

平均碼長接近 entropy lower bound，但 codeword 長度必須是整數 bit，所以不一定等於 entropy。

## 講義截圖

![Huffman coding principle](assets/adsp/ADSP_Write5_p041_huffman_principle.png)

