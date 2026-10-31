---
id: reverb-width
site: prod
cat: A7
title: 混响宽度
title_en: Reverb Width
summary: 宽度来自左右尾巴的不相关，而不是把湿声推满。
summary_en: Width comes from decorrelated reverb tails, not from pushing the wet control higher.
level: standard
tags: [效果器, 混响, 宽度, 单声道]
tags_en: [effects, reverb, width, mono]
alias: [混响宽度, 空间宽度, 立体声混响, reverb width, stereo reverb]
links:
  - "[[glossary:reverb]]"
  - "[[glossary:stereo-technique]]"
  - "[[glossary:mid-side]]"
instances:
  - cyberhymnal-006346 | 管风琴赞美诗尾巴长，适合听左右两路是否真的分开
  - pdmx-000070 | 巴伯《弦乐慢板》持续音多，宽与厚的差别容易分辨
  - m21-000602 | 合唱声部横向铺开，适合检查加宽后中央是否变空
sources:
  - Michael Vorländer, Auralization.
  - Kendall, The Decorrelation of Audio Signals and Its Impact on Spatial Imagery, Computer Music Journal.
  - Valhalla DSP, ValhallaVintageVerb user manual.
updated: 2026-10-31
order: 444
---

::: zh
把混响宽度推到最大，人声反而退成一条细线。宽度不来自湿声多少，而来自左右两路尾巴有多不相关。

## 相关性决定宽度

左右完全相同的混响叠在中间，听感就是单声道。早期反射的到达时间与方向不同，扩散网络给出不同的尾音，缓慢调制让两路持续错开，宽度才出现。很多宽度旋钮做的只是改变侧声道比例，并没有增加新的反射。

## 四种加宽手段

不同手段拿到的宽不是同一种宽。

| 手段 | 做法 | 听感 | 单声道折叠 |
|---|---|---|---|
| 早期反射错开 | 左右使用不同反射图案 | 边缘清楚 | 部分抵消 |
| 扩散与调制 | 提高扩散，加轻微调制 | 尾巴变厚 | 基本保留 |
| 预延迟分离 | 左右预延迟差 5–15 ms | 空间更深 | 产生梳状滤波 |
| 只加宽中高频 | 侧声道高通后提升 | 空气感 | 低频不受影响 |

## 低频为什么留在中间

低频波长长，侧声道内容在单声道折叠时会抵消。把侧声道在 120–200 Hz 以下高通，低频回到中间，宽度留给镲片、弦乐与混响尾部。鼓组与贝斯的低频最怕这种抵消，手机扬声器一放就少一半。

## 耳朵要抓的点

先听干声，再加混响，比较左右是否真的分开。按单声道按钮，听宽度是否只剩音量变化。把宽度从 0 推到 100，注意中央人声是否后退，尾巴是否盖住下一个字。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["A3","C4","E4","A4"],"label":"持续和弦，听左右尾巴","label_en":"A sustained chord, listen for the two tails","hint":"先听合奏的宽度，再想左右尾巴若完全相同，宽度会塌到哪里","hint_en":"Hear the width first, then imagine where it collapses if both tails are identical"}
```

## 什么时候不该加宽

单声道为主的场合不加，俱乐部、手机外放与公共广播都只听到中声道。已经很宽的铺底再加宽，只会让中间空掉。长尾混响加宽后，下一乐句的起音会被前一句的尾巴遮住。相关性表长期偏向负值，说明问题在录音或声像，不在宽度旋钮。
:::

::: en
Push reverb width to maximum and the vocal retreats into a thin line. Width is not how much wet signal you add; it is how little the two tails correlate.

## Correlation sets the width

Identical left and right reverb sits in the centre as mono. Width appears when early reflections arrive from different directions at different times, when the diffusion network produces different tails, and when slow modulation keeps the two sides drifting apart. Many width controls only change the side level; they add no new reflections.

## Four ways to widen

Each method produces a different kind of width.

| Method | What it does | What you hear | In mono |
|---|---|---|---|
| Offset early reflections | Different reflection patterns per side | Clearer edges | Partial cancellation |
| Diffusion and modulation | More diffusion, light modulation | Thicker tail | Mostly survives |
| Split pre-delay | 5–15 ms difference between sides | Deeper space | Comb filtering |
| Widen only mids and highs | High-pass the side, then lift | Air | Low end untouched |

## Why the low end stays centred

Long wavelengths mean side content cancels when folded to mono. High-pass the side channel below 120–200 Hz, keep the low end in the middle, and leave width to cymbals, strings and the reverb tail. Kick and bass suffer most from that cancellation; a phone speaker removes half of it at once.

## What the ear should catch

Hear the dry signal, add reverb, and check whether the sides truly separate. Press mono and listen for whether width turns into a level change only. Sweep width from 0 to 100 and notice the centre vocal stepping back and the tail covering the next word.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["A3", "C4", "E4", "A4"], "label": "A sustained chord, listen for the two tails", "label_en": "A sustained chord, listen for the two tails", "hint": "先听合奏的宽度，再想左右尾巴若完全相同，宽度会塌到哪里", "hint_en": "Hear the width first, then imagine where it collapses if both tails are identical"}
```

## When not to widen

Skip it when mono dominates: clubs, phone speakers and public address all hear the mid channel. Widening a pad that is already wide only hollows out the centre. A long tail that has been widened covers the attack of the next phrase. A correlation meter that sits negative for long stretches points to tracking or panning, not to the width control.
:::
