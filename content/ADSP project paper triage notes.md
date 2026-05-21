---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[ADSP course project report MOC]]"
  - "[[Seismic wave signal processing project]]"
  - "[[Hawkes process limit order book project]]"
tags:
  - "adsp"
  - "project-report"
  - "reading-triage"
---

# ADSP project paper triage notes

這篇不是正式報告內容，而是閱讀取捨紀錄。主筆記會故意保留 report-ready argument、notation、核心公式、必要圖表；這篇記錄哪些東西被壓掉，以及什麼情況下才需要回頭用。

取捨原則：

- 若內容只是論文格式需要，例如長背景、文獻鋪陳、dataset bookkeeping，先不放主線。
- 若公式可以自己用統一 notation 重寫，就不用截論文方程式圖。
- 若圖表只是大量結果表或局部案例，除非能支撐報告論點，否則先不放。
- 若細節會讓初稿主線變散，但 final report 的 limitation 或 experiment section 可能需要，記在這裡。

## Seismic Wave Signal Processing Project

主線連到 [[Seismic wave signal processing project]]。這一組 paper 被保留的是 [[Detector statistic|detector statistic]] 的設計邏輯：energy ratio、change point、multiscale consistency、template correlation。被壓掉的內容不是完全沒用，而是目前對 10 頁報告的主論點密度較低。

### Earle and Shearer 1994

主筆記：[[Earle and Shearer 1994 automatic seismic phase picking]]。

保留：[[STA LTA picker|STA/LTA]] envelope picker、trigger threshold、travel-time curve quality control。這些能說明 automatic picking pipeline 如何從 waveform 產生 candidate arrival，再用物理 travel-time structure 做 sanity check。

壓掉：

- 大量 global dataset 與 station/event bookkeeping：對報告的 signal-processing 主線幫助有限；只有在你要寫 data section 時才需要補。
- 個別 phase 類型與全球路徑細節：它們屬於 seismology context，不是 ADSP method comparison 的核心。
- 完整 performance statistics：若 final report 要比較 false alarm/missed pick 才回頭補，否則初稿只需說明 threshold trade-off。
- 論文中的流程細節圖若只是操作步驟，不如在文中用「envelope -> STA/LTA ratio -> threshold trigger -> [[Travel time curve|travel-time]] validation」四步文字化。

回頭使用時機：需要寫「dataset and evaluation」小節，或老師要求說明 automatic picks 如何被 validated。

### Zhang Thurber Rowe 2003

主筆記：[[Zhang Thurber Rowe 2003 wavelet AIC P-wave picking]]。

保留：AIC as change-point criterion、[[Wavelet transform for seismic picking|wavelet]] multiscale representation、跨尺度一致性提升 robustness。

壓掉：

- 小波母函數、尺度選擇、濾波參數的細節：目前先不用塞入主線，因為你要先懂 wavelet step 的角色是 representation，不是背參數表。
- 多個相似 waveform examples：只保留最能說明 multiscale AIC minima 的圖；其餘案例容易讓筆記變成圖庫。
- 實驗資料逐筆描述：除非你 final report 要做 reproduction 或比較不同 SNR case，否則先不用。
- AIC 原始推導的細節：已經整理成 [[AIC picker]] 和 [[Change point detection]]，用統一 notation 寫比截圖更有用。

回頭使用時機：需要寫「why wavelet improves AIC」的細節段落，或要補 wavelet scale selection 的 limitation。

### Gibbons Ringdal 2006

主筆記：[[Gibbons Ringdal 2006 array waveform correlation]]。

保留：normalized running cross-correlation、array coherent stacking、weak event detection 的 matched-filter view。

壓掉：

- 長篇地震區域背景與事件 catalog 討論：對方法概念不是必要，除非報告要介紹 case study。
- 論文原本的 correlation 方程式截圖：已改寫在 [[Waveform correlation detector]] 和 [[Seismic project notation]]。
- 大量 detection examples：只保留能看出 coherent stack 增益的圖；其餘案例可以在 final report 的 appendix-style discussion 才拿。
- 門檻參數與 station-specific details：會讓初學者誤以為重點是調參，而不是 template similarity + array coherence。

