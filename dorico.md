---
id: dorico
site: prod
cat: C
order: 41
title: Dorico（记谱与排版）
title_en: Dorico
summary: 把音符、分句与版面做成可交付的总谱与分谱，面向出版与配乐。
summary_en: A notation program built for score and part production, from chamber music to orchestral and film sessions.
level: standard
tags: [记谱, 制谱, 排版, 分谱]
tags_en: [notation, engraving, parts, orchestral]
alias: [Dorico, 多里科, Dorico Pro, Steinberg 制谱, Dorico 记谱]
links:
  - "[[glossary:score]]"
  - "[[glossary:full-score]]"
  - "[[glossary:clef]]"
instances:
  - musicnet-000067 | 弦乐四重奏乐章，四个声部同页，是总谱与分谱交付的参照
  - mutopia-000498 | 交响曲慢乐章，系统多、声部密，可对照自动分谱后的版面，是该工具常见产出的参照
  - openscore-000008 | 人声与钢琴两个谱表，歌词与伴奏的对齐最考验间距，是该工具常见产出的参照
  - m21-000001 | 四声部众赞歌，声部走向与符干方向一眼可辨，是该工具常见产出的参照
sources:
  - Dorico 的 Flow、Condensing 与 Engrave 模式，对照Steinberg 公开文档整理。
  - 总谱与分谱的版面规则（制谱与出版资料）。
tool_kind: notation
tool_vendor: Steinberg
tool_form: 桌面应用
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [制谱, 排版, 管弦乐, 影视配乐]
tool_verified: 2026-10-30
updated: 2026-10-30
---

::: zh
Dorico 的目标不是把音符画上去，而是让一份总谱在改过十次之后仍然能直接印。它把演奏者、编制与版面当成结构的一部分。

## 能替你做完什么

把一首弦乐四重奏从空白工程做到可打印的总谱与四份分谱。把管弦乐总谱按编制压成双行谱表，需要时再展开。在一个工程里放下多乐章或整套配乐，每段有自己的速度、调号与排练号。为画面写谱，并把速度映射对齐到帧。给学校或教堂做四声部赞美诗，歌词逐字落位。

## 它怎么工作

工程按 Flow 分段，每段带自己的速度、调号与谱表模板。Write 模式负责音符、歌词与和弦符号；Engrave 模式负责间距、连线、分页与手动避让；Condensing 把同族乐器合成一行，分谱由总谱派生，改总谱时分谱同步更新。版面用 frame chain 串起页面，回放走内置音源或 VST3，导出 PDF、MusicXML 与音频。

## 哪里会坑你

- 模式划分与术语自成一套，前两周会比在 Sibelius 里慢；键盘输入习惯建立后才反过来快。
- 回放是校对工具，不是混音环境；音色层与效果远不如 DAW，成品音频仍要回去做。
- Condensing 依赖正确的编制与声部编号，编制写错时合并会错行，返工比重排更久。
- 从别处导入的复杂谱面，MusicXML 带得走音符与多数记号，带不走手动调过的版面。
- 没有 Linux 版，激活走 Steinberg 账号，首次需要联网。

## 换成什么

院校或出版社已有 Sibelius 流程时，换 Dorico 的收益主要在自动分谱与弹性间距，不在功能有无。预算为零时先用 MuseScore 把编制与段落跑通，再决定是否换。需要完全用文本控制版面，LilyPond 仍是另一条路。

## 先学三件事

先学三件事：Flow 与编制模板、Write 模式的键盘输入、Engrave 模式的间距与分页。再读这里的打谱与排版规范、记谱软件导论、配乐交付与分轨，用一首四声部众赞歌走完总谱到分谱。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G3","D4","A4","E5"],"label":"一条要被读成乐句的旋律","label_en":"One line that must read as a phrase","hint":"听四个音之间的连接，再想它在谱上要写成怎样的连线与分句","hint_en":"Hear how the four notes connect, then picture the slurs and phrasing on the page"}
```
:::

::: en
Dorico is built so that a score is still printable after the tenth revision. Performers, ensemble and layout are part of the structure, not decoration applied at the end.

## What it finishes for you

Take a string quartet from an empty project to a printable score and four parts. Condense a full orchestral score onto two staves and expand it again. Keep several movements or a whole cue set in one project, each with its own tempo, key and rehearsal marks. Write to picture with a tempo map that lands on frames. Set a four-part hymn with lyrics under every syllable. Export the score as PDF, MusicXML and audio for players, copyists or a DAW.

## How it works

A project is split into flows, each with its own tempo, key and staff template. Write mode handles notes, lyrics and chord symbols. Engrave mode handles spacing, slurs, page breaks and manual collisions. Condensing merges instruments of one family onto a single staff; parts are derived from the score and follow later edits. Frame chains place music on the page. Playback uses the bundled sounds or VST3 instruments; export goes to PDF, MusicXML and audio.

## Where it bites

- The mode split and vocabulary are their own language; the first two weeks are slower than Sibelius, and only keyboard entry makes it faster later.
- Playback is a proofing tool. It is not a mixing environment, and finished audio still belongs in a DAW.
- Condensing depends on correct ensemble setup and voice numbering; a wrong setup merges the wrong lines and costs more time than redoing the layout.
- MusicXML from another program carries notes and most markings, but not hand-adjusted layout.
- There is no Linux version, and activation runs through a Steinberg account with an online first check.

## What to swap in

If an institution or publisher already runs Sibelius, the gain from Dorico is automatic part generation and elastic spacing rather than features that do not exist elsewhere. With no budget, MuseScore is enough to settle the ensemble and the sections before switching. When every spacing decision must be scripted, LilyPond remains the other route. Pair it with a DAW: the score is finished here, the sounds and mix are finished there.

## First three things

Flows and ensemble templates, keyboard note entry in Write mode, and spacing and page turns in Engrave mode. Then read Engraving and Layout Rules, Introduction to Notation Software, and Score Delivery and Stems, and take one four-part chorale from score to parts.

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G3","D4","A4","E5"],"label":"One line that must read as a phrase","label_en":"One line that must read as a phrase","hint":"Hear how the four notes connect, then picture the slurs and phrasing on the page","hint_en":"Hear how the four notes connect, then picture the slurs and phrasing on the page"}
```
:::
