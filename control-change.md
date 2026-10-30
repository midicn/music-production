---
id: control-change
site: prod
cat: B1
title: 控制变化（CC）
title_en: Control Change
summary: CC 是连续控制的通道，7 号音量与 64 号延音踏板都走这条通道。
summary_en: Control Change carries continuous gestures such as volume and sustain, one controller number at a time.
level: standard
tags: [MIDI, CC, 控制器, 表情]
tags_en: [MIDI, CC, controller, expression]
alias: [控制变化, 控制器消息, CC, Control Change]
links:
  - "[[glossary:midi-protocol]]"
  - "[[glossary:velocity]]"
  - "[[instrument:violin]]"
instances:
  - musicnet-000265 | 钢琴四重奏，弦乐通道有 4798 条 CC11，表情随乐句起伏
  - musicnet-000073 | 钢琴奏鸣曲，两个通道各 28 条 CC64，踏板起落清楚
  - oga-000089 | 游戏配乐，通道 0 有 147 条 CC11，另有 RPN 设置弯音范围
sources:
  - MIDI 1.0 规范的控制器编号表，依 MMA 公开规范核查，未抄文本
  - CC 与 RPN 的实际用法，依通行合成器文档核查，未抄文本
updated: 2026-10-28
---

::: zh
音符只说明按了哪个键、用了多大力；音量、踏板与滤波的明暗，都走控制变化。

## 问题

回放时没有踏板、弦乐没有起伏、推子动了音量却不变，多半是 CC 号或通道写错。CC 是通道消息，对象错了，整条曲线都落在别处。

## 协议或消息

CC 的状态字节是 0xBn，后跟控制器号与数值，各取 0 到 127。7 号音量、10 号声像、11 号表情、1 号调制、64 号延音、71 号共鸣、74 号截止、91 号混响。100 与 101 号用来选择 RPN，再由 6 号与 38 号写入。14 位控制器用 0 到 31 号与 32 到 63 号成对。121 号重置所有控制器，123 号关闭所有音。

## 参数与做法

表情与音量分开用，表情留给乐句，音量留给平衡。踏板 0 到 63 为关，64 到 127 为开。RPN 要先选参数再写值，顺序反了不生效。曲线控制点不必太密，耳朵听的是走向。

## 听什么

弦乐长音上的 CC11 起伏像呼吸；钢琴的 CC64 让和弦叠成一片；CC7 改变整体响度，却不改变音色。

## 常见误解

CC 不等于自动化曲线，曲线只是编辑界面。CC7 不是力度。同一个 CC 在不同音源上可能完全不同。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G4","A4","B4","D5"],"label":"表情推子留下的呼吸","label_en":"A breath left by expression","hint":"听长音中间的起伏，想象 CC11 在音符内部推移","hint_en":"Hear the swell inside the long notes and picture CC11 moving during them"}
```
:::

::: en
Notes say which key was pressed and how hard. Volume, pedals and filter brightness travel as Control Change.

## The problem

No pedal on playback, flat strings, or a fader that moves without effect usually means a wrong CC number or channel. A CC is a channel message, so the wrong channel puts the whole curve on another part.

## Protocol or message

CC uses 0xBn, then a controller number and a value, both 0 to 127. 7 is volume, 10 pan, 11 expression, 1 modulation, 64 sustain, 71 resonance, 74 cutoff and 91 reverb. Controllers 100 and 101 select an RPN, which 6 and 38 then write. 14-bit controllers pair 0 to 31 with 32 to 63. 121 resets all controllers and 123 stops all notes.

## Settings and practice

Keep expression and volume separate, expression for phrasing and volume for balance. Sustain is off from 0 to 63 and on from 64 to 127. Select an RPN before writing its value, or the order fails. Curves need fewer points than expected,.

## What to listen for

CC11 on a long string note sounds like breathing. CC64 on piano stacks chords into one surface. CC7 changes overall loudness without changing timbre.

## Common misunderstandings

CC is not the same as an automation curve, which is only an editing view. CC7 is not velocity. The same CC can behave differently on another instrument.

```audiolab
{"type": "instrument", "gm": "Violin", "synth": "bowed", "phrase": ["G4", "A4", "B4", "D5"], "label": "A breath left by expression", "label_en": "A breath left by expression", "hint": "听长音中间的起伏，想象 CC11 在音符内部推移", "hint_en": "Hear the swell inside the long notes and picture CC11 moving during them"}
```
:::
