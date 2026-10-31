---
id: layering-and-splits
site: prod
cat: B3
title: 分层与分键
title_en: Layering and Splits
summary: 一个键区叠几层、另一个键区换音色，键盘就这样被切开。
summary_en: Stack several voices in one range and switch timbre in another; the keyboard becomes a map.
level: standard
tags: [合成, 分层, 分键, 键盘]
tags_en: [synthesis, layering, split, keyboard]
alias: [分层与分键, 键盘分层, 键盘分键, layering and splits, split keyboard]
links:
  - "[[glossary:synthesizer]]"
  - "[[instrument:polysynth]]"
  - "[[instrument:organ]]"
  - "[[period:modern]]"
instances:
  - oga-000143 | 风琴、管钟与哨音各占一段音区，叠层与分键同时存在
  - oga-000033 | 弦乐分低高两区，钟琴与管钟再叠在高音区
  - oga-000309 | 大号、弦乐与钢琴共占低音区，音效层单独在高处
sources:
  - Gordon Reid, Sound On Sound Synth Secrets.
  - Curtis Roads, The Computer Music Tutorial.
updated: 2026-10-28
---

::: zh
## 要解决的事

一只手要弹和弦，另一只手要弹低音，两者音色还不一样；或者一个音要同时像钢琴和弦乐。分层与分键就是为这种需求把键盘分区、分堆。

## 一层层看原理

分层让同一个键同时触发多个声部，每个声部有自己的音色、音量、音区限制与效果。分键把键盘切成上下两段，各自指向不同声部，分界点可以移动。两者可以叠加：低音区一层贝斯加一层钢琴，高音区一层铺底加一层主音。复音数会被层数消耗，叠四层就等于每个音吃掉四个声部。音区限制可以防止两层在同一频段打架。

## 旋钮与耳朵

分层时两层的起音与衰减要接近，否则会听见先后两个音头。音量要让主层突出，副层低 6 到 10 dB 通常够用。分键点要避开旋律常用的音，否则演奏时会突然换音色。两层同音区同波形时，轻微失谐会变宽，完全同相则只是变响。

## 耳朵要抓的点

先听风琴与管钟的叠置，注意同一拍里有两个起音。再听弦乐的低高分区，判断分界大概落在哪个音。最后听低音区的大号、弦乐与钢琴，三层一起响时低频是否糊成一片。

```audiolab
{"type":"instrument","gm":"Drawbar Organ","synth":"blown","phrase":["C3","G3","C4","G4"],"label":"一层风琴加一层钟","label_en":"An organ layer with bells on top","hint":"先听风琴，再想象同键叠一层管钟；起音会变成两个，低音区保持风琴的厚，高音区多出金属边缘","hint_en":"Hear the organ, then imagine bells stacked on the same keys; the attack doubles, the low end keeps the organ body and the top gains a metallic edge"}
```

## 容易弄错的

以为分层越多越好；以为分键只是把键盘切开，忽略两层音区的重叠；忽略复音数被层数吃掉。
:::

::: en
## The problem to solve

One hand needs chords, the other bass, and the two want different timbres; or one key must sound like piano and strings. Layering and splits divide and stack the keyboard for these needs.

## Inside the mechanism

Layering makes one key trigger several voices, each with its own timbre, level, range and effects. A split cuts the keyboard into two sections, each aimed at a voice, with a movable break point. The two can combine: a bass and a piano in the low range, a pad and a lead up top. Polyphony is spent by layers, so four layers cost four voices per note. Key-range limits keep two layers from colliding in the same band.

## Knobs and ears

Layered voices need similar attack and decay, or two attacks arrive in sequence. The main layer should lead, and a secondary layer 6 to 10 dB lower is enough. Place the split away from notes the melody uses, or the timbre changes mid-phrase. Two layers in the same range with a slight detune widen; identical phase only makes them louder.

## What the ear should catch

Hear organ and bells stacked and notice two attacks on the same beat. Then hear the strings split between low and high registers and guess where the break sits. Finally hear tuba, strings and piano low and judge whether three layers turn the bass into mud.

```audiolab
{"type": "instrument", "gm": "Drawbar Organ", "synth": "blown", "phrase": ["C3", "G3", "C4", "G4"], "label": "An organ layer with bells on top", "label_en": "An organ layer with bells on top", "hint": "先听风琴，再想象同键叠一层管钟；起音会变成两个，低音区保持风琴的厚，高音区多出金属边缘", "hint_en": "Hear the organ, then imagine bells stacked on the same keys; the attack doubles, the low end keeps the organ body and the top gains a metallic edge"}
```

## Easy to get wrong

That more layers are always better; that a split only cuts the keyboard, when the two ranges may still overlap; that layered voices do not consume polyphony.
:::
