---
id: multisampling-and-velocity-layers
site: prod
cat: B4
title: 多采样与力度层
title_en: Multisampling and Velocity Layers
summary: 音区与力度各录一层，键盘才不会像一台变调器。
summary_en: Separate samples per register and velocity keep a keyboard from sounding like a pitch shifter.
level: standard
tags: [多采样, 力度层, 采样器]
tags_en: [multisampling, velocity layers, sampler]
alias: [多采样, 力度层, 力度分层, velocity layer]
links:
  - "[[glossary:velocity]]"
  - "[[glossary:timbre]]"
  - "[[instrument:piano]]"
instances:
  - atepp-001114 | 肖邦《叙事曲》从极弱到极强，力度层不足时音色会突然换脸
  - atepp-005385 | 拉威尔《绞刑架》大量极弱和弦，考验弱力度层的细节
  - atepp-003121 | 贝多芬《迪亚贝利变奏曲》主题与进行曲段落在力度上跳变明显
sources:
  - Curtis Roads, The Computer Music Tutorial — 用于核对多采样与力度分层的概念。
  - The New Grove Dictionary of Music and Musicians, entry Piano — 用于核对力度与音色的关系。
updated: 2026-10-28
---

::: zh
## 起点：一个问题

同一个钢琴音色，为什么轻弹和重弹的音色不一样，而不只是音量变小？

## 背后的机制

真实乐器的力度变化会改变激励方式与共鸣。钢琴轻弹时，弦的振动集中在低次谐波，重弹时高次谐波迅速增加，音头也更亮。只用一个样本加音量包络，无法重现这种变化。多采样按音区与力度分别录音，力度层常见四到八层，层与层之间用阈值切换，并用音量与滤波微调做过渡。层数越多，切换越平滑，内存与加载时间也越高。音区层解决变调带来的共振偏移，力度层解决演奏方式带来的频谱变化，两者不能互相替代。

## 旋钮与做法

钢琴常用每八度一到两个音区样本，力度四到八层。弦乐与管乐的力度层可以少一些，但表情层要跟上。切换点放在演奏中较少停留的力度值，避免在长音中间跳层。层间过渡用短交叉淡化或轻微的音量补偿，不要用明显的滤波跳变。检查时弹一段极弱到极强的渐强。

## 耳朵要抓的点

听渐强，注意音色是否在某一刻突然换了一张脸。听重复和弦，弱奏与强奏的泛音比例是否不同。听中音区到高音区的连续半音，注意有没有某个音突然变闷。

## 容易弄错的

以为力度层只是音量档位；以为层数越多越真实；以为音区层可以随意取整。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5"],"label":"轻与重不是同一张脸","label_en":"Soft and hard are not one face","hint":"切到真实音色再切回合成近似，注意强奏时高次泛音是否跟着增加，而不只是变响","hint_en":"Switch to the real timbre, then the synth approximation; hear whether hard playing adds upper partials rather than just level"}
```
:::

::: en
## Starting point: a problem

On one piano patch, why does a soft note differ in colour from a hard one, not just in volume?

## The mechanism

On a real instrument, dynamics change the excitation and resonance of the string or air column. A soft piano strike concentrates energy in low partials; a hard strike adds upper partials quickly and brightens the attack. One sample plus a volume envelope cannot do that. Multisampling records separate zones and velocity layers, often four to eight, switched by thresholds and smoothed with level and filter offset. More layers mean smoother switches but more memory and load time. Key zones address transposition's resonance shift; velocity layers address the spectral change of playing style, and neither replaces the other.

## Knobs and practice

Pianos often use one or two samples per octave and four to eight velocity layers. Strings and winds use fewer, but expression layers still matter. Put switch points where players rarely hold, so a sustained note does not jump mid-breath. Use short crossfades or gentle level compensation between layers, not an obvious filter jump. Test with a slow crescendo from silence to full force.

## What the ear catches

Hear a crescendo and notice whether the tone changes face at some point. Hear repeated chords and compare partial balance between soft and hard. Hear a chromatic run upward and listen for a note that suddenly turns dull.

## Easy to get wrong

That velocity layers are just volume steps; that more layers are always more realistic; that key zones can be rounded off freely.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "C5"], "label": "Soft and hard are not one face", "label_en": "Soft and hard are not one face", "hint": "Switch to the real timbre, then the synth approximation; hear whether hard playing adds upper partials rather than just level", "hint_en": "Switch to the real timbre, then the synth approximation; hear whether hard playing adds upper partials rather than just level"}
```
:::
