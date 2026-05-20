---
created: 2026-05-21
aliases:
  - "ADSP Write4"
  - "Write4"
categories:
  - "[[Evergreen]]"
  - "[[Indexes]]"
topics:
  - "[[Advanced digital signal processing]]"
  - "[[Speech processing]]"
  - "[[Linear algebra]]"
type:
  - "[[MOCs]]"
status:
  - "[[Active]]"
tags:
  - "adsp"
  - "speech"
  - "linear-algebra"
pages:
  - "ADSP_Write4/page_001.png-page_040.png"
---

# ADSP Write4 acoustics speech PCA SVD

Write4 看起來跨很大，其實主線是「把真實訊號變成可分析的 features」。

Audio/speech 部分先讀：

- [[Speech signal processing]]：source-filter model，聲帶提供 excitation，vocal tract 像 filter。
- [[Pitch and harmonics]]：pitch 對應 fundamental frequency，harmonics 是整數倍。
- [[Short-time Fourier transform]]：語音不是 stationary，所以要切 frame 看 time-frequency。
- [[Formant]]：spectral envelope 的 resonance peaks，和發音位置有關。

Linear algebra 部分接著讀：

- [[Covariance matrix]]：描述 variables 如何共同變動。
- [[Eigenvalues and eigenvectors]]：找出被線性轉換保留方向的 axes。
- [[Principal component analysis]] / [[Singular value decomposition]]：把高維資料投影到最重要方向。
- [[Karhunen-Loeve transform]]：用 covariance eigenvectors 做 optimal decorrelation，會在 Write5 的 compression 再出現。

這份講義的連結點是：speech feature extraction 需要 time-frequency 表示，而 PCA/SVD/KLT 是把 feature 或影像資料降維、去相關、集中 energy 的工具。

前置補洞：[[Spectral analysis workflow]]、[[Matrix diagonalization for transforms]]、[[Linear algebra for DSP]]。


## 講義截圖
![Human hearing range](assets/adsp/ADSP_Write4_p002_acoustics_range.png)

![Short-time Fourier transform](assets/adsp/ADSP_Write4_p018_stft.png)

![Speech formants](assets/adsp/ADSP_Write4_p020_formants.png)

![SVD flow](assets/adsp/ADSP_Write4_p027_svd_flow.png)

![PCA flow](assets/adsp/ADSP_Write4_p029_pca_flow.png)
