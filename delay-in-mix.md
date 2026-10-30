---
id: delay-in-mix
site: prod
cat: A6
title: 延迟的用法
title_en: Using Delay in a Mix
summary: 延迟先对齐节奏，再谈空间；重复落在空隙里才有用。
summary_en: Delay locks to the rhythm before it creates space; its repeats only help when they land in the gaps.
level: standard
tags: [混音, 延迟, 节奏, 空间]
tags_en: [mixing, delay, rhythm, space]
alias: [延迟处理, 延时, delay use]
links:
  - "[[glossary:delay]]"
  - "[[glossary:reverb]]"
  - "[[instrument:acoustic-guitar]]"
  - "[[period:contemporary]]"
instances:
  - groove-000000 | 放克鼓组节奏清楚，适合判断延迟音符是否对齐（C1）
  - oga-000018 | 游戏城堡段结构清楚，重复容易听出是否落进空隙（C1）
  - openscore-000018 | 练声曲长句多，适合听延迟如何补住句尾（C1）
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook, delay and spatial effects — background checked, not quoted
  - David Gibson, The Art of Mixing, rhythmic delay placement — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

延迟一开，重复与底鼓错半拍，越听越乱；反馈加多后，中低频堆成一片；人声句尾被自己的重复盖住。问题通常不是延迟不好听，而是音符时值没有和歌曲对齐，滤波也没有做。

## 目标与判断

延迟首先是一个节奏工具，其次才是空间工具。判断时把延迟单独听，重复应落在主唱停顿或鼓的空隙里；若重复与歌词抢字，就换时值或缩短。宽度不是越多越好，单声道延迟也能把一个元素推到侧后方。干声始终优先。

## 做法

用发送而不用插入，方便统一控制。按歌曲速度选八分附点或四分音符，反馈从百分之十五到三十起试。给重复加三百赫兹高通与四千赫兹低通，让它退到后面。需要干净时加侧链衰减，让人声一开口延迟就让路。乒乓延迟只给一个元素用。

## 听什么

听重复是否落在拍点上，是否盖住下一个字，句尾是否自然消失。下面四个音先听原声，再想象每次重复落在哪里。

```audiolab
{"type":"instrument","gm":"Electric Guitar (clean)","synth":"plucked","phrase":["E4","B4","G4","D5"],"label":"重复落在空隙里","label_en":"Repeats that land in the gaps","hint":"听每个音之后的空位，再想八分附点会放在哪","hint_en":"Hear the space after each note and picture where a dotted eighth would sit"}
```

## 常见误解

以为延迟可以替代混响；以为反馈越多越宽；以为人声必须加延迟。
:::

::: en
## The problem

Turn on a delay and the repeats fall half a beat away from the kick, making the groove messier. More feedback piles up the low mids, and the vocal's own repeats cover the end of its phrases. The delay is rarely the problem; the note value is not locked to the song and repeats are unfiltered.

## Goal and judgement

Delay is a rhythmic tool first and a spatial tool second. Solo the effect and check that repeats land in vocal pauses or drum gaps. If they compete with the lyric, change the note value or shorten the delay. Width is not a measure of quality; a mono delay can push an element back and to one side. The dry signal always comes first.

## Method

Use a send rather than an insert so the effect stays under one control. Choose a dotted eighth or a quarter note at the song tempo, and start with fifteen to thirty percent feedback. High-pass the repeats at three hundred hertz and low-pass them at four thousand so they sit behind. For a clean lead, duck the delay whenever the voice is present. Reserve ping-pong for one element only.

## What to listen for

Hear whether repeats land on the beat, cover the next word, or let the tail disappear naturally. The four notes below are dry; hear them, then picture where each repeat falls.

```audiolab
{"type": "instrument", "gm": "Electric Guitar (clean)", "synth": "plucked", "phrase": ["E4", "B4", "G4", "D5"], "label": "Repeats that land in the gaps", "label_en": "Repeats that land in the gaps", "hint": "听每个音之后的空位，再想八分附点会放在哪", "hint_en": "Hear the space after each note and picture where a dotted eighth would sit"}
```

## Common misconceptions

That delay can replace reverb; that more feedback means more width; that every vocal needs a delay.
:::
