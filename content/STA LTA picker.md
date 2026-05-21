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

# STA LTA picker

STA/LTA picker 計算 short-term average 和 long-term average 的 ratio。若短窗能量突然高於長窗背景，就代表可能有 phase arrival。優點是簡單快速；缺點是 threshold sensitive，對 emergent onset 和 nonstationary noise 較弱。
