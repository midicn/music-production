---
id: score-engraving-rules
site: prod
cat: B6
title: 打谱与排版规范
title_en: Engraving and Layout Rules
summary: 谱面排版靠间距、连线与分页规则，让演奏者第一遍就能读对。
summary_en: Engraving rules govern spacing, slurs and page turns so a player reads the music correctly at sight.
level: standard
tags: [制谱, 排版, 乐谱, 版式]
tags_en: [engraving, layout, score, notation]
alias: [打谱与排版规范, 乐谱排版, 制谱规范, engraving rules, music engraving]
links:
  - "[[glossary:score]]"
  - "[[glossary:full-score]]"
  - "[[glossary:clef]]"
  - "[[glossary:ledger-line]]"
instances:
  - m21-000000 | 四声部众赞歌，声部间距与符干方向直接决定读谱是否顺畅
  - atepp-000075 | 钢琴奏鸣曲音区跨度大，加线密集，最能检验纵向避让
  - oga-000045 | 管弦配乐层次多，适合观察总谱的系统断点与分谱抽取
  - mutopia-000789 | 人声与钢琴两个谱表，歌词与伴奏的对齐最考验间距
sources:
  - 传统雕版与当代制谱软件的间距、连线与分页规则，依公开规范核查，未抄文本
  - 总谱与分谱的版面惯例，依出版与制谱资料核查，未抄文本
updated: 2026-10-28
---

::: zh
同一段音乐，间距、连线与分页不同，演奏者读到的难度完全不同。排版的目标不是漂亮，而是减少误读。

## 问题

谱表挤在一起，临时记号容易看错行；连线跨过系统，分句就断；翻页落在乐句中间，排练必然停。

## 原理或流程

水平间距按最短时值分配，再按和声密度、装饰音与歌词伸缩；垂直方向避免声部、符干与临时记号碰撞；连线避开符头；系统断点落在乐句之间，分页留出翻页时间。软件用碰撞检测与弹性间距实现，总谱与分谱分别排版。

## 做法与判断

先定谱表大小与页边距，再调节拍间距，最后处理连线与分页。检查同音连线是否跨行、临时记号是否重复、符干方向是否清楚；缩到七成看是否仍可读；总谱通过后再抽分谱。

## 听什么

跟着慢速回放读谱，卡住的地方往往就是间距或连线的问题。听分句的气口，判断系统断点是否落在正确位置。

## 常见误解

自动排版不是一键完成；留白多不等于清楚；总谱好看不代表分谱可用。系统拉得太满时，页数少反而更难读。

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"blown","phrase":["C3","G3","C4","E4","G4"],"label":"四个声部叠在一起，听它们的间距","label_en":"Four voices stacked, hear the spacing","hint":"听低音与高音之间有没有空隙，再想象它们在谱表上的垂直距离","hint_en":"Hear the gap between bass and treble, then picture their vertical distance on the staves"}
```
:::

::: en
The same music reads very differently with different spacing, slurs and page breaks. Engraving aims at fewer misreadings, not decoration.

## The problem

Crowded staves make accidentals point to the wrong line. A slur broken across a system cuts a phrase, and a page turn inside a phrase stops rehearsal.

## How it works

Horizontal spacing follows the shortest duration, then stretches for dense harmony, ornaments and lyrics. Vertically, voices, stems and accidentals avoid collisions, and slurs clear noteheads. System breaks fall between phrases, and pages leave time to turn. Software uses collision detection and elastic spacing. Full and part scores are laid out separately.

## Practice and judgement

Set staff size and margins, adjust beat spacing, then slurs and page turns. Check tied notes across systems, repeated accidentals and stem direction between voices. Shrink to seventy percent to test legibility; extract parts after the full score.

## What to listen for

Layout is silent, but reading along at slow playback shows where you stumble. Hear the breath at phrase ends and judge whether system breaks support it.

## Common misunderstandings

Auto layout is not one click; white space is not clarity; a fine full score does not make a usable part. Fewer pages can read worse when systems are stretched full.

```audiolab
{"type": "instrument", "gm": "Church Organ", "synth": "blown", "phrase": ["C3", "G3", "C4", "E4", "G4"], "label": "Four voices stacked, hear the spacing", "label_en": "Four voices stacked, hear the spacing", "hint": "听低音与高音之间有没有空隙，再想象它们在谱表上的垂直距离", "hint_en": "Hear the gap between bass and treble, then picture their vertical distance on the staves"}
```
:::
