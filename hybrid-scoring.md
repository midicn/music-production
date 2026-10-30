---
id: hybrid-scoring
site: prod
cat: A9
title: 电子与混合配乐
title_en: Electronic and Hybrid Scoring
summary: 电子给脉冲与低频，管弦给动态与和声重量。
summary_en: Electronics supply pulse and low end while the orchestra supplies dynamics and harmonic weight.
level: standard
tags: [配乐, 混合编制, 电子, 管弦, 游戏]
tags_en: [scoring, hybrid ensemble, electronic, orchestral, games]
alias: [电子配乐, 混合配乐, 管弦电子, hybrid scoring, electronic scoring]
links:
  - "[[glossary:sound-design]]"
  - "[[instrument:software-synth]]"
  - "[[glossary:texture]]"
instances:
  - oga-000067 | 锯齿主音、合成贝斯与弦乐、定音鼓同场，电子与管弦各占一层
  - oga-000011 | 弦乐、Orchestra Hit 与大号并置，采样式管弦与真实声部同框
  - oga-000004 | 弦乐、铜管与太鼓组成战斗编制，打击层带明显的采样感
sources:
  - Buhler, Nevelsteen and Deemer，Hearing the Movies（Oxford）— 混合配乐与音色分层章节核对，未引用
  - Collins, Karen，Game Sound（MIT Press）— 电子与管弦混合编制章节核对，未引用
updated: 2026-10-28
---

::: zh
## 问题
管弦与电子同场，不是把合成器叠在乐队上。两者的时间感、动态与频段不同，混在一起很容易只剩一层厚墙。

## 原理或做法
分工先于音色。电子负责脉冲、低频与纹理，管弦负责动态、和声重量与高点。常见做法是合成低音托底、管弦占中高频、采样打击强化节奏。管弦有真实房间，合成没有，需要用混响与短延迟把它们放进同一空间。低频只留一个主人，必要时用侧链让合成低音给底鼓让位。

## 参数与判断
先定谁负责节奏、谁负责和声、谁负责高点。电子层要给管弦留出中频，别把锯齿铺满。混合编制里真实乐器不必更多，但必须更清楚。动态对比交给管弦，电子负责稳定。粘合靠共用混响，不靠压缩。

## 听什么
合成主音与弦乐是否互相掩蔽，太鼓与定音鼓是否重复同一节奏，低频是否只有一个来源，电子层撤掉后管弦是否仍然成立。

```audiolab
{"type":"instrument","gm":"Lead 2 (sawtooth)","synth":"bowed","phrase":["A3","C4","E4","A4"],"label":"锯齿主音的持续音","label_en":"A sustained sawtooth lead","hint":"先听它的稳定与亮度，再想象它与弦乐叠置时谁该让出中频","hint_en":"Hear its steadiness and brightness, then imagine who should yield the midrange when strings join"}
```

## 常见误解
以为混合就是管弦加鼓机。真正的混合是频段与时间的分工。采样也不能替代实录，它缺少力度与厅堂的连续变化。
:::

::: en
## The problem
Putting orchestra and electronics together is not stacking a synth on a band. The two have different senses of time, dynamics and frequency range, and the mixture easily becomes one thick wall.

## How it works
Division of labour comes before timbre. Electronics carry pulse, low end and texture; the orchestra carries dynamics, harmonic weight and peaks. A common layout puts a synth bass underneath, orchestra in the middle and highs, and sampled percussion on the rhythm. The orchestra has a real room and the synth does not, so shared reverb and short delays place them in one space. Keep one owner for the low end, and sidechain the synth bass to the kick when needed.

## Settings and judgement
Decide who owns rhythm, who owns harmony, who owns the peak. Leave midrange for the orchestra instead of filling it with saws. A hybrid ensemble does not need more real players, only clearer ones. Give dynamic contrast to the orchestra and steadiness to the electronics. Glue with a shared reverb, not with compression.

## What to listen for
Whether the lead and strings mask each other, whether taiko and timpani double the same rhythm, whether the low end has one source, and whether the orchestra still stands when the electronic layer is muted.

```audiolab
{"type": "instrument", "gm": "Lead 2 (sawtooth)", "synth": "bowed", "phrase": ["A3", "C4", "E4", "A4"], "label": "A sustained sawtooth lead", "label_en": "A sustained sawtooth lead", "hint": "先听它的稳定与亮度，再想象它与弦乐叠置时谁该让出中频", "hint_en": "Hear its steadiness and brightness, then imagine who should yield the midrange when strings join"}
```

## Common misconceptions
That hybrid means orchestra plus a drum machine. Real hybrid work divides frequency and time. Samples cannot replace a recording either; they lack the continuous change of dynamics and hall.
:::
