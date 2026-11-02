---
id: adc-dac-conversion
site: prod
cat: B5
title: 模拟到数字转换
title_en: Analog-to-Digital and Digital-to-Analog Conversion
summary: 采样与重建两道关口，决定数字音频保留了什么。
summary_en: Sampling and reconstruction are the two gates that decide what digital audio keeps.
level: standard
tags: [采样, 转换器, 抗混叠, 重建滤波]
tags_en: [sampling, converters, anti-aliasing, reconstruction]
alias: [模拟数字转换, 模数转换, 数模转换, ADC, DAC, AD/DA]
links:
  - "[[glossary:sample-rate]]"
  - "[[glossary:oversampling]]"
  - "[[glossary:signal-to-noise]]"
instances:
  - cyberhymnal-006346 | 持续和声的音符素材，可另渲染后用于转换实验（C1） | Sustained-harmony notes for a separately rendered conversion experiment (C1)
  - atepp-000195 | 钢琴弱奏的音乐参照，不包含不同转换器录音（C1） | A quiet-piano musical reference without recordings from different converters (C1)
  - giantmidi-003263 | 钢琴音符与时值素材，不记录原录音的量化噪声（C1） | Piano-note and timing data without original-recording quantisation noise (C1)
sources:
  - "https://docs.scipy.org/doc/scipy/reference/generated/scipy.signal.resample_poly.html"
  - Pohlmann, Principles of Digital Audio, sampling and conversion chapters.
  - 转换器滤波模式与时钟的差异（厂商公开技术文档）。
updated: 2026-11-02
---

::: zh
## 问题

ADC 把模拟输入转换为数字样点，DAC 把数字样点转换为模拟输出。评价一套转换链，应看输入范围、噪声、失真、频率响应和同步条件；换设备不保证一定听到高频或尾音变化。

## 原理

采样按固定时间间隔取值，并非每个波形周期只取一点。输入带宽需受抗混叠滤波限制；幅度再由有限精度表示，重新量化会产生误差。DAC 的具体实现可能包含过采样、插值和噪声整形，最终用模拟滤波抑制采样镜像。阶梯图是解释方式，不代表所有转换器都以相同电路输出阶梯。

## 参数与做法

先使工程采样率、输入格式和数字接口同步设置一致，再根据电平表给录音留出峰值余量。提高标称采样率不能补回已经丢失的信息。比较转换器时保持模拟电平、路径、采样率和监听条件一致，并校准时间差；需要多台数字设备直连时，按各设备手册设置时钟或采样率转换。

## 听什么

可先用回环录音检查通道是否过载、底噪是否异常，再用同一输入信号比较两条转换路径。遇到发闷、失真或噪声，不要直接归因于滤波太陡或位深不足，还要排查电平、线缆、输入模式和原素材。

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"reed","phrase":["C3","G3","C4","E4","G4"],"label":"持续和声参照","label_en":"Sustained-harmony reference","hint":"此演示合成音符，没有经过可切换的 AD/DA 转换器。要比较转换，须使用受控录音或实际设备回环。","hint_en":"This synthesizes notes without switchable AD/DA hardware. Compare converters using controlled recordings or an actual hardware loopback."}
```

## 常见误解

采样率限定理论可表示带宽，实际可用通带还受滤波器过渡带影响。位深涉及幅度量化，整条设备链的实际信噪比未必达到标称位数。DAC 输出的重建质量要结合测量与受控听音评估。
:::

::: en
## The question

An ADC converts analogue input to digital samples; a DAC converts samples to analogue output. Evaluate input range, noise, distortion, frequency response and synchronisation. Changing devices does not guarantee an audible change in treble or decay.

## How it works

Sampling takes values at fixed time intervals, not one value per waveform cycle. Anti-alias filtering limits input bandwidth; finite amplitude precision creates quantisation error. A DAC may use oversampling, interpolation and noise shaping, followed by analogue filtering to suppress sampling images. A staircase illustration does not imply that every converter uses the same output circuit.

## Settings and practice

Match session rate, input format and digital-interface synchronisation, then leave suitable peak headroom. Raising a nominal sample rate cannot restore lost information. Compare converters with the same analogue level, path, rate and monitoring, compensating timing differences. For linked digital devices, configure clocks or sample-rate conversion according to their manuals.

## What to listen for

Use a loopback recording to check overload and abnormal noise, then compare paths with one input signal. Dullness, distortion or noise do not identify filter steepness or inadequate bit depth by themselves; also check level, cabling, input mode and source material.

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"reed","phrase":["C3","G3","C4","E4","G4"],"label":"Sustained-harmony reference","label_en":"Sustained-harmony reference","hint":"This synthesizes notes without switchable AD/DA hardware. Compare converters using controlled recordings or an actual hardware loopback.","hint_en":"This synthesizes notes without switchable AD/DA hardware. Compare converters using controlled recordings or an actual hardware loopback."}
```

## Common misconceptions

Sample rate sets a theoretical representable bandwidth; the usable passband also depends on the filter transition. Bit depth concerns amplitude quantisation, while actual system signal-to-noise ratio may fall short of its nominal depth. Assess DAC reconstruction with measurements and controlled listening.
:::
