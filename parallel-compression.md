---
id: parallel-compression
site: prod
cat: A6
title: 并行压缩
title_en: Parallel Compression
summary: 干声保留冲击，重压声补密度，两者并排而不是二选一。
summary_en: Keep the dry transient and add density from a crushed copy, side by side.
level: standard
tags: [混音, 压缩, 并行处理, 鼓]
tags_en: [mixing, compression, parallel, drums]
alias: [并行压缩, 并联压缩, parallel compression, New York compression]
links:
  - "[[glossary:compressor]]"
  - "[[glossary:bus]]"
  - "[[instrument:drum-kit]]"
  - "[[period:contemporary]]"
instances:
  - groove-000000 | 放克鼓组瞬态清楚，并行压缩的干湿比例容易判断
  - groove-000011 | 长循环超过三分钟，适合反复对比厚度与瞬态
  - pdmx-000450 | 大型合唱动态大，并行压缩可抬弱声而不动强声
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook, parallel compression section — background checked, not quoted
  - Huber and Runstein, Modern Recording Techniques, dynamics processing — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

直接压缩鼓组会把瞬态压平。想保留冲击力又要厚度，单靠一条压缩链很难两全。两条链各做一件事，反而更容易听清。

## 目标与判断

并行压缩把干声与重压声并排。判断标准是干声的点击仍在，重压声只补密度。若加入后鼓变慢或变糊，说明重压声的高频与瞬态被削得太多。

## 做法

复制鼓总线，重压到十比一以上，启动一到五毫秒，释放五十到一百毫秒，让增益衰减持续可见；把重压声高通到一百到二百赫兹再混入；干湿比例从一成起，加到能感到厚度为止。也可以只压房间轨，保留主对的清晰。混入时保持总线峰值不变，只比较密度与瞬态。

## 听什么

听军鼓的击打边缘是否还在；听底鼓尾巴是否变长；独奏重压声，听它是否只剩中频；旁通时整体是否只是变薄。

```audiolab
{"type":"instrument","gm":"Taiko Drum","synth":"perc","phrase":["C2","C2","G2","C2"],"label":"太鼓四击","label_en":"Four taiko hits","hint":"先听点击，再听并行压缩后的厚度","hint_en":"Hear the click, then the weight after parallel compression"}
```

## 常见误解

以为并行压缩等于并联均衡；以为重压声越大越好；以为所有素材都适合并行压缩。
:::

::: en
## The problem

Compressing a drum bus directly flattens transients. Keeping impact and adding weight with one chain is hard.

## Goal and judgement

Parallel compression runs a clean signal beside a heavily compressed copy. The dry click must remain; the compressed copy only adds density. If the drums slow down or blur, the copy has lost too much high end and transient.

## Method

Duplicate the drum bus. Compress the copy above 10 to 1 with 1 to 5 ms attack and 50 to 100 ms release, so gain reduction stays visible. High-pass the copy around 100 to 200 Hz before blending. Start at 10 percent wet and raise until weight is felt. The room mics alone can be compressed instead, leaving the main pair clear. Keep the bus peak matched while blending, so you compare density and transient rather than level.

## What to listen for

Whether the snare edge survives; whether the kick tail grows; whether the compressed copy alone is only midrange; whether bypass makes the whole kit merely thinner.

```audiolab
{"type": "instrument", "gm": "Taiko Drum", "synth": "perc", "phrase": ["C2", "C2", "G2", "C2"], "label": "Four taiko hits", "label_en": "Four taiko hits", "hint": "先听点击，再听并行压缩后的厚度", "hint_en": "Hear the click, then the weight after parallel compression"}
```

## Common misconceptions

That parallel compression is parallel EQ; that more compressed signal is better; that every source suits the technique.
:::
