---
id: hybrid-synthesis
site: prod
cat: B3
title: 混合合成
title_en: Hybrid Synthesis
summary: 采样与合成各取一半，既要有真实感，也要能变形。
summary_en: Take half a sample and half a synth, keeping the realism while gaining the ability to morph.
level: standard
tags: [合成, 混合, 采样, 数字]
tags_en: [synthesis, hybrid, sampling, digital]
alias: [混合合成, 采样加合成, 混合音源, hybrid synthesis]
links:
  - "[[glossary:synthesizer]]"
  - "[[glossary:sampler]]"
  - "[[instrument:dx7-fm]]"
  - "[[period:contemporary]]"
instances:
  - oga-000270 | 采样吉他、方波主音与暖铺底同场，两种音源互相补位
  - oga-000327 | 失真吉他、弦乐与锯齿主音叠置，采样与合成共用一个编曲
  - oga-000319 | 方波、锯齿与合成弦乐并置，电子音色里仍有钢琴与贝斯
sources:
  - Curtis Roads, The Computer Music Tutorial — hybrid synthesis checked, not quoted
  - Udo Zölzer, DAFX — Digital Audio Effects, hybrid instruments checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

采样像照片，真实但不便变形；合成像素描，可改但缺细节。混合合成把两者放进同一台乐器，问题是它们怎样分工才不互相打架。

## 原理

常见做法有三种：采样过合成器的滤波器与包络，让录音获得新的动态；合成层叠在采样上，补足低频或高频；用采样触发合成，例如用真实音头带动合成尾音。数字合成器时代，采样与 FM、波表共用一套键盘与调制。分工的关键在频段与时间：采样负责音头与噪声，合成负责持续段与变形，或者反过来。

## 参数与听感

两层同时起音会显得厚，但相位与音量稍有不齐就会糊。采样层做音头、合成层做尾巴时，衔接点的音量要平滑，否则听见「换了一个音」。滤波与包络同时作用于两层时，参数翻倍，调试要一层一层来。失谐会让两层拍频，适度变宽，过度则音高不稳。

## 听什么

先听钢琴与合成铺底的叠加，注意真实音头与合成尾巴的接缝。再听失真吉他配锯齿主音，判断哪一层在提供中频。最后听电子曲里的贝斯，是采样贝斯还是合成贝斯，往往靠音头与尾音判断。

```audiolab
{"type":"instrument","gm":"Electric Piano 1","synth":"struck","phrase":["C4","E4","G4","B4"],"label":"采样层与合成层的分工","label_en":"A sample layer and a synth layer dividing the work","hint":"先按真实音色听采样层，再按合成近似听合成层；混合时让采样管音头、合成管尾音，接缝才不突兀","hint_en":"Play the real timbre for the sample layer, then the synth approximation; let the sample own the attack and the synth the tail so the seam stays smooth"}
```

## 常见误解

以为混合就是简单叠两层；以为采样层一定更真实；忽略相位、音量与包络的衔接。
:::

::: en
## The question

A sample is a photograph, realistic but hard to reshape; a synth is a sketch, flexible but short on detail. Hybrid synthesis puts both in one instrument, and the question is the division of work.

## How it works

A sample can pass through the synth's filter and envelope for new dynamics. A synth layer can fill missing low or high energy. A sample can trigger a synth, so a real attack leads into a synthetic tail. Samples now share one keyboard and modulation system with FM and wavetables. The division follows frequency and time: the sample owns attack and noise, the synth owns sustain and transformation, or the reverse.

## Settings and what you hear

Two layers starting together sound thick, but a small phase or level mismatch muddies them. When the sample supplies the attack and the synth the tail, level must be smooth at the join or it sounds like another note. Filter and envelope on both layers double every adjustment, so tune one at a time. Detuning makes layers beat; a little widens the tone, too much makes pitch unstable.

## What to listen for

Hear a piano layered with a pad and listen for the seam between attack and tail. Then hear distorted guitars with a saw lead and decide which layer supplies midrange. Finally hear the bass; whether it is sampled or synthesized usually shows in attack and tail.

```audiolab
{"type": "instrument", "gm": "Electric Piano 1", "synth": "struck", "phrase": ["C4", "E4", "G4", "B4"], "label": "A sample layer and a synth layer dividing the work", "label_en": "A sample layer and a synth layer dividing the work", "hint": "先按真实音色听采样层，再按合成近似听合成层；混合时让采样管音头、合成管尾音，接缝才不突兀", "hint_en": "Play the real timbre for the sample layer, then the synth approximation; let the sample own the attack and the synth the tail so the seam stays smooth"}
```

## Common misconceptions

That hybrid means stacking two layers; that the sampled layer is always more realistic; that phase and level joins need no attention.
:::
