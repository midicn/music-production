---
id: clock-master-slave
site: prod
cat: B2
title: 时钟源与主从
title_en: Clock Source and Master-Slave
summary: 多台设备共用一条时间基准，只能有一个主时钟。
summary_en: Several devices can share one time base, but only one of them may be the master clock.
level: standard
tags: [音序, 时钟, 同步, MIDI]
tags_en: [sequencing, clock, sync, MIDI]
alias: [时钟源, 主从时钟, 主时钟, clock source, master clock, slave]
links:
  - "[[glossary:midi-protocol]]"
  - "[[glossary:sample-rate]]"
  - "[[instrument:sequencer]]"
instances:
  - groove-001103 | 迪斯科的四拍脉冲，速度稳定到可以当基准
  - atepp-000195 | 自由速度的钢琴独奏，无法跟随固定时钟
  - mutopia-001330 | 多声部合奏，各声部必须共用一条时间线
sources:
  - MIDI 时钟的二十四拍分辨率与字时钟定义，依 MIDI 规范核查，未抄文本
  - 主从同步链路与漂移的排查方法，依录音棚工程通识核查，未抄文本
updated: 2026-10-28
---

::: zh
多台设备一起工作时，只能有一个时钟源，其余设备跟随它走。

## 问题

音源、鼓机、音频接口各有自己的晶振，频率不会完全一致。两台设备各走各的时钟，几分钟后就会错开，录进来的音轨对不上。

## 原理

主设备发出时钟脉冲，从设备按脉冲推进。MIDI 时钟每四分音符发二十四拍，精度到消息级；字时钟是音频采样的节拍；两者解决的对象不同。主从链越长，累积的抖动越多。

## 做法与参数

只设一个主时钟，通常让音频接口当主，DAW 跟随外部时钟；从设备切到外部同步并确认采样率一致；避免把多台设备串成过长的链，能用分配器就用分配器；录音前先跑一分钟，检查有没有漂移。

## 听什么

两台设备漂移时，同一材料会慢慢出现梳状滤波般的金属声。稳定时声像不动，不稳定时高频会周期性摆动。

## 常见误解

MIDI 时钟不传音频，字时钟也不传音符。设备越多不代表同步越好，主从关系混乱才是常见故障源。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q q q q","bpm":120,"label":"一台机器的脉冲","label_en":"Pulse from one machine","hint":"听它有多稳，再想第二台设备如何跟上","hint_en":"Hear its steadiness, then how a second device follows"}
```
:::

::: en
When several devices play together, only one can be the clock source and the rest must follow it.

## The problem

Synths, drum machines and audio interfaces each run on their own crystal, and the frequencies never match exactly. Two free-running clocks drift apart within minutes, and the recorded tracks no longer line up.

## How it works

A master sends pulses and slaves advance on them. MIDI clock sends twenty-four pulses per quarter note and works at message resolution; word clock is the beat of audio samples. They solve different problems, and a longer master-slave chain accumulates more jitter.

## Settings and practice

Set one master, usually the audio interface, with the DAW following external clock. Switch slaves to external sync and confirm matching sample rates. Avoid long chains and use a distributor where possible. Run for a minute before recording and check for drift.

## What to listen for

Drift between two devices adds a metallic, comb-filtered colour to the same material. When locked, the image stays still; when not, high frequencies sway periodically.

## Common misunderstandings

MIDI clock carries no audio, and word clock carries no notes. More devices do not improve sync; confused master-slave roles are the usual fault.

```audiolab
{"type": "rhythm", "sig": "4/4", "pattern": "q q q q", "bpm": 120, "label": "Pulse from one machine", "label_en": "Pulse from one machine", "hint": "听它有多稳，再想第二台设备如何跟上", "hint_en": "Hear its steadiness, then how a second device follows"}
```
:::
