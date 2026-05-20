---
created: 2026-05-21
aliases:
  - "快速演算法設計"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Fast algorithms]]"
tags:
  - "adsp"
  - "fast-algorithms"
source:
  - "[[ADSP Write6 fast algorithms]]"
pages:
  - "ADSP_Write6/page_001.png"
---

# Fast algorithm design

Fast algorithm design 的核心是「找結構」。如果一個運算可以寫成矩陣乘法，直接做通常會浪費很多重複計算；fast algorithm 會把矩陣拆成更便宜的 pieces。

常見可利用的結構：

- symmetry：例如 cosine/sine 或 DFT kernel 的共軛對稱。
- periodicity：例如 $W_N^{k+N}=W_N^k$。
- sparsity：很多 factor matrix 只有少數非零項。
- separability：2-D transform 可拆成 rows 再 columns。
- reuse：butterfly 把中間結果同時餵給多個 output。

在 Write6 裡，這個觀念先用 [[Matrix multiplication complexity]] 表達，再落到 [[Fast Fourier transform]]、[[Butterfly computation]]、[[Cooley-Tukey FFT]]。所以這篇不需要背特定公式；它是讀後面所有 wiring diagrams 的方法論。


## 講義截圖
![Fast algorithm design goals](assets/adsp/ADSP_Write6_p001_fast_algorithm_design.png)
