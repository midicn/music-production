---
id: score-to-midi-export
site: prod
cat: B6
title: 从乐谱导出 MIDI
title_en: Exporting MIDI from a Score
summary: 乐谱导出 MIDI 时，时值、力度与表情会被折成离散事件。
summary_en: Exporting a score to MIDI turns durations, dynamics and expression into discrete events.
level: standard
tags: [MIDI, 导出, 乐谱, 回放]
tags_en: [MIDI, export, score, playback]
alias: [从乐谱导出 MIDI, 乐谱导出, 谱面转 MIDI, score to MIDI, MIDI export]
links:
  - "[[glossary:midi-protocol]]"
  - "[[glossary:tempo]]"
  - "[[glossary:velocity]]"
  - "[[glossary:rubato]]"
instances:
  - atepp-000369 | 自由速度的夜曲，导出后最能听出量化抹掉了多少呼吸
  - m21-000000 | 四声部众赞歌节拍规整，适合检查和弦是否被导齐
  - oga-000045 | 配乐中间有速度变化，可对照速度事件是否写进文件
  - atepp-001875 | 三声部创意曲的连奏与断奏，导出后容易变成同一种音头
sources:
  - MIDI 1.0 规范中音符、速度与控制器消息的定义（MMA 公开规范）。
  - 制谱软件导出 MIDI 的反复、装饰音与力度选项，参考公开文档。
updated: 2026-10-28
---

::: zh
谱面写的是记号，MIDI 要的是时间、音高与力度。导出就是把连续的表情折成离散事件。

## 为什么会用到

作曲家在谱上写渐强、延长记号与自由速度，回放却只有固定的拍点与有限的力度级。导出设置不同，同一份谱会得到完全不同的 MIDI。

## 它怎么运转

每个音变成 Note On 与 Note Off，时值换算成 tick；速度记号写成 tempo 事件；力度记号映射成 velocity；连奏、踏板与颤音写成控制器。装饰音被分配极短时值，颤音有时被展开，反复记号按设置决定展开次数。量化会把演奏的微小偏移吸到网格上。

## 做法与判断

导出前确认反复是否展开、速度曲线是否写入、装饰音如何分配。到 DAW 里检查第一个音是否落在拍点、尾音是否被截断、和弦是否齐。需要保留演奏感时，把原始演奏轨单独留一份，不要让量化覆盖它。

## 耳朵要抓的点

听和弦是否同时到达，长音是否被下一个音切掉，渐强是否变成一级一级的台阶。再听自由速度段落，判断导出后是否还剩呼吸。

## 容易弄错的

MIDI 能保留所有记号；音色选对就等于还原；量化越细越忠实。事实正相反，量化越细，越容易把分句磨平。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["G4","F4","E4","D4","C4"],"label":"一条下行旋律，听它的音头","label_en":"A descending line, hear each attack","hint":"先听每个音是否一样重，再想象导出后力度被压成几个固定档","hint_en":"Hear whether every note has the same weight, then imagine velocity reduced to a few fixed levels"}
```
:::

::: en
A score carries signs; MIDI carries time, pitch and velocity. Export folds continuous expression into discrete events.

## Why you reach for it

Composers write crescendos, fermatas and rubato, but playback offers fixed beats and a limited set of velocity levels. Different export settings turn one score into very different MIDI.

## How it runs

Each note becomes Note On and Note Off, with duration in ticks. Tempo marks become tempo events; dynamics map to velocity; legato, pedals and trills become controller data. Grace notes receive very short durations, trills may be written out, and repeats may export once. Quantisation snaps small timing offsets to the grid.

## Practice and judgement

Before export, decide whether repeats unfold, whether the tempo curve is written and how grace notes divide time. In the DAW, check the first attack, truncated tails and chord alignment. Keep the original performance take when feel matters.

## What the ear catches

Hear whether chords arrive together, whether long notes are cut and whether a crescendo becomes a staircase. Then hear a rubato passage and ask whether any breath remains.

## Easy to get wrong

MIDI keeps every mark; the right sound equals a faithful rendering; finer quantisation is more faithful. The opposite is common, because finer grids flatten phrasing.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["G4", "F4", "E4", "D4", "C4"], "label": "A descending line, hear each attack", "label_en": "A descending line, hear each attack", "hint": "先听每个音是否一样重，再想象导出后力度被压成几个固定档", "hint_en": "Hear whether every note has the same weight, then imagine velocity reduced to a few fixed levels"}
```
:::
