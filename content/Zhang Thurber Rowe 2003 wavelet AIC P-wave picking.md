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

# Zhang Thurber Rowe 2003 wavelet AIC P-wave picking

這篇把 picking 問題改寫成 multiscale change-point problem。純 AIC 在低 SNR 或 window 不佳時容易選錯 minimum；wavelet transform 先把訊號拆成不同 scales，再檢查 arrival 是否在多尺度上穩定出現。

## Method

1. 對 sliding time window 做 discrete wavelet transform。
2. 取 thresholded absolute wavelet coefficients，降低 noise 和 secondary arrivals 的干擾。
3. 在每個 scale 上套 AIC picker。
4. 比較不同 scales 的 AIC picks 是否一致。
5. 若一致，才確認 P-wave arrival；最後在合適 window 中用 AIC 精修 pick time。

## Report-Level Reading

它不是「wavelet 比 AIC 好」這麼簡單，而是 wavelet 提供一個 robustness layer：真正的 P arrival 是 signal singularity，應該在多個 resolution 上留下 consistent evidence。

## Limitations

需要選 wavelet family、scale、window length、threshold。這些 hyperparameters 會影響 detection/picking；報告中可以把它列為相對於 STA/LTA 的成本。

## Figures For Report

![AIC picker behavior under different SNR conditions](assets/adsp/projects/seismic_aic_picker_examples_cropped.png)

![Wavelet-AIC picks across several scales](assets/adsp/projects/seismic_wavelet_aic_multiscale_examples.png)
