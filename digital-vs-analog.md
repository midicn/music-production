---
id: digital-vs-analog
site: prod
cat: A4
title: 数字与模拟
title_en: Digital and Analogue
summary: 模拟加噪声与饱和，数字加量化与时钟误差，差别在方式
summary_en: Analogue adds noise and saturation, digital adds quantisation and clock error. The method differs.
level: standard
tags: [录音, 模拟, 数字]
tags_en: [recording, analogue, digital]
alias: [模拟录音, 数字录音, 模拟与数字, analog vs digital, analogue, digital]
links:
  - "[[glossary:bit-depth]]"
  - "[[glossary:dither]]"
  - "[[period:contemporary]]"
instances:
  - mutopia-000180 | 十二分钟的连续长音，模拟介质会随时间长出嘶声
  - atepp-005000 | 变奏尾段的极弱长音，最考验两种介质的底噪
  - cyberhymnal-001740 | 持续和弦没有打击瞬态，差别只剩底噪与高频
sources:
  - Watkinson, The Art of Digital Audio, conversion and storage chapters
  - AES Convention paper on tape saturation and digital capture
updated: 2026-10-28
---

::: zh
## 问题

模拟录音把声音存成磁带的磁化强度，数字录音把它存成一串采样值。两者都会改变声音，只是改变的方式不同：一边加噪声与饱和，另一边加量化与时钟误差。

## 信号链

模拟链是话筒、话放、磁带机；数字链把磁带机换成转换器与文件。磁带会压缩瞬态、随时间长出嘶声，每复制一次再糊一点；数字复制在逐位相同的意义上不损失。

## 摆位与参数

模拟段把峰值压在饱和点以下 3 至 6 dB，数字段峰值落在 -12 至 -6 dBFS。用 24 位采集，把余量留给弱奏，不要靠推子补。想要模拟染色时，先在数字域录干净，再单独过一道磁带。

```audiolab
{"type":"instrument","gm":"Cello","synth":"bowed","phrase":["C3","G3","C4"],"label":"持续音背后的安静","label_en":"The silence behind sustained notes","hint":"听长音之间有多干净，再想磁带会在这里长出什么","hint_en":"Hear how clean the gaps are, then imagine what tape would grow there"}
```

## 听什么

对比同一次演奏的两种记录：模拟版的弱奏尾音背后有嘶声，数字版是均匀的安静。再听瞬态，模拟常把鼓点削圆一点，数字保留原来的尖。

## 常见误解

- **数字就是原声** → 采样与量化同样是一种改写。
- **模拟一定更暖** → 暖来自饱和与高频损失，不是介质本身。
- **位深越高越像模拟** → 位深只决定噪声底。
:::

::: en
## The problem

Analogue recording stores sound as magnetisation on tape; digital recording stores it as a stream of samples. Both change the sound, each in its own way: one adds noise and saturation, the other quantisation and clock error.

## Signal chain

The analogue chain is microphone, preamp, tape machine. The digital chain replaces the tape machine with a converter and a file. Tape compresses transients, grows hiss over time and blurs with every copy; a digital copy stays bit-for-bit identical.

## Placement and settings

Keep analogue peaks 3 to 6 dB below the saturation point, and digital peaks between -12 and -6 dBFS. Record at 24 bits and leave headroom for the soft passages instead of fixing them with a fader. If you want tape colour, record clean digitally first and pass the signal through tape afterwards.

```audiolab
{"type": "instrument", "gm": "Cello", "synth": "bowed", "phrase": ["C3", "G3", "C4"], "label": "The silence behind sustained notes", "label_en": "The silence behind sustained notes", "hint": "听长音之间有多干净，再想磁带会在这里长出什么", "hint_en": "Hear how clean the gaps are, then imagine what tape would grow there"}
```

## What to listen for

Compare two recordings of one performance: behind the soft tails, the analogue version has hiss, the digital one has even silence. Listen to transients too; tape rounds the drum attack slightly, while digital keeps the original edge.

## Common misconceptions

- **Digital is the original sound** → sampling and quantisation are a rewrite as well.
- **Analogue is always warmer** → warmth comes from saturation and high-frequency loss, not the medium.
- **More bits sound more analogue** → bit depth only sets the noise floor.
:::
