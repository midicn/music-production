---
id: buffer-size
site: prod
cat: B5
title: 缓冲区大小
title_en: Buffer Size
summary: 块越大越省 CPU，延迟越高；块越小越跟手，越易爆音。
summary_en: A larger block saves CPU but adds delay, a smaller one feels immediate but risks dropouts.
level: standard
tags: [缓冲, CPU, 实时, 爆音]
tags_en: [buffer, CPU, real time, dropouts]
alias: [缓冲区, 缓冲大小, 块大小, buffer size, block size]
links:
  - "[[glossary:buffer-size]]"
  - "[[glossary:latency]]"
  - "[[glossary:monitoring]]"
instances:
  - groove-000010 | 放克鼓循环踩镲连续，块太大时实时跟打会粘（C1）
  - giantmidi-001994 | 阿尔坎练习曲音符极密，缓冲拉大后连奏颗粒容易糊成一片（C1）
  - thesession-000040 | 吉格舞曲三拍连缀不断，块太大时装饰音挤在一起（C1）
sources:
  - 块大小与欠载的关系，依音频接口与宿主公开文档核查，未抄文本
  - Pohlmann, Principles of Digital Audio, real-time processing sections — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

声卡按块工作，一块填满才处理。块大省 CPU 但反应慢，块小跟手但容易断，缓冲区大小就是两者之间的旋钮。

## 原理

缓冲时间等于块大小除以采样率。48 kHz 下 64 个样点约 1.3 毫秒，1024 个样点约 21.3 毫秒。CPU 必须在下一块到来前算完，否则欠载，出现咔嗒或静音。插件越多、越吃算力，能稳定运行的最小块就越大。

## 参数与做法

录音用 64 到 128，混音用 256 到 512，母带与离线渲染用 1024。重插件先冻结或渲染。实时演奏时减小块，导出时加大。出现爆音先看 CPU 占用与驱动，不要一味加大缓冲。换工程后重测最小稳定值。

## 听什么

在放克鼓循环里听踩镲的连续击打，在阿尔坎练习曲里听快速音型的颗粒，在吉格舞曲里听三拍连缀。块太大时实时跟打会粘连，块太小时出现周期性咔嗒，间隔正好等于缓冲时间。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":120,"label":"连续的短击","label_en":"A run of short hits","hint":"先听它是否均匀，再想缓冲加大后哪里会粘","hint_en":"Hear whether it stays even, then imagine where a larger block would smear it"}
```

## 常见误解

缓冲区是硬盘缓存，其实它属于音频接口的处理块。加大缓冲不提升音质，只降低爆音概率。爆音不一定是声卡坏了，也可能是驱动或插件。所有实时音频都要经过它，不只 MIDI。
:::

::: en
## The question

An interface works in blocks, processing only when one fills. A large block saves CPU but reacts slowly; a small one feels immediate but breaks up.

## How it works

Buffer time is block size divided by sample rate. At 48 kHz, 64 samples last about 1.3 ms and 1024 samples about 21.3 ms. The CPU must finish each block before the next arrives, or it underruns into clicks or silence. More and heavier plug-ins raise the smallest stable block.

## Settings and practice

Use 64 to 128 samples for tracking, 256 to 512 for mixing, and 1024 for mastering or offline rendering. Freeze or render heavy plug-ins. Shrink the block when playing and enlarge it when exporting. If clicks appear, check CPU and drivers before raising the buffer.

## What to listen for

In a funk loop, hear the hi-hat. In Alkan etudes, hear the grain of fast figures. In a jig, hear the three-beat run. Too large a block smears live playing; too small a block clicks at intervals equal to the buffer time.

```audiolab
{"type": "rhythm", "sig": "4/4", "pattern": "s s s s s s s s s s s s s s s s", "bpm": 120, "label": "A run of short hits", "label_en": "A run of short hits", "hint": "先听它是否均匀，再想缓冲加大后哪里会粘", "hint_en": "Hear whether it stays even, then imagine where a larger block would smear it"}
```

## Common misconceptions

A buffer is not a disk cache but the processing block of the interface. Raising it does not improve quality, only the odds against dropouts. Clicks may come from drivers or plug-ins, not a broken one. Every real-time audio path uses it, not only MIDI.
:::
