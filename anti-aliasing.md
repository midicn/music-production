---
id: anti-aliasing
site: prod
cat: B4
title: 抗混叠
title_en: Anti-Aliasing
summary: 采样前压掉超上限的高频，防止它们折回成假声。
summary_en: Filtering above the ceiling before sampling stops high frequencies folding back as false tones.
level: standard
tags: [抗混叠, 采样率, 滤波器]
tags_en: [anti-aliasing, sample rate, filter]
alias: [混叠, 折叠失真, aliasing, anti-aliasing filter]
links:
  - "[[glossary:sample-rate]]"
  - "[[glossary:harmonics]]"
  - "[[glossary:timbre]]"
instances:
  - groove-000000 | 踩镲与军鼓的高频成分多，降采样时最容易折回成沙声
  - pdmx-000251 | 钢片琴的密集泛音在低采样率下会折叠到中频
  - atepp-000381 | 高音区钢琴泛音丰富，混叠会让音头多一层金属毛边
sources:
  - Ken C. Pohlmann, Principles of Digital Audio — 用于核对混叠与过采样的机制。
  - Julius O. Smith III, Digital Audio Resampling — 用于核对重采样滤波与过渡带的说明。
updated: 2026-10-28
---

::: zh
## 要解决的事

为什么有些录音一降采样，镲片就多出一层沙沙的假声，而原始文件里并没有这层声音？

## 它怎么工作

采样前如果没有把奈奎斯特频率以上的成分滤掉，它们会折叠到可听频段，这叫混叠。折叠不是衰减，而是频率镜像，假声会出现在与原音无关的位置，像金属摩擦或嘶嘶声。抗混叠滤波器要在采样之前工作，过渡带要窄，否则要么切掉太多高频，要么漏进折叠成分。降采样、变调与波表读取都可能重新引入混叠，所以每一步都要检查带宽。

## 旋钮与做法

录音与导出保持 44.1 或 48 kHz，让转换器负责滤波。做大幅升调时先升采样再变调，或直接用带抗混叠的算法。自己做波表或失真时，在生成阶段就限制谐波，别等播放时再救。检查方法是把升降调前后的频谱对齐，看有没有非谐波成分突然出现。

## 耳朵要抓的点

听踩镲与沙锤的尾音，折叠后会出现一层不随力度变化的沙声。听钢片琴的高音，假声会让音头变脏。听锯齿波主音上滑，若出现反向下行的假音，多半是混叠。听人声齿音，混叠会让齿音变成一片细碎的噪点。

## 容易弄错的

以为混叠只发生在低端设备；以为加一个低通效果器就能解决；以为提高音量可以掩盖。

```audiolab
{"type":"instrument","gm":"Lead 2 (sawtooth)","synth":"bowed","phrase":["A5","C6","E6","A6"],"label":"锯齿波的高音","label_en":"A sawtooth high up","hint":"演示在固定采样率下合成，听高音区锯齿的毛边；真正的折叠要在低采样率导出时对比","hint_en":"The lab synthesises at a fixed rate, so listen for the gritty edge up high; real folding needs a low-rate export to compare"}
```
:::

::: en
## The problem to solve

Why does downsampling sometimes add a sandy layer to cymbals that was not in the original file?

## How it works

If content above Nyquist is not removed before sampling, it folds into the audible band. This is aliasing, and it is a mirror in frequency, not a fade, so the false tones often land far from the original pitch and read as metallic friction or hiss. The anti-aliasing filter must act before conversion, with a narrow transition band; too wide and it cuts useful highs, too gentle and folded content leaks through. Modern converters oversample and filter digitally, easing the analog stage. Downsampling, pitch shifting and wavetable lookup can each reintroduce aliasing, so every stage needs a bandwidth check.

## Knobs and practice

Record and deliver at 44.1 or 48 kHz and let the converter filter. For large upward shifts, upsample before shifting or use an algorithm with built-in anti-aliasing. When generating wavetables or distortion, limit harmonics at the source instead of repairing later. To check, align spectra before and after the shift and look for non-harmonic content that appears from nowhere.

## What the ear catches

Hear hi-hat and shaker tails: aliasing adds a sandy layer that does not follow velocity. Hear celesta high notes, where the attack turns dirty. Slide a sawtooth lead upward and listen for a false tone moving the wrong way. Hear vocal sibilance, which can collapse into fine noise.

## Easy to get wrong

That aliasing only happens on cheap gear; that a low-pass effect fixes it; that louder playback hides it.

```audiolab
{"type": "instrument", "gm": "Lead 2 (sawtooth)", "synth": "bowed", "phrase": ["A5", "C6", "E6", "A6"], "label": "A sawtooth high up", "label_en": "A sawtooth high up", "hint": "The lab synthesises at a fixed rate, so listen for the gritty edge up high; real folding needs a low-rate export to compare", "hint_en": "The lab synthesises at a fixed rate, so listen for the gritty edge up high; real folding needs a low-rate export to compare"}
```
:::
