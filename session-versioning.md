---
id: session-versioning
site: prod
cat: A1
title: 工程版本管理
title_en: Session Versioning
summary: 用可回溯的命名与快照，避免最终版最终版二吞掉好想法。
summary_en: Saving recoverable snapshots with clear names, so a good take survives the next round of edits and every change can be explained.
level: standard
tags: [DAW, 版本管理, 工作流]
tags_en: [DAW, versioning, workflow]
alias: [版本管理, 工程版本, 快照, versioning, session version]
links:
  - "[[glossary:daw]]"
  - "[[glossary:stems]]"
  - "[[glossary:lufs]]"
instances:
  - pdmx-000614 | 《致爱丽丝》的一个版本，可与另一份回放对照速度与力度
  - pdmx-000643 | 同一作品的另一份文件，用来练版本命名与 A/B 比较
  - atepp-003117 | 贝多芬回旋曲的演奏版，适合记录不同阶段的选择
sources:
  - 工程快照、分支与命名规则——依据来自软件工程版本管理惯例与 DAW 文档。
  - 交付版本的响度与文件归档做法，对照母带与交付规范惯例整理。
updated: 2026-10-28
---

::: zh
版本管理不是给文件改个名字，而是让每一次重要改动都能回去，也能说清改了什么。

## 要解决的事

改坏了想回到昨天，覆盖保存却已经来不及。最终版、最终版二、最终版二改，最后连自己都不知道哪一版能交。

## 为什么这样有效

版本是工程快照，包含工程文件、素材与插件状态。做法很简单，关键节点另存新文件，用日期、序号与一句变更说明命名。只追加不覆盖，试验性改动可以开分支，确认后再合并回主线。

## 参数与取舍

每天至少存一个可交付版，重要录音与混音前各存一次。保留最近三到五个版本就够，太久远的归档到冷存储。工程说明里写清改了速度、音色还是结构。

## 耳朵要抓的点

拿同一首曲子的两个演出版本对比，听速度、力度与混响的差别。版本不只是文件名，它记录了当时的选择。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["E4","D4","E4","G4"],"label":"两个版本共用的主题","label_en":"A theme two versions share","hint":"听同一主题在不同演奏里的速度与力度","hint_en":"Hear tempo and touch change across performances"}
```

## 容易弄错的

版本管理不等于云备份，备份只防丢，版本才防改坏。文件越多也不越安全，没有命名的副本只会增加混乱。
:::

::: en
Versioning is not renaming a file. It is making every important change recoverable, and being able to say what changed.

## The problem to solve

You want yesterday's mix back, but the save has already overwritten it. Final, final two, final two revised, and soon nobody knows which file is deliverable.

## Why it works

A version is a project snapshot; it holds the project file, its media and the plug-in state. The practice is simple. Save a new file at each key point, name it with a date, a number and one line about the change, and append rather than overwrite. Experimental work can branch, then merge back when confirmed.

## Settings and trade-offs

Save one deliverable version each day, and one before each important recording or mix. Three to five recent versions are enough; archive older ones to cold storage. Note whether tempo, sounds or structure changed.

## What the ear catches

Compare two performances of the same work and hear differences in tempo, dynamics and reverb. A version is not just a filename; it records the choices of that moment.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["E4", "D4", "E4", "G4"], "label": "A theme two versions share", "label_en": "A theme two versions share", "hint": "听同一主题在不同演奏里的速度与力度", "hint_en": "Hear tempo and touch change across performances"}
```

## Easy to get wrong

Versioning is not cloud backup. Backup prevents loss, versions prevent damage. More files are not safer either; unnamed copies only add confusion.
:::
