---
id: lossy-compression
site: prod
cat: B5
title: 有损压缩原理
title_en: How Lossy Compression Works
summary: 丢弃被掩蔽的成分换体积，代价藏在瞬态与高频里。
summary_en: Discarding masked content saves space, and the cost hides in transients and high frequencies.
level: standard
tags: [有损压缩, 心理声学, 码率, 预回声]
tags_en: [lossy compression, psychoacoustics, bitrate, pre-echo]
alias: [有损压缩, 心理声学编码, 预回声, lossy compression]
links:
  - "[[glossary:sample-rate]]"
  - "[[glossary:monitoring]]"
instances:
  - atepp-001868 | 亨德尔《和谐的铁匠》变奏音符密集，低码率下快速音型先糊（C1）
  - groove-000000 | 踩镲与军鼓的瞬态是编码器的难关，预回声在这里最容易听出（C1）
  - thesession-000083 | 单声部旋律线干净，编码失真没有伴奏遮掩（C1）
sources:
  - 心理声学模型与掩蔽阈值的通识；音频编码教材是主要依据。
  - Opus 与 AAC 的公开测试资料——依据来自规范与听测报告。
updated: 2026-10-28
---

::: zh
## 问题

有损编码不存全部样点，而是判断哪些成分人耳听不见，把它们用更少的比特表示。体积降下来，代价藏在瞬态与高频里。

## 原理

心理声学模型计算掩蔽阈值，响的成分会盖住邻近的弱成分，被盖住的部分可以粗量化。编码器把信号分帧做频域变换，量化系数再熵编码。码率低时量化噪声上升，瞬态前出现预回声，高频被截掉，声场变窄。联合立体声再利用左右相关压缩声像。

## 参数与做法

音乐在 256 kbps 以上通常已接近透明，语音用 64 到 96 kbps，低延迟通信用 Opus。母带与归档不要用有损格式。避免多次转码。编码前把峰值留到负 1 dBFS 左右。

## 听什么

在亨德尔《和谐的铁匠》变奏里听快速音型是否发糊，在放克鼓循环里听踩镲与军鼓的预回声，在单声部旋律里听高频沙感与尾音。编码失真在安静段与瞬态前最明显。

```audiolab
{"type":"instrument","gm":"Harpsichord","synth":"plucked","phrase":["C5","E5","G5","C6","G5","E5","C5"],"label":"密集的快速音型","label_en":"A dense fast figure","hint":"把码率压低再听，注意瞬态前是否多出一层沙","hint_en":"Drop the bitrate and listen for a layer of sand before each attack"}
```

## 常见误解

有损就一定听得出来，高码率下多数人难以分辨。码率高就一定好，编码器与素材同样重要。有损文件可以再压成无损，那只是换了容器。有损压缩不只影响高频，瞬态与声像也会受损。
:::

::: en
## The question

Lossy coding skips what the ear will not notice, spending fewer bits there. Size falls, and the cost hides in transients and highs.

## How it works

A psychoacoustic model computes masking thresholds, where loud content hides nearby quiet content, so masked parts can be coarsely quantized. The encoder frames the signal, transforms it to frequency, then quantizes and entropy-codes the coefficients. At low rates quantization noise rises, pre-echo appears before transients, highs are cut and the image narrows. Joint stereo exploits the correlation between channels.

## Settings and practice

Music is usually near-transparent above 256 kbps; speech uses 64 to 96 kbps, and Opus suits low latency. Do not use lossy formats for masters or archives, and avoid repeated transcoding. Leave peaks near minus 1 dBFS before encoding.

## What to listen for

In Handel's Harmonious Blacksmith variations, hear whether fast figures turn muddy. In a funk loop, hear pre-echo around hi-hat and snare. On a single melodic line, hear high-frequency sand and tails. Codec damage shows most in quiet passages and before attacks.

```audiolab
{"type": "instrument", "gm": "Harpsichord", "synth": "plucked", "phrase": ["C5", "E5", "G5", "C6", "G5", "E5", "C5"], "label": "A dense fast figure", "label_en": "A dense fast figure", "hint": "把码率压低再听，注意瞬态前是否多出一层沙", "hint_en": "Drop the bitrate and listen for a layer of sand before each attack"}
```

## Common misconceptions

Lossy is not always audible; at high rates most listeners cannot tell. A higher rate is not automatically better, since encoder and material matter too. A lossy file cannot be made lossless by repackaging. Nor is high frequency the only casualty, because transients and image suffer as well.
:::
