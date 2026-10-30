---
id: sampling-rate-and-nyquist
site: prod
cat: B4
title: 采样率与奈奎斯特
title_en: Sample Rate and Nyquist
summary: 采样率划出可记录的最高频率，奈奎斯特给出这条上限。
summary_en: Sample rate sets the highest frequency a system can capture; Nyquist gives that ceiling.
level: standard
tags: [采样率, 奈奎斯特, 数字音频]
tags_en: [sample rate, nyquist, digital audio]
alias: [采样率, 奈奎斯特频率, 抗混叠上限, nyquist frequency]
links:
  - "[[glossary:sample-rate]]"
  - "[[glossary:harmonics]]"
  - "[[glossary:pitch]]"
  - "[[instrument:samplers]]"
instances:
  - pdmx-000251 | 钢片琴的高音泛音接近听觉上限，采样率不足时这里最先变空
  - atepp-000381 | 格里格《钟声》依赖高音区的金属泛音，降采样后最先变钝
  - groove-000000 | 放克鼓循环的踩镲集中在高频，低采样率下镲片先失去边缘
sources:
  - Harry Nyquist, Certain Topics in Telegraph Transmission Theory — 采样上限的原始论述核对，未抄原文
  - Ken C. Pohlmann, Principles of Digital Audio — 采样率与转换滤波的通行说法核对，未抄原文
updated: 2026-10-28
---

::: zh
## 问题

采样每秒只取有限个点，为什么还能还原连续的声音？又为什么有些高频消失后，变成了另一种声音？

## 原理

采样把连续波形按固定间隔取值。每秒取 fs 个点，能表示的最高频率是 fs/2，也就是奈奎斯特频率。44.1 kHz 的上限约 22.05 kHz，刚好覆盖多数人的听觉范围。超过上限的成分不会凭空消失，而会折回低频，变成与原始演奏无关的音。所以采样前必须用抗混叠滤波把上限以上压掉，这一步通常由转换芯片完成。48 kHz 给影视与视频留出余量；96 kHz 更多是为后续处理与变调留空间，而不是让耳朵听到更高。

## 做法与参数

音乐交付常用 44.1 kHz 或 48 kHz。素材要大幅变调或拉伸时，录 88.2 或 96 kHz，给算法留余量。降采样要先滤波再抽点，顺序不能反。检查频谱时看 20 kHz 附近有没有突然截断，那通常是滤波器的脚印。

## 听什么

先听钢片琴或钟类的高音，注意上方那层细碎的泛音。再把同一段降到 22.05 kHz 播放，高频会变暗，某些亮片会变成中频的沙声。踩镲的金属感也会先失去边缘。最后听低音，采样率对低频的影响很小，别把变调感错当成采样率问题。

## 常见误解

以为采样率越高声音越好；以为超声波成分完全无用；以为降采样只是把高频音量调小。

```audiolab
{"type":"instrument","gm":"Celesta","synth":"struck","phrase":["C6","E6","G6","C7"],"label":"钢片琴的高音泛音","label_en":"High partials on celesta","hint":"切到真实音色，听高音区上方的细碎泛音；再想同一段降到 22.05 kHz 后，这些泛音会先消失","hint_en":"Switch to the real timbre and hear the fine partials above the high notes; then imagine the same phrase at 22.05 kHz, where those partials go first"}
```
:::

::: en
## The problem

A sampler stores only a limited number of points each second, yet the result sounds continuous. Why does some high-frequency content seem to become a different sound instead of disappearing?

## How it works

Sampling reads a continuous waveform at fixed intervals. With fs points per second, the highest representable frequency is fs/2, the Nyquist frequency. At 44.1 kHz the ceiling is about 22.05 kHz, covering most listeners. Content above the ceiling does not vanish; it folds back into the audible band as unrelated tones. An anti-aliasing filter before conversion removes that content, usually inside the converter chip. A 48 kHz rate leaves room for video work, while 96 kHz mainly gives processing and pitch shifting more headroom, not more hearing.

## Practice and settings

Deliver music at 44.1 or 48 kHz. Record at 88.2 or 96 kHz when material will be shifted or stretched far, giving the algorithm room. When downsampling, filter first and drop points second; the order matters. Inspect the spectrum near 20 kHz for a sudden cliff, the filter's footprint.

## What to listen for

Start with celesta or bell high notes and notice the fine layer of partials above them. Play the same passage at 22.05 kHz: the top turns dull and some bright sparks become midrange hiss. Hi-hats lose their edge first. Hear the bass, which barely changes, and do not mistake a transposition artifact for a rate problem.

## Common misconceptions

That a higher rate always sounds better; that ultrasonic content is useless; that downsampling just turns down the treble.

```audiolab
{"type": "instrument", "gm": "Celesta", "synth": "struck", "phrase": ["C6", "E6", "G6", "C7"], "label": "High partials on celesta", "label_en": "High partials on celesta", "hint": "Switch to the real timbre and hear the fine partials above the high notes; then imagine the same phrase at 22.05 kHz, where those partials go first", "hint_en": "Switch to the real timbre and hear the fine partials above the high notes; then imagine the same phrase at 22.05 kHz, where those partials go first"}
```
:::
