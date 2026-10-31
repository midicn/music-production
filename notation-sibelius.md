---
id: notation-sibelius
site: prod
cat: B6
order: 502
title: Sibelius 工作流
title_en: A Sibelius Workflow
summary: 拿到别人的谱，先清理再排版；分谱随总谱一起长，不是最后才抽。
summary_en: With a score from someone else, clean before you lay out; parts grow with the score, not at the end.
level: standard
tags: [Sibelius, 制谱, 分谱, 改编]
tags_en: [Sibelius, notation, parts, arranging]
alias: [Sibelius 工作流, Sibelius 制谱流程, Sibelius 分谱, Sibelius workflow]
links:
  - "[[glossary:score]]"
  - "[[glossary:full-score]]"
  - "[[instrument:voice]]"
instances:
  - musicnet-000248 | 木管五重奏，五份分谱各自独立，适合检查 Dynamic Parts 是否跟着总谱改
  - cyberhymnal-000005 | 四声部赞美诗加管风琴，声部与和声规矩，导入后最容易看出清理是否到位
  - pdmx-000600 | 《拉德茨基进行曲》，反复多、段落短，分谱的跳转与排练号最容易被改乱
  - pdmx-000007 | 莫扎特第四十交响曲，声部密，适合检查总谱到分谱的版面继承
sources:
  - Avid Sibelius Reference Guide，Dynamic Parts、Magnetic Layout 与 Review 章节（官方文档）。
  - Elaine Gould, Behind Bars, Faber，分谱与总谱的版面规则。
  - MusicXML 4.0 规范，导入导出的字段定义。
updated: 2026-10-31
---

::: zh
别人发来的 MusicXML 打开就能印，是很少见的情况。导入后的第一小时，决定的不是版面，而是后面还要改几遍。

## 拿到一份别人的谱

先看三件事：拍号与速度有没有落在正确的小节，移调乐器是否按谱表设置，歌词与力度是否还在各自的位置。导入器会把认得的记号放进去，认不出的变成文字或直接丢失。先别动版面，把结构对齐，再谈排版。结构错一小节，后面每一页都要跟着挪。

## 导入后的清理清单

| 检查项 | 通过标准 |
|---|---|
| 拍号、调号、速度 | 从小节线开始，速度文字附着在拍号上 |
| 连音线与三连音 | 跨过正确的小节，括号完整 |
| 移调乐器 | 谱表设置与显示音高一致 |
| 力度、奏法、文字 | 附着在音符上，不浮在小节线上 |
| 隐藏谱表与空白小节 | 没有多余空页与空系统 |
| 分谱页面 | 尺寸与页边继承总谱，不是默认值 |

清单过完再改版面。清理时用 Focus on Staves 一次只看几行，比在满页总谱里找错快。遇到认不出的文字，先确认它是记号还是注释，再决定删掉还是重做。

## 分谱与总谱的关系

Sibelius 的 Dynamic Parts 从总谱生成，改总谱时分谱同步。分谱里手动挪过的对象会保留局部位置，改得越多，越要在每次大改后重看。给分谱设单独的页面与谱表大小，别把总谱的缩编版面直接套给演奏者。排练号、提示与翻页要按分谱检查，总谱上看不出来。

## 版面三个开关

Magnetic Layout 负责避让，关掉它会得到更多自由，也会得到更多碰撞。House Style 决定字体、线宽与间距，从一份已经合格的谱导入样式，比逐项调快。Document Setup 管纸张、页边与谱表大小，改它会让所有手动断行重算。三个开关都动过之后，导一次 PDF 逐页看。

## 交付前的失败模式

只查总谱不查分谱，演奏者拿到的是另一份版面；导入时丢了三连音括号，回放听着对，谱面却读不出三连音；字体在对方机器上缺失，替换字体把间距撑开。Sibelius 能记住很多局部修改，代价是这些修改不会自己变干净。交付前把分谱当独立文件读一遍，比再调一次总谱有用。

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"blown","phrase":["C4","E4","G4","C5"],"label":"赞美诗的四声部","label_en":"Four voices in a hymn","hint":"听四个声部是否同时换气，再想它们在总谱与分谱上各占一行","hint_en":"Hear whether the four voices breathe together, then picture each one on its own staff"}
```
:::

::: en
A MusicXML file from someone else rarely opens ready to print. The first hour decides not the layout but how many more passes the score will need.

## A score someone else wrote

Check three things first: whether time signatures and tempo marks land on the right bar, whether transposing instruments follow their staves, and whether lyrics and dynamics still sit where they belong. The importer keeps what it recognises; the rest becomes text or disappears. Leave the layout alone until the structure lines up. One bar off and every page after it shifts.

## Clean-up checklist

| Check | Pass condition |
|---|---|
| Time signature, key, tempo | Start on the barline; tempo text attaches to the mark |
| Slurs and triplets | Cross the correct bars with complete brackets |
| Transposing instruments | Staff setting matches the displayed pitch |
| Dynamics, articulations, text | Attach to notes, not floating over barlines |
| Hidden staves and empty bars | No stray blank pages or systems |
| Part pages | Size and margins follow the score, not defaults |

Finish the list before touching layout. Focus on Staves, a few lines at a time, finds errors faster than a full page. When text is unrecognised, decide whether it was a marking or a comment before deleting or rebuilding it.

## How parts relate to the score

Sibelius generates Dynamic Parts from the score, and a score edit reaches the part. Objects moved by hand keep local positions, so the more edits you make, the more often the part needs another look. Give parts their own page and staff size instead of applying the condensed score layout to the player. Check rehearsal marks, cues and page turns in the part; the score will not show the problem.

## Three layout switches

Magnetic Layout handles collision avoidance. Turn it off and you gain freedom and collisions in equal measure. House Style sets fonts, line widths and spacing; importing a style from a score that already reads well beats adjusting each value. Document Setup controls paper, margins and staff size, and changing it recalculates every manual break. After touching all three, export a PDF and read every page.

## Failure modes before delivery

Check the score but not the parts and the player receives a different layout. Lose a triplet bracket on import and playback still sounds right while the page no longer reads as a triplet. A missing font on the recipient's machine substitutes another and pushes the spacing open. Sibelius remembers many local edits, and those edits do not clean themselves up. Read each part as a separate document before delivery; it is more useful than another pass on the score.

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"blown","phrase":["C4","E4","G4","C5"],"label":"Four voices in a hymn","label_en":"Four voices in a hymn","hint":"Hear whether the four voices breathe together, then picture each one on its own staff","hint_en":"Hear whether the four voices breathe together, then picture each one on its own staff"}
```
:::
