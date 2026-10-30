---
id: multiband-mastering
site: prod
cat: A8
title: 母带多段处理
title_en: Multiband Mastering
summary: 把频段分开处理，只修需要修的地方，保住整体音色。
summary_en: Splitting the spectrum so only the problem band is controlled, while the rest of the master keeps its tone and impact.
level: standard
tags: [母带, 多段压缩, 频段]
tags_en: [mastering, multiband, frequency]
alias: [多段压缩, 多段处理, multiband processing]
links:
  - "[[glossary:limiter]]"
  - "[[glossary:maximizer]]"
  - "[[glossary:lufs]]"
instances:
  - musicnet-000257 | 德沃夏克四重奏的中频密集，适合听多段处理是否让人声区变薄
  - pdmx-001129 | 贝多芬第五的低频与定音鼓冲击，适合观察低频段是否抽吸
  - groove-000008 | 灵魂乐鼓循环的低频稳定，适合对照分频点前后的鼓组
sources:
  - 多段压缩的分频、斜率与相位取舍，依动态处理与母带教材通识核查，未抄文本
  - 多段处理只修正问题频段的原则，依母带工程通识核查，未抄文本
updated: 2026-10-28
---

::: zh
多段处理把频谱分成几块，分别控制动态。它的价值是让一个问题频段不要拖累整首。

## 问题

全频压缩时，底鼓一敲，整首音量往下缩，高频也跟着抽吸。人声所在的中频本来就挤，再用单段压缩压整体，只会更扁。

## 目标与标准

只修需要修的频段，其他频段尽量不动。常见做法是分两到三段，分频点放在 100 到 200 Hz 与 1 到 3 kHz 附近。低频段可以更稳，中频保持人声与乐器的轮廓，高频只做轻微柔化。处理后整体音色、相位与单声道兼容都不应明显变化。

## 做法

先问问题是否真的来自某个频段，能用均衡解决就不要上多段。需要时从两段开始，逐步增加。低频段启动与释放较慢，中频轻压，高频少动。每次调整都用 bypass 对比，并检查分频点附近的相位与单声道折叠。

## 听什么

听底鼓出现时低频是否整体下沉，人声是否变薄，镲片是否突然更亮。下面这段钢琴的低音与和弦可以听分频点附近有没有断层。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","G3","C4","E4","G4"],"label":"低音与和弦的接缝","label_en":"Seam between bass and chord","hint":"注意低音与中高音之间是否还连成一件乐器","hint_en":"Does bass and mid still sound like one instrument"}
```

## 常见误解

多段不一定比单段好，分得越细越容易破坏相位与自然感。多段压缩也修不了单轨的问题，那些要回混音。它更不是响度工具，响度仍由限制与增益决定。
:::

::: en
Multiband processing splits the spectrum and controls each range. Its value is keeping one problem band from dragging down the whole master.

## The problem

With full-band compression, one kick pulls the whole level down and the highs pump. The midrange where the vocal lives is already crowded, and single-band compression flattens it further.

## Goals and standards

Fix only the band that needs it and leave the rest alone. A common approach uses two or three bands with crossovers near 100 to 200 Hz and 1 to 3 kHz. The low band can be steadier, the mid keeps outlines, and the top is only gently softened.

## Practice

Ask whether the problem really comes from one band; if EQ solves it, skip multiband. Start with two bands and add complexity slowly. Use slower attack on the low band, light mid compression and very little on top. Compare bypass and check phase.

## What to listen for

Hear whether the low end ducks when the kick lands, whether the vocal thins, and whether cymbals brighten.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C3", "G3", "C4", "E4", "G4"], "label": "Seam between bass and chord", "label_en": "Seam between bass and chord", "hint": "注意低音与中高音之间是否还连成一件乐器", "hint_en": "Does bass and mid still sound like one instrument"}
```

## Common misunderstandings

Multiband is not automatically better than single-band, and finer splits damage phase more easily. It cannot fix a single track either; that belongs in the mix. Nor is it a loudness tool.
:::
