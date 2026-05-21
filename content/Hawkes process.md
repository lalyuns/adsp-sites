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

# Hawkes process

Hawkes process 是 self-exciting point process：事件發生後，短時間內會提高後續事件的 [[Conditional intensity]]。它很適合描述 clustering，例如 aftershocks、order arrivals、click streams。

單變量 Hawkes 只看一類 event；[[Multivariate Hawkes process]] 讓不同 event types 互相 excitation；[[Marked Hawkes process]] 則把 event size 或屬性一起建模。報告中要記住：Hawkes 的核心不是平均 rate，而是 history-dependent rate。
