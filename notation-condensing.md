---
id: notation-condensing
site: prod
cat: B6
title: 总谱缩编
title_en: Condensing a Full Score
summary: 缩编是给眼睛看的版本，分谱与力度仍要逐行还原。
summary_en: A condensed score is a reading view; parts, dynamics and cues still have to be unfolded line by line.
level: standard
tags: [记谱, 总谱, 缩编, 分谱]
tags_en: [notation, full score, condensing, parts]
alias: [总谱缩编, 缩编谱, condensing, condensed score]
order: 513
links:
  - "[[glossary:full-score]]"
  - "[[glossary:short-score]]"
  - "[[glossary:doubling]]"
  - "[[glossary:part]]"
  - "[[glossary:rehearsal-mark]]"
instances:
  - pdmx-000007 | 莫扎特《第四十交响曲》，长笛、双簧管、单簧管、巴松与圆号各占一轨，弦乐五部另起五行 | Mozart's Fortieth, flute, oboes, clarinet, bassoon and horns on separate tracks, five string lines beside them
  - mutopia-000497 | 贝多芬第五第一乐章，12 条轨按 one 到 twelve 编号，木管四支、圆号两支与弦乐五部各占一行 | Beethoven's Fifth, first movement, twelve tracks named one to twelve, four winds, two horns and five strings kept apart
  - oga-000052 | 游戏配乐《exploring the halls》除鼓组外有 8 条乐器轨，其中四条同为 Synth Strings 2，缩编时按功能并成两行 | A game cue with eight instrument tracks besides drums, four of them on the same Synth Strings 2 patch, where folding begins
sources:
  - Dorico 官方文档的 Condensing 章节，缩编组、分裂与合并规则
  - Samuel Adler, The Study of Orchestration, W. W. Norton，木管与铜管的加倍写法
  - Elaine Gould, Behind Bars, Faber Music，总谱布局与分谱标记
updated: 2026-10-31
---

::: zh
把四支圆号压成两行，指挥看得更清楚，圆号手却可能不知道哪一行是自己。缩编解决的是阅读，不是省纸。

## 缩编给谁看

缩编总谱主要给指挥、作曲者与排练用：一眼看到声部关系、和声密度与进入顺序。录音与出版仍用完整总谱，每个演奏员一行，力度、换乐器与休止都写清楚。缩编是显示层，底下的分谱与源文件不动。把缩编谱发给演奏员，等于让每个人猜自己属于哪一声部。

## 哪些行能并

能并的前提是节奏相同或互补，并且两台乐器在同一段里不需要各自的力度。木管两支一行最常见，铜管按 1/2 与 3/4 分两行，弦乐分奏不并。

| 组 | 常见缩法 | 前提 | 丢了什么 |
|---|---|---|---|
| 长笛 1/2 | 一行，符干分上下 | 节奏一致 | 各自的呼吸与力度 |
| 双簧管 1/2 | 一行，标 a2 | 节奏一致 | 音色差别 |
| 单簧管 B♭ 与 A | 一行，换乐器处注明 | 移调已处理 | 换乐器的间隙 |
| 巴松 1/2 | 一行 | 低音区分奏少 | 低音独立线 |
| 圆号 1 到 4 | 两行，1/2 与 3/4 | 分组固定 | 四支各自的力度 |
| 小号 1 到 3 | 一行或两行 | 换弱音器处拆开 | 弱音器切换 |
| 长号 1/2 与低音长号 | 两行，低音长号单列 | 低音长号有独立声部 | 合并后的低音走向 |
| 弦乐分奏 | 不并，按 div. 展开 | 分奏段 | 并了会被读成齐奏 |

## 标记与分谱

缩编行里的力度要么写两份，要么写成 1. 强 2. 弱；两支吹同一句标 a2，只有一支时标 1. 或 solo。换乐器、加弱音器、分奏与合奏都要在行首写清。分谱从缩编总谱导出时逐行还原，提示音符与排练号跟着声部走。圆号 3 与 4 写在同一行时，用符干方向区分，别让一支替另一支让位。

## 哪里会坏

节奏不同的声部硬并，看起来像一个人吹，实际要两个人，排练才发现。缩编后丢了提示音符，演奏员在长休止里数错小节。软件的自动缩编遇到声部交叉、换乐器或一方休止，会反复分合，需要手动锁死。页面少了，信息密度反而更高，翻页更急。拿缩编谱进录音棚，平衡与力度全凭猜。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["G3","B3","D4","D4"],"label":"两个声部落到同一个音，缩编后只画一个音头","label_en":"Two parts land on the same pitch, drawn as one note head after condensing","hint":"听最后两个音重合，再想这一处在谱上标 a2 还是只写一个音","hint_en":"Hear the last two notes merge, then decide whether the page says a2 or just one note"}
```
:::

::: en
Put four horns on two staves and the conductor reads faster, while the horn players may no longer recognise their own line. Condensing serves reading, not paper.

## Who reads it

A condensed score serves the conductor, the composer and the rehearsal: voice leading, harmonic density and the order of entries at a glance. Recording and publication keep the full score, one staff per player, with dynamics, instrument changes and rests spelled out. Condensing is a view; the parts and the source file stay untouched. Hand a condensed score to a player and you ask each one to guess their own line.

## Which staves can merge

Merging works when the rhythms match or interlock and neither instrument needs its own dynamic in that passage. Two woodwinds share a staff most often, horns split 1/2 and 3/4, and divisi strings stay open.

| Group | Usual fold | Condition | What is lost |
|---|---|---|---|
| Flutes 1/2 | One staff, stems up and down | Same rhythm | Separate breaths and dynamics |
| Oboes 1/2 | One staff marked a2 | Same rhythm | Timbre difference |
| Clarinets B♭ and A | One staff, change noted | Transposition handled | The gap for the swap |
| Bassoons 1/2 | One staff | Little low divisi | Independent bass line |
| Horns 1 to 4 | Two staves, 1/2 and 3/4 | Fixed pairing | Four separate dynamics |
| Trumpets 1 to 3 | One or two staves | Split at mute changes | Mute changes |
| Trombones 1/2 plus bass | Two staves, bass separate | Bass has its own line | The merged bass motion |
| Divisi strings | Do not fold, expand | Divisi passage | Folded, it reads as unison |

## Marks travel with the staff

Dynamics on a folded staff are printed twice or written as 1. loud 2. soft. Two players on one phrase take a2; one player takes 1. or solo. Instrument changes, mutes, divisi and tutti belong at the start of the line. Extracting parts unfolds every fold, and cue notes and rehearsal marks follow the voice. Horns 3 and 4 on one staff need opposing stems so one does not yield to the other.

## Where it breaks

Fold parts with different rhythms and the page looks like one player while the music needs two; the rehearsal finds out. Lose the cue notes and a player miscounts bars of rest. Automatic condensing splits and recombines around voice crossings, instrument changes and one-sided rests unless you lock it. Fewer pages raise the density, so page turns get harder. Take a condensed score into a session and balance becomes guesswork.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["G3", "B3", "D4", "D4"], "label": "Two parts settle on one pitch and share a line after condensing", "label_en": "Two parts settle on one pitch and share a line after condensing", "hint": "Hear the last two notes merge, then decide whether the page says a2 or just one note", "hint_en": "Hear the last two notes merge, then decide whether the page says a2 or just one note"}
```
:::
