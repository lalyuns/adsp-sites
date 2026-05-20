---
created: 2026-05-21
aliases:
  - "mini-max FIR"
  - "Chebyshev approximation"
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
  - "ADSP_Write1/page_054.png"
---

# Minimax FIR design

Minimax FIR design 用 $L_\infty$ norm 控制 maximal error：

$$\max_{F\notin\text{transition band}} |W(F)(R(F)-H_d(F))|.$$

它追求 equiripple：重要 extreme points 上的誤差大小相等、正負交替。這比 MSE 更重視 worst-case accuracy。

## 講義截圖

![Minimax FIR equiripple error](assets/adsp/ADSP_Write1_p054_minimax_error.png)

