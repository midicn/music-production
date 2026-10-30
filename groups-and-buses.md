---
id: groups-and-buses
site: prod
cat: A1
title: 编组与总线
title_en: Groups and Buses
summary: 把多条轨道汇到一条总线上统一处理，省插件也统一听感。
summary_en: Summing tracks into a bus, or tying their controls together, so a mix can be shaped in fewer, clearer moves.
level: standard
tags: [DAW, 编组, 总线, 混音]
tags_en: [DAW, group, bus, mixing]
alias: [编组, 总线, 分组, group, bus]
links:
  - "[[glossary:bus]]"
  - "[[glossary:compressor]]"
  - "[[glossary:sidechain]]"
instances:
  - pdmx-000368 | 《卡门》配器层次多，适合按弦乐、管乐与打击分总线
  - oga-000011 | 游戏头目曲分层明显，鼓组与合成器可各走一条总线
  - pdmx-000166 | 巴洛克协奏曲的独奏与合奏对比，适合练总线的整体处理
sources:
  - 编组、总线与发送的信号流，依通行调音台与 DAW 文档核查，未抄文本
  - 总线压缩、并联压缩与增益结构的用法，依混音教材核查，未抄文本
updated: 2026-10-28
---

::: zh
编组是把几条轨的控制绑在一起，总线是让几条轨的声音汇到一处。前者管动作，后者管信号。

## 问题

逐轨加压缩与均衡，容易让整体更挤，也难保持一致的听感。把鼓、人声或弦乐先汇到总线，再统一处理，既省插件，也让它们像一件事。

## 原理或做法

编组只影响控制，比如一起推音量、一起静音；总线真的把信号相加。总线可以串联，也可以并联。混响返回是另一种总线，所有发送都汇到那里。增益结构要先对，否则总线压缩只是在压一个已经过载的混合。

## 参数与判断

总线压缩要轻，表头动一到三 dB 就够。均衡用来看整体掩蔽，不要替单轨修问题。并联压缩保留瞬态。顺序通常是均衡、压缩、饱和，但要以听感为准。

## 听什么

鼓组总线压缩后，底鼓与贝斯会更贴；弦乐总线一压，齐奏的毛边会变整齐。短句演示是合奏音色，先听整体，再想它该不该被压。

```audiolab
{"type":"instrument","gm":"Brass Section","synth":"brass","phrase":["C4","F4","G4","C5"],"label":"一条铜管总线的材料","label_en":"Material for a brass bus","hint":"先听齐奏的毛边，再想象轻度压缩","hint_en":"Hear the unison edge, then imagine gentle compression"}
```

## 常见误解

总线不是越多越好，层级越深越难排查。总线压缩也救不了糟糕的平衡，它只会把问题压得更平。
:::

::: en
Grouping ties the controls of several tracks together; a bus sums their sound. The first manages actions, the second manages signal.

## The problem

Compressing and EQing every track separately makes the whole mix crowded and inconsistent. Summing drums, vocals or strings to a bus first lets you process them as one thing, saving plug-ins and keeping a common tone.

## How it works

A group affects control only, such as moving or muting tracks together; a bus actually adds the signals. Buses can run in series or parallel. A reverb return is another kind of bus, where all sends meet. Gain staging must be right first, or bus compression only squeezes an already overloaded sum.

## Settings and judgement

Keep bus compression light, with one to three dB of movement. Use EQ to see overall masking, not to fix single tracks. Parallel compression keeps transients. The usual order is EQ, compression, saturation, but trust your ears.

## What to listen for

A compressed drum bus makes kick and bass sit closer; a compressed string bus smooths the roughness of unison. The demo is an ensemble timbre, so hear the whole first, then ask whether it should be compressed.

```audiolab
{"type": "instrument", "gm": "Brass Section", "synth": "brass", "phrase": ["C4", "F4", "G4", "C5"], "label": "Material for a brass bus", "label_en": "Material for a brass bus", "hint": "先听齐奏的毛边，再想象轻度压缩", "hint_en": "Hear the unison edge, then imagine gentle compression"}
```

## Common misunderstandings

More buses is not more professional; deeper hierarchies are harder to troubleshoot. Bus compression cannot rescue a bad balance; it only flattens the problem.
:::
