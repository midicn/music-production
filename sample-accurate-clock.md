---
id: sample-accurate-clock
site: prod
cat: B2
title: 采样精度时钟
title_en: Sample-Accurate Clock
summary: 音频事件落在采样格上，精度远高于 MIDI 时钟。
summary_en: Audio events land on the sample grid, far more precisely than any MIDI clock.
level: standard
tags: [音序, 时钟, 采样率, 同步]
tags_en: [sequencing, clock, sample rate, sync]
alias: [采样精度, 采样时钟, 采样级对齐, sample accurate, sample clock, sample accuracy]
links:
  - "[[glossary:sample-rate]]"
  - "[[glossary:automation]]"
  - "[[glossary:midi-protocol]]"
instances:
  - groove-001104 | 迪斯科电子鼓组，四拍位置按网格排列
  - groove-000664 | 新奥尔良鼓循环，底鼓与军鼓的叠层关系清楚
  - atepp-002441 | 钢琴演奏的速度与力度连续变化，适合观察网格外的偏差
sources:
  - 采样间隔与 MIDI 消息传输时间的换算；数字音频与 MIDI 规范是主要依据。
  - 叠层对齐与采样级淡化的做法——依据来自混音工程惯例。
updated: 2026-10-28
---

::: zh
音频的每一次采样都由采样时钟定位，事件落在哪一个采样点，决定了它有多准。

## 要解决的事

两条同样的底鼓叠在一起，若起点差了几个采样，低频会互相抵消。MIDI 的时间精度比采样网格粗得多，靠它对齐只能做到毫秒级。

## 工作方式

四十四点一千赫兹下，一个采样间隔是二十二点七微秒。音频事件按采样格调度，自动化曲线也按采样点写入。MIDI 一个三字节消息在三十一点二五千波特下要占近一毫秒，多个消息还会排队。

## 旋钮与做法

让音频接口提供主时钟；叠层音色用采样级对齐，放大波形看第一个峰；淡入淡出写到采样级，避免阶梯噪声；缓冲区只影响监听延迟，不改变网格精度；需要精确对齐时先渲染再微调。

## 耳朵要抓的点

叠层底鼓发闷或发薄，常是相位差而不是音色差。把其中一轨前后移动一个采样，低频的厚度会立刻变化。

## 容易弄错的

提高采样率不能消除 MIDI 抖动；减小缓冲区也不会让 MIDI 消息更准。采样精度描述的是音频网格，不是所有输入的时间质量。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s","bpm":120,"label":"采样网格上的短脉冲","label_en":"Short pulses on the sample grid","hint":"每一击都落在同样的采样位置","hint_en":"Every hit lands on the same sample position"}
```
:::

::: en
Every audio sample is placed by the sample clock, and which sample an event lands on decides how precise it is.

## The problem to solve

Two identical kicks stacked with a start difference of a few samples cancel low frequencies. MIDI timing is far coarser than the sample grid, so aligning with it only reaches the millisecond range.

## The working principle

At forty-four point one kilohertz one sample lasts twenty-two point seven microseconds. Audio events and automation points are scheduled on the sample grid. A three-byte MIDI message takes nearly a millisecond at thirty-one point two five kilobaud, and messages queue behind each other.

## Settings and practice

Let the audio interface supply the master clock. Align layered sounds at sample level by zooming into the first peak, and write fades at sample resolution to avoid stair-step noise. Buffer size changes monitoring latency, not grid precision. Render before fine alignment when precision matters.

## What the ear catches

A stacked kick that sounds dull or thin is often a phase difference, not a timbre difference. Nudge one track by a single sample and the low end changes at once.

## Common misunderstandings

A higher sample rate does not remove MIDI jitter, and a smaller buffer does not make MIDI messages more accurate. Sample accuracy describes the audio grid, not the timing quality of every input.

```audiolab
{"type": "rhythm", "sig": "4/4", "pattern": "s s s s s s s s", "bpm": 120, "label": "Short pulses on the sample grid", "label_en": "Short pulses on the sample grid", "hint": "每一击都落在同样的采样位置", "hint_en": "Every hit lands on the same sample position"}
```
:::
