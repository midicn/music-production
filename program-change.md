---
id: program-change
site: prod
cat: B1
title: 音色切换消息
title_en: Program Change
summary: 音色切换消息只改通道上的音色，不改音符，也不改轨道。
summary_en: Program Change swaps the timbre on one channel without touching notes, tracks or sounding voices.
level: standard
tags: [MIDI, 音色, 通道, GM]
tags_en: [MIDI, program, channel, GM]
alias: [音色切换, 换音色, Program Change, 程序切换]
links:
  - "[[glossary:midi-protocol]]"
  - "[[instrument:violin]]"
  - "[[period:classical]]"
instances:
  - musicnet-000302 | 鳟鱼五重奏第四乐章，3 号通道在 43 与 45 之间切换，低音改拨弦
  - oga-000297 | 单轨文件里有 6 次音色切换，4 个旋律通道各设音色，第 10 通道打鼓
  - oga-000077 | 32 轨共用 16 通道，全曲共 31 次音色切换，逐段重置
sources:
  - MIDI 1.0 规范对 Program Change 与音色库选择的定义，依 MMA 公开规范核查，未抄文本
  - GM 音色表与 0 起算的编号约定，依通用 MIDI 规范核查，未抄文本
updated: 2026-10-28
---

::: zh
换音色是一条短消息，不是换轨。

## 问题

一段音乐中途要换乐器，复制轨道最省事，却让通道与音符翻倍。用 Program Change 可以在同一条通道上换，但发错时机就会切在音上。

## 协议或消息

状态字节 0xCn，后跟一个 0 到 127 的音色号。人读的 GM 列表从 1 起算，文件里从 0 起算，40 号对应小提琴。需要音色库时先发 CC0 与 CC32 选库，再发音色号。第 10 通道在 GM 下固定为鼓，音色号对它无效。消息只改通道，不改轨道，也不改已经发出的音符。

## 参数与做法

在乐句开始前发，避免音尾被切。同一通道重复发同值没有坏处，能防止状态丢失。换音色前先关掉正在发声的音。多轨共用通道时，一次切换会影响所有轨。

## 听什么

同一段旋律用钢琴与弦乐，音头与延音完全不同。低音从 43 换到 45，断奏感立刻出现。

## 常见误解

切换音色不会改已发出的音符。GM 编号与厂商编号不是一套。程序切换也不是轨道属性。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G4","B4","D5","G5"],"label":"换一条消息就换一件乐器","label_en":"One message, another instrument","hint":"同一串音高，想象它由钢琴改由弦乐奏出","hint_en":"Keep the same pitches and imagine them moving from piano to strings"}
```
:::

::: en
Changing an instrument is one short message, not a new track.

## The problem

When a piece needs another sound halfway, copying the track is easy but doubles channels and notes. Program Change can switch within one channel, though a badly timed message cuts a sounding note.

## Protocol or message

The status byte is 0xCn, followed by a program number from 0 to 127. The GM list people read starts at 1, while files start at 0, so 40 is Violin. To select a bank, send CC0 and CC32 first, then the program. Channel 10 is fixed to drums under GM and ignores the program number. The message changes a channel, not a track, and not notes already sounding.

## Settings and practice

Send it before a phrase begins so no tail is cut. Repeating the same value on a channel is harmless and guards against lost state. Close sounding notes before switching. When several tracks share a channel, one switch affects them all.

## What to listen for

The same melody on piano and strings differs in attack and decay. A bass moving from 43 to 45 gains an audible pluck.

## Common misunderstandings

A switch does not retune sounding notes. GM numbers are not vendor numbers. Program Change is not a track property.

```audiolab
{"type": "instrument", "gm": "Violin", "synth": "bowed", "phrase": ["G4", "B4", "D5", "G5"], "label": "One message, another instrument", "label_en": "One message, another instrument", "hint": "同一串音高，想象它由钢琴改由弦乐奏出", "hint_en": "Keep the same pitches and imagine them moving from piano to strings"}
```
:::
