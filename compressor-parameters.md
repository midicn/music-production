---
id: compressor-parameters
site: prod
cat: A7
title: 压缩器的五个参数
title_en: Five Compressor Settings
summary: 阈值、比率、启动、释放与拐点各自改变什么，怎么听出来。
summary_en: What threshold, ratio, attack, release and knee each change, and how to hear the difference on one loop.
level: standard
tags: [效果器, 动态, 压缩, 听感]
tags_en: [effects, dynamics, compression, listening]
alias: [压缩器, 压缩参数, 阈值, 比率, 启动, 释放, compressor, threshold, ratio]
links:
  - "[[glossary:compressor]]"
  - "[[glossary:sidechain]]"
  - "[[glossary:bus]]"
  - "[[instrument:drum-kit]]"
instances:
  - groove-000000 | 放克鼓循环的军鼓边缘清楚，改启动时间时差别最直接
  - groove-000011 | 鼓与贝斯交替出现，释放过长时会听到整体随低频抽吸
  - pdmx-000450 | 勃拉姆斯《德意志安魂曲》动态跨度大，适合观察压缩对强弱层次的保留
sources:
  - Giannoulis, Massberg and Reiss, Digital Dynamic Range Compressor Design, JAES 2012 — background checked, not quoted
  - Huber and Runstein, Modern Recording Techniques, dynamics chapter — typical ranges checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

「压一下」这句话里至少藏着五个参数。只动阈值，声音会忽然变扁；把启动与释放配好，压缩才像在托住演奏，而不是把它按平。

## 原理

检测器读输入电平，超过阈值后按比率缩小增益。2:1 表示超出 10 dB 只留下 5 dB；拐点决定压缩是突然开始还是渐变；启动与释放是增益变化的速度，不是声音的快慢。补偿增益把整体抬回，否则只会觉得变小。

## 参数与听感

人声常从 −20 dB 阈值、3:1 起手，启动 10–30 ms 放过字头，释放 80–200 ms 跟住句子。启动快于 5 ms 会削掉鼓槌的点击；释放太短会随低音起伏，产生抽吸。软拐点适合总线，硬拐点适合控制单个音头。

## 听什么

放鼓组循环，先听军鼓的敲击边缘，再把启动从 30 ms 收到 1 ms。然后让贝斯与鼓同时出现，听整体是否随低音一压一放。

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E2","E2","G2","A2"],"label":"贝斯短句","label_en":"Bass figure","hint":"先听干声，再对比慢启动与快启动","hint_en":"Hear it dry, then compare slow and fast attack"}
```

## 常见误解

把压缩当音量旋钮；以为比率越高越响；认为启动越快越安全。
:::

::: en
## The question

The instruction to compress it hides at least five settings. Move only the threshold and the sound turns flat; match attack and release and compression starts to hold the performance instead of pressing it down.

## How it works

A detector reads the input level and, above the threshold, scales gain by the ratio. At 2 to 1, 10 dB over the threshold leaves 5 dB. The knee decides whether gain reduction begins abruptly or gradually. Attack and release are speeds of gain change, not speeds of the sound. Makeup gain restores the overall level, without which compression only seems quieter.

## Settings and what you hear

For a vocal, start near minus 20 dB with 3 to 1, attack 10 to 30 ms to let consonants through, release 80 to 200 ms to follow phrases. Attack faster than 5 ms removes the beater click of a drum; a very short release pumps with the bass. A soft knee suits a bus; a hard knee suits taming a single transient.

## What to listen for

Play a drum loop and listen to the edge of the snare, then pull attack from 30 ms to 1 ms. Next, with bass and drums together, hear whether the whole picture dips and recovers with every bass note.

```audiolab
{"type": "instrument", "gm": "Electric Bass (finger)", "synth": "plucked", "phrase": ["E2", "E2", "G2", "A2"], "label": "Bass figure", "label_en": "Bass figure", "hint": "先听干声，再对比慢启动与快启动", "hint_en": "Hear it dry, then compare slow and fast attack"}
```

## Common misconceptions

That compression is a volume knob; that a higher ratio means louder; that the fastest attack is always safest.
:::
