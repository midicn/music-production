---
id: gs-and-xg
site: prod
cat: B1
title: GS 与 XG 扩展
title_en: GS and XG Extensions
summary: GS 与 XG 在 GM 之上扩展音色库、鼓组与效果，复位方式各不相同。
summary_en: GS and XG extend GM with banks, drum kits and effects, each with its own reset.
level: standard
tags: [MIDI, GS, XG, 音色库]
tags_en: [MIDI, GS, XG, sound bank]
alias: [GS, XG, Roland GS, Yamaha XG, 扩展音色]
links:
  - "[[glossary:midi-protocol]]"
  - "[[instrument:digital-piano]]"
  - "[[instrument:drum-kit]]"
instances:
  - musicnet-000300 | 开头 GM System On 之后紧跟 GS 复位，弦乐分到 40 到 43 号音色
  - musicnet-000301 | 同一组复位，18 条轨只用 5 个通道，弦乐仍按 GS 分声部
  - musicnet-000302 | 复位后低音提琴通道在 43 与 45 号音色之间往返
sources:
  - Roland GS 复位与 Yamaha XG System On 的字节序列——依据来自公开规范。
  - GM System On 与库选择控制器的约定，对照通用 MIDI 规范整理。
updated: 2026-10-28
---

::: zh
GM 只保证 128 个音色，编制一大就不够用。GS 与 XG 都想解决这件事，却各自修了一条路。

## 问题

同一个音色号，在 GS 设备上是弦乐，在 XG 设备上可能变成别的东西。文件没有写库号与复位，换一台音源就面目全非。

## 协议或消息

两者都先用 CC0 与 CC32 选库，再发 Program Change。GS 是 Roland 的扩展，增加声部、鼓组与效果参数，复位是 F0 41 10 42 12 40 00 7F 00 41 F7。XG 是 Yamaha 的扩展，用系统块管理音色、鼓组与效果，复位是 F0 43 10 4C 00 00 7E 00 F7。GM 复位是 F0 7E 7F 09 01 F7，三者不能混用。

## 参数与做法

文件开头先发 GM System On，再发目标扩展的复位，顺序反了音源会回到默认。选音色时先写库号，再写音色号，缺一项就会落到另一件乐器。跨设备前查清对方支持哪一级扩展，也要确认鼓组编号是否一致。不要假设 GS 的库号在 XG 上同义。

## 听什么

同一段弦乐，GS 与 XG 的默认混响与音头不同。复位发错，鼓组会落到旋律音色上，镲片变成钢琴键。

## 常见误解

GS 不是 GM 的同义词。XG 不是 GS 的升级。复位只改设置，不改文件里的音符。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","B4"],"label":"复位之后的弦乐","label_en":"Strings after a reset","hint":"听齐奏的混响，再想 GS 复位把空间与音色库改回默认","hint_en":"Hear the section reverb and imagine a GS reset returning space and bank to default"}
```
:::

::: en
GM guarantees 128 sounds, thin for a large arrangement. GS and XG both attack the limit, each along its own road.

## The problem

The same program can be strings on GS and something else on XG. Without bank numbers and a reset in the file, changing the sound source changes everything.

## Protocol or message

Both select a bank with CC0 and CC32 before Program Change. GS is Roland's extension, adding parts, drum kits and effect parameters, reset by F0 41 10 42 12 40 00 7F 00 41 F7. XG is Yamaha's, managing voices, kits and effects through system blocks, reset by F0 43 10 4C 00 00 7E 00 F7. The GM reset is F0 7E 7F 09 01 F7, and the three do not interchange.

## Settings and practice

Send GM System On at the top of a file, then the reset of the target extension. Write the bank before the program number. Check which extension a device supports before exchange. Never assume a GS bank means the same on XG.

## What to listen for

The same string passage has a different default reverb and attack under GS and XG. A wrong reset drops the drum kit onto a melodic program, turning cymbals into piano keys.

## Common misunderstandings

GS is not a synonym for GM. XG is not an upgrade of GS. A reset changes settings, not the notes in the file.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C4", "E4", "G4", "B4"], "label": "Strings after a reset", "label_en": "Strings after a reset", "hint": "听齐奏的混响，再想 GS 复位把空间与音色库改回默认", "hint_en": "Hear the section reverb and imagine a GS reset returning space and bank to default"}
```
:::
