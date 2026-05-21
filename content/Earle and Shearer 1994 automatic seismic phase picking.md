---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Seismic wave signal processing project]]"
tags:
  - "adsp"
  - "seismic"
  - "paper-note"
---

# Earle and Shearer 1994 automatic seismic phase picking

這篇提供地震波專題的 classical baseline。作者用 envelope function 上的 STA/LTA ratio 進行 automatic phase picking，並把方法套到 NEIC 大量全球 seismograms。

可放進 report 的重點：

- Method：先把 seismogram 轉成 envelope，再計算 [[STA LTA picker]]。STA/LTA 超過 threshold 時產生 phase arrival candidate，並估計 pick quality。
- ADSP 連結：envelope extraction、smoothing、thresholding、time-domain detector、travel-time visualization。
- Result interpretation：high-frequency data pick precision 較好；long-period data 可看到更多 low-frequency phases。travel-time plots 可以看成大量 automatic picks 疊出的 time-distance image。
- Limitations：threshold-based detector 對 noise、emergent onset、phase overlap 敏感。

報告中可把它當作「能量型 detector」代表，和 [[AIC picker]]、[[Waveform correlation detector]] 比較。

## 論文圖表截圖

![STA/LTA envelope picking procedure](assets/adsp/projects/seismic_earle_shearer_1994_p002_sta_lta_procedure.png)

![Global seismic travel-time curves from automatic picks](assets/adsp/projects/seismic_earle_shearer_1994_p005_global_travel_time_curves.png)
