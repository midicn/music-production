---
id: step-sequencer
site: prod
cat: B2
title: 步进音序器
title_en: Step Sequencer
summary: 把时间切成等长格子，每格决定这一步响不响。
summary_en: A grid of equal cells where each cell answers one question, whether that step fires.
level: standard
tags: [音序, 步进, 鼓机, 节奏]
tags_en: [sequencing, step sequencing, drum machine, rhythm]
alias: [步进音序器, 步进序列, 步进编排, step sequencer, step seq]
links:
  - "[[instrument:sequencer]]"
  - "[[glossary:sequence]]"
  - "[[glossary:tempo]]"
instances:
  - groove-000000 | 放克鼓型按十六步排列，开关与重音一眼可辨
  - groove-001103 | 迪斯科的四拍底鼓，每步位置最规整
  - oga-000000 | 二十三秒的游戏配乐，短小到能整段数清步数
sources:
  - 步进音序的格子模型与连步用法；鼓机与音序软件说明是主要依据。
  - 步长、重音与概率触发的参数范围——依据来自电子音乐制作惯例。
updated: 2026-10-28
---

::: zh
步进音序器把时间切成等长的格子，每一格只回答一个问题：这一步响不响。

## 要解决的事

鼓机与舞曲依赖十六分音符级的重复，靠手弹很难每遍都落在同一位置。演奏关心手感，步进关心位置；把动作拆成开关，重复才稳定。

## 声音是怎么来的

一条轨道是一行格子，行对应音高或鼓件，列对应步。每步有开关、力度与音高偏移，连步把相邻格并成一个长音。时钟每走一步，引擎读取整列，同时触发所有打开的行。步长由音符时值决定，一小节十六步就是十六分音符。

## 旋钮与做法

先定步长与循环长度，再放底鼓和军鼓，最后补踩镲。重音放在每四步的第一格；连步用于滑音与长音；用概率触发或几毫秒的微移打散机械感。改速度后确认步长仍按拍计算，而不是按秒。

## 耳朵要抓的点

听同一格重复时的稳定度，以及重音落在第几步。关掉踩镲只听底鼓，判断骨架是否成立；再打开踩镲，听十六分的密度有没有盖过人声。

## 容易弄错的

步进不等于电子音乐，任何需要精确重复的段落都能用。步进器也不等于量化，格子只是输入方式，输出仍可带力度与微差。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":138,"label":"十六个等长的步","label_en":"Sixteen equal steps","hint":"先数十六格，再听重音落在第几步","hint_en":"Count sixteen cells, then hear where the accent falls"}
```
:::

::: en
A step sequencer cuts time into equal cells, and each cell answers one question: does this step fire.

## The problem to solve

Drum machines and dance need sixteenth-note repetition that lands identically every pass. Playing by hand is about touch, while step sequencing is about position. Turning gestures into switches makes repetition stable and every cell editable.

## Where the sound comes from

One row is a lane, one column a step. Each cell holds on, off, velocity and pitch offset, and a tie joins adjacent cells into one note. On each clock step the engine reads the column and fires every active lane. Sixteen steps in a bar means sixteenth notes.

## Settings and practice

Set step length and loop length, place kick and snare, then add hats. Accent the first of every four steps, use ties for slides, and add probability or a micro-shift of a few milliseconds. After a tempo change, confirm steps still follow beats.

## What the ear catches

Hear how steady a repeated cell is and which step carries the accent. Mute the hats for the kick skeleton, then judge whether the sixteenths crowd the vocal.

## Common misunderstandings

Step sequencing is not only for electronic music, and a grid is not quantise. The grid is an input method, while the output can still carry velocity and timing offsets.

```audiolab
{"type": "rhythm", "sig": "4/4", "pattern": "s s s s s s s s s s s s s s s s", "bpm": 138, "label": "Sixteen equal steps", "label_en": "Sixteen equal steps", "hint": "先数十六格，再听重音落在第几步", "hint_en": "Count sixteen cells, then hear where the accent falls"}
```
:::
