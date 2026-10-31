---
id: mastering-chain-order
site: prod
cat: A8
title: 母带链顺序
title_en: Mastering Chain Order
summary: 每一级的位置，由它需要看见什么决定。
summary_en: Each stage earns its place by what it needs to see, not by habit or by the order in a preset.
level: standard
tags: [母带, 信号流, 压缩, 限制]
tags_en: [mastering, signal flow, compression, limiting]
alias: [母带链, 母带顺序, 母带信号链, mastering chain, chain order]
links:
  - "[[glossary:limiter]]"
  - "[[glossary:compressor]]"
  - "[[glossary:true-peak]]"
  - "[[glossary:lufs]]"
instances:
  - groove-000007 | 慢速摇滚鼓循环，总线压缩与限制的先后在军鼓上最容易分辨
  - musicnet-000019 | 巴赫赋格的声部交织，均衡放在压缩前后的清晰度差别明显
  - mutopia-001411 | 萨蒂《裸体歌舞》很安静，链上任何一级过量都会先吃掉尾音
sources:
  - Bob Katz, Mastering Audio.
  - iZotope, Ozone 11 documentation, signal chain and module order.
  - ITU-R BS.1770-4, Algorithms to Measure Audio Programme Loudness and True-peak Level.
updated: 2026-10-31
order: 452
---

::: zh
先限制再均衡，等于让限制器替一个还没修好的音色做决定。母带链的顺序由依赖关系决定，不由习惯决定。

## 顺序由依赖决定

修正型处理放在前面，因为它要看见原始问题。音色调整放在动态处理之前或之后，取决于你想让压缩器对哪一种频谱反应。饱和对电平敏感，放在限制器之前，才不会把已经压平的峰再削一次。抖动只在降位深时出现，位置固定在链尾。

## 一条可复用的链

| 顺序 | 环节 | 目的 | 复核点 |
|---|---|---|---|
| 1 | 修正均衡 | 去隆隆、收共振 | 低频变紧还是变薄 |
| 2 | 总线压缩 | 统一起伏 | 起音是否还在 |
| 3 | 音色均衡 | 宽搁架微调 | 中频是否塌陷 |
| 4 | 饱和 | 圆峰值、加密度 | 高频是否起沙 |
| 5 | 限制器 | 守住 ceiling | 释放是否抽吸 |
| 6 | 抖动 | 降位深 | 只在 16 bit 时 |

## 哪些情况要换顺序

线性相位均衡延迟大，放在限制器前会让前视判断失准，可以移到链首。多段压缩若只为修低频，放在宽频压缩之前更清楚。削波器替代限制器时，ceiling 要留得更低，后级不能再推。并行压缩与主链之间要对齐延迟，否则低频先被挖空。

## 耳朵要抓的点

每次只改一级，用同一响度对比。听鼓的起音、贝斯的持续、人声的齿音，以及最静处是否还在。限制器推 1–3 dB 后，先注意释放是否跟着底鼓抽吸，再听高频有没有砂纸感。

```audiolab
{"type":"instrument","gm":"Brass Section","synth":"brass","phrase":["C3","E3","G3","C4","G3","E3"],"label":"铜管齐奏，听链尾的峰值","label_en":"A brass tutti, listen at the end of the chain","hint":"先听齐奏的起音，再想压缩与限制先后调换后，哪一遍更早变硬","hint_en":"Hear the attack, then ask which order of compression and limiting hardens it sooner"}
```

## 顺序救不了的事

混音里的频段冲突不会因为母带链顺序正确而消失。压缩过量后，把限制器往后挪只会让抽吸更明显。限制器之后再抖动，噪声整形的效果会被下一级抹掉。两级限制串联，第二级通常只在替第一级收拾释放。
:::

::: en
Limiting before EQ asks the limiter to decide the tone of a mix that is not fixed yet. Chain order follows dependencies, not habit.

## Order follows dependency

Corrective work goes first because it has to see the original problem. Tone shaping sits before or after dynamics depending on which spectrum you want the compressor to react to. Saturation is level-sensitive, so it belongs before the limiter, where it cannot shave an already flattened peak. Dither appears only when bit depth drops, fixed at the end.

## A chain worth reusing

| Step | Stage | Purpose | What to check |
|---|---|---|---|
| 1 | Corrective EQ | Remove rumble, tame resonances | Low end tighter or thinner |
| 2 | Bus compression | Unify the movement | Attack still present |
| 3 | Tonal EQ | Gentle wide shelves | Mids not hollowed |
| 4 | Saturation | Round peaks, add density | Highs not gritty |
| 5 | Limiter | Hold the ceiling | Release not pumping |
| 6 | Dither | Reduce bit depth | Only at 16 bit |

## When the order changes

Linear-phase EQ adds latency, and ahead of a limiter it can mislead lookahead, so it may move to the front. Multiband compression used only for the low end reads more clearly before wideband compression. When a clipper replaces the limiter, set its ceiling lower, since nothing downstream can push again. Align the delay between parallel and main paths, or the low end cancels first.

## What the ear should catch

Change one stage at a time and compare at matched loudness. Listen to the kick attack, the sustain of the bass, vocal sibilance, and whether the quietest passage still exists. After 1–3 dB of limiting, check whether the release pumps with the kick, then listen for a sandy edge on the highs.

```audiolab
{"type": "instrument", "gm": "Brass Section", "synth": "brass", "phrase": ["C3", "E3", "G3", "C4", "G3", "E3"], "label": "A brass tutti, listen at the end of the chain", "label_en": "A brass tutti, listen at the end of the chain", "hint": "先听齐奏的起音，再想压缩与限制先后调换后，哪一遍更早变硬", "hint_en": "Hear the attack, then ask which order of compression and limiting hardens it sooner"}
```

## What order cannot fix

Frequency clashes in the mix do not vanish because the chain is in the right order. Once compression is excessive, moving the limiter later only makes the pumping clearer. Dither followed by another stage loses its noise shaping. With two limiters in series, the second usually just cleans up the release of the first.
:::
