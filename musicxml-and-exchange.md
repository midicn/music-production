---
id: musicxml-and-exchange
site: prod
cat: B6
title: 乐谱交换格式
title_en: Score Exchange Formats
summary: MusicXML 保布局、MIDI 保时值，跨软件交付要先想清楚丢掉什么。
summary_en: MusicXML keeps layout and MIDI keeps timing; before moving a score between programs, decide what may be lost.
level: standard
tags: [MusicXML, 交换格式, 记谱软件, 互操作]
tags_en: [MusicXML, exchange format, notation software, interoperability]
alias: [MusicXML, 乐谱交换, 格式转换, score exchange]
links:
  - "[[glossary:daw]]"
  - "[[glossary:tempo]]"
  - "[[glossary:timbre]]"
instances:
  - thesession-015842 | 爱尔兰传统曲调的单声部旋律，最考验交换格式是否保住装饰音（C1）
  - musicnet-000068 | 贝多芬弦乐四重奏的多声部织体，跨软件交换时看声部是否错位（C1）
  - atepp-007103 | 莫扎特回旋曲的钢琴织体，看交换后连音线与力度是否还在（C1）
sources:
  - MusicXML 的设计目标与常见丢失项，依公开格式文档核对，未抄原文
  - 记谱软件与 DAW 之间的往返流程，依软件公开说明核对，未抄文本
updated: 2026-10-28
---

::: zh
## 问题

作曲、编曲、排版、录音常在不同软件里完成。把一份谱子从记谱软件送到 DAW，或从 DAW 送回记谱软件，需要一种双方都能读的格式。选错格式，结果可能是一堆没有连音线的音符，或者完全错位的声部。

## 原理

MusicXML 用结构化标签描述音符、休止、连音、力度、歌词与版面，目标是把记谱信息完整搬过去，包括换行与小节分配。MIDI 文件只描述演奏事件：音高、时值、力度、通道，不描述谱面。所以 MIDI 往返会丢掉连音、装饰音写法、分句与版面，而 MusicXML 往返能保住谱面，但演奏细节（如摇摆、自由速度）表达不出来。压缩的 MusicXML 只是换了封装，内容一样。部分软件还支持自己的原生格式，互通性最差。

## 参数与做法

谱面交付优先用 MusicXML，演奏交付优先用 MIDI。导出前检查连音、装饰音、力度与歌词是否都在。导入 DAW 后量化要谨慎，别把装饰音抹平。从 DAW 回记谱软件时，先整理声部与拍号，再交给排版。跨版本时用未压缩格式，减少兼容问题。交付包里同时附 PDF 与源文件，接收方才有选择。

## 听什么

在传统曲调里听装饰音是否还在，在四重奏里听四个声部有没有错位，在钢琴回旋曲里听连音与力度是否保住。格式问题往往在打开文件的那一刻就暴露，不必等到演奏。

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (nylon)","synth":"plucked","phrase":["D4","E4","F#4","G4","A4","G4","F#4","E4"],"label":"装饰音的位置","label_en":"Where the ornaments sit","hint":"装饰音在谱面上是记号，在 MIDI 里只是更短的音符，交换时最容易变形","hint_en":"Ornaments are marks on the page but short notes in MIDI, the first thing to deform in exchange"}
```
:::

::: en
## The problem

Writing, arranging, engraving and recording often happen in different programs. Sending a score from notation software to a DAW, or back again, needs a format both sides can read. Choose badly and you get notes without slurs, or parts in the wrong place.

## How it works

MusicXML describes notes, rests, slurs, dynamics, lyrics and layout with structured tags, aiming to carry notation information intact, including line and bar breaks. A MIDI file describes performance events only: pitch, duration, velocity, channel, not the page. So a MIDI round trip loses slurs, ornament spelling, phrasing and layout, while a MusicXML round trip keeps the page but cannot express swing or free timing. Compressed MusicXML is the same content in a different wrapper. Some programs also offer native formats with the poorest interoperability.

## Settings and practice

Deliver notation as MusicXML and performance as MIDI. Before exporting, check that slurs, ornaments, dynamics and lyrics survive. Quantise cautiously after import so ornaments are not flattened. When returning from a DAW to notation, tidy voices and time signatures first, then hand it to engraving. Use uncompressed files across versions to reduce compatibility trouble. Ship a PDF alongside the source file so the recipient has a fallback.

## What to listen for

On the traditional tune, whether ornaments survive; on the quartet, whether four parts stay aligned; on the piano rondo, whether slurs and dynamics remain. Format problems usually show the moment the file opens, long before anyone plays it.

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (nylon)","synth":"plucked","phrase":["D4","E4","F#4","G4","A4","G4","F#4","E4"],"label":"Where the ornaments sit","label_en":"Where the ornaments sit","hint":"Ornaments are marks on the page but short notes in MIDI, the first thing to deform in exchange","hint_en":"Ornaments are marks on the page but short notes in MIDI, the first thing to deform in exchange"}
```
:::
