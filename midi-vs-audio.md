---
id: midi-vs-audio
site: prod
cat: B1
title: MIDI 与音频的区别
title_en: MIDI versus Audio
summary: MIDI 记动作，音频记波形，两者能改的地方完全不同。
summary_en: MIDI stores actions and audio stores waveforms, so what can still be changed afterwards differs completely.
level: standard
tags: [MIDI, 音频, 录音, 工作流]
tags_en: [MIDI, audio, recording, workflow]
alias: [MIDI 与音频, MIDI 和音频的区别, MIDI vs audio, 音频与 MIDI]
links:
  - "[[glossary:midi-protocol]]"
  - "[[glossary:sampler]]"
  - "[[instrument:piano]]"
instances:
  - musicnet-000300 | 390 秒的五重奏只有 75 KB，换音源就能重新配器
  - groove-000007 | 28 秒鼓组不到 2 KB，击打位置与力度都在，声音不在
  - oga-000012 | 两个力度值、规整网格，听得出这是一串指令而不是录音
sources:
  - MIDI 1.0 的传输速率与消息长度，依 MMA 公开规范核查，未抄文本
  - 数字音频采样率与量化的定义，依通行数字音频教材核查，未抄文本
updated: 2026-10-28
---

::: zh
录下来的音频是一段波形，改一个音就要重录或切开。MIDI 记的是动作，改音高、改速度、换乐器都只是改数字。

## 问题

分不清这两件事，就会在错的轨道上找问题。音频轨里改不动的音准，换到 MIDI 轨只是一条弯音；MIDI 轨里做不出的真实房间，换到音频轨才有。工程里两种轨常常同时存在，职责要分开。

## 协议或消息

音频按采样率把振幅存成一串数值，44.1 kHz 就是每秒四万四千一百个采样，每个采样再按位深取整。MIDI 每秒最多传 3125 个字节，一条音符三个字节。音频的长度由采样数决定，MIDI 的长度由速度与拍数决定。音频的音高已经固化在波形里，MIDI 的音高只是一个键号。

## 参数与做法

要保留演奏细节又想要音色自由，就录 MIDI 再渲染成音频。要有真实话筒声、房间与噪声，只能录音频。两者对齐时用同一个起点，并补偿渲染延迟。混音阶段 MIDI 轨最后都要变成音频，或由 DAW 实时合成。

## 听什么

音频变速会变调，或留下拉伸的痕迹；MIDI 变速音色不变。同一段旋律改音色，MIDI 一瞬间换完，音频只能重录。音频的重复段每次都有细小声差，MIDI 的重复段逐字相同。

## 常见误解

MIDI 不是压缩音频。MIDI 轨也能发声，但声音来自音源。音频也能改音高，只是代价不同。两种轨可以进同一条总线。

```audiolab
{"type":"instrument","gm":"Electric Guitar (clean)","synth":"plucked","phrase":["E3","G3","A3","B3"],"label":"同一份文件，换一种乐器","label_en":"One file, another instrument","hint":"声音可以被替换，写下的动作不能","hint_en":"The sound can be replaced; the actions written down cannot"}
```
:::

::: en
Recorded audio is a waveform, so changing one note means re-recording or cutting it apart. MIDI stores actions, and pitch, tempo or instrument changes are only edits to numbers.

## The problem

Confusing the two sends you to the wrong track. Intonation that audio cannot fix is one pitch bend away on a MIDI track, while a real room cannot be produced by MIDI at all. Sessions hold both.

## Protocol or message

Audio stores amplitude at the sample rate, so 44.1 kHz means 44,100 samples per second, each rounded to a bit depth. MIDI carries at most 3,125 bytes per second, and a note message takes three bytes. Audio length comes from the sample count; MIDI length from tempo and bars. Audio pitch is fixed in the waveform, while a MIDI pitch is only a key number.

## Settings and practice

Record MIDI and render it for performance detail with free timbre. Record audio for a real microphone, room and noise. Align both from one start point and compensate for render delay. By the mix, MIDI becomes audio or is synthesised by the DAW.

## What to listen for

Audio stretched in tempo shifts pitch or leaves artefacts; MIDI changes tempo without touching timbre. Swapping a melody's sound takes an instant in MIDI and a new take in audio. Repeated audio phrases differ slightly, while repeated MIDI phrases are identical.

## Common misunderstandings

MIDI is not compressed audio. A MIDI track makes sound, but the sound comes from a source. Audio pitch can be edited, at a different cost. Both kinds of track feed one bus.

```audiolab
{"type": "instrument", "gm": "Electric Guitar (clean)", "synth": "plucked", "phrase": ["E3", "G3", "A3", "B3"], "label": "One file, another instrument", "label_en": "One file, another instrument", "hint": "声音可以被替换，写下的动作不能", "hint_en": "The sound can be replaced; the actions written down cannot"}
```
:::
