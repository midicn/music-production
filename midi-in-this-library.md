---
id: midi-in-this-library
site: prod
cat: B1
title: MIDI 在本库中的样子
title_en: MIDI in This Library
summary: 库里的每首曲子都是一个 id、一条路径与一串可解析的 MIDI 事件。
summary_en: Every track in the library is an id, a path and a stream of parseable MIDI events.
level: standard
tags: [MIDI, 曲库, 元数据, 实例]
tags_en: [MIDI, library, metadata, examples]
alias: [本库, catalog, MIDI 文件统计, 库内呈现]
links:
  - "[[glossary:midi-protocol]]"
  - "[[glossary:daw]]"
  - "[[instrument:midi-controller]]"
instances:
  - oga-000297 | 单轨格式 0，5 个通道 1081 个音符，57.9 秒，适合看事件如何挤在一条轨里
  - groove-000007 | 单轨鼓循环，210 个音符，27.6 秒，依赖第 10 通道与 GM 鼓映射
  - pdmx-000594 | 格式 1，47 条轨 15 个通道，15205 个音符，487.5 秒，适合看大编制的轨与通道比例
sources:
  - 本库 catalog 的字段定义与许可分档（库内文档）。
  - 本库文件的格式与事件统计，由本地 SMF 解析脚本核对，数值随文件而定
updated: 2026-10-28
---

::: zh
面对十三万个文件，怎么知道某一首里有什么？只看标题不够，得看事件与统计。本库把这件事做成了可查的字段。

## 问题

标题常常来自文件名或采集源，不能说明编制与内容。同一首曲子可能有多个版本，音符数、时长与许可都不一样，凭印象引用就会张冠李戴。

## 协议或消息

库以 SMF 保存，catalog 给每首一个 id、标题、来源、许可、时长与音符数。文件路径按来源与风格分目录。解析后能看到轨、通道、音色、CC 与速度。许可分为 main、piano-special、study 三档，条目实例优先取 main。

## 参数与做法

先用 id 定位，再读 catalog 的音符数与时长。需要验证某条消息时，直接解析对应文件。引用实例时写清为什么选它，别只写标题。跨条目复用同一首时，换一个听点。

## 听什么

同一首在不同音源上，鼓与贝斯最先暴露差异。文件里的音符数不等于听感密度，长音与重复音都算。

## 常见误解

库里的文件不是录音。id 不是文件名。catalog 的时长是计算值，不是音频长度。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5"],"label":"文件里的一行事件","label_en":"One line of events in a file","hint":"听这段钢琴，再想它在库里只是一个 id 与若干事件","hint_en":"Hear the piano and picture it as an id plus a stream of events"}
```
:::

::: en
With over a hundred thousand files, a title says little about what is inside. Events and statistics answer the question, and the library turns them into fields.

## The problem

Titles often come from file names or collectors, so they say nothing about scoring or content. One piece may exist in several versions with different note counts, durations and licences, and a guess attaches the wrong facts.

## Protocol or message

The library stores Standard MIDI Files, and the catalog gives each track an id, title, source, licence, duration and note count. Paths are grouped by source and genre. Parsing reveals tracks, channels, programs, controllers and tempo. Licences fall into main, piano-special and study, and entry examples prefer main.

## Settings and practice

Locate a track by id, then read its note count and duration from the catalog. Parse the file when a message needs proof. Explain why an example was chosen instead of quoting its title. When reusing a track across entries, listen for a different detail.

## What to listen for

Drums and bass expose differences first when the same file meets another sound source. Note count is not density, since long notes and repeats both count.

## Common misunderstandings

Library files are not recordings. An id is not a file name. Catalog duration is computed, not an audio length.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "C5"], "label": "One line of events in a file", "label_en": "One line of events in a file", "hint": "听这段钢琴，再想它在库里只是一个 id 与若干事件", "hint_en": "Hear the piano and picture it as an id plus a stream of events"}
```
:::
