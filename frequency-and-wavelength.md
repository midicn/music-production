---
id: frequency-and-wavelength
site: prod
cat: A5
title: 频率与波长
title_en: Frequency and Wavelength
summary: 频率决定音高，波长决定它与房间和话筒怎样相互作用。
summary_en: Frequency sets pitch, wavelength sets how sound meets rooms, obstacles and absorbers.
level: standard
tags: [频率, 波长, 声速, 绕射, 低频]
tags_en: [frequency, wavelength, speed of sound, diffraction, low end]
alias: [波长, 频率, 声速, frequency, wavelength, speed of sound]
links:
  - "[[glossary:room-mode]]"
  - "[[glossary:absorption]]"
  - "[[instrument:cello]]"
instances:
  - pdmx-000801 | 低音提琴协奏曲的钢琴改编，低音区持续音适合听波长与房间的相互作用（C1）
  - giantmidi-000171 | 管风琴前奏曲的钢琴改编，高低声部同时发声，便于对比两端的方向感（C1）
  - atepp-000011 | 斯克里亚宾练习曲，钢琴全音域，用来听高频随位置变化（C1）
sources:
  - Everest, F. Alton，Master Handbook of Acoustics（McGraw-Hill）— 波长、绕射与吸声章节核对，未引用
  - Toole, Floyd，Sound Reproduction（Focal Press）— 房间与听觉章节核对，未引用
updated: 2026-10-28
---

::: zh
## 问题
低频穿墙、绕角，高频一转身就暗，这些现象常被当成「低频更有力」。真正决定它们的是频率对应的波长，以及波长与障碍物、房间尺寸的比例。

## 物理或房间
波长等于声速除以频率。20 °C 空气中，20 Hz 约 17 米，100 Hz 约 3.4 米，1 kHz 约 34 厘米，10 kHz 只有 3.4 厘米。障碍物接近或小于波长时，声波绕过去；远大于波长时被反射。房间边长也按这个尺度与低频作用。

## 做法与判断
先算三个数：房间最长边、监听距离、要处理的频段。吸音层厚度要与四分之一波长相比，薄棉对 100 Hz 基本无效；低频要利用墙角。摆位时让音箱与墙的距离避开设定的抵消频率，再用测量确认，而不是堆材料。

## 听什么
播一段 20 Hz 到 20 kHz 的扫频，注意哪几个低音突然变响、哪几个消失。站在房间不同位置重复，高频会随头部移动明显变化，低频更稳定。听军鼓与铙钹，判断高频是直达还是被空气吃掉。

## 常见误解
波长对应同相位点之间的间隔，对正弦波就是相邻波峰的距离。高频并不传得更远，空气吸收反而让它衰减更快。低频全向只在声源尺寸远小于波长时成立，大房间与大音箱并不一样。

```audiolab
{"type":"instrument","gm":"Cello","synth":"bowed","phrase":["C2","C3","C4","C5"],"label":"同一把弓，跨四个八度","label_en":"One bow, four octaves","hint":"低音更松、更绕；高音更紧、更指向。不要只比较音量，听余响与方向感。","hint_en":"The low notes are looser and less directional; the high notes are tighter and more focused. Listen past level to the tail and direction."}
```
:::

::: en
## The problem
Bass passes through walls and bends around corners; treble dulls when you turn your head. The cause is wavelength, not power.

## Physics or room
Wavelength is sound speed divided by frequency. At 20 °C, 20 Hz spans 17 m, 100 Hz 3.4 m, 1 kHz 34 cm and 10 kHz 3.4 cm. Sound bends around objects near its wavelength and reflects from much larger ones; rooms interact with bass on the same scale.

## Practice and judgement
Work out the longest room dimension, listening distance and target band. Absorber thickness is judged against a quarter wavelength, so thin foam does little at 100 Hz. Avoid predicted cancellations when placing speakers, then measure.

## What to listen for
Sweep 20 Hz to 20 kHz and note which bass notes swell or vanish. Repeat at different positions; treble changes as you move, bass less so. On snare and cymbals, hear whether the top arrives directly or is lost to air.

## Common misunderstandings
Wavelength is the spacing between points of the same phase, not successive peaks. Treble fades faster through air, not farther. Bass is omnidirectional only when the source is small against the wavelength.

```audiolab
{"type":"instrument","gm":"Cello","synth":"bowed","phrase":["C2","C3","C4","C5"],"label":"One bow, four octaves","label_en":"One bow, four octaves","hint":"The low notes are looser and less directional; the high notes are tighter and more focused. Listen past level to the tail and direction.","hint_en":"The low notes are looser and less directional; the high notes are tighter and more focused. Listen past level to the tail and direction."}
```
:::
