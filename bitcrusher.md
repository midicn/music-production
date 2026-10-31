---
id: bitcrusher
site: prod
cat: A7
title: 比特压碎
title_en: Bitcrushing
summary: 降位深与降采样率是两件事，一个给颗粒，一个给镜像。
summary_en: Lowering bit depth and sample rate are two different moves, one adds grain, the other aliases.
level: standard
tags: [效果器, 低保真, 量化, 混叠]
tags_en: [effects, lo-fi, quantization, aliasing]
alias: [比特压碎, 位深压缩, 降采样, 比特粉碎, bitcrusher, bit crush]
links:
  - "[[glossary:bit-depth]]"
  - "[[glossary:harmonics]]"
  - "[[instrument:software-synth]]"
instances:
  - oga-000013 | 复古头目战的主旋律是方波，降位深后弱奏会先变成沙粒
  - oga-000014 | 8-bit 编曲的鼓点短促，降采样率的镜像在高频最明显
  - oga-000015 | 同类 8-bit 战斗曲的贝斯线低而连续，适合听量化台阶
sources:
  - Curtis Roads, The Computer Music Tutorial, quantization sections.
  - Udo Zölzer, DAFX.
updated: 2026-10-28
---

::: zh
## 为什么会用到它

比特压碎同时降低位深与采样率，制造粗颗粒和镜像频率。它听起来像旧游戏机，但两件事的作用并不相同。

## 它怎么工作

位深决定量化台阶，8 bit 的理论信噪比约 48 dB，低电平细节会落进台阶里。降低采样率让高于新奈奎斯特频率的成分折返，形成镜像；采样保持还让波形变成阶梯。位深降低带来的是颗粒噪声，采样率降低带来的是金属味和混叠。先抗混叠再降采样，声音会干净一些；直接降采样，镜像会留在高频。

## 旋钮与耳朵

bits 从 16 降到 8 已经很明显，4 bit 以下适合特殊音效；sample rate 从 44.1 kHz 降到 8 kHz 会切掉空气感并带回镜像。mix 控制并行量，放在鼓组上 20–30% 就能听出颗粒。

## 耳朵要抓的点

在 8-bit 风格的战斗曲上听主旋律的方波边缘，降低 bits 后注意弱奏是否变成沙粒。再把采样率降到 8 kHz，听高频镜像如何让镲片变成金属屑。换到干净钢琴，同样的设置会暴露尾音被量化台阶切碎。

```audiolab
{"type":"instrument","gm":"Lead 1 (square)","synth":"reed","phrase":["C4","E4","G4","C5","G4","E4"],"label":"方波主旋律","label_en":"A square-wave lead","hint":"先听干净的方波，再想象 8 bit 与 8 kHz 各自留下的痕迹","hint_en":"Hear the clean square, then what 8 bit and 8 kHz each leave behind"}
```

## 容易弄错的

以为比特压碎等于全部 lo-fi；以为降位深与降采样率是一回事；以为加上去就会自动复古。
:::

::: en
## Why reach for it

A bitcrusher lowers both bit depth and sample rate, producing coarse grain and mirror frequencies. It sounds like an old game console, but the two moves do different things.

## How it works

Bit depth sets the quantization step size. At 8 bit the theoretical signal-to-noise ratio is about 48 dB, so quiet detail falls between steps. Lowering the sample rate folds content above Nyquist back as images, and sample-and-hold turns the waveform into stairs. Fewer bits give granular noise; a lower rate gives a metallic edge and aliasing. Anti-alias before decimating for a cleaner result; direct decimation leaves images in the high end.

## Knobs and ears

Dropping bits from 16 to 8 is obvious, and below 4 bit suits effects. Dropping the rate from 44.1 kHz to 8 kHz removes air and brings images back. Mix sets the parallel amount; on drums, 20 to 30 percent reveals the grain.

## What the ear should catch

On an 8-bit battle cue, listen to the square lead, lower the bits and hear quiet notes turn sandy. At 8 kHz, hear cymbals turn into metal filings. On a clean piano, the same setting chops the decay into steps.

```audiolab
{"type": "instrument", "gm": "Lead 1 (square)", "synth": "reed", "phrase": ["C4", "E4", "G4", "C5", "G4", "E4"], "label": "A square-wave lead", "label_en": "A square-wave lead", "hint": "先听干净的方波，再想象 8 bit 与 8 kHz 各自留下的痕迹", "hint_en": "Hear the clean square, then what 8 bit and 8 kHz each leave behind"}
```

## Easy to get wrong

That bitcrushing accounts for all lo-fi; that lowering bit depth and lowering sample rate are the same; that adding it automatically sounds retro.
:::
