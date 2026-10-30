---
id: track-naming-and-color
site: prod
cat: A1
title: 轨道命名与配色
title_en: Track Naming and Colour
summary: 命名与配色决定三个月后还能不能读懂自己的工程。
summary_en: Consistent names and colours keep a large session readable at a glance and make routing mistakes obvious.
level: standard
tags: [轨道, 命名, 工程整理]
tags_en: [tracks, naming, organization]
alias: [轨道命名, 轨道颜色, 工程整洁, track naming]
links:
  - "[[glossary:daw]]"
  - "[[glossary:bus]]"
  - "[[glossary:stems]]"
instances:
  - pdmx-000600 | 进行曲声部多，适合练按乐器族命名与配色
  - mutopia-000514 | 交响曲各声部层次多，适合练分组色带与总线路由
  - oga-000001 | 分层配乐含多类音色，适合练按功能而非音源命名
sources:
  - 轨道命名与总线对应的做法，依通行 DAW 文档核查，未抄文本
  - 颜色分组与可读性的经验，依音乐制作工作流通识核查，未抄文本
updated: 2026-10-28
---

::: zh
命名与配色不是装饰，它们是工程的索引，决定三个月后还能不能读懂自己做过什么。

## 问题

混音台里一排 Audio 1、Audio 2、Kontakt 5，全是默认灰，唯一被静音的轨藏在两条之间。回到旧工程，要先独奏二十分钟，才知道当初搭了什么。

## 做法

按角色加来源命名，例如 Kick、Bass DI、Violin 1，同一种乐器有多条时再加编号。按族配色，鼓一色、低频一色、键盘一色、吉他一色、人声一色、效果一色，全局统一。总线名与子轨对应。备用 take 用前缀标出，不要混在正常轨里。

## 参数与判断

颜色控制在五到六种，眼睛才读得动。名字要短，窄推子下不被截断。红色留给录音待命轨，别处不用。命名在录音前完成，因为那一刻记忆最清楚。

## 听什么

问自己能不能在三秒内找到任意一条轨。独奏一个颜色组，听它是否构成一个完整的层。若一组听起来不像一件事，多半是命名掩盖了路由问题。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","C5","G4","E4"],"label":"按声部拆开的一层","label_en":"One layer split by part","hint":"听这一层是否像一个整体，再决定它归哪一组","hint_en":"Hear whether the layer sounds like one thing, then decide its group"}
```

## 常见误解

颜色不是装饰，它在编码乐器族。长描述在推子里会被截断，反而更难认。事后改名可以，但会打断已经建立的肌肉记忆。
:::

::: en
Names and colours are not decoration. They index a session and decide whether you can still read it in three months.

## The problem

The mixer shows Audio 1, Audio 2 and Kontakt 5 in default grey, and the muted track hides between two others. Returning to the project costs twenty minutes of soloing to learn what you built.

## The practice

Name by role and source, such as Kick, Bass DI or Violin 1, and add numbers only when several share a role. Colour by family, using one colour for drums, one for low end, one for keys, one for guitars, one for voices and one for effects. Make bus names match their children. Mark alternate takes with a prefix instead of leaving them in the flow.

## Settings and judgement

Keep the palette to six colours so the eye still reads it. Keep names short enough to survive a narrow mixer strip. Reserve red for record-armed tracks and use it nowhere else. Name before recording, not after, because the moment after is when memory is strongest.

## What to listen for

Ask whether you can find any track within three seconds. Solo a colour family and hear whether it forms a coherent layer. If a group does not sound like one thing, the naming is probably hiding a routing decision.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C4", "E4", "G4", "C5", "G4", "E4"], "label": "One layer split by part", "label_en": "One layer split by part", "hint": "听这一层是否像一个整体，再决定它归哪一组", "hint_en": "Hear whether the layer sounds like one thing, then decide its group"}
```

## Common misunderstandings

Colour is not cosmetic when it encodes family. Long descriptive names do not help in a mixer strip, because they get truncated. Renaming later breaks the memory you built.
:::
