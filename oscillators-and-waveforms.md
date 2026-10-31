---
id: oscillators-and-waveforms
site: prod
cat: B3
title: 振荡器与波形
title_en: Oscillators and Waveforms
summary: 波形是一张谐波配方，决定音色的底色与滤波起点。
summary_en: A waveform is a harmonic recipe that sets the base colour and where filtering begins.
level: standard
tags: [合成, 振荡器, 波形, 谐波]
tags_en: [synthesis, oscillator, waveform, harmonics]
alias: [振荡器, 波形, 锯齿波, 方波, oscillator, waveform]
links:
  - "[[glossary:timbre]]"
  - "[[glossary:eq]]"
  - "[[instrument:prophet-5]]"
  - "[[period:modern]]"
instances:
  - oga-000013 | 方波主音在失真吉他之上仍可辨认，空心感来自缺少偶次谐波
  - oga-000163 | 锯齿主音谐波连续，与同曲的陶笛音色对照最清楚
  - oga-000334 | 单声部气氛铺底音色柔和，适合与方波、锯齿的锐利边缘对照
sources:
  - Gordon Reid, Sound On Sound Synth Secrets — waveform spectra checked, not quoted
  - Udo Zölzer, DAFX — Digital Audio Effects, oscillators and aliasing chapter — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 为什么会用到它

合成器面板上第一个旋钮常常是波形。正弦、三角、方波、锯齿都能当起点，可它们究竟差在哪里，为什么换一个波形整条音色就变了？

## 它怎么工作

任何周期波都能拆成基频与整数倍谐波。正弦只有基频；三角波含奇次谐波且幅度按次数平方衰减，听感柔和；方波也只含奇次，但幅度按次数衰减，空洞而有木管感；锯齿含全部谐波，最亮也最粗糙。脉冲波的占空比会改变谐波分布，窄脉冲更薄更尖。实际振荡器还要处理混叠，高音区尤其明显。

## 数值怎么变成声音

波形决定基础亮度与谐波的奇偶，八度决定音区，微调与失谐让多个振荡器相互拍频，宽度因此变厚。脉冲宽度从一半收窄时，声音先变薄再变尖。锯齿适合主音与贝斯，方波适合空心主音，三角适合柔和铺底。

## 耳朵要抓的点

先单独听方波与锯齿的同一个音，再各加低通。方波缺少偶次谐波，滤波后更容易留下空洞感；锯齿的谐波连续，扫动时过渡更顺。听两个失谐锯齿，注意拍频让声音变宽，也让它变脏。

```audiolab
{"type":"instrument","gm":"Lead 1 (square)","synth":"bowed","phrase":["A4","C5","E5","A5"],"label":"方波主音","label_en":"A square-wave lead","hint":"先听方波的空心感，再想象同一条旋律换成锯齿；高频会更满，边缘也更糙","hint_en":"Hear the hollow square, then imagine the same line on a saw; the top fills in and the edge roughens"}
```

## 容易弄错的

以为波形只影响音色、不影响滤波后的表现；以为锯齿一定更响，其实亮度与响度不是一回事；以为相位无所谓，叠层时相位会改变瞬态。
:::

::: en
## Why reach for it

The first knob on many synths is the waveform. Sine, triangle, square and saw can all be a starting point, so what differs, and why does a change recolour everything?

## How it works

Any periodic wave splits into a fundamental and integer harmonics. A sine has only the fundamental. A triangle carries odd harmonics falling as the square of the number, so it reads soft. A square also carries odd harmonics, falling more slowly, which gives the hollow, woody tone. A saw carries every harmonic and is the brightest and roughest. Pulse width redistributes the harmonics, and a narrow pulse sounds thinner and sharper. Real oscillators must manage aliasing, especially high up.

## From numbers to sound

Waveform sets brightness and whether even harmonics exist. Octave sets register; fine tune and detune make oscillators beat and thicken the width. Narrowing pulse width first thins, then sharpens. Saws suit leads and basses, squares hollow leads, triangles soft pads.

## What the ear should catch

Hear a square and a saw on the same note, then add a low-pass to each. The square lacks even harmonics, so it keeps a hollow core after filtering; the saw has continuous harmonics and sweeps smoothly. Detune two saws and notice the beating widen the sound and dirty it at the same time.

```audiolab
{"type":"instrument","gm":"Lead 1 (square)","synth":"bowed","phrase":["A4","C5","E5","A5"],"label":"A square-wave lead","label_en":"A square-wave lead","hint":"Hear the hollow square, then imagine the same line on a saw; the top fills in and the edge roughens","hint_en":"Hear the hollow square, then imagine the same line on a saw; the top fills in and the edge roughens"}
```

## Easy to get wrong

That waveform affects only tone and not how a filter behaves; that a saw is always louder, when brightness and level are different things; that phase is irrelevant, when it changes transients in stacked layers.
:::
