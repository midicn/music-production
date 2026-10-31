---
id: phase-distortion
site: prod
cat: B3
title: 相位失真
title_en: Phase Distortion
summary: 不改波形，只改相位，就能让正弦长出锯齿般的亮度。
summary_en: Keep the waveform and bend its phase; a sine gains the edge of a sawtooth.
level: standard
tags: [合成, 相位失真, 数字合成, 波形]
tags_en: [synthesis, phase distortion, digital, waveform]
alias: [相位失真, 相位扭曲, phase distortion, PD 合成]
links:
  - "[[glossary:timbre]]"
  - "[[glossary:synthesizer]]"
  - "[[instrument:software-synth]]"
  - "[[period:modern]]"
instances:
  - oga-000101 | 金属铺底与钢琴同场，硬亮边缘不靠滤波扫出
  - oga-000270 | 吉他泛音与金属铺底叠置，高频边缘比常规锯齿更硬
  - oga-000160 | 钢鼓与卡林巴并置，硬亮瞬态适合对照相位折线
sources:
  - Casio CZ-101 Owner's Manual.
  - Curtis Roads, The Computer Music Tutorial.
updated: 2026-10-28
---

::: zh
## 起点：一个问题

滤波靠削掉高频来变暗，相位失真却能在不削任何东西时让正弦变亮。它改了什么，为什么像锯齿却没有整齐的谐波？

## 它怎么工作

相位失真把一个周期内的读取速度加快或减慢，相当于给相位加了一条折线。波形本身仍是正弦，但周期内的相位不再匀速，于是谐波被重新分配，出现类似锯齿或方波的边缘。Casio 的 CZ 系列用数字查表实现这件事，调制的是读取相位而不是频率。波表换整张波形，相位失真只改读取轨迹。因为不经过滤波器，高频可以一直保留到很靠上的位置。

## 数值怎么变成声音

失真量小时，音色只是稍微变硬；推大后会出现明显的谐振峰与金属感。把相位折点对准不同位置，会产生类似人声元音或木管的共振。包络推动失真量，可以让音头很硬、尾巴变软。折点过陡时会有刺耳的高频，音量也容易突然增大。

## 耳朵要抓的点

先听一个纯正弦，再听加了相位失真的版本，注意亮度增加但基频没变。然后听它和锯齿的区别：相位失真的高次谐波更不规则，像加了金属味。最后听音头，失真量随包络下降时，声音会从硬变圆。

```audiolab
{"type":"instrument","gm":"Lead 3 (calliope)","synth":"reed","phrase":["C4","E4","G4","C5"],"label":"正弦被相位折线推亮","label_en":"A sine brightened by a phase bend","hint":"先听主音的硬边，再想象把失真量关小；亮度会退成接近正弦的圆润，而基频不动","hint_en":"Hear the hard edge, then imagine reducing the distortion amount; the tone rounds toward a sine while the fundamental stays put"}
```

## 容易弄错的

以为相位失真等于相位器；以为它必须靠滤波器收尾；以为数字合成一定冷硬，其实它可以做得很圆。
:::

::: en
## Starting point: a problem

A filter darkens by removing highs, yet phase distortion brightens a sine without removing anything. What changes, and why does it read as a sawtooth without orderly harmonics?

## How it works

Phase distortion speeds up or slows the read-through of one cycle, drawing a bend into the phase. The wave is still a sine, but phase no longer advances evenly, so energy is redistributed and saw-like edges appear. Casio's CZ range did this with digital lookup tables, modulating the read phase rather than the frequency. A wavetable swaps the whole wave; phase distortion changes only the reading path. Without a filter, high partials survive far up.

## From numbers to sound

At low amounts the tone merely hardens. Push further and a clear resonant peak and metallic colour appear. Placing the phase break at different points produces vowel-like or woody resonances. An envelope on the distortion amount can make the attack hard and the tail soft. Very steep bends add harsh highs, and the level can jump.

## What the ear should catch

Hear a pure sine, then the distorted version; brightness rises while the fundamental stays fixed. Compare it with a sawtooth; its upper partials are less regular and carry a metallic taste. Last, hear the attack: as the amount falls with the envelope, the sound rounds off.

```audiolab
{"type": "instrument", "gm": "Lead 3 (calliope)", "synth": "reed", "phrase": ["C4", "E4", "G4", "C5"], "label": "A sine brightened by a phase bend", "label_en": "A sine brightened by a phase bend", "hint": "先听主音的硬边，再想象把失真量关小；亮度会退成接近正弦的圆润，而基频不动", "hint_en": "Hear the hard edge, then imagine reducing the distortion amount; the tone rounds toward a sine while the fundamental stays put"}
```

## Easy to get wrong

That phase distortion is a phaser; that it needs a filter; that digital synthesis must be cold, when it can be round and vocal.
:::
