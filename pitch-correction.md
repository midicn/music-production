---
id: pitch-correction
site: prod
cat: A7
title: 音高修正
title_en: Pitch Correction
summary: 修音高改的不只是音准，还有滑音、颤音与共振峰。
summary_en: Pitch correction moves more than tuning; it touches glides, vibrato and formants.
level: standard
tags: [效果器, 修音, 人声, 共振峰, 滑音]
tags_en: [effects, pitch correction, vocals, formants, glides]
alias: [音高修正, 修音, 自动修音, pitch correction, vocal tuning]
links:
  - "[[instrument:auto-tune]]"
  - "[[glossary:pitch]]"
  - "[[instrument:voice]]"
instances:
  - mutopia-000546 | 人声长音与钢琴伴奏，修音痕迹在长音尾巴上最容易听出
  - mutopia-000690 | 声乐线条多为半音级进，硬调会把滑音切成阶梯
  - essen-000517 | 单声部民歌旋律，没有伴奏掩盖，修音对滑音的改变很清楚
sources:
  - Zölzer, Udo，DAFX — Digital Audio Effects（Wiley）— 音高移位与共振峰处理章节核对，未引用
  - Sound On Sound, pitch correction explained — 硬调与软调听感描述核对，未引用
updated: 2026-10-28
---

::: zh
## 难在哪
修音高不是把每个音对准十二平均律。它同时改变滑音、颤音与共振峰，处理过头，人声会失去说话般的自然。

## 背后的逻辑
工具先检测基频，再通过时间拉伸与重采样把音移到目标。硬调在音符边界瞬间跳变，形成楼梯状的电音；软调用曲线过渡，保留一点滑音。共振峰若不随音高移动，声音会像花栗鼠或变低沉；现代工具把音高与共振峰分开，并允许保留颤音的深度与速率。

## 参数与取舍
先修长音与明显走音，再处理经过音。保留十到二十音分的自然偏差，完全归零反而僵硬。滑音处用曲线，不要用阶梯。合唱或二重唱共用参考音高时要留出差音，否则会出现梳状滤波。修正量以听不出修过为准，而不是以表头归零为准。

## 耳朵要抓的点
长音尾巴是否变平，滑音是否被切成半音，共振峰是否随音高移动，二重唱是否出现空洞的合唱效应。

```audiolab
{"type":"instrument","gm":"Voice Oohs","synth":"vocal","phrase":["A3","G3","F3","E3","D3","C3"],"label":"级进下行的人声","label_en":"A descending vocal line","hint":"先听音与音之间的滑动，再想象每一步被瞬间对齐成半音阶后的僵硬","hint_en":"Hear the slide between notes first, then imagine each step snapped instantly to the chromatic scale"}
```

## 容易弄错的
以为修音一定难听。轻量修正几乎不可闻，真正难听的是共振峰不动与零偏差。修音也不只用于人声，独奏管乐同样常见。
:::

::: en
## Where it gets hard
Pitch correction is not just aligning every note to equal temperament. It also moves glides, vibrato and formants, and past a point the voice loses its spoken naturalness.

## The logic behind it
The tool estimates the fundamental, then shifts it with time stretching and resampling. Hard tuning jumps at note boundaries and produces the familiar stair-step effect; soft tuning glides on a curve and keeps some portamento. If formants do not move with pitch, the result sounds like a chipmunk or a giant; modern tools separate pitch from formant and let vibrato depth and rate survive.

## Settings and trade-offs
Fix long notes and obvious errors first, then passing notes. Keep ten to twenty cents of natural deviation; zero is stiff. Use curves on glides, never steps. When a duet shares a reference pitch, leave some detune or a comb filter appears. Judge by whether the correction is audible, not by whether the display reads zero.

## What the ear catches
Whether long notes flatten out, whether glides become semitone steps, whether formants follow the pitch, and whether a duet develops a hollow chorus effect.

```audiolab
{"type": "instrument", "gm": "Voice Oohs", "synth": "vocal", "phrase": ["A3", "G3", "F3", "E3", "D3", "C3"], "label": "A descending vocal line", "label_en": "A descending vocal line", "hint": "先听音与音之间的滑动，再想象每一步被瞬间对齐成半音阶后的僵硬", "hint_en": "Hear the slide between notes first, then imagine each step snapped instantly to the chromatic scale"}
```

## Common misconceptions
That correction always sounds bad. Light correction is nearly inaudible; what sounds bad is frozen formants and zero deviation. Correction is not only for voices either; solo winds receive it just as often.
:::
