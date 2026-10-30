---
id: phase-and-delay
site: prod
cat: A5
title: 相位与延迟
title_en: Phase and Delay
summary: 相位差与延迟造成梳状滤波，改变音色与声像。
summary_en: Phase differences and delay cause comb filtering, changing timbre and stereo image.
level: standard
tags: [相位, 延迟, 梳状滤波, 极性, 单声道]
tags_en: [phase, delay, comb filtering, polarity, mono]
alias: [相位, 延迟, 极性, 梳状滤波, phase, delay, comb filtering]
links:
  - "[[glossary:phase]]"
  - "[[glossary:comb-filtering]]"
  - "[[glossary:delay]]"
  - "[[glossary:monitoring]]"
instances:
  - pdmx-000237 | 钢琴与贝斯的多轨爵士，单声道检查时低频与中央声像最容易暴露相位问题（C1）
  - essen-000517 | 单声部民歌，素材干净，适合做极性与延迟的对照（C1）
  - mutopia-000497 | 贝多芬第五交响曲，声部多，单声道下能听出哪些宽度来自相位（C1）
sources:
  - Everest, F. Alton，Master Handbook of Acoustics（McGraw-Hill）— 相位与梳状滤波章节核对，未引用
  - Howard, David M. & Angus, Jamie，Acoustics and Psychoacoustics（Focal Press）— 延迟与听觉章节核对，未引用
updated: 2026-10-28
---

::: zh
## 问题
两支话筒录同一声源，推子一合，低频少了、声音变薄；单声道检查时，宽大的合成器突然塌到中间。相位与延迟在求和时改变了频谱。

## 物理或房间
相位描述一个周期内的位置，延迟是时间平移。两个相同信号相隔 τ 秒相加，会在每半个周期的奇数倍处抵消，形成梳状滤波；τ 越小，梳齿越宽。极性反转是 180 度，不等于任意相位旋转。声音每米约延迟 2.9 毫秒。

## 做法与判断
先查极性，再查时间。用点击或脉冲对齐话筒与音箱单元，测脉冲响应，不能只靠耳朵猜。平行压缩的两路要同步，避免几毫秒延迟把低频挖空。单声道检查是必做项；某件乐器消失，先找延迟与相位，而不是加宽。

## 听什么
按单声道按钮，听低频与中央人声是否变薄；再切换一支话筒的极性，比较哪一种更实。播短促鼓点，听两路合并后音头是否变软。用延迟时，听梳状滤波是想要的颜色，还是意外的空洞。

## 常见误解
相位与极性不是一回事，180 度反转只是特例。反转极性不一定更好，要看话筒距离与声源。延迟不总是敌人，立体声加宽与回声都要用它。

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (steel)","synth":"plucked","phrase":["C4","G4","C4","G4"],"label":"短句，用延迟复制一路再听","label_en":"A short phrase, copied with a few milliseconds of delay","hint":"播这段短句，再用几毫秒延迟复制一路，注意低频与音头是否被梳状滤波改变。","hint_en":"Play this phrase, then copy it with a few milliseconds of delay; hear the bass and attack change as comb filtering sets in."}
```
:::

::: en
## The problem
Two mics on one source sum and the bass disappears; a wide synth collapses in mono. Phase and delay have changed the spectrum.

## Physics or room
Phase is position within a cycle; delay is a shift in time. Two identical signals separated by τ cancel at odd multiples of a half cycle, producing comb filtering. Polarity inversion is 180 degrees, not any phase rotation. Sound travels 2.9 ms per metre.

## Practice and judgement
Check polarity first, then time. Align mics and drivers with a click and measure. Keep parallel paths in sync, or a few milliseconds will scoop the bass. When an instrument vanishes, look for phase before adding width.

## What to listen for
Press mono and hear whether bass and vocal thin out; flip one mic's polarity. On a drum hit, hear if the attack softens. With delay, decide whether the comb is colour or a hole.

## Common misunderstandings
Phase and polarity differ; a 180-degree flip is a special case. Inverting is not always better; it depends on distance and source. Delay is not always the enemy; widening and echo rely on it.

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (steel)","synth":"plucked","phrase":["C4","G4","C4","G4"],"label":"A short phrase, copied with a few milliseconds of delay","label_en":"A short phrase, copied with a few milliseconds of delay","hint":"Play this phrase, then copy it with a few milliseconds of delay; hear the bass and attack change as comb filtering sets in.","hint_en":"Play this phrase, then copy it with a few milliseconds of delay; hear the bass and attack change as comb filtering sets in."}
```
:::
