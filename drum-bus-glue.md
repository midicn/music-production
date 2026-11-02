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
  - groove-000000 | 放克鼓点的源素材，不包含胶合处理前后对照 | Funk drum events without before-and-after glue processing
  - groove-000007 | 慢速鼓型的空隙参照，拖尾变化须另施压缩检验 | Gaps in a slow drum pattern; compressor tail changes need separate processing
  - oga-000004 | 高密度鼓组编排参照，未比较饱和与并行处理 | Dense drum arrangement without a saturation-versus-parallel-processing comparison
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook（Cengage）鼓总线压缩章节
  - Michael Stavrou, Mixing with Your Mind（Flux Research）鼓组与并行处理章节
  - Universal Audio, API 2500 Bus Compressor 官方使用说明
updated: 2026-11-02
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

总线压缩会让多个鼓件共用检测和增益变化，饱和与并行处理则提供其他密度和音色选择。没有必要把三种都加上；先用旁通比较确定缺少的是峰值控制、持续部分还是音色，再选择一项。

## 一个可复现的起点

让鼓组输入留出与后续设备相容的余量，记录处理前峰值和响度。先调阈值观察哪些击打触发，再听攻击与释放是否符合节奏。并行支路从静音开始逐渐加入，补偿总输出后比较；所需衰减和干湿比例不能由统一数字决定。

## 顺序与增益

画清信号流：原鼓轨可同时送主鼓总线与并行压缩支路；并行返回也可以送回鼓总线，只要没有再从返回点送回自身输入形成闭环。推子前或推子后发送取决于希望怎样跟随音量变化。检查插件延迟补偿和单声道合并，再决定EQ位于压缩前还是后。

## 什么时候不用

若原素材已符合目标，可不再处理。并行压缩可能抬高房间声或串音，是否有用要在全组判断。若已经发生转换器或定点文件削波，后级压缩不能恢复被丢掉的波形；若只是浮点节点超过0 dBFS且未经过有界或非线性环节，降低增益可能仍能恢复余量。

```audiolab
{"type":"instrument","gm":"Taiko Drum","synth":"perc","phrase":["C2","C2","G1","C2"],"label":"鼓点起音参照","label_en":"Drum-attack reference","hint":"这里不提供总线处理旁通。请在同一鼓组音频上比较总线压缩的起音、余响和整体响度。","hint_en":"There is no bus-processing bypass here. Compare attack, sustain and loudness on the same drum audio through an actual bus compressor."}
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

Bus compression gives multiple kit pieces shared detection and gain changes; saturation and parallel processing offer other density and timbre choices. There is no need to use all three. Compare bypass first to determine whether the aim is peak control, sustain or timbre, then choose a process.

## A repeatable starting point

Leave input headroom suitable for the next stage and record peak and loudness. Set threshold to see which hits trigger processing, then judge attack and recovery against the groove. Bring a parallel branch up from silence and compare after output compensation. No universal reduction or blend value suits every kit.

## Order and gain

Draw the routing: drum tracks may feed a main bus and a parallel compressor, whose return may also enter the drum bus provided no route feeds its own input. Pre- or post-fader sends depend on desired level tracking. Check latency compensation and mono summing before choosing EQ before or after compression.

## When not to use it

Leave suitable source material alone. Parallel compression may raise room sound or spill, which must be judged in context. Compression cannot restore waveform information lost to converter or fixed-point clipping. If only a floating-point node exceeded 0 dBFS without a bounded or nonlinear stage, reducing gain may still recover headroom.

```audiolab
{"type":"instrument","gm":"Taiko Drum","synth":"perc","phrase":["C2","C2","G1","C2"],"label":"Drum-attack reference","label_en":"Drum-attack reference","hint":"There is no bus-processing bypass here. Compare attack, sustain and loudness on the same drum audio through an actual bus compressor.","hint_en":"There is no bus-processing bypass here. Compare attack, sustain and loudness on the same drum audio through an actual bus compressor."}
```
:::
