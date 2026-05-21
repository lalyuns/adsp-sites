---
created: 2026-05-21
aliases:
  - "matrix-vector complexity"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Linear algebra]]"
  - "[[Fast algorithms]]"
tags:
  - "adsp"
  - "linear-algebra"
  - "complexity"
source:
  - "[[ADSP Write6 fast algorithms]]"
pages:
  - "ADSP_Write6/page_004.png"
---

# Matrix multiplication complexity

把 transform 寫成矩陣乘法可以看見 fast algorithm 的形狀。[[Discrete Fourier transform|DFT]] 可寫成

$$
X = F_N x,
$$

其中 $F_N$ 是 dense matrix；直接相乘要很多乘加。FFT 的想法是把 $F_N$ 分解成

$$
F_N = P_1 B_1 D_1 P_2 B_2 D_2 \cdots,
$$

其中 $P$ 是 permutation，$B$ 是 butterfly/small DFT block，$D$ 是 diagonal twiddle factor。這些 matrix individually 都比 dense $F_N$ 便宜。

同樣的觀念也解釋 fast DCT。[[Discrete cosine transform]] 的矩陣可利用 even symmetry 和 separability 拆開；在 [[JPEG compression|JPEG]] 中，8x8 block DCT 能快速計算，才讓壓縮 pipeline 可實作。

相關路徑：[[Fast algorithm design]] -> [[Butterfly computation]] -> [[Cooley-Tukey FFT]]。


## 講義截圖
![Matrix simplification for fast algorithms](assets/adsp/ADSP_Write6_p004_matrix_simplification.png)
