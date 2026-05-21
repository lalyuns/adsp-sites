---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Hawkes process limit order book project]]"
tags:
  - "adsp"
  - "project-concept"
  - "hawkes-process"
---

# Hawkes kernel matrix

Hawkes kernel matrix 的 entry $\phi_{ij}(t)$ 表示 type $j$ 的過去事件，對 type $i$ 未來 [[Conditional intensity]] 的影響。對角線是 self-excitation；非對角線是 cross-excitation。

在 [[Multivariate Hawkes process]] 中，kernel matrix 是可解釋性的主要來源：它告訴你哪一類 LOB event 會激發哪一類後續 event。若把 kernel 對時間積分成 matrix $G$，就能連到 [[Hawkes branching ratio]] 與 stability；若用資料反推 kernel shape，就連到 [[Nonparametric Hawkes estimation]]。
