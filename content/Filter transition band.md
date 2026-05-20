---
created: 2026-05-21
aliases:
  - "transition band"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Filter design]]"
tags:
  - "adsp"
  - "filter-design"
source:
  - "[[ADSP Write2 FIR design details]]"
pages:
  - "ADSP_Write2/page_001.png"
---

# Filter transition band

Transition band 是 passband 與 stopband 中間不要求精準逼近的區域。FIR design 通常把 transition band 排除在 error 計算之外，因為 discontinuity 附近最難逼近。

經驗上，transition band 越窄、ripple 要求越小，filter length $N$ 越大。

## 講義截圖

![Filter length, transition band, and ripple](assets/adsp/ADSP_Write2_p001_filter_length_transition_ripple.png)

