---
id: audio-interface
site: prod
cat: B5
title: 音频接口
title_en: Audio Interface
summary: 接口决定几路进出、多低延迟、转换够不够稳，话筒前级别忘了算。
summary_en: The interface sets how many channels you get, how low latency goes and how stable conversion is; don't forget preamp gain.
level: standard
tags: [音频接口, 声卡, 话放, 驱动]
tags_en: [audio interface, sound card, preamp, driver]
alias: [声卡, 音频接口, 录音接口, audio interface]
links:
  - "[[glossary:latency]]"
  - "[[glossary:monitoring]]"
  - "[[glossary:daw]]"
instances:
  - musicnet-000067 | 贝多芬第十五弦乐四重奏，四件乐器分轨录制时要算清输入通道与话筒数量（C1）
  - groove-000002 | 86 BPM 灵魂乐鼓组，边录边监听时接口延迟决定鼓手跟不跟得上（C1）
  - thesession-015842 | 爱尔兰传统曲调，单支话筒或线路输入就能录，通道数不是越多越好（C1）
sources:
  - 接口的通道、话放与监听通路，依厂商公开规格核对，未抄文本
  - 缓冲与延迟的换算关系，依数字音频通识核对，未抄原文
updated: 2026-10-28
---

::: zh
## 问题

接口是电脑与声音世界之间的门。它要解决四件事：把话筒信号放大到可用电平、把模拟信号转成数字、把数字信号送回去变成声音、让这一切在演奏者察觉不到的延迟内完成。买错接口，通常是通道不够、话放太弱或驱动不稳，而不是参数表不好看。

## 原理

话筒输出是毫伏级信号，需要话放放大几十 dB 才到转换器的合适区间。转换器前面有抗混叠滤波，后面有重建滤波。接口与电脑之间走 USB、雷电或 PCIe，驱动决定缓冲大小与延迟。直接监听把输入信号在接口内部直接送到输出，绕开电脑，延迟接近零但听不到插件效果。回环通道把输出再送回输入，用于录制系统声音或直播。

## 参数与做法

先数同时要用的输入：录鼓至少八路，录人声一两路就够。看话放增益范围与是否带幻象电源，电容话筒需要 48 V。看有没有独立音量旋钮的直接监听。确认驱动在所用系统上长期稳定，这比多两个通道重要。笔记本供电时注意 USB 总线电流是否够。留出扩展余地，但不必为想象中的需求买单。

## 听什么

在四重奏分轨里听四件乐器是否都干净、有没有串音，在灵魂乐鼓组里边打边听延迟是否跟手，在单支话筒的传统曲调里听话放噪声是否可闻。接口本身不改音色，但话放与转换的余量会决定录音能不能推到该有的响度。

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (nylon)","synth":"plucked","phrase":["D4","F#4","A4","D5","A4","F#4","D4","A3"],"label":"线路输入的木吉他","label_en":"A guitar on a line input","hint":"这类信号不需要话放放大，听它进接口后是否仍然干净","hint_en":"This needs no preamp gain; listen for whether it stays clean through the interface"}
```
:::

::: en
## The problem

The interface is the door between the computer and the sonic world. It has four jobs: raise microphone levels to something usable, turn analogue into digital, turn digital back into sound, and do all of it inside a delay the player cannot feel. Buying the wrong one usually means too few channels, a weak preamp or an unstable driver, not an ugly spec sheet.

## How it works

A microphone puts out millivolts, so a preamp adds tens of dB before the converter sees a sensible level. The converter has an anti-aliasing filter in front and a reconstruction filter behind. The box talks to the computer over USB, Thunderbolt or PCIe, and the driver sets buffer size and latency. Direct monitoring sends the input straight to an output inside the interface, bypassing the computer, so latency is near zero but plug-ins are not heard. A loopback channel returns the output to an input for capturing system audio or streaming.

## Settings and practice

Count the inputs you will use at once: eight or more for a drum kit, one or two for a voice. Check preamp gain range and phantom power, since condenser microphones need 48 V. Look for an independent direct-monitor level. Confirm the driver is stable on your platform over the long run, which matters more than two extra channels. On a laptop, check that the USB bus can supply enough current. Leave room to grow, but do not pay for imagined needs.

## What to listen for

On the quartet tracks, listen for clean separation and crosstalk between instruments; on the soul kit, for whether playing along feels immediate; on the single-mic traditional tune, for audible preamp noise. The interface does not colour the sound by itself, but preamp and converter headroom decide how loud the recording can later go.

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (nylon)","synth":"plucked","phrase":["D4","F#4","A4","D5","A4","F#4","D4","A3"],"label":"A guitar on a line input","label_en":"A guitar on a line input","hint":"This needs no preamp gain; listen for whether it stays clean through the interface","hint_en":"This needs no preamp gain; listen for whether it stays clean through the interface"}
```
:::
