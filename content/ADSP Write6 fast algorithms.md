---
created: 2026-05-21
aliases:
  - "ADSP Write6"
  - "Write6"
categories:
  - "[[Evergreen]]"
  - "[[Indexes]]"
topics:
  - "[[Advanced digital signal processing]]"
  - "[[Fast algorithms]]"
type:
  - "[[MOCs]]"
status:
  - "[[Active]]"
tags:
  - "adsp"
  - "fast-algorithms"
  - "fft"
pages:
  - "ADSP_Write6/page_001.png-page_038.png"
---

# ADSP Write6 fast algorithms

Write6 的核心是 fast algorithm design：用 factorization、symmetry、butterfly、replacement of DFTs 來省乘法與加法。主線是從矩陣乘法觀點看 [[Discrete Fourier transform]]，再導向 [[Fast Fourier transform]]、[[Cooley-Tukey FFT]]、[[Radix-4 FFT]]、[[Prime factor FFT]]。

## 講義截圖

![Fast algorithm design goals](assets/adsp/ADSP_Write6_p001_fast_algorithm_design.png)

![Two-point DFT butterfly](assets/adsp/ADSP_Write6_p021_butterfly.png)

![Cooley-Tukey decomposition](assets/adsp/ADSP_Write6_p022_cooley_tukey.png)

![Radix-4 algorithm](assets/adsp/ADSP_Write6_p027_radix4.png)

![Prime factor FFT](assets/adsp/ADSP_Write6_p037_prime_factor_fft.png)

