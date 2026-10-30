---
id: kick-and-bass
site: prod
cat: A6
title: 底鼓与贝斯
title_en: Kick and Bass
summary: 一个管瞬态一个管持续，低频要让位而不是互相加音量。
summary_en: One owns the transient, the other sustain, so low end needs room rather than more level.
level: standard
tags: [混音, 低频, 底鼓, 贝斯]
tags_en: [mixing, low-end, kick, bass]
alias: [底鼓, 贝斯, 低频冲突, kick, bass]
links:
  - "[[glossary:eq]]"
  - "[[glossary:sidechain]]"
  - "[[glossary:compressor]]"
  - "[[instrument:drum-kit]]"
instances:
  - oga-000002 | 游戏配乐里鼓与合成贝斯同时出现，低频掩蔽最直接
  - groove-001103 | 四拍迪斯科鼓，底鼓落点稳定，适合先定基频
  - pdmx-000450 | 合唱低音声部下探很低，可与底鼓对照让位
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook, low-end chapter — background checked, not quoted
  - Huber and Runstein, Modern Recording Techniques, rhythm section mixing — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

底鼓与贝斯抢同一段低频，谁都不想退。结果是低频很响，却没有冲击力，音高也含糊，鼓与贝斯都失去轮廓。

## 目标与判断

底鼓负责瞬态与点击，贝斯负责持续与音高。先决定谁承担最低那一层，再谈处理。判断时先找两者的基频是否重叠；重叠不可怕，持续掩蔽才可怕。若贝斯在底鼓每次出现时都听不见，它需要让位，而不是加音量。

## 做法

先定底鼓的基频，再让贝斯在该频点做两到三分贝的窄衰减；或用侧链压缩让贝斯短时后退。底鼓尾巴过长时，先缩短包络，不要靠均衡硬切。贝斯的高频谐波要保留，帮助小音箱听见旋律。每次改完都回到整段，确认冲击力而不是只看低频表。

## 听什么

听底鼓的点击是否每次都穿出来；听贝斯的音高是否稳定；在小音量与手机上听两者是否还在。

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E1","E1","G1","A1"],"label":"贝斯短句","label_en":"Bass figure","hint":"先听音高与尾巴，再与底鼓交替","hint_en":"Hear the pitch and tail, then alternate with the kick"}
```

## 常见误解

以为低频越多越有力量；以为侧链一定比均衡好；以为底鼓和贝斯必须完全分开。
:::

::: en
## The problem

Kick and bass fight over the same low band, and neither wants to move. The result is loud low end with no impact and an unclear pitch.

## Goal and judgement

The kick owns the transient and click; the bass owns sustain and pitch. Check whether their fundamentals overlap. Overlap is not the problem; constant masking is. If the bass disappears every time the kick hits, it needs room, not more level.

## Method

Find the kick fundamental, then cut the bass 2 to 3 dB at that point with a narrow bell. Alternatively, sidechain the bass so it steps back briefly. If the kick tail is too long, shorten its envelope instead of cutting with EQ. Keep some bass harmonics so small speakers can hear the line. Return to the full section after each change and judge impact, not just the low-frequency meter.

## What to listen for

Whether the kick click comes through every time; whether the bass pitch stays stable; whether both survive on a phone speaker at low volume.

```audiolab
{"type": "instrument", "gm": "Electric Bass (finger)", "synth": "plucked", "phrase": ["E1", "E1", "G1", "A1"], "label": "Bass figure", "label_en": "Bass figure", "hint": "先听音高与尾巴，再与底鼓交替", "hint_en": "Hear the pitch and tail, then alternate with the kick"}
```

## Common misconceptions

That more low end means more power; that sidechain always beats EQ; that kick and bass must occupy completely separate bands.
:::
