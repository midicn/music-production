---
id: arpeggiator
site: prod
cat: B2
title: 琶音器
title_en: Arpeggiator
summary: 把按住的和弦拆成依次发声的音符序列。
summary_en: Turns a held chord into a sequence of single notes fired one after another.
level: standard
tags: [音序, 琶音, MIDI, 演奏]
tags_en: [sequencing, arpeggio, MIDI, performance]
alias: [琶音器, 琶音, 自动琶音, arpeggiator, arp]
links:
  - "[[glossary:arpeggio]]"
  - "[[instrument:sequencer]]"
  - "[[glossary:midi-protocol]]"
instances:
  - atepp-002861 | 平均律第一册 C 大调前奏，整段由分解和弦构成
  - thesession-005941 | 曲名即琶音，旋律在和弦音之间来回
  - pdmx-000373 | 左手分解和弦铺底，音型重复且有方向
sources:
  - 琶音器的排序模式与门限参数，对照合成器与音序软件说明整理。
  - 实时琶音与手写琶音的差别（键盘演奏惯例）。
updated: 2026-10-28
---

::: zh
琶音器把按住的音符拆开，按设定顺序与速度依次触发。

## 难在哪

一只手按和弦，另一只手弹旋律，很难再挤出连续的十六分。琶音器把静态和弦变成流动音型，速度与顺序都可控。

## 它怎么工作

它读取当前按住的音，按上行、下行、上下行、随机或按键顺序排列，再以设定的音符时值逐个发声。八度范围决定跨几个八度取音，门限决定每个音响多久，latch 让松手后继续运行。

## 旋钮与做法

速率设十六分，八度取一到二，门限百分之五十到八十；需要呼吸感时把门限缩短，需要铺底时拉长；latch 关闭便于现场换和弦；录成 MIDI 后再手改个别音，比一直挂着琶音器更灵活。

## 耳朵要抓的点

听每个音的间隔是否均匀，重音是否跟着按下的力度走。与手弹琶音对比，机器版更齐，手弹版有轻重与微小提前。

## 容易弄错的

琶音器不是音源，它只重排已有音符；上下行模式不一定在两端重复，具体取决于实现。画好的琶音与实时琶音听感接近，可改性完全不同。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"plucked","phrase":["C4","E4","G4","C5","G4","E4"],"label":"上行再下行的琶音","label_en":"An arpeggio up and back","hint":"听顺序与间隔，再想按住的和弦","hint_en":"Hear order and spacing, then picture the held chord"}
```
:::

::: en
An arpeggiator breaks a held chord into single notes, firing them in a set order and rate.

## Where it gets hard

One hand holds the chord and the other plays the melody, leaving no hand for continuous sixteenths. The arpeggiator turns a static chord into a moving figure with controllable order and speed.

## How it works

It reads the held notes, orders them up, down, up-down, randomly or as played, then triggers them one by one at the chosen note value. Octave range sets how far it reaches, gate sets how long each note sounds, and latch keeps it running after release.

## Settings and practice

Use a sixteenth rate, one or two octaves and a gate of fifty to eighty percent. Shorten the gate for air and lengthen it for a pad. Leave latch off when changing chords live, and record to MIDI so individual notes can be edited later.

## What the ear catches

Hear whether the spacing is even and whether accents follow the velocity you played. Against a hand-played arpeggio, the machine is tighter while the hand carries weight and small anticipations.

## Common misunderstandings

An arpeggiator is not a sound source; it only reorders existing notes. Up-down patterns do not always repeat the end notes, depending on the implementation. A drawn arpeggio can sound close to a live one but edits very differently.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "plucked", "phrase": ["C4", "E4", "G4", "C5", "G4", "E4"], "label": "An arpeggio up and back", "label_en": "An arpeggio up and back", "hint": "听顺序与间隔，再想按住的和弦", "hint_en": "Hear order and spacing, then picture the held chord"}
```
:::
