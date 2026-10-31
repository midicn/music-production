---
id: melodyne
site: prod
cat: C
order: 22
title: Melodyne（音高与时值编辑）
title_en: Melodyne (Pitch and Timing Editing)
summary: 把音频拆成音符来处理，音高、时值与共振峰各自可动。
summary_en: Audio becomes notes, with pitch, timing and formants edited as separate dimensions.
level: standard
tags: [插件, 音高, 时值, 编辑]
tags_en: [plugin, pitch, timing, editing]
alias: [Melodyne, Celemony Melodyne, DNA, 音高编辑, 音频转 MIDI]
tool_kind: plugin
tool_vendor: Celemony
tool_form: 插件
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [混音, 修复, 编曲]
tool_verified: 2026-10-30
links:
  - "[[glossary:pitch]]"
  - "[[instrument:voice]]"
  - "[[instrument:popular-voice]]"
instances:
  - thesession-022200 | 爱尔兰传统曲调独奏，装饰音密集，拆成音符后能逐个改时值（C1）。
  - musicnet-000020 | 巴赫大提琴组曲前奏，单声部、连奏多，音符边界清楚，适合练时值拉伸（C1）。
  - mutopia-000005 | 阿瓜多古典吉他练习曲，同时有旋律与低音，多声部识别是否干净一听就知道（C1）。
  - essen-000009 | 《茶田山歌》，自由节拍的山歌，音符切分与呼吸位置都要手动确认（C1）。
sources:
  - Celemony 官方产品页的音符编辑、多声部识别与 ARA 说明，参考公开资料。
  - 音频转 MIDI 与共振峰编辑的常见做法；编辑惯例是主要依据。
updated: 2026-10-30
---

::: zh
## 适用工作

- 把一条唱得可以的声乐轨逐音修到可用，保留原有的语气。
- 把独奏的连奏改得更平均，或故意做出人性的推拉。
- 改音符时值与位置，让演奏和节拍对齐而不切碎音频。
- 在多声部素材上单独移动一个声部，做和声调整或改错音。
- 把音频转成 MIDI，拿去换音色或做编曲草稿。
- 修共振峰与颤音，改变音色的粗细与稳定度。

## 原理

软件先做音高与瞬态的检测，把连续的音频切成一个个音符对象。每个对象带音高、起点、时长、共振峰与音量等参数，编辑时只改这些参数，再按原相位重建波形。多声部识别会尝试把同时发声的音分开，干净的单声部最稳，密集混音会出错。音符分离阈值可调，太高会把颤音拆成多个音，太低会并掉经过音。ARA 模式下它直接读宿主的时间线，不用把音频传进传出；不支持 ARA 的宿主则走桥接或独立应用。

## 边界

- 多声部识别不是万能，混响重、失真多或声部交叠时会把音符分错，改之前要逐段核对。
- 编辑越深，重建痕迹越明显；大幅改时值会让起音变软，大幅移调会改变共振峰。
- ARA 支持因宿主与版本而异，不支持的工程只能导出音频再导入，往返次数要控制。
- 功能按版本分档，多声部与音频转 MIDI 不是每个档位都有，买前先确认。
- 工程采样率变化后要重新分析，旧编辑会错位。
- 它不做实时处理，现场修音要用别的工具。

## 替代

Auto-Tune 更适合实时与快速修音；ReVoice Pro 擅长对白与双轨对齐；Cubase 的 VariAudio 与 Logic 的 Flex Pitch 是宿主内置的同类功能。它常与压缩、均衡串成一条链：先用它做音符级编辑，再收动态与音色。改实时演出就用不上它。

## 上手

先学音符对象的边界与检测，再学时值与音高的分开编辑，最后学多声部与 ARA 工作流。配合「音高」「人声」「流行唱法」三篇读。

```audiolab
{"type":"instrument","gm":"Flute","synth":"blown","phrase":["D4","E4","F4","A4","G4","F4","D4"],"label":"一条待拆音符的旋律","label_en":"A line to split into notes","hint":"先听每个音的起音，再想时值拉伸后气口会落在哪里","hint_en":"Hear each onset first, then imagine where the breath lands after timing is stretched"}
```
:::

::: en
## Jobs it covers

- Tune a usable vocal take note by note while keeping its original delivery.
- Even out a soloist's legato, or push and pull it deliberately for a human feel.
- Move note timing and duration so a performance sits on the beat without cutting the audio.
- Shift one voice inside polyphonic material for harmony fixes or wrong notes.
- Convert audio to MIDI for a different sound or an arrangement sketch.
- Edit formants and vibrato to change weight and steadiness.

## How it works

The software detects pitch and transients and cuts continuous audio into note objects. Each object carries pitch, onset, duration, formant and level, and editing changes those values before rebuilding the waveform with the original phase. Polyphonic detection tries to separate simultaneous notes; clean single lines are reliable, dense mixes are not. The note-separation threshold is adjustable: too high splits vibrato into several notes, too low merges passing tones. In ARA mode it reads the host timeline directly without exporting audio; hosts without ARA use a bridge or the standalone application.

## Limits

- Polyphonic detection is not universal. Heavy reverb, distortion or overlapping voices cause misassignment, so verify each section before editing.
- Deep edits leave traces: large timing changes soften attacks, and large pitch moves alter formants.
- ARA support varies by host and version; sessions without it must export and re-import, so limit the round trips.
- Features are tiered, and polyphony plus audio-to-MIDI are not in every edition; confirm before buying.
- Changing a project's sample rate requires re-analysis, and old edits land in the wrong place.
- It does not process in real time, so live tuning needs another tool.

## Alternatives

Auto-Tune is better for real-time and quick fixes. ReVoice Pro excels at dialogue and double alignment. VariAudio in Cubase and Flex Pitch in Logic are the built-in equivalents. Melodyne usually handles note-level editing first, then compression and EQ finish the track.

## First three things

Learn how note objects are detected, then edit timing and pitch separately, then work with polyphony and ARA. Read the site's pages on pitch, the voice and popular voice alongside it.

```audiolab
{"type":"instrument","gm":"Flute","synth":"blown","phrase":["D4","E4","F4","A4","G4","F4","D4"],"label":"一条待拆音符的旋律","label_en":"A line to split into notes","hint":"先听每个音的起音，再想时值拉伸后气口会落在哪里","hint_en":"Hear each onset first, then imagine where the breath lands after timing is stretched"}
```
:::
