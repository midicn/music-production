---
id: note-on-and-note-off
site: prod
cat: B1
title: Note On 与 Note Off
title_en: Note On and Note Off
summary: 音符的开始与结束是两条消息，收尾方式决定重叠音与鼓的时值。
summary_en: Note On starts a note and Note Off ends it, and the way it ends shapes overlaps and drum decay.
level: standard
tags: [MIDI, 音符, 力度, 事件]
tags_en: [MIDI, note, velocity, event]
alias: [音符开关, 音符结束, Note On, Note Off]
links:
  - "[[glossary:velocity]]"
  - "[[glossary:midi-protocol]]"
  - "[[instrument:piano]]"
instances:
  - musicnet-000265 | 钢琴四重奏，7702 条 Note Off 全写成力度 0 的 Note On
  - musicnet-000073 | 钢琴奏鸣曲，6615 条 Note Off 全用 0x80 写成，可与上一条对照
  - groove-000000 | 放克鼓循环，闭镲 42 键重复 101 次，靠 Note Off 切出长短
sources:
  - MIDI 1.0 规范对 Note On 与 Note Off 的定义，参考MMA 公开规范。
  - 力度 0 的旧约定与重叠音处理；音序器文档是主要依据。
updated: 2026-10-28
---

::: zh
一个音要两条消息才完整，开始一条，结束一条。收尾方式决定了断奏、连奏与鼓的时值。

## 问题

只发 Note On 会留下挂音，Note Off 发早了会截断尾音。重叠的同音更难处理，前一个音的结束消息可能把后一个音一起关掉。

## 协议或消息

Note On 用 0x9n 加键号与力度，Note Off 用 0x8n。力度为 0 的 Note On 按 Note Off 处理，这是省字节的旧约定。Note Off 自带的释放力度，多数音源并不读取。同一个键连续敲两次时，必须先结束前一个音，否则音源分不清哪条结束消息对应哪个音。文件里事件按 delta 排序，结束消息可以晚于下一个开始。

## 参数与做法

钢琴长音用 CC64 延音，不要靠拉长 Note Off。鼓通常忽略 Note Off，一次触发就放完整采样。写断奏时把结束提前，而不是把力度压低。

## 听什么

断奏与连奏的差别就在结束的时刻，提前二十毫秒就能听出干湿不同。重叠音被误关时，尾音会突然消失。

## 常见误解

Note Off 的释放力度不是音量。不是所有音源都接受力度 0 的写法。音符长度也不等于响度。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","C4","E4","G4"],"label":"重复音怎样收尾","label_en":"How a repeated note ends","hint":"听第二个 C4 进来时，前一个音是否被干净地关掉","hint_en":"When the second C4 arrives, hear whether the first one was closed cleanly"}
```
:::

::: en
Every note needs two messages, one to start and one to stop. How it stops decides staccato, legato and the length of a drum hit.

## The problem

A Note On without an end leaves a stuck note, while an early Note Off cuts the tail. Overlapping the same pitch is harder, since the first end may close the second.

## Protocol or message

Note On uses 0x9n with key and velocity, Note Off uses 0x8n. A Note On with velocity 0 counts as Note Off, an old byte-saving convention. Most instruments ignore the release velocity. When the same key repeats, the first note must end before the second starts, or the instrument cannot pair ends with starts. Events are ordered by delta time, so an end can follow the next start.

## Settings and practice

Hold piano notes with CC64 rather than a stretched Note Off. Drums usually ignore Note Off and play the whole sample after a trigger. For staccato, move the end earlier instead of lowering velocity.

## What to listen for

Staccato and legato differ at the moment of release, and twenty milliseconds changes what you hear. When an end closes the wrong note, the tail disappears.

## Common misunderstandings

Release velocity is not volume. Not every instrument accepts velocity 0 as Note Off. Note length is not loudness.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "C4", "E4", "G4"], "label": "How a repeated note ends", "label_en": "How a repeated note ends", "hint": "听第二个 C4 进来时，前一个音是否被干净地关掉", "hint_en": "When the second C4 arrives, hear whether the first one was closed cleanly"}
```
:::
