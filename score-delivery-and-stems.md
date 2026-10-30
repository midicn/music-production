---
id: score-delivery-and-stems
site: prod
cat: A9
title: 配乐交付与分轨
title_en: Score Delivery and Stems
summary: 交付不是交一个立体声文件，分轨命名与响度标准同样算交付内容。
summary_en: Delivery is more than one stereo file; stem naming and loudness standards are part of the hand-off.
level: standard
tags: [交付, 分轨, 命名, 响度]
tags_en: [delivery, stems, naming, loudness]
alias: [配乐交付, 分轨交付, 交片, stems, delivery]
links:
  - "[[glossary:stems]]"
  - "[[glossary:lufs]]"
  - "[[glossary:headroom]]"
instances:
  - mutopia-000497 | 贝多芬第五的第一乐章，若按声部拆成弦乐、木管、铜管分轨，剪辑师可单独调整（C1）
  - musicnet-000069 | 贝多芬四重奏的慢乐章，四声部拆分后仍要能合回原样（C1）
  - atepp-005387 | 拉威尔《绞刑架》，极弱段落的分轨要保留动态，不能被归一化压平（C1）
sources:
  - 影视与游戏配乐的分轨交付惯例，依后期制作公开资料核对，未抄原文
  - 响度与真峰值的交付标准，依流媒体与广播规范说明核对，未抄文本
updated: 2026-10-28
---

::: zh
## 问题

导演、剪辑师、混录师拿到音乐后要能改：某段太响要压、某件乐器要抽掉、结尾要延长。只交一个立体声混音，等于把这些可能性全关掉。交付的质量，决定后期有多少回旋余地。

## 原理

分轨是把混音按功能拆成若干组，常见拆法是弦乐、木管、铜管、打击、合成与音效层。所有分轨相加应与完整混音一致，否则后期一改就对不上。分轨要同步起始、统一采样率与位深，命名清晰。响度按交付平台标准给，一般留出余量给后期混音。交付还包括总谱、MIDI、工程文件与授权说明。

## 参数与做法

先确认交付清单：立体声混音、分轨、无人声版、短版、总谱与分轨说明。分轨从同一时间零点开始，长度一致，文件名写清曲名、段落、版本与日期。采样率与位深统一，别混用。响度按平台定值，真峰值留余量。检查每一条分轨单独播放时不爆音，合起来与原混音一致。附一份说明文档，写清楚授权范围与使用限制。

## 听什么

在交响曲的分轨里听弦乐、木管、铜管是否能单独成立又能合回原样，在四重奏里听四声部拆分后是否仍然对齐，在极弱段落里听分轨是否保住动态。交付做得好的项目，后期几乎不需要回头问问题。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","C5","B4","G4","E4","C4"],"label":"一条弦乐分轨","label_en":"One string stem","hint":"单独听这条分轨应当完整，与其他分轨相加又应当回到原混音","hint_en":"Alone the stem should stand, and summed with the others it should equal the mix"}
```
:::

::: en
## The problem

Directors, editors and re-recording mixers need to change things after the music arrives: duck a loud passage, drop an instrument, extend an ending. Handing over a single stereo mix closes all those doors. Delivery quality decides how much room post-production still has.

## How it works

Stems split a mix into functional groups, commonly strings, woodwinds, brass, percussion and synth or effects layers. Summed together they must equal the full mix, or later changes will not line up. Stems start at the same time zero, share sample rate and bit depth, and carry clear names. Loudness follows the delivery platform standard, usually with headroom left for the final mix. Delivery also includes the score, MIDI, session files and a licence statement.

## Settings and practice

Agree the list first: stereo mix, stems, instrumental version, short edits, score and stem notes. Start stems at the same zero point and keep equal lengths, with file names giving title, cue, version and date. Unify sample rate and bit depth rather than mixing them. Set loudness to the platform target and leave true-peak headroom. Check each stem alone for clipping and all stems together against the original mix. Attach a document describing usage rights and limits.

## What to listen for

In the symphony stems, whether strings, woodwinds and brass stand alone and still sum correctly; in the quartet, whether four parts stay aligned after splitting; in the quiet passage, whether dynamics survive. A well-delivered project leaves post-production with almost no questions to ask.

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","C5","B4","G4","E4","C4"],"label":"One string stem","label_en":"One string stem","hint":"Alone the stem should stand, and summed with the others it should equal the mix","hint_en":"Alone the stem should stand, and summed with the others it should equal the mix"}
```
:::
