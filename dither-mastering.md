---
id: dither-mastering
site: prod
cat: A8
order: 461
title: 母带抖动
title_en: Dither in Mastering
summary: 只在最后一次降位深时加抖动，16 位交付要算清噪声整形与峰值余量。
summary_en: Add dither only at the final bit-depth reduction, and account for noise shaping and peak margin on 16-bit releases.
level: standard
tags: [母带, 抖动, 位深, 量化, 噪声整形]
tags_en: [mastering, dither, bit depth, quantization, noise shaping]
alias: [母带抖动, 降位深, 抖动噪声, dithering, dither mastering]
links:
  - "[[glossary:dither]]"
  - "[[glossary:bit-depth]]"
  - "[[glossary:noise-floor]]"
  - "[[glossary:true-peak-limiter]]"
instances:
  - giantmidi-009128 | 道兰《鲁特琴教程集》的钢琴改编音量低、织体细，16 位截断时量化台阶最容易在弱音处露出来
  - openscore-000000 | 艺术歌曲的人声与钢琴同时收弱，加不加抖动在尾音上分得开
  - atepp-000369 | 格里格《夜曲》尾音渐弱，噪声整形把噪声推向高频后，弱奏段更耐听
sources:
  - Pohlmann, Principles of Digital Audio（McGraw-Hill）— 量化、抖动与噪声整形章节。
  - Lipschitz 与 Vanderkooy 在 AES 会议上关于量化与抖动噪声的论文 — 误差去相关与噪声整形的依据。
  - ITU-R BS.1770 与 EBU R128 — 真峰值与交付余量的计量口径。
updated: 2026-10-31
---

::: zh
16 位母带在最后一次截断时，最弱的那几秒会先坏。抖动不是给整条母带加一层噪声，而是在降位深的那一刻，把跟着信号走的量化失真换成稳定的细噪。

## 什么时候才需要抖动

只在最后一次降位深时加。混音、母带处理与限制都在浮点里完成，导出 24 位时通常不必抖动，因为 24 位的噪声底已经低于大多数录音本底。真正需要的是 16 位交付：CD、部分广播与老式播放链路。若同一版还要转成有损格式，先做 16 位抖动，再编码；不要在有损编码之后补抖动。

## 误差怎么变成噪声

量化把连续幅度截到最近的格点，误差在弱音、长音与周期性强的材料上会排成有规律的形状，听感发沙。抖动在截断前加入约一个最低位的随机噪声，让误差与信号失去相关，代价是底噪略抬。噪声整形再把误差推向人耳不敏感的高频，换取中频更低的噪声。整形越重，高频噪声越多，也越容易在低码率编码与黑胶刻片时出问题。

## 参数与交付

位深决定要不要抖动，整形档位决定噪声往哪里去，真峰值余量决定编码后会不会削波。

| 交付 | 位深 | 抖动 | 整形 | 峰值余量 |
| --- | --- | --- | --- | --- |
| CD / 16 位 WAV | 16 bit | TPDF | 轻到中 | -1 dBTP |
| 流媒体母带 | 24 bit | 通常不加 | 不加 | -1 dBTP |
| 归档母带 | 24 或 32 bit 浮点 | 不加 | 不加 | 留 3 到 6 dB |
| 有损预览 | 16 bit 源 | 加一次 | 轻 | 编码前留余量 |

## 听什么

听弱奏的尾音、钢琴的余韵与混响的尾巴。抖动开与关的差别不在响处，而在最后一两秒：是稳定的细噪，还是随音高变化的沙声。下面这段钢琴用弱起与长尾，方便对照。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","G4","E4","C5"],"label":"弱奏尾音里的量化噪声","label_en":"Quantization noise in a soft tail","hint":"注意尾音是稳定的细噪，还是随音高变化的沙声","hint_en":"Listen for steady hiss versus pitch-linked grit in the tail"}
```

## 做坏的地方

在有损编码后再加抖动，只会把噪声留在已经损失过的信号上；给 24 位母带加 16 位抖动，等于白抬底噪；重整形在低码率 MP3 或黑胶上可能变成高频嘶声。若发行方要求未抖动母带，就交未抖动版，另附一份 16 位参考。抖动不能补救过载、削波或糟糕的录音，它只处理最后一次量化。
:::

::: en
A 16-bit master fails first in its quietest seconds. Dither is not a noise layer over the whole record; it is the choice made at the final truncation, trading signal-linked quantization distortion for steady, low-level hiss.

## When dither belongs

Only at the last bit-depth reduction. Mixing, mastering and limiting happen in float, and a 24-bit export usually needs no dither because its noise floor already sits below most recordings. The real case is 16-bit delivery: CD, some broadcast chains and older players. If the same version will be encoded lossily, dither to 16 bit first and encode afterwards; never add dither after the codec.

## How the error becomes audible

Quantization snaps continuous amplitude to the nearest step. On soft notes, long tones and periodic material the error lines up into a pattern and sounds gritty. Dither adds about one least significant bit of random noise before truncation so the error decorrelates from the signal, at the cost of a slightly higher floor. Noise shaping pushes that error toward high frequencies where hearing is less sensitive, buying a quieter midrange. Heavier shaping means more high-frequency noise and more trouble in low-bitrate codecs and lacquer cutting.

## Settings and delivery

Bit depth decides whether dither is needed, the shaping curve decides where the noise goes, and true-peak margin decides whether encoding clips.

| Delivery | Bit depth | Dither | Shaping | Peak margin |
| --- | --- | --- | --- | --- |
| CD / 16-bit WAV | 16 bit | TPDF | Light to medium | -1 dBTP |
| Streaming master | 24 bit | Usually none | None | -1 dBTP |
| Archive master | 24 or 32-bit float | None | None | 3 to 6 dB left |
| Lossy preview | 16-bit source | Once | Light | Margin before encoding |

## What to listen for

Hear the tail of a soft note, piano decay and reverb. The difference is not in the loud part but in the last second or two: steady hiss or pitch-linked grit. The piano figure below starts softly and leaves a long tail.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "G4", "E4", "C5"], "label": "Quantization noise in a soft tail", "label_en": "Quantization noise in a soft tail", "hint": "注意尾音是稳定的细噪，还是随音高变化的沙声", "hint_en": "Listen for steady hiss versus pitch-linked grit in the tail"}
```

## Where it goes wrong

Dither after lossy encoding only adds noise to an already damaged signal. A 16-bit dither on a 24-bit master raises the floor for nothing. Heavy shaping can turn into high-frequency hiss in low-bitrate MP3 or on vinyl. If the distributor asks for an undithered master, send that and attach a 16-bit reference. Dither cannot fix overload, clipping or a bad recording; it only handles the final quantization.
:::
