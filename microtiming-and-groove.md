---
id: microtiming-and-groove
site: prod
cat: B2
title: 微时序与律动
title_en: Microtiming and Groove
summary: 音符不必落在整格上，几毫秒的前后推拉决定律动的手感。
summary_en: Notes need not sit on exact grid lines; a few milliseconds of push and pull decide how a groove feels.
level: standard
tags: [微时序, 律动, 摇摆, 量化]
tags_en: [microtiming, groove, swing, quantisation]
alias: [微时序, 律动, 摇摆感, microtiming, groove]
links:
  - "[[glossary:tempo]]"
  - "[[glossary:velocity]]"
  - "[[glossary:daw]]"
instances:
  - groove-000000 | 138 BPM 放克鼓组，军鼓比网格稍晚、踩镲稍早，律动才有推力（C1）
  - groove-000005 | 87 BPM 嘻哈鼓组，底鼓与采样切片的错位是风格的来源（C1）
  - thesession-005995 | 吉普赛风格曲调，装饰音在拍前抢进，听的是弹性而不是整齐（C1）
sources:
  - 摇摆比例与微时序的测量方法，依节奏研究公开资料核对，未抄原文
  - 鼓组时值与律动的关系，依制作实践通识核对，未抄文本
updated: 2026-10-28
---

::: zh
## 问题

把鼓组全部量化到网格，听起来干净却没有劲；把演奏原样保留，又可能散得合不拢。区别常在几毫秒：军鼓稍微落后、踩镲稍微提前、贝斯与底鼓咬合的方式，决定了这段律动是推着走还是拖着走。

## 原理

人耳对时间差的辨别在毫秒级，几毫秒的偏移就能改变律动的感觉。摇摆是把八分音符的后半拍往后推，推的比例从均分到三连音不等。不同乐器对时间的处理不同：鼓组里底鼓常在拍上，军鼓略后，踩镲略前；贝斯跟底鼓咬合，吉他扫弦可以稍早。量化把偏移抹平，也抹掉了风格。

## 参数与做法

先保留原始演奏，再局部量化：只量化明显出错的音，保留有意的偏移。用摇摆量化时选合适的比例，别一律套三连音。鼓组可以只量化底鼓，保留军鼓与踩镲的手感。贝斯与底鼓对齐，但保留细微的时间差以增加厚度。复制段落时连同微时序一起复制。过度对齐会让节奏失去人味，过度保留又会让段落之间接不上。

## 听什么

在放克鼓组里听军鼓略后带来的推力，在嘻哈鼓组里听底鼓与切片错位形成的摇摆，在吉普赛曲调里听装饰音抢拍的弹性。律动的差别不在音符本身，而在它们落下的时刻。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":138,"label":"推着走的十六分","label_en":"Sixteenths with forward lean","hint":"重音稍早一点会显得急，稍晚一点会显得拖，听两种的差别","hint_en":"Nudge accents earlier and the groove hurries; later and it drags; hear the difference"}
```
:::

::: en
## The problem

Quantise a drum kit fully to the grid and it sounds clean but has no push; leave the take untouched and it may fall apart. The difference often lies in a few milliseconds: a snare slightly late, a hi-hat slightly early, the way bass locks with kick. That is what makes a groove drive or drag.

## How it works

The ear resolves timing differences in the millisecond range, so a tiny offset changes how a groove feels. Swing pushes the second eighth of each pair later, anywhere from even to triplet feel. Instruments relate to time differently: in a kit the kick usually sits on the beat, the snare a touch behind and the hi-hat a touch ahead; bass locks to kick while guitar strums may lead. Quantisation erases offsets, and with them the style.

## Settings and practice

Keep the original take and quantise selectively, fixing obvious errors while preserving deliberate offsets. Choose a swing ratio that fits rather than applying triplets everywhere. On drums, quantise only the kick and leave the snare and hats alone. Align bass to kick but keep a small difference for weight. Copy microtiming along with duplicated sections. Over-alignment kills the human feel, while over-preservation makes sections fail to connect.

## What to listen for

On the funk kit, the push from a slightly late snare; on the hip-hop kit, the sway from kick against sliced samples; on the gypsy tune, the snap of ornaments landing early. The difference is not in the notes but in the moment they land.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":138,"label":"Sixteenths with forward lean","label_en":"Sixteenths with forward lean","hint":"Nudge accents earlier and the groove hurries; later and it drags; hear the difference","hint_en":"Nudge accents earlier and the groove hurries; later and it drags; hear the difference"}
```
:::
