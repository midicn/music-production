---
id: virtual-ports-and-loopback
site: prod
cat: B1
title: 虚拟端口与回环
title_en: Virtual Ports and Loopback
summary: 虚拟端口在系统内造出 MIDI 线，回环把输出接回输入，方便软件互连。
summary_en: A virtual port is a MIDI cable inside the system, and a loopback returns an output to an input.
level: standard
tags: [MIDI, 虚拟端口, 回环, 路由]
tags_en: [MIDI, virtual port, loopback, routing]
alias: [虚拟 MIDI 端口, 回环, loopback, IAC]
links:
  - "[[glossary:midi-protocol]]"
  - "[[glossary:daw]]"
  - "[[instrument:software-synth]]"
instances:
  - pdmx-002317 | 16 个通道全满，30 条轨共用，第二个端口才有分流余地
  - pdmx-000143 | 31 条轨铺在 16 个通道上，端口元事件逐轨出现
  - pdmx-000799 | 43 条轨只用 15 个通道，合并时通道号最容易相撞
sources:
  - 操作系统虚拟 MIDI 端点与回环的通行做法，依公开驱动文档核查，未抄文本
  - 端口元事件与多端口寻址的约定，依 SMF 规范核查，未抄文本
updated: 2026-10-28
---

::: zh
两个软件都想当主机，或一台电脑要同时跑音序器与音源，物理接口就不够用。虚拟端口解决连线，回环解决自测。

## 问题

没有端口，软件之间只能靠导出文件传递。端口名选错，消息会进了另一个程序；回环接错，输出又回到自己，音符越积越多。

## 协议或消息

虚拟端口是驱动在系统内注册的 MIDI 端点，一端出现在发送方，另一端出现在接收方。回环是把输出端直接接到输入端，消息原样返回。每个端口仍只有 16 个通道，端口名就是路由地址。合并会把多条流叠进一个端口，通道号相同的消息会相撞。

## 参数与做法

先建端口，再在两端选同一个名字。回环测试时发一个音，看是否只回来一次。多个软件共用时给端口加前缀。需要更多通道就加端口，不要把全部声部压进 16 个通道。关闭不用的端口，减少轮询。

## 听什么

回环接错会形成消息风暴，音符越积越多。端口选错，推子会控制到另一条轨。

## 常见误解

虚拟端口不是插件。回环不是录音。端口数不等于通道数。

```audiolab
{"type":"instrument","gm":"Electric Piano 1","synth":"struck","phrase":["C4","E4","G4","B4"],"label":"两条线，两个世界","label_en":"Two lines, two worlds","hint":"听分层，再想它们本可以来自两个端口","hint_en":"Hear the layers and picture them arriving on two ports"}
```
:::

::: en
Two programs both want to be host, or a sequencer and a sound source share one computer. Virtual ports replace cables, and loopbacks make self-tests possible.

## The problem

Without ports, programs can only exchange files. A wrong port name sends messages into another application, while a miswired loopback returns the output to itself until notes pile up.

## Protocol or message

A virtual port is an endpoint registered by a driver, visible to a sender at one end and a receiver at the other. A loopback connects an output straight to an input, returning messages unchanged. Each port still holds sixteen channels, and the port name is the routing address. Merging stacks several streams into one port, where identical channel numbers collide.

## Settings and practice

Create the port first, then pick the same name at both ends. Send one note through a loopback and confirm it returns once. Prefix port names when several programs share them. Add a port when channels run out instead of squeezing every part into sixteen. Close unused ports to cut polling.

## What to listen for

A miswired loopback creates a message storm as notes pile up. A wrong port makes a fader move another track.

## Common misunderstandings

A virtual port is not a plug-in. A loopback is not a recording. Port count is not channel count.

```audiolab
{"type": "instrument", "gm": "Electric Piano 1", "synth": "struck", "phrase": ["C4", "E4", "G4", "B4"], "label": "Two lines, two worlds", "label_en": "Two lines, two worlds", "hint": "听分层，再想它们本可以来自两个端口", "hint_en": "Hear the layers and picture them arriving on two ports"}
```
:::
