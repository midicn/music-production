---
id: phaser
site: prod
cat: A7
title: 相位器
title_en: The Phaser
summary: 全通滤波器移动陷波，扫动比镶边更柔、更宽。
summary_en: All-pass stages move notches for a sweep that is softer and wider than flanging.
level: standard
tags: [效果器, 调制, 相位器, 全通滤波]
tags_en: [effects, modulation, phaser, all-pass]
alias: [相位器, 移相器, 全通滤波, phaser, phase shifter]
links:
  - "[[glossary:phase]]"
  - "[[glossary:modulation]]"
  - "[[instrument:polysynth]]"
instances:
  - oga-000057 | 太空铺底的和声长而稳定，慢速相位扫动容易听出层次
  - oga-000306 | 雪景音乐以稀疏长音为主，陷波移动不会被鼓点遮住
  - groove-000014 | 爵士放克鼓循环里的踩镲持续，能听出扫动经过高频的位置
sources:
  - Vadim Zavalishin, The Art of VA Filter Design — all-pass stages checked, not quoted
  - Udo Zölzer, DAFX — Digital Audio Effects, modulation chapter — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 这件事难在哪

相位器也做扫动，但它不靠延迟，而靠全通滤波器改变相位。听感比镶边更柔，陷波位置不按谐波排列。

## 它怎么工作

几级全通滤波器在特定频率产生相位移动，与原信号相加后形成陷波。LFO 扫过全通级的中心频率，陷波就上下移动。级数越多，陷波越多；反馈让陷波更深，也会带出类似共振的峰值。因为陷波间隔不均匀，相位器听起来不像镶边那样有明显的金属梳子。

## 数值怎么变成声音

4 级最温和，8–12 级更明显；rate 0.05–1 Hz 适合铺底，2 Hz 以上适合节奏素材。depth 控制扫动范围，feedback 20–50% 增加尖锐度。干湿各半时陷波最清楚，全湿会变成另一种音色。

## 耳朵要抓的点

在环境铺底上把 rate 设到 0.1 Hz，听陷波从低频慢慢移到高频，像一层雾在移动。换到爵士鼓循环，注意踩镲的声像是否随扫动漂移。再与镶边对比，相位器的扫动更宽、更慢，缺少梳状的金属边。

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["C4","E4","G4","B4","G4","E4"],"label":"温暖铺底的长和弦","label_en":"A warm sustained pad","hint":"先听干声，再想象四级全通缓慢扫过时陷波的位置","hint_en":"Hear it dry, then picture the notches of four all-pass stages sweeping slowly"}
```

## 容易弄错的

以为相位器会改变声像；以为级数越多越好；以为相位器与镶边是同一个效果。
:::

::: en
## What makes it hard

A phaser also sweeps, but it does not use a delay. It shifts phase with all-pass filters instead. The result is softer than flanging, and its notches are not spaced in a harmonic series.

## How it works

Several all-pass stages shift phase around a set of frequencies. Summing that path with the dry signal creates notches. An LFO sweeps the centre frequency, so the notches move. More stages mean more notches; feedback deepens them and adds resonant peaks. Because the spacing is uneven, a phaser lacks the metallic comb of a flanger.

## From numbers to sound

Four stages are the gentlest setting, while 8 to 12 are more obvious. A rate of 0.05 to 1 Hz suits pads, and above 2 Hz suits rhythmic material. Depth sets the sweep range, and feedback around 20 to 50 percent adds bite. An equal blend makes the notches clearest; fully wet becomes a different tone altogether.

## What the ear should catch

On an ambient pad, set the rate to 0.1 Hz and hear the notch travel from low to high like moving mist. On a jazz-funk loop, notice whether the hi-hat seems to drift as the sweep passes. Unlike a flanger, it moves wider and slower.

```audiolab
{"type": "instrument", "gm": "Pad 2 (warm)", "synth": "bowed", "phrase": ["C4", "E4", "G4", "B4", "G4", "E4"], "label": "A warm sustained pad", "label_en": "A warm sustained pad", "hint": "先听干声，再想象四级全通缓慢扫过时陷波的位置", "hint_en": "Hear it dry, then picture the notches of four all-pass stages sweeping slowly"}
```

## Easy to get wrong

That a phaser changes stereo position; that more stages are always better; that a phaser and a flanger are the same effect.
:::
