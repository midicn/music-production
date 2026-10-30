---
id: dynamic-range-and-perception
site: prod
cat: A8
title: 动态范围与听感
title_en: Dynamic Range and Perception
summary: 动态范围不是越大越好，压缩过度会让音乐失去呼吸。
summary_en: Dynamic range is not a score to maximise; too much compression removes the breath and impact that make a performance feel alive.
level: standard
tags: [母带, 动态, 压缩]
tags_en: [mastering, dynamics, compression]
alias: [动态范围, 动态处理, dynamic range]
links:
  - "[[glossary:lufs]]"
  - "[[glossary:limiter]]"
  - "[[glossary:maximizer]]"
instances:
  - pdmx-000834 | 贝多芬第四交响篇幅长，适合观察整首的强弱弧线是否被压平
  - pdmx-000007 | 莫扎特第四十的乐句起伏清楚，适合练分段测短时响度
  - pdmx-002214 | 肖斯塔科维奇第十的织体厚重，适合听限制器是否让低频失去弹性
sources:
  - 积分响度、短时响度与动态范围的关系，依响度测量与母带通识核查，未抄文本
  - 压缩与限制对瞬态和乐句起伏的影响，依动态处理教材通识核查，未抄文本
updated: 2026-10-28
---

::: zh
动态范围是音乐最轻与最响之间的距离。它不只是数字，更是乐句的呼吸、鼓的冲击和听众的注意力。

## 问题

只盯着响度表，很容易把整首压成一条平线。安静段落被抬起来，副歌就不再显得高；鼓的起音被限制器削平，只剩一团低频。

## 目标与标准

动态范围可用 crest factor 或 LRA 观察，但最终要回到听感。流行与摇滚通常需要稳定能量，古典与爵士需要更大起伏。好的母带在最响处仍有冲击，在最静处仍有内容，整首的 short-term 响度不会忽高忽低。

## 做法

分段测 short-term LUFS，找出副歌与前奏的差距。需要提升整体时，先用增益自动化处理段落，再让限制器只收峰值，而不是全曲重压。每次处理都保留 bypass 对比，并在手机小音量下检查。动态要与风格匹配，不是越多越好。

## 听什么

听鼓的起音是否还有力，人声的呼吸是否还在，弦乐的渐强是否真的变强。下面这段弦乐有渐强与收束，可以对照处理前后的呼吸感。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","A4","G4","E4","C4"],"label":"渐强与收束","label_en":"Crescendo and release","hint":"听渐强是靠演奏力度，还是只靠音量被推高","hint_en":"Is the rise played, or merely pushed up in level"}
```

## 常见误解

动态越大越好的说法，忽略了播放环境与风格。压缩也不等于损失，适度压缩能让小音量下更清楚。低 LUFS 不自动等于好动态，安静而扁的母带同样没有呼吸。
:::

::: en
Dynamic range is the distance between the quietest and loudest moments. It is also the breath of a phrase and the impact of a drum.

## The problem

A loudness meter alone makes it easy to flatten a whole song. Quiet passages rise, so the chorus no longer feels high; drum attacks are shaved until only low-frequency mass remains.

## Goals and standards

Crest factor or LRA can describe dynamic range, but the ear has the final say. Pop and rock usually want steady energy, while classical and jazz need wider swings. A good master still hits hard at its loudest and holds content at its quietest.

## Practice

Measure short-term LUFS by section and find the gap between verse and chorus. When the whole needs level, use gain automation first, then let the limiter catch peaks. Keep a bypass comparison and check detail on a phone.

## What to listen for

Hear whether drum attacks still strike, whether the vocal still breathes, and whether a string crescendo truly grows. The line below rises and releases.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C4", "E4", "G4", "A4", "G4", "E4", "C4"], "label": "Crescendo and release", "label_en": "Crescendo and release", "hint": "听渐强是靠演奏力度，还是只靠音量被推高", "hint_en": "Is the rise played, or merely pushed up in level"}
```

## Common misunderstandings

A wider range is not automatically more audiophile; that ignores playback context and genre. Compression is not always loss either. A low LUFS reading does not prove good dynamics.
:::
