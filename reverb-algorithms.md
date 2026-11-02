---
id: reverb-algorithms
site: prod
cat: A7
title: 混响算法与卷积
title_en: Reverb Algorithms and Convolution
summary: 房间、厅堂、板式与弹簧各自的声音特征，卷积又补上了什么。
summary_en: How room, hall, plate and spring reverbs differ, and where convolution fits among them.
level: standard
tags: [效果器, 混响, 空间, 听感]
tags_en: [effects, reverb, space, listening]
alias: [混响, 混响算法, 房间混响, 厅堂, 板式, 弹簧, 卷积混响, reverb, convolution]
links:
  - "[[glossary:reverb]]"
  - "[[glossary:bus]]"
  - "[[instrument:organ]]"
instances:
  - cyberhymnal-008348 | 持续和弦可渲染成测试素材，再分别送入房间与厅堂混响，匹配湿声电平 | Render sustained chords and send them through room and hall reverbs at matched wet level
  - pdmx-000070 | 持续弦乐可用于外部混响比较，先匹配衰减与湿声电平，再比较密度 | Use sustained strings for an external reverb comparison, matching decay and wet level before judging density
  - mutopia-001413 | 钢琴句间空隙可用于听外加混响的尾音，保留同一干声作参照 | Piano gaps can reveal added reverb tails; retain the same dry source as reference
sources:
  - Välimäki, Parker and Savioja, Fifty Years of Artificial Reverberation, IEEE TASLP 2012.
  - Udo Zölzer, DAFX.
updated: 2026-11-02
---

::: zh
## 为什么会用到它

房间、厅堂、板式和弹簧描述空间或装置特性，算法与卷积描述实现方式。两种分类不是互斥的：算法可以模拟板式，卷积也可以使用板式装置的脉冲响应。先确定需要的反射、衰减和音色，再选实现。

## 背后的机制

算法混响可用延迟网络、滤波与调制产生反射和衰减；卷积把输入与脉冲响应组合，响应可以来自真实空间、装置或人工设计。固定卷积通常受所录响应限制，但产品可提供编辑和混合方案。某种实现不自动比另一种更真实或更适合所有素材。

## 数值怎么变成声音

在同一短句上分别调整预延迟、早期反射、衰减与湿声电平，每次只改一项。目标是让下一句仍清楚、空间与编制相符，而不是给大厅、军鼓或弹簧一律指定秒数。比较时保留干声比例并检查单声道。

## 耳朵要抓的点

拍一次手，比较房间与厅堂的尾巴。在军鼓上换板式，变化的不只是长度，还有密度。把弹簧放在吉他上，尾音会带出金属味。

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"blown","phrase":["C3","G3","C4","E4"],"label":"管风琴混响测试素材","label_en":"Organ material for reverb tests","hint":"在 DAW 中给同一干声分别加厅堂与板式混响，匹配衰减和湿声电平，比较早期反射及尾音密度。","hint_en":"In a DAW, apply hall and plate reverbs to one dry source. Match decay and wet level, then compare early reflections and tail density."}
```

## 容易弄错的

以为衰减越长空间越大；用混响掩盖音准问题；认为卷积一定比算法真实。
:::

::: en
## Why reach for it

Room, hall, plate and spring describe spaces or devices; algorithmic and convolution describe implementations. The categories overlap: an algorithm can model a plate and convolution can use a plate impulse response. Define reflections, decay and timbre before choosing an implementation.

## The mechanism

Algorithmic reverbs can use delay networks, filters and modulation; convolution combines input with an impulse response captured from a space or device or designed artificially. Fixed convolution is constrained by its response, though products may offer editing and hybrid methods. Neither implementation is automatically more realistic or suitable for every source.

## From numbers to sound

Adjust pre-delay, early reflections, decay and wet level separately on one phrase. Aim for clear following phrases and space appropriate to the arrangement rather than fixed decay seconds for halls, snares or springs. Preserve the dry balance and check mono when comparing.

## What the ear should catch

Clap once and compare a room with a hall. Swap a plate onto a snare and hear density change, not only length. Put a spring on guitar and the tail turns metallic.

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"blown","phrase":["C3","G3","C4","E4"],"label":"Organ material for reverb tests","label_en":"Organ material for reverb tests","hint":"In a DAW, apply hall and plate reverbs to one dry source. Match decay and wet level, then compare early reflections and tail density.","hint_en":"In a DAW, apply hall and plate reverbs to one dry source. Match decay and wet level, then compare early reflections and tail density."}
```

## Easy to get wrong

That longer decay means a bigger space; that reverb hides tuning problems; that convolution is always more real than an algorithm.
:::
