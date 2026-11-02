---
id: headroom-and-clipping
site: prod
cat: B5
title: 余量与削波
title_en: Headroom and Clipping
summary: 区分录音、浮点处理与最终输出的余量，找到削波真正发生的位置。
summary_en: Distinguish recording, floating-point processing and final-output headroom to locate where clipping occurs.
level: standard
tags: [余量, 削波, 满刻度, 增益结构]
tags_en: [headroom, clipping, full scale, gain structure]
alias: [余量, 削波, 过载, headroom, clipping]
links:
  - "[[glossary:headroom]]"
  - "[[glossary:bit-depth]]"
  - "[[glossary:compressor]]"
instances:
  - groove-000005 | 可渲染鼓组并逐步提高求和电平，检查哪一级出现过载 | Render the kit and raise summing level gradually to locate the stage that overloads
  - atepp-001114 | 钢琴演奏数据可作峰值素材；渲染后测量，勿把它称为含观众噪声的原现场录音 | Piano performance data supplies peaks for measurement after rendering, not an original live recording with audience noise
  - mutopia-000498 | 可渲染渐强段检查求和峰值，削波位置需结合实际运算与输出格式 | Render a crescendo and inspect summed peaks; clipping depends on actual processing and output format
sources:
  - 浮点与定点满刻度的差别，对照数字音频惯例整理。
  - 增益结构的分级做法（录音工程公开资料）。
updated: 2026-11-02
---

::: zh
## 起点：一个问题

Headroom是信号离下一个环节可接受上限的余量。定点文件与转换器通常以0 dBFS为数字满刻度，浮点内部节点可以表示更大数值；因此看到表头越零时，应先判断它在哪个环节，以及是否已经发生有界削波或非线性处理。

## 它怎么工作

把超范围数值写入有限范围的整数PCM时，必须先做增益或限幅等处理；具体工具也可能直接截断而留下削波。浮点链路能表示超过0 dBFS的数值，但有界或非线性环节仍可能失真。削波产生的谐波、互调与可能的混叠取决于信号和实现。轨道瞬时样值按带符号相加，整体峰值取决于各路出现峰值的时刻与相关性，不能把各轨峰值数字简单相加。

## 参数与做法

录音时让预计最强的演奏仍有余量；具体峰值随声源与设备而定。混音中检查插件输入输出和主输出，不必给每种工程规定相同的−6 dB峰值。最终按交付要求检查采样峰值与真峰值。降低后级推子可恢复未削波浮点节点的余量，却不能找回转换器或定点文件已丢失的波形。

## 耳朵要抓的点

用同一测试音或录音，分别观察电平进入与离开各环节的情况，确认失真最早出现在哪里。对比时匹配输出响度，避免把更响当作更好。削波既可能改变峰值，也可能改变平均响度与谐波，不能说削波后只变脏、绝不变响。

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E1","E1","G1","A1","E1","E1","D1","E1"],"label":"贝斯峰值测试素材","label_en":"Bass material for a peak test","hint":"在 DAW 测这段的峰值，再按小步长提高增益；检查定点输出前的峰值，不预设低频一定先削波。","hint_en":"Measure this phrase’s peaks in a DAW and raise gain in small steps. Check before fixed-point output rather than assuming bass must clip first."}
```
:::

::: en
## Starting point: a problem

Headroom is the margin below the next stage’s acceptable limit. Fixed-point files and converters normally use 0 dBFS as digital full scale, while floating-point internal nodes can represent larger values. If a meter crosses zero, identify the stage and whether bounded clipping or nonlinearity has already occurred.

## How it works

Values beyond an integer-PCM range need gain or other appropriate treatment before writing; a tool may instead clamp them and leave clipping. Float paths can represent values above 0 dBFS, while bounded or nonlinear stages can still distort. Harmonics, intermodulation and possible aliasing depend on signal and implementation. Track samples sum with their signs; combined peak depends on timing and correlation, not a simple sum of each track’s peak number.

## Settings and practice

During recording, leave room above the expected loudest performance. Check plug-in inputs, outputs and master output rather than imposing one −6 dB peak on every session. Verify sample and true peaks for delivery. A later fader can recover headroom at an unclipped floating-point node, but not waveform information already lost in a converter or fixed-point file.

## What the ear catches

Follow the same test signal or recording through the chain to locate where distortion first appears. Match output loudness before comparison. Clipping can change peaks, average loudness and harmonics; it is not limited to adding dirt without changing perceived level.

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E1","E1","G1","A1","E1","E1","D1","E1"],"label":"Bass material for a peak test","label_en":"Bass material for a peak test","hint":"Measure this phrase’s peaks in a DAW and raise gain in small steps. Check before fixed-point output rather than assuming bass must clip first.","hint_en":"Measure this phrase’s peaks in a DAW and raise gain in small steps. Check before fixed-point output rather than assuming bass must clip first."}
```
:::
