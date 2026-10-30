---
id: mixing-vs-mastering
site: prod
cat: A8
title: 母带与混音的分工
title_en: Mixing versus Mastering
summary: 混音决定作品内部，母带决定作品与外界之间的最后一道关口。
summary_en: Mixing builds the internal balance, while mastering makes the finished record translate to the outside world without changing its intent.
level: standard
tags: [母带, 混音, 分工]
tags_en: [mastering, mixing, workflow]
alias: [混音与母带, 母带分工, mixing and mastering]
links:
  - "[[glossary:limiter]]"
  - "[[glossary:maximizer]]"
  - "[[glossary:lufs]]"
instances:
  - pdmx-000435 | 贝多芬第九的合唱与乐队层次，适合判断混音平衡是否已经完成
  - musicnet-000236 | 勃拉姆斯钢琴四重奏的声部交织，能听出母带是否破坏内部比例
  - oga-000004 | 短小的游戏战斗循环，适合练习混音交付与母带处理的边界
sources:
  - 混音交母带的余量、采样率与是否含总线处理的惯例，依后期制作通识核查，未抄文本
  - 母带只做全局判断而不重混的原则，依母带工程教材通识核查，未抄文本
updated: 2026-10-28
---

::: zh
混音与母带是两道不同的工序。混音决定作品内部怎么组织，母带决定它作为成品如何面对外界。

## 问题

有人把限制器挂在混音总线上，边混边压，结果鼓的瞬态没了，人声也前后不定。也有人把频段冲突与混乱声场留到母带，指望最后一步自动变好。

## 目标与标准

混音解决平衡、空间与情绪，单件乐器的取舍都在这里完成。母带解决整体响度、音色一致性与交付规格。交给母带的混音通常留 4 到 6 dB 峰值余量，不挂最终限制器，也不做位深抖动，并写清总线处理。

## 做法

混音阶段处理频率冲突、动态和声像，导出与工程同采样率、24 bit 的版本。母带阶段只做全局微调，遇到单件乐器的问题就回混音。双方共用一首参考曲与一份说明，避免各听各的。

## 听什么

对比混音版与母带版，听人声位置、低频紧度和鼓的起音。若人声后退、鼓变扁，说明处理越界了。下面这段弦乐可以听声部是否仍然分得开。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","G4","E4","C5"],"label":"声部是否还分得开","label_en":"Do the parts still separate","hint":"先听四个音各自的轮廓，再想母带压缩会不会把它们糊成一块","hint_en":"Hear each note's outline, then ask whether master compression would smear them together"}
```

## 常见误解

母带师不会替你重混，也不该靠母带修单轨。混音阶段先上最大化器并不省事，只会让后面失去判断空间。混音够响也不等于母带合格。
:::

::: en
Mixing and mastering are separate stages. The mix builds the record inside; mastering makes it meet the outside world.

## The problem

Some engineers put a limiter on the mix bus and compress while balancing, until transients vanish and the vocal drifts. Others leave frequency clashes and a vague image for mastering.

## Goals and standards

A mix aims at balance, space and emotion, and every individual choice belongs there. Mastering aims at overall loudness, tonal consistency and delivery specs. A mix for mastering usually leaves 4 to 6 dB of headroom, with no final limiter or dither, and a note on bus processing.

## Practice

Solve clashes, dynamics and panning in the mix, and export at the session rate and 24 bit. In mastering, make global changes only; if one instrument is wrong, return to the mix. Share one reference and one brief.

## What to listen for

Compare the mix and master for vocal position, low-end tightness and drum attack. If the vocal moves back or drums flatten, processing has overstepped.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C4", "G4", "E4", "C5"], "label": "Do the parts still separate", "label_en": "Do the parts still separate", "hint": "先听四个音各自的轮廓，再想母带压缩会不会把它们糊成一块", "hint_en": "Hear each note's outline, then ask whether master compression would smear them together"}
```

## Common misunderstandings

A mastering engineer will not remix for you, and mastering should not repair one track. A maximizer on the mix bus early removes room to judge later. A loud mix is not a finished master.
:::
