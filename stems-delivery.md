---
id: stems-delivery
site: prod
cat: A1
title: Stems 交付
title_en: Delivering Stems
summary: 按约定把混音拆成若干组音频，交给母带、影视或现场使用。
summary_en: Splitting a mix into agreed groups of audio for mastering, film or live use, with formats and names that others can actually work with.
level: standard
tags: [交付, Stems, 工作流]
tags_en: [delivery, stems, workflow]
alias: [Stems, 分轨交付, 分组导出, stems delivery]
links:
  - "[[glossary:stems]]"
  - "[[glossary:bus]]"
  - "[[glossary:bit-depth]]"
instances:
  - pdmx-000407 | 《春》的合奏层次清楚，适合练按乐器组拆 stems
  - oga-000004 | 游戏战斗曲分层明显，交付时可按鼓、低音与旋律拆组
  - groove-000010 | 放克鼓循环的时值与力度层次，适合练分组的命名与对齐
sources:
  - Stems 与分轨、总线的区别，对照影视声音与母带交付惯例整理。
  - 48 kHz、24 bit 与等长起点等交付惯例（后期交付规范）。
updated: 2026-10-28
---

::: zh
Stems 是按约定拆开的几组音频，每一组可以独立调整，合起来又接近原来的混音。它不是分轨，也不是随便导出的几条总线。

## 为什么会用到

母带师要单独修鼓，影视混音要压对白下的音乐，游戏要按场景切换层次。给对方一条立体声混音不够用，给几十条分轨又太重。

## 为什么这样有效

Stems 通常按乐器组拆，比如鼓、贝斯、吉他、键盘、人声、效果。所有 stem 同时播放应接近混音，所以处理要提前分配好。文件从同一时间点开始，等长，采样率与位深统一，命名清楚。

## 参数与取舍

常见交付是 48 kHz、24 bit。峰值留余量，别在 stem 上做最终限制。附一份说明，写清有没有做总线处理、速度与调性。无处理版与打印版要分开。

## 耳朵要抓的点

先逐个 solo，再全放，检查相加是否与混音一致。若全放时某组突然变大，说明总线处理没有分配好。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","G4","D5"],"label":"一条弦乐 stem 的材料","label_en":"Material for one string stem","hint":"先听这一组，再想象它与其他组合起来","hint_en":"Hear this group alone, then imagine it summed with others"}
```

## 容易弄错的

Stems 不是分轨，分轨是每一件乐器，stems 是若干组。Stems 也不该各自母带，那会让相加后的平衡走样。
:::

::: en
Stems are a few agreed groups of audio that can be adjusted independently and still add up to something close to the mix. They are not multitracks, and not any bus you happen to export.

## Why you reach for it

A mastering engineer wants to fix only the drums; a film mixer must duck music under dialogue; a game needs layers that switch by scene. One stereo mix is not enough, and dozens of multitracks are too much.

## Why it works

Stems are usually split by instrument group, such as drums, bass, guitars, keys, vocals and effects. Played together they should resemble the mix, so processing must be divided deliberately. Files start at the same time, run the same length, share sample rate and bit depth, and carry clear names.

## Settings and trade-offs

A common delivery is 48 kHz and 24 bit. Leave peak headroom and do not limit individual stems. Include a note on bus processing, tempo and key. Keep an unprocessed set separate from the printed set.

## What the ear catches

Solo each stem, then play all together and check that the sum matches the mix. If one group jumps forward in the full set, the bus processing was not divided well.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C4", "G4", "D5"], "label": "Material for one string stem", "label_en": "Material for one string stem", "hint": "先听这一组，再想象它与其他组合起来", "hint_en": "Hear this group alone, then imagine it summed with others"}
```

## Easy to get wrong

Stems are not multitracks. Multitracks are individual instruments; stems are groups. Stems should not be mastered separately either, because that breaks the balance when they are summed.
:::
