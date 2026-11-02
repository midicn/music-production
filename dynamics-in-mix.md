---
id: dynamics-in-mix
site: prod
cat: A6
title: 动态控制的目的
title_en: The Purpose of Dynamics Control
summary: 压缩不是为了更响，而是让段落之间的强弱关系站得住。
summary_en: Compression is not there to make things louder; it lets the contrast between sections hold together.
level: standard
tags: [混音, 动态, 压缩, 段落]
tags_en: [mixing, dynamics, compression, sections]
alias: [混音动态, 动态控制, mix dynamics]
links:
  - "[[glossary:compressor]]"
  - "[[glossary:parallel-compression]]"
  - "[[instrument:drum-kit]]"
  - "[[period:romantic]]"
instances:
  - musicnet-000069 | 室内乐乐句起伏的谱面参照，没有压缩前后两份音频（C1） | Scored chamber-music phrasing without two compression renders (C1)
  - oga-000004 | 高密度战斗曲编排参照，不证明波形动态被压平（C1） | A dense battle-music arrangement that does not establish compressed waveform dynamics (C1)
  - atepp-000369 | 钢琴强弱层次的音乐参照，可用于讨论段落对比（C1） | Piano dynamic contrasts for discussing sections (C1)
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook, dynamic control and bus compression.
  - David Gibson, The Art of Mixing, energy and section contrast.
updated: 2026-11-02
---

::: zh
## 问题

每轨都挂压缩，总线再加限制器，副歌确实更响了，却和主歌一样平。鼓的起音被削掉，人声一直贴在前景，听众找不到可以呼吸的地方。动态被当成了需要消灭的东西。

## 目标与判断

先决定段落希望怎样变化：更强的演奏、更多声部、更亮音区和更高电平是不同手段。短时响度可帮助记录差异，但没有所有主副歌都必须相差两到四dB的规定。也可通过收窄伴奏或减少前景声部，让后一个段落显得更展开。

## 做法

先用编曲和自动化建立段落关系，再只处理需要稳定或塑形的声部。加入压缩前后匹配响度，检查主线、音头和安静细节；不必给每轨规定衰减量。若并行处理增加了不想要的房间声或抽吸，应重新调整路径或不用它。

## 听什么

在同一工程中比较版本，先听主歌到副歌的关系，再把两版匹配整体响度，判断是否只是更响。安静部分的细节变化要用实际音频确认，不能从四个合成音符推断整首歌的压缩效果。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"音头与持续部分","label_en":"Attacks and sustained sound","hint":"这里呈现固定音符与力度，没有实际压缩。对照动态处理需使用同一音频并匹配响度。","hint_en":"These are fixed notes and velocities without compression. Compare dynamic processing using the same audio at matched loudness."}
```

## 常见误解

以为压缩越多越专业；以为响度就是能量；以为每一条轨都必须压缩。
:::

::: en
## The problem

Compress every track, add a limiter on the bus, and the chorus does get louder, yet it feels as flat as the verse. Drum attacks are shaved off, the vocal stays pinned in front, and listeners find nowhere to breathe. Dynamics have been treated as something to eliminate.

## Goal and judgement

Decide how sections should differ: stronger performance, additional parts, brighter register and higher level are different tools. Short-term loudness can log differences, but no universal verse-to-chorus dB gap applies. Reducing accompaniment or foreground activity earlier can also make a later section feel more open.

## Method

Establish sectional relationships with arrangement and automation, then process only parts needing control or shaping. Match loudness around compression and check the lead, attacks and quiet detail rather than assigning reduction to every track. If parallel processing adds unwanted ambience or pumping, adjust the route or omit it.

## What to listen for

Compare versions of the same session: hear the sectional relationship, then match overall loudness to distinguish improvement from simple level increase. Verify quiet-detail changes in actual audio rather than inferring a whole mix’s compression from four synthesized notes.

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"Attacks and sustained sound","label_en":"Attacks and sustained sound","hint":"These are fixed notes and velocities without compression. Compare dynamic processing using the same audio at matched loudness.","hint_en":"These are fixed notes and velocities without compression. Compare dynamic processing using the same audio at matched loudness."}
```

## Common misconceptions

That more compression sounds more professional; that loudness equals energy; that every track needs a compressor.
:::
