---
id: gm-drum-map
site: prod
cat: B1
title: GM 鼓映射
title_en: GM Drum Map
summary: 第 10 通道的每个键号对应一件打击乐器，与音色号无关。
summary_en: On channel 10 each key number is a percussion instrument, and the program number has no say.
level: standard
tags: [MIDI, GM, 鼓, 键号]
tags_en: [MIDI, GM, drums, key number]
alias: [GM 鼓表, 鼓映射, 鼓键号, drum map]
links:
  - "[[instrument:drum-kit]]"
  - "[[glossary:midi-protocol]]"
  - "[[glossary:velocity]]"
instances:
  - groove-000007 | 闭镲 42 出现 128 次，底鼓 36 与军鼓 38 清晰可数
  - groove-000000 | 除 42、36、38 外还用了 22 键，后者不在 GM 鼓表里
  - oga-000013 | 底鼓 36 有 164 次，踩镲 44 有 83 次，闭镲 42 有 54 次
sources:
  - 通用 MIDI 规范对打击通道与键号的映射，依 MMA 公开规范核查，未抄文本
  - 本库鼓轨的键号统计，由本地 SMF 解析脚本核对，数值随文件而定
updated: 2026-10-28
---

::: zh
在鼓通道上，键号就是乐器名。写旋律的习惯到了这里要换一套。

## 问题

鼓没有音高，键号差一个，军鼓可能变成通鼓；把鼓写到别的通道，整套节奏会变成钢琴。

## 协议或消息

GM 把第 10 通道固定为鼓组，键号 35 到 81 各对应一件打击乐器。36 底鼓、38 军鼓、42 闭镲、46 开镲、49 吊镲、51 叮叮镲、39 拍手、37 边击。音源收到 Note On 就触发采样，通常忽略 Note Off。键号 22 一类不在 GM 表内，只出现在某些硬件的私有映射里。CC4 常用来控制踩镲踏板。

## 参数与做法

写鼓固定用第 10 通道。用键号而不是音名。闭镲与开镲不要写在同一时刻。力度分层决定军鼓的手感。底鼓与贝斯留出频段。同一键号在不同鼓音源上的音色可能不同，但语义不变。

## 听什么

42 与 46 的差别在尾音长短；36 与 35 的低频厚度不同；错一个键号，节奏型会立刻含糊。

## 常见误解

鼓通道也能写旋律，只是音源会按鼓键解释。第 10 通道不是第十轨。Note Off 对鼓通常没有意义。

```audiolab
{"type":"instrument","drum":"36","phrase":["36","38","42","36","38","46"],"label":"底鼓、军鼓、闭镲与开镲","label_en":"Kick, snare, closed and open hat","hint":"听闭镲 42 与开镲 46 的尾音长短","hint_en":"Compare the tail length of closed hat 42 and open hat 46"}
```
:::

::: en
On the drum channel, a key number is an instrument name. Habit from melodic writing has to change here.

## The problem

Drums have no pitch, so one key off turns a snare into a tom, and a drum part sent to another channel becomes a piano line.

## Protocol or message

GM fixes channel 10 as drums, with keys 35 to 81 mapped to percussion. 36 is kick, 38 snare, 42 closed hat, 46 open hat, 49 crash, 51 ride, 39 clap and 37 side stick. An instrument triggers its sample on Note On and usually ignores Note Off. Keys such as 22 sit outside the GM table and appear only in private hardware maps. CC4 often controls the hi-hat pedal.

## Settings and practice

Always write drums on channel 10. Use key numbers rather than note names. Do not place closed and open hats at the same instant. Velocity layers shape the snare. Leave room for kick and bass in the spectrum.

## What to listen for

Closed hat 42 and open hat 46 differ in tail length. Kick 36 and 35 differ in low-end weight. One wrong key makes a pattern muddy at once.

## Common misunderstandings

The drum channel can hold melody, but the instrument reads it as drum keys. Channel 10 is not the tenth track. Note Off rarely matters for drums.

```audiolab
{"type": "instrument", "drum": "36", "phrase": ["36", "38", "42", "36", "38", "46"], "label": "Kick, snare, closed and open hat", "label_en": "Kick, snare, closed and open hat", "hint": "听闭镲 42 与开镲 46 的尾音长短", "hint_en": "Compare the tail length of closed hat 42 and open hat 46"}
```
:::
