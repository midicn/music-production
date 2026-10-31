---
id: audio-vs-midi-tracks
site: prod
cat: A1
title: 音频轨与 MIDI 轨
title_en: Audio and MIDI Tracks
summary: 一条存声音，一条存演奏动作，编辑自由度与音色来源都不同。
summary_en: One stores sound, the other stores performance, so editability and sound source differ in ways that shape the whole session.
level: standard
tags: [DAW, 音频轨, MIDI, 工作流]
tags_en: [DAW, audio track, MIDI, workflow]
alias: [音频轨, MIDI轨, 音频与MIDI, audio track, MIDI track]
links:
  - "[[glossary:midi-protocol]]"
  - "[[glossary:velocity]]"
  - "[[glossary:sample-rate]]"
instances:
  - groove-000007 | 摇滚鼓循环，既能当音频切片，也能用 MIDI 重排
  - atepp-000195 | 钢琴独奏的踏板与弱音，只在 MIDI 事件里能逐项修改
  - pdmx-000210 | 多声部协奏曲，分谱后常是 MIDI 与音频轨并存
sources:
  - 音频轨与 MIDI 轨的数据结构差异；MIDI 规范与数字音频教材是主要依据。
  - 切片、冻结与延迟补偿的做法——依据来自 DAW 文档。
updated: 2026-10-28
---

::: zh
音频轨存的是声音，MIDI 轨存的是演奏动作。两者都能出声，但你能改的东西完全不同。

## 要解决的事

改一个音高，音频要重录或变调，MIDI 改一个数字即可；可 MIDI 离开音源就没有声音。选择哪一种轨，先问自己后面还要改什么。

## 它怎么工作

音频轨是采样序列，编辑单位是波形，切片、淡化与时间拉伸都在采样上做。MIDI 轨是事件流，编辑单位是音符、力度与控制变化，回放时才由音源生成声音。冻结或渲染把 MIDI 变成音频，也把可改性换成稳定。

## 参数与取舍

需要改速度、移调或换音色的声部保留 MIDI；人声、吉他等以音色与演奏细节为主的内容存音频。注意延迟补偿，别让 MIDI 轨与音频轨差出几个毫秒。

## 耳朵要抓的点

同一段钢琴，音频与 MIDI 的差别常在踏板、噪声与力度细节。MIDI 回放容易过于整齐，音频则保留演奏的毛边。听的时候先找尾音，再找弱音。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","D4","E4","G4"],"label":"同一段钢琴的两种存法","label_en":"One piano phrase, two ways to store it","hint":"听力度与尾音，想象哪些还能改","hint_en":"Hear velocity and tail, then ask what can still change"}
```

## 容易弄错的

MIDI 不是声音，只是指令。音频轨也不是不能量化，切片之后同样可以对网格。
:::

::: en
An audio track stores sound; a MIDI track stores performance. Both make sound, but what you can change afterwards is completely different.

## The problem to solve

To change a pitch, audio must be re-recorded or shifted, while MIDI needs one number changed; yet MIDI makes no sound without an instrument. Which track to use depends on what you still need to edit.

## How it works

An audio track is a sample sequence. Editing works on the waveform, so slicing, fades and time-stretching all touch samples. A MIDI track is an event stream. Editing works on notes, velocity and controller changes, and an instrument generates sound at playback. Freezing or rendering turns MIDI into audio and trades editability for stability.

## Settings and trade-offs

Keep MIDI for parts that need tempo changes, transposition or a different sound. Keep audio for voices, guitars and anything whose character is in the performance. Watch delay compensation so MIDI and audio tracks do not drift by a few milliseconds.

## What the ear catches

On the same piano passage, audio and MIDI differ in pedal, noise and velocity detail. MIDI playback tends to sound too even; audio keeps the rough edges. Listen for the tail first, then for the quiet notes.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "D4", "E4", "G4"], "label": "One piano phrase, two ways to store it", "label_en": "One piano phrase, two ways to store it", "hint": "听力度与尾音，想象哪些还能改", "hint_en": "Hear velocity and tail, then ask what can still change"}
```

## Easy to get wrong

MIDI is not sound, only instructions. Audio tracks are not unquantisable either; after slicing, they can be aligned to a grid.
:::
