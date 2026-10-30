---
id: project-file-management
site: prod
cat: A1
title: 工程与文件管理
title_en: Project and File Management
summary: 工程、素材、导出分开放，换台电脑也能一次打开。
summary_en: Keeping project, media and export folders separate so a session opens on another machine without relinking every file.
level: standard
tags: [工程管理, 文件结构, 工作流]
tags_en: [project management, file structure, workflow]
alias: [文件管理, 工程目录, 相对路径, project management]
links:
  - "[[glossary:daw]]"
  - "[[glossary:stems]]"
  - "[[glossary:bit-depth]]"
instances:
  - oga-000001 | 配乐工程含多条音频与采样，适合练目录分层与相对路径
  - pdmx-000922 | 单一素材的小工程，适合先练工程、素材与导出三层结构
  - groove-000010 | 长循环被多次引用，适合练素材去重与统一存放
sources:
  - 工程目录与相对路径的做法，依通行 DAW 文档与音频工程教材核查，未抄文本
  - 素材、导出与备份的分层惯例，依后期交付流程通识核查，未抄文本
updated: 2026-10-28
---

::: zh
工程文件只是一张地图，声音在别处。文件管理让这张地图在哪台机器上都指得到路。

## 问题

工程能打开，素材却整排离线；导出混在录音里，三天后分不清哪条是成品。换电脑、换硬盘或发给别人，路径一变，工程就残了一半。

## 做法

一个工程一个文件夹，里面分工程文件、素材、导出、备份四层。素材先拷进工程夹再导入，不要从桌面或下载目录直接引用。用相对路径记录素材位置，让工程只说「素材在隔壁」。录音与导出按日期加用途命名，混音稿与母带稿分开放。

## 参数与判断

工程夹放在固定盘位，路径短，少用空格与特殊字符，跨系统同步更稳。采样率与位深在建工程时定下，中途改要重采样。素材量大时，未用的归档到冷盘，工程只留实际引用的。每完成一个阶段，整夹复制到备份盘，别只拷工程。

## 听什么

在另一台机器打开工程，逐轨独奏。缺文件时往往不报错，而是静音或被换成无声片段。一遍就能找出哪条轨没有响。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5","G4","E4"],"label":"搬家后逐轨试听","label_en":"Track-by-track check after moving","hint":"独奏每条轨，确认素材真的在响","hint_en":"Solo each track and confirm the media actually plays"}
```

## 常见误解

工程文件里没有声音，拷走一个工程文件不等于交付。绝对路径也不更可靠，换机器就会断。素材和工程放同一块盘不等于备份，误删会一起消失。
:::

::: en
A project file is only a map; the sound lives elsewhere. File management keeps that map pointing to the right place on any machine.

## The problem

The session opens but every audio file is offline. Exports sit among recordings, and days later nobody knows which file is the master. Move to another computer or drive, and a changed path breaks half the project.

## The practice

Give each project one folder with four layers, namely project, media, exports and backups. Copy media into the folder before importing, never reference the desktop or downloads folder. Use relative paths so the project records that media sits next door. Name recordings and exports with date and purpose, and keep mixes apart from masters.

## Settings and judgement

Keep project folders on a fixed drive, with short paths and few special characters, so syncing behaves predictably. Fix sample rate and bit depth at the start; changing later means resampling. Archive unused media to a cold drive and keep only referenced files in the session. At each milestone, copy the whole folder, not just the project.

## What to listen for

Open the session on another machine and solo every track. Missing media often fails silently, as silence or a substitute tone. One pass reveals which track is silent.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "C5", "G4", "E4"], "label": "Track-by-track check after moving", "label_en": "Track-by-track check after moving", "hint": "独奏每条轨，确认素材真的在响", "hint_en": "Solo each track and confirm the media actually plays"}
```

## Common misunderstandings

A project file holds no audio, so copying it is not a delivery. Absolute paths are not safer; they break on the next machine. Keeping media on the same drive is not a backup, because one deletion takes both.
:::
