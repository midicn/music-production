---
id: granular-sampling
site: prod
cat: B4
title: 粒子采样
title_en: Granular Sampling
summary: 把采样切成毫秒级颗粒再重组，能拉长、冻结，也能做出云雾般的质感。
summary_en: Chop a sample into millisecond grains and reassemble them to stretch, freeze or cloud the sound.
level: standard
tags: [粒子采样, 时间拉伸, 声音设计, 采样]
tags_en: [granular sampling, time stretch, sound design, sampling]
alias: [粒子采样, 颗粒合成, granular, 粒子]
links:
  - "[[glossary:sampler]]"
  - "[[glossary:sample-rate]]"
  - "[[glossary:timbre]]"
instances:
  - atepp-005388 | 拉威尔《绞刑架》的钢琴尾音，粒子处理能把余韵拉成持续音（C1）
  - cyberhymnal-000000 | 管风琴赞美诗的长音，颗粒化后变成缓慢起伏的声云（C1）
  - groove-000003 | 80 BPM 灵魂乐鼓循环，粒子处理可以把瞬态打散成节奏纹理（C1）
sources:
  - 粒子合成的窗函数与重叠原理——依据来自声音设计公开资料。
  - 颗粒长度与音色变化的关系，对照数字音频惯例整理。
updated: 2026-10-28
---

::: zh
## 为什么会用到

想把一段录音拉长十倍又不改变音高，或想把一个和弦冻结成永不消失的云，常规的时间拉伸做不到，或者做出来满是金属味。粒子采样换了一个思路：不处理整段波形，而是把它切成无数短颗粒，再按新的时间与音高重新排布。

## 它怎么工作

每个颗粒只有几毫秒到一百多毫秒，带窗函数，避免切口产生咔嗒。颗粒按重叠方式排列，重叠越多越平滑，越少越有颗粒感。播放位置可以扫描、随机或冻结，扫描速度决定是拉长还是压缩。颗粒长度影响音色：太短会失去低频，太长会听出原来的音高片段。多个颗粒叠加时相位不一致，会产生梳状滤波与随机干涉。

## 参数与做法

先选颗粒长度，再从短到长试。重叠比例决定平滑度，声云用高重叠，节奏纹理用低重叠。扫描速度为零就是冻结，慢速正向扫描是拉长。加随机偏移可以打散金属感，但过多会失去音高感。用滤波与包络塑形，别指望粒子本身给出清晰的低频。处理后的素材适合做铺底、过渡与音效，不一定适合做主旋律。

## 耳朵要抓的点

在钢琴尾音里听余韵如何被拉成持续音，在管风琴长音里听声云的起伏，在鼓循环里听瞬态如何被打散成纹理。粒子处理的声音往往介于乐器与噪声之间，听的是质感而不是音高。

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"blown","phrase":["C3","G3","C4","E4","G4","E4","C4","G3"],"label":"拉长的声云","label_en":"A stretched cloud","hint":"每个音都被拉成一片，听颗粒重叠带来的流动感","hint_en":"Each note becomes a sheet of sound; hear the drift from overlapping grains"}
```
:::

::: en
## Why you reach for it

Stretching a recording tenfold without changing pitch, or freezing a chord into a cloud that never fades, is beyond ordinary time stretching, which either fails or leaves a metallic residue. Granular sampling takes another route: instead of processing the whole waveform, it cuts the sound into countless short grains and rearranges them in new time and pitch.

## How it works

Each grain lasts from a few milliseconds to over a hundred, shaped by a window so the cuts do not click. Grains overlap, and more overlap means smoother while less means grainier. The read position can scan, randomise or freeze, and scan speed decides whether the result stretches or compresses. Grain length shapes timbre: too short loses low end, too long reveals fragments of the original pitch. Overlapping grains are not phase-aligned, so comb filtering and random interference appear.

## Settings and practice

Choose grain length first and try short before long. Overlap sets smoothness: high for clouds, low for rhythmic texture. Zero scan speed freezes; slow forward scanning stretches. Add random offset to break up the metallic edge, but not so much that pitch dissolves. Shape with filters and envelopes rather than expecting grains to supply clear bass. The result suits beds, transitions and effects more than lead melodies.

## What the ear catches

In the piano tail, how the decay stretches into a sustained tone; in the organ, the drift of the cloud; in the drum loop, how transients scatter into texture. Granular sound sits between instrument and noise, and what you listen for is texture rather than pitch.

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"blown","phrase":["C3","G3","C4","E4","G4","E4","C4","G3"],"label":"A stretched cloud","label_en":"A stretched cloud","hint":"Each note becomes a sheet of sound; hear the drift from overlapping grains","hint_en":"Each note becomes a sheet of sound; hear the drift from overlapping grains"}
```
:::
