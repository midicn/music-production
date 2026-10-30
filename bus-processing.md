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
  - oga-000011 | 游戏首领段层次密，适合听总线压缩是否把攻击压平（C1）
  - musicnet-000019 | 巴赫赋格声部交织，总线均衡一动就能听出声部变化（C1）
  - groove-000010 | 放克鼓组长循环，适合对照鼓总线压缩前后的紧度（C1）
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook, mix bus processing — background checked, not quoted
  - David Gibson, The Art of Mixing, subgroup and master bus strategy — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

有人在混音一开始就把压缩器与限制器挂在总线上，边混边压，鼓的瞬态被提前削掉，单轨怎么推都回不来。也有人把所有频段问题留到总线均衡，一推就把整体音色带歪。

## 目标与判断

总线负责全局粘合、控峰与轻微的色调统一，不负责修复单轨。判断时先旁通，比较接通前后：瞬态是否更整齐，低频是否更稳，声部是否还分得开。若某一轨的问题在总线上被放大，说明它该回单轨处理。增益衰减一到三 dB 足够，超过就要怀疑前面。

## 做法

先按鼓、贝斯、人声、乐器分组，把组内的平衡与频段处理好。总线压缩用二比一、慢启动、自动释放，只做一到二 dB；总线均衡只做零点五到一 dB 的宽幅调整。保持增益结构，接通后响度略增时用输出补偿，避免靠响度判断好坏。

## 听什么

听旁通瞬间鼓的起音是否更活，低频是否更松，人声是否还在原位。下面四个音先听整体，再想总线压缩会先抓到哪一个。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","G4","E4","B4"],"label":"总线先抓到谁","label_en":"What the bus grabs first","hint":"听四个音依次响时的重心，再想象慢启动压缩放过起音","hint_en":"Hear the center of the four-note phrase, then picture slow attack letting onsets through"}
```

## 常见误解

以为总线压缩能让混音变响；以为总线均衡能修单轨；以为总线越多越专业。
:::

::: en
## The problem

Some engineers put a compressor and limiter on the mix bus from the first fader move. Drum transients are shaved off before the mix exists, and no amount of track-level work brings them back. Others leave every frequency problem for the bus EQ and tilt the whole sound with one move.

## Goal and judgement

The bus provides global glue, peak control and slight tonal unity. It does not repair single tracks. Bypass it and compare: are transients more even, is the low end steadier, do the parts still separate? If one track's problem worsens through the bus, fix it on that track. One to three dB of gain reduction is enough; more suggests something earlier is wrong.

## Method

Group drums, bass, vocal and instruments, and solve balance and frequency inside each group first. Set bus compression near two to one with a slow attack and auto release, reducing only one to two dB. Use bus EQ for broad moves of half a dB to one dB. Preserve gain structure, and compensate output when the engaged bus adds level so loudness does not make the decision.

## What to listen for

Hear whether drum attacks come alive when the bus is bypassed, whether the low end relaxes, and whether the vocal stays in place. The four notes sound in turn; hear the whole, then picture what it grabs first.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C4", "G4", "E4", "B4"], "label": "What the bus grabs first", "label_en": "What the bus grabs first", "hint": "听四个音依次响时的重心，再想象慢启动压缩放过起音", "hint_en": "Hear the center of the four-note phrase, then picture slow attack letting onsets through"}
```

## Common misconceptions

That bus compression makes a mix loud; that bus EQ can fix a single track; that more bus processing sounds more professional.
:::
