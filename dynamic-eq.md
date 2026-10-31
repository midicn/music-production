---
id: dynamic-eq
site: prod
cat: A7
title: 动态 EQ
title_en: Dynamic EQ
summary: 只在超过阈值时动某个频段，比静态 EQ 更少误伤。
summary_en: A band that moves only above a threshold, doing less collateral damage than a static EQ.
level: standard
tags: [效果器, 均衡, 动态, 共鸣]
tags_en: [effects, equalization, dynamics, resonance]
alias: [动态 EQ, 动态均衡, 动态均衡器, dynamic eq, dynamic equalizer]
links:
  - "[[glossary:eq]]"
  - "[[glossary:compressor]]"
  - "[[instrument:voice]]"
instances:
  - mutopia-000546 | 女声与钢琴同段，强句时 3 kHz 附近的突起只在那一刻需要压
  - groove-000002 | 灵魂乐鼓循环的底鼓有固定共鸣，弱击时不该被一起切掉
  - giantmidi-000000 | 夜曲低音区的轰鸣只在大声和弦出现，动态 EQ 可只处理强奏
sources:
  - Udo Zölzer, DAFX.
  - Bristow-Johnson, Cookbook Formulae for Audio EQ Biquad Filter Coefficients.
updated: 2026-10-28
---

::: zh
## 起点：一个问题

静态 EQ 一旦切下去，安静段和响亮段都被切。动态 EQ 只在电平超过阈值时改变某个频段，像一位只在需要时伸手的助手。

## 背后的机制

动态 EQ 把带通检测器与增益级结合，检测到设定频段超过阈值后，按比率压低或提升该频段。它可以只对某一个钟形滤波生效，也可以由侧链信号触发。与多段压缩相比，它的频段更窄、形状更接近 EQ，适合处理共鸣而不是控制整体动态。阈值、启动、释放决定它多快介入、多久退出。

## 旋钮与耳朵

频率选在问题最集中的位置，Q 取 1–3，range 先设 −3 dB。启动 1–10 ms 抓住瞬态，释放 50–200 ms 跟随句子。用来压箱声时，阈值要高于正常演唱，只在强音时动作；用来提存在感时，方向反过来。

## 耳朵要抓的点

在钢琴独奏上找到低音区的轰鸣，让动态 EQ 只在强奏时衰减 3 dB，弱奏应保持原样。换到人声，把 3 kHz 的阈值调到只在喊句时触发，听齿音与喊声是否分开。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","G3","C4","E4","G3","C3"],"label":"钢琴低音区的强奏","label_en":"Strong low piano notes","hint":"先听干声，再想象只有大声和弦才触发那 3 dB 衰减","hint_en":"Hear it dry, then picture 3 dB of cut triggered only by the loud chord"}
```

## 容易弄错的

以为动态 EQ 就是压缩器；以为它可以替代所有手动自动化；以为它只能衰减、不能提升。
:::

::: en
## Starting point: a problem

A static EQ cuts the quiet passages and the loud ones alike. A dynamic EQ changes a band only when its level passes a threshold, reaching in only when needed.

## The mechanism

A dynamic EQ combines a band-pass detector with a gain stage. When the chosen band exceeds the threshold, it is cut or boosted by a ratio. It can act on one bell or follow a sidechain. Its band is narrower than multiband compression and closer to an EQ shape, suiting resonance rather than overall dynamics. Threshold, attack and release set how fast it engages and leaves.

## Knobs and ears

Place the frequency at the problem, set Q between 1 and 3, and start with 3 dB of range. Attack of 1 to 10 ms catches transients; release of 50 to 200 ms follows phrases. To tame boxiness, set the threshold above normal singing so it acts on loud notes only; to add presence, reverse the direction.

## What the ear should catch

On piano, find the low boom and let the dynamic EQ cut 3 dB only on strong chords; quiet playing stays untouched. On a voice, set 3 kHz to trigger on shouts and hear sibilance separate from the shout.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C3", "G3", "C4", "E4", "G3", "C3"], "label": "Strong low piano notes", "label_en": "Strong low piano notes", "hint": "先听干声，再想象只有大声和弦才触发那 3 dB 衰减", "hint_en": "Hear it dry, then picture 3 dB of cut triggered only by the loud chord"}
```

## Easy to get wrong

That a dynamic EQ is just a compressor; that it replaces all manual automation; that it can only cut and never boost.
:::
