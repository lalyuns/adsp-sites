---
created: 2026-05-21
aliases:
  - "快速演算法設計"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Fast algorithms]]"
tags:
  - "adsp"
  - "fast-algorithms"
source:
  - "[[ADSP Write6 fast algorithms]]"
pages:
  - "ADSP_Write6/page_001.png"
---

# Fast algorithm design

Fast algorithm design 的目標是省 computational time 與 hardware cost：減少 additions、multiplications、time cycles、buffer size，並重複使用 structure。

Write6 的核心觀念是把大矩陣/大 DFT 拆成較小問題，再利用 symmetry 與 special constants。

## 講義截圖

![Fast algorithm design goals](assets/adsp/ADSP_Write6_p001_fast_algorithm_design.png)

