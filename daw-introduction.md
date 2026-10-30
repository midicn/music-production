---
id: daw-introduction
site: prod
cat: A1
title: 数字音频工作站
title_en: Digital Audio Workstation
summary: 把录音、编辑、混音与导出放进同一条时间线的软件。
summary_en: Software that puts recording, editing, mixing and export on one timeline, and what that changes in practice.
level: standard
tags: [DAW, 工作流, 基础]
tags_en: [DAW, workflow, basics]
alias: [DAW, 宿主软件, 音频工作站, digital audio workstation]
links:
  - "[[glossary:daw]]"
  - "[[glossary:sample-rate]]"
  - "[[glossary:bit-depth]]"
instances:
  - pdmx-000922 | 八十秒的巴洛克协奏曲，导入、编辑到导出可以在一节课内走完
  - oga-000001 | 短小的游戏管弦片段，适合练片段复制、循环与工程结构
  - groove-000006 | 单轨鼓循环，第一次建工程时用来确认速度、网格与监听
sources:
  - 数字音频工作站的功能范围与工程结构，依通行 DAW 文档与音频工程教材核查，未抄文本
  - 采样率、位深与缓冲的取舍，依数字音频基础通识核查，未抄文本
updated: 2026-10-28
---

::: zh
DAW 是一类把录音、编辑、混音与导出收进同一张时间线的工具。它不改变声音，只让这些工作共享时间。

## 问题

录音机、编辑器与调音台分开用时，换工具就要重新对时，状态也散在几个文件里。DAW 把素材、处理与决定放在一处，让改动可回退、可比较。

## 原理或做法

工程文件不存声音，只记轨道、片段位置、插件参数与自动化。音频引擎按缓冲区分块计算，缓冲越小延迟越低，CPU 压力越大。采样率与位深在建工程时定下，再改需重采样。

## 参数与判断

先定采样率与位深，再定缓冲。录音用 128 到 256 样本，混音放到 512 以上。速度与拍号要跟素材一致。导出前确认无轨道静音或旁路。

## 听什么

用同一段钢琴短句，在监听与导出文件之间切换。差别通常不在音色，而在延迟、尾音与电平。若导出更闷，先查采样率与监听链，而不是插件。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5"],"label":"工程里的试听短句","label_en":"A short phrase in the project","hint":"听尾音与房间感，再对比导出文件","hint_en":"Listen to the tail and space, then compare the export"}
```

## 常见误解

DAW 不保证音质，音质取决于录音、处理与导出。工程能打开也不等于能复现，缺插件或采样库时声音会被换掉。工程文件不是音频，不能当成品发给别人。
:::

::: en
A DAW is not a brand name but a class of tool that gathers sound work onto one timeline. It does not make sound better; it makes recording, editing, mixing and export share one clock and level scale.

## The problem

When recorder, editor and console live in separate tools, every switch costs a re-alignment, and the work scatters across files. A DAW keeps material, processing and decisions together so changes can be undone and compared.

## How it works

The project file stores no audio, only tracks, clip positions, plug-in settings and automation. The audio engine works in buffer blocks, so a smaller buffer lowers latency and raises CPU load. Sample rate and bit depth are fixed at creation; changing them later means resampling.

## Settings and judgement

Set sample rate and bit depth first, then buffer size. Use 128 to 256 samples for recording, 512 or more for mixing. Match tempo, meter and grid to the material. Before export, check that no track is soloed or bypassed.

## What to listen for

Play the same piano phrase through live monitoring and through the export. The difference is usually latency, tail and level, not tone. If the export sounds duller, check sample rate and monitoring before blaming a plug-in.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "C5"], "label": "A short phrase in the project", "label_en": "A short phrase in the project", "hint": "听尾音与房间感，再对比导出文件", "hint_en": "Listen to the tail and space, then compare the export"}
```

## Common misunderstandings

A DAW does not guarantee quality; recording, processing and export settings do. A project that opens may not reproduce, because missing plug-ins or samples are replaced silently. A project file is not an audio file and cannot be sent as a master.
:::
