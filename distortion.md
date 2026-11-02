---
id: distortion
site: prod
cat: A7
title: 失真与过载
title_en: Distortion and Overdrive
summary: 三种削波程度如何改写谐波与动态，而不只是变脏。
summary_en: How three degrees of clipping rewrite harmonics and dynamics rather than merely adding dirt.
level: standard
tags: [效果器, 非线性, 失真, 谐波]
tags_en: [effects, nonlinear, distortion, harmonics]
alias: [失真, 过载, 模糊, 削波, distortion, overdrive, fuzz]
links:
  - "[[glossary:harmonics]]"
  - "[[glossary:clipping]]"
  - "[[instrument:electric-guitar]]"
instances:
  - cyberhymnal-000000 | 持续和弦的音符素材，可另渲染后施加削波 | Sustained-chord notes for separate rendering and clipping
  - oga-000004 | 铜管齐奏声部参照，未提供过载前后的版本 | Brass-unison parts without before-and-after overload
  - mutopia-000005 | 吉他音符素材，不包含真实拨弦录音中的指尖噪声 | Guitar-note material without recorded finger noise
sources:
  - Udo Zölzer, DAFX.
  - Julius O. Smith, Physical Audio Signal Processing, nonlinear distortion sections.
updated: 2026-11-02
---

::: zh
## 为什么会用到它

Distortion、overdrive与fuzz通常指不同设计和风格的非线性效果，不能排成同一算法由轻到重的三个档位。它们可能同时改变谐波、动态和频响，实际行为要看电路或算法。

## 背后的机制

非线性会产生输入中原本没有的频率分量。对称或不对称的传递曲线会影响谐波组成，但“奇次硬、偶次暖”不是可靠的通用听感定律。复杂和弦还会产生互调；输入电平、前后滤波和处理器内部设计共同决定结果。

## 旋钮与耳朵

一次改变输入或drive，匹配输出后听新增谐波与音头变化。处理贝斯时可把低频保留在干声支路，只对中高频支路失真，再检查分频与延迟对齐；若直接高通整条贝斯，会连基音一起削弱。并行量和tone按目标调整，不必固定为某个百分比。

## 耳朵要抓的点

从单音开始区分原有谐波与新增分量，再试双音和和弦，观察互调。用同一段干声比较旁通、全处理和并行混合，并检查峰值；预设失真音色不能代替一条可控的处理链。

```audiolab
{"type":"instrument","gm":"Distortion Guitar","synth":"plucked","phrase":["E2","E2","B2","B2","G3","G3","D3"],"label":"吉他和弦音色","label_en":"Guitar-chord timbre","hint":"预设失真吉他音色并非可切换的削波处理。要比较新增谐波，应把同一干声送入实际失真器再做旁通。","hint_en":"A distorted-guitar preset is not switchable clipping. Compare added harmonics by routing the same dry audio through an actual distortion processor."}
```

## 容易弄错的

以为失真只是变脏；以为数字失真一定不如模拟；以为 drive 越大越好。
:::

::: en
## Why reach for it

Distortion, overdrive and fuzz name nonlinear effects with different designs and styles, not three strengths of one algorithm. They may change harmonics, dynamics and frequency response together; behaviour depends on the circuit or algorithm.

## The mechanism

Nonlinearity creates frequency components absent from the input. Symmetric and asymmetric transfer curves affect harmonic content, but odd means hard and even means warm is not a universal listening rule. Complex chords also produce intermodulation. Input level, pre/post filtering and internal design all affect the result.

## Knobs and ears

Change input or drive one at a time and match output to judge harmonics and attacks. For bass, retain lows in a dry branch and distort a higher band if useful, checking crossover and delay alignment. High-passing the whole bass also removes fundamental energy. Set blend and tone for the goal rather than a fixed percentage.

## What the ear should catch

Start with one note to distinguish original and added components, then test two notes and chords for intermodulation. Compare bypass, wet and parallel versions of the same dry audio and check peaks. A distorted instrument preset is not a substitute for a controlled processing chain.

```audiolab
{"type":"instrument","gm":"Distortion Guitar","synth":"plucked","phrase":["E2","E2","B2","B2","G3","G3","D3"],"label":"Guitar-chord timbre","label_en":"Guitar-chord timbre","hint":"A distorted-guitar preset is not switchable clipping. Compare added harmonics by routing the same dry audio through an actual distortion processor.","hint_en":"A distorted-guitar preset is not switchable clipping. Compare added harmonics by routing the same dry audio through an actual distortion processor."}
```

## Easy to get wrong

That distortion only makes a sound dirty; that digital distortion must sound worse than analog; that more drive is always better.
:::
