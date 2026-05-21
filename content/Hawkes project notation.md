---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Hawkes process limit order book project]]"
tags:
  - "adsp"
  - "hawkes-process"
  - "notation"
  - "project-report"
---

# Hawkes project notation

這篇統一 Hawkes/LOB 報告中的 notation。

## Counting Processes

$N_i(t)$ 表示 type $i$ event 到時間 $t$ 為止的累積數量。它的 increment $dN_i(t)$ 在時間 $t$ 有事件時為 1，否則為 0。

## Conditional Intensity

Hawkes process 的核心是 conditional intensity：

$$
\lambda_i(t)=\mu_i+\sum_{j=1}^{K}\int_0^t \phi_{ij}(t-s)dN_j(s).
$$

也可寫成 sum over past events：

$$
\lambda_i(t)=\mu_i+\sum_{j=1}^{K}\sum_{t_n^j<t}\phi_{ij}(t-t_n^j).
$$

$\mu_i$ 是 baseline intensity，$\phi_{ij}$ 是 type $j$ event 對 type $i$ intensity 的 kernel。

## Stability

定義 branching matrix

$$
\Gamma_{ij}=\int_0^\infty \phi_{ij}(u)du.
$$

若 spectral radius $\rho(\Gamma)<1$，process 通常可保持 stationary，不會 self-excitation 爆炸。

## Marks

marked Hawkes 可寫成

$$
\lambda_i(t,v)=\lambda_i(t)\,p_i(v\mid \mathcal{H}_t).
$$

傳統模型可能讓 $p_i$ 很簡單；[[Neural marked Hawkes process]] 讓 $p_i(v\mid \mathcal{H}_t)$ 由 neural history vector 決定。
