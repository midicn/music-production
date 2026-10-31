---
id: filter-and-resonance
site: prod
cat: B3
title: 滤波器与共振
title_en: Filters and Resonance
summary: 截止决定明暗，共振决定截止点附近谁先被听见。
summary_en: Cutoff sets brightness; resonance decides which band around the cutoff speaks first.
level: standard
tags: [合成, 滤波器, 共振, 截止]
tags_en: [synthesis, filter, resonance, cutoff]
alias: [滤波器与共振, 截止频率, 滤波器共振, resonance, filter cutoff]
links:
  - "[[glossary:timbre]]"
  - "[[instrument:minimoog]]"
  - "[[instrument:moog-modular]]"
  - "[[period:modern]]"
instances:
  - oga-000163 | 锯齿主音持续音多，推高截止时谐波会一层层露出
  - oga-000286 | 锯齿主音与两种合成贝斯同场，低频共振的突出感容易比较
  - oga-000111 | 锯齿低音与音乐盒高音对照，截止高低造成的明暗差别明显
sources:
  - Gordon Reid, Sound On Sound Synth Secrets — filter and resonance behaviour checked, not quoted
  - Udo Zölzer, DAFX — Digital Audio Effects, filter chapter checked, not quoted
updated: 2026-10-28
---

::: zh
## 起点：一个问题

同样一条锯齿波，截止调低像蒙住，调高又刺耳；共振一加，某个音突然跳到前面。滤波器到底在做什么，为什么这两个旋钮总是一起动？

## 工作方式

低通让截止以下的频率通过，以上的按固定斜率滚降，常见每倍频程 12 或 24 dB。截止不是一刀切，拐点附近仍有过渡。共振在截止处制造一个峰，把该频段抬高；峰越窄越高，听感越像「哇」或「哨」。高通、带通与陷波只是把通过区换到别处。滤波器还会改变相位，叠层时可能对不齐。数字滤波器在高截止、高共振时容易自激，音量会突然变大。

## 旋钮与耳朵

截止下移，先失去齿音与空气感，再失去中频细节，最后只剩低频。共振适中时音色有咬字感，过高会盖住基频，甚至自己发声。包络量决定音头比持续段开多少，键盘跟踪让高音区自动开大截止。斜率越陡，扫动越像开关；越缓，过渡越自然。

## 耳朵要抓的点

播一段持续锯齿音，把截止从高往低扫，注意音量变化不大而亮度先退。再把共振从零慢慢推高，听某个音是否开始突出，低频是否变得有鼻音。最后比较 12 dB 与 24 dB，前者扫动柔和，后者更像硬切。

```audiolab
{"type":"instrument","gm":"Lead 2 (sawtooth)","synth":"bowed","phrase":["A3","C4","E4","A4"],"label":"截止与共振的两次扫动","label_en":"Two sweeps of cutoff and resonance","hint":"先听原始的亮，再想象截止降到 400 Hz；共振推高时注意某个音先跳出来，而不是整体变响","hint_en":"Hear the bright source, then imagine the cutoff at 400 Hz; as resonance rises one note jumps forward rather than the whole sound getting louder"}
```

## 容易弄错的

以为截止就是音量旋钮；以为共振只是「更亮」；忽略滤波器有斜率与相位，叠两层时明暗与时间对齐会一起变。
:::

::: en
## Starting point: a problem

The same sawtooth sounds muffled with the cutoff low and harsh with it high; add resonance and one note steps forward. Why do these two controls move together?

## The working principle

A low-pass lets everything below the cutoff through and rolls off the rest at a fixed slope, often 12 or 24 dB per octave. The cutoff is no brick wall. Resonance creates a peak at the cutoff and lifts that band; a narrow, tall peak reads as a howl or whistle. High-pass, band-pass and notch move the passing region elsewhere. The filter also shifts phase, so stacked layers may lose alignment. At high cutoff and strong resonance a digital filter can self-oscillate.

## Knobs and ears

As the cutoff falls, sibilance and air go first, then midrange detail, until only lows remain. Moderate resonance gives a vocal edge; too much masks the fundamental. Envelope amount sets how much brighter the attack is, and key tracking opens the cutoff up high. A steep slope sweeps like a switch; a gentle one stays natural.

## What the ear should catch

Play a sustained sawtooth and sweep the cutoff down. The level barely changes while the top disappears. Raise resonance and hear whether one note stands out or the low end turns nasal. Compare 12 dB and 24 dB; the first sweeps softly, the second cuts harder.

```audiolab
{"type": "instrument", "gm": "Lead 2 (sawtooth)", "synth": "bowed", "phrase": ["A3", "C4", "E4", "A4"], "label": "Two sweeps of cutoff and resonance", "label_en": "Two sweeps of cutoff and resonance", "hint": "先听原始的亮，再想象截止降到 400 Hz；共振推高时注意某个音先跳出来，而不是整体变响", "hint_en": "Hear the bright source, then imagine the cutoff at 400 Hz; as resonance rises one note jumps forward rather than the whole sound getting louder"}
```

## Easy to get wrong

That cutoff is volume; that resonance means brighter; that a filter changes tone only, when slope and phase alter blend and timing.
:::
