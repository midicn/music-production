---
id: midi-file-format
site: prod
cat: B1
title: MIDI 文件格式
title_en: MIDI File Format
summary: SMF 用 MThd 与 MTrk 组织事件，0 与 1 两种格式各有用途。
summary_en: SMF stores events in MThd and MTrk chunks, and formats 0 and 1 serve different jobs.
level: standard
tags: [MIDI, SMF, 文件, 轨道]
tags_en: [MIDI, SMF, file, track]
alias: [MIDI 文件, SMF, 标准 MIDI 文件, Standard MIDI File]
links:
  - "[[glossary:midi-protocol]]"
  - "[[glossary:sample-rate]]"
  - "[[glossary:daw]]"
instances:
  - oga-000297 | format 0，单条 MTrk 装着 5 个通道、1081 个音符
  - musicnet-000300 | format 1，18 条 MTrk，速度表里有多次变速
  - oga-000077 | format 1，32 条 MTrk，却只用 16 个通道
sources:
  - SMF 1.0 规范对 MThd 与 MTrk 的结构定义（MMA 公开规范）。
  - format 0、1、2 与 division 的用法，参考音序器文档。
updated: 2026-10-28
---

::: zh
文件格式决定事件怎样排队，也决定拆轨与变速是否方便。

## 问题

同一段演奏，存成一条轨还是多条轨，编辑体验完全不同。拿到的文件打不开、速度不对、轨道全挤在一起，往往要从文件头找原因。

## 协议或消息

文件以 MThd 开头，头长 6 字节，记录 format、ntrks 与 division，整个头共 14 字节。format 0 只有一条 MTrk；format 1 有多条同步的 MTrk，通常第一条放速度与拍号；format 2 是彼此独立的片段，很少见。每条 MTrk 里是 delta time 加事件，delta 用可变长度编码。division 表示每四分音符的 tick 数，也可以写成 SMPTE。Meta 事件以 0xFF 开头，0x51 是速度，0x58 是拍号，0x2F 是结束。

## 参数与做法

编曲用 format 1，分轨清楚。交换文件也用 format 1，兼容性最好。小型播放器可以吃 format 0。改速度时确认改在 tempo 轨上。

## 听什么

两种格式回放应当一致。若不一致，多半是速度轨或通道分配出了问题。拆轨后逐轨听，确认力度与踏板还在原来的位置。

## 常见误解

轨道数不等于通道数。format 1 的所有轨共用一条时间线。扩展名相同不代表都是 GM。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","D4","E4","G4","C5"],"label":"一条轨与多条轨","label_en":"One track or many","hint":"两种存法听感相同，差别在文件里的事件怎样排队","hint_en":"Both storage ways sound alike, the difference is how events queue inside the file"}
```
:::

::: en
The format decides how events queue and how easily tempo can be edited.

## The problem

Storing the same performance as one track or many changes editing completely. A file that will not open, plays at the wrong tempo or crams parts together points to the header.

## Protocol or message

A file begins with MThd, a 6-byte field holding format, ntrks and division, so the header is 14 bytes. Format 0 has one MTrk. Format 1 has several synchronised MTrk chunks, usually with tempo and time signature first. Format 2 holds independent patterns and is rare. Each MTrk holds delta times and events, with delta as a variable-length number. Division gives ticks per quarter note, or an SMPTE value. Meta events start with 0xFF, where 0x51 is tempo, 0x58 is time signature and 0x2F ends the track.

## Settings and practice

Use format 1 for arranging and exchange, since tracks stay separate and compatibility is best. Small players may prefer format 0. When changing tempo, edit the tempo track.

## What to listen for

Both formats should sound identical. A difference usually means a tempo track or channel problem. After splitting tracks, listen one by one and check that velocity and pedal stayed put.

## Common misunderstandings

Track count is not channel count. Every track in format 1 shares one timeline. The same extension does not guarantee GM.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "D4", "E4", "G4", "C5"], "label": "One track or many", "label_en": "One track or many", "hint": "两种存法听感相同，差别在文件里的事件怎样排队", "hint_en": "Both storage ways sound alike, the difference is how events queue inside the file"}
```
:::
