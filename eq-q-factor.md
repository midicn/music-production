---
id: eq-q-factor
site: prod
cat: A7
title: EQ 的 Q 值
title_en: The Q of an EQ
summary: Q 值决定提升的宽窄，同一条曲线会因它变成两种听感。
summary_en: Q sets how wide a boost or cut reaches, and the same curve can sound like two different moves.
level: standard
tags: [效果器, 均衡, Q 值, 听感]
tags_en: [effects, equalization, q factor, listening]
alias: [Q 值, 品质因数, 带宽, 钟形滤波, q factor, bandwidth]
links:
  - "[[glossary:eq]]"
  - "[[instrument:piano]]"
  - "[[instrument:voice]]"
instances:
  - thesession-000000 | 提琴旋律的音身共鸣集中，窄 Q 扫过时最容易听出音高感
  - giantmidi-000000 | 钢琴低音区有多个接近的共鸣峰，宽窄 Q 的差别很清楚
  - mutopia-000546 | 女声与钢琴同时出现，窄 Q 会先抓住某一个元音
sources:
  - Bristow-Johnson, Cookbook Formulae for Audio EQ Biquad Filter Coefficients — formulas checked, not quoted
  - Udo Zölzer, DAFX — Digital Audio Effects, filters chapter — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 要解决的事

提升同一个频点，Q 值一变，声音就从「整段变厚」变成「某个音高在叫」。Q 不决定提升多少，它决定这个提升占多宽。

## 工作方式

Q 是中心频率与带宽之比，带宽按 −3 dB 点计算。Q 越高，受影响的频段越窄，相位变化也越集中在中心附近。钟形滤波的 Q 与增益共同决定曲线，增益大时窄 Q 更容易出现振铃。搁架式的 Q 则改变转折的陡峭程度，而不是选出一个频点。

## 旋钮与耳朵

宽 Q 约 0.5–1，适合给整体加厚；2–4 用于处理具体的共鸣；高于 8 只适合找啸叫或做很窄的衰减。窄提升会带出类似音高的音色，宽提升更像换了一层垫子。扫频时先用高 Q 找到问题，再放宽度决定要带走多少。

## 耳朵要抓的点

在提琴或人声上从 200 Hz 扫到 800 Hz，保持提升量不变，只改 Q。窄 Q 经过某个频率时会突然「呜」一下，宽 Q 则让整段都变厚。换到钢琴低音区，窄 Q 的振铃更容易听成额外的嗡声。

```audiolab
{"type":"instrument","gm":"Fiddle","synth":"bowed","phrase":["G3","D4","A4","E4"],"label":"提琴上的窄 Q 扫频","label_en":"A narrow Q sweep on fiddle","hint":"先听干声，再把 Q 从宽收到窄，注意音身共鸣的变化","hint_en":"Hear it dry, then narrow Q for body resonance"}
```

## 容易弄错的

以为 Q 越高越精确就越好；以为 Q 只影响宽度、不影响相位；以为窄衰减没有副作用。
:::

::: en
## The problem to solve

Lift one frequency and change only Q, and the result moves from a thicker range to one pitch calling out. Q sets how much spectrum the boost occupies, not how much boost there is.

## The working principle

Q is the centre frequency divided by the bandwidth, measured between the minus 3 dB points. A higher Q narrows the band and concentrates the phase shift near the centre. On a bell filter, Q and gain shape the curve together, and a narrow high gain rings more. On a shelf, Q changes how abrupt the transition is, not which frequency is chosen.

## Knobs and ears

A wide Q near 0.5 to 1 thickens a range. Values from 2 to 4 address a specific resonance. Above 8 suits hunting a whistle. A narrow boost adds a pitch-like character; a wide one feels like another layer. Sweep to find the problem, then widen to decide how much to remove.

## What the ear should catch

Sweep a violin or voice from 200 Hz to 800 Hz, keep the boost fixed and change only Q. A narrow setting hums suddenly as it crosses one frequency; a wide one thickens the passage. On low piano notes, narrow ringing sounds like an extra drone.

```audiolab
{"type": "instrument", "gm": "Fiddle", "synth": "bowed", "phrase": ["G3", "D4", "A4", "E4"], "label": "A narrow Q sweep on fiddle", "label_en": "A narrow Q sweep on fiddle", "hint": "先听干声，再把 Q 从宽收到窄，注意音身共鸣的变化", "hint_en": "Hear it dry, then narrow Q for body resonance"}
```

## Easy to get wrong

That a higher Q is always better; that Q changes width but not phase; that a narrow cut has no side effects.
:::
