---
id: digital-audio-cables
site: prod
cat: B5
title: 数字音频线缆
title_en: Digital Audio Cables
summary: 数字线传的是码流，阻抗与长度不对时误码率上升，声音先变得不稳。
summary_en: A digital cable carries a bitstream; wrong impedance or length raises error rates and the sound turns unstable.
level: standard
tags: [数字线缆, 阻抗, AES3, ADAT]
tags_en: [digital cable, impedance, AES3, ADAT]
alias: [数字线, AES3, S/PDIF, ADAT, 同轴线]
links:
  - "[[glossary:sample-rate]]"
  - "[[glossary:bit-depth]]"
  - "[[glossary:latency]]"
instances:
  - groove-000000 | 138 BPM 放克鼓组，数字链路出错时镲片会先出现细碎的杂音（C1）
  - atepp-000122 | 德彪西练习曲的和弦，码流失步时高频会变得粗糙（C1）
  - cyberhymnal-000000 | 苏格兰诗篇的管风琴，长音最能听出数字链路是否稳定（C1）
sources:
  - AES3 与 S/PDIF 的阻抗与电平差异，依公开标准说明核对，未抄原文
  - 数字线缆长度对误码的影响，依接口厂商技术资料核对，未抄文本
updated: 2026-10-28
---

::: zh
## 问题

数字线看起来和模拟线差不多，其实是两回事。它传的是采样点组成的码流，线材阻抗不对、长度过长或接头氧化，都会让接收端认错位，严重的直接失锁，轻微的表现为偶发爆音或高频毛刺。数字不是"要么通要么不通"，它有中间状态。

## 原理

AES3 用 110 欧姆平衡线，S/PDIF 同轴用 75 欧姆，光纤用塑料或玻璃纤维。阻抗不匹配会在接头处反射，方波边沿变钝，接收端采样窗口变窄。时钟信息与音频数据在同一码流里，误码会同时影响两者。长距离传输时衰减与抖动累积，超过几十米就要考虑重新分配或改用光纤。光纤不受电磁干扰，但弯折半径太小时会漏光。

## 参数与做法

同轴用 75 欧姆视频线或专用数字线，别拿普通话筒线凑合。平衡 AES3 用 110 欧姆双绞线，接头焊点要牢。光纤接头保持清洁，弯折留出余量。线不要盘成小圈，多余长度松散盘放。数字链路先短后长地排查，换线换口是最快的定位方法。需要长距离时用分配器或网络音频协议。

## 听什么

在放克鼓组的镲片上听有没有偶发的细碎杂音，在德彪西和弦上听高频是否粗糙，在管风琴长音上听是否稳定。数字链路的问题常常是间歇性的，安静段落里反而更容易听见。

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"blown","phrase":["C3","G3","C4","E4","G4","C4","G3","C3"],"label":"管风琴长音","label_en":"A sustained organ chord","hint":"长音里任何一次码流失步都会留下短暂的毛刺","hint_en":"Any dropped frame leaves a brief rasp inside a sustained chord"}
```
:::

::: en
## The problem

A digital cable looks much like an analogue one, but it does a different job. It carries a bitstream of sample points, and wrong impedance, excessive length or oxidised connectors can make the receiver misread positions, losing lock outright or producing occasional clicks and high-frequency grit. Digital is not simply working or broken; it has in-between states.

## How it works

AES3 runs on 110-ohm balanced cable, coaxial S/PDIF on 75 ohm, and optical links on plastic or glass fibre. Impedance mismatches reflect at connectors, blunting square-wave edges and narrowing the receiver's sampling window. Clock and audio data share the same stream, so errors hit both. Over distance, attenuation and jitter accumulate, and runs beyond a few tens of metres call for redistribution or fibre. Fibre ignores electromagnetic interference but leaks light if bent too tightly.

## Settings and practice

Use 75-ohm video or dedicated digital cable for coax rather than microphone cable. Use 110-ohm twisted pair for balanced AES3 and keep solder joints solid. Keep optical connectors clean and leave slack at bends. Do not coil cable into tight loops; coil surplus loosely. Troubleshoot a digital chain from the shortest link outward, swapping cable and port first. For long runs, use a distribution amplifier or a networked audio protocol.

## What to listen for

On the funk kit cymbals, listen for occasional fine-grained noise; on the Debussy chords, for roughness in the top; on the organ, for steadiness in long notes. Digital faults are often intermittent and easier to hear in quiet passages.

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"blown","phrase":["C3","G3","C4","E4","G4","C4","G3","C3"],"label":"A sustained organ chord","label_en":"A sustained organ chord","hint":"Any dropped frame leaves a brief rasp inside a sustained chord","hint_en":"Any dropped frame leaves a brief rasp inside a sustained chord"}
```
:::
