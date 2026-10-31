---
id: sample-loops-and-crossfades
site: prod
cat: B4
title: 采样循环与交叉淡化
title_en: Sample Loops and Crossfades
summary: 循环点决定长音能否续住，交叉淡化决定接缝听不听得见。
summary_en: Loop points keep a sustained note alive; crossfades decide whether the seam is audible.
level: standard
tags: [循环, 交叉淡化, 采样器]
tags_en: [loop, crossfade, sampler]
alias: [循环点, 交叉淡化, loop point, crossfade loop]
links:
  - "[[glossary:sampler]]"
  - "[[glossary:timbre]]"
  - "[[instrument:samplers]]"
instances:
  - pdmx-000070 | 巴伯《弦乐柔板》的长弦音没有明显起音，循环点错位会听成脉动
  - cyberhymnal-000000 | 风琴持续和弦最容易暴露循环接缝
  - pdmx-000183 | 合唱长音的气口与颤音让交叉淡化更难藏
sources:
  - Curtis Roads, The Computer Music Tutorial — 用于核对循环与交叉淡化的做法。
  - Ken C. Pohlmann, Principles of Digital Audio — 用于核对采样回放的接缝与相位问题。
updated: 2026-10-28
---

::: zh
## 难在哪

一个只有两秒的样本，为什么能撑住十秒的和弦，而且听不出接缝？

## 工作方式

采样器在循环起点与终点之间反复播放，让声音持续。循环点若没有落在波形的整周期上，每次回头都会产生跳变，听起来像脉动或嗡嗡声。常见解法有两种，一是把循环点对齐到过零点或整周期，二是用交叉淡化，让尾部和头部重叠一段，平滑过渡。淡化太短会留下接缝，太长会把两个相位不同的波形叠在一起，产生梳状滤波，音色变薄。起音段通常不参与循环，循环只覆盖稳定段。

## 旋钮与做法

持续音样本的循环区放在波形最稳定的中段，长度取几个周期。交叉淡化从 20 到 80 毫秒起步，按音高调整，低音可以更长。对齐时先看波形再看频谱，别把拍频当成音色。循环点不要放在渐弱段，否则每次回头都听到音量回升。改完循环点，用连续长音检查一分钟。

## 耳朵要抓的点

听长弦音，注意有没有规律的起伏。听风琴和弦，接缝会让某个音头出现轻微的咔声。听合唱长音，交叉淡化过长时声音会变薄，像被挖掉中频。听低音持续音，循环错位时最容易听成颤音。

## 容易弄错的

以为循环点越短越省内存就越好；以为交叉淡化能掩盖任何接缝；以为循环只影响长度，不影响音色。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["D3","A3","D4"],"label":"长音能否续住","label_en":"Can the long note hold","hint":"按住长音的余韵，听它是否平稳；循环接缝只有在采样器里反复播放同一段时才会出现","hint_en":"Hold the long note and hear whether it stays steady; a loop seam only appears when a sampler repeats the same region"}
```
:::

::: en
## Where it gets hard

How does a two-second sample hold a ten-second chord without an audible seam?

## The working principle

The sampler repeats the region between loop start and loop end. If those points do not land on whole cycles, every return creates a jump that reads as pulsing or buzzing. Two fixes are common: align to zero crossings or whole periods, or crossfade so the tail overlaps the head. A short fade leaves a seam; a long one sums two out-of-phase waveforms and produces comb filtering, thinning the tone. The attack stays outside the loop, which covers only the steady portion.

## Knobs and practice

Place the loop in the most stable middle of the waveform and span several periods. Start crossfades at 20 to 80 ms and lengthen them for low notes. Align by eye on the waveform, then confirm on a spectrum so beating is not mistaken for character. Never loop inside a decaying section, or level will rise on every pass. After editing, audition a sustained note for a full minute.

## What the ear catches

Hear a long string note and listen for regular undulation. Hear an organ chord, where a seam may click at the attack of one voice. Hear a choir sustain, which thins like a scooped midrange when the crossfade is too long. Hear a low drone, where a misaligned loop is most easily heard as vibrato.

## Easy to get wrong

That a shorter loop always saves memory without cost; that a crossfade hides any seam; that looping affects length but not timbre.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["D3", "A3", "D4"], "label": "Can the long note hold", "label_en": "Can the long note hold", "hint": "Hold the long note and hear whether it stays steady; a loop seam only appears when a sampler repeats the same region", "hint_en": "Hold the long note and hear whether it stays steady; a loop seam only appears when a sampler repeats the same region"}
```
:::
