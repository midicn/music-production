---
id: piano-roll
site: prod
cat: B2
title: 钢琴卷帘
title_en: Piano Roll
summary: 音符变成横条，音高、时值与力度在一张网格里同时可见。
summary_en: Notes become horizontal bars, so pitch, length and velocity share one editable grid.
level: standard
tags: [音序, 钢琴卷帘, MIDI 编辑, 网格]
tags_en: [sequencing, piano roll, MIDI editing, grid]
alias: [钢琴卷帘, 卷帘窗, 钢琴卷轴, piano roll, pianoroll]
links:
  - "[[glossary:midi-protocol]]"
  - "[[glossary:velocity]]"
  - "[[glossary:daw]]"
instances:
  - atepp-001997 | 前奏的分解和弦在卷帘里是一排整齐的横条
  - pdmx-000373 | 左手长音与右手旋律的时值差别，在卷帘上一目了然
  - oga-000018 | 多轨游戏配乐，各声部的音区与重叠关系同屏可见
sources:
  - 钢琴卷帘的坐标、力度条与吸附设置，参考 DAW 文档。
  - 音符时值、连奏与多轨叠加的编辑方法；数字音频工作流惯例是主要依据。
updated: 2026-10-28
---

::: zh
钢琴卷帘把音符画成横条，纵轴是音高，横轴是时间，条的左端是音头。

## 为什么会碰到

和弦是否叠在一起、声部有没有交叉、一个音拖了多长，这些在事件列表里要逐行读。卷帘把这些问题摊在同一张图上，改音高只需上下拖一格。

## 背后的机制

纵轴按半音排列，旁边常配键盘；横轴按拍与小节分格。横条长度就是发声时长，下方力度条控制每个音的力度，再往下是控制器与踏板。多条轨道可以叠在同一视图里，用颜色区分；吸附决定拖动时落在哪个格。

## 旋钮与做法

网格设到实际用到的最大分辨率，常见是十六分或八分三连；需要连奏时把条的右端拖过下一音的音头；检查和弦内各音是否对齐；用另一轨的浅色音符作参照，避免声部撞在一起。

## 耳朵要抓的点

先听和弦是齐的还是依次滚开，再听长音有没有被下一个音切断。拖动一个音后，注意音头位置变化带来的推拉感。

## 容易弄错的

卷帘不只服务钢琴，任何有音高的声部都能用；它也不是乐谱的替代，读谱需要的连线与分句在这里看不到。横条不是音频，改长度不会改变音色。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5","G4","E4"],"label":"卷帘里的一串音符","label_en":"A phrase as bars in the roll","hint":"听音高与长短，想象它们在格子里的位置","hint_en":"Hear pitch and length, then picture the bars"}
```
:::

::: en
A piano roll draws notes as horizontal bars, with pitch vertical, time horizontal and the left edge as the attack.

## Why you meet it

Stacked or spread chords, crossing voices and note lengths take line-by-line reading in an event list. The roll puts them on one surface, and a pitch change becomes a one-cell drag.

## The mechanism

The vertical axis is chromatic, usually beside a keyboard, while the horizontal axis divides into beats and bars. Bar length is duration, a velocity lane sits below, and controller or pedal lanes follow. Several tracks can share the view in colours, and snap sets where a drag lands.

## Settings and practice

Set the grid to the finest value the part uses, often a sixteenth or an eighth-note triplet. For legato, drag the right edge past the next attack. Check chord alignment and use a ghosted track as a reference.

## What the ear catches

Hear whether chords arrive together or roll open, then whether a long note is cut. After moving a note, notice the push and pull of the new attack.

## Common misunderstandings

The roll serves any pitched part, not only piano, and it is not notation; slurs and phrasing are absent. Bars are not audio, so length does not change timbre.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "C5", "G4", "E4"], "label": "A phrase as bars in the roll", "label_en": "A phrase as bars in the roll", "hint": "听音高与长短，想象它们在格子里的位置", "hint_en": "Hear pitch and length, then picture the bars"}
```
:::
