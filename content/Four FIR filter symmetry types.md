---
created: 2026-05-21
aliases:
  - "FIR Types I II III IV"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Filter design]]"
tags:
  - "adsp"
  - "fir"
source:
  - "[[ADSP Write2 FIR design details]]"
pages:
  - "ADSP_Write2/page_010.png"
---

# Four FIR filter symmetry types

Linear phase FIR 依 $h[n]$ symmetry 與 $N$ 奇偶分成四型：Type 1/2 是 even symmetric，用 cosine 展開；Type 3/4 是 odd symmetric，用 sine 展開。

這四型決定 $R(F)$ 的可表示形式，也決定某些頻率點是否必然為 0。

## 講義截圖

![Four FIR symmetry types](assets/adsp/ADSP_Write2_p010_four_fir_types.png)

