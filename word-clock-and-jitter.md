---
id: word-clock-and-jitter
site: prod
cat: B5
title: 字时钟与抖动
title_en: Word Clock and Jitter
summary: 数字设备共享一个时钟，抖动让采样点前后挪，高频先变刺。
summary_en: Digital boxes share one clock, and jitter nudges sample points in time until the top end turns harsh.
level: standard
tags: [字时钟, 抖动, 同步, 转换器]
tags_en: [word clock, jitter, synchronisation, converter]
alias: [字时钟, 时钟同步, 抖动, word clock, jitter]
links:
  - "[[glossary:sample-rate]]"
  - "[[glossary:latency]]"
  - "[[glossary:monitoring]]"
instances:
  - groove-000001 | 105 BPM 放克鼓组，踩镲的金属尾音最能暴露时钟抖动（C1）
  - atepp-000121 | 德彪西练习曲，弱奏的高音区在抖动下会失去稳定的位置感（C1）
  - cyberhymnal-008314 | 管风琴赞美诗，多路话筒合轨时时钟不齐会让声像变虚（C1）
sources:
  - 时钟分配与抖动对转换的影响，参考音频接口厂商技术文档。
  - AES11 数字音频参考时钟的用途；公开标准说明是主要依据。
updated: 2026-10-28
---

::: zh
## 卡住的地方

两台以上数字设备连在一起，就必须商量谁定节拍。各自用自己的晶振，采样点会一点点错开，合起来声音发虚；如果时钟本身不稳，采样点在时间上前后抖，转换时就多出不该有的边带。

## 原理

采样是等间隔取点，间隔由时钟决定。时钟抖动指相邻采样点的时间偏差，几十皮秒到几纳秒不等。转换器在重建波形时把时间误差折算成幅度误差，频率越高误差越大，所以高频最先变刺。多设备系统中，从设备要用锁相环跟踪主时钟，锁相环的带宽决定它滤掉多少抖动、又跟随多少漂移。字时钟用 BNC 线传方波，AES11 规定了参考时钟的规范。S/PDIF 与 ADAT 的光纤信号里也带时钟，但用专门的时钟线通常更稳。

## 参数与做法

一台设备当主时钟，其余全部跟随它，不要互相跟。BNC 线用 75 欧姆规格，分支分配比菊花链稳。接长线时注意终端匹配。USB 与雷电接口的时钟由主机或接口内部产生，多接口并联时要确认谁在主导。把转换器放在主时钟一侧，别让便宜的声卡决定全系统的时基。怀疑抖动时，先换一根线、换一个主时钟，再怀疑设备。

## 耳朵要抓的点

在放克鼓组的踩镲上听金属尾音是否发干、发刺，在德彪西的弱奏高音上听音头是否稳定，在管风琴合轨时听声像是否聚得拢。抖动带来的变化通常很轻微，但当多轨叠加时会开始显得不干净。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":105,"label":"等间隔的十六分音符","label_en":"Even sixteenths","hint":"每一格都是等长的，时钟抖动就是让这些间隔忽长忽短","hint_en":"Every step should be equal; clock jitter makes those gaps wobble"}
```
:::

::: en
## Where it snags

Once two or more digital devices are wired together, they have to agree on who keeps time. If each runs on its own crystal, sample points drift apart and the combined sound blurs. If the clock itself is unstable, sample points shift back and forth in time during conversion and produce sidebands that should not exist.

## Principle

Sampling takes points at equal intervals set by the clock. Jitter is the timing error between neighbouring sample points, from tens of picoseconds to a few nanoseconds. A converter turns timing error into amplitude error while rebuilding the waveform, and the error grows with frequency, so the top end suffers first. In a multi-device system the slave tracks the master through a phase-locked loop whose bandwidth decides how much jitter it filters and how much drift it follows. Word clock travels as a square wave over BNC cable, and AES11 defines the reference-clock specification. S/PDIF and ADAT carry clock inside their optical signals, but a dedicated clock line is usually steadier.

## Settings and practice

Pick one master clock and have everything else follow it, never the reverse. Use 75-ohm BNC cable, and prefer a distribution amplifier over daisy-chaining. Watch termination on long runs. USB and Thunderbolt interfaces generate clock internally or from the host, so confirm who leads when several are patched together. Put the converter on the master side rather than letting the cheapest box set the system timebase. When jitter is suspected, swap the cable and the master before blaming a device.

## What the ear catches

On the funk kit, listen for a dry, brittle edge on the hi-hat tail; on the Debussy étude, for a shaky attack in quiet high notes; on the combined organ tracks, for an image that will not settle. Jitter is usually subtle, but it starts to sound unclean as tracks stack up.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":105,"label":"Even sixteenths","label_en":"Even sixteenths","hint":"Every step should be equal; clock jitter makes those gaps wobble","hint_en":"Every step should be equal; clock jitter makes those gaps wobble"}
```
:::
