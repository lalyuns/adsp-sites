---
created: 2026-05-21
aliases:
  - "linear phase FIR"
  - "線性相位 FIR"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Filter design]]"
tags:
  - "adsp"
  - "fir"
source:
  - "[[ADSP Write1 filter design and transforms]]"
pages:
  - "ADSP_Write1/page_045.png"
  - "ADSP_Write2/page_010.png"
---

# Linear phase FIR filter

Linear phase FIR filter 的 impulse response 具有 symmetry 或 anti-symmetry，使相位近似線性，重要結果是不同頻率 component 的 delay 一致，不會扭曲波形形狀。

若 $N$ 為奇數且 $h[n]=h[N-1-n]$，可把 impulse response 重新中心化，得到只含 cosine 的 $R(F)$。

## 講義截圖

![Linear phase FIR impulse response](assets/adsp/ADSP_Write1_p045_linear_phase_fir.png)

![Four FIR symmetry types](assets/adsp/ADSP_Write2_p010_four_fir_types.png)

