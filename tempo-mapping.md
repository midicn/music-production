---
id: tempo-mapping
site: prod
cat: B2
title: 速度映射
title_en: Tempo Mapping
summary: 速度不是一条直线，速度映射把演奏的呼吸画进时间轴。
summary_en: Tempo is never a straight line; a tempo map draws a performance's breathing onto the timeline.
level: standard
tags: [速度, 映射, 自由速度, 时间轴]
tags_en: [tempo, mapping, rubato, timeline]
alias: [速度映射, tempo map, 变速, 弹性速度]
links:
  - "[[glossary:tempo]]"
  - "[[glossary:daw]]"
  - "[[glossary:velocity]]"
instances:
  - atepp-001115 | 肖邦第一叙事曲的自由速度，演奏速度不断伸缩，固定节拍器对不上（C1）
  - musicnet-000068 | 贝多芬四重奏的乐句呼吸，速度微调让句尾自然松开（C1）
  - cyberhymnal-008729 | 管风琴赞美诗的稳定速度，作为对照听速度映射的必要性（C1）
sources:
  - 速度映射与自由速度的处理方式，依 DAW 公开文档核对，未抄原文
  - 演奏速度变化与记谱的关系，依表演实践通识核对，未抄文本
updated: 2026-10-28
---

::: zh
## 问题

在 DAW 里给演奏录音配网格，常遇到一个麻烦：演奏者并没有按固定速度弹，句尾会松、高潮会赶。强行把网格设成一条直线，音符就会离网格越来越远。速度映射就是把演奏实际的速度变化画出来，让网格跟着人走。

## 原理

速度映射在时间轴上放置一系列速度值，两点之间线性或曲线过渡。MIDI 文件里对应的是速度事件，音频文件则需要先分析瞬态或让演奏者跟着点击声录。映射好之后，量化、复制段落与添加虚拟乐器才有共同的参照。自由速度段落的速度曲线可以很密，机械段落则保持平直。

## 参数与做法

先听整段，标出速度明显变化的节点，再在节点之间做平滑过渡。句尾放慢、高潮略快是常见处理，但幅度要克制。用点击声录制时，点击声本身也要跟随速度变化。映射完成后检查网格与小节线是否落在乐句的自然位置上。复制段落前确认速度曲线也一起复制。给虚拟乐器加自动化时，速度映射能让它与人声或独奏贴合。

## 听什么

在叙事曲里听速度伸缩是否被完整记录，在四重奏里听句尾的松开是否自然，在赞美诗的稳定段落里听固定速度与自由速度的对比。速度映射做得好，时间轴会看起来像演奏，而不是像节拍器。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["E4","G4","B4","E5","D5","B4","G4","E4"],"label":"句尾的松开","label_en":"A phrase easing at the end","hint":"最后两个音稍慢一点，速度映射就是把这种变化画出来","hint_en":"The last two notes ease; a tempo map is how that easing gets drawn"}
```
:::

::: en
## The problem

Putting a played take on a DAW grid runs into a familiar snag: the player did not keep a fixed tempo, easing at phrase ends and pushing at climaxes. Force the grid to a straight line and notes drift further and further from it. A tempo map draws the performance's actual speed changes so the grid follows the player.

## How it works

A tempo map places a series of tempo values along the timeline with linear or curved transitions between them. In a MIDI file they are tempo events; for audio you first analyse transients or record the player against a click that itself moves. Once mapped, quantising, copying sections and adding virtual instruments all share one reference. Free passages can carry a dense curve while mechanical sections stay flat.

## Settings and practice

Listen through first and mark the points where tempo clearly shifts, then smooth the transitions between them. Easing at phrase ends and lifting slightly at climaxes is normal, but keep the amounts modest. When recording to a click, make the click follow the tempo changes too. After mapping, check that bars and grid lines land on natural phrase points. Confirm the tempo curve copies with any duplicated section. Automating virtual instruments against a tempo map is what lets them sit with a voice or a soloist.

## What to listen for

In the ballade, whether the rubato is captured whole; in the quartet, whether phrase endings relax naturally; in the hymn, how steady tempo contrasts with free playing. A good tempo map makes the timeline look like a performance rather than a metronome.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["E4","G4","B4","E5","D5","B4","G4","E4"],"label":"A phrase easing at the end","label_en":"A phrase easing at the end","hint":"The last two notes ease; a tempo map is how that easing gets drawn","hint_en":"The last two notes ease; a tempo map is how that easing gets drawn"}
```
:::