回頭使用時機：需要具體說明 array configuration、threshold calibration，或要寫「method works best for repeating/co-located events」的 limitation。

## Hawkes Process Limit Order Book Project

主線連到 [[Hawkes process limit order book project]]。這一組 paper 被保留的是 [[Conditional intensity|conditional intensity]]、[[Hawkes kernel matrix|kernel matrix]]、branching/stability、mark distribution、neural history dependence。被壓掉的是金融市場背景、表格堆疊、以及可以用文字公式重寫的模型定義截圖。

### Bacry and Muzy 2015

主筆記：[[Bacry Muzy 2015 Hawkes second-order statistics]]。

保留：multivariate Hawkes intensity、kernel influence function、second-order statistics 對 nonparametric kernel estimation 的意義。

壓掉：

- [[Wiener filter|Wiener]]-Hopf 方程完整推導：對目前報告主線太重；先保留「second-order statistics can identify kernels」這個概念即可。
- 公式截圖：已用 [[Hawkes project notation]] 統一 notation，避免每篇 paper 的符號互相打架。
- 細緻估計演算法步驟：除非 final report 要主打 estimation method，否則只需要解釋它為何提供 interpretable kernel。
- 過多 theoretical conditions：先把 stability 放到 [[Hawkes branching ratio]]，避免主筆記變成機率論筆記。

回頭使用時機：要寫更數學的 methodology section，或要比較 parametric vs nonparametric Hawkes estimation。

### Compound Hawkes LOB Paper

主筆記：[[Compound Hawkes process for LOB order size modeling]]。

保留：event time/type 與 order-size mark 的結合、calibrated kernels、market impact/volume interpretation。

壓掉：

- 大量金融市場背景和 simulator description：目前報告主線是 signal/event modeling，不是建立交易模擬器。
- 多張 fit/result tables：若只是比較數字，不如用文字說明「marks make intensity model financially meaningful」；表格要等 final report 有明確 comparison metric 才放。
- 細節參數、calibration setup、資料清理流程：除非要寫 experiment section，否則先不放。
- 可由公式表達的 compound process 定義截圖：已用 $S_i(t)=\sum v_n^i$ 這類文字公式整理。

回頭使用時機：需要寫 empirical results、[[Market impact simulation|market impact]] simulation，或要補 stylized facts。

### Neural Marked Hawkes Process Paper

主筆記：[[Neural marked Hawkes process for LOB]]。

保留：history encoder、intensity head、mark head、[[History dependent mark distribution]]。這是用來說明 neural method 為何比固定 kernel/parametric mark 更 flexible。

壓掉：

- 大量 architecture/training implementation details：初稿只需要理解模組分工，不需要每個 layer 或 hyperparameter。
- 結果表格截圖：表格適合 final report 的 comparison section，但在筆記階段容易變成「看分數」而不是懂模型。
- benchmark dataset 細節：等你確定要把 neural [[Marked Hawkes process|marked Hawkes]] 作為主題中心，再回頭補。
- loss function 的完整 technical derivation：先用 conditional intensity + mark likelihood 的概念理解即可。

回頭使用時機：final report 若選 Hawkes/LOB 題目，且想把 neural model 作為 conclusion 前的 advanced extension，就需要補 training objective、evaluation metric、與 baseline table。

## How To Use This Note

寫報告時先從 project hub 進去，不要從這篇開始。當你覺得某一節太薄，或老師可能會問「資料怎麼來、實驗怎麼驗證、參數怎麼選」時，再回這篇找該補哪一類細節。

最重要的原則：主文要講清楚 model assumption 和 signal-processing interpretation；paper-specific details 只在它支撐論點時才放進去。
