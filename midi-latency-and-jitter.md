---
id: midi-latency-and-jitter
site: prod
cat: B1
title: MIDI 延迟与抖动
title_en: MIDI Latency and Jitter
summary: 延迟是消息到达晚，抖动是每次晚得不一样；两者都改变律动。
summary_en: Latency is a message arriving late; jitter is each arrival being late by a different amount.
level: standard
tags: [MIDI, 延迟, 抖动, 缓冲]
tags_en: [MIDI, latency, jitter, buffer]
alias: [MIDI 延迟, 抖动, jitter, 回环延迟]
links:
  - "[[glossary:latency]]"
  - "[[glossary:midi-protocol]]"
  - "[[glossary:latency-compensation]]"
  - "[[instrument:software-synth]]"
instances:
  - musicnet-000315 | 演奏的微时间写成 2647 条速度事件，落点本来就不在网格上
  - groove-000693 | 100 BPM 的鼓循环只有 5.5% 的音落在十六分网格，律动靠偏移
  - pdmx-000799 | 21709 个音符里不到一半对齐十六分网格，速度变化有 40 处
sources:
  - MIDI 1.0 串行速率与 USB MIDI 类帧长的公开定义——依据来自规范。
  - 本库文件的音符落点统计，由本地 SMF 解析脚本核对，数值随文件而定
updated: 2026-10-28
---

::: zh
软音源按下键盘有拖尾，录音后音符整体偏后，或前后不稳。多半不是音源慢，而是链路与缓冲。

## 问题

延迟与抖动常被混为一谈。前者让整段一起晚，后者让每个音晚得不同。前者可以补偿，后者只能减小。

## 协议或消息

MIDI 1.0 的串行速率是 31250 比特每秒，一个字节约 320 微秒，一条三字节消息接近 1 毫秒。USB MIDI 1.0 类按 1 毫秒帧打包，驱动再打时间戳。延迟来自缓冲、驱动与音频接口；抖动来自帧对齐与系统调度。时钟抖动会让跟随设备忽快忽慢。

## 参数与做法

先测回环延迟，再调缓冲。录音时用直接监听，或开启延迟补偿。不要把缓冲区压到爆音。多设备级联时把最慢的一台放末端。时钟只留一个主源。

## 听什么

整体偏后像拖拍，抖动像鼓手不稳。低频与鼓点最敏感，几毫秒就能听出松。

## 常见误解

延迟不是音源的问题。降低缓冲不总是更好。MIDI 时间戳不等于音频采样位置。

```audiolab
{"type":"rhythm","sig":"4/4","bpm":100,"pattern":"q e e q e e","label":"网格之外的那几毫秒","label_en":"The milliseconds off the grid","hint":"跟节拍器数，听落点是否整齐","hint_en":"Count with the click and hear whether the attacks sit evenly"}
```
:::

::: en
A software instrument feels sluggish, a recording lands behind the beat, or notes drift. The cause is often the chain and the buffer, not the sound engine.

## The problem

Latency and jitter are easily confused. The first moves a whole passage late, the second makes every note late by a different amount. One can be compensated, the other only reduced.

## Protocol or message

MIDI 1.0 runs at 31,250 bits per second, so one byte takes about 320 microseconds and a three-byte message nearly a millisecond. USB MIDI 1.0 class packets travel in one-millisecond frames, and the driver adds timestamps. Latency comes from buffers, drivers and the audio interface; jitter comes from frame alignment and scheduling. Clock jitter makes a follower drift.

## Settings and practice

Measure loopback delay before changing the buffer. Use direct monitoring or delay compensation while recording. Do not crush the buffer until it clicks. Put the slowest device last in a chain. Keep one clock master.

## What to listen for

A constant offset sounds like dragging; jitter sounds like an unsteady drummer. Bass and kick reveal it first, where a few milliseconds already feel loose.

## Common misunderstandings

Latency is not the sound source's fault. A smaller buffer is not always better. A MIDI timestamp is not an audio sample position.

```audiolab
{"type": "rhythm", "sig": "4/4", "bpm": 100, "pattern": "q e e q e e", "label": "The milliseconds off the grid", "label_en": "The milliseconds off the grid", "hint": "跟节拍器数，听落点是否整齐", "hint_en": "Count with the click and hear whether the attacks sit evenly"}
```
:::
