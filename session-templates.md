---
id: session-templates
site: prod
cat: A1
title: 工程模板
title_en: Session Templates
summary: 把常用轨道、总线与插件预先存好，开工少做重复决定。
summary_en: A saved project skeleton that removes repeated setup work and keeps monitoring, routing and export settings consistent.
level: standard
tags: [DAW, 模板, 工作流]
tags_en: [DAW, template, workflow]
alias: [模板, 工程模板, 工程骨架, template, session template]
links:
  - "[[glossary:daw]]"
  - "[[glossary:bus]]"
  - "[[glossary:stems]]"
instances:
  - groove-000000 | 放克鼓循环，可直接做成模板里的节拍轨与剪辑范例
  - pdmx-000600 | 进行曲的管弦编制，适合做配乐模板的总线与分组预设
  - oga-000027 | 短小的城市循环，适合做游戏配乐模板的片段结构示例
sources:
  - 工程模板的组成与保存方式，依通行 DAW 文档核查，未抄文本
  - 模板中的路由、监听与导出设置，依音乐制作工作流通识核查，未抄文本
updated: 2026-10-28
---

::: zh
模板是一份预先搭好的工程骨架，开工时少做重复决定，也少漏掉监听与导出设置。

## 问题

每次从零建轨，命名、颜色、总线与监听都要重来，忙起来最容易漏。模板把这些决定提前做好，让注意力留给音乐。

## 原理或做法

模板就是工程快照，包含轨道结构、路由、插件预设与导入路径，但不含具体素材。可以按类型分，比如歌曲、配乐、播客。模板越简单越耐用，塞满插件反而拖慢启动。

## 参数与判断

先定采样率、缓冲与文件命名规则，再放总线与参考轨。导出预设要跟交付格式一致。每季度清理一次，把不再用的插件与轨道删掉。

## 听什么

用同一段电钢琴短句，在空白工程与模板里各听一次。差别应在监听链与总线上，而不是音色本身。若模板一打开就变闷，先查总线。

```audiolab
{"type":"instrument","gm":"Electric Piano 1","synth":"struck","phrase":["C4","E4","G4","B4"],"label":"模板试听用的短句","label_en":"A phrase for testing a template","hint":"在空白工程与模板里各放一次，比较空间","hint_en":"Play it in an empty project and in the template, then compare space"}
```

## 常见误解

模板越多越专业，其实常用的一两个就够。模板也不能代替编曲决定，它只帮你省掉重复劳动。
:::

::: en
A template is a prepared project skeleton. It removes repeated decisions at the start and makes it harder to forget monitoring or export settings.

## The problem

Building tracks from scratch means redoing names, colours, buses and monitoring every time, and busy sessions are where things get missed. A template makes those decisions in advance so attention goes to the music.

## How it works

A template is a project snapshot; it holds track structure, routing, plug-in presets and import paths, but no actual material. It can be typed for songs, cues or podcasts. Simpler templates last longer; a template stuffed with plug-ins slows every start.

## Settings and judgement

Set sample rate, buffer and file-naming rules first, then add buses and a reference track. Export presets should match the delivery format. Clean the template every few months and remove tracks and plug-ins you no longer use.

## What to listen for

Play the same electric-piano phrase in an empty project and in the template. The difference should be monitoring and bus tone, not the instrument. If the template sounds dull on opening, check the bus first.

```audiolab
{"type": "instrument", "gm": "Electric Piano 1", "synth": "struck", "phrase": ["C4", "E4", "G4", "B4"], "label": "A phrase for testing a template", "label_en": "A phrase for testing a template", "hint": "在空白工程与模板里各放一次，比较空间", "hint_en": "Play it in an empty project and in the template, then compare space"}
```

## Common misunderstandings

More templates is not more professional; one or two used often are enough. A template cannot make arranging decisions for you; it only removes repeated work.
:::
