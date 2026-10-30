---
id: what-is-mastering
site: prod
cat: A8
title: 母带是什么
title_en: What Mastering Is
summary: 母带是混音之后的最后一道加工，让作品在各系统上站得住。
summary_en: The final pass after the mix, shaping loudness, tone and peaks so a finished track holds up on many playback systems.
level: standard
tags: [母带, 响度, 流程]
tags_en: [mastering, loudness, workflow]
alias: [母带处理, 母带制作, mastering]
links:
  - "[[glossary:lufs]]"
  - "[[glossary:limiter]]"
  - "[[glossary:maximizer]]"
instances:
  - mutopia-000497 | 贝多芬第五第一乐章动态跨度大，能听出母带是否压扁了起伏
  - musicnet-000067 | 晚期四重奏的弱奏细节，适合检查母带噪声与尾音
  - groove-000010 | 放克鼓循环电平稳定，适合对照限制器前后的瞬态
sources:
  - 母带链中均衡、压缩与限制的分工，依母带工程通识核查，未抄文本
  - 流媒体响度归一与真峰值交付惯例，依平台公开说明核查，未抄文本
updated: 2026-10-28
---

::: zh
母带是混音定稿后的最后一道加工。它不改写编曲，也不替混音补课，只让作品在不同系统上站得住。

## 问题

同一首歌在监听上刚好，到了手机或车里却又薄又轻。几首单曲分开听都不错，放进专辑却响度忽大忽小。

## 目标与标准

母带要守住混音的比例与情绪，同时统一响度、音色和真峰值。常见做法是把整首的 integrated LUFS 定在明确目标，真峰值留在 -1 dBTP 附近，转成有损格式也不削波。标准不是固定数字，而是可重复、可交付，在各系统上都不露馅。

## 做法

先完整听几遍混音，记下低频、动态与声场的问题，只做全局修正。用均衡整理音色，用压缩或限制收住峰值，再检查响度与真峰值。导出高分辨率母带与无损交付版，保留未限制版本。

## 听什么

听低频是否紧实，人声是否稳定，最响处是否刺耳，最静处是否还在。下面这段钢琴可听起音与尾音是否被压扁。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","G4","C5","G4"],"label":"听起音与尾音","label_en":"Attack and tail","hint":"注意每个音的头和余韵，母带过度会先吃掉这两头","hint_en":"Watch the attack and the decay; heavy mastering eats both first"}
```

## 常见误解

母带救不了混音，频段冲突与失衡要回混音解决。它也不等于挂一个限制器，还包括音色判断、曲序与交付。更响不代表更好，平台会做响度归一。
:::

::: en
Mastering is the final pass after the mix is approved. It does not rewrite the arrangement or repair the mix.

## The problem

A song that sits well on studio monitors can turn thin on a phone or in a car. Singles that sound fine alone may jump in level on one album.

## Goals and standards

Mastering preserves the mix's proportions while unifying loudness, tone and true peak. A common approach sets one integrated LUFS target and keeps true peak near -1 dBTP, so lossy encoding does not clip. The result should be repeatable and survive phones, cars and headphones.

## Practice

Listen through the mix and note low-end, dynamic and stereo issues. Make global changes only. Use EQ for tone and compression or limiting for peaks, then check loudness and true peak. Export a high-resolution master and a lossless version, and keep an unlimited copy.

## What to listen for

Hear whether the low end stays tight, the vocal stays stable, loud passages turn harsh and quiet ones still exist. The piano phrase checks attack and tail.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "G4", "C5", "G4"], "label": "Attack and tail", "label_en": "Attack and tail", "hint": "注意每个音的头和余韵，母带过度会先吃掉这两头", "hint_en": "Watch the attack and the decay; heavy mastering eats both first"}
```

## Common misunderstandings

Mastering cannot rescue a mix; frequency clashes belong in the mix. It is more than a limiter, since it includes tone, sequencing and delivery. Louder is not better, because platforms normalise loudness.
:::
