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
  - pdmx-002592 | 密集配器的音符参照，可用于讨论声部让位 | Dense-instrumentation notes for discussing part spacing
  - groove-000000 | 鼓组节奏参照，不包含过度压缩的音频版本 | Drum-rhythm reference without an overcompressed audio version
  - mutopia-000546 | 声乐与钢琴的声部参照，不记录真实演唱齿音 | Voice-and-piano parts without recorded vocal sibilance
sources:
  - Owsinski, Bobby，The Mixing Engineer's Handbook（Cengage）— 混音常见问题章节核对，未引用
  - Katz, Bob，Mastering Audio（Focal Press）— 单声道检查与动态判断章节核对，未引用
updated: 2026-11-02
---

::: zh
## 为什么会用到
混音的错误往往不刺耳，只是还行，直到换一套系统才暴露。听辨训练的目标是给每种毛病找到对应的症状与动作。

## 它怎么工作
把症状当线索而非诊断：浑浊可能来自音区、增益、混响或频谱重叠；刺耳也可能只出现在少数音节；起音变弱可能来自演奏、包络或动态处理。检查单声道时应将左右声道按正确方式求和，关闭一只音箱只会少听一条声道，不能代替单声道折叠。

## 参数与取舍
先用较小监听音量检查平衡，再与匹配响度的参考比较。逐个旁通可疑处理，在上下文中判断原因：若降低一条声部就解决掩蔽，不必先给每轨高通；若只有一个擦音刺耳，可局部处理，不必削暗整首。独奏用于定位，最终判断仍要回到全组。

## 耳朵要抓的点
贝斯与底鼓是否在同一条线上，人声是否被埋，镲片是否先于内容吸引注意，关掉混响后细节是否回来。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","D3","E3","G3","B3"],"label":"低音区密集和弦","label_en":"Dense bass-register chord","hint":"可以观察低音区音符叠置的听感；实际混音问题还需检查音色、增益和效果链，不能只由谱面判断。","hint_en":"Hear notes crowded into the bass register. Actual mix faults also require checking timbre, gain and processing rather than the score alone."}
```

## 容易弄错的
以为响就是好，或每个轨道都要加均衡。问题常常出在编曲与音区，而不是插件；母带也救不回已经糊掉的中频。
:::

::: en
## Why you reach for it
Mix mistakes rarely shout; they pass as fine until another system exposes them. Critical listening should attach a symptom and an action to each fault.

## How it works
Treat symptoms as clues rather than diagnoses: mud may come from register, gain, reverb or spectral overlap; harshness may affect only a few syllables; weak attacks may reflect performance, envelopes or dynamics. A mono check sums left and right correctly. Muting one speaker removes a channel and is not a substitute.

## Settings and trade-offs
Check balance at moderate level, then compare a loudness-matched reference. Bypass suspect processing one element at a time in context. If lowering one part fixes masking, do not automatically high-pass every track; if one sibilant is harsh, treat it locally rather than darkening the whole mix. Soloing locates problems, but final judgement belongs in the mix.

## What the ear catches
Whether bass and kick share one line, whether the voice is buried, whether cymbals draw attention before the content, and whether detail returns when the reverb is bypassed.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","D3","E3","G3","B3"],"label":"Dense bass-register chord","label_en":"Dense bass-register chord","hint":"Hear notes crowded into the bass register. Actual mix faults also require checking timbre, gain and processing rather than the score alone.","hint_en":"Hear notes crowded into the bass register. Actual mix faults also require checking timbre, gain and processing rather than the score alone."}
```

## Common misconceptions
That loud is good, or that every track needs EQ. The problem often sits in the arrangement and register rather than a plug-in; mastering cannot rescue a midrange that has already turned to mud.
:::
