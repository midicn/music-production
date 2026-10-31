---
id: fixed-point-and-float
site: prod
cat: B5
title: 定点与浮点
title_en: Fixed Point and Floating Point
summary: 定点有硬顶，浮点有余量，混音决策由此而来。
summary_en: Fixed point has a hard ceiling, floating point has room to spare, and that shapes every mixing decision.
level: standard
tags: [浮点, 定点, 余量, 削波]
tags_en: [floating point, fixed point, headroom, clipping]
alias: [定点, 浮点, 32 位浮点, fixed point, floating point]
links:
  - "[[glossary:headroom]]"
  - "[[glossary:clipping]]"
  - "[[glossary:bit-depth]]"
instances:
  - pdmx-000435 | 贝多芬第九的乐谱声部极多，叠加后的峰值最能说明定点与浮点的余量差（C1）
  - oga-000001 | 游戏管弦编曲轨数多、音色杂，总线求和的余量不足就会削波（C1）
  - musicnet-000067 | 四重奏四个声部同时强奏，密集和声处的峰值为浮点留出余量（C1）
sources:
  - 浮点与定点音频通路的差异——依据来自DAW 厂商公开文档。
  - Pohlmann, Principles of Digital Audio, DSP chapters — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

同一段声音可以用整数或浮点表示。前者在满刻度处硬性截断，后者把小数点挪来挪去，混音留多少余量由此决定。

## 原理

定点数的小数点位置固定，24 位整数超出满刻度就再无处可去，多轨相加越过 0 dBFS 便被削平。浮点用指数记录数量级，32 位浮点的动态范围远超听觉上限，通路内部可以暂时超过 0 dBFS 而不失真，只在送到定点设备时才需回到范围内。浮点并非无限，极大增益与反复处理仍会累积误差。

## 参数与做法

混音总线保持 32 位浮点，进 DAC 或导出整数文件前留 3 到 6 dB 余量并限幅。不要因为浮点有余量就纵容每轨过响，插件之间仍按增益结构安排。导出后回放确认峰值。

## 听什么

在贝多芬第九的乐谱上听多声部齐奏，在游戏管弦编曲里听密集配器，在四重奏的强奏和弦里听四个声部叠加。把总线推过 0 dBFS 再拉回，浮点下听不出异样，导出 16 位后削波就会现形。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C3","G3","C4","E4","G4"],"label":"多声部叠加","label_en":"Voices stacked together","hint":"想象十条这样的声部同时进来，总线还剩下多少余量","hint_en":"Imagine ten such parts at once, then ask how much headroom the bus has left"}
```

## 常见误解

浮点可以随便超 0 dBFS，最终仍要落到有上限的设备。浮点也不是没有噪声，只是噪声底极低。定点不等于低音质，24 位足够完成大部分录音。32 位浮点文件不会让原始录音多出信息。
:::

::: en
## The question

A sample can be an integer or a float. The first clips at full scale, the second shifts the decimal point, and the difference sets the headroom a mix needs.

## How it works

Fixed point holds the decimal point in place, so a 24-bit integer has no room past full scale and summed tracks that cross 0 dBFS flatten. Float stores an exponent, so 32-bit float spans far beyond the ear and a path can pass 0 dBFS undistorted. Only the trip to a fixed-point device needs a return to range. Huge gains still accumulate error.

## Settings and practice

Keep the mix bus at 32-bit float, leave 3 to 6 dB before the DAC or an integer export, and limit there. Do not let float headroom excuse hot tracks.

## What to listen for

On the Beethoven Ninth score, hear many parts at once. In a quartet's loud chord, hear four voices stack. Push the bus past 0 dBFS and pull back: float hides it, a 16-bit export does not.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C3", "G3", "C4", "E4", "G4"], "label": "Voices stacked together", "label_en": "Voices stacked together", "hint": "想象十条这样的声部同时进来，总线还剩下多少余量", "hint_en": "Imagine ten such parts at once, then ask how much headroom the bus has left"}
```

## Common misconceptions

Float does not allow endless overs, because playback ends at a ceiling. It is not noise-free, only very quiet. Fixed point is not low fidelity, since 24 bit covers most recording. A 32-bit float file adds no detail the source lacked.
:::
