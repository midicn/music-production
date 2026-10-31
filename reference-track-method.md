---
id: reference-track-method
site: prod
cat: A1
title: 参考曲目工作法
title_en: Working with Reference Tracks
summary: 用熟悉的成品当标尺，校准平衡、响度与空间，而不是凭当天心情。
summary_en: Using familiar finished records as a ruler for balance, loudness and space, with level matching so the comparison stays honest.
level: standard
tags: [参考曲, 混音, 工作流]
tags_en: [reference track, mixing, workflow]
alias: [参考曲, 参考曲目, A/B对比, reference track]
links:
  - "[[glossary:lufs]]"
  - "[[glossary:eq]]"
  - "[[glossary:compressor]]"
instances:
  - mutopia-001411 | 萨蒂《裸体歌舞》第一首，弱奏与空间感可作音色参考
  - pdmx-002278 | 《拉德茨基进行曲》的管弦动态，可作整体起伏的参照
  - groove-000008 | 灵魂乐鼓循环的时值与音色，适合做节奏参考
sources:
  - 参考曲目的选择与电平匹配方法，对照混音教材与听感训练惯例整理。
  - 响度匹配与 A/B 切换的做法（母带与监听惯例）。
updated: 2026-10-28
---

::: zh
参考曲目是一把尺子。用熟悉的成品校准平衡、响度与空间，比凭当天的心情可靠。

## 起点：一个问题

耳朵会漂移，房间也会骗人。同一套混音早上听着正好，晚上却觉得闷。参考曲提供已知的基准，让判断有落点。

## 背后的逻辑

选两到三首同类型、制作可靠的成品，把它们的响度降到与你正在做的音乐接近，再切换比较。一次只比一个维度，比如低频量、人声位置或混响长度。参考是标尺，不是模板，别把它的每个选择都搬过来。

## 参数与取舍

用响度表把参考降到同一 LUFS，避免响的听起来更好。切换点选在副歌或鼓组进入处。记录差异，比如参考的低频更少、人声更前，再回到自己的工程找对应参数。

## 耳朵要抓的点

听钢琴弱奏的空间，听管弦乐的动态，听灵魂乐鼓循环的时值。短句演示是中性的钢琴材料，用来校准音色，不承载参考曲的编曲。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5"],"label":"中性的钢琴参照","label_en":"A neutral piano reference","hint":"先记住它的亮度与尾音，再切到参考曲","hint_en":"Fix its brightness and tail in mind, then switch to the reference"}
```

## 容易弄错的

参考不是抄袭，学的是判断标准，不是旋律与音色。参考也不是越响越好，响度匹配之后，比较才公平。
:::

::: en
A reference track is a ruler. A familiar finished record calibrates balance, loudness and space better than the mood of the day.

## Starting point: a problem

Ears drift, and rooms lie. A mix that sounds right in the morning can sound dull at night. A reference gives a known baseline, so judgement has somewhere to land.

## The logic behind it

Choose two or three well-made tracks in the same genre, bring their loudness close to the music you are working on, then switch between them. Compare one dimension at a time, such as low-end weight, vocal position or reverb length. A reference is a ruler, not a template, so do not copy every choice.

## Settings and trade-offs

Match the reference to the same LUFS with a loudness meter so louder does not win. Switch at a chorus or where the drums enter. Write down the difference, such as less low end or a more forward vocal, then find the parameter in your own project.

## What the ear catches

Hear the space around a solo piano, the dynamics of an orchestra, the kick-to-bass ratio in soul. The short demo is neutral piano material for checking tone, not an arrangement to copy.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "C5"], "label": "A neutral piano reference", "label_en": "A neutral piano reference", "hint": "先记住它的亮度与尾音，再切到参考曲", "hint_en": "Fix its brightness and tail in mind, then switch to the reference"}
```

## Easy to get wrong

Reference is not plagiarism. You learn a standard, not a melody or a sound. Louder is not better either; only after loudness matching is the comparison fair.
:::
