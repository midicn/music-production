---
id: tape-emulation
site: prod
cat: A7
title: 磁带模拟
title_en: Tape Emulation
summary: 磁带同时改变频响、饱和、抖晃与底噪，不只加暖。
summary_en: Tape changes frequency response, saturation, wow and hiss at once; it is not just warmth.
level: standard
tags: [效果器, 磁带, 饱和, 抖晃, 底噪]
tags_en: [effects, tape, saturation, wow and flutter, hiss]
alias: [磁带模拟, 磁带饱和, 磁带味, tape emulation, tape saturation]
links:
  - "[[instrument:tape-music]]"
  - "[[glossary:noise-floor]]"
  - "[[glossary:harmonics]]"
  - "[[glossary:headroom]]"
instances:
  - groove-000000 | 鼓循环的镲片与军鼓，磁带的高频损失与饱和最容易判断
  - pdmx-000031 | 钢琴音头与尾音都清楚，可听磁带怎样改变瞬态与衰减
  - oga-000002 | 风琴与失真吉他持续发声，驱动量改变谐波的比例听得出来
sources:
  - Zölzer, Udo，DAFX — Digital Audio Effects（Wiley）— 磁带饱和与抖晃建模章节核对，未引用
  - Sound On Sound, tape emulation explained — 速度、偏磁与高频损失描述核对，未引用
updated: 2026-10-28
---

::: zh
## 问题
磁带常被当作温暖的代名词。它实际同时改变频响、饱和、抖晃与底噪，四件事方向不同，叠加起来才是所谓磁带味。

## 原理或做法
录音与放音头有高频损失，速度越低损失越早；磁带饱和以奇次谐波为主，偏磁量改变谐波比例；抖晃是转速的慢变与快变，分别造成音高漂移与颤音；底噪则随速度与轨道宽度变化。插件通常把这几段拆开，驱动量、速度与噪声各自可调。

## 参数与判断
轻推做胶水，重推做效果。先听高频是否变暗、低频是否变松，再决定要不要补高频。抖晃深度过大会走音，用在整轨上要谨慎。噪声应低于素材本底，否则只是加了一层嘶声。串联时先饱和后均衡，避免把噪声一起抬高。

## 听什么
镲片是否失去沙沙的细节，钢琴尾音是否变短，贝斯是否变圆，整体是否变窄。与未处理版本对比时，先对齐响度。

```audiolab
{"type":"instrument","gm":"Electric Guitar (clean)","synth":"plucked","phrase":["E2","G2","A2","B2","E3"],"label":"清音吉他的持续音","label_en":"Clean guitar, left to ring","hint":"先听拨弦的亮边，再想象高频被抹掉一截后它怎样变圆","hint_en":"Hear the bright pick edge, then imagine a slice of high end gone and the tone rounded"}
```

## 常见误解
以为磁带等于暖，或插件越旧越好。磁带也会让声音变窄、变慢；它不能修复刺耳，只会把刺耳染成另一种颜色。
:::

::: en
## The problem
Tape is often treated as a synonym for warmth. It actually changes frequency response, saturation, wow and flutter, and hiss at once, and the combination is what we call tape sound.

## How it works
Record and playback heads lose high end, earlier at lower speeds. Tape saturation is mostly odd-harmonic, and bias changes the ratio. Wow and flutter are slow and fast speed variations, producing pitch drift and tremolo respectively. Hiss depends on speed and track width. Plug-ins usually separate these stages, so drive, speed and noise can be set independently.

## Settings and judgement
A light push glues, a heavy one becomes an effect. Hear whether the top darkens and the bass loosens before adding high end back. Too much wow drifts out of tune, so be careful across a whole mix. Noise should sit below the source floor, or it is just added hiss. When chaining, saturate before EQ so the noise is not lifted with the top end.

## What to listen for
Whether cymbals lose their sandy detail, whether piano tails shorten, whether bass rounds out, and whether the whole image narrows. Match loudness before comparing with the untreated version.

```audiolab
{"type": "instrument", "gm": "Electric Guitar (clean)", "synth": "plucked", "phrase": ["E2", "G2", "A2", "B2", "E3"], "label": "Clean guitar, left to ring", "label_en": "Clean guitar, left to ring", "hint": "先听拨弦的亮边，再想象高频被抹掉一截后它怎样变圆", "hint_en": "Hear the bright pick edge, then imagine a slice of high end gone and the tone rounded"}
```

## Common misconceptions
That tape equals warmth, or that older plug-ins sound better. Tape also narrows and slows a sound; it cannot repair harshness, only dye it another colour.
:::
