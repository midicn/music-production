---
id: headroom-and-clipping
site: prod
cat: B5
title: 余量与削波
title_en: Headroom and Clipping
summary: 数字满刻度是硬墙，留出余量才能容下瞬态与后续处理。
summary_en: Digital full scale is a hard wall; headroom is what lets transients and later processing fit.
level: standard
tags: [余量, 削波, 满刻度, 增益结构]
tags_en: [headroom, clipping, full scale, gain structure]
alias: [余量, 削波, 过载, headroom, clipping]
links:
  - "[[glossary:headroom]]"
  - "[[glossary:bit-depth]]"
  - "[[glossary:compressor]]"
instances:
  - groove-000005 | 87 BPM 嘻哈鼓组，底鼓与军鼓叠加时最容易顶到满刻度（C1）
  - atepp-001114 | 肖邦叙事曲现场录音，演奏者的重和弦与观众噪声叠加后需要余量（C1）
  - mutopia-000498 | 贝多芬第五第二乐章，弦乐渐强层层叠加，余量不足时先糊后削（C1）
sources:
  - 浮点与定点满刻度的差别，对照数字音频惯例整理。
  - 增益结构的分级做法（录音工程公开资料）。
updated: 2026-10-28
---

::: zh
## 起点：一个问题

数字音频的上限是 0 dBFS，越过就是削波，波形顶部被切平，产生刺耳的高频。每次加效果、加轨道、加自动化都可能把电平推高，所以录音与混音都要预留余量。余量不是浪费动态，而是给后面的每一步留空间。

## 它怎么工作

定点格式在 0 dBFS 处硬切，超出的部分直接丢掉。浮点格式在内部有巨大的动态余量，超过 0 dBFS 不会立刻削波，但送出到定点设备或编码器时还是会切。削波产生的高频谐波听上去像破裂声，短暂而过分的削波有时被当成响度手段，代价是失真。多个轨道相加时峰值不是简单相加，但相位对齐时会叠加得很高，所以总线上要留更多余量。

## 参数与做法

录音时峰值定在负 12 到负 6 dBFS，给演奏的意外留空间。混音时总线峰值留 6 dB 左右，母带前留 3 到 6 dB。用浮点工程，别在中间环节反复定点化。插件前后都看一眼电平，有的插件会明显增益。总线限幅只用来接住瞬态，不用来整体推响。练耳时把削波与压缩区分开，前者是波形被切，后者是动态被收。

## 耳朵要抓的点

在嘻哈鼓组里听底鼓与军鼓同时落下时是否发破，在现场叙事曲里听重和弦与掌声叠加处是否刺耳，在弦乐渐强里听层次是否还分得开。真正削波的声音不会变响，只会变脏。

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E1","E1","G1","A1","E1","E1","D1","E1"],"label":"低频顶到上限","label_en":"Bass against the ceiling","hint":"低频能量最大，余量不足时最先在这里削波","hint_en":"Low end carries the most energy and clips first when headroom runs out"}
```
:::

::: en
## Starting point: a problem

Digital audio tops out at 0 dBFS, and anything beyond is clipped, with the tops of the waveform sliced flat and harsh high frequencies left behind. Every plug-in, extra track and automation move can raise the level, so both recording and mixing need spare room. Headroom is not wasted dynamics; it is space for every step that follows.

## How it works

Fixed-point formats cut hard at 0 dBFS and discard what exceeds it. Floating point carries enormous internal range and does not clip immediately above zero, but it still clips when handed to a fixed-point device or encoder. Clipping generates high harmonics that sound like breakup, and brief heavy clipping is sometimes used as a loudness trick at the cost of distortion. Summing tracks does not add peaks arithmetically, but when phases align they can stack very high, which is why buses need more room.

## Settings and practice

Record with peaks around minus 12 to minus 6 dBFS to cover performance surprises. Mix with bus peaks near minus 6 dB and leave 3 to 6 dB before mastering. Work in floating point and avoid repeated fixed-point conversions in the chain. Check level before and after every plug-in, since some add obvious gain. Use a bus limiter to catch transients, not to push the whole mix louder. When ear training, separate clipping from compression: one slices the waveform, the other narrows the dynamics.

## What the ear catches

On the hip-hop kit, whether kick and snare together break up; on the live ballade, whether heavy chords plus applause turn harsh; on the string crescendo, whether the layers stay separate. Genuine clipping does not sound louder, only dirtier.

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E1","E1","G1","A1","E1","E1","D1","E1"],"label":"Bass against the ceiling","label_en":"Bass against the ceiling","hint":"Low end carries the most energy and clips first when headroom runs out","hint_en":"Low end carries the most energy and clips first when headroom runs out"}
```
:::
