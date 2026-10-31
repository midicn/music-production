---
id: mpe
site: prod
cat: B1
title: MPE 复音表达
title_en: MPE
summary: MPE 把每个音分到独立通道，让弯音、压力和音色各自随音走。
summary_en: MPE gives every note its own channel so bend, pressure and timbre follow the note.
level: standard
tags: [MIDI, MPE, 复音, 表情]
tags_en: [MIDI, MPE, polyphony, expression]
alias: [MPE, 多维复音表达, 每音弯音, polyphonic expression]
links:
  - "[[glossary:midi-protocol]]"
  - "[[instrument:violin]]"
  - "[[instrument:midi-controller]]"
instances:
  - oga-000087 | 11 个通道里弯音最密的一条有 5725 条，但 34 个音共享同一条曲线
  - oga-000327 | 14 个通道共 5848 条弯音，主音与节奏吉他各占一条通道
  - oga-000003 | 176 条弯音有 173 条在第 1 通道，150 个音一起承受
sources:
  - MPE 规范对 Zone、主通道与成员通道的约定，对照MMA 公开规范整理。
  - 每音弯音与 RPN 6 的配置方式（公开实现文档）。
updated: 2026-10-28
---

::: zh
传统通道消息由整条通道共享。和弦里想把一个音推高，其他音也会跟着弯；想让一个音变亮，整条通道都变。

## 问题

弦乐四重奏、吉他推弦、合成器独奏，都需要每个音有自己的表情。通道只有 16 个，按声部分配很快就会用完。

## 协议或消息

MPE 用一音一通道。一个 Zone 分为主通道与成员通道，主通道发全局设置，成员通道各管一个音。默认弯音范围是 48 个半音，CC74 管音色，通道压力管力度。RPN 6 用来声明 Zone 的范围。上行与下行 Zone 可以分居两端，互不干扰。

## 参数与做法

控制器与音源都要开 MPE 模式，否则弯音范围对不上。每音的表情要画在对应通道上。和弦密集时注意成员通道数量，16 个通道很快用完。录完检查通道分配，别把两个音叠进同一条。

## 听什么

和弦中单个音可以独立滑音或颤音，其他音保持不动。音色随压力变化，像每个音都有自己的呼吸。

## 常见误解

MPE 不是新协议，仍是 MIDI 1.0 消息。它不是复音触后的别名。不开 MPE 模式时，通道压力仍作用于整条通道。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"一个通道，一条表情","label_en":"One channel, one expression","hint":"听和弦共享同一条曲线，想象 MPE 把每个音分到独立通道","hint_en":"Hear the chord share one curve and imagine MPE giving each note its own channel"}
```
:::

::: en
Channel messages are shared by the whole channel. Bend one note of a chord and the others follow; brighten one note and the entire part brightens.

## The problem

A string quartet, a bent guitar note and a synth solo all need expression per note. Sixteen channels disappear quickly when each part takes one.

## Protocol or message

MPE uses one channel per note. A zone has a master channel for global settings and member channels for individual notes. The default bend range is 48 semitones, CC74 carries timbre and channel pressure carries force. RPN 6 declares the zone. Lower and upper zones can sit at opposite ends without interfering.

## Settings and practice

Enable MPE on both the controller and the sound source, or the bend ranges will disagree. Draw per-note expression on the matching channel. Watch the member count, because sixteen channels vanish fast. Check the channel map after recording so two notes never share a channel.

## What to listen for

One note in a chord can slide or vibrate while the others hold. Timbre follows pressure, as if each note had its own breath.

## Common misunderstandings

MPE is not a new protocol but MIDI 1.0 messages. It is not another name for poly aftertouch. Without MPE mode, channel pressure still affects the whole channel.

```audiolab
{"type": "instrument", "gm": "Violin", "synth": "bowed", "phrase": ["C4", "E4", "G4", "C5"], "label": "One channel, one expression", "label_en": "One channel, one expression", "hint": "听和弦共享同一条曲线，想象 MPE 把每个音分到独立通道", "hint_en": "Hear the chord share one curve and imagine MPE giving each note its own channel"}
```
:::
