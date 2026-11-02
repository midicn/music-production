---
id: volume-balance
site: prod
cat: A6
title: 音量平衡
title_en: Level Balance
summary: 确定声部前后关系，用可重复的对照调整静态平衡与段落变化
summary_en: Set the relationship between parts and compare static balance and section changes
level: standard
tags: [混音, 音量, 平衡, 推子]
tags_en: [mixing, level, balance, faders]
alias: [音量平衡, 推子, 静态平衡, volume balance, fader]
links:
  - "[[glossary:bus]]"
  - "[[glossary:automation]]"
  - "[[instrument:voice]]"
  - "[[instrument:drum-kit]]"
instances:
  - openscore-000008 | 舒伯特《魔王》的谱面参照，声部可在工程中另行分配 | Score reference for Schubert’s Erlkönig; parts can be assigned separately in a session
  - oga-000000 | 游戏音乐素材参照，不预设其轨道数或混音平衡 | Game-music material without an assumed track count or mix balance
  - groove-000002 | 鼓组 MIDI 参照，可在自己的鼓音源中调整各件关系 | Drum MIDI for testing relative instrument levels in your own drum source
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook, fader balance chapter.
  - David Gibson, The Art of Mixing, visual mapping of level and pan.
updated: 2026-11-02
---

::: zh
## 先确定谁是前景

音量平衡安排各声部在不同段落中的相对位置。没有固定的“占混音八成”比例，也不要求每个声部始终同样清楚。先明确该段落要听见的旋律、节奏与低音，再决定哪些材料需要突出。

## 建立一版静态平衡

先关闭会明显改变响度的处理，降低监听音量，并为总线留出余量。选择编制较完整的一段，依次加入声部；每加入一轨，判断它承担的功能，而不是只听单轨是否好听。

随后检查较稀疏的段落和段落转换。副歌合适的平衡未必适合主歌；可以用自动化调整，而不必整首共用一个推子位置。若某个声部被遮住，分别检查音量、音区、时机、声像与音色，不以“需要提高 6 dB”作为某类问题的诊断标准。

## 一个可重复的比较

保留当前平衡作为版本 A，只改变一个关系，例如主旋律相对伴奏提高一点，保存为版本 B。尽量匹配两版的整体响度，交替听相同位置，记录主线是否更清楚，以及其他声部是否被压住。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","E3","G3","C4","G3","E3"],"label":"短句参照","label_en":"Short-phrase reference","hint":"听音符的强弱与连接；声部平衡要在可独立调节的工程轨道中比较。","hint_en":"Hear dynamics and connections; compare balance using separately adjustable session parts."}
```

这个短句只播放一个音色，没有独立的旋律/伴奏推子。要做平衡实验，应在工程里准备可独立调节的声部，再进行上述对照。

## 判断结果

在整段音乐中检查句头、持续音和句尾，注意低音是否掩盖节奏、人声空隙是否让伴奏突然突出。换一档合理的监听音量复核，但不要只把总线衰减某个固定值就认定完成了响度匹配。

音量平衡不能代替编曲、均衡或动态处理；这些手段也不应代替先把声部关系听清楚。
:::

::: en
## Establish the foreground

Level balance sets the relative position of parts across a piece. No fixed percentage of mixing is achieved by faders alone, and every part need not remain equally prominent. Identify the melody, rhythm and bass that matter in the section before deciding what should lead.

## Building a static balance

Begin without processing that substantially changes loudness, use a moderate monitoring level and leave bus headroom. Choose a fuller section and add parts in turn, judging each function in the ensemble rather than its solo sound alone.

Check sparser sections and transitions afterwards. A chorus balance may not suit a verse; automation can change it instead of retaining one fader setting throughout. For masking, examine level, register, timing, pan and timbre separately. A need for 6 dB more gain is not a universal diagnosis.

## A repeatable comparison

Save the current balance as A. Change one relationship, such as a small increase of melody relative to accompaniment, and save B. Match overall loudness as closely as practical, alternate the same passage, and note both improved clarity and any newly obscured parts.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","E3","G3","C4","G3","E3"],"label":"短句参照","label_en":"Short-phrase reference","hint":"听音符的强弱与连接；声部平衡要在可独立调节的工程轨道中比较。","hint_en":"Hear dynamics and connections; compare balance using separately adjustable session parts."}
```

This phrase uses one timbre and provides no independent melody and accompaniment faders. A balance experiment requires separately adjustable parts in a production session.

## Judging the result

Check phrase onsets, sustained notes and endings in context. Notice whether bass masks rhythmic detail or accompaniment jumps forward between vocal phrases. Recheck at another reasonable monitoring level; a fixed reduction of the master is not by itself loudness matching.

Balance does not replace arrangement, EQ or dynamics processing. Those tools likewise do not replace listening to the basic relationships between parts.
:::
