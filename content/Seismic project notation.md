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

可寫成

$$
\mathrm{STA}[n]=\frac{1}{N_s}\sum_{i=n-N_s+1}^{n} e[i],
\quad
\mathrm{LTA}[n]=\frac{1}{N_l}\sum_{i=n-N_l+1}^{n} e[i],
$$

$$
R[n]=\frac{\mathrm{STA}[n]}{\mathrm{LTA}[n]+\epsilon}.
$$

當 $R[n]$ 超過 threshold 時，代表 short-term energy 相對 background 有突增。

## AIC Change-Point Statistic

對長度 $N$ 的 window，候選切點 $k$ 的常見形式為

$$
\mathrm{AIC}(k)=k\log\operatorname{var}(x[1:k])+(N-k-1)\log\operatorname{var}(x[k+1:N]).
$$

$\mathrm{AIC}(k)$ 最小的位置作為 arrival pick。

## Wavelet Coefficients

Continuous notation 可寫成

$$
W_x(a,b)=\frac{1}{\sqrt{a}}\int x(t)\psi\left(\frac{t-b}{a}\right)dt,
$$

其中 $a$ 是 scale、$b$ 是 time shift。報告中可用這個式子解釋 multiscale，而不必深入所有 wavelet family。

## Normalized Correlation

template detector 可寫成

$$
C_m[\ell]=
\frac{\sum_n s_m[n]x_m[n+\ell]}
{\sqrt{\sum_n s_m[n]^2}\sqrt{\sum_n x_m[n+\ell]^2}}.
$$

array detector 再把多個 $C_m$ 對齊後加權平均：

$$
C_{\mathrm{array}}[\ell]=\sum_{m=1}^{M}w_m C_m[\ell+\delta_m].
$$

連結：[[STA LTA picker]]、[[AIC picker]]、[[Waveform correlation detector]]。
