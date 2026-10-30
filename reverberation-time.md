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
  - cyberhymnal-000785 | 赞美诗《All for Jesus》，持续和弦与停顿清楚，适合听房间尾巴（C1）
  - atepp-000369 | 格里格《夜曲》，钢琴断句与踏板清楚，能比较不同位置的混响（C1）
  - essen-000191 | 单声部民歌，句尾有自然停顿，便于判断房间衰减（C1）
sources:
  - Everest, F. Alton，Master Handbook of Acoustics（McGraw-Hill）— 混响时间与临界距离章节核对，未引用
  - Newell, Philip，Recording Studio Design（Focal Press）— 控制室衰减目标章节核对，未引用
updated: 2026-10-28
---

::: zh
## 问题
同一套鼓，在小房间录得像纸盒，在大厅里却拖成一片；混音时加多少混响都不对。问题常不在效果器，而在房间的衰减时间。

## 物理或房间
RT60 是声源停止后声压级衰减 60 dB 所需的时间，随频率变化，低频通常更长。按 Sabine 公式，混响时间与房间容积成正比、与总吸声量成反比。小房间常在 0.2 到 0.4 秒，控制室希望更短且各频段接近；大厅可达 1.5 到 2.5 秒。直达声与混响声相等的位置叫临界距离。

## 做法与判断
先测，不先买材料。用拍手、气球或扫频测各频段衰减，看低频是否明显长于中频。处理顺序是低频陷阱、第一反射点、后墙扩散。目标不是越短越好，而是各频段平衡、尾巴干净。录人声时话筒留在临界距离以内。

## 听什么
在房间里拍手，听尾巴是「啪」还是「嗡」；说话时听辅音是否被拖尾糊住。播断奏钢琴，注意每个音结束后房间还剩多少。走到不同位置，临界距离外会突然变模糊。

## 常见误解
RT60 不是一个数，它随频率变化，单个数字会掩盖低频问题。混响长不一定坏，教堂与大厅需要长混响。地毯只吸高频，不能解决低频拖尾。

```audiolab
{"type":"instrument","gm":"Timpani","synth":"struck","phrase":["D2","A2","D3"],"label":"短促的三下，听尾巴多长","label_en":"Three short hits, how long is the tail","hint":"在房间里重放，听每一下之后尾巴多久消失；换到房间另一处再听。","hint_en":"Play this in the room and hear how long the tail lasts after each hit; repeat at another position."}
```
:::

::: en
## The problem
The same drums sound like a box in a small room and smeared in a hall; no reverb setting fixes it. The room's decay is the usual culprit.

## Physics or room
RT60 is the time for sound to fall 60 dB after the source stops. It varies with frequency, usually longer in the bass. Sabine's formula ties it to volume and absorption. Small rooms run 0.2 to 0.4 s, halls 1.5 to 2.5 s; where direct and reverberant sound are equal is the critical distance.

## Practice and judgement
Measure first. Use a clap or sweep to plot decay per band and see whether bass rings longer. Treat bass traps, reflections and the rear wall. Aim for even decay, not the shortest number. Keep vocal mics inside that distance.

## What to listen for
Clap and hear whether the tail snaps or booms; on speech, check whether consonants smear. Play staccato piano and hear what remains. Walk the room; beyond the critical distance it turns vague.

## Common misunderstandings
RT60 is not one number; it changes with frequency, and one figure hides bass problems. Long reverb is not always wrong; halls need it. Carpet absorbs highs, not bass ring.

```audiolab
{"type":"instrument","gm":"Timpani","synth":"struck","phrase":["D2","A2","D3"],"label":"Three short hits, how long is the tail","label_en":"Three short hits, how long is the tail","hint":"Play this in the room and hear how long the tail lasts after each hit; repeat at another position.","hint_en":"Play this in the room and hear how long the tail lasts after each hit; repeat at another position."}
```
:::
