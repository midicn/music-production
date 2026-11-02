---
id: bit-depth-and-quantization-noise
site: prod
cat: B4
title: 位深与量化噪声
title_en: Bit Depth and Quantization Noise
summary: 位深决定最轻的声音能否留下，量化噪声是它的代价。
summary_en: Bit depth decides whether the quietest detail survives, and quantization noise is the price.
level: standard
tags: [位深, 量化噪声, 数字音频]
tags_en: [bit depth, quantization noise, digital audio]
alias: [位深, 量化噪声, 比特深度, bit depth]
links:
  - "[[glossary:bit-depth]]"
  - "[[glossary:dither]]"
  - "[[glossary:noise-floor]]"
instances:
  - atepp-000195 | 钢琴音符和力度素材，可另行制作低位深淡出实验 | Piano notes and velocities for a separate reduced-depth fade experiment
  - giantmidi-003263 | 和弦衰减的音乐参照，不包含低位深渲染 | A musical reference for chord decay without reduced-depth renders
  - atepp-003869 | 低音区持续音符，不记录量化噪声的实际频谱 | Sustained bass-register notes without a measured quantisation-noise spectrum
sources:
  - "https://downloads.izotope.com/docs/rx6/39-dither/index.html"
  - Ken C. Pohlmann, Principles of Digital Audio — 用于核对量化噪声与位深的换算。
  - Stanley Lipshitz, John Vanderkooy, Quantization and Dither — 用于核对抖动与噪声整形的结论。
updated: 2026-11-02
---

::: zh
## 起点：一个问题

位深改变幅度量化的精度，实际听到的底噪还包含录音设备和环境。比较两个文件前，应先确认它们来自同一源音频、处理链一致，而不是把不同录音的噪声差异归给位深。

## 它怎么工作

16 位定点 PCM 有 65536 个编码级，24 位有 16777216 个。理想量化器在一定信号与误差模型下，每增加一位，信噪比约改善 6 dB；未加抖动的误差不一定是均匀噪声，也可能与信号相关。浮点使用有效数字和指数表示幅度，可提供很大的数值余量，但精度仍有限，也不能消除原录音噪声。

## 旋钮与做法

录制与交付位深先按设备能力和接收方要求确定。录音时为突发峰值留余量，混音时了解 DAW 的内部运算格式，最终转为定点输出时配置抖动。把原有16位文件放进浮点工程有助于后续计算，却不会恢复已经损失的录音信息。

## 耳朵要抓的点

取同一低电平音频淡出，分别导出低位深的加抖动与不加抖动版本，再在安全监听电平下比较尾音和频谱。文件不同不代表必定可闻；底噪、播放设备和音量都会影响判断。

## 容易弄错的

以为位深决定频率上限；以为 24 位一定比 16 位好听；以为抖动可以补救削波。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["E4","G4","B4","E5"],"label":"钢琴衰减参照","label_en":"Piano-decay reference","hint":"合成与 GM 钢琴都由 MIDI 触发，不能称为原演奏录音。量化对照需另制同一源音频的不同位深版本。","hint_en":"Both synthesized and GM piano are triggered from MIDI, not original performance recordings. Compare quantisation using alternate bit-depth renders of one source."}
```
:::

::: en
## Starting point: a problem

Bit depth changes amplitude-quantisation precision; audible noise also includes recording equipment and environment. Before comparing files, confirm one source and matching processing rather than attributing differences between recordings to bit depth.

## How it works

16-bit fixed-point PCM has 65536 code levels and 24-bit PCM has 16777216. Under suitable ideal signal and error assumptions, each added bit improves signal-to-noise ratio by about 6 dB. Undithered error need not be uniform noise and may be signal-correlated. Floating point uses a significand and exponent for large numerical headroom, but precision remains finite and existing recording noise remains.

## Knobs and practice

Choose recording and delivery depth for equipment and recipient requirements. Leave room for unexpected peaks, know the DAW’s internal format, and configure dither at final fixed-point quantisation. Loading an existing 16-bit file into a floating-point session supports later computation but does not restore lost recording information.

## What the ear catches

Render one low-level fade at reduced depth with and without dither, then compare decay and spectrum at a safe monitor level. Different files need not sound detectably different; source noise, playback equipment and level affect the judgement.

## Easy to get wrong

That bit depth sets the frequency limit; that 24 bits always sounds better; that dither can rescue clipping.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["E4","G4","B4","E5"],"label":"Piano-decay reference","label_en":"Piano-decay reference","hint":"Both synthesized and GM piano are triggered from MIDI, not original performance recordings. Compare quantisation using alternate bit-depth renders of one source.","hint_en":"Both synthesized and GM piano are triggered from MIDI, not original performance recordings. Compare quantisation using alternate bit-depth renders of one source."}
```
:::
