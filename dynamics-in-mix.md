---
id: dynamics-in-mix
site: prod
cat: A6
title: 动态控制的目的
title_en: The Purpose of Dynamics Control
summary: 压缩不是为了更响，而是让段落之间的强弱关系站得住。
summary_en: Compression is not there to make things louder; it lets the contrast between sections hold together.
level: standard
tags: [混音, 动态, 压缩, 段落]
tags_en: [mixing, dynamics, compression, sections]
alias: [混音动态, 动态控制, mix dynamics]
links:
  - "[[glossary:compressor]]"
  - "[[glossary:parallel-compression]]"
  - "[[instrument:drum-kit]]"
  - "[[period:romantic]]"
instances:
  - musicnet-000069 | 弦乐四重奏的慢乐章起伏长，适合听压缩前后的呼吸（C1）
  - oga-000004 | 游戏战斗循环几乎全程满能量，容易听出动态被压平（C1）
  - atepp-000369 | 格里格《夜曲》钢琴强弱跨度大，适合对照段落对比（C1）
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook, dynamic control and bus compression — background checked, not quoted
  - David Gibson, The Art of Mixing, energy and section contrast — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

每轨都挂压缩，总线再加限制器，副歌确实更响了，却和主歌一样平。鼓的起音被削掉，人声一直贴在前景，听众找不到可以呼吸的地方。动态被当成了需要消灭的东西。

## 目标与判断

动态要服务段落。主歌留出让歌词落地的空间，副歌通过演奏力度、编曲密度与少量电平提升推出两到四 dB 的差距。判断时看短时响度差，也看鼓的瞬态是否还在。压缩的任务是粘合与控峰，不是把整首歌压成一个音量。

## 做法

先用推子自动化做出段落的自然起伏，再给单轨二到四 dB 的增益衰减。总线压缩用慢启动、二比一左右，只做一到二 dB，保留鼓的起音。需要密度时用并行压缩，把干净信号留在前面。每加一级都旁通对比，确认没有把弱音也推上来。

## 听什么

听主歌到副歌是变强还是只变响，鼓的起音是否还在，安静段落的指尖声与呼吸是否保留。下面四个音先听起音，再想压缩会削掉哪一部分。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"起音还在不在","label_en":"Is the attack still there","hint":"听每个音的开头，再想象慢启动压缩如何放过它","hint_en":"Hear each onset and picture a slow-attack compressor letting it through"}
```

## 常见误解

以为压缩越多越专业；以为响度就是能量；以为每一条轨都必须压缩。
:::

::: en
## The problem

Compress every track, add a limiter on the bus, and the chorus does get louder, yet it feels as flat as the verse. Drum attacks are shaved off, the vocal stays pinned in front, and listeners find nowhere to breathe. Dynamics have been treated as something to eliminate.

## Goal and judgement

Dynamics should serve the sections. The verse leaves room for the lyric to land; the chorus earns a two to four dB lift through performance, arrangement density and a small level rise. Judge the short-term loudness difference and whether drum transients survive. Compression exists to glue and control peaks, not to force the whole song into one level.

## Method

Ride faders first to create natural section movement, then ask each track for two to four dB of gain reduction. Use bus compression with a slow attack and a ratio near two to one, reducing only one to two dB so drum attacks pass through. When density is needed, use parallel compression and keep the clean signal in front. Bypass at every stage and confirm that quiet notes have not been pushed up.

## What to listen for

Hear whether the chorus grows stronger or merely louder, whether drum attacks remain, and whether finger noise and breath survive in quiet passages. The four notes below have clear onsets; hear them first, then imagine what compression would remove.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C4", "E4", "G4", "C5"], "label": "Is the attack still there", "label_en": "Is the attack still there", "hint": "听每个音的开头，再想象慢启动压缩如何放过它", "hint_en": "Hear each onset and picture a slow-attack compressor letting it through"}
```

## Common misconceptions

That more compression sounds more professional; that loudness equals energy; that every track needs a compressor.
:::
