---
id: polar-patterns
site: prod
cat: A4
title: 指向性
title_en: Polar Patterns
summary: 指向性决定话筒对哪个方向敏感，也决定近讲效应与串音
summary_en: A microphone's polar pattern sets what it hears from each direction, and with it bleed and proximity effect.
level: standard
tags: [录音, 话筒, 指向性]
tags_en: [recording, microphone, polar pattern]
alias: [指向性, 拾音模式, 心形, 全指向, 8字形, polar pattern, cardioid]
links:
  - "[[glossary:polar-pattern]]"
  - "[[glossary:microphone]]"
  - "[[instrument:drum-kit]]"
instances:
  - m21-000602 | 合唱织体宽，适合用全指向收取房间与整体
  - openscore-000008 | 单个男声靠近讲话时，心形的低频抬升最容易听出
  - groove-000003 | 鼓组串音多，适合检查心形后方零点是否安静
sources:
  - Eargle, The Microphone Book, 3rd ed., directivity and proximity chapters
  - Olson, Acoustical Engineering, pressure-gradient microphone theory
updated: 2026-10-28
---

::: zh
## 问题

话筒对正前方最敏感，对侧面和后方也有不同程度的响应。这个方向图决定了串音、近讲效应与房间声的比例。摆位之前先想清楚要收什么、要躲什么。

## 信号链

心形指向用单振膜加后方声学延迟，后方形成零点。全指向没有近讲效应，低频更平直。8 字形两侧反相，正后方也是零点，适合两人对唱或侧向隔离。可切换指向的话筒用双振膜，改变两面的极化比例。

## 摆位与参数

心形主轴对准声源，歌手距离 15 至 25 厘米；太近会因近讲效应让低频膨胀。全指向适合合唱与房间声，放在 1 米外。8 字形让声源落在两瓣之一，把另一瓣对准需要隔离的方向。

```audiolab
{"type":"instrument","drum":"38","synth":"perc","phrase":["38","42","36"],"label":"军鼓与底鼓的方向感","label_en":"Snare and kick, heard off-axis","hint":"先听合成近似，再听 GM 打击采样","hint_en":"Compare the synthetic approximation with the GM drum sample"}
```

## 听什么

绕话筒走一圈拍手，听音量与音色如何变化；再靠近说话，听低频是否变厚。把心形转到 180 度，确认零点是否真的安静。

## 常见误解

- **心形能完全隔离后方** → 低频会绕射，后方仍有声音。
- **全指向没有近讲效应** → 确实没有，所以低频更可控。
- **指向性只影响音量** → 离轴频响也会改变音色。
:::

::: en
## The problem

A microphone is most sensitive in front but still hears the sides and rear. That pattern sets bleed, proximity effect and room in the capture. Before placing it, decide what to pick up and what to avoid.

## Signal chain

A cardioid uses one diaphragm and an acoustic delay at the rear, creating a null behind. An omnidirectional capsule has no proximity effect and a flatter low end. A figure-eight is out of phase on the two sides and also null at the rear; it suits two singers facing each other or side isolation. A switchable pattern uses two diaphragms and changes their polarisation.

## Placement and settings

Aim the cardioid axis at the source, with a singer 15 to 25 cm away; closer than that, proximity effect inflates the low end. Use omni for a choir or room sound at one metre. With figure-eight, put the source in one lobe and aim the other at what you want to reject.

```audiolab
{"type": "instrument", "drum": "38", "synth": "perc", "phrase": ["38", "42", "36"], "label": "Snare and kick, heard off-axis", "label_en": "Snare and kick, heard off-axis", "hint": "先听合成近似，再听 GM 打击采样", "hint_en": "Compare the synthetic approximation with the GM drum sample"}
```

## What to listen for

Walk a full circle around the microphone while clapping, and hear how level and tone change. Move in close and speak, listening for a thicker low end. Turn the cardioid to 180 degrees and check that the null is quiet.

## Common misconceptions

- **Cardioid rejects everything behind it** → low frequencies diffract around the body, so the rear is not silent.
- **Omni has no proximity effect** → correct, which makes its low end easier to control.
- **Pattern only changes level** → off-axis response changes tone as well.
:::
