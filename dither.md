---
id: dither
site: prod
cat: B5
title: 抖动
title_en: Dither
summary: 降位深前加一点噪声，把量化失真换成细噪。
summary_en: A trace of noise before bit-depth reduction turns quantization distortion into a steady hiss.
level: standard
tags: [位深, 量化, 噪声整形, 母带]
tags_en: [bit depth, quantization, noise shaping, mastering]
alias: [抖动, 抖动噪声, 量化噪声, dither]
links:
  - "[[glossary:dither]]"
  - "[[glossary:bit-depth]]"
  - "[[glossary:noise-floor]]"
instances:
  - giantmidi-009128 | 道兰《鲁特琴教程集》的钢琴改编音量小、织体细，量化台阶在安静处最明显（C1）
  - openscore-000000 | 艺术歌曲人声与钢琴同时收弱，抖动与否在尾音上分得开（C1）
  - atepp-000369 | 格里格《夜曲》尾音渐弱，噪声整形把噪声推向高频后更耐听（C1）
sources:
  - Lipschitz 与 Vanderkooy 关于抖动的公开论文，依原文核查，未抄文本
  - Pohlmann, Principles of Digital Audio, quantization chapters — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

降位深或把浮点混音落成定点文件时，最弱的部分会撞上量化台阶，得到跟着信号变化的失真。

## 原理

量化把连续值截到最近的格点，误差在低电平、周期性强的信号上会排成有规律的形状，听感沙哑。抖动在截断前加入约一个最低位的随机噪声，让误差与信号失去相关，代价是底噪略抬。噪声整形再把噪声推向高频，人耳不敏感处多承担，带内噪声更低。

## 参数与做法

16 位交付用 TPDF 抖动，配适度的噪声整形。只在最后一次降位深时加，加完不要再改增益或做二次编码。24 位通常不必，噪声底已低于录音本底。高频吃重的素材选较轻的整形档。

## 听什么

在鲁特琴曲集的安静段落听量化台阶，在艺术歌曲的收尾听人声与钢琴同时变弱时是否出现沙粒，在《夜曲》的长尾音里听细噪是否均匀。无抖动时尾音一段段发干，有抖动时是连续的细沙。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C6","G5","E5","C5"],"label":"高音区的弱奏","label_en":"A quiet line in the high register","hint":"把音量调低，听尾音是连续细噪还是一段段发干","hint_en":"Turn it down and hear whether the tail is steady hiss or dry steps"}
```

## 常见误解

抖动加噪声，所以一定降低音质；它换来的是失真变噪声，通常更耐听。也不必每次导出都加，只有降位深时才需要。24 位加抖动没有意义。它不能修复已经削波的素材。
:::

::: en
## The question

Reduce bit depth, or print a floating-point mix to a fixed-point file, and the quietest parts hit the steps.

## How it works

Quantization rounds values to the nearest step, and on quiet, periodic material the error lines up into audible grain. Dither adds random noise of about one least significant bit before rounding, so the error decorrelates and the floor rises slightly. Noise shaping then pushes it toward high frequencies, where the ear is less sensitive.

## Settings and practice

Use TPDF dither with moderate shaping for 16-bit delivery. Add it once at the final reduction, then change no gain and encode nothing further. At 24 bit it is usually unnecessary, since the floor sits below the recording. Choose lighter shaping for bright material.

## What to listen for

In quiet lute pieces, listen for the steps. At a song's end, hear whether voice and piano turn sandy as they fade. In a long nocturne tail, check whether the hiss stays even. Without dither the tail dries in patches; with it you hear continuous fine sand.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C6", "G5", "E5", "C5"], "label": "A quiet line in the high register", "label_en": "A quiet line in the high register", "hint": "把音量调低，听尾音是连续细噪还是一段段发干", "hint_en": "Turn it down and hear whether the tail is steady hiss or dry steps"}
```

## Common misconceptions

Dither adds noise, so it must reduce quality; what it trades is distortion for noise, which wears better. It is not needed on every export, only when reducing depth. Adding it at 24 bit achieves nothing. It cannot repair already clipped material.
:::
