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
  - cyberhymnal-006346 | 管风琴持续和弦泛音密集，重建滤波的痕迹在稳定音上最容易听出（C1）
  - atepp-000195 | 德彪西《月光》弱奏层次多，位深不够时最轻的触键先糊掉（C1）
  - giantmidi-003263 | 萨蒂《裸体歌舞》整体很轻，噪声底与量化台阶在安静段最清楚（C1）
sources:
  - Pohlmann, Principles of Digital Audio, sampling and conversion chapters.
  - 转换器滤波模式与时钟的差异（厂商公开技术文档）。
updated: 2026-10-28
---

::: zh
## 问题

声音进电脑前要变成数字，离开时再变回模拟。同一段演奏，换一套转换器，高频、弱奏与尾音就会不同。

## 原理

采样每周期取一点，前提是先把高于采样率一半的成分滤掉，否则会折返回可听频段。取到的值要量化成有限台阶，余数成为噪声。回放时样点先还原成阶梯，再由重建滤波抹平。真实转换器的滤波有过渡带，量化有噪声，时钟还会抖动。过采样把噪声摊到更宽频段再滤回，减轻模拟滤波的压力。

## 参数与做法

44.1 kHz 与 48 kHz 最常见，96 kHz 留给需要大幅移调或重度处理的素材。录音留 6 到 12 dB 余量，各转换器共用字时钟。线性相位保瞬态形状但会预振铃，最小相位延迟低。别在不同采样率之间反复转换。

## 听什么

管风琴持续和弦上听泛音是否被削薄，《月光》弱奏里听最轻的触键是否还在，《裸体歌舞》安静段听噪声底。高频发闷多半是抗混叠滤波太陡，弱奏发糊多半是位深不够。

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"reed","phrase":["C3","G3","C4","E4","G4"],"label":"管风琴持续和弦","label_en":"A sustained organ chord","hint":"先听泛音是否完整，再想采样与重建各自留下了什么","hint_en":"Hear the overtones first, then what sampling and reconstruction each leave behind"}
```

## 常见误解

采样率高不等于好听，44.1 kHz 已覆盖人耳范围。位深不只影响音量，它决定弱信号能否离开噪声底。DAC 不是被动接线，它决定重建滤波的形状。96 kHz 采样记录的最高频率是 48 kHz。
:::

::: en
## The question

A converter turns voltage into numbers and back again. Change the converter and the air, the soft notes and the tails change with it.

## How it works

Sampling needs a low-pass filter first, or content above half the rate folds back into the audible band. Each sample is then quantized, and the remainder becomes noise. Playback rebuilds a staircase and smooths it with a reconstruction filter. Real converters add filter transition bands, quantization noise and clock jitter. Oversampling spreads that noise wider before filtering it back, easing the analog stage.

## Settings and practice

44.1 and 48 kHz cover most work; 96 kHz suits heavy pitch shifting. Track with 6 to 12 dB of headroom and one word clock. Linear-phase filters keep transients but pre-ring; minimum-phase filters delay less. Avoid repeated rate conversions.

## What to listen for

On a sustained organ chord, hear whether overtones thin. In the soft passages of Clair de lune, hear whether the lightest touch survives. In quiet Satie, listen to the noise floor. Dull highs suggest a steep anti-alias filter; smeared soft notes suggest too few bits.

```audiolab
{"type": "instrument", "gm": "Church Organ", "synth": "reed", "phrase": ["C3", "G3", "C4", "E4", "G4"], "label": "A sustained organ chord", "label_en": "A sustained organ chord", "hint": "先听泛音是否完整，再想采样与重建各自留下了什么", "hint_en": "Hear the overtones first, then what sampling and reconstruction each leave behind"}
```

## Common misconceptions

A higher rate is not automatically better, since 44.1 kHz covers the audible range. Bit depth is not just loudness; it decides whether quiet detail clears the noise. A DAC is not passive wiring. And 96 kHz captures content only up to 48 kHz.
:::
