---
id: depth-and-layering
site: prod
cat: A6
title: 前后层次
title_en: Front-to-Back Depth
summary: 远近由电平、频段、瞬态与混响共同决定，不只靠音量。
summary_en: Distance comes from level, spectrum, transients and reverb together, not level alone.
level: standard
tags: [混音, 层次, 深度, 混响]
tags_en: [mixing, depth, layering, reverb]
alias: [前后层次, 深度, 远近, depth, layering]
links:
  - "[[glossary:reverb]]"
  - "[[glossary:delay]]"
  - "[[instrument:drum-kit]]"
  - "[[period:romantic]]"
instances:
  - pdmx-000450 | 合唱、独唱与乐队并存，远近层次本来就有
  - oga-000002 | 游戏场景元素多，干湿差异大，层次容易糊
  - groove-000007 | 慢速摇滚鼓，近场敲击与房间感的差别容易听
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook, depth and reverb chapter — background checked, not quoted
  - David Gibson, The Art of Mixing, front-to-back perspective — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

所有轨都贴在同一平面，音量再准也会挤。远近不是玄学，它由电平、频段、瞬态与混响共同决定。

## 目标与判断

前景是主唱、主奏与底鼓；中景是节奏吉他与和弦；背景是铺底、氛围与尾音。判断标准是闭上眼能指出每个声部的大致距离，而不是每件都听得清。远不等于小声，近也不等于加高频。层次靠关系，不靠堆叠。

## 做法

先降背景轨的高频与瞬态，再给短混响；前景少混响、多干声。用预延迟把主唱与房间分开，用低切去掉远处声部的低频。避免每轨用不同混响，优先共享一两个空间。混响发送量按段落调整，副歌可以比主歌更湿。层次不够时，先删掉一件乐器，再考虑加效果。

## 听什么

听主歌进入副歌时背景是否后退；听主唱尾音是否被混响拖住；把混响全部旁通，检查层次是否只靠音量。

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["A3","C4","E4","D4"],"label":"远近对比","label_en":"Near and far","hint":"先听干声，再加混响听距离变化","hint_en":"Hear the dry sound, then add reverb and hear the distance change"}
```

## 常见误解

以为混响越大越远；以为远近只靠音量；以为每轨都该有独立空间。
:::

::: en
## The problem

When every track sits on the same plane, accurate levels still feel crowded. Distance is not mysterious. It comes from level, spectrum, transients and reverb together.

## Goal and judgement

Foreground is lead vocal, solo line and kick. Midground is rhythm guitar and chords. Background is pads, atmosphere and tails. The test: with eyes closed, you can point to roughly where each part sits, without needing to hear every detail. Far does not mean quiet; near does not mean brighter. Depth comes from relationships, not from stacking more parts.

## Method

Roll off highs and soften transients on background parts, then add a short reverb. Keep the foreground dry and close. Use pre-delay to separate the lead from the room, and high-pass distant parts. Avoid a different reverb on every track; share one or two spaces. Automate reverb sends by section; the chorus can be wetter than the verse. When depth is missing, remove an instrument before adding another effect.

## What to listen for

Whether the background steps back when the chorus arrives; whether reverb drags the vocal tail; whether the layers survive with all reverbs bypassed.

```audiolab
{"type": "instrument", "gm": "Choir Aahs", "synth": "vocal", "phrase": ["A3", "C4", "E4", "D4"], "label": "Near and far", "label_en": "Near and far", "hint": "先听干声，再加混响听距离变化", "hint_en": "Hear the dry sound, then add reverb and hear the distance change"}
```

## Common misconceptions

That more reverb means more distance; that distance is only level; that every track needs its own space.
:::
