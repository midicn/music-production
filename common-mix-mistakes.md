---
id: common-mix-mistakes
site: prod
cat: A6
title: 常见错误的听辨
title_en: Hearing Common Mix Mistakes
summary: 浑浊、刺耳、扁平、空心，四种症状对应四类动作。
summary_en: Mud, harshness, flatness and hollowness are four symptoms pointing to four different moves.
level: standard
tags: [混音, 听辨, 浑浊, 相位, 动态]
tags_en: [mixing, listening, mud, phase, dynamics]
alias: [常见错误, 混音错误, 听辨错误, mix mistakes, critical listening]
links:
  - "[[glossary:mixdown]]"
  - "[[glossary:phase-check]]"
  - "[[glossary:headroom]]"
instances:
  - pdmx-002592 | 木管与弦乐密集，中低浑浊与掩蔽最容易在这一段暴露
  - groove-000000 | 鼓循环的瞬态清楚，过度压缩与镲片刺耳可当场辨认
  - mutopia-000546 | 人声与钢琴同场，齿音与中频掩蔽的典型素材
sources:
  - Owsinski, Bobby，The Mixing Engineer's Handbook（Cengage）— 混音常见问题章节核对，未引用
  - Katz, Bob，Mastering Audio（Focal Press）— 单声道检查与动态判断章节核对，未引用
updated: 2026-10-28
---

::: zh
## 为什么会用到
混音的错误往往不刺耳，只是还行，直到换一套系统才暴露。听辨训练的目标是给每种毛病找到对应的症状与动作。

## 它怎么工作
常见问题可以归成四类。中低频堆积让声音浑浊，症状是贝斯与底鼓争同一八度；高频过多让耳朵疲劳，症状是镲片比人声还亮；过度压缩让瞬态消失，症状是鼓没有起音、整体变平；相位问题让单声道塌陷，症状是关掉一只音箱后某些元素消失。混响过多则是另一种远，细节被尾巴盖住。

## 参数与取舍
先小音量听平衡，再用单声道检查相位，最后与参考曲对比亮度与低频。独奏每个元素，确认它单独成立，再放回整体。高频刺耳先查二到四千赫兹的堆积，而不是继续加均衡。低频浑浊先切高通，再决定要不要减。

## 耳朵要抓的点
贝斯与底鼓是否在同一条线上，人声是否被埋，镲片是否先于内容吸引注意，关掉混响后细节是否回来。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","D3","E3","G3","B3"],"label":"低音区的密集和弦","label_en":"A dense chord in the low register","hint":"先听这几个低音挤在一起，再想象叠加贝斯后浑浊会加重多少","hint_en":"Hear these low notes crowd together, then imagine how much muddier they become under a bass"}
```

## 容易弄错的
以为响就是好，或每个轨道都要加均衡。问题常常出在编曲与音区，而不是插件；母带也救不回已经糊掉的中频。
:::

::: en
## Why you reach for it
Mix mistakes rarely shout; they pass as fine until another system exposes them. Critical listening should attach a symptom and an action to each fault.

## How it works
Four families cover most of them. Build-up in the low midrange makes mud, and the symptom is bass and kick fighting over one octave. Excess highs tire the ear, and the symptom is cymbals brighter than the voice. Over-compression removes transients, and the symptom is drums with no attack and a flat whole. Phase trouble collapses mono, and the symptom is elements disappearing when one speaker is muted. Too much reverb is a different kind of distance, where the tail covers detail.

## Settings and trade-offs
Listen quietly for balance first, check phase in mono next, then compare brightness and bass with a reference. Solo each element to confirm it stands alone, then return it to the whole. For harsh highs, look for a pile-up between two and four kilohertz instead of adding more EQ. For low mud, high-pass first and then decide whether to cut.

## What the ear catches
Whether bass and kick share one line, whether the voice is buried, whether cymbals draw attention before the content, and whether detail returns when the reverb is bypassed.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C3", "D3", "E3", "G3", "B3"], "label": "A dense chord in the low register", "label_en": "A dense chord in the low register", "hint": "先听这几个低音挤在一起，再想象叠加贝斯后浑浊会加重多少", "hint_en": "Hear these low notes crowd together, then imagine how much muddier they become under a bass"}
```

## Common misconceptions
That loud is good, or that every track needs EQ. The problem often sits in the arrangement and register rather than a plug-in; mastering cannot rescue a midrange that has already turned to mud.
:::
