---
id: anti-aliasing
site: prod
cat: B4
title: 抗混叠
title_en: Anti-Aliasing
summary: 采样前压掉超上限的高频，防止它们折回成假声。
summary_en: Filtering above the ceiling before sampling stops high frequencies folding back as false tones.
level: standard
tags: [抗混叠, 采样率, 滤波器]
tags_en: [anti-aliasing, sample rate, filter]
alias: [混叠, 折叠失真, aliasing, anti-aliasing filter]
links:
  - "[[glossary:sample-rate]]"
  - "[[glossary:harmonics]]"
  - "[[glossary:timbre]]"
instances:
  - groove-000000 | 鼓组音符素材，可另行渲染后做抗混叠实验 | Drum notes for a separately rendered anti-aliasing experiment
  - pdmx-000251 | 高音打击乐的音符参照，不包含降采样后的音频 | High-percussion notes without downsampled audio
  - atepp-000381 | 钢琴高音区音符参照，不证明出现了混叠 | High piano notes that do not establish aliasing
sources:
  - "https://docs.scipy.org/doc/scipy/reference/generated/scipy.signal.resample_poly.html"
  - Ken C. Pohlmann, Principles of Digital Audio — 用于核对混叠与过采样的机制。
  - Julius O. Smith III, Digital Audio Resampling — 用于核对重采样滤波与过渡带的说明。
updated: 2026-11-02
---

::: zh
## 要解决的事

为什么有些录音一降采样，镲片就多出一层沙沙的假声，而原始文件里并没有这层声音？

## 它怎么工作

采样率为 Fs 时，输入中超出奈奎斯特频率 Fs/2 的成分可能映射到较低频率。例如以 8 kHz 采样未受限的 6 kHz 正弦，会与 2 kHz 分量混淆。抗混叠滤波必须在这一步折返之前限制带宽；折返一旦与有用信号重叠，事后低通不能自动分开。过渡带、衰减与运算成本需要一起设计。

## 旋钮与做法

降采样应使用带抗混叠滤波的转换器。非线性失真和部分变调算法可能新生成高频成分，可比较其过采样或带限选项；仅把文件采样率调高并不保证算法正确。用扫频或单频测试时，记录输入频率、采样率和处理设置，并在频谱中检查原信号以外的折返分量。

## 耳朵要抓的点

升高一个测试正弦的频率，若出现向相反方向移动的频谱线，可结合采样率计算它是否是混叠。复杂音乐中的金属声、粗糙感或嘶声也可能来自失真、编码和音色本身，不能只凭这些形容词确诊。

## 容易弄错的

以为混叠只发生在低端设备；以为加一个低通效果器就能解决；以为提高音量可以掩盖。

```audiolab
{"type":"instrument","gm":"Lead 2 (sawtooth)","synth":"bowed","phrase":["A5","C6","E6","A6"],"label":"高音区锯齿音色","label_en":"High-register sawtooth timbre","hint":"高音区音色可供参照，但播放器没有切换抗混叠滤波。真正的混叠测试要指定频率、采样率和算法，再检查折返分量。","hint_en":"This high-register timbre is a reference without an anti-alias filter switch. Specify frequency, rate and algorithm before inspecting alias components."}
```
:::

::: en
## The problem to solve

Why does downsampling sometimes add a sandy layer to cymbals that was not in the original file?

## How it works

At sample rate Fs, components above the Nyquist frequency Fs/2 can map to lower frequencies. An unfiltered 6 kHz sine sampled at 8 kHz, for example, aliases to 2 kHz. Bandwidth must be limited before that folding occurs; a later low-pass cannot automatically separate aliases already overlapping wanted signal. Transition width, attenuation and computation cost must be designed together.

## Knobs and practice

Use an anti-aliased converter for downsampling. Nonlinear distortion and some pitch algorithms can generate new high frequencies, so compare available oversampling or band-limited modes; raising the file rate alone is not a guarantee. For a sine or sweep test, record frequency, rate and settings and inspect folded components in the spectrum.

## What the ear catches

When a test sine rises, an oppositely moving spectral component can be checked against the sample rate as a possible alias. Metallic sound, roughness or hiss in music can also come from distortion, coding or the instrument itself; these descriptions alone do not diagnose aliasing.

## Easy to get wrong

That aliasing only happens on cheap gear; that a low-pass effect fixes it; that louder playback hides it.

```audiolab
{"type":"instrument","gm":"Lead 2 (sawtooth)","synth":"bowed","phrase":["A5","C6","E6","A6"],"label":"High-register sawtooth timbre","label_en":"High-register sawtooth timbre","hint":"This high-register timbre is a reference without an anti-alias filter switch. Specify frequency, rate and algorithm before inspecting alias components.","hint_en":"This high-register timbre is a reference without an anti-alias filter switch. Specify frequency, rate and algorithm before inspecting alias components."}
```
:::
