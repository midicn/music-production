---
id: phase-problems
site: prod
cat: A4
title: 相位问题
title_en: Phase Problems
summary: 两支话筒收同一声音，时间差会把某些频率抵消，先查相位再调音色
summary_en: Two microphones on one source produce time differences that cancel frequencies. Check phase before tone.
level: standard
tags: [录音, 相位, 多话筒]
tags_en: [recording, phase, multiple microphones]
alias: [相位, 相位抵消, 梳状滤波, 极性, phase, comb filtering, polarity]
links:
  - "[[glossary:phase]]"
  - "[[glossary:phase-check]]"
  - "[[glossary:stereo-technique]]"
instances:
  - groove-000010 | 鼓组多话筒，顶与底最容易出相位问题
  - atepp-003869 | 钢琴双点拾音，梳状滤波在持续音上最明显
  - musicnet-000067 | 弦乐四重奏多话筒，合起来才听得出中频变薄
sources:
  - AES Convention paper on comb filtering and microphone arrays
  - Eargle, The Microphone Book, 3rd ed., multi-microphone phase chapters
updated: 2026-10-28
---

::: zh
## 问题

两支话筒收同一个声音，只要到达时间不同，某些频率就会抵消。听起来像 EQ 被挖空，怎么推都补不回来。独奏时不明显，两支合起来才暴露。

## 信号链

声波到达两支话筒的时间差造成相位差，叠加后形成梳状滤波。极性反转是 180 度，对所有频率一样；时间对齐则随频率变化。两者不是一回事。距离差越大，抵消的频率越低、间隔越密。

## 摆位与参数

遵守三比一规则，第二支话筒到声源的距离至少是第一支的三倍。鼓的顶与底、钢琴的双点、吉他的近远，都要先查极性。需要微调时用样本延迟对齐，不要只按反相开关。

```audiolab
{"type":"instrument","drum":"36","synth":"perc","phrase":["36","38","42"],"label":"低频先抵消","label_en":"The low end cancels first","hint":"先听合成近似，再听 GM 打击采样，注意鼓心的厚度","hint_en":"Compare synth and GM drum sample, listening for body on the kick"}
```

## 听什么

把两支话筒合到单声道，听低频与中频是否变薄；移动一支话筒几厘米，听音色是否突然变空。也可以只在一支话筒上做极性反转，比较两种叠加结果。

## 常见误解

- **相位就是极性** → 极性只是 180 度的一个特例。
- **反相开关能解决所有相位问题** → 时间差造成的梳状滤波需要延迟。
- **相位只在录音时存在** → 混音的多话筒素材同样要查。
:::

::: en
## The problem

When two microphones hear the same source, any difference in arrival time cancels some frequencies. It sounds like a hole cut into the EQ that no boost can fill. A single microphone hides it; the pair exposes it.

## Signal chain

The time difference between the two arrivals creates a phase difference, and summing them produces comb filtering. Polarity inversion is 180 degrees at every frequency; time alignment shifts with frequency. They are not the same thing. A larger distance difference pushes the first cancellation lower and the notches closer together.

## Placement and settings

Follow the three-to-one rule — the second microphone should be at least three times farther from the source than the first. Check polarity on the top and bottom of a drum, on two piano pickups and on close plus distant guitar mics. Fine-tune with sample delay rather than relying on the polarity switch alone.

```audiolab
{"type": "instrument", "drum": "36", "synth": "perc", "phrase": ["36", "38", "42"], "label": "The low end cancels first", "label_en": "The low end cancels first", "hint": "先听合成近似，再听 GM 打击采样，注意鼓心的厚度", "hint_en": "Compare synth and GM drum sample, listening for body on the kick"}
```

## What to listen for

Sum the two microphones to mono and hear whether the lows and low mids thin out. Move one microphone a few centimetres and listen for a sudden hollow tone. You can also invert polarity on one microphone and compare the two sums.

## Common misconceptions

- **Phase is polarity** → polarity is only the 180-degree case.
- **The polarity switch fixes every phase problem** → comb filtering from a time difference needs delay.
- **Phase only matters while tracking** → multi-microphone material needs the same check at mixdown.
:::
