---
id: low-frequency-oscillator
site: prod
cat: B3
title: 低频振荡器 LFO
title_en: Low-Frequency Oscillator
summary: 慢速振荡器不发声，却让音色持续运动。
summary_en: A slow oscillator makes no sound of its own, yet keeps the timbre in motion.
level: standard
tags: [合成, LFO, 调制, 颤音]
tags_en: [synthesis, LFO, modulation, vibrato]
alias: [LFO, 低频振荡器, 颤音, 震音, low frequency oscillator]
links:
  - "[[glossary:modulation]]"
  - "[[glossary:timbre]]"
  - "[[instrument:moog-modular]]"
  - "[[period:modern]]"
instances:
  - oga-000009 | 持续铺底与海浪声交叠，缓慢起伏容易听出是颤音还是音量变化
  - oga-000067 | 长弦乐与金属铺底贯穿，颤音快慢对紧张感的影响明显
  - oga-000270 | 多层吉他与暖铺底并存，缓慢摆动的宽度可与其他层分开听
sources:
  - Gordon Reid, Sound On Sound Synth Secrets.
  - Curtis Roads, The Computer Music Tutorial.
updated: 2026-10-28
---

::: zh
## 为什么会用到它

低频振荡器自己不发声，却在几乎每台合成器上占一个旋钮。它到底做什么，为什么慢速运动能让音色活起来？

## 一层层看原理

LFO 是频率低于音频范围的振荡器，通常零点几到二十赫兹。它不直接进入耳朵，而是去推动别的参数。推到音高叫颤音，推到音量叫震音，推到滤波器截止叫摆动，推到声像叫左右，推到脉冲宽度叫脉宽调制。速率决定快慢，深度决定幅度，波形决定平滑、阶梯还是随机。延迟淡入可让长音先稳住再开始颤。

## 旋钮与耳朵

零点一到两赫兹适合缓慢漂移与呼吸感，四到七赫兹接近人声与小提琴的颤音，按拍同步的四分或八分适合有节奏的摆动。深度小则若有若无，深度大则夸张甚至失控。正弦最自然，方波呈阶梯，随机波形适合制造不安。

## 耳朵要抓的点

先听持续铺底，注意音色是否在缓慢开合，而不是音量在起伏。再听长弦乐，判断颤动是音高还是音量。最后把速率从零点三赫兹慢慢提高到六赫兹，听它从呼吸变成紧张，再变成明显的颤音。

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"缓慢起伏的铺底","label_en":"A pad drifting slowly","hint":"先听稳定的长音，再想象一个 0.3 Hz 的慢波在推动截止；音色会像呼吸一样开合","hint_en":"Hear the steady pad, then imagine a 0.3 Hz wave pushing the cutoff; the tone opens and closes like breathing"}
```

## 容易弄错的

把 LFO 等同于颤音，其实它还能推音量、滤波与声像；以为速率越快越有表现力，过快只会让人紧张；以为 LFO 不会改变音高，推到音高时它正是颤音的来源。
:::

::: en
## Why reach for it

A low-frequency oscillator makes no sound, yet almost every synth gives it a knob. What does it do, and why does slow motion bring a timbre alive?

## Inside the mechanism

An LFO runs below audio, usually from a fraction of a hertz to twenty hertz. It never reaches the ear directly; it pushes another parameter. To pitch it is vibrato, to level tremolo, to cutoff a wobble, to pan movement, to pulse width PWM. Rate sets speed, depth sets amount, and shape decides whether motion is smooth, stepped or random. A fade-in delay lets a long note settle first.

## Knobs and ears

Zero point one to two hertz suits slow drift and breathing. Four to seven hertz approaches the vibrato of a voice or a violin. Tempo-synced quarters or eighths give a rhythmic sway. A small depth is barely there, a large one exaggerated. Sine feels natural, square steps, and random shapes unsettle.

## What the ear should catch

Hear a sustained pad and ask whether the tone is opening and closing rather than the level rising and falling. Then hear long strings and decide whether the wobble is pitch or level. Finally raise the rate from 0.3 Hz to 6 Hz and hear it turn from breath to tension to obvious vibrato.

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"A pad drifting slowly","label_en":"A pad drifting slowly","hint":"Hear the steady pad, then imagine a 0.3 Hz wave pushing the cutoff; the tone opens and closes like breathing","hint_en":"Hear the steady pad, then imagine a 0.3 Hz wave pushing the cutoff; the tone opens and closes like breathing"}
```

## Easy to get wrong

That an LFO means vibrato, when it can push level, filter and pan; that faster is more expressive, when too fast only creates tension; that an LFO cannot change pitch, when pitch modulation is vibrato.
:::
