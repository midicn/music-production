---
id: noise-and-hum
site: prod
cat: A4
title: 噪声与哼声
title_en: Noise and Hum
summary: 嘶声来自电路，哼声来自接地，两者要先分清再处理
summary_en: Hiss comes from the circuit, hum from the grounding. Separate them before you treat either.
level: standard
tags: [录音, 噪声, 接地]
tags_en: [recording, noise, grounding]
alias: [底噪, 哼声, 交流声, 嘶声, hum, hiss, noise]
links:
  - "[[glossary:noise-floor]]"
  - "[[glossary:signal-to-noise]]"
  - "[[instrument:organ]]"
instances:
  - cyberhymnal-001740 | 管风琴持续音不衰减，哼声会一直贴在和声里
  - mutopia-000848 | 独奏吉他动态小，弱奏时底噪的占比最高
  - openscore-000667 | 艺术歌曲的弱唱段，房间声与电流声一起进来
sources:
  - Ballou, Handbook for Sound Engineers, grounding and shielding chapters
  - AES Convention paper on hum, ground loops and balanced interconnection
updated: 2026-10-28
---

::: zh
## 问题

安静段落里，嘶声与低频嗡声会先于音乐被听见。嘶声来自电路与增益，哼声来自供电与接地，两者的成因不同，处理手段也不能互换。

## 信号链

噪声沿着整条链累积。话筒拾取房间与电磁场，话放把自身底噪和信号一起放大，转换器再加一点。哼声多由地环路引起，基频落在 50 Hz，并带整数倍谐波，随线缆与电源变化。

## 摆位与参数

增益按最强段设定，让峰值落在 -12 dBFS 附近，弱奏段不要再补。话筒线远离电源线与显示器，所有设备插同一路电源。查出哼声先拔输入判断来源，再用平衡线与正确接地解决，不要用 EQ 硬削。

```audiolab
{"type":"instrument","gm":"Contrabass","synth":"bowed","phrase":["G1","G1"],"label":"哼声所在的低频带","label_en":"The band where hum sits","hint":"先听 G1 的厚度，市电哼声就在它上方一点","hint_en":"Hear the weight of G1; mains hum sits just above it"}
```

## 听什么

在无声段落把监听推高，听嘶声是否随增益一起变大；换一个电源插座，再听低频嗡声是否改变。哼声的谐波常落在人声低频区，容易被误认为低频太厚。

## 常见误解

- **噪声大就换话筒** → 增益分配与接地更常见。
- **降噪插件能救一切** → 它会连弱奏的尾音一起吃掉。
- **哼声是设备坏了** → 多数来自地环路。
:::

::: en
## The problem

In quiet passages, hiss and hum arrive before the music. Hiss comes from circuits and gain; hum from power and grounding. Their causes differ, and so do the cures.

## Signal chain

Noise accumulates along the chain. The microphone picks up the room and electromagnetic fields, the preamp amplifies its own noise floor with the signal, and the converter adds more. Hum usually comes from a ground loop at 50 Hz with harmonics that shift with cables and outlets.

## Placement and settings

Set gain from the loudest passage so peaks land near -12 dBFS, and do not make up level later. Keep microphone cables away from mains cables and displays, and plug every device into the same outlet strip. When hum appears, unplug inputs to find the source, then fix it with balanced wiring and correct grounding instead of EQ.

```audiolab
{"type": "instrument", "gm": "Contrabass", "synth": "bowed", "phrase": ["G1", "G1"], "label": "The band where hum sits", "label_en": "The band where hum sits", "hint": "先听 G1 的厚度，市电哼声就在它上方一点", "hint_en": "Hear the weight of G1; mains hum sits just above it"}
```

## What to listen for

In a silent passage, raise the monitor and hear whether hiss grows with gain. Change the power outlet and hear whether the hum moves. Its harmonics often land in the low voice range, where they can be mistaken for too much body.

## Common misconceptions

- **Noise means a bad microphone** → gain staging and grounding are more common.
- **A denoiser fixes everything** → it also eats the tails of soft notes.
- **Hum means broken gear** → most hum is a ground loop.
:::
