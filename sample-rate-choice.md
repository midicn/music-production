---
id: sample-rate-choice
site: prod
cat: A4
title: 采样率选择
title_en: Choosing a Sample Rate
summary: 采样率决定能记录的最高频率，也决定体积与流程兼容
summary_en: Sample rate sets the highest frequency you can capture, and the file size and workflow that follow.
level: standard
tags: [录音, 采样率, 交付]
tags_en: [recording, sample rate, delivery]
alias: [采样率, 采样频率, 取样率, sample rate, sample frequency]
links:
  - "[[glossary:sample-rate]]"
  - "[[glossary:bit-depth]]"
  - "[[instrument:cymbals]]"
instances:
  - groove-001062 | 拉丁打击乐里镲与沙锤的能量集中在高频，降采样先变钝
  - mutopia-000981 | 人声独唱，齿音集中在高频，采样率的选择在这里可听
  - openscore-001257 | 钢琴与人声，高音区泛音密集，速率不足先失去光泽
sources:
  - Pohlmann, Principles of Digital Audio, sampling and conversion chapters
  - AES recommended practice for sampling frequency and studio interchange
updated: 2026-10-28
---

::: zh
## 问题

采样率决定能记录的最高频率，也决定文件大小与处理负担。44.1、48 与 96 kHz 没有绝对优劣，只有与用途、后续流程是否匹配。

## 信号链

话筒信号经话放进入转换器的抗混叠滤波器，再按设定速率采样。转换器内部的过采样与滤波设计，往往比工程上标称的数字更影响高频表现。

## 摆位与参数

音乐成品用 44.1 kHz，影视与视频用 48 kHz，需要大量变调或重处理时用 88.2 或 96 kHz。整张工程只用一个速率，避免反复转换。交付前先确认平台要求，不要等到母带阶段才改。

```audiolab
{"type":"instrument","drum":"49","synth":"perc","phrase":["49","49"],"label":"镲片的高频先受影响","label_en":"Cymbal top end feels it first","hint":"先听镲的能量，再想采样率把最上面一截切在哪里","hint_en":"Hear the cymbal energy, then picture where the rate cuts the top"}
```

## 听什么

拿镲片与齿音多的素材对比：低速率下 15 kHz 以上先变钝，高速率经过多次变调仍保留边缘。差别很细，听不出时按交付格式选即可。

## 常见误解

- **96 kHz 一定更好听** → 多数回放设备听不出，代价是体积与 CPU。
- **采样率可以随时改** → 每次转换都是一次滤波。
- **44.1 与 48 只差一点** → 差的是整条流程的兼容性。
:::

::: en
## The problem

Sample rate sets the highest frequency you can capture, and with it file size and processing load. 44.1, 48 and 96 kHz are not better or worse; they either match the job and workflow, or they do not.

## Signal chain

The microphone signal passes through the preamp into the converter's anti-aliasing filter, then is sampled at the chosen rate. The converter's oversampling and filter design often matter more than the number on the session.

## Placement and settings

Use 44.1 kHz for music releases, 48 kHz for film and video, and 88.2 or 96 kHz for heavy pitch shifting. Keep one rate for the whole project and avoid repeated conversion. Confirm the delivery requirement before mastering.

```audiolab
{"type": "instrument", "drum": "49", "synth": "perc", "phrase": ["49", "49"], "label": "Cymbal top end feels it first", "label_en": "Cymbal top end feels it first", "hint": "先听镲的能量，再想采样率把最上面一截切在哪里", "hint_en": "Hear the cymbal energy, then picture where the rate cuts the top"}
```

## What to listen for

Compare material rich in cymbals and sibilance. At a low rate the top above roughly 15 kHz dulls first; at a high rate the edge survives repeated pitch shifts. The difference is subtle, so when you cannot hear it, choose by delivery format.

## Common misconceptions

- **96 kHz always sounds better** → most playback systems cannot show it, and it costs space and CPU.
- **The rate can be changed at any time** → every conversion is another filter.
- **44.1 and 48 are almost the same** → what differs is compatibility along the chain.
:::
