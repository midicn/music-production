---
id: frequency-allocation
site: prod
cat: A2
title: 频段分配
title_en: Frequency Allocation
summary: 在上游决定谁占低、中、高，避免几个音源挤在一起。
summary_en: Decide who owns low, mid and high before anything gets crowded.
level: standard
tags: [编曲, 频段, 频谱]
tags_en: [arranging, frequency, spectrum]
alias: [频段分配, 频率分配, frequency allocation, frequency split]
links:
  - "[[glossary:spacing]]"
  - "[[glossary:register]]"
  - "[[glossary:tessitura]]"
  - "[[instrument:double-bass]]"
instances:
  - musicnet-000090 | 贝多芬第十二弦乐四重奏首乐章，四件弦乐器分居低中高各带，频段界线清楚
  - oga-000004 | 游戏战斗曲，定音鼓与太鼓守住低频，长号、小号与弦乐分居中高，可听各带的主次
  - mutopia-000178 | 巴赫管风琴托卡塔，脚踏板守低频，手键盘填中高，是天然的频段分工
sources:
  - The New Grove Dictionary of Music and Musicians, 2nd ed., entry Orchestration（Oxford University Press），用于核对音区与频段分工
  - David M. Howard and Jamie Angus, Acoustics and Psychoacoustics, 4th ed.（Focal Press, 2013），用于核对频段与掩蔽的基本数据
updated: 2026-10-28
---

::: zh
编曲里的浑多半不是效果器造成的，而是几个音源挤在同一频段。频段分配就是在上游决定谁占低、中、高，给每个角色留出可辨的位置。

## 问题
所有乐器都在中频发力时，加 EQ 只能救一时。先问哪一层本该让路，比事后切频更有效。

## 织体或频段
大致可分四带，低频给底鼓与贝斯基音，低中给和弦根音与低把位，中高频给主旋律与人声，高频给镲片与泛音。每带不必空着，但同一带里不要放两个同等重要的持续声源。

## 做法与判断
先安排低音与底鼓，让两者在时间上错开，而不是争同一瞬间。旋律与铺底若在同一音区，把铺底移高八度或改成短音，通常比加 EQ 更自然。中频拥挤时，删掉一层比切掉两边更干净。

## 听什么
用单声道或一只音箱听，冲突会更明显。若旋律在某几个音上突然被盖住，问题多半出在那一带的持续声源，而不是旋律太轻。

## 常见误解
高频多不等于清晰，低频多也不等于厚。清晰来自各频段有主次，而不是每段都推满。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C2","G2","C4","E4","G5","E5","C5","G4"],"label":"从低到高排开","label_en":"Spread from low to high","hint":"听低、中、高三个区域依次亮起，想象每件乐器只占其中一段","hint_en":"Hear low, mid and high light up in turn"}
```
:::

::: en
Muddiness usually comes from several sources crowding one band, not from a missing plug-in. Frequency allocation decides upstream who owns low, mid and high.

## The problem
When every instrument pushes in the midrange, EQ buys only temporary relief. Ask which layer should yield first.

## Texture or frequency band
Four rough bands work: low for kick and bass roots, low-mid for chord roots and low positions, upper-mid for lead melody and voice, high for cymbals and air. Do not put two equally important sustained sources in one band.

## Approach and judgement
Place bass and kick first, separating them in time rather than letting them fight for the same instant. If melody and pad share a register, lift the pad an octave or shorten its notes; this usually sounds more natural than EQ. In a crowded midrange, removing a layer is cleaner than carving both sides.

## What to listen for
Listen in mono or on one speaker and the conflict becomes obvious. If the melody disappears on a few notes, the cause is usually a sustained source in that band, not a quiet melody.

## Common misunderstandings
More highs do not equal clarity, and more lows do not equal weight. Clarity comes from a hierarchy in each band, not from filling every band.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C2", "G2", "C4", "E4", "G5", "E5", "C5", "G4"], "label": "Spread from low to high", "label_en": "Spread from low to high", "hint": "听低、中、高三个区域依次亮起，想象每件乐器只占其中一段", "hint_en": "Hear low, mid and high light up in turn"}
```
:::
