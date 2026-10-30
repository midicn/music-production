---
id: time-stretch-and-pitch-shift
site: prod
cat: B4
title: 时间拉伸与变调
title_en: Time Stretching and Pitch Shifting
summary: 拉伸改时长不改音高，变调改音高不改时长，两者都会留痕。
summary_en: Stretching changes duration, shifting changes pitch, and both leave traces on the material.
level: standard
tags: [时间拉伸, 变调, 算法]
tags_en: [time stretch, pitch shift, algorithm]
alias: [时间拉伸, 音高变换, time stretch, pitch shift]
links:
  - "[[glossary:pitch]]"
  - "[[glossary:octave]]"
  - "[[glossary:timbre]]"
instances:
  - pdmx-002097 | 《野蜂飞舞》的快速音群被拉伸后会露出颗粒与重复
  - giantmidi-003263 | 萨蒂《玄秘曲》速度慢，变调后共振峰的移动很容易听出
  - mutopia-000546 | 布拉姆斯艺术歌曲有人声与钢琴，变调时共振峰是否保留一听便知
sources:
  - Curtis Roads, The Computer Music Tutorial — 相位声码器与颗粒合成的说明核对，未抄原文
  - Jean Laroche, Mark Dolson, Improved Phase Vocoder Time-Scale Modification — 瞬态处理的结论核对，未抄原文
updated: 2026-10-28
---

::: zh
## 问题

把一段录音放慢，为什么音高不变，但鼓点会变得黏糊？

## 原理

时间拉伸改变时长而保持音高，音高变换改变音高而保持时长。常见算法有相位声码器、颗粒合成与瞬态保留。相位声码器把信号切成短帧，在频域移动相位，适合持续音，但对瞬态不友好，鼓点会被抹开。颗粒合成把声音切成小片重新排列，拉伸比例大时会出现重复与金属味。音高变换可以靠重采样加快慢，也可以改共振峰。保留共振峰的变调更像同一个人换音高，不保留则像加速录音。

## 做法与参数

拉伸比例控制在正负 15% 以内，超过就换录音或重奏。鼓与贝斯优先用瞬态保留模式，人声优先保留共振峰。大幅拉伸时先切片对齐瞬态，再对小片做拉伸。变调超过五个半音时，检查齿音与呼吸是否自然。处理前后对齐响度，避免把变响误当成变好。

## 听什么

听鼓循环放慢后的军鼓，瞬态会从一击变成一片。听人声降调，共振峰不保留时会像慢放磁带。听钢琴升调，低音区的共鸣整体上移，变得单薄。听持续弦乐，拉伸过度会出现周期性的颤动。

## 常见误解

以为拉伸与变调是同一件事；以为任何素材都能大幅拉伸；以为保留共振峰只是音色偏好。

```audiolab
{"type":"instrument","gm":"Flute","synth":"blown","phrase":["C5","D5","E5","G5","A5","G5","E5","D5"],"label":"原速的气口与颤音","label_en":"Breath and vibrato at speed","hint":"先按原速听，再想放慢一半后气口会被拉长成什么形状","hint_en":"Hear it at speed, then imagine a half-speed stretch and how the breath between notes would lengthen"}
```
:::

::: en
## The problem

When a recording is slowed down, why does the pitch stay put while the drums turn mushy?

## How it works

Time stretching changes duration while holding pitch; pitch shifting changes pitch while holding duration. Common methods include the phase vocoder, granular synthesis and transient preservation. A phase vocoder cuts the signal into frames and moves phase in the frequency domain; it suits sustained tones but smears transients, so drums spread out. Granular synthesis rearranges small grains, producing repetition and a metallic edge at large ratios. Pitch shifting can resample or move formants. Keeping formants makes a transposed voice sound like the same person; dropping them sounds like a sped-up tape.

## Practice and settings

Keep stretching within about 15 percent; beyond that, re-record or replay. Use transient-preserving modes for drums and bass, and formant preservation for voice. For large stretches, slice and align transients first, then stretch the slices. Above five semitones of shift, check sibilance and breath. Match loudness before and after, so louder is not mistaken for better.

## What to listen for

Hear a slowed drum loop: the snare turns from a hit into a smear. Hear a voice shifted down without formant preservation and it sounds like slow tape. Hear a piano shifted up: the low resonance moves up and thins. Hear sustained strings, where heavy stretching adds periodic wobble.

## Common misconceptions

That stretching and pitch shifting are the same operation; that any material can be stretched far; that formant preservation is only a colour preference.

```audiolab
{"type": "instrument", "gm": "Flute", "synth": "blown", "phrase": ["C5", "D5", "E5", "G5", "A5", "G5", "E5", "D5"], "label": "Breath and vibrato at speed", "label_en": "Breath and vibrato at speed", "hint": "Hear it at speed, then imagine a half-speed stretch and how the breath between notes would lengthen", "hint_en": "Hear it at speed, then imagine a half-speed stretch and how the breath between notes would lengthen"}
```
:::
