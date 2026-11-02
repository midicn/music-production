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
  - giantmidi-009128 | 钢琴改编的音符素材，可另行制作低位深淡出实验（C1） | Notes from a piano arrangement for a separately rendered low-bit-depth fade (C1)
  - openscore-000000 | 歌声与钢琴的声部参照，不包含加/不加抖动的导出（C1） | Voice-and-piano parts without dithered and undithered exports (C1)
  - atepp-000369 | 渐弱段落的音乐参照，不是噪声整形效果对照（C1） | A musical reference for a fading passage, not a noise-shaping comparison (C1)
sources:
  - "https://downloads.izotope.com/docs/rx6/39-dither/index.html"
  - Lipschitz 与 Vanderkooy 关于抖动的公开论文.
updated: 2026-11-02
---

::: zh
## 问题

降位深或把浮点混音落成定点文件时，最弱的部分会撞上量化台阶，得到跟着信号变化的失真。

## 原理

量化把连续值截到最近的格点，误差在低电平、周期性强的信号上会排成有规律的形状，听感沙哑。抖动在截断前加入约一个最低位的随机噪声，让误差与信号失去相关，代价是底噪略抬。噪声整形再把噪声推向高频，人耳不敏感处多承担，带内噪声更低。

## 参数与做法

若交付要求 16 位定点 PCM，可在最后的限幅和增益处理之后、量化输出时加入合适的抖动。TPDF 是常见选择，是否加噪声整形按软件实现与用途决定。24 位也会重新量化，只是新增噪声常远低于素材本底；不能说加抖动必然没有意义。压缩编码属于另一个环节，保存高质量母版后再生成所需发行文件。

## 听什么

用同一条低电平正弦或音频淡出制作加抖动与不加抖动的低位深导出，匹配电平后比较失真成分与噪声。测试应使用真实音频渲染，本站的鲁特琴、人声或钢琴 MIDI 只提供弱奏听感素材，不包含抖动开关，不能听它就判断某种算法好坏。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C6","G5","E5","C5"],"label":"弱音与衰减","label_en":"Soft notes and decay","hint":"听音符何时变弱；此演示没有加/不加抖动两种渲染，不能据此评价抖动算法。","hint_en":"Listen to the decay. There are no dithered and undithered renders here, so this block does not evaluate a dithering algorithm."}
```

## 常见误解

抖动把与信号相关的量化失真转为较稳定的噪声，通常用于降低最终定点量化的失真。它不会消除原录音的底噪，也不能修复已经削波的波形。反复加抖动只会累积噪声。
:::

::: en
## The question

Reduce bit depth, or print a floating-point mix to a fixed-point file, and the quietest parts hit the steps.

## How it works

Quantization rounds values to the nearest step, and on quiet, periodic material the error lines up into audible grain. Dither adds random noise of about one least significant bit before rounding, so the error decorrelates and the floor rises slightly. Noise shaping then pushes it toward high frequencies, where the ear is less sensitive.

## Settings and practice

For 16-bit fixed-point PCM delivery, apply suitable dither at output quantisation after final limiting and gain changes. TPDF is a common option; noise shaping depends on implementation and use. Requantisation also occurs at 24 bits, though its added noise often lies far below the recording's existing noise. Preserve a high-quality master before making required lossy distribution files.

## What to listen for

Render the same low-level sine or audio fade at reduced depth with and without dither, then compare distortion and noise at matched gain. This needs actual audio renders. The lute, voice and piano MIDI examples only supply quiet passages; they have no dither switch and cannot rank dithering algorithms.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C6","G5","E5","C5"],"label":"Soft notes and decay","label_en":"Soft notes and decay","hint":"Listen to the decay. There are no dithered and undithered renders here, so this block does not evaluate a dithering algorithm.","hint_en":"Listen to the decay. There are no dithered and undithered renders here, so this block does not evaluate a dithering algorithm."}
```

## Common misconceptions

Dither trades signal-correlated quantisation distortion for more stable noise at fixed-point quantisation. It does not remove recording noise or repair a clipped waveform. Repeated applications accumulate noise.
:::
