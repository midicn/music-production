---
id: notation-daw-roundtrip
site: prod
cat: B6
title: 制谱与 DAW 往返
title_en: Score and DAW Round Trips
summary: 乐谱与 DAW 往返，真正的难题是力度、连奏与时间基准的转换。
summary_en: Round trips between score and DAW succeed or fail on velocity, legato and the time base.
level: standard
tags: [制谱, DAW, 交换, 工作流]
tags_en: [notation, DAW, exchange, workflow]
alias: [制谱与 DAW 往返, 乐谱往返, 谱面交换, score DAW round trip, notation workflow]
links:
  - "[[glossary:daw]]"
  - "[[glossary:score]]"
  - "[[glossary:tempo]]"
instances:
  - oga-000052 | 配乐里有速度与拍号变化，往返时最容易暴露时间基准问题
  - atepp-001875 | 三声部创意曲的连奏细密，换成 MIDI 后声部容易粘在一起
  - m21-000001 | 众赞歌节奏方正，适合逐小节对比往返前后的音符数
  - atepp-000369 | 自由速度的夜曲，往返后重音与呼吸最容易移位
sources:
  - MusicXML 与标准 MIDI 文件在符号与事件上的差异，依公开规范核查，未抄文本
  - 制谱软件与 DAW 之间交换工程的通行做法，依公开文档核查，未抄文本
updated: 2026-10-28
---

::: zh
在 DAW 里改完回谱，或在谱里改完回 DAW，两次转换都要经过格式，每次都会重新解释一部分信息。

## 问题

谱面关心分句、连线、力度记号与排练号，DAW 关心精确时间、控制器与自动化。两边都以为自己保存了完整信息，交换后才发现各少一半。

## 原理或流程

MusicXML 保存符号与版面，MIDI 保存事件与时间。连奏在谱上是连线，在 MIDI 里是音尾重叠或 CC64；渐强在谱上是发夹记号，在 MIDI 里是一串力度值。往返时轨道名、速度图与小节编号常被重写。

## 做法与判断

先定一个主版本，结构修改只在一端进行。谱面交换用 MusicXML，演奏交换用 MIDI。每次往返后对比小节数、速度事件、轨道数与首尾音；总谱与分谱分开管理；交付前冻结一次。

## 听什么

听连奏是否变成断奏，重音是否移位，渐强是否还在。把往返前后的同一段接起来听，接缝处的音头最说明问题。

## 常见误解

往返无损；格式开放就通用；DAW 的量化可以替代谱面分句。量化只对齐时间，不会替你决定哪里换气。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","D4","E4","F4","G4"],"label":"一条连奏线，听音与音之间有没有缝","label_en":"A legato line, hear the seam between notes","hint":"先听音尾怎样交给下一个音，再想它经过两种格式后会变成什么样","hint_en":"Hear how each tail hands over to the next, then imagine it after two format conversions"}
```
:::

::: en
Revise in the DAW and return to the score, or revise the score and return to the DAW. Each trip goes through a format, and each can lose something.

## The problem

A score cares about phrasing, slurs, dynamics and rehearsal marks. A DAW cares about exact time, controllers and automation. Both assume they hold everything until the exchange shows what is missing.

## How it works

MusicXML keeps symbols and layout; MIDI keeps events and time. A slur is a curve in the score, but overlapping tails or CC64 in MIDI. A hairpin is a mark on the page, but a stream of velocity values. Track names, tempo maps and bar numbers are rewritten on the way.

## Practice and judgement

Choose one master version and make structural edits at one end only. Exchange notation with MusicXML and performance with MIDI. After each trip compare bar count, tempo events, track count and first and last notes. Keep full and part scores separate, then freeze before delivery.

## What to listen for

Hear whether legato turns into staccato, accents shift or the crescendo survives. Join the passage from before and after; the attack at the seam tells the story.

## Common misunderstandings

Round trips are lossless; an open format works everywhere; DAW quantisation replaces phrasing. Quantisation aligns time, not breath.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C4", "D4", "E4", "F4", "G4"], "label": "A legato line, hear the seam between notes", "label_en": "A legato line, hear the seam between notes", "hint": "先听音尾怎样交给下一个音，再想它经过两种格式后会变成什么样", "hint_en": "Hear how each tail hands over to the next, then imagine it after two format conversions"}
```
:::
