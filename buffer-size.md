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
  - groove-000010 | 鼓点时序参照；预先播放不测量实时输入延迟（C1） | Drum-event timing reference; scheduled playback does not measure live-input latency (C1)
  - giantmidi-001994 | 密集钢琴音型参照；缓冲大小不会自动改变文件内的连奏（C1） | Dense piano figures; buffer size does not automatically alter the file’s legato (C1)
  - thesession-000040 | 吉格舞曲的拍点与装饰音参照，不是不同缓冲设置的处理结果（C1） | Jig beats and ornaments, not renders using different buffer settings (C1)
sources:
  - "https://help.ableton.com/hc/en-us/articles/209070329-How-to-avoid-crackles-and-audio-dropouts"
  - "https://help.ableton.com/hc/en-us/articles/360010545559-How-Latency-Works"
  - 块大小与欠载的关系；音频接口与宿主公开文档是主要依据。
  - Pohlmann, Principles of Digital Audio, real-time processing sections.
updated: 2026-11-02
---

::: zh
## 问题

声卡按块工作，一块填满才处理。块大省 CPU 但反应慢，块小跟手但容易断，缓冲区大小就是两者之间的旋钮。

## 原理

单个缓冲块的时长等于样点数除以采样率。48 kHz 下，64 样点约为 1.33 ms，1024 样点约为 21.33 ms；这不是整条监听链路的总延迟。输入与输出缓冲、转换器、驱动和带前瞻的插件还会增加时间。实时处理来不及交付下一块数据时，可能出现爆音或中断。

## 参数与做法

从接口支持的较小块开始，边演奏边观察是否稳定，再逐档增大。64–128 样点可作为录音时的试验起点，不是所有电脑都能稳定使用；混音不需实时跟手时可放宽。冻结重插件、检查驱动和后台负载，往往比一直改数值更有效。离线导出不必服从声卡的实时缓冲设置，取决于 DAW 的渲染实现。

## 听什么

用实际键盘或录音输入测试跟手程度，单纯播放已经排好的 MIDI 不能说明演奏延迟。再用同一工程逐档改变缓冲，记录爆音次数和 DAW 报告的总延迟。爆音通常与调度、驱动或瞬时负载有关，不保证以一个缓冲块的周期出现。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":120,"label":"连续短击","label_en":"Repeated short attacks","hint":"听短击的节奏关系。这里没有改变音频接口缓冲；缓冲延迟要用实际演奏输入与返回声音测量。","hint_en":"Listen to attack timing. This block does not change the audio-interface buffer; measure buffer latency using live input and returned sound."}
```

## 常见误解

缓冲区是硬盘缓存，其实它属于音频接口的处理块。加大缓冲不提升音质，只降低爆音概率。爆音不一定是声卡坏了，也可能是驱动或插件。所有实时音频都要经过它，不只 MIDI。
:::

::: en
## The question

An interface works in blocks, processing only when one fills. A large block saves CPU but reacts slowly; a small one feels immediate but breaks up.

## How it works

One buffer lasts its sample count divided by sample rate: about 1.33 ms for 64 samples at 48 kHz, or 21.33 ms for 1024. That is not the total monitoring delay. Input and output buffers, converters, drivers and look-ahead plug-ins add time. Missing a real-time processing deadline can cause clicks or dropouts.

## Settings and practice

Start with a small supported block, play through the session, and increase it if stability suffers. A 64–128-sample tracking buffer is a trial starting point, not a guarantee for every computer. Mixing can tolerate more delay. Freeze heavy plug-ins and check drivers and background load. Offline rendering may use a different processing scheme and need not follow the interface's real-time buffer setting.

## What to listen for

Test responsiveness with a keyboard or live recording input; playing a pre-sequenced MIDI file does not measure playing latency. Change the buffer one step at a time in the same session and record dropout count and reported overall latency. Dropouts can depend on scheduling, drivers and load spikes; their spacing need not equal one buffer period.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":120,"label":"Repeated short attacks","label_en":"Repeated short attacks","hint":"Listen to attack timing. This block does not change the audio-interface buffer; measure buffer latency using live input and returned sound.","hint_en":"Listen to attack timing. This block does not change the audio-interface buffer; measure buffer latency using live input and returned sound."}
```

## Common misconceptions

A buffer is not a disk cache but the processing block of the interface. Raising it does not improve quality, only the odds against dropouts. Clicks may come from drivers or plug-ins, not a broken one. Every real-time audio path uses it, not only MIDI.
:::
