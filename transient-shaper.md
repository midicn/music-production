---
id: transient-shaper
site: prod
cat: A7
title: 瞬态整形器
title_en: Transient Shaper
summary: 把音头与余音分开处理，为什么它不需要阈值也不会随力度变。
summary_en: Separating attack from sustain, and why a transient shaper needs no threshold and ignores playing level.
level: standard
tags: [效果器, 动态, 瞬态, 听感]
tags_en: [effects, dynamics, transient, listening]
alias: [瞬态整形器, 瞬态塑形, 音头, 延音, transient shaper]
links:
  - "[[glossary:compressor]]"
  - "[[instrument:drum-kit]]"
  - "[[glossary:bus]]"
instances:
  - groove-000006 | 流行鼓循环音头整齐，攻击加减对拍击感的影响最直接
  - groove-000010 | 放克鼓循环有轻有重，可检验整形器是否随力度改变结果
  - pdmx-000031 | 拉威尔《波莱罗》钢琴版节奏重复，音头变化不会被人声遮住
sources:
  - Udo Zölzer, DAFX — Digital Audio Effects, dynamics chapter — transient shaping background checked, not quoted
  - Sound On Sound, transient shaping explained — typical attack and sustain ranges checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

压缩器会连音头与余音一起压。瞬态整形器把两者分开，只动音头或只动余音，所以不需要阈值，也不会随演奏力度改变结果。

## 原理

包络跟随器取出快速与慢速两条包络，二者之差被当作瞬态成分。攻击旋钮改变前几毫秒的增益，延音旋钮改变后段电平。它本质是双包络的增益塑形器，不判断绝对电平，轻奏与重奏会得到同样的比例。

## 参数与听感

攻击加 3–6 dB，鼓槌的点击变清楚；攻击减 3 dB，声音变软、距离变远。延音减 2–4 dB 能让鼓更紧，加则更饱满。两段都推会很快失真，镲片尤其明显。

## 听什么

在鼓组上单独推攻击，先听底鼓的拍击，再听军鼓的响弦。切到钢琴，同样的动作像换了另一种触键。

```audiolab
{"type":"instrument","gm":"Marimba","synth":"struck","phrase":["C4","E4","G4","C5"],"label":"马林巴音头","label_en":"Marimba attacks","hint":"先听干声，再对比攻击加减的差别","hint_en":"Hear it dry, then compare attack cut and boost"}
```

## 常见误解

把瞬态整形器当压缩器；以为加攻击一定更响；用它代替 EQ 处理清晰度。
:::

::: en
## The question

A compressor turns down the attack and the body together. A transient shaper separates them, moving only the attack or only the sustain, so it needs no threshold and does not change with playing level.

## How it works

An envelope follower derives a fast and a slow envelope, and their difference is treated as the transient. The attack control changes gain over the first few milliseconds; the sustain control changes the later level. It is a dual-envelope gain shaper, not a level detector, so a soft and a hard hit receive the same proportional shape.

## Settings and what you hear

Plus 3 to 6 dB of attack sharpens a beater click; minus 3 dB softens the sound and pushes it back. Cutting sustain by 2 to 4 dB tightens a drum, while adding makes it fuller. Boosting both distorts quickly, especially on cymbals.

## What to listen for

On drums, raise attack alone and listen first to the kick beater, then to the snare wires. Switch to piano and the same move feels like a different touch.

```audiolab
{"type": "instrument", "gm": "Marimba", "synth": "struck", "phrase": ["C4", "E4", "G4", "C5"], "label": "Marimba attacks", "label_en": "Marimba attacks", "hint": "先听干声，再对比攻击加减的差别", "hint_en": "Hear it dry, then compare attack cut and boost"}
```

## Common misconceptions

That a transient shaper is a compressor; that more attack always means louder; that it can replace EQ for clarity.
:::
