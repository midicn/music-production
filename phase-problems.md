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
  - groove-000010 | 可渲染鼓组，再用同一录音的延迟副本检查音头与求和变化 | Render the kit, then compare attacks and summation using a delayed copy of the same recording
  - atepp-003869 | 可渲染持续钢琴音，在 DAW 里制作等增益延迟副本，检查梳状滤波 | Render sustained piano and create an equal-gain delayed copy in a DAW to inspect comb filtering
  - musicnet-000067 | 可将四重奏渲染为音频，检查声部独奏与合奏，勿把配器差异当话筒相位证据 | Render the quartet to compare isolated and combined parts; orchestration differences do not establish mic phase
sources:
  - "https://www.shure.com/en-US/docs/education/Microphone-Techniques-for-Recording"
  - AES Convention paper on comb filtering and microphone arrays
  - Eargle, The Microphone Book, 3rd ed., multi-microphone phase chapters
updated: 2026-11-02
---

::: zh
## 问题

同一声源的相关信号从两支话筒相加时，时间、幅度和频响差异可能造成梳状滤波。表现可以是音色变薄，也可能是局部增强；结果取决于距离、声源带宽和两路电平。先比较单路与合成，再判断是否需要处理。

## 信号链

相关信号以不同时间或不同滤波响应相加，可能产生频率相关的增强与抵消。极性反转把整个波形乘以−1；纯延迟的相位变化则随频率而变。对单一正弦，两者在某个频率可能恰好相当，但不能因此把宽带信号的极性当成一段固定延迟。

## 摆位与参数

三比一是降低多话筒串音相加影响的经验规则：话筒间距约为话筒到各自目标声源距离的三倍或更多，并非“第二支离同一声源三倍远”。它不是立体声主阵列或近远话筒的普遍几何要求。先听目标声与串音比例，再比较极性、摆位和必要的延迟；保留未移位版本，避免破坏需要的空间关系。

```audiolab
{"type":"instrument","drum":"36","synth":"perc","phrase":["36","38","42"],"label":"用于制作延迟对照的鼓点","label_en":"Drum hits for a delay comparison","hint":"本按钮切换合成与采样音色；要比较相位，请在 DAW 复制同一录音，给一路加延迟后单声道求和。","hint_en":"This button changes synthetic and sampled timbres. For phase comparison, duplicate one recording in a DAW, delay one copy and sum to mono."}
```

## 听什么

把两支话筒合到单声道，听低频与中频是否变薄；移动一支话筒几厘米，听音色是否突然变空。也可以只在一支话筒上做极性反转，比较两种叠加结果。

## 常见误解

- 极性反转和时间移动是不同操作
- 一个频段改善不代表所有频段都改善
- 同一声源的多个拾音点不必全部对齐到同一波峰
- 最终按完整混音、单声道兼容与所需空间感判断
:::

::: en
## The problem

Summing related signals from two microphones can create comb filtering through differences in timing, amplitude and response. The result may be thinning or reinforcement in some bands, depending on distance, source bandwidth and relative level. Compare each mic with the sum before deciding what needs correction.

## Signal chain

Related signals combined with different delays or filtering can reinforce and cancel by frequency. Polarity inversion multiplies the waveform by −1; a pure delay produces frequency-dependent phase. They can coincide for one sine at one frequency without making polarity inversion equivalent to a fixed delay on broadband sound.

## Placement and settings

The 3:1 guideline reduces the summed impact of spill: spacing between microphones is roughly three times or more their distance to their respective intended sources. It does not mean placing a second mic three times farther from one source, nor is it universal geometry for stereo or close/room arrays. Check wanted/spill balance, polarity, placement and any necessary delay, retaining an unshifted version.

```audiolab
{"type":"instrument","drum":"36","synth":"perc","phrase":["36","38","42"],"label":"Drum hits for a delay comparison","label_en":"Drum hits for a delay comparison","hint":"This button changes synthetic and sampled timbres. For phase comparison, duplicate one recording in a DAW, delay one copy and sum to mono.","hint_en":"This button changes synthetic and sampled timbres. For phase comparison, duplicate one recording in a DAW, delay one copy and sum to mono."}
```

## What to listen for

Sum the two microphones to mono and hear whether the lows and low mids thin out. Move one microphone a few centimetres and listen for a sudden hollow tone. You can also invert polarity on one microphone and compare the two sums.

## Common misconceptions

- Polarity inversion and time shifting are different operations
- Improvement in one band does not prove improvement everywhere
- Multiple captures of one source need not all align to one peak
- Judge the full mix, mono compatibility and intended space
:::
