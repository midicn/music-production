---
id: bit-depth-and-noise-floor
site: prod
cat: A4
title: 位深与噪声底
title_en: Bit Depth and Noise Floor
summary: 位深决定量化噪声的底，也就是弱奏能安静到哪里
summary_en: Bit depth sets the quantisation noise floor, and therefore how quiet a soft passage can stay.
level: standard
tags: [录音, 位深, 噪声]
tags_en: [recording, bit depth, noise]
alias: [位深, 比特深度, 量化噪声, bit depth, word length, noise floor]
links:
  - "[[glossary:bit-depth]]"
  - "[[glossary:noise-floor]]"
  - "[[glossary:dither]]"
instances:
  - atepp-005000 | 变奏尾段极弱，尾音能不能留住就看噪声底
  - openscore-000818 | 弱唱与轻触钢琴，两轨都要靠位深保住细节
  - mutopia-001594 | 吉他练习曲尾音长，量化噪声会在衰减末段浮出
sources:
  - Lipshitz, Wannamaker and Vanderkooy, Quantization and Dither, JAES
  - AES Convention paper on bit-depth audibility in quiet passages
updated: 2026-10-28
---

::: zh
## 问题

位深决定量化噪声的底，也就是弱奏能安静到哪里。24 位与 16 位的差别不是清晰度，而是安静程度与余量。

## 信号链

转换器把模拟电压切成离散台阶，台阶越细，量化误差越小。误差分布在高频，听感接近一层极轻的嘶声；信号越弱，这层嘶声占的比例越大。

## 摆位与参数

录音用 24 位，峰值落在 -12 至 -6 dBFS，给意外留余量。混音内部用 32 位浮点，导出母带再降到 16 位并加抖动。不要在 16 位工程里大幅推子，那会把噪声底一起推上来。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4"],"label":"弱奏尾音的去处","label_en":"Where a soft tail goes","hint":"把监听推到刚好听清，尾音消失前那段就是噪声底","hint_en":"Raise the monitor until it is just audible; the gap before the tail vanishes is the noise floor"}
```

## 听什么

找一段极弱的钢琴尾音，把监听推到刚好听清：24 位素材在尾音消失前仍是干净的，16 位会有轻微颗粒。再把同一段提升 20 dB，听底噪是否先冒出来。

## 常见误解

- **24 位更清晰** → 它降低的是噪声底，不是失真。
- **浮点可以无限推** → 它防削波，不防噪声。
- **抖动可以省** → 降到 16 位时不加抖动，弱奏会被量化噪声切碎。
:::

::: en
## The problem

Bit depth sets the level of quantisation noise, and therefore how quiet a soft passage can stay. The difference between 24 and 16 bits is not clarity but silence and headroom.

## Signal chain

The converter cuts the analogue voltage into discrete steps; finer steps mean smaller quantisation error. The error spreads across the high frequencies and sounds like a very light hiss, which takes up a larger share as the signal gets quieter.

## Placement and settings

Record at 24 bits with peaks between -12 and -6 dBFS to leave room for surprises. Mix internally at 32-bit float, then reduce to 16 bits with dither for the master. Do not make large fader moves in a 16-bit project; the noise floor rises with them.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4"], "label": "Where a soft tail goes", "label_en": "Where a soft tail goes", "hint": "把监听推到刚好听清，尾音消失前那段就是噪声底", "hint_en": "Raise the monitor until it is just audible; the gap before the tail vanishes is the noise floor"}
```

## What to listen for

Find a very soft piano tail and raise the monitor until it is just audible: a 24-bit take stays clean until the tail vanishes, while a 16-bit take shows a faint grain. Then lift the same passage by 20 dB and hear whether the noise floor arrives first.

## Common misconceptions

- **24 bits sound clearer** → they lower the noise floor, not the distortion.
- **Float lets you push anything** → it prevents clipping, not noise.
- **Dither is optional** → without it, soft passages break up when reduced to 16 bits.
:::
