---
id: quantize
site: prod
cat: B2
title: 量化
title_en: Quantise
summary: 把演奏的音头吸到网格上，用强度决定吸多少。
summary_en: Pulls performed attacks onto a grid, with strength deciding how far each note moves.
level: standard
tags: [音序, 量化, 节奏, 网格]
tags_en: [sequencing, quantise, rhythm, grid]
alias: [量化, 对齐网格, 音符吸附, quantize, quantise, quantization]
links:
  - "[[glossary:tempo]]"
  - "[[glossary:velocity]]"
  - "[[instrument:sequencer]]"
instances:
  - groove-000664 | 新奥尔良第二线鼓型，节奏骨架清楚，适合对照网格
  - atepp-000195 | 月光的速度自由起伏，量化会削掉呼吸
  - groove-000725 | 嘻哈鼓循环，踩镲的微差最容易被听出
sources:
  - 量化的网格分辨率与强度混合，依通行音序软件说明核查，未抄文本
  - 音频切片量化的边界处理，依数字音频工作流通识核查，未抄文本
updated: 2026-10-28
---

::: zh
量化把音头吸到最近的网格线上，强度决定吸过去多少。

## 问题

演奏的音头总会偏离节拍，偏得整齐是律动，偏得零散是拖沓。量化要解决后者，而不是把所有偏差抹平。

## 原理

引擎读每个音的起点，找最近的网格点，再按强度在原点与格点之间取中间值。网格可以是十六分、八分三连或摇摆格；音符终点与力度默认不动。音频的量化要先切片，再移动切片边界。

## 做法与参数

先选能容纳最短音值的网格，宁可粗一点；强度从一半开始试，听不出改善再提高；只量化音头，保留尾音；三连音材料不要用直网格；鼓组保留人性的微差，贝斯与和弦可以更贴格。

## 听什么

听音头是否一齐，以及重音有没有被吸走。踩镲与底鼓的关系最能暴露过度量化，军鼓稍微靠后常更有推力。

## 常见误解

量化不能修复写错的音符，也不能自动产生律动。百分之百贴格不是标准答案，很多时候一半强度更自然。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"e e e e e e e e","bpm":100,"label":"八分音符的网格","label_en":"An eighth-note grid","hint":"听每一拍被切成两半","hint_en":"Hear each beat split in two"}
```
:::

::: en
Quantise pulls each attack to the nearest grid line, and strength decides how far it travels.

## The problem

Attacks always sit off the beat; an even offset is groove, a scattered one is drag. Quantise fixes the second, not every deviation.

## How it works

The engine reads each note start, finds the nearest grid point, and blends between origin and grid by strength. The grid can be a sixteenth, an eighth triplet or a swing grid; note ends and velocity stay put by default. Audio is sliced first, and then slice edges move.

## Settings and practice

Choose the coarsest grid that still holds the shortest value, start strength at half and raise it only if the result is unclear. Quantise onsets and keep tails, never put triplets on a straight grid, and leave drum micro-timing while bass and chords can sit tighter.

## What to listen for

Hear whether attacks lock and whether accents are pulled away. The hat-to-kick relation exposes over-quantising, while a slightly late snare adds push.

## Common misunderstandings

Quantise cannot fix wrong notes or create groove. Full snapping is not the goal, and half strength is often more natural.

```audiolab
{"type": "rhythm", "sig": "4/4", "pattern": "e e e e e e e e", "bpm": 100, "label": "An eighth-note grid", "label_en": "An eighth-note grid", "hint": "听每一拍被切成两半", "hint_en": "Hear each beat split in two"}
```
:::
