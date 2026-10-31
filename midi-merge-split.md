---
id: midi-merge-split
site: prod
cat: B1
title: MIDI 合并与拆分
title_en: Merging and Splitting MIDI
summary: 合并丢的是轨道名与通道分配，拆分要先定通道再定轨道。
summary_en: Merging loses track names and channel assignments, so split by channel before rebuilding tracks.
level: standard
tags: [MIDI, 轨道, 通道, 编辑]
tags_en: [MIDI, tracks, channels, editing]
alias: [MIDI 合并, MIDI 拆分, 轨道合并, 通道拆分, midi merge, midi split]
order: 340
links:
  - "[[glossary:midi-protocol]]"
  - "[[glossary:velocity]]"
  - "[[instrument:drum-kit]]"
instances:
  - oga-000025 | 十六个通道各有名字，钢琴、吉他、贝斯、小号、弦乐分列，合并前能一眼看到归属 | Sixteen named channels covering piano, guitars, bass, trumpet and strings
  - oga-000297 | 格式 0 的单轨文件，五个通道共 1081 个音符，拆分只能按通道抽 | A format 0 file with five channels and 1081 notes in one track
  - pdmx-000007 | 莫扎特《第四十交响曲》，十一条轨与十五个通道并存，轨名写乐器，通道数却多过轨数 | Mozart's Fortieth Symphony, eleven tracks against fifteen channels, with more channels than tracks
  - pdmx-000068 | 巴赫《三架羽管键琴协奏曲》，十条轨只落在五个通道上 | Bach's triple harpsichord concerto, ten tracks collapsed onto five channels
sources:
  - MIDI 1.0 Detailed Specification, MMA, 通道消息与轨道块的定义
  - Apple Logic Pro User Guide, MIDI 编辑与合并操作
  - Ableton Live Reference Manual, MIDI 轨道与片段
updated: 2026-10-31
---

::: zh
把钢琴左右手两条轨合并成一条，再拆开时，踏板曲线常常只剩一条，另一只手的位置全丢了。

## 合并时丢的是什么

音符、时值、力度都还在，丢的是轨道名、通道分配、端口和控制器归属。两条轨原本各走一个通道，合并后如果都落到通道 1，两个音色切换会互相覆盖，只剩最后一个生效。鼓轨更明显：[[instrument:drum-kit|鼓组]]的键号一旦从打击通道换到旋律通道，整套鼓就变成一串音高。

## 轨道、通道、端口

轨道是文件里的容器，通道是消息里的四位地址，端口是软件之间的虚拟线。一个轨道可以写多个通道，一个通道也可以跨轨道。合并通常按轨道走，拆分却常按通道走，信息就是在这里丢的。

| 概念 | 范围 | 合并时 | 拆分时 |
|---|---|---|---|
| 轨道 | 文件内任意条 | 名字与顺序会合并 | 需要重新命名 |
| 通道 | 每端口十六个 | 同号通道互相覆盖 | 按通道拆分最稳 |
| 端口 | 软件虚拟端口 | 常被忽略 | 多端口要分别处理 |
| 控制器 | 绑定通道 | CC 只跟一个通道 | 拆分前先复制 |

## 什么时候该合并

鼓的多支麦克风、同一条线的八度加倍、分段录的 comping，都适合并成一条。合并后检查通道号、第一个音色切换和 CC 的位置。需要保留演奏细节时，先复制一份再合并，原件留着对照。合并之前先确认这条轨不再需要分开编辑。

## 拆分怎么不丢

先按通道拆，再按音高拆。拆之前把延音踏板、表情和弯音复制到每条新轨，拆之后逐个确认开头有没有音色切换。名字要重写，不要留下 Track 1 copy 这种默认名。格式 0 的文件只有一条轨，拆分等于把[[glossary:midi-protocol|通道]]一条条抽出来，抽完要重新存成格式 1。

## 失败模式

两条轨落到同一个通道号，音符就会叠在一起，[[glossary:velocity|力度]]也乱了；鼓轨与旋律轨合并，键号越界；拆分时只拆音符不拆 CC，踏板全留在原轨；轨道名重复，混音时找不到对应的乐器。合并前先存一版，比事后猜更省时间。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5","G4"],"label":"合并后的一条钢琴轨","label_en":"One piano track after a merge","hint":"这些音原本可能分属两只手，合并后只剩一条轨，踏板也只能跟一条","hint_en":"These notes may have come from two hands; after the merge there is one track and one pedal line"}
```
:::

::: en
Merge the two piano tracks into one, split them again, and the sustain pedal is often a single curve while one hand has lost its place.

## What a merge loses

Notes, lengths and velocities survive. Track names, channel assignments, ports and controller ownership do not. If two tracks that used separate channels both land on channel 1, their program changes overwrite each other and only the last one applies. Drums make it obvious: move a drum part off the percussion channel and the kit turns into a row of pitches.

## Tracks, channels, ports

A track is a container in the file, a channel is the four-bit address inside a message, and a port is a virtual cable between programs. One track can carry several channels, and one channel can span tracks. Merging usually works by track, while splitting usually works by channel, which is exactly where information disappears.

| Idea | Scope | On merge | On split |
|---|---|---|---|
| Track | Any number per file | Names and order collapse | Rename afterwards |
| Channel | Sixteen per port | Same number overwrites | Split by channel first |
| Port | Virtual cable | Often ignored | Handle each port separately |
| Controller | Bound to a channel | CC follows one channel only | Copy before splitting |

## When to merge

Multiple drum microphones, octave doublings and comped takes all belong on one track. After merging, check channel numbers, the first program change and the position of the CC data. If performance detail matters, duplicate before merging and keep the original for comparison. Confirm the track no longer needs separate editing before merging it.

## Splitting without loss

Split by channel first, then by pitch. Before splitting, copy sustain, expression and pitch bend onto every new track, then confirm each one starts with the right program. Rename everything instead of leaving Track 1 copy in place. A format 0 file has one track, so splitting means pulling channels out one by one and saving the result as format 1.

## Failure modes

Two tracks land on the same channel number, so notes pile up and velocities scramble. A drum track merges with a melody and the keys fall outside the drum map. Only notes are split, so the pedal stays behind on the original track. Track names repeat and the mixer no longer shows which instrument is which. Save a copy before merging; guessing afterwards costs more time.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "C5", "G4"], "label": "One piano track after a merge", "label_en": "One piano track after a merge", "hint": "These notes may have come from two hands; after the merge there is one track and one pedal line", "hint_en": "These notes may have come from two hands; after the merge there is one track and one pedal line"}
```
:::
