---
id: notation-software-introduction
site: prod
cat: B6
title: 记谱软件导论
title_en: Introduction to Notation Software
summary: 记谱软件把音符、符号与版面存成可编辑结构，供人读也供机器读。
summary_en: Notation software stores pitches, symbols and page layout as an editable structure for players and machines alike.
level: standard
tags: [记谱, 制谱软件, 乐谱, 排版]
tags_en: [notation, scoring software, score, engraving]
alias: [记谱软件导论, 制谱软件, 打谱软件, notation software, scoring software]
links:
  - "[[glossary:score]]"
  - "[[glossary:midi-protocol]]"
  - "[[glossary:daw]]"
instances:
  - m21-000000 | 四声部众赞歌，每个声部在谱面上各有清楚的走向
  - atepp-001875 | 三声部创意曲，声部交叉与主题追逐在谱面上一眼可辨
  - oga-000052 | 游戏配乐的多层编制，适合观察总谱怎样压缩成若干谱表
  - mutopia-000439 | 人声与钢琴两个谱表，能看清歌词与钢琴伴奏怎样对齐
sources:
  - MusicXML 与 SMuFL 的谱面结构与符号定义，依公开规范核查，未抄文本
  - 常见记谱软件的录入、回放与交换设置，依公开文档核查，未抄文本
updated: 2026-10-28
---

::: zh
记谱软件不只是把音符画得好看，它把音高、时值、分句与版面存成可编辑结构，能打印、回放和交换。

## 问题

手写谱改一个调号要重抄整页，DAW 的钢琴卷帘能听却给不了分句、指法与翻页。演奏者要读得顺，编曲者要改得动，这两件事只能由记谱软件承担。

## 原理或流程

输入层接收 MIDI 键盘、电脑键盘或鼠标，记下音高与时值；符号层补连线、力度记号、装饰音与歌词；版面层决定系统和小节怎样落页。文件同时保存语义与坐标，导出时转成 MusicXML 或 MIDI。回放依据速度曲线与力度映射，和真人演奏仍有距离。

## 做法与判断

先定编制、纸张与谱表大小，再录入音符，最后做分句和版面。判断标准是演奏者第一遍读谱能否找到拍点、气口与下一页。交换用 MusicXML，编曲或音频再导 MIDI。录入阶段不必追求完美排版，后续改谱会让间距反复变化。

## 听什么

听回放的连奏有没有被切断，重音是否落在拍点上，长音有没有留够余量。把同一段导出 MIDI 再听，能听出软件做了哪些量化。

## 常见误解

记谱软件不等于 DAW，它不擅长多轨混音；导出的 MIDI 也不等于乐谱，分句与力度记号多半留不住。页面好看不代表读得顺，谱表太密或翻页太急都会让排练停下来。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5"],"label":"四个音同时进入，像谱面上的四个声部","label_en":"Four notes entering together, four voices on a score","hint":"听这四个音是否整齐，再想象它们在谱上分行写成四个声部","hint_en":"Hear whether the four notes align, then picture them written as four separate voices"}
```
:::

::: en
Notation software does more than draw tidy notes. It stores pitch, duration, phrasing and page layout as an editable structure that can be printed, played back and exchanged.

## The problem

Changing a key signature by hand means recopying a page, while a DAW piano roll can play but cannot show phrasing, fingering or page turns. Players need a score that reads smoothly; arrangers need a file that stays editable.

## How it works

An input layer takes notes from a MIDI keyboard, the computer keyboard or the mouse. A symbol layer adds slurs, dynamics, ornaments and lyrics. A layout layer places systems and bars on the page. The file keeps meaning and coordinates together, then exports MusicXML or MIDI. Playback follows a tempo curve and a velocity map, short of a human performance.

## Practice and judgement

Set the ensemble, paper size and staff size first, enter notes, then shape phrasing and layout. The test is whether a player finds the beat, the breath and the next page at sight. Use MusicXML for notation and MIDI for arranging. Do not chase perfect spacing early; later edits move everything.

## What to listen for

Hear whether playback cuts slurs, whether accents land on the beat and whether long notes keep enough tail. Export it as MIDI and listen for the quantisation applied.

## Common misunderstandings

Notation software is not a DAW and does not mix many tracks. Exported MIDI is not the score; phrasing and dynamic marks rarely survive. A handsome page is not always readable; tight spacing and rushed page turns stop rehearsals.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "C5"], "label": "Four notes entering together, four voices on a score", "label_en": "Four notes entering together, four voices on a score", "hint": "听这四个音是否整齐，再想象它们在谱上分行写成四个声部", "hint_en": "Hear whether the four notes align, then picture them written as four separate voices"}
```
:::
