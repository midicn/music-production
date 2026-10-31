---
id: formant-synthesis
site: prod
cat: B3
title: 形式合成
title_en: Formant Synthesis
summary: 用几个共振峰代替滤波器，让合成器唱出元音。
summary_en: Replace the filter with a few resonant peaks and a synth can sing vowels.
level: standard
tags: [合成, 形式, 元音, 共振峰]
tags_en: [synthesis, formant, vowel, resonance]
alias: [形式合成, 共振峰合成, 元音合成, formant synthesis]
links:
  - "[[glossary:timbre]]"
  - "[[glossary:synthesizer]]"
  - "[[instrument:vocoder]]"
  - "[[period:contemporary]]"
instances:
  - oga-000008 | 合唱音色贯穿全曲，元音般的共振峰最容易听出
  - oga-000135 | 合唱铺底连奏整段，峰位移动带来的元音变化清楚
  - oga-000040 | 合唱与打击乐并置，人声的喉音与气声可分开听
sources:
  - Miller Puckette, The Theory and Technique of Electronic Music.
  - Curtis Roads, The Computer Music Tutorial.
updated: 2026-10-28
---

::: zh
## 为什么会用到它

人声唱「啊」和「呜」时，声带给的音高差不多，差别全在口腔的共振。合成器能不能不录人声，只靠几个峰就做出元音？

## 声音是怎么来的

元音的能量集中在几个共振峰上，第一峰约在 300 至 800 Hz，第二峰约在 800 至 2500 Hz，第三峰再往上。形式合成不去模拟声带波形，而是把一串谐波送进几个窄带谐振器，峰的位置决定听到哪个元音。峰越窄越高，元音越清楚；峰太宽则像含混的哼声。声码器走的是另一条路，用真实人声去控制滤波器组，但两者都靠共振峰工作。

## 旋钮与耳朵

第一峰抬高会让声音更「喉」，第二峰前移会让「啊」偏向「诶」。峰的带宽决定清晰度，窄带宽像机器在念字，宽带像捂着嘴唱。加一点气声噪声会更像人，但太多会盖住音高。滑音从一个元音过渡到另一个元音时，峰要跟着移动，否则会听见断裂。

## 耳朵要抓的点

先听合唱铺底的长音，注意它有一种「有字但听不清」的感觉。再听哨音，窄峰让高音像「呜」。最后对比纯锯齿，锯齿没有峰，所以只是亮，不会像在唱。

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["A3","E4","A4","E5"],"label":"共振峰堆出的元音","label_en":"Vowels built from formant peaks","hint":"先听合唱长音，再想象只留下第一峰与第二峰；峰位一改，同一个音会从「啊」滑向「呜」","hint_en":"Hear the choir tone, then imagine keeping only the first two peaks; moving them slides the same note from an ah toward an oo"}
```

## 容易弄错的

以为形式合成只能做人声；以为峰越多越像人，其实前两峰最关键；把它和声码器混为一谈。
:::

::: en
## Why reach for it

A singer's pitch barely changes between an ah and an oo; the difference lies in the mouth's resonances. Can a synth make vowels from a few peaks without recording a voice?

## Where the sound comes from

Vowel energy gathers around a few formants. The first sits near 300 to 800 Hz, the second near 800 to 2500 Hz. Formant synthesis does not mimic the vocal folds; it feeds a harmonic source into narrow resonators, and peak positions decide which vowel is heard. Narrow, tall peaks make the vowel clear; broad peaks turn it into a vague hum. A vocoder uses a real voice to control a filter bank, but both depend on formants.

## Knobs and ears

Lifting the first peak makes the tone throatier; moving the second forward pulls an ah toward an eh. Peak bandwidth sets intelligibility: narrow reads as a machine speaking, wide as singing behind a hand. A little breath noise adds humanity, but too much masks the pitch. When a glide moves between vowels, the peaks must travel too or the sound breaks.

## What the ear should catch

Hear a choir pad and notice that it seems to hold words without saying them. Then hear a whistle-like tone, where a narrow peak makes the top sound like oo. Finally compare a plain sawtooth; it has no peaks, so it is only bright and never seems to sing.

```audiolab
{"type": "instrument", "gm": "Choir Aahs", "synth": "vocal", "phrase": ["A3", "E4", "A4", "E5"], "label": "Vowels built from formant peaks", "label_en": "Vowels built from formant peaks", "hint": "先听合唱长音，再想象只留下第一峰与第二峰；峰位一改，同一个音会从「啊」滑向「呜」", "hint_en": "Hear the choir tone, then imagine keeping only the first two peaks; moving them slides the same note from an ah toward an oo"}
```

## Easy to get wrong

That formant synthesis can only imitate voices; that more peaks sound more human, when the first two matter most; that it is the same thing as a vocoder.
:::
