---
created: 2026-05-21
aliases:
  - "Parks-McClellan algorithm"
  - "Remez"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Filter design]]"
tags:
  - "adsp"
  - "fir"
  - "optimization"
source:
  - "[[ADSP Write1 filter design and transforms]]"
pages:
  - "ADSP_Write1/page_058.png"
---

# Remez exchange algorithm

Remez exchange algorithm 是 minimax/equiripple FIR design 的迭代流程。先猜 $k+2$ 個 extreme frequencies，解出 filter coefficients 與 error $e$，再從 error curve 裡換入新的 extreme points，直到 error 收斂。

它背後是 [[Optimization norm for filter design]] 與 alternation theorem 的思想。

## 講義截圖

![Remez exchange process](assets/adsp/ADSP_Write1_p058_remez_process.png)

