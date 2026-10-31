---
id: distortion
site: prod
cat: A7
title: 失真与过载
title_en: Distortion and Overdrive
summary: 三种削波程度如何改写谐波与动态，而不只是变脏。
summary_en: How three degrees of clipping rewrite harmonics and dynamics rather than merely adding dirt.
level: standard
tags: [效果器, 非线性, 失真, 谐波]
tags_en: [effects, nonlinear, distortion, harmonics]
alias: [失真, 过载, 模糊, 削波, distortion, overdrive, fuzz]
links:
  - "[[glossary:harmonics]]"
  - "[[glossary:clipping]]"
  - "[[instrument:electric-guitar]]"
instances:
  - cyberhymnal-000000 | 风琴持续和弦的泛音密，削波后新增的谐波最容易分辨
  - oga-000004 | 战斗音乐的铜管齐奏厚，过载会让齐奏边缘先变硬
  - mutopia-000005 | 古典吉他的拨弦颗粒细，少量失真会把指尖噪声一起放大
sources:
  - Udo Zölzer, DAFX.
  - Julius O. Smith, Physical Audio Signal Processing, nonlinear distortion sections.
updated: 2026-10-28
---

::: zh
## 为什么会用到它

失真、过载、模糊是同一类非线性的三种程度。它们改变的不只是「脏」，还有谐波结构、动态和频响。

## 背后的机制

信号超过器件的线性范围后被削平，削波产生新的谐波。对称削波以奇次谐波为主，听感硬；不对称削波加入偶次谐波，听感暖。过载的拐点较软，失真更硬，模糊把增益推到几乎方波。输入电平决定削波量，所以前级增益比 drive 旋钮更能改变结果。削波也会压缩动态，低频互调会让和弦变糊。

## 旋钮与耳朵

drive 从 3 dB 开始试，tone 控制削波后的高频；mix 保持 30–50% 可以保留原始瞬态。给贝斯加失真时先高通到 100 Hz 以下，避免低频互调。人声少量失真会增加存在感，过量会咬住齿音。

## 耳朵要抓的点

在持续的风琴和弦上听削波如何把音头压平；换到失真吉他，注意五度和弦的低频是否出现新的嗡声。把 mix 从 100% 降到 40%，原始拨弦的颗粒会回来。

```audiolab
{"type":"instrument","gm":"Distortion Guitar","synth":"plucked","phrase":["E2","E2","B2","B2","G3","G3","D3"],"label":"失真吉他的五度和弦","label_en":"Power chords on a distorted guitar","hint":"先听干声的拨弦，再想象削波后多出来的谐波与压平的音头","hint_en":"Hear the dry pick, then picture added harmonics and a flattened attack"}
```

## 容易弄错的

以为失真只是变脏；以为数字失真一定不如模拟；以为 drive 越大越好。
:::

::: en
## Why reach for it

Distortion, overdrive and fuzz are three degrees of the same nonlinear family. They change harmonic structure, dynamics and frequency response, not just how dirty the sound seems.

## The mechanism

Once a signal exceeds the linear range, it is clipped, and clipping creates new harmonics. Symmetrical clipping favours odd harmonics and sounds hard; asymmetrical clipping adds even harmonics and sounds warmer. Overdrive has a softer knee, distortion is harder, and fuzz pushes gain toward a square wave. Input level sets the amount of clipping, so pre-gain matters more than the drive control alone. Clipping also compresses dynamics, and low-frequency intermodulation turns chords muddy.

## Knobs and ears

Start with about 3 dB of drive, use tone to shape the clipped high end, and keep mix at 30 to 50 percent to retain the original transient. Before distorting a bass, high-pass it below 100 Hz to avoid low intermodulation. A little distortion on a voice adds presence; too much grabs the sibilants.

## What the ear should catch

On a sustained organ chord, hear how clipping flattens the attack. On a distorted guitar, listen for a new hum under fifth chords. Pull mix from 100 to 40 percent and the grain of the original pick returns.

```audiolab
{"type": "instrument", "gm": "Distortion Guitar", "synth": "plucked", "phrase": ["E2", "E2", "B2", "B2", "G3", "G3", "D3"], "label": "Power chords on a distorted guitar", "label_en": "Power chords on a distorted guitar", "hint": "先听干声的拨弦，再想象削波后多出来的谐波与压平的音头", "hint_en": "Hear the dry pick, then picture added harmonics and a flattened attack"}
```

## Easy to get wrong

That distortion only makes a sound dirty; that digital distortion must sound worse than analog; that more drive is always better.
:::
