---
id: ai-notation-transcription
site: prod
cat: B7
title: AI 记谱与转写
title_en: AI Transcription and Scoring
summary: AI 记谱把演奏或音频转成谱面，量化与分句是主要误差来源。
summary_en: AI transcription turns a performance or audio into notation, with quantisation and phrasing as the main error sources.
level: standard
tags: [AI, 记谱, 转写, 扒谱]
tags_en: [AI, notation, transcription, scoring]
alias: [AI 记谱与转写, 自动记谱, 音频转谱, AI transcription, automatic transcription]
links:
  - "[[glossary:score]]"
  - "[[glossary:rubato]]"
  - "[[glossary:velocity]]"
  - "[[glossary:midi-protocol]]"
instances:
  - atepp-000369 | 自由速度的夜曲，最能检验转写会不会把呼吸压成网格
  - atepp-000075 | 钢琴奏鸣曲音区宽、踏板多，复调与和声都难分
  - m21-000000 | 四声部众赞歌起音整齐，是转写最容易成功的对照
  - oga-000052 | 多层游戏配乐，声部多且音色接近，适合看分声部的误差
sources:
  - 自动音乐转写的音高、起音与量化流程，依公开论文核查，未抄文本
  - 乐谱语义与 MusicXML 交换格式，依公开规范核查，未抄文本
updated: 2026-10-28
---

::: zh
把一段演奏变成谱面，要同时判断音高、起音、拍子与分句。每一项都有歧义，模型只是把歧义摆到明面上。

## 问题

演奏不会严格落在网格上，和弦会滚开，踏板会让和声重叠。自动转写若只抓音高，谱面就会布满奇怪的时值。

## 原理或流程

音频转写先做音高检测与起音检测，再量化到网格，最后分配声部与节奏。复调与踏板是难点，因为同一时刻有多个音，且它们未必属于同一个声部。符号转写则从 MIDI 推断拍号、调号与分句。模型给出候选，拍点与声部仍要人工确认。

## 做法与判断

先定拍号与速度，再转写。单声部先用单音模型，复调再分声部。检查装饰音是否被写成正规时值、跨小节连线是否断开、休止符是否被填满。用慢速回放对照，导出 MusicXML 后在制谱软件里修。

## 听什么

听转写后的重音是否与演奏一致，长音是否被切成多个音，踏板是否让和声变浑。再听休止，真正的气口常被模型填成延音。

## 常见误解

转写等于扒谱；音高对就够；自动量化能替代拍点判断。谱面读得顺不顺，取决于分句，不取决于音高数量。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["E4","G4","B4","D5","B4","G4","E4"],"label":"一串带踏板的和弦，听音与音怎样叠","label_en":"Pedalled chords, hear how the notes overlap","hint":"听上一个和弦的尾音有没有留到下一个，再想转写该把它写成延音还是休止","hint_en":"Hear whether the previous chord rings into the next, then decide whether notation should show a tie or a rest"}
```
:::

::: en
Turning a performance into notation means judging pitch, onset, metre and phrasing at once. Every judgement is ambiguous; a model simply makes the ambiguity visible.

## The problem

Performances do not sit on the grid. Chords roll, and the pedal overlaps harmony. A transcription that tracks only pitch produces strange durations.

## How it works

Audio transcription detects pitch and onsets, quantises to a grid, then assigns voices and rhythm. Polyphony and pedalling are hard because several notes sound at once and need not belong to one voice. Symbolic transcription infers metre, key and phrasing from MIDI. The model proposes; beats and voices still need confirmation.

## Practice and judgement

Set metre and tempo before transcribing. Use a monophonic model first, then split voices. Check whether grace notes became full values, ties break across systems and rests are filled. Compare at slow playback, then export MusicXML and correct in notation software.

## What to listen for

Hear whether accents match the performance, long notes split into several and pedalling muddies harmony. Then hear the rests; real breaths are filled with sustain.

## Common misunderstandings

Transcription is copying a record; correct pitch is enough; automatic quantisation replaces beat judgement. Readability comes from phrasing, not note count.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["E4", "G4", "B4", "D5", "B4", "G4", "E4"], "label": "Pedalled chords, hear how the notes overlap", "label_en": "Pedalled chords, hear how the notes overlap", "hint": "听上一个和弦的尾音有没有留到下一个，再想转写该把它写成延音还是休止", "hint_en": "Hear whether the previous chord rings into the next, then decide whether notation should show a tie or a rest"}
```
:::
