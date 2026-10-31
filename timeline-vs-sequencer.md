---
id: timeline-vs-sequencer
site: prod
cat: A1
title: 时间线与音序器
title_en: Timeline and Sequencer
summary: 两种组织音乐时间的界面，决定你先想秒还是先想小节。
summary_en: Two ways to organise musical time, one counting seconds and one counting bars, and how that choice shapes editing.
level: standard
tags: [DAW, 时间线, 音序器, 工作流]
tags_en: [DAW, timeline, sequencer, workflow]
alias: [时间线, 音序器, 线性编辑, timeline, sequencer]
links:
  - "[[glossary:daw]]"
  - "[[glossary:automation]]"
  - "[[period:baroque]]"
instances:
  - oga-000018 | 短循环的城堡配乐，按小节复制与变奏最顺手
  - atepp-003869 | 自由速度的钢琴奏鸣曲，段落靠绝对时间定位
  - pdmx-000531 | 十四分钟的协奏曲，通篇结构需要时间线总览
sources:
  - 时间线与音序器的界面差异——依据来自DAW 文档与音序软件说明。
  - 速度轨、吸附与片段时间基准的用法，对照数字音频工作流惯例整理。
updated: 2026-10-28
---

::: zh
时间线按秒走，音序器按小节走。多数 DAW 两者都有，差别不在功能，而在你第一眼看到什么。

## 卡住的地方

给画面配乐，要卡在台词后两秒；做舞曲，要让八小节循环严丝合缝。两种任务对时间的提问不同，界面若逼你用另一单位思考，就会多出换算。

## 为什么这样有效

时间线以绝对时间为横轴，片段自由摆放，适合对白、音效与画面同步。音序器以拍和小节为单位，循环、量化与复制是原生动作。现代 DAW 常共用一条时间线，只切换标尺与吸附，区别在习惯，不在品类。

## 参数与取舍

看标尺单位、速度轨与吸附。有渐慢、自由速度或同步点时，用绝对时间；节拍稳定的段落用音乐时间。循环片段要确认起点落在拍上，速度变化时检查片段是否跟随。

## 耳朵要抓的点

先听一段按小节循环的配乐，再听一首速度自由的钢琴曲。前者让你数拍，后者让你看秒。把同一短句放进两种视图，注意先找网格还是时间点。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","G4","E4","C5"],"label":"同一材料换一种时间观","label_en":"One phrase under two views of time","hint":"先听循环感，再想它落在时间线的哪里","hint_en":"Hear the loop first, then place it on a timeline"}
```

## 容易弄错的

时间线不只属于影视，音序器也不只属于电子音乐。决定因素是素材有无稳定拍点，以及你要不要跟画面某一帧对齐。
:::

::: en
A timeline counts seconds; a sequencer counts bars. Most DAWs offer both, and the difference is less about features than about what you see first.

## Where it snags

A cue must land two seconds after a line; a dance track must loop eight bars without a seam. The two tasks ask different questions about time, and an interface that forces the other unit adds mental arithmetic.

## Why it works

A timeline uses absolute time as its horizontal axis, so clips can sit anywhere and follow dialogue, effects or picture. A sequencer works in beats and bars, where looping, quantising and pattern copying are native actions. Modern DAWs often share one timeline and switch only the ruler and snap, so the difference is habit, not product category.

## Settings and trade-offs

Watch the ruler unit, tempo map and snap. Use absolute time for ritardandi, free tempo or picture sync points; use musical time for steady sections. Check that loop starts fall on beats, and that clips follow when tempo changes.

## What the ear catches

Hear a cue that loops by bars, then a free-tempo piano sonata. The first makes you count; the second makes you watch seconds. Place the same short phrase in both views and notice whether you look for a grid or a time point first.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C4", "G4", "E4", "C5"], "label": "One phrase under two views of time", "label_en": "One phrase under two views of time", "hint": "先听循环感，再想它落在时间线的哪里", "hint_en": "Hear the loop first, then place it on a timeline"}
```

## Easy to get wrong

Timelines are not only for film, and sequencers are not only for electronic music. What decides is whether the material has a steady pulse, and whether you must align to a frame.
:::
