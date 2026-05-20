---
created: 2026-05-21
aliases:
  - "ADSP Write2"
  - "Write2"
categories:
  - "[[Evergreen]]"
  - "[[Indexes]]"
topics:
  - "[[Advanced digital signal processing]]"
  - "[[FIR filters]]"
type:
  - "[[MOCs]]"
status:
  - "[[Active]]"
tags:
  - "adsp"
  - "fir"
  - "filter-design"
pages:
  - "ADSP_Write2/page_001.png-page_033.png"
---

# ADSP Write2 FIR design details

Write2 延伸 Write1 的 FIR design，重點是把 error specification、weight function、linear phase symmetry、frequency sampling method 全部整理成可以設計濾波器的流程。

## Concepts

- Specification: [[Filter transition band]], [[Weighted approximation error]], [[Optimization norm for filter design]]
- Symmetry: [[Four FIR filter symmetry types]], [[Linear phase FIR filter]]
- Design methods: [[Least MSE FIR design]], [[Minimax FIR design]], [[Frequency sampling FIR design]]
- Implementation notes: [[Python and MATLAB for signal processing]]

## 講義截圖

![Filter length, transition band, and ripple](assets/adsp/ADSP_Write2_p001_filter_length_transition_ripple.png)

![Weight functions and accuracy](assets/adsp/ADSP_Write2_p004_weight_function_accuracy.png)

![Four FIR symmetry types](assets/adsp/ADSP_Write2_p010_four_fir_types.png)

![Frequency sampling FIR method](assets/adsp/ADSP_Write2_p026_frequency_sampling_method.png)

