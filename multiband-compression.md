---
id: multiband-compression
site: prod
cat: A7
title: 多段压缩
title_en: Multiband Compression
summary: 分频段各自控制动态，让低频不再拖着高频一起抽吸。
summary_en: Separate dynamics per frequency band, so the low end no longer pumps the whole mix.
level: standard
tags: [效果器, 动态, 多段压缩, 分频]
tags_en: [effects, dynamics, multiband, crossover]
alias: [多段压缩, 分频压缩, 多频段压缩, multiband compression, multiband]
links:
  - "[[glossary:compressor]]"
  - "[[glossary:eq]]"
  - "[[instrument:drum-kit]]"
instances:
  - groove-000011 | 鼓循环可渲染后送入多段处理器，分别观察低频与镲片频段的衰减 | Render the drum loop into a multiband processor and observe bass and cymbal-band reduction separately
  - oga-000001 | 管弦素材可检查分频前后差异，先旁通所有动态动作再比较分频本身 | Orchestral material can reveal crossover differences; bypass all dynamics before comparing the crossover itself
  - mutopia-000546 | 声乐与钢琴可用来判断目标频段是否需要独立动态控制，处理效果需实测 | Voice and piano can test whether one band needs independent control; assess actual processing results
sources:
  - Udo Zölzer, DAFX.
  - Giannoulis, Massberg and Reiss, Digital Dynamic Range Compressor Design, JAES 2012.
updated: 2026-11-02
---

::: zh
## 要解决的事

全频压缩使用共同增益控制时，某个频段触发的动作会影响整路声音。多段压缩按频带独立检测和处理，可减少不需要的联动；但也会带来分频、时间响应和频带平衡的新问题，应先确认是否真的需要。

## 它怎么工作

多段处理先用分频器分开频带，再分别检测和改变增益，最后相加。Linkwitz–Riley是一种常见分频设计，在满足设计与对齐条件时可得到平坦的求和幅度；并非所有产品都采用它。线性相位可让频带经历相近群延迟，但可能增加延迟和前振铃，不是没有任何副作用。

## 数值怎么变成声音

先确定哪一段在何时过量，再用尽量少的频带覆盖问题。独听频带帮助定位，最终以全频混合判断；调阈值让异常事件触发，再检查交叉频率附近是否产生新的音色变化。没有所有低频都要慢启动或每段都压2–4 dB的规则。

## 耳朵要抓的点

比较同一音频的全频压缩、只处理目标频带和旁通版本，匹配输出响度。观察高频是否仍随低频触发而变化，也检查分频本身的影响；需要时试动态EQ以避免不必要的全频带切分。

```audiolab
{"type":"instrument","drum":"36","synth":"perc","phrase":["36","42","38","42","36","42","38","46"],"label":"多段处理的鼓声素材","label_en":"Drum material for multiband processing","hint":"在 DAW 先关闭各段动态，只比较分频与旁通；再让一个频段动作，记录衰减量并等响度比较。","hint_en":"First disable band dynamics in a DAW and compare crossover versus bypass. Then activate one band, log gain reduction and compare at matched loudness."}
```

## 容易弄错的

以为多段压缩等于多段 EQ；以为分得越细越好；以为分频不会带来相位问题。
:::

::: en
## The problem to solve

With one gain control across the spectrum, an event detected in one band can affect the whole signal. Multiband compression detects and processes bands separately to reduce unwanted interaction, but introduces crossover, timing and balance considerations. First establish whether that separation is needed.

## How it works

Multiband processing splits bands, detects and changes gain separately, then sums them. Linkwitz–Riley is one common crossover design whose summed magnitude can be flat under the intended design and alignment conditions; not every product uses it. Linear-phase modes can equalise group delay between bands but may add latency and pre-ringing.

## From numbers to sound

Identify which band is excessive and when, then use as few bands as needed. Solo bands to locate issues but judge the full mix. Set threshold for unwanted events and inspect changes near crossovers. There is no rule that all bass needs slow attack or every band needs 2–4 dB reduction.

## What the ear should catch

Compare full-band compression, target-band processing and bypass on one audio source at matched loudness. Check whether highs still react to bass triggers and assess the crossover itself. Dynamic EQ may avoid unnecessary full-band splitting.

```audiolab
{"type":"instrument","drum":"36","synth":"perc","phrase":["36","42","38","42","36","42","38","46"],"label":"Drum material for multiband processing","label_en":"Drum material for multiband processing","hint":"First disable band dynamics in a DAW and compare crossover versus bypass. Then activate one band, log gain reduction and compare at matched loudness.","hint_en":"First disable band dynamics in a DAW and compare crossover versus bypass. Then activate one band, log gain reduction and compare at matched loudness."}
```

## Easy to get wrong

That multiband compression is multiband EQ; that more bands are always better; that splitting introduces no phase problems.
:::
