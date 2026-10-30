---
id: comping-and-alignment
site: prod
cat: A4
title: 切片与对齐
title_en: Comping and Alignment
summary: 从多次录音里挑出最好的片段，接成一条听不出接缝的轨
summary_en: Pick the best fragments from several takes and join them into one seamless track.
level: standard
tags: [录音, 剪辑, 拼接]
tags_en: [recording, editing, comping]
alias: [切片, 拼接, 剪辑对齐, comping, take comping, comp]
links:
  - "[[glossary:daw]]"
  - "[[glossary:latency-compensation]]"
  - "[[instrument:acoustic-guitar]]"
instances:
  - groove-000039 | 拉丁打击乐小节短而循环多，切点密集且都落在拍上
  - mutopia-000848 | 独奏吉他练习曲分句清楚，接缝藏在句尾最容易听不出
  - atepp-004305 | 主题反复回到同一句，适合对比不同段落的表现取舍
sources:
  - AES Convention paper on edit-point perception and crossfade length
  - Eargle, Handbook of Recording Engineering, editing and assembly chapters
updated: 2026-10-28
---

::: zh
## 问题

一遍录完往往没有一条全对：这一句音准好，那一句情绪好。切片就是把多次录音里最好的片段挑出来，接成一条完整的轨，再让接缝听不出来。

## 信号链

同一段录三到五遍，各自成轨并对齐到同一时间原点，播放时只让一条发声。选定片段后用短交叉淡化连接，接缝前后的环境声、呼吸与尾音要保持连续。

## 摆位与参数

切点放在字头之前或换气处，避开长音中间。交叉淡化取 5 至 20 毫秒，长度随素材疏密调整。切完逐句用单声道回听，再整体连续播放，检查电平与音色在接缝处是否跳。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"e e e e e e e e","bpm":100,"label":"切点落在这张网格上","label_en":"Cut points on this grid","hint":"先听八分网格，再想哪一格适合下刀","hint_en":"Hear the eighth grid, then choose the cell to cut on"}
```

## 听什么

先听接缝有没有咔嗒或突然的安静，再听同一句两个版本交替时的音色差。连续播放整段，注意呼吸是否被打断，重音是否还落在同一位置。

## 常见误解

- **切片只是剪掉错音** → 拼的是表现，不只是准确。
- **切点越短越安全** → 淡化太短会留下咔嗒。
- **对齐只靠看波形** → 波形对齐后仍要用耳朵确认瞬态。
:::

::: en
## The problem

A single pass rarely gets everything right: one phrase has tuning, another has feel. Comping chooses the best fragments from several takes and joins them into one track whose seams no one hears.

## Signal chain

Record the section three to five times, each on its own track and aligned to the same start point, only one playing at a time. Join the chosen fragments with short crossfades so room tone, breath and tails stay continuous.

## Placement and settings

Put edit points before a consonant or inside a breath, never inside a sustained note. Use crossfades of 5 to 20 ms, scaled to the material. Check each phrase in mono, then play the whole take to hear whether level and tone jump at the joins.

```audiolab
{"type": "rhythm", "sig": "4/4", "pattern": "e e e e e e e e", "bpm": 100, "label": "Cut points on this grid", "label_en": "Cut points on this grid", "hint": "先听八分网格，再想哪一格适合下刀", "hint_en": "Hear the eighth grid, then choose the cell to cut on"}
```

## What to listen for

Listen first for a click or sudden silence at the join, then for tone changes as two versions of the same phrase alternate. Play the whole section and notice whether the breathing is broken and the accents still fall in the same place.

## Common misconceptions

- **Comping only removes wrong notes** → it chooses interpretation, not just accuracy.
- **Shorter fades are always safer** → too short a fade leaves a click.
- **Alignment is a visual job** → after matching waveforms, confirm attacks by ear.
:::
