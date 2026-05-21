---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Seismic wave signal processing project]]"
tags:
  - "adsp"
  - "project-concept"
  - "seismic"
---

# Travel time curve

Travel-time curve 描述 seismic phase arrival time 隨 epicentral distance/range 的變化。它不是 detector 本身，而是用來檢查 [[Seismic phase picking]] 是否符合地震波傳播物理。

在 [[Earle and Shearer 1994 automatic seismic phase picking]] 中，大量 automatic picks 疊在 time-distance plane 上，可以形成 phase image。對報告來說，它連接了 [[Detector statistic]] 與 physical validation：local trigger 只說「這裡像 arrival」，travel-time structure 才幫你判斷這些 picks 是否像真實 phase。

## ADSP Course Connection

這是 signal-processing result 的 domain validation。ADSP detector 產生 picks，但 travel-time curve 幫你判斷 picks 是否形成物理合理的 structure。

## Mathematical Statistics Connection

可把它看成 model checking / sanity check：若大量 picks 不沿著 expected structure 分布，detector statistic 可能產生過多 false triggers。

## Links

- [[Seismic phase picking]]
- [[Detector statistic]]
- [[Earle and Shearer 1994 automatic seismic phase picking]]
- [[Seismic wave signal processing project]]
