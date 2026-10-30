---
id: effects-chain-order
site: prod
cat: A7
title: 效果链顺序
title_en: Effect Chain Order
summary: 同一组效果换个先后，音色与动态就会走向不同的结果。
summary_en: The same effects in a different order take tone and dynamics to a different result.
level: standard
tags: [效果器, 信号流, 工作流, 听感]
tags_en: [effects, signal flow, workflow, listening]
alias: [效果链顺序, 效果器顺序, 信号链, 信号流, effect chain, signal chain]
links:
  - "[[glossary:gain-staging]]"
  - "[[glossary:eq]]"
  - "[[glossary:compressor]]"
  - "[[instrument:voice]]"
instances:
  - groove-000000 | 放克鼓循环的瞬态清楚，压缩与 EQ 的先后差别比想象中明显
  - mutopia-000546 | 女声与钢琴需要先修齿音再压缩，顺序错了会放大刺耳感
  - oga-000001 | 管弦铺底层次多，总线上先 EQ 后压缩更容易听出低频触发
sources:
  - Pirkle, Designing Audio Effect Plugins in C++ — signal flow sections checked, not quoted
  - Huber and Runstein, Modern Recording Techniques, effects and signal processing chapter — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

同一组效果，换个顺序就是另一种音色。顺序不是界面上的排列，而是信号实际经过的路径。

## 原理

线性效果如 EQ 可以交换，非线性和时间效果不行。失真对输入电平敏感，放在 EQ 前，EQ 会改变进入削波器的电平与频谱；放在 EQ 后，削波结果不会被后续滤波改变。压缩器放在混响前，会让混响尾巴保持稳定；放在混响后，尾巴会随干声一起被压。延迟与混响通常放在链尾，避免被失真重复削波。

## 参数与听感

人声链常见顺序是高通、去齿音、压缩、EQ、调制、延迟与混响。吉他链常见是滤波、过载、调制、延迟、混响。总线链把 EQ 与压缩放在最后，顺序取决于你想让谁先看到峰值。每加一个效果，都问它应该看见干声还是已经处理过的声音。

## 听什么

在放克鼓循环上对比「先压缩后 EQ」与「先 EQ 后压缩」，前者更稳，后者更容易让某些击打先触发压缩。在人声上把混响放到压缩前，听尾巴是否被压得忽大忽小。

```audiolab
{"type":"instrument","gm":"Electric Guitar (clean)","synth":"plucked","phrase":["E3","B3","G3","D4","A3","E4"],"label":"一条可改顺序的吉他句","label_en":"A guitar line whose chain can be reordered","hint":"先听干声，再想滤波与过载谁先看到这一句","hint_en":"Hear it dry, then ask whether filtering or drive should see the line first"}
```

## 常见误解

以为顺序无关；以为插件列表的顺序就是信号流；以为所有轨道都该用同一条链。
:::

::: en
## The question

The same effects in a different order become a different tone. Order is not the on-screen list but the path the signal travels.

## How it works

Linear effects such as EQ can trade places. Nonlinear and time-based effects cannot. Distortion is sensitive to input level, so an EQ before it changes the level and spectrum entering the clipper; an EQ after it filters an already clipped result. A compressor before reverb steadies the tail, while one after reverb pulls the tail down with the dry. Delay and reverb usually sit at the end so distortion cannot clip their repeats.

## Settings and what you hear

A vocal chain runs high-pass, de-esser, compressor, EQ, modulation, delay and reverb. A guitar chain runs filter, overdrive, modulation, delay and reverb. On a bus, EQ and compression come last, their order depending on which sees peaks first. For each effect, ask whether it should see the dry or processed sound.

## What to listen for

On a funk drum loop, compare compression before EQ with EQ before compression. The first stays steadier; the second lets some hits trigger the compressor. On a voice, put reverb before compression and hear whether the tail moves with the dry line.

```audiolab
{"type": "instrument", "gm": "Electric Guitar (clean)", "synth": "plucked", "phrase": ["E3", "B3", "G3", "D4", "A3", "E4"], "label": "A guitar line whose chain can be reordered", "label_en": "A guitar line whose chain can be reordered", "hint": "先听干声，再想滤波与过载谁先看到这一句", "hint_en": "Hear it dry, then ask whether filtering or drive should see the line first"}
```

## Common misconceptions

That order does not matter; that the order of plugins in a list is the signal flow; that every track should use the same chain.
:::
