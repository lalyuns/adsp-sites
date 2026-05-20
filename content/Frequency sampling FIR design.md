---
created: 2026-05-21
aliases:
  - "frequency sampling method"
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
  - "ADSP_Write2/page_026.png"
---

# Frequency sampling FIR design

Frequency sampling method 先在 $F=m/N$ 的 grid 上指定 desired response $H_d(m/N)$，再用 IDFT 得到 impulse response。

它的概念很直接：設計頻域樣本，再轉回時域；但在樣本點之外的 response 可能有較大誤差，尤其 transition band 附近。

## 講義截圖

![Frequency sampling FIR method](assets/adsp/ADSP_Write2_p026_frequency_sampling_method.png)

