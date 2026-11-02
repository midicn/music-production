---
id: close-vs-distant-miking
site: prod
cat: A4
title: 近场与远场
title_en: Close and Distant Miking
summary: 距离改变直达声与房间声的比例，近场要细节，远场要空间
summary_en: Distance sets the ratio of direct sound to room sound. Close miking gives detail, distant miking gives space.
level: standard
tags: [录音, 摆位, 空间感]
tags_en: [recording, placement, space]
alias: [近场, 远场, 近距拾音, 远距拾音, 临界距离, close miking, distant miking]
links:
  - "[[glossary:room-treatment]]"
  - "[[glossary:reverb]]"
  - "[[instrument:classical-guitar]]"
instances:
  - atepp-003869 | 钢琴音符与踏板事件参照，不是近、远距离话筒对照 | Piano notes and pedal events, not close and distant microphone recordings
  - mutopia-001411 | 稀疏钢琴织体参照，音源尾音不等于原房间声 | Sparse piano texture; instrument decay is not the original room sound
  - m21-000602 | 合唱声部的谱面参照，不包含远距离拾音记录 | Scored choral parts without a distant-microphone recording
sources:
  - Eargle, The Microphone Book, 3rd ed., close and distant pickup chapters
  - Everest, Master Handbook of Acoustics, direct and reverberant field chapters
updated: 2026-11-02
---

::: zh
## 问题

近距离有细节，但没有空间；远距离有空间，但细节被房间盖住。录音要先决定这一段需要哪一种，而不是把所有东西都录成同一个距离。

## 信号链

话筒收到直达声与房间反射的混合。距离越近，直达声占比越高；超过临界距离，房间声开始主导。近场不是没有房间声，只是比例低。距离同时改变近讲效应与乐器的辐射角度。

## 摆位与参数

人声 15 至 25 厘米，木吉他 20 至 30 厘米，鼓皮 2 至 10 厘米。需要空间时退到 1 至 3 米，或把话筒放到房间的有利位置。用距离换混响比，不要用混响器补空间。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["A3","E4","A4","C5"],"label":"音头与尾音","label_en":"Attack and decay","hint":"这里只能比较音色包络，没有同一话筒的近、远距离录音。摆位差异需要实际录制同一乐句并匹配电平。","hint_en":"This compares timbral envelopes, not close and distant recordings with one microphone. Record the same phrase at matched level to evaluate placement."}
```

## 听什么

近场听呼吸、手指与踏板，远场听乐器整体与房间尾巴。对比同一乐句的低频厚度、瞬态边缘与声像宽度。

## 常见误解

- 近拾音仍含房间反射，比例受指向性和环境影响。
- 远拾音是否合适，取决于房间声是否值得录入。
- 卷积或算法混响可以合成早期反射，但不能自动修复录音中已经存在的梳状滤波和串音。
:::

::: en
## The problem

Close miking gives detail but little space. Distant miking gives space but lets the room cover the detail. Decide which one this passage needs instead of recording everything from the same distance.

## Signal chain

The microphone hears direct sound mixed with room reflections. The closer it is, the higher the direct share; beyond the critical distance, the room takes over. Close miking still contains room sound, just less of it. Distance also changes proximity effect and the angle at which the instrument radiates.

## Placement and settings

Place a voice 15 to 25 cm away, an acoustic guitar 20 to 30 cm away, and a drum head 2 to 10 cm away. For space, move back to 1 to 3 metres or find a favourable spot in the room. Trade distance for the reverb ratio instead of adding space with a plugin.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["A3","E4","A4","C5"],"label":"Attack and decay","label_en":"Attack and decay","hint":"This compares timbral envelopes, not close and distant recordings with one microphone. Record the same phrase at matched level to evaluate placement.","hint_en":"This compares timbral envelopes, not close and distant recordings with one microphone. Record the same phrase at matched level to evaluate placement."}
```

## What to listen for

Close up, listen for breath, fingers and pedals. Farther away, listen to the whole instrument and the room tail. Compare low-end weight, transient edge and image width on the same phrase.

## Common misconceptions

- Close microphones still capture reflections, depending on pattern and room.
- Distant placement is useful when the room contribution is useful.
- Convolution and algorithmic reverbs can create early reflections, but do not automatically repair comb filtering or spill already in the recording.
:::
