---
id: stereo-techniques
site: prod
cat: A4
title: 立体声制式
title_en: Stereo Techniques
summary: XY、ORTF、AB、MS 在宽度、相位与单声道兼容上各有取舍
summary_en: XY, ORTF, AB and MS trade width against phase and mono compatibility.
level: standard
tags: [录音, 立体声, 话筒摆位]
tags_en: [recording, stereo, microphone array]
alias: [立体声制式, 立体声拾音, XY, ORTF, AB, MS, stereo technique]
links:
  - "[[glossary:stereo-technique]]"
  - "[[glossary:phase]]"
  - "[[instrument:choir-scoring]]"
instances:
  - pdmx-000166 | 管弦乐声部铺得开，适合比较 XY 与 ORTF 的宽度
  - musicnet-000067 | 弦乐四重奏声像集中，适合听单声道兼容
  - m21-000602 | 合唱声部横向分布清楚，适合听 AB 的中间空洞
sources:
  - Streicher and Dooley, Basic Stereo Microphone Perspectives, AES preprint
  - Eargle, The Microphone Book, 3rd ed., stereo array chapters
updated: 2026-10-28
---

::: zh
## 问题

单支话筒只有一个点，听不出乐队宽度。两支话筒一放，时间差又会让某些频率抵消。制式就是在这两件事之间做选择，没有一种能同时拿到最宽、最稳与最好的单声道兼容。

## 信号链

XY 两支话筒重合，只有强度差，单声道兼容最好。ORTF 两支相距 17 厘米、夹角 110 度，兼有强度差与时间差。AB 间距更大，时间差主导，宽度大但单声道会变薄。MS 用一支中置心形与一支侧向 8 字，解码后宽度可调。

## 摆位与参数

XY 夹角 90 至 135 度，对准声源中心。ORTF 保持 17 厘米与 110 度。AB 从 40 至 60 厘米起，按声源宽度调整。MS 的侧向话筒要正对两侧，中置正对前方，再按 M+S 与 M-S 解码。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"宽度从哪里来","label_en":"Where the width comes from","hint":"先听合成近似，再听 GM 采样，注意声部是否铺开","hint_en":"Compare synth and GM sample, listening for how the parts spread"}
```

## 听什么

切到单声道，听中央是否变薄、低频是否还在；再听声源左右移动时是否连续。宽度不是越大越好，稳定更重要。

## 常见误解

- **间距越大越宽越好** → 时间差过大，单声道抵消更严重。
- **ORTF 属于 AB** → 它是夹角与间距的组合制式。
- **MS 必须三支话筒** → 两支就够，一支中置、一支侧向。
:::

::: en
## The problem

One microphone gives a single point and no sense of width. Two microphones introduce a time difference that cancels some frequencies. A stereo technique is a choice between those problems. None of them delivers maximum width, stability and mono compatibility at once.

## Signal chain

XY places two capsules together, so only level differs and mono compatibility is best. ORTF spaces them 17 cm apart at 110 degrees, combining level and time differences. AB uses a wider spacing where time dominates; it is wide but thins out in mono. MS uses a forward cardioid and a sideways figure-eight, with width adjustable at decode.

## Placement and settings

Set XY between 90 and 135 degrees, aimed at the centre of the source. Keep ORTF at 17 cm and 110 degrees. Start AB at 40 to 60 cm and widen for a larger source. For MS, point the side capsule at the sides and the mid capsule forward, then decode with M+S and M-S.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C4", "E4", "G4", "C5"], "label": "Where the width comes from", "label_en": "Where the width comes from", "hint": "先听合成近似，再听 GM 采样，注意声部是否铺开", "hint_en": "Compare synth and GM sample, listening for how the parts spread"}
```

## What to listen for

Switch to mono and hear whether the centre thins and the low end survives. Then listen for continuity as the source moves across the image. More width is not automatically better; stability matters more.

## Common misconceptions

- **Wider spacing always gives better width** → too much time difference causes stronger mono cancellation.
- **ORTF is a kind of AB** → it is a combined angle-and-spacing array.
- **MS needs three microphones** → two are enough, one mid and one side.
:::
