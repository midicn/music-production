---
id: overdubbing
site: prod
cat: A4
title: 叠录
title_en: Overdubbing
summary: 一遍一遍叠上去，难点是让每遍贴住第一遍的时间与呼吸
summary_en: Overdubs only work when each pass locks to the first in time, tuning and breath.
level: standard
tags: [录音, 叠录, 多轨]
tags_en: [recording, overdub, multitrack]
alias: [叠录, 多遍录音, 叠加录音, overdub, overdubbing, stacking takes]
links:
  - "[[glossary:headphone-mix]]"
  - "[[glossary:latency]]"
  - "[[instrument:voice]]"
instances:
  - groove-000545 | 鼓组先录成基准，后续声部都贴着这条拍子叠
  - openscore-000818 | 人声与钢琴分属两轨，叠录顺序决定谁跟谁呼吸
  - mutopia-000234 | 四声部赞美诗适合逐部叠录，最后听纵向和声是否齐
sources:
  - Huber and Runstein, Modern Recording Techniques, overdubbing and cue-mix chapters
  - AES Convention paper on latency and timing in layered studio performance
updated: 2026-10-28
---

::: zh
## 问题

乐队不能同时演奏，或一个人要奏几个声部时，录音只能一遍一遍叠上去。难的不是录，而是第二遍要贴住第一遍的时间、音准与呼吸，否则叠得越多越散。

## 信号链

先录基准轨，通常是鼓或吉他，它同时是节拍与和声的参照。之后每一遍通过耳机返送听到已有声部，再把自己的演奏录进新轨。返送、延迟与话筒串音共同决定叠得准不准。

## 摆位与参数

基准轨先定速度与调，全程开节拍。返送里给足已录声部，自己的乐器或人声略低一点。缓冲区压到 64 至 128 采样，让往返延迟落在 10 毫秒内。每遍录完立刻回听，不要攒到最后一起听。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q q q q","bpm":96,"label":"每一遍都要贴住的参考拍","label_en":"The pulse every pass must follow","hint":"先跟着拍子数四拍，再想第二遍要在哪一拍进","hint_en":"Count four beats with it, then decide where the second pass enters"}
```

## 听什么

把基准轨与新轨单独合起来，听音头是否同时到达。再听叠了四遍的合唱或吉他，声部一多，时间差会变成一片模糊的宽，而不是更厚。

## 常见误解

- **叠得越多越厚** → 时间不齐时，叠加只增加模糊。
- **返送越大越好** → 听不清自己，音准与力度先失控。
- **必须一遍录到完美** → 分段录、之后切片，是常规做法。
:::

::: en
## The problem

When a band cannot play together, or one player covers several parts, the recording is built one pass at a time. The difficulty is making each new pass sit with the timing, tuning and breath of the first; the more passes, the easier they drift apart.

## Signal chain

Record a reference part first, usually drums or guitar, carrying the tempo and harmony. Each later pass hears the existing parts through headphones and records to a new track. Cue mix, latency and bleed decide how tight the stack becomes.

## Placement and settings

Set tempo and key with the reference part and run a click throughout. Give the existing parts plenty of level in the cue and keep your own instrument slightly lower. Use a buffer of 64 or 128 samples so latency stays under 10 ms, and listen back after every pass.

```audiolab
{"type": "rhythm", "sig": "4/4", "pattern": "q q q q", "bpm": 96, "label": "The pulse every pass must follow", "label_en": "The pulse every pass must follow", "hint": "先跟着拍子数四拍，再想第二遍要在哪一拍进", "hint_en": "Count four beats with it, then decide where the second pass enters"}
```

## What to listen for

Sum the reference and the new pass alone and hear whether the attacks land together. A four-pass stack turns timing differences into blurry width rather than weight.

## Common misconceptions

- **More layers means more weight** → without timing, layers only add blur.
- **The louder the cue the better** → if you cannot hear yourself, pitch and dynamics go first.
- **Every pass must be perfect** → recording in sections and comping later is normal.
:::
