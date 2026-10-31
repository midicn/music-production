---
id: volume-balance
site: prod
cat: A6
title: 音量平衡是八成
title_en: Level Balance Is Most of the Mix
summary: 推子定下谁在前谁在后，多数音色问题会随平衡一起消失。
summary_en: Faders decide what sits forward and back, and many tone problems disappear with balance.
level: standard
tags: [混音, 音量, 平衡, 推子]
tags_en: [mixing, level, balance, faders]
alias: [音量平衡, 推子, 静态平衡, volume balance, fader]
links:
  - "[[glossary:bus]]"
  - "[[glossary:automation]]"
  - "[[instrument:voice]]"
  - "[[instrument:drum-kit]]"
instances:
  - openscore-000008 | 艺术歌曲的旋律与钢琴并置，推子一动就知谁在主导
  - oga-000000 | 三轨小编制，声部少，平衡问题不会被遮住
  - groove-000002 | 灵魂乐鼓组，各件之间的平衡先于任何处理
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook, fader balance chapter — background checked, not quoted
  - David Gibson, The Art of Mixing, visual mapping of level and pan — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

推子是最便宜也最有效的工具，但很多人先动均衡。音量关系一变，同一段均衡的听感也会变。

## 目标与判断

目标是让每个声部在需要时出现，不需要时退后。判断标准很简单，合奏里没有哪一轨需要费力去找。平衡不是每轨一样响，而是每轨在该在的位置。若某轨要推高 6 dB 才听得见，问题多半在编曲或频段，不在推子。人声、底鼓与贝斯通常占前景，铺底与装饰让位。

## 做法

从副歌开始，先定人声与鼓的相对位置；再加贝斯，让底鼓与贝斯交替占低频；和弦铺底降到刚好能感到和声；最后加装饰。每次只动一轨，动完回到整体听十秒。把总线衰减 6 dB，检查平衡是否依赖响度。

## 听什么

听主唱换气时伴奏是否忽然变大；听贝斯与底鼓是否互相盖住；把总音量降到很小，听旋律是否还在。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","E3","G3","C4","G3","E3"],"label":"旋律与伴奏","label_en":"Melody and accompaniment","hint":"先听谁在前，再把伴奏推高 3 dB 对比","hint_en":"Hear what leads, then lift the accompaniment 3 dB and compare"}
```

## 常见误解

把推子当补偿均衡用；以为所有轨都要听得见；以为平衡一次就能定稿。
:::

::: en
## The problem

The fader is the cheapest and strongest tool, yet many reach for EQ first. Change the level relationship and the same EQ is heard differently.

## Goal and judgement

Each part should appear when needed and step back when not. The test is simple: nothing is hard to find in the full mix. Balance is not equal loudness; it is each part sitting where it belongs. If a track needs 6 dB more to be audible, the problem is usually arrangement or spectrum, not the fader. Lead vocal, kick and bass normally sit forward; pads and ornaments give way.

## Method

Begin at the chorus. Set the vocal against the drums, add bass so kick and bass take turns in the low end, bring chords down until harmony is felt rather than heard, then add ornaments. Move one fader at a time and return to the whole mix for ten seconds. Drop the master by 6 dB to check whether balance depends on loudness.

## What to listen for

Whether the backing jumps up between vocal phrases; whether bass and kick cover each other; whether the melody survives at very low volume.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C3", "E3", "G3", "C4", "G3", "E3"], "label": "Melody and accompaniment", "label_en": "Melody and accompaniment", "hint": "先听谁在前，再把伴奏推高 3 dB 对比", "hint_en": "Hear what leads, then lift the accompaniment 3 dB and compare"}
```

## Common misconceptions

Using faders to fix EQ problems; believing every track must be audible; expecting one balance pass to be final.
:::
