---
id: symbolic-music-generation
site: prod
cat: B7
title: 符号域生成
title_en: Symbolic Music Generation
summary: 符号域生成在音符与事件层面建模，输出可编辑的 MIDI 或乐谱。
summary_en: Symbolic generation models notes and events, producing editable MIDI or notation.
level: standard
tags: [AI, 符号音乐, MIDI, 生成]
tags_en: [AI, symbolic music, MIDI, generation]
alias: [符号域生成, MIDI 生成, 符号音乐生成, symbolic generation, MIDI generation]
links:
  - "[[glossary:midi-protocol]]"
  - "[[glossary:score]]"
  - "[[glossary:counterpoint]]"
  - "[[glossary:motive]]"
instances:
  - m21-000000 | 四声部众赞歌的和声语法清楚，适合看模型是否守住声部规则
  - atepp-001875 | 三声部创意曲靠动机追逐展开，最能检验生成有没有方向
  - thesession-000001 | 爱尔兰吉格舞曲的变体传统，说明同一动机可以怎样改写
  - atepp-000238 | 肖斯塔科维奇的前奏与赋格，复调密度高，适合压力测试
sources:
  - 符号音乐表示与 token 化方法的公开研究，参考ISMIR 论文。
  - 音乐生成评估中和声、动机与节奏的常用判据；公开论文是主要依据。
updated: 2026-10-28
---

::: zh
符号域生成不碰波形，它把音高、时值与力度当作词，学着写出下一串。

## 卡住的地方

音频生成难以只改一个音，符号生成可以；但模型写出的声部常缺少方向，听起来像练习曲。

## 它怎么运转

把 MIDI 切成 token，音高、时值、力度分别编码，用 Transformer 或扩散模型学上下文。条件可以是风格、和弦进行、动机或段落标记。生成长度受上下文窗口限制，长曲需要分段续写，段与段的接缝要单独处理。

## 做法与判断

先给和弦骨架或一个动机，再让模型续写。限制音域与复调数量，生成多条取长补短。到 DAW 里改力度、连奏与配器，保留种子与参数以便复现。判断一段生成是否可用，看它有没有终止式、低音是否只是根音重复、内声部有没有独立走向。

## 耳朵要抓的点

听乐句在哪里呼吸，终止式是否解决，动机有没有在下一次出现时变形。再听低音，如果它只会踩根音，和声就站不住。

## 容易弄错的

符号生成等于作曲；数据越多越好；输出 MIDI 就不用修。模型给的是素材，分句与配器仍要人来定。

```audiolab
{"type":"instrument","gm":"Harpsichord","synth":"plucked","phrase":["C4","E4","G4","C5","G4","E4","C4"],"label":"一个可被模仿的动机","label_en":"A motif that invites imitation","hint":"听完这段，试着在心里接一句相似的答句，再想模型会不会只换音高不换节奏","hint_en":"After the phrase, imagine a matching answer, then ask whether a model would change pitch but keep the rhythm"}
```
:::

::: en
Symbolic generation never touches a waveform. It treats pitch, duration and velocity as words and learns to write the next string.

## Where it snags

Audio generation cannot easily change one note; symbolic generation can. Yet the voices a model writes lack direction and sound like studies.

## How it runs

MIDI becomes tokens, with pitch, duration and velocity encoded separately, and a Transformer or diffusion model learns context. Conditions can be style, chord progression, motif or section markers. Length is limited by the context window, so long pieces need continuation and careful seams.

## Practice and judgement

Supply a chord skeleton or motif, then let the model continue. Limit range and polyphony, generate several takes and combine. Edit velocity, legato and orchestration in the DAW, and keep seeds and settings for reproduction. Judge a take by cadences, a bass that does more than repeat roots, and inner voices with their own motion.

## What the ear catches

Hear where phrases breathe, whether cadences resolve and whether the motif changes on return. Then hear the bass; if it only stamps roots, the harmony cannot stand.

## Easy to get wrong

Symbolic generation is composition; more data is always better; MIDI output needs no editing. The model supplies material; phrasing and orchestration remain human decisions.

```audiolab
{"type": "instrument", "gm": "Harpsichord", "synth": "plucked", "phrase": ["C4", "E4", "G4", "C5", "G4", "E4", "C4"], "label": "A motif that invites imitation", "label_en": "A motif that invites imitation", "hint": "听完这段，试着在心里接一句相似的答句，再想模型会不会只换音高不换节奏", "hint_en": "After the phrase, imagine a matching answer, then ask whether a model would change pitch but keep the rhythm"}
```
:::
