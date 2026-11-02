---
id: reverberation-time
site: prod
cat: A5
title: 混响时间 RT60
title_en: Reverberation Time (RT60)
summary: RT60 描述房间衰减快慢，是判断录音与混音空间的基准。
summary_en: RT60 describes how fast a room decays and is the baseline for judging recording and mixing spaces.
level: standard
tags: [混响时间, RT60, 临界距离, 声学测量, 衰减]
tags_en: [reverberation time, RT60, critical distance, acoustic measurement, decay]
alias: [混响时间, 残响时间, RT60, reverberation time, decay time]
links:
  - "[[glossary:reverb]]"
  - "[[glossary:absorption]]"
  - "[[glossary:room-treatment]]"
  - "[[glossary:monitoring]]"
instances:
  - cyberhymnal-000785 | 持续和弦与停顿可作房间重放练习；量化衰减需测量信号与脉冲响应 | Chords and pauses support room playback practice; quantitative decay requires measurement signals and impulse responses
  - atepp-000369 | 可用钢琴断句作听感参考，勿把音源或踏板尾音直接计为房间 RT60 | Piano phrasing is a listening reference; do not count source or pedal decay directly as room RT60
  - essen-000191 | 短句可用于辨认停顿后的残响，房间衰减测量仍需覆盖目标频段 | A short phrase helps identify residual reverb; room measurements still require coverage of the target frequency bands
sources:
  - Everest, F. Alton，Master Handbook of Acoustics（McGraw-Hill）— 混响时间与临界距离章节核对，未引用
  - Newell, Philip，Recording Studio Design（Focal Press）— 控制室衰减目标章节核对，未引用
updated: 2026-11-02
---

::: zh
## 问题
同一套鼓，在小房间录得像纸盒，在大厅里却拖成一片；混音时加多少混响都不对。问题常不在效果器，而在房间的衰减时间。

## 物理或房间
混响时间按频带描述声能衰减，常以衰减60 dB的等效时间表示。实际测量可能从较短的有效衰减区间外推，需满足信噪比和测量规范。Sabine公式适用于一定扩散声场等假设，小房间的低频常由离散模态主导，不能只用一个宽带RT60数字评价。临界距离描述直达与混响能量相当的区域，并不是越过后音色突然改变的边界。

## 做法与判断
用合适的测量声源和分析方法，在多个位置检查各频带衰减与早期反射。拍手只适合发现明显回声，不足以可靠测量低频。是否使用吸收、扩散或改变位置，应由测量和用途决定；不能把“低频陷阱→反射点→后墙扩散”当所有房间的施工顺序。

## 听什么
主观听音可记录停顿后的尾音、语音清晰度和位置差异，但播放音色自身的混响、扬声器与房间会共同影响结果。需要比较房间时固定音源、播放电平和位置；不要把某个MIDI音色的长尾直接当作房间RT60。

## 常见误解
RT60 不是一个数，它随频率变化，单个数字会掩盖低频问题。混响长不一定坏，教堂与大厅需要长混响。地毯只吸高频，不能解决低频拖尾。

```audiolab
{"type":"instrument","gm":"Timpani","synth":"struck","phrase":["D2","A2","D3"],"label":"鼓声尾音与房间尾音","label_en":"Instrument decay and room decay","hint":"鼓音源自身有尾音，播放它只能作房间听感参考；测 RT60 请使用合适激励、测量麦克风及分频段衰减分析。","hint_en":"The drum source has its own decay, so playback is only a room-listening reference. Measure RT60 with suitable excitation, a measurement mic and band-limited decay analysis."}
```
:::

::: en
## The problem
The same drums sound like a box in a small room and smeared in a hall; no reverb setting fixes it. The room's decay is the usual culprit.

## Physics or room
Reverberation time describes decay by frequency band, commonly as an equivalent 60 dB decay time. Measurements may extrapolate from shorter usable decay intervals subject to noise and method requirements. Sabine’s formula assumes conditions such as a diffuse field; small-room bass may be dominated by discrete modes, so one broadband RT60 figure is insufficient. Critical distance is not an abrupt tonal boundary.

## Practice and judgement
Measure decay and early reflections in several positions using an appropriate source and analysis method. Claps can reveal obvious echoes but do not reliably measure bass decay. Choose absorption, diffusion or repositioning for the findings and use, not one construction sequence for every room.

## What to listen for
Listening can log tails, speech clarity and positional differences, but instrument reverb, loudspeaker and room all contribute. Fix source, level and positions for room comparisons rather than taking a MIDI instrument’s decay as the room RT60.

## Common misunderstandings
RT60 is not one number; it changes with frequency, and one figure hides bass problems. Long reverb is not always wrong; halls need it. Carpet absorbs highs, not bass ring.

```audiolab
{"type":"instrument","gm":"Timpani","synth":"struck","phrase":["D2","A2","D3"],"label":"Instrument decay and room decay","label_en":"Instrument decay and room decay","hint":"The drum source has its own decay, so playback is only a room-listening reference. Measure RT60 with suitable excitation, a measurement mic and band-limited decay analysis.","hint_en":"The drum source has its own decay, so playback is only a room-listening reference. Measure RT60 with suitable excitation, a measurement mic and band-limited decay analysis."}
```
:::
