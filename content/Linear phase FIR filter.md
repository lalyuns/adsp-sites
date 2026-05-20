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

Linear phase 表示 phase 是 $-\omega d$ 加常數，所有頻率 delay 相同，waveform 不會被 phase distortion 扭曲。FIR 的對稱/反對稱係數是達成 linear phase 的關鍵。

連結：[[Optimization for filter design]]、[[Frequency response]]。


## 講義截圖
![Linear phase FIR impulse response](assets/adsp/ADSP_Write1_p045_linear_phase_fir.png)

![Four FIR symmetry types](assets/adsp/ADSP_Write2_p010_four_fir_types.png)
