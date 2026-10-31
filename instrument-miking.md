---
id: instrument-miking
site: prod
cat: A4
title: 乐器拾音
title_en: Miking Instruments
summary: 钢琴、吉他、鼓与人声的拾音点不同，移动几厘米就能改变音色
summary_en: Pianos, guitars, drums and voices need different pickup points. A few centimetres can change the tone.
level: standard
tags: [录音, 摆位, 乐器]
tags_en: [recording, placement, instruments]
alias: [乐器拾音, 乐器录音, 拾音点, 钢琴拾音, 吉他拾音, 鼓拾音, instrument miking]
links:
  - "[[instrument:piano]]"
  - "[[instrument:drum-kit]]"
  - "[[instrument:classical-guitar]]"
  - "[[glossary:microphone]]"
instances:
  - atepp-003869 | 钢琴独奏，弦槌与音板的拾音点差别明显
  - mutopia-001541 | 尼龙弦吉他，12 品与音孔的音色差别清楚
  - groove-000010 | 鼓组各鼓件距离近，适合听鼓皮与鼓边的选择
sources:
  - Eargle, The Microphone Book, 3rd ed., instrument miking chapters
  - Bartlett, Practical Recording Techniques, acoustic instrument chapters
updated: 2026-10-28
---

::: zh
## 问题

每种乐器的发声方式不同，拾音点决定了你听到的是哪一部分。钢琴的弦槌、吉他的音孔、鼓的鼓皮、人声的唇齿，位置差几厘米，音色就换一个方向。

## 信号链

声源 → 话筒 → 话放 → 转换器。乐器拾音先选点，再选距离，最后选指向。近点取攻击与细节，远点取整体与空间；双点拾音要先查相位，再谈混合比例。

## 摆位与参数

钢琴双话筒在弦上方 20 至 30 厘米，避开中央，分别偏向高低音区。木吉他对准 12 品，距离 15 至 25 厘米，略偏琴颈可减少音孔轰鸣。军鼓上话筒距鼓皮 3 至 5 厘米，指向鼓心。人声 15 至 25 厘米，加防喷罩。

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (nylon)","synth":"plucked","phrase":["E3","B3","E4","G4"],"label":"拾音点改变音色","label_en":"The pickup point changes the tone","hint":"先听合成近似，再听 GM 采样，注意指板噪声与音孔厚度","hint_en":"Compare synth and GM sample, listening for fret noise and body depth"}
```

## 听什么

每移动 5 厘米录一次，听音头、木质与金属的比例。近点听手指与鼓棒细节，远点听乐器整体是否平衡。

## 常见误解

- **一支话筒能录好所有乐器** → 发声方式不同，拾音点无法通用。
- **越近越好** → 太近会放大气流、噪声与近讲效应。
- **立体声必须两支同型号** → 不同型号也能用，但要先查相位与音色差。
:::

::: en
## The problem

Every instrument radiates sound differently, and the pickup point decides which part you hear. A piano hammer, a guitar soundhole, a drum skin and a singer's lips all change character when the microphone moves a few centimetres.

## Signal chain

Source → microphone → preamp → converter. Choose the point first, then the distance, then the pattern. Close pickup gives attack and detail; distant pickup gives the whole instrument and the space. With two microphones, check phase before setting the blend.

## Placement and settings

For piano, place two microphones 20 to 30 cm above the strings, off centre and angled toward the high and low registers. For acoustic guitar, aim at the 12th fret from 15 to 25 cm, slightly toward the neck to reduce boom from the soundhole. For snare, put the top microphone 3 to 5 cm above the head, aimed at the centre. For voice, work at 15 to 25 cm with a pop filter.

```audiolab
{"type": "instrument", "gm": "Acoustic Guitar (nylon)", "synth": "plucked", "phrase": ["E3", "B3", "E4", "G4"], "label": "The pickup point changes the tone", "label_en": "The pickup point changes the tone", "hint": "先听合成近似，再听 GM 采样，注意指板噪声与音孔厚度", "hint_en": "Compare synth and GM sample, listening for fret noise and body depth"}
```

## What to listen for

Record at every 5 cm and compare the balance of attack, wood and metal. Close up, listen for fingers and sticks; farther away, check whether the instrument sounds balanced as a whole.

## Common misconceptions

- **One microphone suits every instrument** → the pickup point cannot be shared across different radiation patterns.
- **Closer is always better** → too close amplifies breath, noise and proximity effect.
- **Stereo requires matched models** → mismatched pairs can work, but check phase and tonal difference first.
:::
