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
  - https://midi.org/general-midi-level-1
  - https://midi.org/general-midi
  - 通用 MIDI 一级规范对音色表与通道的约定——依据来自 MMA 公开规范。
  - GM 2 增加的音色库与控制器，对照通用 MIDI 规范整理。
updated: 2026-11-03
---

::: zh
GM 是一份最小共同约定，让同一份文件在不同设备上大致可听。

## 问题

没有约定，0 号音色在每台设备上可以是任何东西。GM 把 128 个音色、16 个通道与一套鼓固定下来，文件才有可交换性。

## 协议或消息

GM 规定 128 个旋律音色，按 16 个族排列，每族 8 个。通道 10 固定为鼓组，键号 35 到 81 对应打击乐器。音符编号 0 到 127。GM System On 用 SysEx 复位。GM 2 增加音色库、更多的 CC 与包络控制。文件里的音色号是 0 到 127，人读的列表常写成 1 到 128。

## 参数与做法

播放前确认设备处于 GM 模式。鼓固定在第 10 通道。不要依赖扩展音色。按声部选择对应的 GM 音色，不要把所有声部都改成钢琴。将所需 Program Change 写在对应通道首个音符之前，并注明软件使用 0–127 还是 1–128 编号；说明文件中的文字音色名不能代替实际消息。交付前在目标播放器回放，检查旋律音色和鼓键映射。

## 听什么

GM 钢琴在哪台设备上都认得出，但亮度与尾音不同；弦乐齐奏的厚度差异最大。同一份文件换音源，先听鼓与贝斯。鼓的键号在 GM 下含义固定，换音源也不改语义。

## 常见误解

GM 规定兼容行为与音色名称，不规定具体采样或音质。这里的固定鼓映射以 GM 1 为边界；GM 2、GS、XG 的鼓组选择与扩展行为应另查相应规范。

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

Confirm the device is in GM mode before playback. Keep drums on channel 10. Do not depend on extension sounds. Choose the GM program appropriate to each part instead of replacing every part with piano. Place Program Change messages before the first note on the relevant channel and state whether the software uses 0–127 or 1–128 numbering. A written instrument name does not replace the actual message. Verify melodic sounds and drum mappings in the receiving player.

## What to listen for

A GM piano is recognisable everywhere, but brightness and tails differ. String ensembles vary most in weight. When changing sound sources, listen to drums and bass first.

## Common misunderstandings

GM specifies compatible behavior and sound names, not a particular sample set or sound quality. The fixed drum-map discussion here concerns GM 1; consult the relevant specification for GM 2, GS or XG kit-selection behavior.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C4", "E4", "G4", "C5"], "label": "The common floor of GM strings", "label_en": "The common floor of GM strings", "hint": "听齐奏的厚度，再想同一份文件在另一台设备上的差别", "hint_en": "Hear the unison weight, then imagine the same file on another device"}
```
:::
