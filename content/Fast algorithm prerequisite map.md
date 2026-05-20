---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Advanced digital signal processing]]"
  - "[[Meta knowledge]]"
tags:
  - "adsp"
  - "meta-knowledge"
  - "prerequisite"
---

# Fast algorithm prerequisite map

這篇只保留 Write6 需要的前置工具。

先補三個 notation：

- [[Discrete Fourier transform]]：知道 DFT matrix 和 $W_N^{kn}$。
- [[Twiddle factor]]：知道 $W_N^k=e^{-j2\pi k/N}$ 是 complex rotation。
- [[Matrix multiplication complexity]]：知道 dense matrix-vector multiplication 為什麼貴。

再補三個讀圖技巧：

- index decomposition：把 $n,k$ 拆成 smaller indices。
- permutation：有些線只是重新排序，不是新的數學運算。
- stage：每一層通常做 small DFT、butterfly、或 twiddle multiplication。

最後回到主線：[[Fast Fourier transform]]、[[Cooley-Tukey FFT]]、[[Radix-4 FFT]]、[[Prime factor FFT]]。如果你能說出每張圖中哪些是加減、哪些是旋轉、哪些是重排，就已經抓到 Write6 的核心。
