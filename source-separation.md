---
id: source-separation
site: prod
cat: B7
title: 音源分离
title_en: Source Separation
summary: 音源分离把混音拆成若干轨，分离质量取决于重叠与相位。
summary_en: Source separation splits a mix into parts, and quality depends on overlap and phase.
level: standard
tags: [AI, 音源分离, 分轨, 混音]
tags_en: [AI, source separation, stems, mixing]
alias: [音源分离, 分轨, 人声分离, source separation, stem separation]
links:
  - "[[glossary:stems]]"
  - "[[glossary:mix-bus]]"
  - "[[glossary:timbre]]"
instances:
  - oga-000045 | 配乐层次厚，弦乐与合成垫音重叠，适合听分离后的串音
  - oga-000324 | 多层游戏配乐，鼓与低音的瞬态关系清楚，便于判断分离是否变软
  - mutopia-000439 | 人声与钢琴两个源，重叠少，是分离最容易成功的情形
  - thesession-000000 | 单声部民间曲调，分离前后几乎无差别，可当作对照
sources:
  - 音源分离的时频掩码与深度模型方法，对照公开论文整理。
  - 分离轨的伪影与串音评估（音乐信息检索资料）。
updated: 2026-10-28
---

::: zh
手上只有一轨立体声，却想单独改人声或鼓，音源分离就是把这层混合物拆开。

## 起点：一个问题

混音把各声部压进两个声道，频段、相位与混响都缠在一起。分离要判断每个时刻的每个频率属于谁，判断错就留下串音。

## 它怎么运转

常见做法是时频掩码，模型估计每个频点属于人声、鼓、贝斯或其他源，再重建波形。人声与鼓在频段和瞬态上差异大，容易分；两把吉他或弦乐群重叠多，容易互相带走。相位与混响会让分离轨留下金属味或空洞感。

## 做法与判断

先确定用途。只要人声就选人声模型，要重混就选多轨模型。分离前统一采样率，分出来后检查串音，用均衡与门限清理，不要把分离轨当原始分轨做大幅处理。需要反复调整时，保留未处理版本。

## 耳朵要抓的点

听齿音是否被削掉，鼓的瞬态是否变软，背景和声是否留在人声轨里。再听独奏时的房间尾巴，混响被拆散后常显得不自然。

## 容易弄错的

分离等于拿到分轨；分离越干净越好；分离后可以随意重混。分离是估计，不是还原，伪影会跟着处理一起被放大。

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["C3","G3","C4","E4","G4"],"label":"一层厚垫音，听各音能否被分开","label_en":"A thick pad, hear whether its notes can be pulled apart","hint":"先听整体，再试着只跟踪最低的那个音，分离算法面对的就是这件事","hint_en":"Hear the whole first, then follow only the lowest note; that is the task given to a separation model"}
```
:::

::: en
A single stereo file may be all you have, yet you want to change only the vocal or the drums. Source separation pulls the mixture apart.

## Starting point: a problem

A mix presses every part into two channels, where frequency ranges, phase and reverb overlap. Separation must decide which source owns each frequency at each moment; a wrong decision leaves bleed.

## How it runs

A common approach predicts a time-frequency mask for vocals, drums, bass or other sources, then rebuilds the waveform. Vocals and drums differ in range and attack, so they separate well; two guitars or a string section overlap and pull each other along. Phase and reverb leave a metallic or hollow residue.

## Practice and judgement

Decide the use first. Choose a vocal model for an a cappella, a multi-stem model for a remix. Match sample rates before separation, check bleed afterwards, clean with EQ and gating, and avoid heavy processing on separated stems. Keep an unprocessed copy.

## What the ear catches

Hear whether sibilance is dulled, drum transients softened and backing vocals left in the vocal stem. Then hear the room tail in solo; separated reverb sounds unnatural.

## Easy to get wrong

Separation gives you stems; cleaner is always better; separated tracks can be remixed freely. Separation is an estimate, not a recovery, and artefacts grow with processing.

```audiolab
{"type": "instrument", "gm": "Pad 2 (warm)", "synth": "bowed", "phrase": ["C3", "G3", "C4", "E4", "G4"], "label": "A thick pad, hear whether its notes can be pulled apart", "label_en": "A thick pad, hear whether its notes can be pulled apart", "hint": "先听整体，再试着只跟踪最低的那个音，分离算法面对的就是这件事", "hint_en": "Hear the whole first, then follow only the lowest note; that is the task given to a separation model"}
```
:::
