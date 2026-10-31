---
id: musescore
site: prod
cat: C
order: 43
title: MuseScore（开源记谱）
title_en: MuseScore
summary: 免费开源的制谱软件，够学校与个人把谱子写完、导出与共享。
summary_en: Free, open-source notation software that carries a score from entry to export and sharing.
level: standard
tags: [记谱, 开源, 制谱, 教学]
tags_en: [notation, open source, engraving, education]
alias: [MuseScore, MuseScore Studio, 缪斯谱, 开源制谱]
links:
  - "[[glossary:tablature]]"
  - "[[glossary:lead-sheet]]"
  - "[[instrument:classical-guitar]]"
instances:
  - thesession-000000 | 单声部舞曲，调号与反复清楚，是社区谱与 lead sheet 的参照，不是该工具的演示
  - nottingham-000001 | 民歌旋律短小，适合当作课堂记谱练习的参照，不是该工具的演示
  - mutopia-000005 | 古典吉他练习曲，可对照六线谱与标准谱的并排写法，是吉他谱交付的参照，不是该工具的演示
  - pdmx-000013 | 民歌改编的简易钢琴版，是入门改编谱的参照，不是该工具的演示
  - openscore-000001 | 人声与钢琴的艺术歌曲，歌词与伴奏都完整，是歌曲记谱的参照，不是该工具的演示
sources:
  - MuseScore Studio 的音符输入、谱表类型与导出格式，对照官方文档整理。
  - MuseScore.com 与桌面应用的服务边界（官方说明）。
tool_kind: notation
tool_vendor: MuseScore
tool_form: 桌面应用
tool_platforms: [macOS, Windows, Linux]
tool_price: 免费
tool_jobs: [制谱, 教学, 改编, 分谱]
tool_verified: 2026-10-30
updated: 2026-10-30
---

::: zh
MuseScore 的意义在于把记谱的门槛降到零：学生、业余乐团与独立作者都能把谱子写完、导出、发给别人，而不用先解决授权。

## 它能完成什么

让学生交一份钢琴谱 PDF 与一份 MIDI，作业从写到交都在一台机器上完成。吉他手做六线谱与和弦图，标准谱与六线谱并排。把一首民歌记下来，导出 MusicXML 交给编曲。小乐队做一页 lead sheet，和弦符号、旋律与歌词对齐。把一本老谱重新录入，做成可搜索、可转调的版本。

## 它怎么工作

单窗口加面板，音符、时值、连线与力度都在同一套快捷键里。谱表可切换标准谱、六线谱与打击乐谱，分谱从总谱的大谱表派生。回放默认用内置音源，装了 Muse Sounds 之后音色更好，那是单独下载的采样包。文件导出 PDF、PNG、MusicXML、MIDI 与音频；在线谱库是另一个服务，账号与条款和桌面应用分开。

## 边界与坑

- 复杂管弦乐总谱的版面控制弱于 Dorico 与 Sibelius，碰撞、分页与分谱细节要手工调。
- 多乐章结构与分谱要逐项设，工程大时回放吃内存，旧机器会卡。
- 应用免费不等于服务免费，在线谱库与音源各有自己的条款。
- 社区谱的版权状态不一，不能因为能下载就当作可商用。
- 升级偶尔改快捷键与面板位置，教学机房要锁版本。

## 替代与搭配

Dorico 的免费版功能受限，但版面能力更强，值得在正式出版前比较；Sibelius 在院校流程里更完整；LilyPond 用纯文本描述版面，适合批量与模板化出谱。与 DAW 的配合靠 MIDI 与 MusicXML：谱面在 MuseScore 定稿，音色与混音回 DAW 做。

## 上手路径

先学音符输入与时值、谱表与分谱、MusicXML 导出。读这里的记谱软件导论、打谱与排版规范、乐谱交换格式，用一首民歌走完录入到导出。

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (nylon)","synth":"plucked","phrase":["E3","A3","C4","E4","A4"],"label":"六线谱上的一条分解和弦","label_en":"An arpeggio as it sits on a tab staff","hint":"听每个音的落点，再想它在六线谱上是第几弦第几品","hint_en":"Hear where each note lands, then picture the string and fret on a tab staff"}
```
:::

::: en
MuseScore matters because it removes the licence question from notation. Students, amateur ensembles and independent authors can finish a score, export it and send it without solving licensing first.

## What it lets you finish

Have a student hand in a piano score as PDF and MIDI, written and exported on one machine. Build a guitar part with tablature and chord diagrams side by side with the staff. Notate a folk tune and export MusicXML for an arranger. Make a one-page lead sheet with chord symbols, melody and lyrics aligned. Re-enter an old score as a searchable, transposable version.

## How it works

One window with panels; notes, durations, slurs and dynamics share a small set of shortcuts. Staves can switch between standard notation, tablature and percussion, and parts are derived from the score's grand staff. Playback uses the built-in sounds by default; Muse Sounds is a separate sample download that improves the tone. Export covers PDF, PNG, MusicXML, MIDI and audio. The online score library is a separate service with its own account and terms.

## Limits and traps

- Layout control for large orchestral scores is weaker than Dorico or Sibelius; collisions, page turns and part details need manual work.
- Multi-movement structure and parts are set item by item, and playback of a big project eats memory on an older machine.
- A free application is not a free service: the online library and the sample sounds have their own terms.
- Community scores carry mixed copyright status; being downloadable does not make them usable commercially.
- Updates sometimes move shortcuts and panels, so a teaching lab should pin one version.

## Alternatives and pairings

Dorico's free tier is limited but stronger at layout, and worth comparing before publication. Sibelius fits an institutional chain more completely. LilyPond describes layout in plain text, which suits templated batch work. With a DAW, the handoff is MIDI and MusicXML: finish the score here, finish the sounds and mix there.

## First three things to learn

Note entry and durations, staves and parts, and MusicXML export. Then read Introduction to Notation Software, Engraving and Layout Rules, and Score Exchange Formats, and take one folk tune from entry to export.

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (nylon)","synth":"plucked","phrase":["E3","A3","C4","E4","A4"],"label":"An arpeggio as it sits on a tab staff","label_en":"An arpeggio as it sits on a tab staff","hint":"Hear where each note lands, then picture the string and fret on a tab staff","hint_en":"Hear where each note lands, then picture the string and fret on a tab staff"}
```
:::
