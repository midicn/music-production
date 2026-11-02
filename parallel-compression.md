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
  - groove-000000 | 可渲染鼓组，建立干声和压缩返回，匹配输出响度后比较瞬态与持续声 | Render the kit, create dry and compressed returns, then compare attack and sustain at matched loudness
  - groove-000011 | 循环适合固定小节反复比较并行比例，先检查延迟补偿与等响度 | Loop fixed bars to compare parallel balance after checking latency compensation and loudness
  - pdmx-000450 | 合唱可作动态练习；并行压缩会改变强弱比例，并非保证强声完全不变 | Choir offers dynamic practice; parallel compression changes relative levels rather than guaranteeing unchanged loud passages
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook, parallel compression section.
  - Huber and Runstein, Modern Recording Techniques, dynamics processing.
updated: 2026-11-02
---

::: zh
## 问题

并行压缩将原始路径与压缩路径混合，便于分别控制音头、持续部分与密度。常规串联压缩也能保留所需瞬态；是否使用并行取决于目标，不是两种效果无法兼得时的唯一选择。

## 目标与判断

加入并行支路后出现变薄、变糊或鼓点重影，应先检查路径延迟、极性和支路滤波，再判断压缩参数。数字插件的延迟补偿和干湿旋钮实现并不总相同；不要只把问题归因于压掉太多高频。

## 做法

先把两路设为无处理并匹配增益，验证相加行为；再只在支路加入压缩，保持原路径不变。从支路静音开始逐渐混入，听持续部分和背景声是否被抬高。比率、时间和支路高通应按素材选择；降低支路低频并不总是必要，也可能改变两路相位关系。

## 听什么

在完整混音里比较旁通与并行版本，匹配总体响度，检查音头、持续部分与原有背景声。独听压缩支路可以定位抽吸或失真，但是否合用应听回混后的结果；不要把更响或背景更明显直接当作密度改善。

```audiolab
{"type":"instrument","gm":"Taiko Drum","synth":"perc","phrase":["C2","C2","G2","C2"],"label":"并行压缩的鼓声素材","label_en":"Drum material for parallel compression","hint":"在 DAW 复制同一鼓声，一路压缩后混回；核对延迟补偿，等响度比较音头、持续声和尾音。","hint_en":"Duplicate one drum recording in a DAW, compress one path and blend it back. Check latency compensation and compare attack, sustain and decay at matched loudness."}
```

## 常见误解

以为并行压缩等于并联均衡；以为重压声越大越好；以为所有素材都适合并行压缩。
:::

::: en
## The problem

Parallel compression blends an original and a compressed path to control attacks, sustain and density separately. Serial compression can also preserve wanted attacks; parallel processing is a choice, not the only way to combine impact and body.

## Goal and judgement

If a parallel branch thins, blurs or doubles attacks, check delay, polarity and branch filtering before compression settings. Plug-in delay compensation and mix controls differ. Excessive high-frequency reduction is not the only possible cause.

## Method

First compare the two paths unprocessed at matched gain, then compress the branch with the original unchanged. Bring the branch up from silence and listen for raised sustain and background sound. Choose ratio, timing and any branch high-pass for the source; low-frequency filtering is not always needed and may change phase relationships.

## What to listen for

Compare bypass and parallel versions in the full mix at matched loudness, checking attack, sustain and existing background sound. Solo the compressed path to locate pumping or distortion, then judge the blend. More level or more audible background is not automatically useful density.

```audiolab
{"type":"instrument","gm":"Taiko Drum","synth":"perc","phrase":["C2","C2","G2","C2"],"label":"Drum material for parallel compression","label_en":"Drum material for parallel compression","hint":"Duplicate one drum recording in a DAW, compress one path and blend it back. Check latency compensation and compare attack, sustain and decay at matched loudness.","hint_en":"Duplicate one drum recording in a DAW, compress one path and blend it back. Check latency compensation and compare attack, sustain and decay at matched loudness."}
```

## Common misconceptions

That parallel compression is parallel EQ; that more compressed signal is better; that every source suits the technique.
:::
