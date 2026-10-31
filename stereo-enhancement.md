---
id: stereo-enhancement
site: prod
cat: A8
title: 立体声增强
title_en: Stereo Enhancement
summary: 在不过度牺牲单声道兼容的前提下，让混音更宽更深。
summary_en: Widening and deepening a master through careful mid-side work while keeping mono compatibility and a solid centre.
level: standard
tags: [母带, 立体声, 声场]
tags_en: [mastering, stereo, imaging]
alias: [立体声加宽, 声场增强, stereo widening]
links:
  - "[[glossary:lufs]]"
  - "[[glossary:limiter]]"
  - "[[glossary:maximizer]]"
instances:
  - mutopia-000514 | 贝多芬第七第一乐章的乐队铺陈，适合听加宽后声场是否仍然稳
  - musicnet-000090 | 贝多芬四重奏的声部位置清楚，适合检查中置是否被拉空
  - pdmx-000407 | 维瓦尔第《春》的弦乐层次，适合对照加宽前后的单声道折叠
sources:
  - mid-side 处理与单声道兼容的判断，对照立体声与母带惯例整理。
  - 低频保持中置、侧向信号谨慎提升的做法（母带工程惯例）。
updated: 2026-10-28
---

::: zh
宽度首先来自编曲与空间，而不是插件上的旋钮。母带的立体声增强只能整理已有的空间，不能凭空造出深度。

## 问题

混音在音箱上听着很宽，折成单声道后鼓和人声却变薄。有人把 side 推得很高，结果低频散开，中心空了，手机外放只剩一层高频。

## 目标与标准

增强后，中心的人声、底鼓与贝斯仍然扎实，左右信息更清楚但不过分。单声道折叠时，主要元素不应明显掉音量或改变音色。常见做法是只提升 1 到 2 dB 的 side，低频保持中置，高频可以稍宽。宽度要服务音乐。

## 做法

先检查单声道，再决定是否需要加宽。需要时用 M/S 工具轻微提升 side，或只对 side 做高频搁架。加宽后重新检查相位与低频，必要时把低频单独留在中置。Haas 延迟要谨慎，超过三十毫秒就会变成可听的回声。

## 听什么

听中心的人声是否还站得住，鼓的低频是否仍集中，左右细节是否更清楚而不是更模糊。下面这段弦乐和声可以听声部之间的空间。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","B4"],"label":"和声里的空间","label_en":"Space inside a chord","hint":"先听四个声部的层次，再想加宽会不会把它们推散","hint_en":"Hear the four parts, then ask whether widening would pull them apart"}
```

## 常见误解

越宽越好的想法常让中心失去支撑。加宽插件也救不了本身很窄的编曲，那要回到声像与配器。
:::

::: en
Width comes first from arrangement and space, not from a knob. Mastering can tidy existing space; it cannot invent depth.

## The problem

A mix that sounds wide on speakers can turn thin in mono, with drums and vocal losing body. Push the side hard and the low end spreads, the centre empties.

## Goals and standards

After enhancement, the vocal, kick and bass still feel solid, while left and right information is clearer. In mono, key elements should not lose level or change tone. A common approach raises the side by only 1 to 2 dB and keeps lows centred.

## Practice

Check mono first, then decide whether widening is needed. Use a mid-side tool to lift the side gently, or add a high shelf to the side only. Recheck phase and low end, and keep bass centred. Haas delays over about thirty milliseconds become audible echoes.

## What to listen for

Hear whether the centre vocal still stands, whether drum low end stays focused, and whether side detail becomes clearer.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C4", "E4", "G4", "B4"], "label": "Space inside a chord", "label_en": "Space inside a chord", "hint": "先听四个声部的层次，再想加宽会不会把它们推散", "hint_en": "Hear the four parts, then ask whether widening would pull them apart"}
```

## Common misunderstandings

Wider is not better; excess width removes the centre's support. A widening plugin cannot rescue a narrow arrangement. Clumsy mid-side settings also break mono compatibility.
:::
