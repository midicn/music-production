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
  - atepp-000195 | 德彪西《月光》的弱奏与长衰减把噪声底推到能听见的位置
  - giantmidi-003263 | 萨蒂《玄秘曲》里极弱的和弦余韵最考验低位深的尾巴
  - atepp-003869 | 贝多芬《月光》低音区的持续音让量化噪声更像一层薄雾
sources:
  - Ken C. Pohlmann, Principles of Digital Audio — 用于核对量化噪声与位深的换算。
  - Stanley Lipshitz, John Vanderkooy, Quantization and Dither — 用于核对抖动与噪声整形的结论。
updated: 2026-10-28
---

::: zh
## 起点：一个问题

同样是 44.1 kHz，为什么 8 位录音的底噪像一层沙，而 24 位几乎听不见？

## 它怎么工作

每个采样点要存成一个整数，位数决定可用的台阶数。16 位有 65536 级，24 位约有一千六百多万级。台阶越粗，最轻的声音越容易被抹平，差距变成量化噪声。量化噪声大致均匀分布在频带里，位深每增加一位，噪声底约下降 6 dB。16 位在正常监听音量下已经够用，24 位留出的余量主要用于录音时避免削波，以及多次处理后的累积误差。浮点格式把台阶换成指数，处理过程中几乎不再增加噪声。

## 旋钮与做法

录音用 24 位，留 12 到 18 dB 余量。混音内部用 32 位浮点。交付用 24 位，需要 16 位版本时最后再加抖动。判断位深够不够，看最安静的段落有没有被噪声盖住，而不是看文件大小。衰减很大的轨道，例如长混响尾巴，最容易暴露噪声。多次增益变化之后，检查一次噪声底。

## 耳朵要抓的点

听钢琴弱奏后的余韵，低位深会让尾巴提前断掉，或者带上颗粒。听人声句尾的气息，噪声底高时气息会变成一层薄纱。听淡出结尾，量化噪声常在最后几秒变得明显。听极安静的室内乐，注意力放在两件乐器之间，而不是音符本身。

## 容易弄错的

以为位深决定频率上限；以为 24 位一定比 16 位好听；以为抖动可以补救削波。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["E4","G4","B4","E5"],"label":"弱奏后的余韵","label_en":"The tail after a soft chord","hint":"先听真实钢琴的余韵，再听合成近似的尾巴；低位深的粗糙感要在导出成 8 位时对比","hint_en":"Hear the real piano tail, then the synth approximation; the roughness of low bit depth needs an 8-bit export to compare"}
```
:::

::: en
## Starting point: a problem

At the same 44.1 kHz, why does an 8-bit recording hiss like sand while a 24-bit one is nearly silent?

## How it works

Every sample is an integer, and bit depth sets how many steps are available. Sixteen bits give 65,536 steps; 24 bits give about 16.7 million. Coarser steps flatten the quietest detail, and the error becomes quantization noise. That noise is spread fairly evenly across the band, and each extra bit lowers the floor by roughly 6 dB. Sixteen bits are enough at normal listening levels; the extra room mainly prevents clipping and absorbs accumulated error across processing. Floating point replaces steps with an exponent, so processing adds almost no noise.

## Knobs and practice

Record at 24 bits with 12 to 18 dB of headroom. Mix internally at 32-bit float. Deliver 24-bit files, and add dither only when making the 16-bit version. Judge depth by whether the quietest passage is buried, not by file size. Tracks with heavy attenuation, such as long reverb tails, expose the floor first.

## What the ear catches

Hear a soft piano note's tail: low depth cuts it short or adds grain. Hear the breath at the end of a vocal phrase, which turns into a thin veil when the floor is high. Hear a fade-out, where quantization noise often becomes obvious in the last seconds. In quiet chamber music, listen between the instruments, not the notes.

## Easy to get wrong

That bit depth sets the frequency limit; that 24 bits always sounds better; that dither can rescue clipping.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["E4", "G4", "B4", "E5"], "label": "The tail after a soft chord", "label_en": "The tail after a soft chord", "hint": "Hear the real piano tail, then the synth approximation; the roughness of low bit depth needs an 8-bit export to compare", "hint_en": "Hear the real piano tail, then the synth approximation; the roughness of low bit depth needs an 8-bit export to compare"}
```
:::
