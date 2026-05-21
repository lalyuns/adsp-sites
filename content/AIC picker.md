---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Seismic wave signal processing project]]"
tags:
  - "adsp"
  - "project-concept"
---

# AIC picker

AIC picker 把一個時間窗切成 arrival 前後兩段，假設兩段可用不同 statistical model 表示，選擇讓 AIC 最小的切點。它常用於精細定位 onset，但容易受 window choice 和 local minima 影響。
