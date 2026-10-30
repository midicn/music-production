---
id: midi-message-structure
site: prod
cat: B1
title: MIDI 消息结构
title_en: MIDI Message Structure
summary: 一条消息由状态字节与数据字节组成，读懂骨架才能读懂事件流。
summary_en: A message is a status byte plus data bytes, and its frame explains most playback oddities.
level: standard
tags: [MIDI, 协议, 字节, 状态字节]
tags_en: [MIDI, protocol, bytes, status byte]
alias: [消息结构, MIDI 字节, 状态字节, message structure]
links:
  - "[[glossary:midi-protocol]]"
  - "[[glossary:bit-depth]]"
  - "[[instrument:drum-kit]]"
instances:
  - groove-000007 | 单轨鼓循环，210 个音符都由三字节的通道消息构成
  - oga-000297 | 单条轨里装着 5 个通道与 1081 个音符，状态字节的通道位很清楚
  - oga-000025 | 17 条轨、16 个通道，事件流里能同时看到音符、CC 与弯音
sources:
  - MIDI 1.0 规范对状态字节与数据字节的定义，依 MMA 公开规范核查，未抄文本
  - 本库 main 区文件的字节统计，由本地 SMF 解析脚本核对，数值随文件而定
updated: 2026-10-28
---

::: zh
MIDI 传送的不是声音，而是一串结构固定的短消息。看懂骨架，回放怪象就有落点。

## 问题

同一个音在不同软件里时而正常时而错位，问题常在消息而非音源。通道错一位，钢琴会落到鼓组；数据字节越界，会被当成新状态。

## 协议或消息

状态字节最高位为 1，高四位是类型，低四位是通道。0x9n 是 Note On，0x8n 是 Note Off，0xBn 是 CC，0xCn 是 Program Change。数据字节最高位为 0，取值 0 到 127。鼓循环里的 99 2A 57 表示第 10 通道、键号 42、力度 87。文件里每条事件前还有可变长度的 delta time。连续同类消息可省略状态字节，这叫运行状态。

## 参数与做法

排查先看通道，再看类型，最后看数值是否在 0 到 127。超过 127 的值要拆成两条消息或改用 14 位控制器。手工编辑别依赖运行状态，导出时让音序器自己写。

## 听什么

通道差一位，钢琴可能变成鼓，音头与尾音全变。力度差几个数值听感还在，差到二十以上，重音位置就会移动。

## 常见误解

消息不是音频采样，删掉不会留下声音。通道从 0 数起，界面上的 1 到 16 只是显示习惯。运行状态不是压缩算法，只省略重复的状态字节。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5"],"label":"三个字节能说明什么","label_en":"What three bytes can say","hint":"听第一个音的音头，再想状态、键号与力度各占一个字节","hint_en":"Hear the first attack, then picture status, key and velocity each taking one byte"}
```
:::

::: en
MIDI carries short, rigidly structured messages rather than sound.

## The problem

The same note behaves differently in two programs, often because of the message. A channel off by one sends piano to the drums, while an out-of-range byte reads as a new status.

## Protocol or message

A status byte has its top bit set; the high nibble is the type, the low nibble the channel. 0x9n is Note On, 0x8n is Note Off, 0xBn is Control Change, 0xCn Program Change. Data bytes run 0 to 127. A drum loop here stores 99 2A 57, meaning channel 10, key 42, velocity 87. Each event also carries a variable-length delta. Repeated messages may drop the status byte, called running status.

## Settings and practice

Check the channel, the type, then the value range. A value above 127 needs two messages or a 14-bit controller. Do not rely on running status in hand edits; let the sequencer write the file.

## What to listen for

Move a phrase to a neighbouring channel and piano may become drums, changing attack and tail. A few velocity steps go unnoticed, twenty move the accents.

## Common misunderstandings

Messages are not samples, so deleting one leaves no sound. Channels count from 0, while 1 to 16 in interfaces is only a habit. Running status only omits a repeated status byte; it is not compression.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "C5"], "label": "What three bytes can say", "label_en": "What three bytes can say", "hint": "听第一个音的音头，再想状态、键号与力度各占一个字节", "hint_en": "Hear the first attack, then picture status, key and velocity each taking one byte"}
```
:::
