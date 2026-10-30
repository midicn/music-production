---
id: key-and-velocity-zones
site: prod
cat: B4
title: 采样映射
title_en: Key and Velocity Zones
summary: 键区与力度区把演奏切成格子，格线两侧的音色要接得上。
summary_en: Key and velocity zones cut performance into cells, and the sound must join across each border.
level: standard
tags: [采样映射, 键区, 力度区]
tags_en: [sample mapping, key zones, velocity zones]
alias: [采样映射, 键区, 力度区, key zone]
links:
  - "[[glossary:pitch]]"
  - "[[glossary:velocity]]"
  - "[[instrument:samplers]]"
instances:
  - atepp-005536 | 《侏儒》在极低与极高音区之间跳跃，键区分界点很容易听出来
  - pdmx-002097 | 《野蜂飞舞》高速经过高音区，键区接缝会被快速音群放大
  - pdmx-000183 | 《安魂曲》从低音声部到高音独唱，跨度覆盖多个键区
sources:
  - Curtis Roads, The Computer Music Tutorial — 键区与力度区的映射做法核对，未抄原文
  - MIDI Association, General MIDI 1 Sound Set — 鼓组键位范围核对，未抄原文
updated: 2026-10-28
---

::: zh
## 问题

一个采样器里几十个样本，按键时它怎么知道该用哪一个？

## 原理

采样映射把键盘与力度切成网格，每个格子指向一个样本。键区负责音高，力度区负责演奏强度，两者交叉形成二维表。映射的边界叫分界点，分界点两侧若来自不同录音，音色会有细微跳变。设计时让分界点落在使用较少的音上，并让相邻样本的音区略有重叠，切换时用交叉淡化或力度渐变。鼓组是另一套映射，每个键对应一个独立样本，不再按音高变调。映射表还记录调音、声像与输出通道。

## 做法与参数

钢琴类每八度一个键区，分界点避开常用音。贝斯与吉他可以更密，因为低音区变调感更明显。力度分界常放在 64 与 96 附近，避开演奏最常停留的中间值。鼓组按 GM 鼓映射排键，保留 35 到 81 的标准位置。检查映射时从最低音到最高音弹半音阶，听有没有突然变薄的音。

## 听什么

听跨分界点的半音，注意音色是否从厚变薄。听同一音的高力度与低力度，判断是换了样本还是只改了音量。听鼓组每个键，确认键位与音色对得上。听极端音区，确认最高与最低的样本没有超出录制范围。

## 常见误解

以为一个样本可以覆盖整个键盘；以为分界点越多越好；以为鼓组也按音高变调。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["A1","A2","A3","A4","A5","A6"],"label":"从最低到最高","label_en":"Lowest to highest","hint":"听这串跨音区的音，注意音色在哪一段变薄，那通常就是键区分界的位置","hint_en":"Hear this run across registers; where the colour thins is usually a key-zone split"}
```
:::

::: en
## The problem

With dozens of samples inside a sampler, how does a keypress know which to use?

## How it works

Mapping cuts the keyboard and velocity range into a grid, and each cell points to a sample. Key zones handle pitch, velocity zones handle playing strength, and together they form a two-dimensional table. Boundaries are split points; if the two sides come from different recordings, the colour shifts. Designers place splits on less-used notes and let neighbouring zones overlap, smoothing the switch with a crossfade or velocity fade. Drum kits use another map, where each key is an independent sample and transposition stops. The map stores tuning, pan and output routing.

## Practice and settings

Pianos usually take one key zone per octave, with splits away from common notes. Basses and guitars can be denser; transposition is more audible low down. Velocity splits often sit near 64 and 96, away from values players hold. Drum kits follow the GM map and keep standard 35 to 81 positions. To check a map, play a chromatic scale from bottom to top and listen for a thin spot.

## What to listen for

Hear semitones across a split and notice whether the tone thins. Hear one note at high and low velocity; did the sample change or only the level? Hear every drum key and confirm the match. Hear the extremes and confirm both samples stay inside their recorded range.

## Common misconceptions

That one sample covers the keyboard; that more splits are better; that drum kits are transposed by pitch.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["A1", "A2", "A3", "A4", "A5", "A6"], "label": "Lowest to highest", "label_en": "Lowest to highest", "hint": "Hear this run across registers; where the colour thins is usually a key-zone split", "hint_en": "Hear this run across registers; where the colour thins is usually a key-zone split"}
```
:::
