---
id: round-robin-and-articulations
site: prod
cat: B4
title: 轮替采样与奏法切换
title_en: Round Robin and Articulation Switching
summary: 同一个音连打会露出机器味，轮替与奏法切换让它像真乐器。
summary_en: Repeating one sample exposes the machine; round robin and articulation switching make it sound played.
level: standard
tags: [轮替采样, 奏法, 采样器, 拟真]
tags_en: [round robin, articulation, sampler, realism]
alias: [轮替采样, 奏法切换, round robin, articulation switching]
links:
  - "[[glossary:sampler]]"
  - "[[glossary:velocity]]"
  - "[[instrument:violin]]"
instances:
  - thesession-006629 | 爱尔兰曲调的连奏与断奏，同一把琴的奏法切换决定乐句语气（C1）
  - musicnet-000067 | 贝多芬四重奏的弓法变化，分弓与连弓是同一音高的不同发声（C1）
  - atepp-000126 | 德彪西六度练习曲，重复音若每次都用同一个样本会立刻露馅（C1）
sources:
  - 轮替采样与奏法切换的实现方式，依采样器公开文档核对，未抄原文
  - 乐器奏法对起音与衰减的影响，依配器通识核对，未抄文本
updated: 2026-10-28
---

::: zh
## 问题

用采样做弦乐或管乐，最容易露馅的是重复音：同一个音连打三次，如果每次都放同一个样本，三次的起音、噪声与尾音完全一样，耳朵立刻听出是机器。轮替采样与奏法切换就是解决这个问题。

## 原理

轮替采样为同一个音准备多个录音，每次触发换一个，避免机械重复。奏法切换为连奏、断奏、滑音、弱音器等准备不同的样本组，用键位或控制器切换。力度层解决强弱，轮替解决重复，奏法解决语气。三者结合才能接近真实演奏。切换点若处理不好，会出现音量跳变或音色断层。

## 参数与做法

先设好力度层与轮替组的数量，再分配切换键。连奏段落用连音样本，断奏用短音样本。滑音用专门的过渡样本，别用弯音轮硬拉。切换时用渐变更自然，避免硬切。检查轮替组的音量是否一致，不一致会听起来忽大忽小。演奏时把奏法切换当成演奏的一部分，而不是后期修补。

## 听什么

在爱尔兰曲调里听连奏与断奏的语气差别，在四重奏的弓法变化里听同一音高的不同发声，在德彪西的重复音里听轮替是否消除了机械感。好的采样演奏让人忘记这是采样。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["A4","A4","A4","A4","G4","F4","E4","D4"],"label":"重复音的轮替","label_en":"Repeated notes with round robin","hint":"四个同音若每次都一样就露馅，轮替让每次起音略有不同","hint_en":"Four identical notes expose a single sample; round robin varies each attack slightly"}
```
:::

::: en
## The problem

Sampled strings and winds give themselves away on repeated notes: play the same pitch three times and, if the same sample fires each time, the attack, noise and tail are identical, and the ear hears a machine. Round robin and articulation switching exist to fix that.

## How it works

Round robin keeps several recordings of one note and rotates through them so repeats never duplicate. Articulation switching supplies separate sample sets for legato, staccato, portamento and mutes, selected by keyswitch or controller. Velocity layers handle loud and soft, round robin handles repetition, articulation handles phrasing. Only all three together approach a real performance. Poorly handled switches produce level jumps or breaks in timbre.

## Settings and practice

Set velocity layers and round-robin groups first, then assign keyswitches. Use legato samples in connected passages and short samples for staccato. Reserve dedicated transition samples for slides instead of bending the pitch wheel. Crossfade switches where possible rather than cutting. Check that round-robin groups match in level, or the part will seem to swell and shrink. Treat articulation switching as part of playing, not as post-production repair.

## What to listen for

In the Irish tune, the difference in tone between legato and staccato; in the quartet's bowing changes, one pitch produced two ways; in the Debussy repeats, whether rotation removes the mechanical edge. Good sampled playing makes you forget it is sampled.

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["A4","A4","A4","A4","G4","F4","E4","D4"],"label":"Repeated notes with round robin","label_en":"Repeated notes with round robin","hint":"Four identical notes expose a single sample; round robin varies each attack slightly","hint_en":"Four identical notes expose a single sample; round robin varies each attack slightly"}
```
:::
