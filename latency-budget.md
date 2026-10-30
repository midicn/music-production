---
id: latency-budget
site: prod
cat: B5
title: 延迟预算
title_en: Latency Budget
summary: 输入、处理、输出三段延迟相加，决定演奏跟手与否。
summary_en: Input, processing and output buffers add up to a round-trip delay that decides whether playing feels immediate.
level: standard
tags: [延迟, 缓冲, 监听, 演奏]
tags_en: [latency, buffering, monitoring, performance]
alias: [延迟, 往返延迟, 监听延迟, round-trip latency]
links:
  - "[[glossary:latency]]"
  - "[[glossary:buffer-size]]"
  - "[[glossary:latency-compensation]]"
instances:
  - thesession-000083 | 里尔舞曲速度快、装饰音密，监听延迟一大就拖拍（C1）
  - groove-000000 | 138 BPM 的十六分音符间隔约 109 毫秒，往返延迟占多少一算便知（C1）
  - oga-000005 | 战斗曲切分重音多，边弹边听时延迟会让重音落到拍后（C1）
sources:
  - 缓冲、采样率与往返延迟的换算，依音频接口厂商公开资料核查，未抄文本
  - 监听距离与声速的关系，依声学通识核查，未抄文本
updated: 2026-10-28
---

::: zh
## 问题

按下琴键到听见声音，中间要经过输入缓冲、插件处理与输出缓冲。三段相加就是往返延迟，超过一二十毫秒，演奏者会觉得声音落在手后面。

## 原理

缓冲按块处理，块大小除以采样率就是一块的时间。48 kHz 下 256 个样点约 5.3 毫秒，往返约 10.7 毫秒，加上转换器与驱动开销常到 15 到 20 毫秒。声学乐器本身也有延迟，钢琴击弦到出声、管风琴管道充气都要时间，监听距离每米约 2.9 毫秒。延迟是一笔预算。

## 参数与做法

录音时把缓冲降到 64 到 128 个样点，混音时放宽到 256 到 512。能用硬件直接监听就绕开软件通路。测量实际往返延迟，不要只看设置面板。重插件用冻结或渲染。换接口后重新测。

## 听什么

在里尔舞曲的装饰音上听跟手程度，在 138 BPM 的放克鼓循环里数十六分音符的间隔，在战斗曲的切分重音上听重音是否落到拍后。延迟大时演奏者会不自觉赶拍，听起来反而更急。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":138,"label":"138 BPM 的十六分音符","label_en":"Sixteenths at 138 BPM","hint":"每一格约 109 毫秒，往返延迟占几格一听便知","hint_en":"Each step is about 109 ms, so count how many steps the round trip eats"}
```

## 常见误解

缓冲越小越好，太小会欠载爆音。延迟不只影响录音，混音时推子与旋钮的响应也受影响。USB 麦克风不一定延迟大，取决于驱动与缓冲。延迟补偿只对齐已录素材，不能消除监听延迟。
:::

::: en
## The question

From key press to speaker, sound passes input buffering, plug-in processing and output buffering. They add up to a round-trip delay; past ten or twenty milliseconds, playing feels behind the hand.

## How it works

Buffers work in blocks; block size divided by sample rate gives one block's time. At 48 kHz, 256 samples last about 5.3 ms, so a round trip is about 10.7 ms, while converter and driver overhead push it to 15 or 20 ms. Acoustic instruments carry their own delay, and each metre of monitoring distance adds about 2.9 ms. Latency is a budget.

## Settings and practice

Drop the buffer to 64 or 128 samples when tracking and relax to 256 or 512 when mixing. Use hardware direct monitoring to bypass the software path. Measure the real round trip rather than trusting a settings panel, then re-measure after changing interfaces.

## What to listen for

On a reel, hear how ornaments sit under the fingers. In a 138 BPM funk loop, count the sixteenth-note spacing. Too much delay makes a player rush, which sounds hurried.

```audiolab
{"type": "rhythm", "sig": "4/4", "pattern": "s s s s s s s s s s s s s s s s", "bpm": 138, "label": "Sixteenths at 138 BPM", "label_en": "Sixteenths at 138 BPM", "hint": "每一格约 109 毫秒，往返延迟占几格一听便知", "hint_en": "Each step is about 109 ms, so count how many steps the round trip eats"}
```

## Common misconceptions

Smaller buffers are not always better, because too small causes dropouts. Latency affects mixing too, in fader and knob response. A USB microphone is not necessarily slow; the driver and buffer matter. Delay compensation aligns recorded material but does not remove monitoring delay.
:::
