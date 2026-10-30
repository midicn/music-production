---
id: plugin-formats
site: prod
cat: B5
title: 插件格式
title_en: Plug-in Formats
summary: VST3、AU、AAX、CLAP 决定工程能否在另一台机器打开。
summary_en: VST3, AU, AAX and CLAP decide whether a project opens on another machine.
level: standard
tags: [插件, 宿主, 兼容, 工程交付]
tags_en: [plug-ins, host, compatibility, session delivery]
alias: [插件格式, VST, VST3, AU, AAX, CLAP]
links:
  - "[[glossary:plugin]]"
  - "[[glossary:daw]]"
  - "[[instrument:software-synth]]"
instances:
  - oga-000001 | 一轨一音色的管弦编曲要挂十几件虚拟乐器，格式不通工程就打不开（C1）
  - openscore-000001 | 舒伯特艺术歌曲人声加钢琴，两件乐器常来自不同插件，换机容易缺一件（C1）
  - musicnet-000067 | 弦乐四重奏按声部分轨，四把提琴可能来自四个不同的采样器（C1）
sources:
  - VST3、AU、AAX 与 CLAP 的定位，依各格式公开规范核查，未抄文本
  - 工程交接中的插件缺失问题，依制作实务通识核查，未抄文本
updated: 2026-10-28
---

::: zh
## 问题

插件要装进宿主才能发声，不同格式的封装、授权与兼容并不相同。工程换一台机器打不开，常常不是文件坏了，而是少了一个格式。

## 原理

VST3 跨平台，支持侧链与多端口，是多数宿主的通用选择。AU 是 macOS 的系统级格式，Logic 只认 AU。AAX 是 Pro Tools 的格式，分原生与 DSP 两种。CLAP 较新，开源，支持复音调制与更清晰的线程模型。格式本身不改变算法，改变的是宿主能否加载、参数如何暴露、能否离线渲染。

## 参数与做法

交付工程前附插件清单与版本号，优先选同时提供 VST3 与 AU 的插件。同一插件不要混装多个版本。升级前在副本工程里验证。无法保证对方装齐时，冻结轨道或导出分轨兜底。

## 听什么

同一预设在不同格式下应当一致。若换格式后音色变了，多半是版本差异或默认参数不同，而不是格式本身。在多插件工程里，先听缺件的那一轨是否整段消失。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","B4"],"label":"四声部的和弦","label_en":"A four-part chord","hint":"四个声部可能来自四件插件，缺一件就少一条线","hint_en":"Four parts may come from four plug-ins, and one missing leaves a gap"}
```

## 常见误解

AAX 音质更好，其实它只是 Pro Tools 的加载格式。VST 并非只能在 Windows 使用。装得越多越专业，装得多只增加冲突与扫描时间。插件格式不决定采样率与位深，那些由工程设置决定。
:::

::: en
## The question

A plug-in must load inside a host, and formats differ in packaging, licensing and compatibility. A project that will not open on another machine usually lacks a format, not a file.

## How it works

VST3 runs across platforms, supports sidechains and multiple ports, and is widely used. AU is the macOS system format, and Logic loads only AU. AAX belongs to Pro Tools, in native and DSP versions. CLAP is newer and open, with polyphonic modulation and cleaner threading. The format changes no algorithm, only whether a host loads it, how parameters appear and whether offline rendering works.

## Settings and practice

List every plug-in and version before handover, and prefer makers who ship both VST3 and AU. Do not install several versions of one plug-in. Test upgrades on a copy. When the other side may lack a plug-in, freeze tracks or export stems.

## What to listen for

The same preset should sound the same in any format. If the tone changes, suspect a version or default-parameter difference, not the format. In a many-plug-in project, first hear whether the missing track vanishes.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C4", "E4", "G4", "B4"], "label": "A four-part chord", "label_en": "A four-part chord", "hint": "四个声部可能来自四件插件，缺一件就少一条线", "hint_en": "Four parts may come from four plug-ins, and one missing leaves a gap"}
```

## Common misconceptions

AAX does not sound better; it is simply how Pro Tools loads. VST is not Windows-only. Installing more is not more professional; it only adds conflicts and scan time. Nor does the format set sample rate or bit depth.
:::
