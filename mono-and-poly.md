---
id: mono-and-poly
site: prod
cat: B3
title: 单音与复音
title_en: Mono and Poly
summary: 一次只响一个音还是同时响多个，决定了演奏与编曲的写法。
summary_en: One voice at a time or many at once; the choice changes both playing and arranging.
level: standard
tags: [合成, 单音, 复音, 声部]
tags_en: [synthesis, monophonic, polyphonic, voices]
alias: [单音与复音, 单音合成, 复音合成, mono and poly, monophonic polyphonic]
links:
  - "[[glossary:portamento]]"
  - "[[instrument:minimoog]]"
  - "[[instrument:polysynth]]"
  - "[[period:modern]]"
instances:
  - oga-000269 | 单通道主奏几乎不叠音，句子始终是一条单线
  - oga-000143 | 风琴同时按出六个音，厚和弦靠复音堆起来
  - oga-000330 | 钢琴、电钢琴与贝斯各自成声部，复音数被分给多层
sources:
  - Gordon Reid, Sound On Sound Synth Secrets — monophonic and polyphonic behaviour checked, not quoted
  - Curtis Roads, The Computer Music Tutorial — voice allocation checked, not quoted
updated: 2026-10-28
---

::: zh
## 这件事难在哪

为什么有些合成器一按新键，上一个音就断了；有些却能同时按住六个音？单音与复音不只是规格，它决定了句子怎么写。

## 一层层看原理

单音合成器只有一个发声单元，后按的键会接管前一个音，于是必须选择接管时是否滑音。复音合成器有多个声部，按键时分配空闲声部，声部用尽就偷取最早或最轻的音。复音数决定同时能响几个音，也决定长释放时会不会被截断。分频式复音是另一种做法，用少量振荡器分频出多个音，但同音名不能重复。

## 旋钮与耳朵

单音模式适合贝斯与主奏，句子要写成一条线，换音时的滑音时间决定它是「唱」还是「跳」。复音模式适合和弦与铺底，声部越多，低频越容易堆。偷音发生在释放很长时，听感是尾巴突然消失。单音加连奏时，包络不重触发，音头只出现一次。

## 耳朵要抓的点

先听单通道主奏，注意任意时刻只有一个音在响，换音时没有和弦。再听风琴和弦，数一数同时响几个音。最后听钢琴加贝斯，判断复音是被分给多层，还是留给了和弦。

```audiolab
{"type":"instrument","gm":"Lead 1 (square)","synth":"reed","phrase":["A3","C4","E4","A4"],"label":"先听单线，再想三音同响","label_en":"Hear a single line, then imagine three notes at once","hint":"先听一次只响一个音的旋律，再想象三个音同时按下；单音的滑音与断句会立刻变成和弦的厚度","hint_en":"Hear one note at a time, then imagine three keys held together; the glide and phrasing of a mono line become the thickness of a chord"}
```

## 容易弄错的

以为复音数只影响和弦；以为单音一定简单，单音线条的滑音与力度更难控制；忽略长释放会吃声部。
:::

::: en
## What makes it hard

Why does a new key cut off the previous note on some synths, while others hold six? Mono and poly are not just specifications; they decide how a line is written.

## Inside the mechanism

A mono synth has one voice, so a new key takes over the previous note, and the player chooses whether it glides. A poly synth has several voices; a keypress claims a free one, and when none remain it steals the oldest or quietest. Voice count sets how many notes can sound together, and whether long releases are cut short. Octave-divider polyphony generates several notes from a few oscillators, but the same note name cannot repeat.

## Knobs and ears

Mono suits bass and lead lines, written as a single thread; the glide between notes decides whether it sings or jumps. Poly suits chords and pads, and more voices pile up more low end. Voice stealing appears when releases are long, and the tail vanishes. In mono legato the envelope is not retriggered, so the attack appears once.

## What the ear should catch

Hear a single-channel lead and notice that only one note sounds at any moment, with no chord at the changes. Then hear an organ chord and count the notes sounding together. Finally hear piano plus bass and decide whether polyphony is spent on layers or saved for chords.

```audiolab
{"type": "instrument", "gm": "Lead 1 (square)", "synth": "reed", "phrase": ["A3", "C4", "E4", "A4"], "label": "Hear a single line, then imagine three notes at once", "label_en": "Hear a single line, then imagine three notes at once", "hint": "先听一次只响一个音的旋律，再想象三个音同时按下；单音的滑音与断句会立刻变成和弦的厚度", "hint_en": "Hear one note at a time, then imagine three keys held together; the glide and phrasing of a mono line become the thickness of a chord"}
```

## Easy to get wrong

That voice count only limits chords; that mono is always simpler, when glide and dynamics are harder to control on a single line; that long releases do not consume voices.
:::
