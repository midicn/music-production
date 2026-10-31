---
id: drum-bus-glue
site: prod
cat: A6
order: 434
title: 鼓总线胶合：压缩、饱和与并行
title_en: Drum Bus Glue: Compression, Saturation and Parallel
summary: 胶合让分开录的鼓件像一套乐器，同时保住每一下的起音。
summary_en: Glue makes separately recorded drums feel like one kit while preserving the attack of each hit.
level: standard
tags: [混音, 鼓, 总线, 压缩, 饱和]
tags_en: [mixing, drums, bus, compression, saturation]
alias: [鼓总线, 鼓胶合, drum bus, drum glue]
links:
  - "[[glossary:bus]]"
  - "[[glossary:compressor]]"
  - "[[glossary:parallel-compression]]"
  - "[[instrument:drum-kit]]"
instances:
  - groove-000000 | 放克鼓循环瞬态清楚，胶合前后最容易对照
  - groove-000007 | 慢速摇滚鼓点留白多，适合听总线压缩是否拖尾
  - oga-000004 | 战斗循环鼓组持续满能量，饱和与并行的密度差一听便知
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook（Cengage）鼓总线压缩章节
  - Michael Stavrou, Mixing with Your Mind（Flux Research）鼓组与并行处理章节
  - Universal Audio, API 2500 Bus Compressor 官方使用说明
updated: 2026-10-31
---

::: zh
## 胶合与压扁的区别

鼓件分开录，起音时间、尾音长度、谐波都不同。胶合让它们共享一点包络与谐波，听起来像一个人在敲一套鼓；压扁则是每一下都被削到同一高度。前者保留军鼓的脆和底鼓的厚，后者让两者都变成墙。判断时旁通对比，听鼓组是否更像一件乐器，而不是只看压缩表动了多少。

## 三种工具

| 工具 | 作用 | 起点 | 过量 |
|---|---|---|---|
| 总线压缩 | 共享包络 | 2:1–4:1，启动 10–30 ms，释放 100–300 ms，1–3 dB | 军鼓失去起音，镲片抽吸 |
| 饱和 | 共享谐波 | 轻微驱动，并联混 5%–15% | 镲片刺、低频糊 |
| 并行压缩 | 补密度 | 快速压缩，混回 −12 至 −6 dB | 房间声变脏、瞬态重影 |

压缩负责整体起伏，饱和负责厚度，并行负责小音量下的存在感。三样都轻，合起来才有胶水感；任何一样过重，都会先吃掉瞬态。

## 一个可复现的起点

先把鼓组峰值控制在 −6 dBFS 左右，留够余量。总线压缩从二比一、二十毫秒启动、自动释放开始，表头动两 dB 就停。饱和只加一点，旁通时音量应几乎不变。并行支路用快启动、快释放的 FET 式压缩，压得狠一些，再混回总音量之下。每一步都与旁通对比，并把响度对齐。

## 顺序与增益

修频段的总线均衡放在压缩前，做音色的放在饱和后。并行支路从推子前取信号，返回不要再次进入鼓总线，否则会形成循环。补偿增益放在链尾，保证接通与旁通响度接近。总线推子给后续段落留三到六 dB 的自动化余量。

## 什么时候不用

爵士鼓、古典打击乐和已经重压过的采样循环，往往不需要再加胶合。底鼓与军鼓本来就不在一个律动里，先改演奏或编辑，再谈总线。并行压缩会把房间声一起放大，房间不好听时只会更脏。总线已经开始削波，任何压缩都救不回来。

```audiolab
{"type":"instrument","gm":"Taiko Drum","synth":"perc","phrase":["C2","C2","G1","C2"],"label":"四下鼓点，先听起音","label_en":"Four drum hits, listen to the attack","hint":"旁通总线处理，比较每一下的起音和尾巴是否还在","hint_en":"Bypass the bus processing and compare whether each attack and tail survives"}
```
:::

::: en
## Glue is not squash

Drums recorded apart differ in attack, tail and harmonics. Glue lets them share a little envelope and harmonic content so they feel like one kit played by one person; squash cuts every hit to the same height. Glue keeps the snap of the snare distinct from the weight of the kick; squash turns both into a wall. Compare bypass and ask whether the kit sounds more like one instrument, not how far the meter moves.

## Three tools

| Tool | Job | Starting point | Too much |
|---|---|---|---|
| Bus compression | shared envelope | 2:1–4:1, 10–30 ms attack, 100–300 ms release, 1–3 dB | snare loses attack, cymbals pump |
| Saturation | shared harmonics | gentle drive, 5%–15% parallel blend | harsh cymbals, muddy lows |
| Parallel compression | density | fast compression, blend −12 to −6 dB | dirty room, doubled transients |

Compression shapes the overall movement, saturation adds body, and the parallel path adds presence at low volume. Keep all three light; any one too heavy will eat the transients first.

## A repeatable starting point

Set drum peaks near −6 dBFS for headroom. Start bus compression at 2:1, 20 ms attack, auto release, and stop at 2 dB of gain reduction. Add slight saturation; bypassed level should hardly change. Use a fast FET-style compressor on the parallel path, compress harder, and blend it under the dry bus. Compare every stage against bypass at matched loudness.

## Order and gain

Corrective bus EQ before compression; tonal EQ after saturation. Feed the parallel path pre-fader, and do not route its return back into the drum bus or it will loop. Put makeup gain at the end so bypass and engaged levels are close. Leave 3–6 dB on the bus fader for later sections.

## When not to use it

Jazz drums, classical percussion and sample loops that are already compressed rarely need more glue. If kick and snare do not share a groove, fix performance or editing first. Parallel compression lifts the room too; a bad room only gets dirtier. Once the bus clips, no compressor will recover it.

```audiolab
{"type": "instrument", "gm": "Taiko Drum", "synth": "perc", "phrase": ["C2", "C2", "G1", "C2"], "label": "Four drum hits, listen to the attack", "label_en": "Four drum hits, listen to the attack", "hint": "Bypass the bus processing and compare whether each attack and tail survives", "hint_en": "Bypass the bus processing and compare whether each attack and tail survives"}
```
:::
