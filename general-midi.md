---
id: general-midi
site: prod
cat: B1
title: General MIDI
title_en: General MIDI
summary: GM 规定了 128 个音色、16 个通道与第 10 通道的鼓组。
summary_en: GM fixes 128 programs, 16 channels and a drum kit on channel 10 so files travel between devices.
level: standard
tags: [MIDI, GM, 音色表, 兼容]
tags_en: [MIDI, GM, program map, compatibility]
alias: [通用 MIDI, GM, General MIDI, GM 标准]
links:
  - "[[glossary:midi-protocol]]"
  - "[[instrument:drum-kit]]"
  - "[[glossary:velocity]]"
instances:
  - oga-000297 | 以 GM 音色 32、25、28 开场，分给三个通道，第 10 通道打鼓
  - musicnet-000300 | 弦乐按 40 到 43 分配，钢琴用 0 号音色
  - groove-000007 | 只有第 10 通道，没有音色切换，完全依赖 GM 鼓映射
sources:
  - 通用 MIDI 一级规范对音色表与通道的约定，依 MMA 公开规范核查，未抄文本
  - GM 2 增加的音色库与控制器，依通用 MIDI 规范核查，未抄文本
updated: 2026-10-28
---

::: zh
GM 是一份最小共同约定，让同一份文件在不同设备上大致可听。

## 问题

没有约定，0 号音色在每台设备上可以是任何东西。GM 把 128 个音色、16 个通道与一套鼓固定下来，文件才有可交换性。

## 协议或消息

GM 规定 128 个旋律音色，按 16 个族排列，每族 8 个。通道 10 固定为鼓组，键号 35 到 81 对应打击乐器。音符编号 0 到 127。GM System On 用 SysEx 复位。GM 2 增加音色库、更多的 CC 与包络控制。文件里的音色号是 0 到 127，人读的列表常写成 1 到 128。

## 参数与做法

播放前确认设备处于 GM 模式。鼓固定在第 10 通道。不要依赖扩展音色。默认用 0 号钢琴最安全。跨设备交换时，把音色号写进元数据。

## 听什么

GM 钢琴在哪台设备上都认得出，但亮度与尾音不同；弦乐齐奏的厚度差异最大。同一份文件换音源，先听鼓与贝斯。鼓的键号在 GM 下含义固定，换音源也不改语义。

## 常见误解

GM 不是音质标准。GM 音色号不等于厂商音色号。第 10 通道的鼓不受音色号影响。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"GM 弦乐的共同底线","label_en":"The common floor of GM strings","hint":"听齐奏的厚度，再想同一份文件在另一台设备上的差别","hint_en":"Hear the unison weight, then imagine the same file on another device"}
```
:::

::: en
General MIDI is a minimum agreement that lets one file sound roughly right on many devices.

## The problem

Without it, program 0 can be anything on any device. GM fixes 128 sounds, 16 channels and one drum kit, which is what makes a file portable.

## Protocol or message

GM defines 128 melodic programs in 16 families of eight. Channel 10 is always drums, with keys 35 to 81 mapped to percussion. Notes run from 0 to 127. GM System On resets the device over SysEx. GM 2 adds banks, more controllers and envelope control. Program numbers in files run 0 to 127, while printed lists often show 1 to 128.

## Settings and practice

Confirm the device is in GM mode before playback. Keep drums on channel 10. Do not depend on extension sounds. Program 0 is the safest default. For exchange, write the program numbers into the metadata.

## What to listen for

A GM piano is recognisable everywhere, but brightness and tails differ. String ensembles vary most in weight. When changing sound sources, listen to drums and bass first.

## Common misunderstandings

GM is not a sound-quality standard. GM numbers are not vendor numbers. Drums on channel 10 ignore the program number.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C4", "E4", "G4", "C5"], "label": "The common floor of GM strings", "label_en": "The common floor of GM strings", "hint": "听齐奏的厚度，再想同一份文件在另一台设备上的差别", "hint_en": "Hear the unison weight, then imagine the same file on another device"}
```
:::
