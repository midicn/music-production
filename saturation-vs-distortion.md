---
id: saturation-vs-distortion
site: prod
cat: A7
title: 饱和与失真
title_en: Saturation vs Distortion
summary: 同样是非线性，饱和留住轮廓，失真改写轮廓。
summary_en: Both are nonlinear, yet saturation keeps the shape of a transient while distortion rewrites it.
level: standard
tags: [效果器, 饱和, 失真, 谐波]
tags_en: [effects, saturation, distortion, harmonics]
alias: [饱和与失真, 软削波, 硬削波, 过载, saturation vs distortion, overdrive]
links:
  - "[[glossary:clipping]]"
  - "[[glossary:bus]]"
  - "[[instrument:electric-guitar]]"
instances:
  - pdmx-000031 | 拉威尔《波莱罗》钢琴版力度层层增强，饱和与失真的分界随电平移动
  - oga-000004 | 战斗段落的合成器与打击密集，少量处理就会改变整体的硬度
  - mutopia-000005 | 古典吉他拨弦颗粒细，失真会先把指尖噪声一起放大
sources:
  - Zölzer, DAFX.
  - FabFilter, Saturn 2 user manual, drive, mix and oversampling controls.
  - Sound On Sound, saturation and harmonic distortion explained.
updated: 2026-10-31
order: 448
---

::: zh
把饱和器推到失真器的位置，人声不会更厚，只会更早变硬。两者都来自非线性，差别在曲线拐得多急、输入被推得多高。

## 曲线决定音色

饱和的传输曲线是软拐点，输入超过某点后增益缓慢下降，峰值被压圆，低次谐波先出现。失真的曲线接近硬拐点，越过阈值立刻削平，方波边缘带来大量高次谐波。同一个插件把驱动推高，饱和会过渡成失真，分界不在名字，而在工作点。轻柔演奏时几乎不出现，重击时突然变硬，说明曲线已经接近硬拐点。

## 一张对照

| 维度 | 饱和 | 失真 |
|---|---|---|
| 传输曲线 | 软拐点，渐进 | 硬拐点，突然 |
| 驱动量 | 少量，峰值变圆 | 大量，波形趋方 |
| 动态 | 起音保留 | 起音压平 |
| 谐波 | 低次为主，随电平变化 | 高次多，音色固定 |
| 常见位置 | 总线、人声、贝斯 | 吉他、合成器、音效 |

## 电平先于旋钮

非线性处理看见的是输入电平。前一环节的均衡推了 3 dB，饱和的量就跟着变。比较两种失真之前，先把输入对齐到同一响度，否则听到的只是谁更响。输入差 2 dB，谐波比例就会换一个档位；用固定设置对比两种插件，结论往往只是电平差。并联一点干声能保住起音，混量从一成开始试。

```audiolab
{"type":"instrument","gm":"Electric Guitar (clean)","synth":"plucked","phrase":["E2","E2","G2","A2","B2","E3"],"label":"从干净到推满的同一句","label_en":"One phrase from clean to driven","hint":"先听干净拨弦，再想驱动加大后，第二遍的起音是保留还是被压平","hint_en":"Hear the clean pluck, then ask whether the second pass keeps its attack or flattens it as drive rises"}
```

## 用错的地方

没有过采样的失真器会在高频折叠，镲片与齿音先出现砂砾感。贝斯加失真后失去音高轮廓，多半是低频谐波堆得太密。多级串联把每一级都推一点，听到的是压缩而不是厚度。素材本身已经密，再叠饱和只会让混音失去层次。
:::

::: en
Drive a saturator to where a distortion pedal lives and a vocal does not get thicker; it hardens sooner. Both are nonlinear. The difference is how abruptly the curve bends and how hard the input is pushed.

## The curve sets the tone

Saturation uses a soft knee: past a point, gain falls gradually, peaks round off, and low-order harmonics appear first. Distortion approaches a hard knee, flattening everything above the threshold so square edges add many high harmonics. Push one plugin harder and saturation becomes distortion. The border is a working point, not a label. A stage that stays clean in soft playing and hardens under a heavy attack is already close to a hard knee.

## A side-by-side view

| Dimension | Saturation | Distortion |
|---|---|---|
| Transfer curve | Soft knee, gradual | Hard knee, abrupt |
| Drive | Little; peaks round | Much; waveform squares |
| Dynamics | Attack survives | Attack flattened |
| Harmonics | Mostly low order, level-dependent | Many high orders, fixed tone |
| Usual place | Bus, vocal, bass | Guitar, synth, sound design |

## Level comes before the knob

A nonlinear stage sees input level. If the EQ before it adds 3 dB, the amount of saturation changes with it. Match input loudness before comparing two kinds of drive, or you only hear which one is louder. A 2 dB difference at the input moves the harmonic balance to another step; comparing two plugins at fixed settings then measures level, not character. Blend a little dry signal to keep the attack, starting around ten percent mix.

```audiolab
{"type": "instrument", "gm": "Electric Guitar (clean)", "synth": "plucked", "phrase": ["E2", "E2", "G2", "A2", "B2", "E3"], "label": "One phrase from clean to driven", "label_en": "One phrase from clean to driven", "hint": "先听干净拨弦，再想驱动加大后，第二遍的起音是保留还是被压平", "hint_en": "Hear the clean pluck, then ask whether the second pass keeps its attack or flattens it as drive rises"}
```

## Where it goes wrong

A distortion stage without oversampling folds high frequencies, and cymbals and sibilance turn gritty first. Bass that loses its pitch outline usually has too many low harmonics packed together. Stack several gentle stages and the result is compression, not weight. On material that is already dense, more saturation only costs separation.
:::
