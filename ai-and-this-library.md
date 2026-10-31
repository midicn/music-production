---
id: ai-and-this-library
site: prod
cat: B7
title: AI 与本库
title_en: AI and This Library
summary: 本库文字采用 CC BY 4.0，曲目另有许可，训练用途不能一概而论。
summary_en: This library's text is CC BY 4.0, tracks carry their own licences, and training use cannot be treated as one case.
level: standard
tags: [AI, 许可, 训练数据, midicn]
tags_en: [AI, licensing, training data, this site]
alias: [AI 与本库, midicn 与 AI, 训练条款, AI and this library, LLM terms]
links:
  - "[[glossary:creative-commons]]"
  - "[[glossary:midi-protocol]]"
  - "[[glossary:music-copyright]]"
instances:
  - thesession-000001 | 社区曲库来源的曲调，条目元数据保留了它的许可字段
  - m21-000000 | 巴赫众赞歌属公有领域，文字与曲目的许可要分开看
  - atepp-001875 | 演奏录音采用开放许可，但许可条件与 midicn 文字不同
  - oga-000033 | 游戏配乐采用 CC0，是曲目中限制最少的一类
sources:
  - 文字许可与曲目来源条款（站内公开说明）。
  - 知识共享许可 4.0 与 robots 排除惯例，参考官方文本。
updated: 2026-10-28
---

::: zh
midicn 的文字与曲目不是一份许可。文字用 CC BY 4.0，曲目逐首保留上游条款，训练用途要分开判断。

## 要解决的事

读者常把“站上能看到”当成“可以随便用”。实际上，文字、曲目数据与录音是三类对象，许可各不相同。

## 原理与流程

文字采用 CC BY 4.0，允许复制、改写与商用，条件是署名并给出 midicn 的链接；该许可不限制用途，也未另设禁止训练的条款。曲目不由 midicn 授权，每首的许可记在数据集的 l 字段，部分社区来源还有自己的再分发条款。把整库当成一份训练语料，会同时踩到多种条款。

## 做法与判断

引用文字时保留署名与链接；使用曲目时按单曲许可核对；训练前确认文字与曲目各自的条件，不要把 midicn 当作免清权素材库；需要批量使用时先取得书面许可；发现异常抓取可依 robots 与站点条款处理。

## 耳朵要抓的点

这一条没有声音可听。用一首传统曲与一首受版权保护的改编对照，听旋律相近而权利不同，能记住许可与作品是两件事。

## 容易弄错的

CC BY 等于无需署名；站点免费等于素材免费；标注 midicn 就完成清权。署名是义务，不是万能钥匙。

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (nylon)","synth":"plucked","phrase":["G3","B3","D4","G4","D4","B3"],"label":"一段传统曲调，听它被怎样演奏","label_en":"A traditional tune, hear how it is performed","hint":"同一个曲调可以有不同编配与录音，旋律、表演与文件各有各的权利","hint_en":"One tune can carry different arrangements and recordings; melody, performance and file each hold separate rights"}
```
:::

::: en
The text and the tracks on this site do not share one licence. Text is CC BY 4.0; each track keeps its upstream terms; training use must be judged separately.

## The problem to solve

Readers treat "visible on the site" as "free to use". In fact text, track data and recordings are three different objects with different licences.

## Principle and process

Text is CC BY 4.0, which permits copying, adaptation and commercial use on condition of attribution and a link to this site. The licence does not restrict purpose, and the site adds no separate ban on training. Tracks are not licensed by this site; each carries its licence in the dataset's licence field, and some community sources add their own redistribution terms. Treating the whole library as one training corpus collides with several sets of terms.

## Practice and judgement

Keep attribution and a link when quoting text; check each track's licence before use; confirm the conditions for text and tracks separately before training; do not treat the site as a clearance-free stock library; seek written permission for bulk use; handle abnormal crawling through robots and site terms.

## What the ear catches

This entry has no sound. Compare a traditional tune with a copyrighted arrangement; the melodies may be close while the rights differ, which keeps licence and work separate in mind.

## Easy to get wrong

CC BY means no credit is needed; a free site means free material; crediting this site completes clearance. Attribution is an obligation, not a master key.

```audiolab
{"type": "instrument", "gm": "Acoustic Guitar (nylon)", "synth": "plucked", "phrase": ["G3", "B3", "D4", "G4", "D4", "B3"], "label": "A traditional tune, hear how it is performed", "label_en": "A traditional tune, hear how it is performed", "hint": "同一个曲调可以有不同编配与录音，旋律、表演与文件各有各的权利", "hint_en": "One tune can carry different arrangements and recordings; melody, performance and file each hold separate rights"}
```
:::
