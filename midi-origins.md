---
id: midi-origins
site: prod
cat: B1
title: MIDI 的由来
title_en: How MIDI Began
summary: 1983 年定下的串行协议，用三字节讲清音高、力度与开关。
summary_en: A serial agreement from 1983 that describes pitch, touch and switches in three bytes.
level: standard
tags: [MIDI, 历史, 协议, 1983]
tags_en: [MIDI, history, protocol, 1983]
alias: [MIDI 由来, MIDI 历史, 1983, MIDI 1.0]
links:
  - "[[glossary:midi-protocol]]"
  - "[[glossary:synthesizer]]"
  - "[[period:contemporary]]"
instances:
  - oga-000297 | 格式 0 单轨文件，5 个通道 1081 个音符，仍是 1983 年的消息骨架
  - groove-000007 | 单轨鼓循环，210 个音符全靠 Note On 与 Note Off 说清
  - pdmx-000799 | 格式 1 的 43 条轨，15 个通道共用同一套三字节语法
sources:
  - MIDI 1.0 规范对物理层、串行速率与消息格式的定义，依 MMA 公开规范核查，未抄文本
  - 1983 年规范发布前后的行业协作背景，依公开技术史料核查，未抄文本
updated: 2026-10-28
---

::: zh
MIDI 不是音源，也不是文件格式，而是一份关于怎样把演奏动作说清楚的约定。1983 年之前，各家合成器用各自的接口，互相对不上。

## 问题

两台设备要一起演奏，先得对齐电压、扫描方式与时间单位。没有共同语言，音高与力度只能靠耳朵和手去凑，换一台机器就要重来。

## 协议或消息

1981 年 Sequential Circuits 提出方案，1983 年 MIDI 1.0 规范由 MMA 与 JMSC 发布。物理层是 5 针 DIN 电流环，31250 比特每秒，接收端用光耦隔离。数据字节只有 7 位，最高位留给状态。音符、力度、音色切换与时钟，都在同一根线上排队。16 个通道让一台控制器分派多个声部。

## 参数与做法

MIDI OUT 接 MIDI IN，THRU 只转发不加工。链路过长会累积延迟，超过三台就改用分配器。两台设备争当主时钟时，只留一个时钟源。老设备只认通道消息，别急着发 SysEx。

## 听什么

同一份演奏换到另一台音源，音高与节拍仍在，音色与力度曲线会变。协议保住了动作，保不住声音。

## 常见误解

MIDI 不是音频，线里没有声音。MIDI 文件也不是波形文件。1983 年的消息今天仍在用，新版只是加宽了数值。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5"],"label":"三字节里的演奏","label_en":"A performance in three bytes","hint":"听音头，再想 1983 年的接收器也收到同样的状态、键号与力度","hint_en":"Hear the attack, then picture a 1983 receiver getting the same status, key and velocity"}
```
:::

::: en
MIDI is neither a sound nor a file format but an agreement about describing performance actions. Before 1983, every synth had its own interface.

## The problem

Two devices had to agree on voltage, scanning and time. Without a shared language, pitch and touch were matched by ear, and every new machine started over.

## Protocol or message

Sequential Circuits proposed a scheme in 1981, and MIDI 1.0 appeared in 1983 from the MMA and JMSC. Its physical layer is a five-pin DIN current loop at 31,250 bits per second, isolated by an opto-coupler. Data bytes carry seven bits, the top bit reserved for status. Notes, velocity, program changes and clock queue on one wire. Sixteen channels let a controller address several parts.

## Settings and practice

Connect MIDI OUT to MIDI IN; THRU forwards unchanged. Long chains accumulate delay, so use a splitter beyond three devices. When two devices want to be clock master, keep one source. Old gear understands channel messages, so skip SysEx at first.

## What to listen for

Move the performance to another sound source and pitch and tempo remain, while timbre and the velocity curve change. The protocol preserves the action, not the sound.

## Common misunderstandings

MIDI is not audio and the cable carries no sound. A MIDI file is not a waveform. Messages from 1983 still work, and newer versions widen the numbers.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "C5"], "label": "A performance in three bytes", "label_en": "A performance in three bytes", "hint": "听音头，再想 1983 年的接收器也收到同样的状态、键号与力度", "hint_en": "Hear the attack, then picture a 1983 receiver getting the same status, key and velocity"}
```
:::
