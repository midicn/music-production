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
  - musicnet-000302 | 以 1 起算的第 4 通道在程序值 43 与 45 间切换，可在事件列表核对 | Human-numbered channel 4 switches between program values 43 and 45, visible in the event list
  - oga-000297 | 单轨文件含 6 次程序消息，旋律通道和鼓通道共存 | A single-track file containing six program messages with melodic and drum channels
  - oga-000077 | 32 轨共享 MIDI 通道，含 31 次程序消息；轨道与通道并非一一对应 | 32 tracks share MIDI channels and contain 31 program messages; tracks and channels are not one-to-one
sources:
  - "https://midi.org/summary-of-midi-1-0-messages"
  - MIDI 1.0 规范对 Program Change 与音色库选择的定义，对照 MMA 公开规范整理。
  - GM 音色表与 0 起算的编号约定（通用 MIDI 规范）。
updated: 2026-11-02
---

::: zh
换音色是一条短消息，不是换轨。

## 问题

一段音乐中途要换乐器，复制轨道最省事，却让通道与音符翻倍。用 Program Change 可以在同一条通道上换，但发错时机就会切在音上。

## 协议或消息

状态字节 0xCn，后跟一个 0 到 127 的音色号。人读的 GM 列表从 1 起算，文件里从 0 起算，40 号对应小提琴。需要音色库时先发 CC0 与 CC32 选库，再发音色号。第 10 通道在 GM 下固定为鼓，音色号对它无效。消息只改通道，不改轨道，也不改已经发出的音符。

## 参数与做法

把选库和音色消息放在乐句之前，给设备按说明书留出载入时间。先释放音符与延音踏板，再检查换音色是否截断尾音、重置效果或丢失控制器状态。不要假定重复发送同一程序值永远无副作用；有的设备会重新载入音色。多轨共用通道时，一次切换会影响这些轨后续触发的音符。

## 听什么

同一段旋律用钢琴与弦乐，音头与延音完全不同。低音从 43 换到 45，断奏感立刻出现。

## 常见误解

切换音色不会改已发出的音符。GM 编号与厂商编号不是一套。程序切换也不是轨道属性。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G4","B4","D5","G5"],"label":"乐器音色参照","label_en":"Instrument timbre reference","hint":"这里的固定乐句用于熟悉音色，没有在曲中发送 Program Change。实际切换要检查通道、程序值与载入时机。","hint_en":"This fixed phrase illustrates timbre without an in-song Program Change. Check channel, program value and loading time for an actual switch."}
```
:::

::: en
Changing an instrument is one short message, not a new track.

## The problem

When a piece needs another sound halfway, copying the track is easy but doubles channels and notes. Program Change can switch within one channel, though a badly timed message cuts a sounding note.

## Protocol or message

The status byte is 0xCn, followed by a program number from 0 to 127. The GM list people read starts at 1, while files start at 0, so 40 is Violin. To select a bank, send CC0 and CC32 first, then the program. Channel 10 is fixed to drums under GM and ignores the program number. The message changes a channel, not a track, and not notes already sounding.

## Settings and practice

Send bank and program selection before the phrase and allow the loading time specified by the device. Release notes and sustain, then check whether the change cuts tails, resets effects or loses controller state. Repeating a program value is not universally harmless: some instruments reload the patch. Tracks sharing a channel also share its subsequent program selection.

## What to listen for

The same melody on piano and strings differs in attack and decay. A bass moving from 43 to 45 gains an audible pluck.

## Common misunderstandings

A switch does not retune sounding notes. GM numbers are not vendor numbers. Program Change is not a track property.

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G4","B4","D5","G5"],"label":"Instrument timbre reference","label_en":"Instrument timbre reference","hint":"This fixed phrase illustrates timbre without an in-song Program Change. Check channel, program value and loading time for an actual switch.","hint_en":"This fixed phrase illustrates timbre without an in-song Program Change. Check channel, program value and loading time for an actual switch."}
```
:::
