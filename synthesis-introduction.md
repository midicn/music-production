---
id: synthesis-introduction
site: prod
cat: B3
title: 合成导论
title_en: Introduction to Synthesis
summary: 从振荡器到滤波器，先弄清声音是怎样被造出来的。
summary_en: Before choosing a method, learn how oscillators, filters and envelopes turn electricity into a playable timbre.
level: standard
tags: [合成, 导论, 振荡器, 包络]
tags_en: [synthesis, introduction, oscillator, envelope]
alias: [合成导论, 合成器原理, synthesis introduction, synthesis basics]
links:
  - "[[glossary:timbre]]"
  - "[[glossary:synthesizer]]"
  - "[[instrument:minimoog]]"
  - "[[period:modern]]"
instances:
  - oga-000163 | 锯齿主音、扫频铺底与陶笛同曲，三种造音路线可当场对照
  - oga-000143 | 拉杆风琴、管钟与哨音分层，谐波叠加与金属泛音的差别清楚
  - oga-000286 | 锯齿主音配合成贝斯，电子音色的骨架由振荡器与滤波器撑起
sources:
  - Gordon Reid, Sound On Sound Synth Secrets — synthesis chain checked, not quoted
  - Curtis Roads, The Computer Music Tutorial — synthesis methods overview checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

合成器既不采样，也没有琴弦与音管，为什么能模仿铜管、人声和钟？合成导论先给出一张地图：哪些部件造出声音，改动时耳朵听到什么。

## 原理

最短的信号链是振荡器、滤波器与放大器，三者各由一个包络或 LFO 推动。振荡器给出周期波，决定基础的谐波排列；滤波器削掉或强调某段频率；包络规定声音随时间的形状；LFO 提供缓慢起伏。加法、FM、波表与粒子只是换了产生谐波和塑形的算法；采样回放直接播放录音。所有路线最后都落到同样的维度：频谱、包络、空间与调制。

## 参数与听感

先动波形与音高，听谐波是齐整还是空心；再动截止，听高频退去的速度；最后动起音与释放，听它像弓弦、像拨片还是像气吹。轻微失谐会让声音变宽，音量包络过短会让低音失去重量。参数会互相抵消，一次只改一个。

## 听什么

播一首电子曲，先只判断主音是亮还是闷，再把注意力移到低音是圆还是硬，最后听铺底有没有缓慢起伏。能把这三层分开，就已经在按合成器的维度听音乐。

```audiolab
{"type":"instrument","gm":"Lead 2 (sawtooth)","synth":"bowed","phrase":["A3","C4","E4","A4","C5"],"label":"一条信号链的三种声音","label_en":"Three sounds from one signal chain","hint":"先听锯齿主音，再想象关小截止、拉长起音；同一波形会从亮弓弦变成闷铺底","hint_en":"Hear the saw lead, then imagine closing the cutoff and lengthening the attack; one wave turns from bright bow to dull pad"}
```

## 常见误解

以为合成器就是电子琴音色；以为音色只由波形决定，忽略包络与滤波；以为方法越高深越好，其实多数流行音色仍出自减法合成与采样回放。
:::

::: en
## The question

A synthesizer has no strings or bell, yet it can sound like brass, a voice or a struck plate. Before choosing a method, map the parts that make the sound and what each change does.

## How it works

The shortest chain is oscillator, filter and amplifier, each pushed by an envelope or an LFO. The oscillator supplies a periodic wave and harmonics. The filter removes or emphasises a band. The envelope shapes level over time, and the LFO adds slow movement. Additive, FM, wavetable and granular methods swap the harmonic source and shaping for other algorithms; sample playback plays a recording. Every route ends at the same dimensions: spectrum, envelope, space and modulation.

## Settings and what you hear

Change waveform and pitch and listen for a full or hollow harmonic set. Then move the cutoff and hear how quickly the top disappears. Finally change attack and release to read bow, pick or breath. Slight detuning widens the tone, and a short envelope robs bass of weight. Parameters cancel each other, so change one at a time.

## What to listen for

On an electronic track, decide whether the lead is bright or dull, then whether the bass is round or hard. Last, hear whether the pad moves underneath. Separating these three layers is already listening along synthesizer dimensions.

```audiolab
{"type": "instrument", "gm": "Lead 2 (sawtooth)", "synth": "bowed", "phrase": ["A3", "C4", "E4", "A4", "C5"], "label": "Three sounds from one signal chain", "label_en": "Three sounds from one signal chain", "hint": "先听锯齿主音，再想象关小截止、拉长起音；同一波形会从亮弓弦变成闷铺底", "hint_en": "Hear the saw lead, then imagine closing the cutoff and lengthening the attack; one wave turns from bright bow to dull pad"}
```

## Common misconceptions

That a synthesizer is just an electronic keyboard patch; that waveform alone decides timbre, when envelope and filter matter as much; that the more advanced method always wins, when most popular sounds come from subtractive synthesis and samples.
:::
