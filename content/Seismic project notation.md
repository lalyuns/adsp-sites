---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Seismic wave signal processing project]]"
tags:
  - "adsp"
  - "seismic"
  - "notation"
  - "project-report"
---

# Seismic project notation

這篇統一地震波報告中的 notation，避免每篇論文各寫各的。

## Waveform And Arrival

- $x[n]$：single-channel discrete seismogram。
- $x_m[n]$：array 中第 $m$ 個 sensor 的 waveform。
- $\tau$：true phase arrival time；$\hat{\tau}$：algorithm pick。
- $e[n]$：envelope 或 characteristic function，用來放大 amplitude change。

## STA/LTA Statistic

$$
\mathrm{STA}[n]=\frac{1}{N_s}\sum_{i=n-N_s+1}^{n} e[i],
\quad
\mathrm{LTA}[n]=\frac{1}{N_l}\sum_{i=n-N_l+1}^{n} e[i],
$$

$$
R[n]=\frac{\mathrm{STA}[n]}{\mathrm{LTA}[n]+\epsilon}.
$$

## AIC Change-Point Statistic

$$
\mathrm{AIC}(k)=k\log\operatorname{var}(x[1:k])+(N-k-1)\log\operatorname{var}(x[k+1:N]).
$$

$\mathrm{AIC}(k)$ 最小的位置作為 arrival pick。

## Correlation Statistic

$$
C[n]=\frac{\langle x_n-\bar{x}_n, s-\bar{s}\rangle}
{\|x_n-\bar{x}_n\|\,\|s-\bar{s}\|}.
$$

## ADSP Course Connection

這些 notation 把 seismic picking 寫成 detector-statistic design：energy ratio、segmentation cost、template similarity。它們分別連到 filtering/windowing、model selection、matched filtering。

## Mathematical Statistics Connection

AIC 連到 [[Akaike information criterion]] 和 [[Likelihood function]]；correlation 連到 [[Covariance matrix]]；threshold 和 noise interpretation 連到 [[Probability for random signals]]。

## Links

- [[Seismic wave signal processing project]]
- [[Seismic wave detection as ADSP]]
- [[Detector statistic]]
- [[STA LTA picker]]
- [[AIC picker]]
- [[Akaike information criterion]]
- [[Waveform correlation detector]]
- [[Matched filter]]
- [[Covariance matrix]]
- [[Probability for random signals]]
