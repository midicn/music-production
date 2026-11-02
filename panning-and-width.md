---
id: panning-and-width
site: prod
cat: A6
title: 声像与宽度
title_en: Panning and Stereo Width
summary: 用声像、左右差异和中心层次安排宽度，同时检查单声道兼容性。
summary_en: Arrange width through panning, left/right differences and centre balance, while checking mono compatibility.
level: standard
tags: [混音, 声像, 宽度, 单声道]
tags_en: [mixing, panning, width, mono]
alias: [声像, 立体声宽度, 展宽, panning, stereo width]
links:
  - "[[glossary:bus]]"
  - "[[instrument:piano]]"
  - "[[instrument:drum-kit]]"
  - "[[period:classical]]"
instances:
  - oga-000004 | 可在 DAW 将管弦与打击分组，比较居中与左右声像布局 | Group orchestral and percussion parts in a DAW to compare centred and left/right layouts
  - pdmx-000087 | 可渲染后调整钢琴声像与宽度，比较单声道求和及低音定位 | Render and adjust piano position and width, checking mono summation and bass location
  - openscore-000018 | 可尝试人声居中、钢琴不同宽度的布局，按作品意图决定位置 | Try a centred vocal with different piano widths, choosing positions for the piece
sources:
  - David Gibson, The Art of Mixing, stereo field chapter.
  - Huber and Runstein, Modern Recording Techniques, panning and monitoring.
updated: 2026-11-02
---

::: zh
## 问题

声像主要描述声音在左右的位置，宽度描述它占据的横向范围。单声道乐器可被放在一侧而仍很窄；左右存在不同演奏、音色或反射时，整体可能变宽。先确定主线位置，再安排其他声部与它的关系。

## 目标与判断

先确定主线与低频的稳定位置，再安排其他声部。底鼓、贝斯和主唱居中是常见做法，不是所有编制的硬规则。某一侧留白可能是有意设计，也可能需要调整电平或配器，不能仅由“有空洞”断言缺少对位。

## 做法

一次移动一条声部，检查与主线的关系并补偿平移律造成的电平差。真实双轨、立体声音源和延迟复制产生的宽度不同；用短延迟展宽时要听单声道求和与定位是否漂移。自动化按段落目标设置，不必限定只在某一位置或固定百分比移动。

## 听什么

听左右切换时主唱是否移动；听极左极右是否有孤立元素；按单声道，听军鼓与和弦是否互相抵消。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","G4","E4","G4"],"label":"声像练习的弦乐短句","label_en":"A string phrase for panning practice","hint":"先在 DAW 录下短句，再用声像控制比较居中与偏侧；匹配增益，避免把变响误认为变宽。","hint_en":"Record the phrase in a DAW, then compare centre and side positions with pan controls. Match gain so a level change is not mistaken for width."}
```

## 常见误解

以为越宽越好；以为每件乐器都要有独立位置；以为单声道检查只适合老歌。
:::

::: en
## The problem

Panning mainly describes left/right position; width describes the horizontal extent occupied. A mono instrument can sit to one side while remaining narrow. Different performances, timbres or reflections on the two sides can create width. Choose the main line’s position, then arrange other parts around that relationship.

## Goal and judgement

Establish stable positions for the lead and bass before other parts. Centred kick, bass and vocal are common choices, not universal rules. Space on one side can be intentional or require level or arrangement changes; it does not by itself diagnose missing counterpoint.

## Method

Move one part at a time and compensate level changes from the pan law while checking the lead. True double-tracking, stereo sources and delayed copies create different width. For short-delay widening, check mono summation and localisation. Automate for sectional goals rather than prescribed positions or percentages.

## What to listen for

Whether the lead moves when you switch sides; whether hard-panned elements sound isolated; whether snare and chords cancel in mono.

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","G4","E4","G4"],"label":"A string phrase for panning practice","label_en":"A string phrase for panning practice","hint":"Record the phrase in a DAW, then compare centre and side positions with pan controls. Match gain so a level change is not mistaken for width.","hint_en":"Record the phrase in a DAW, then compare centre and side positions with pan controls. Match gain so a level change is not mistaken for width."}
```

## Common misconceptions

That wider is better; that every instrument needs its own position; that mono checks belong only to old records.
:::
