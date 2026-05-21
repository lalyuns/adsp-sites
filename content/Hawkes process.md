---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Hawkes process limit order book project]]"
tags:
  - "adsp"
  - "project-concept"
---

# Hawkes process

Hawkes process 是 self-exciting point process：過去事件會提升未來 intensity。基本式為 $\lambda(t)=\mu+\sum_{t_i<t}\phi(t-t_i)$。它適合描述 clustering，如 earthquakes、social events、order arrivals。
