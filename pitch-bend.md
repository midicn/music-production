---
id: pitch-bend
site: prod
cat: B1
title: 弯音（Pitch Bend）
title_en: Pitch Bend
summary: 弯音用 14 位数值表示偏离中心的量，范围由 RPN 决定。
summary_en: Pitch Bend sends a 14-bit offset from centre, and an RPN decides how far that offset reaches.
level: standard
tags: [MIDI, 弯音, 音高, RPN]
tags_en: [MIDI, pitch bend, pitch, RPN]
alias: [弯音, 弯音轮, Pitch Bend, 滑音轮]
links:
  - "[[glossary:midi-protocol]]"
  - "[[instrument:violin]]"
  - "[[period:romantic]]"
instances:
  - oga-000089 | 有 241 条弯音，数值都在中心以下，最低到 -2702，是持续的下滑
  - oga-000025 | 91 条弯音，最低到 -8192，是默认范围下的满幅下滑
  - oga-000013 | 43 条弯音全在中心值 0，消息存在但听不出偏移
sources:
  - MIDI 1.0 规范对弯音消息的 14 位编码，依 MMA 公开规范核查，未抄文本
  - RPN 0 的弯音范围设置，依通行合成器文档核查，未抄文本
updated: 2026-10-28
---

::: zh
弯音是一条连续的偏移量，不是音符。它的中心、范围和方向都由接收端决定。

## 问题

吉他的推弦、弦乐的滑音、合成器的俯冲，都靠弯音。范围没对齐，同样的数值会滑出不同的音程；忘了回中，整段都会偏高。

## 协议或消息

状态字节 0xEn，后跟两个数据字节，低 7 位在前，高 7 位在后，合成 14 位数值。0x2000 为中心，0 为最低，0x3FFF 为最高，实际偏移由音源设定的范围决定，默认常见为上下各两个半音。RPN 0 可以改范围，先发 CC101 与 CC100 都为 0，再用 CC6 写半音数、CC38 写音分。弯音作用于所在通道的所有发声音符。

## 参数与做法

工程与音源的弯音范围要一致。回中就是发中心值。事件密度决定滑音是否平滑。颤音用 CC1，不要用弯音硬画。

## 听什么

从中心拉到最低，默认范围下是两个半音的下滑；小幅弯音更像音准漂移，大幅才像滑音。

## 常见误解

弯音不是音符，不能单独发声。范围不是固定的。中心值不是 0。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["A4","B4","C5","D5"],"label":"从中心滑到最低","label_en":"From centre to the bottom","hint":"听最后一个音，想象它在两秒内向下滑两个半音","hint_en":"On the last note, imagine a two-semitone slide down across two seconds"}
```
:::

::: en
Pitch Bend is a continuous offset rather than a note. Its centre, range and direction are set by the receiver.

## The problem

Guitar bends, string slides and synth dives all depend on it. If the range is mismatched, the same value produces a different interval, and a forgotten return to centre leaves the whole part sharp.

## Protocol or message

The status byte is 0xEn followed by two data bytes, low 7 bits first and high 7 bits second, forming a 14-bit value. 0x2000 is centre, 0 is the bottom and 0x3FFF the top. The offset comes from the instrument's range, often two semitones each way. RPN 0 changes that range. Send CC101 and CC100 as 0, then CC6 for semitones and CC38 for cents. A bend affects every sounding note on the channel.

## Settings and practice

Match the range in the project and the instrument. Return to centre by sending the centre value. Event density decides how smooth the slide sounds. Use CC1 for vibrato instead of drawing it with bends.

## What to listen for

Pulling to the bottom gives a two-semitone slide at the default range. A small bend sounds like drifting intonation, while a large one sounds like a slide.

## Common misunderstandings

A bend is not a note and cannot sound alone. The range is not fixed. The centre value is not 0.

```audiolab
{"type": "instrument", "gm": "Violin", "synth": "bowed", "phrase": ["A4", "B4", "C5", "D5"], "label": "From centre to the bottom", "label_en": "From centre to the bottom", "hint": "听最后一个音，想象它在两秒内向下滑两个半音", "hint_en": "On the last note, imagine a two-semitone slide down across two seconds"}
```
:::
