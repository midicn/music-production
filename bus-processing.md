---
id: bus-processing
site: prod
cat: A6
title: 总线的处理
title_en: Bus Processing
summary: 总线只做全局粘合与控峰，单轨的问题要回到单轨解决。
summary_en: The bus glues and controls peaks; problems belonging to one track must go back to that track.
level: standard
tags: [混音, 总线, 压缩, 粘合]
tags_en: [mixing, bus, compression, glue]
alias: [总线处理, 总线压缩, bus processing]
links:
  - "[[glossary:bus]]"
  - "[[glossary:compressor]]"
  - "[[glossary:eq]]"
  - "[[instrument:drum-kit]]"
instances:
  - oga-000011 | 密集游戏配乐的声部参照，尚未施加总线压缩（C1） | Dense game-music parts without bus compression (C1)
  - musicnet-000019 | 赋格声部参照，总线EQ效果需要另做处理对照（C1） | Fugal-part reference; bus-EQ effects require a separate processing comparison (C1)
  - groove-000010 | 鼓组长循环的源素材，不包含总线处理前后版本（C1） | A source drum loop without before-and-after bus processing (C1)
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook, mix bus processing.
  - David Gibson, The Art of Mixing, subgroup and master bus strategy.
updated: 2026-11-02
---

::: zh
## 问题

总线把多个信号汇到共同路径，可用于分组平衡、共享效果或整体动态处理。是否从混音开始就带着总线压缩工作，是工作方式选择；关键是知道它改变了什么，并保留足够余量。

## 目标与判断

先确认进入总线的是哪些轨道、返回信号是否会被再次处理，再匹配处理与旁通的响度。若单个过响声部一直触发全组衰减，可先调整该声部、检测滤波或编配。衰减量是否合适由目标与素材决定，不以超过某个dB数就判错。

## 做法

把组内平衡做稳后，一次只改一个总线参数。听启动时间是否保留所需音头，释放是否在下一次重拍前恢复，EQ是否改动了不想改的声部。记录输出补偿；想要密度、控峰或明显泵动时，会需要不同设置。

## 听什么

在同一小节的全组音频上比较，先看重音、低频与主线的关系，再听安静段是否被带起。不要把单音示例的音色变化当作整个总线的检测行为。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","G4","E4","B4"],"label":"多音高音色参照","label_en":"Multi-pitch timbre reference","hint":"这里没有总线处理器。将同一组轨道送入总线后，才可比较压缩、均衡和旁通结果。","hint_en":"There is no bus processor in this block. Route the same tracks through a bus to compare compression, EQ and bypass."}
```

## 常见误解

总线处理既可影响峰值，也可影响响度和音色。分组数量不代表制作水平；每多一条路由，都应能说明它的用途并检查没有非预期反馈。
:::

::: en
## The problem

A bus combines signals for group balance, shared effects or collective dynamic processing. Mixing into a bus compressor from the start is a workflow choice; understand what it changes and retain sufficient headroom.

## Goal and judgement

Confirm which tracks feed the bus and whether returns are processed again, then loudness-match bypass and active paths. If one loud part constantly ducks the group, adjust that part, detector filtering or arrangement. Suitable gain reduction depends on the aim and material rather than a universal dB limit.

## Method

After stabilising group balance, change one bus parameter at a time. Check attack retention, recovery before the next accent and whether EQ alters unintended parts. Log output compensation: density, peak control and deliberate pumping need different settings.

## What to listen for

Compare the same bar of grouped audio, examining accents, bass and the lead, then whether quiet passages are lifted. A timbre change in a single-note example does not establish the detector behaviour of the full bus.

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","G4","E4","B4"],"label":"Multi-pitch timbre reference","label_en":"Multi-pitch timbre reference","hint":"There is no bus processor in this block. Route the same tracks through a bus to compare compression, EQ and bypass.","hint_en":"There is no bus processor in this block. Route the same tracks through a bus to compare compression, EQ and bypass."}
```

## Common misconceptions

Bus processing can affect peaks, loudness and timbre. Group count does not measure production skill; each added route should have a purpose and no unintended feedback.
:::
