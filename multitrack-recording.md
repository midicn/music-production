---
id: multitrack-recording
site: prod
cat: A4
title: 多轨录音
title_en: Multitrack Recording
summary: 分轨录音把乐队拆成可独立调整的轨道，隔离与余量比轨数更重要
summary_en: Multitrack recording gives every sound its own track. Isolation and headroom matter more than track count.
level: standard
tags: [录音, 多轨, 工作流]
tags_en: [recording, multitrack, workflow]
alias: [多轨录音, 分轨录音, 叠录, 多轨, multitrack, tracking]
links:
  - "[[glossary:gain-staging]]"
  - "[[glossary:headroom]]"
  - "[[instrument:drum-kit]]"
instances:
  - mutopia-000497 | 管弦乐声部多，适合对照分轨后的层次与掩蔽
  - groove-000010 | 鼓组节奏骨架，适合作为分轨录音的第一层
  - musicnet-000067 | 四重奏声部独立，适合听单轨串音与合奏平衡
sources:
  - Bartlett, Practical Recording Techniques, multitrack and overdub chapters
  - Ballou, Handbook for Sound Engineers, 5th ed., tracking and monitoring chapters
updated: 2026-10-28
---

::: zh
## 问题

分轨录音不是把乐队拆散，而是把每个声音放进独立轨道，让后期还能改。轨数多不等于好录，隔离与余量才是关键。录之前先想清楚哪些声音必须分开。

## 信号链

每支话筒 → 话放 → 转换器 → 独立轨道。监听混音与录音链分开，所有设备共用同一时钟。先录节奏骨架，再叠加和声与主唱，最后补细节。叠录时保留原始 take，不要覆盖。

## 摆位与参数

每轨峰值控制在 -12 至 -6 dBFS，给后期留 3 dB 余量。耳机混音里加一点混响，让乐手有空间感。串音大的乐器分开录，或用指向性更窄的话筒。需要同步时先确认时钟与延迟补偿。

```audiolab
{"type":"instrument","drum":"38","synth":"perc","phrase":["36","38","42","38"],"label":"先录节奏骨架","label_en":"Lay the rhythmic foundation first","hint":"先听合成近似，再听 GM 打击采样，注意每一下的间隔","hint_en":"Compare synth and GM drum sample, listening to the spacing of the hits"}
```

## 听什么

单轨回放听串音与底噪，合起来听低频是否打架、节奏是否松。叠录后再听一次整体，确认没有为了对齐牺牲律动。

## 常见误解

- **轨数越多越好** → 轨数增加的是选择，不是质量。
- **叠录必须完全对齐** → 过度对齐会让节奏失去呼吸。
- **耳机混音就是成品** → 它只服务于演奏，不等于混音结果。
:::

::: en
## The problem

Multitrack recording does not break up the band. It gives each sound its own track so the mix can still change later. More tracks do not make a better recording; isolation and headroom do. Decide before the session which sounds must stay separate.

## Signal chain

Each microphone → preamp → converter → its own track. Keep the monitor mix separate from the recording chain, and clock every device from one source. Record the rhythmic foundation first, then add harmony and lead vocals, then details. Keep the original take when overdubbing rather than recording over it.

## Placement and settings

Keep each track peaking between -12 and -6 dBFS, leaving 3 dB for later. Add a little reverb to the headphone mix so players hear space. Record loud, leaky instruments separately or use a narrower pattern. When synchronising, confirm clocking and delay compensation first.

```audiolab
{"type": "instrument", "drum": "38", "synth": "perc", "phrase": ["36", "38", "42", "38"], "label": "Lay the rhythmic foundation first", "label_en": "Lay the rhythmic foundation first", "hint": "先听合成近似，再听 GM 打击采样，注意每一下的间隔", "hint_en": "Compare synth and GM drum sample, listening to the spacing of the hits"}
```

## What to listen for

Solo a track for bleed and noise, then hear the whole thing for low-end collisions and a loose pulse. After overdubbing, listen again and check that alignment has not cost you the groove.

## Common misconceptions

- **More tracks are always better** → tracks add options, not quality.
- **Overdubs must line up perfectly** → over-alignment removes the breath from a rhythm.
- **The headphone mix is the finished mix** → it serves the performance, not the final result.
:::
