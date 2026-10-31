---
id: saturation
site: prod
cat: A7
title: 饱和器
title_en: Saturation
summary: 非线性如何造出二次与三次谐波，又为什么让峰值变圆。
summary_en: How nonlinearity adds second and third harmonics, rounds peaks, and changes perceived loudness.
level: standard
tags: [效果器, 谐波, 饱和, 听感]
tags_en: [effects, harmonics, saturation, listening]
alias: [饱和, 饱和器, 谐波失真, 软削波, saturation, saturator]
links:
  - "[[instrument:electric-guitar]]"
  - "[[glossary:eq]]"
  - "[[glossary:bus]]"
instances:
  - pdmx-000031 | 拉威尔《波莱罗》钢琴版力度逐渐增强，饱和对峰值的压缩容易听出
  - oga-000004 | 战斗段落的合成器与打击密集，小量饱和后整体是否变密一听便知
  - groove-000007 | 摇滚鼓循环本身偏厚，加饱和后镲片起沙的程度容易判断
sources:
  - Udo Zölzer, DAFX — Digital Audio Effects, nonlinear processing chapter — background checked, not quoted
  - Sound On Sound, saturation explained — harmonic behaviour checked, not quoted
updated: 2026-10-28
---

::: zh
## 这件事难在哪

饱和常被当作「失真」的同义词。它确实来自非线性，但目的通常不是破坏，而是增加谐波、压住尖峰，让声音在同样的响度下更靠前。

## 背后的机制

信号经过一条弯曲的传输曲线，正弦波被折出整数倍频率。曲线上下对称时以三次谐波为主，声音发硬；不对称时出现二次谐波，听感更暖。输入越大，谐波越多，峰值也被软削，动态因此自然收紧。数字实现若不做过采样，高频谐波会折返成混叠。

## 数值怎么变成声音

Drive 决定进入曲线的电平，混音控制干湿，输出补偿避免效果只是变响。轻推能让人声变实，重推会让镲片起沙；贝斯加饱和后在中频更容易被听见。

## 耳朵要抓的点

先听干净的正弦或贝斯，再加饱和，注意新出现的谐波与变圆的峰值。在鼓组上小量使用，听整体是否变密而不是变破。

```audiolab
{"type":"instrument","gm":"Overdriven Guitar","synth":"plucked","phrase":["E2","E2","G2","A2"],"label":"过载吉他","label_en":"Overdriven guitar","hint":"先听干声，再想象轻推与重推的差别","hint_en":"Hear it dry, then imagine a light and a heavy push"}
```

## 容易弄错的

把饱和当失真踏板；以为推得越多越好而忘了补偿；用饱和去掩盖浑浊。
:::

::: en
## What makes it hard

Saturation is often used as a synonym for distortion. It does come from nonlinearity, but the aim is usually not damage, it is extra harmonics and rounded peaks that make a sound sit forward at the same loudness.

## The mechanism

The signal passes through a curved transfer function, and a sine wave gains integer multiples of its frequency. A symmetric curve produces mostly third harmonic and sounds hard; an asymmetric one adds second harmonic and reads warmer. More input means more harmonics and soft peak clipping, so dynamics tighten naturally. Digital versions need oversampling, or high harmonics fold back as aliasing.

## From numbers to sound

Drive sets the level into the curve, mix controls dry and wet, and output trim stops the effect from being just louder. A light push solidifies a vocal; a heavy push makes cymbals sandy. Bass gains midrange presence after saturation.

## What the ear should catch

Hear a clean sine or bass first, then add saturation and notice the new harmonics and rounded peaks. Use a small amount on drums and hear whether the kit gets denser rather than broken.

```audiolab
{"type": "instrument", "gm": "Overdriven Guitar", "synth": "plucked", "phrase": ["E2", "E2", "G2", "A2"], "label": "Overdriven guitar", "label_en": "Overdriven guitar", "hint": "先听干声，再想象轻推与重推的差别", "hint_en": "Hear it dry, then imagine a light and a heavy push"}
```

## Easy to get wrong

That saturation is a distortion pedal; that more drive is better without output compensation; that saturation hides mud.
:::
