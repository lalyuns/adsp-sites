---
created: 2026-05-21
aliases:
  - "weight function"
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
  - "ADSP_Write2/page_004.png"
---

# Weighted approximation error

Weighted approximation error 寫成

$$err(F)=W(F)(R(F)-H_d(F)).$$

如果 stopband 更重要，就讓 stopband 的 $W(F)$ 較大；如果 passband 更重要，就反過來。Weighted error 是把「哪個頻帶比較不能錯」放進 optimization 的方式。

## 講義截圖

![Weight functions and accuracy](assets/adsp/ADSP_Write2_p004_weight_function_accuracy.png)

