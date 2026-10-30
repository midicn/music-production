---
id: vocal-chain
site: prod
cat: A6
title: 人声处理链
title_en: Vocal Processing Chain
summary: 先判断问题再加环节，链条越长越容易把字头磨钝。
summary_en: Name the problem before adding a stage, because a longer chain blunts consonants.
level: standard
tags: [混音, 人声, 压缩, 效果链]
tags_en: [mixing, vocal, compression, chain]
alias: [人声链, 人声处理, vocal chain, vocal processing]
links:
  - "[[glossary:compressor]]"
  - "[[glossary:eq]]"
  - "[[instrument:voice]]"
  - "[[period:romantic]]"
instances:
  - openscore-000008 | 戏剧性艺术歌曲，旋律动态大，压缩与均衡的取舍听得出
  - openscore-000007 | 长句多的法语艺术歌曲，气口与释音时间容易判断
  - openscore-000018 | 无词练声曲，旋律连续，适合先练压缩与均衡
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook, vocal mixing chapter — background checked, not quoted
  - David Gibson, The Art of Mixing, lead vocal treatment — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

人声链常被堆成一长串，去齿音、压缩、均衡、饱和、混响样样都有。每一步都合理，合起来却让字头变钝，独奏时甚至听不出问题。

## 目标与判断

先判断问题类型，是电平起伏、频段缺陷、齿音，还是空间不足，只处理真正存在的那个。目标是歌词清楚、情绪连贯，而不是独奏像成品。压缩要看整句，不要只盯峰值。

## 做法

顺序通常是高通、去齿音、压缩、均衡、饱和、空间。压缩从三比一、五到十五毫秒启动、八十到一百五十毫秒释放起；均衡先衰减再提升；饱和只加一点。并行压缩用来保留字头，空间用发送，不要直接插在轨道上。每加一步都旁通一次，确认它真的解决了问题。

## 听什么

听换气与字头是否被压掉；听齿音是否刺耳；加入伴奏后听人声是否仍需推高；听副歌是否比主歌更近。

```audiolab
{"type":"instrument","gm":"Voice Oohs","synth":"vocal","phrase":["A3","C4","E4","D4"],"label":"人声长音","label_en":"Sustained voice","hint":"先听字头，再听压缩后的连贯","hint_en":"Hear the onset, then the continuity after compression"}
```

## 常见误解

以为链条越长越专业；以为压缩越狠越稳；以为齿音只能靠去齿音器解决。
:::

::: en
## The problem

Vocal chains grow into long lists: de-esser, compressor, EQ, saturation, reverb. Each step is reasonable, yet together they blunt every consonant.

## Goal and judgement

Name the problem first: level movement, spectral gap, sibilance, or lack of space. Treat only what is actually there. The goal is intelligible lyrics and a continuous emotional line, not a solo that sounds finished. Compression should follow phrases, not peaks.

## Method

A common order is high-pass, de-esser, compression, EQ, saturation, space. Start compression near 3 to 1 with 5 to 15 ms attack and 80 to 150 ms release. Prefer cuts over boosts in EQ, and add only a little saturation. Use parallel compression to keep consonants. Send to reverb; do not insert it on the track. Bypass each new stage once to confirm it solves a real problem.

## What to listen for

Whether breaths and consonants are crushed; whether sibilants sting; whether the vocal still needs a push once the backing is in; whether the chorus sits closer than the verse.

```audiolab
{"type": "instrument", "gm": "Voice Oohs", "synth": "vocal", "phrase": ["A3", "C4", "E4", "D4"], "label": "Sustained voice", "label_en": "Sustained voice", "hint": "先听字头，再听压缩后的连贯", "hint_en": "Hear the onset, then the continuity after compression"}
```

## Common misconceptions

That a longer chain is more professional; that harder compression is steadier; that sibilance can only be fixed with a de-esser.
:::
