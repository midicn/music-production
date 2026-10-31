---
id: sampler-architecture
site: prod
cat: B4
title: 采样器的结构
title_en: Sampler Architecture
summary: 采样器由样本池、映射、声部与包络组成，不只是一个播放键。
summary_en: A sampler is a pool, a map, voices and envelopes working together, not a play button.
level: standard
tags: [采样器, 声部, 映射]
tags_en: [sampler, voices, mapping]
alias: [采样器结构, 采样器架构, sampler architecture]
links:
  - "[[glossary:sampler]]"
  - "[[instrument:samplers]]"
  - "[[instrument:drum-kit]]"
instances:
  - pdmx-000183 | 多声部与多音色并存，能听出声部分配与映射表的层次
  - groove-000000 | 鼓组每个键对应独立样本，是一次性触发的典型结构
  - oga-000004 | 战斗曲把多层音色叠在一起，能听出样本池与包络的分工
sources:
  - Curtis Roads, The Computer Music Tutorial — 用于核对采样器声部与循环结构。
  - MIDI Association, General MIDI 1 Sound Set — 用于核对音色与鼓组编号。
updated: 2026-10-28
---

::: zh
## 起点：一个问题

采样器看起来只是放录音，为什么它还有滤波、包络、调制和路由？

## 工作方式

采样器由几部分组成。样本池存放录音与元数据；映射表把键区与力度区指向样本；声部引擎负责变调、循环与交叉淡化；包络与滤波塑造音头与亮度；调制矩阵把 LFO、力度与控制器接到参数；效果与输出段负责声像、混响与总线。多声部时，每个按键分配一个声部，声部数决定同时能响多少音。流式读取让大样本不必全部进内存，代价是首次触发可能延迟。

## 旋钮与做法

先用映射表把样本摆好，再调包络，最后加滤波与效果。包络的起音不要短于样本本身的音头，否则会削掉瞬态。滤波截止跟着力度走，可以补回变调丢失的亮度。声部数按最密的段落估算，留出余量。流式读取的预读长度影响首音延迟，现场演奏时优先保证响应。改完任何一段，从最低音到最高音过一遍。

## 耳朵要抓的点

听快速和弦，声部数不足时先触发的声音会被截断。听低音区，流式读取不畅时首音会迟一拍。听滤波包络，截止太低会让音头变闷，太高则露出变调的毛边。听多层叠加，确认各层的包络起点是否一致。

## 容易弄错的

以为采样器只有一个播放引擎；以为声部数只影响音量；以为滤波只是装饰。

```audiolab
{"type":"instrument","drum":38,"synth":"perc","phrase":["36","38","42","38"],"label":"底鼓、军鼓与闭镲","label_en":"Kick, snare and closed hat","hint":"每个键都是一个独立样本，听每次触发是否共用同一套包络与滤波","hint_en":"Each key is an independent sample; hear whether every trigger shares one envelope and filter setting"}
```
:::

::: en
## Starting point: a problem

A sampler looks like it only plays recordings, so why does it also have filters, envelopes, modulation and routing?

## The working principle

A sampler is built from parts. The sample pool holds recordings and metadata; the map points key and velocity zones at samples; the voice engine handles transposition, looping and crossfades; envelopes and filters shape attack and brightness; the modulation matrix connects LFOs, velocity and controllers to parameters; effects and output handle pan, reverb and bus routing. Each keypress takes a voice, and the voice count sets how many notes sound at once. Disk streaming keeps large samples out of memory, at the cost of latency on the first trigger.

## Knobs and practice

Place samples in the map first, then shape envelopes, then add filtering and effects. Do not set an attack shorter than the sample's onset, or the transient is cut. Let filter cutoff follow velocity to restore brightness lost in transposition. Size the voice count for the densest passage and leave headroom. Streaming preload length affects first-note latency, so prioritise response in live use.

## What the ear catches

Hear a fast chord: with too few voices, the earliest notes cut off. Hear the low register, where poor streaming delays the first note by a beat. Hear the filter envelope: too low a cutoff dulls the attack, too high exposes transposition grit. Hear stacked layers and check whether envelopes start together.

## Easy to get wrong

That a sampler has one playback engine; that voice count only affects loudness; that the filter is decoration.

```audiolab
{"type": "instrument", "drum": 38, "synth": "perc", "phrase": ["36", "38", "42", "38"], "label": "Kick, snare and closed hat", "label_en": "Kick, snare and closed hat", "hint": "Each key is an independent sample; hear whether every trigger shares one envelope and filter setting", "hint_en": "Each key is an independent sample; hear whether every trigger shares one envelope and filter setting"}
```
:::
