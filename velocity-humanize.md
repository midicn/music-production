---
id: velocity-humanize
site: prod
cat: B2
title: 力度与人性化
title_en: Velocity and Humanising
summary: 力度与微小时差让程序化的声部重新有呼吸。
summary_en: Velocity and tiny timing offsets give a programmed part its breath back.
level: standard
tags: [音序, 力度, 人性化, MIDI]
tags_en: [sequencing, velocity, humanising, MIDI]
alias: [力度, 人性化, 随机微调, velocity, humanize, humanise]
links:
  - "[[glossary:velocity]]"
  - "[[glossary:midi-protocol]]"
  - "[[glossary:daw]]"
instances:
  - atepp-002442 | 戈德堡咏叹调，旋律与伴奏的轻重层次清楚
  - groove-000005 | 程序化嘻哈鼓型，每一击的力度几乎相同
  - atepp-001997 | 演奏版前奏，音与音之间有细微时差
sources:
  - MIDI 力度与音源响度、音色的映射关系，对照 MIDI 规范整理。
  - 人性化时差与力度范围的操作惯例（数字音频工作流惯例）。
updated: 2026-10-28
---

::: zh
力度决定一个音有多响、音色有多硬；人性化把过分工整的力度与时差重新打散。

## 卡住的地方

程序化的和弦每个音一样重，听感像一块板。真实演奏里，旋律音比伴奏音重，强拍比弱拍重，同一和弦内各音也不完全同时。

## 声音是怎么来的

MIDI 力度是 1 到 127 的整数，音源把它映射为响度与音色亮度，力度低时高频少。人性化工具在设定范围内随机改力度与音头位置；随机只解决太齐，解决不了重音逻辑。

## 旋钮与做法

先画力度曲线，让旋律音高出伴奏十到二十；强拍加三到五，弱拍减同样的量；时差控制在正负五到十五毫秒，底鼓与军鼓尽量少动；先量化再人性化，顺序反了会把微差再吸回去。

## 耳朵要抓的点

听重音是否落在该落的地方，而不是听有没有随机。同一和弦重复四次，注意每次的强弱走向是否一致。

## 容易弄错的

人性化不等于真实演奏，参数拉满只会得到另一种机械。力度也不只是音量，它同时改变音色。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s","bpm":96,"label":"每一步都一样重","label_en":"Every step the same weight","hint":"听这份整齐，再想哪里该有轻重","hint_en":"Hear the evenness, then ask where weight belongs"}
```
:::

::: en
Velocity sets how loud and how hard a note sounds; humanising scatters velocity and timing that have become too even.

## Where it snags

A programmed chord hits every note with the same weight and sounds like a slab. In real playing the melody outweighs the accompaniment, strong beats outweigh weak ones, and the notes of one chord are not perfectly simultaneous.

## Where the sound comes from

MIDI velocity is an integer from 1 to 127, mapped by the instrument to loudness and brightness; low velocity carries less high frequency. Humanise tools randomise velocity and attack within a range. Randomness fixes over-tidiness, not accent logic.

## Settings and practice

Draw a velocity curve, keeping melody notes ten to twenty above the accompaniment. Add three to five on strong beats and subtract the same on weak ones. Limit timing shifts to plus or minus five to fifteen milliseconds and leave kick and snare nearly fixed. Quantise before humanising, or the offsets get pulled back.

## What the ear catches

Hear whether accents land where they should, not whether randomness exists. Repeat one chord four times and follow the weight of each pass.

## Common misunderstandings

Humanising is not a real performance; maximum settings simply create another machine. Velocity is not only volume, since it changes timbre too.

```audiolab
{"type": "rhythm", "sig": "4/4", "pattern": "s s s s s s s s", "bpm": 96, "label": "Every step the same weight", "label_en": "Every step the same weight", "hint": "听这份整齐，再想哪里该有轻重", "hint_en": "Hear the evenness, then ask where weight belongs"}
```
:::
