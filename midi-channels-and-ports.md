---
id: midi-channels-and-ports
site: prod
cat: B1
title: MIDI 通道与端口
title_en: MIDI Channels and Ports
summary: 16 个通道组成一个端口，轨道数与通道数从来不是一回事。
summary_en: Sixteen channels make one port, and track count is never the same thing as channel count.
level: standard
tags: [MIDI, 通道, 端口, 鼓]
tags_en: [MIDI, channel, port, drums]
alias: [MIDI 通道, 端口, 通道与端口, channel, port]
links:
  - "[[glossary:midi-protocol]]"
  - "[[glossary:daw]]"
  - "[[instrument:drum-kit]]"
instances:
  - oga-000003 | 16 个通道都收到设置消息，实际只有 4 个通道发声，全部装在 5 条轨里
  - oga-000077 | 32 条轨挤进 16 个通道，鼓固定在第 10 通道
  - oga-000025 | 16 个通道各有音色，第 10 通道打了 1300 个鼓音
sources:
  - MIDI 1.0 规范的通道消息与端口概念，对照 MMA 公开规范整理。
  - GM 对第 10 通道的鼓组约定（通用 MIDI 规范）。
updated: 2026-10-28
---

::: zh
通道是消息的地址，端口是通道的容器。两者都数得清，却经常被混为一谈。

## 问题

声部一多，16 个通道就不够用。有人把两条轨指向同一通道，结果一轨的推子带动另一轨；也有人以为换端口就能自动分开通道。

## 协议或消息

一个端口有 16 个通道，编号 0 到 15。GM 规定第 10 通道为鼓。端口可以是 DIN 接口、USB 接口或虚拟端口，每个端口独立计数，因此不同端口可以有相同的通道号。Omni 打开时接收所有通道。轨道是文件里的组织单位，通道是消息里的地址，两者不必相等。

## 参数与做法

每个声部固定通道，鼓留 10。多端口时在工程里标清端口。虚拟回环用来连接两个软件。避免两轨同通道同音区。16 个通道不够时，优先拆端口，而不是让声部共用。

## 听什么

两轨共用通道，一轨的 CC7 会改另一轨的音量；鼓落到 1 号通道，会变成钢琴键。

## 常见误解

轨道数不等于通道数。第 10 通道不是第十轨。USB 不等于无限通道。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","G3","C4","E4"],"label":"一条通道，一条地址","label_en":"One channel, one address","hint":"听和弦，再想每个音都带着同一个通道号","hint_en":"Hear the chord, then picture every note carrying the same channel number"}
```
:::

::: en
A channel is the address inside a message, and a port is the container for channels. Both can be counted, yet they are often confused.

## The problem

With many parts, sixteen channels run out. Two tracks aimed at one channel mean one fader moves the other, while changing ports is expected to separate channels automatically.

## Protocol or message

A port holds 16 channels, numbered 0 to 15. GM fixes channel 10 to drums. A port can be a DIN socket, a USB connection or a virtual port, and each counts separately, so the same channel number can appear on two ports. Omni mode receives every channel. A track is an organising unit in a file, a channel is an address in a message, and the two need not match.

## Settings and practice

Give each part its own channel and leave 10 for drums. Label ports in the project when more than one is in use. Virtual loopbacks connect two programs. Avoid two tracks sharing a channel and register. When sixteen channels run out, add a port instead of sharing.

## What to listen for

When two tracks share a channel, one track's CC7 changes the other's level. A drum part sent to channel 1 turns into piano keys.

## Common misunderstandings

Track count is not channel count. Channel 10 is not the tenth track. USB does not mean unlimited channels.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C3", "G3", "C4", "E4"], "label": "One channel, one address", "label_en": "One channel, one address", "hint": "听和弦，再想每个音都带着同一个通道号", "hint_en": "Hear the chord, then picture every note carrying the same channel number"}
```
:::
