---
id: subtractive-synthesis
site: prod
cat: B3
title: 减法合成
title_en: Subtractive Synthesis
summary: 从富谐波波形出发，用滤波器与包络削出音色。
summary_en: Start with a harmonically rich waveform and carve the tone with a filter and envelope.
level: standard
tags: [合成, 减法, 滤波器, 包络]
tags_en: [synthesis, subtractive, filter, envelope]
alias: [减法合成, 模拟合成, subtractive, subtractive synthesis]
links:
  - "[[glossary:timbre]]"
  - "[[glossary:eq]]"
  - "[[instrument:minimoog]]"
  - "[[period:modern]]"
instances:
  - oga-000163 | 曲名与配器都指向锯齿主音，低通开合时明暗变化最直观
  - oga-000287 | 电子贝斯与锯齿主音分层，适合听滤波器怎样削掉高频
  - oga-000067 | 合成贝斯与方波、锯齿主音同场，滤波与共振的差别容易比较
sources:
  - Gordon Reid, Sound On Sound Synth Secrets — subtractive synthesis principles checked, not quoted
  - Udo Zölzer, DAFX — Digital Audio Effects, filters and oscillators chapter — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 难在哪

同样的振荡器，为什么有人做出铜管，有人做出风琴？减法合成要回答的是，音色不必从零叠加，可以先造一个谐波很满的波，再把不需要的部分削掉。

## 工作方式

锯齿波包含全部整数倍谐波，方波只有奇次谐波，两者都比正弦波亮。滤波器接在振荡器之后，低通把截止频率以上的成分滚降；在截止处提升共振，会让某一频带先被听见。包络再让截止频率随按键时间移动，音头因此可能比持续段更亮。音量包络同时塑形起音与释放，两者合起来决定「像什么」。

## 数值怎么变成声音

截止频率决定明暗，共振决定截止点附近的突出程度，包络量决定音头比持续段亮多少。截止低时声音发闷，慢慢抬高会先露出中频，再出现齿音般的边缘；共振过高会盖住基频，甚至啸叫。键盘跟踪让高音区自动开大截止，避免越往高越暗。

## 耳朵要抓的点

播一段锯齿和弦，把低通从 8 kHz 往下扫，注意不是音量变小，而是高频先退。再对比慢起音与快起音，前者像弦乐铺底，后者像拨弦。听贝斯时留意共振是否让某个音突出。

```audiolab
{"type":"instrument","gm":"Lead 2 (sawtooth)","synth":"bowed","phrase":["A3","C4","E4","A4"],"label":"锯齿和弦与滤波扫动","label_en":"Saw chord under a filter sweep","hint":"先听原样，再想象截止从 8 kHz 缓慢降到 300 Hz；听高频先退而不是音量先退","hint_en":"Hear it plain, then imagine the cutoff falling from 8 kHz to 300 Hz; the top goes before the level does"}
```

## 容易弄错的

以为减法合成只能模仿老式模拟琴；把共振当成越多越好的亮度开关；忽略滤波器也会改变响度与相位，叠层时因此对不齐。
:::

::: en
## Where it gets hard

Why does the same oscillator become a brass section in one patch and a harmonica in another? Subtractive synthesis starts with a harmonically rich wave and removes what the ear does not need.

## The working principle

A sawtooth contains every integer harmonic, a square the odd ones, and both are brighter than a sine. A filter follows the oscillator; a low-pass rolls off everything above the cutoff. Resonance at the cutoff makes one band speak first. An envelope moves the cutoff over time, so the attack can be brighter than the sustain. A second envelope shapes level, and together they decide what instrument the ear hears.

## From numbers to sound

Cutoff sets brightness, resonance sets emphasis around the cutoff, and envelope amount sets how much brighter the attack is. A low cutoff sounds muffled; raising it reveals midrange and an edgy top. Too much resonance masks the fundamental and can whistle. Key tracking opens the cutoff in the high register so the top notes do not go dull.

## What the ear should catch

Play a saw chord and sweep the low-pass down. Notice the level hardly drops while the top disappears. Compare a slow attack with a fast one; the first reads as a pad, the second as a pluck. On bass, hear whether resonance makes a note jump out.

```audiolab
{"type":"instrument","gm":"Lead 2 (sawtooth)","synth":"bowed","phrase":["A3","C4","E4","A4"],"label":"Saw chord under a filter sweep","label_en":"Saw chord under a filter sweep","hint":"Hear it plain, then imagine the cutoff falling from 8 kHz to 300 Hz; the top goes before the level does","hint_en":"Hear it plain, then imagine the cutoff falling from 8 kHz to 300 Hz; the top goes before the level does"}
```

## Easy to get wrong

That subtractive synthesis only imitates old analogue synths; that resonance is a brightness control; that a filter changes only tone, when it also shifts level and phase.
:::
