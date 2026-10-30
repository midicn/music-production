---
id: midi-and-daw
site: prod
cat: B1
title: MIDI 与 DAW 的交互
title_en: MIDI and the DAW
summary: DAW 把 MIDI 文件拆成轨，再按端口与通道送到音源，轨道只是视图。
summary_en: A DAW turns a MIDI file into tracks, then routes them by port and channel; a track is only a view.
level: standard
tags: [MIDI, DAW, 轨道, 导入]
tags_en: [MIDI, DAW, track, import]
alias: [DAW 交互, MIDI 导入, 轨道映射, SMF 导入]
links:
  - "[[glossary:daw]]"
  - "[[instrument:sequencer]]"
  - "[[glossary:midi-protocol]]"
instances:
  - oga-000077 | 32 条轨塞进 15 个通道，31 次音色切换，没有任何 CC
  - pdmx-000799 | 43 条轨、15 个通道、40 处速度变化，导入后最容易看出轨与通道的差别
  - pdmx-000594 | 47 条轨共用 15 个通道，63 次音色切换分布在整曲
sources:
  - SMF 规范对格式 0 与格式 1 的区分，依 MMA 公开规范核查，未抄文本
  - DAW 导入导出时的轨与通道路由规则，依通行软件文档核查，未抄文本
updated: 2026-10-28
---

::: zh
同一份文件导入两台 DAW，轨数可能不同，声部也可能错位。有人以为一条轨就是一个通道，导出之后就乱了。

## 问题

轨是文件的组织单位，通道是消息的地址。两者混为一谈，鼓轨会落到钢琴上，两条弦乐会共用一条表情曲线，速度变化也会整体偏移。

## 协议或消息

SMF 0 把所有事件塞进一条轨，SMF 1 按轨分装再共享时间轴。DAW 导入时按轨建轨，输出时再映射到端口与通道。速度变化写在 Tempo Map，连续控制器需要追捕，否则播放头落在中间时状态不对。多端口时，轨道还要记住自己输出到哪一个端口。

## 参数与做法

导入后先看轨数与通道表。鼓轨固定第 10 通道。多端口时给每轨标清输出。导出前决定用格式 0 还是 1，交换用 1，老设备用 0。别把轨名里的通道号当成唯一依据。

## 听什么

轨道映射错，钢琴会落到鼓组，或两个声部共用一条表情曲线。速度图错位，整段会提前或延后。

## 常见误解

轨数不等于通道数。DAW 的乐器轨不等于 MIDI 轨。导入时的颜色与顺序不携带音乐信息。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","G3","C4","E4"],"label":"轨道只是视图","label_en":"A track is only a view","hint":"听这段音乐，再想 32 条轨如何映射到 16 个通道","hint_en":"Hear the phrase and picture 32 tracks mapping onto 16 channels"}
```
:::

::: en
The same file can import with different track counts, and parts can land in the wrong place. Treating one track as one channel breaks on export.

## The problem

A track is an organising unit, while a channel is an address inside a message. Confusing them sends drums to a piano, shares one curve across two parts, and shifts the tempo map.

## Protocol or message

SMF 0 puts every event in one track; SMF 1 splits by track and shares a timeline. A DAW builds tracks on import, then maps them to ports and channels. Tempo changes live in the tempo map, and continuous controllers need chase so a mid-file start still has the right state. With several ports, each track must remember its destination.

## Settings and practice

Check the track and channel table after import. Keep drums on channel 10. Label the output port when several are in use. Choose format 0 or 1 before export, 1 for exchange and 0 for old gear. Never treat a track name as the only channel clue.

## What to listen for

A wrong map sends piano to the drums, or makes two parts share one expression curve. A misplaced tempo map moves the whole passage earlier or later.

## Common misunderstandings

Track count is not channel count. An instrument track is not a MIDI track. Colours and order in the DAW carry no musical data.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C3", "G3", "C4", "E4"], "label": "A track is only a view", "label_en": "A track is only a view", "hint": "听这段音乐，再想 32 条轨如何映射到 16 个通道", "hint_en": "Hear the phrase and picture 32 tracks mapping onto 16 channels"}
```
:::
