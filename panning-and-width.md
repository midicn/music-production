---
id: panning-and-width
site: prod
cat: A6
title: 声像与宽度
title_en: Panning and Stereo Width
summary: 宽度来自声部差异与稳定的中心，而不是把乐器推到两边。
summary_en: Width comes from differences between parts and a steady centre, not from hard panning.
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
  - oga-000004 | 管弦与打击分层明显，声像铺开后各层位置可辨
  - pdmx-000087 | 钢琴织体宽，左右拉得太开会与低音争夺中心
  - openscore-000018 | 声乐线加钢琴，主奏必须留在中心
sources:
  - David Gibson, The Art of Mixing, stereo field chapter — background checked, not quoted
  - Huber and Runstein, Modern Recording Techniques, panning and monitoring — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

声像不是把乐器随便分到左右。宽度来自声部之间的差异，也来自中心是否稳。中心一塌，再宽也像纸片。宽度是结果，不是起点。

## 目标与判断

低频与主唱留在中心；中频声部错开；高频装饰可以更靠边。判断时先单声道听，中心不塌再展宽。若一条轨推到极左后，另一边出现空洞，说明编曲缺对位，而不是声像没拉开。

## 做法

先摆骨架，底鼓、贝斯与主唱在中心；军鼓稍偏或居中；和弦与打击乐按两成到六成的幅度错开；立体声采样保持原位。用哈斯延迟或双轨展宽时，先检查单声道折叠是否变薄。声像自动化只在段落变化时用。每推一步都回到中心听一次，避免越拉越远。

## 听什么

听左右切换时主唱是否移动；听极左极右是否有孤立元素；按单声道，听军鼓与和弦是否互相抵消。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","G4","E4","G4"],"label":"弦乐铺开","label_en":"String spread","hint":"先听中心，再把声部向两侧展开","hint_en":"Hear the centre first, then spread the parts outward"}
```

## 常见误解

以为越宽越好；以为每件乐器都要有独立位置；以为单声道检查只适合老歌。
:::

::: en
## The problem

Panning is not distributing instruments left and right at random. Width comes from differences between parts, and from a centre that holds. If the centre collapses, more width only sounds thinner. Width is a result, not a starting point.

## Goal and judgement

Keep low end and lead vocal centred. Separate midrange parts. Let bright ornaments sit wider. Check in mono before widening. If a hard-left track leaves a hole on the right, the arrangement lacks a counterpart, not panning.

## Method

Place the skeleton first: kick, bass and lead in the centre, snare near centre or slightly off, chords and percussion spread between 20 and 60 percent, stereo samples left where they are. When using Haas delay or doubled takes, check the mono fold-down for thinning. Automate pan only when the section changes. Return to the centre after each move so the image does not drift.

## What to listen for

Whether the lead moves when you switch sides; whether hard-panned elements sound isolated; whether snare and chords cancel in mono.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C4", "G4", "E4", "G4"], "label": "String spread", "label_en": "String spread", "hint": "先听中心，再把声部向两侧展开", "hint_en": "Hear the centre first, then spread the parts outward"}
```

## Common misconceptions

That wider is better; that every instrument needs its own position; that mono checks belong only to old records.
:::
