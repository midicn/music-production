---
id: interactive-adaptive-music
site: prod
cat: A9
title: 交互音乐与自适应音频
title_en: Interactive and Adaptive Music
summary: 分层、分支与参数化，让音乐随战斗强度与探索状态连续变化。
summary_en: Layers, branches and parameters let music change continuously with combat intensity and exploration.
level: standard
tags: [交互音乐, 自适应音频, 分层, 状态切换, 游戏]
tags_en: [interactive music, adaptive audio, layering, state change, games]
alias: [交互音乐, 自适应音乐, interactive music, adaptive music]
links:
  - "[[glossary:stems]]"
  - "[[glossary:automation]]"
  - "[[glossary:cue]]"
instances:
  - oga-000004 | 战斗曲 battle 01，可作高强度层的参考，听鼓组与低音如何维持推力
  - oga-000031 | 氛围循环 creepy-ambient-loop，适合当作低强度层，观察它如何长期不抢注意力
  - oga-000011 | Boss 曲 boss 01，材料更密，可对比普通战斗与 Boss 战的分层差别
sources:
  - Collins, Karen，Game Sound（MIT Press）— 自适应与交互音乐分类核对，未引用
  - Marks, Aaron，The Complete Guide to Game Audio（Focal Press）— 分层与过渡实现核对，未引用
updated: 2026-10-28
---

::: zh
自适应音乐把一条曲子拆成若干层或若干段，由游戏状态决定哪一层响起、哪一段接上。玩家听到的是一个连续变化的结果。

## 问题

如果战斗开始就硬切一首新曲，音乐会打断沉浸感。如果始终播放同一首，强度又跟不上局势。自适应要解决的是切换的平滑与状态的可读性。

## 交互或流程

常见做法是垂直分层与水平重组。垂直分层让同一段音乐的高强度层随时淡入，水平重组则在段落之间跳转。参数可以是生命值、敌人数量或距离。设计时先定状态，再定每层负责什么，最后才写音符。

## 做法与判断

层数控制在三到五层，每层都要能单独成立。切换阈值留出迟滞，避免玩家在边界来回触发。判断标准是闭眼听能否说出当前状态；若说不出来，说明层的区分不够，而不是音量不够。

## 听什么

听战斗曲的鼓与低音怎样单独撑住节奏，听氛围循环怎样在长时间里保持稳定，再听 Boss 曲多出来的高频与打击乐。演示用弦乐叠一个长音，再逐层加入，听感如何从安静变成紧张。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C3","G3","C4","E4","G4","C5"],"label":"逐层加入的弦乐","label_en":"Strings entering layer by layer","hint":"每两个音当作一层，听厚度怎样改变紧张度","hint_en":"Hear each pair of notes as a layer, and how thickness changes the tension"}
```

## 常见误解

自适应不是随机播放，规则必须可预测。分层越多也不越好，层数过多会让混音失去空间。另一点，过渡时间通常以毫秒到几秒计，写得太快会像故障。
:::

::: en
Adaptive music splits a piece into layers or segments, and the game state decides which layer sounds and which segment comes next. What the player hears is a continuous result.

## The problem

Hard-cutting to a new track when combat starts breaks immersion. One track throughout fails to follow the situation. Adaptive music must make transitions smooth and states legible.

## Interaction or workflow

The usual methods are vertical layering and horizontal re-sequencing. Vertical layering fades a high-intensity layer in and out of the same music; horizontal re-sequencing jumps between segments. Parameters can be health, enemy count or distance. Define the states and each layer's role before writing notes.

## Practice and judgement

Keep three to five layers, each able to stand alone. Add hysteresis to the switch thresholds so the player cannot trigger them back and forth at the boundary. The test is whether a listener with eyes closed can name the state. If not, the layers are not distinct enough; the answer is not more volume.

## What to listen for

Hear drums and bass hold the rhythm alone in the battle cue, the ambient loop stay steady over a long stretch, and the boss cue add high end and percussion. The demo stacks a string chord one layer at a time; hear the mood turn from calm to tense.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C3", "G3", "C4", "E4", "G4", "C5"], "label": "Strings entering layer by layer", "label_en": "Strings entering layer by layer", "hint": "每两个音当作一层，听厚度怎样改变紧张度", "hint_en": "Hear each pair of notes as a layer, and how thickness changes the tension"}
```

## Common misunderstandings

Adaptive is not random playback; its rules must be predictable. More layers are not better, since too many leave no room in the mix. Transitions are measured in milliseconds to seconds; too fast sounds like a glitch.
:::
