---
id: sample-playback-synthesis
site: prod
cat: B3
title: 采样回放合成
title_en: Sample Playback Synthesis
summary: 录下真实乐器的一个音，再用变调与循环铺满键盘。
summary_en: Record one real note, then stretch, loop and pitch it across the keyboard.
level: standard
tags: [合成, 采样, 回放, 音色]
tags_en: [synthesis, sampling, playback, timbre]
alias: [采样回放合成, 采样合成, sample playback, sample-based synthesis]
links:
  - "[[glossary:sampler]]"
  - "[[glossary:timbre]]"
  - "[[instrument:samplers]]"
  - "[[period:modern]]"
instances:
  - oga-000330 | 钢琴、电钢琴与无品贝斯同场，三种采样音色的音头差别清楚
  - oga-000195 | 尼龙弦与闷音吉他交替，拨弦噪声与衰减来自录音而非振荡器
  - oga-000143 | 拉杆风琴与管钟并置，持续音与击发音是两类采样
sources:
  - Curtis Roads, The Computer Music Tutorial — sampling and playback checked, not quoted
  - MIDI Association, General MIDI 1 Sound Set — program list checked, not quoted
updated: 2026-10-28
---

::: zh
## 起点：一个问题

采样器里只有几个录好的音，为什么按不同的键都能响，而且听起来仍像那件乐器？采样回放合成要回答「一个音如何变成一整片键盘」。

## 背后的机制

录音被切成若干键区与力度层，每个区里放一个或几个样本。按键时先选样本，再按音高比例改变播放速度，于是音高变了，时长与共振也一起变。为了省内存，持续音会在循环点之间反复播放；循环点对不齐会产生脉动。样本之间的衔接靠交叉淡化，淡化太长会糊，太短会听见接缝。合成器再给样本加滤波、包络与效果，弥补变调后的失真。

## 数值怎么变成声音

变调越多，样本越像被加速的录音，短促且共振偏移。循环点靠近音头会让音色发紧，靠近尾部则容易听见周期。力度层少时，轻重只靠音量，缺少真实的音色变化。滤波可以压掉变调的亮边，但压多了会失去原乐器的质感。

## 耳朵要抓的点

先听钢琴高音区，注意音头仍像钢琴，但尾巴比低音区短。再听尼龙弦吉他，拨弦噪声每次都有细微差别。最后听管钟，击发后的长衰减是否在循环处出现规律的起伏。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5"],"label":"一个样本铺满四个音","label_en":"One sample spread across four notes","hint":"先按真实音色听采样，再按合成近似听模型；注意越高音越像被加速的录音，尾音也越短","hint_en":"Play the real timbre, then the synth approximation; the higher notes sound like a sped-up recording and their tails shorten"}
```

## 容易弄错的

以为采样回放只是「放录音」；以为一个样本能覆盖所有音区；忽略循环点与力度层对真实感的影响。
:::

::: en
## Starting point: a problem

A sampler holds a handful of recorded notes, yet every key sounds and still reads as the original instrument. How does one note become a keyboard?

## The mechanism

Recordings are divided into key zones and velocity layers, each holding one or more samples. A keypress selects a sample, then playback speed changes in proportion to pitch, so pitch, duration and resonance all move together. To save memory, sustained notes loop between loop points; misaligned points produce pulsing. Zones are joined by crossfades, which blur if too long and expose a seam if too short. The synth then adds filtering, envelopes and effects to hide the artefacts of transposition.

## From numbers to sound

The further a sample is transposed, the more it resembles an accelerated recording, short and shifted in resonance. Loop points close to the attack make the tone tight, while points near the tail expose the cycle. Few velocity layers mean loudness alone carries the accent, without real colour change. Filtering can tame the bright edge of transposition, but too much removes the instrument's body.

## What the ear should catch

Hear a piano's upper register: the attack still reads as piano, but the tail is shorter than below. Then hear a nylon-string guitar, where the finger noise differs slightly on every note. Finally hear tubular bells and check whether the long decay pulses at the loop.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "C5"], "label": "One sample spread across four notes", "label_en": "One sample spread across four notes", "hint": "先按真实音色听采样，再按合成近似听模型；注意越高音越像被加速的录音，尾音也越短", "hint_en": "Play the real timbre, then the synth approximation; the higher notes sound like a sped-up recording and their tails shorten"}
```

## Easy to get wrong

That sample playback is merely pressing play on a recording; that one sample can cover the whole keyboard; that loop points and velocity layers hardly affect realism.
:::
