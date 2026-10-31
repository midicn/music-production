---
id: freeze-and-render
site: prod
cat: A1
title: 冻结与渲染
title_en: Freeze and Render
summary: 把耗 CPU 的轨道先算成音频，换回流畅编辑与稳定导出。
summary_en: Turning heavy tracks into audio ahead of time, and knowing when a frozen file can still be changed and when a render cannot.
level: standard
tags: [DAW, 冻结, 渲染, 工作流]
tags_en: [DAW, freeze, render, workflow]
alias: [冻结, 渲染, 离线导出, freeze, render, bounce]
links:
  - "[[glossary:daw]]"
  - "[[glossary:bit-depth]]"
  - "[[glossary:stems]]"
instances:
  - atepp-002441 | 哥德堡变奏曲的钢琴演奏，插件链长时可先冻结再继续编辑
  - oga-000033 | 五分钟的游戏配乐，冻结后便于继续叠加新层
  - pdmx-000550 | 多声部协奏曲，渲染分轨前要确认各声部的依赖
sources:
  - 冻结与离线渲染的差别（DAW 文档）。
  - 导出位深、余量与尾音检查的做法，参考数字音频工程教材。
updated: 2026-10-28
---

::: zh
冻结是把轨道先算成音频、暂时关掉插件；渲染是把声音正式导出。两者都用磁盘换 CPU，但一个可逆，一个不可逆。

## 难在哪

大型采样库与效果链会让工程卡顿，尤其在录音或加轨时。冻结让已经定型的轨道停止实时计算，等需要改再解冻。

## 原理与做法

冻结会离线渲染整条轨，包括插件与自动化，然后旁路原来的链路。渲染则把结果写成新文件，可能是一首成品，也可能是一组分轨。冻结要考虑侧链与总线依赖，别把还在被别人用的轨道冻掉。

## 参数与取舍

冻结前确认侧链源、自动化与发送。渲染留出余量，别贴着零 dB。导出后核对长度、尾音与采样率一致。需要反复改的轨道先别冻。

## 耳朵要抓的点

冻结前后做 A/B，差别应在噪声底与尾音，不该在音乐性。若一冻就变薄，检查是否有插件在冻结时被跳过。

```audiolab
{"type":"instrument","gm":"Harpsichord","synth":"plucked","phrase":["C4","E4","G4","C5"],"label":"冻结前的羽管键琴","label_en":"A harpsichord before freezing","hint":"听瞬态与尾音，冻结后应保持一致","hint_en":"Hear the attack and tail; freezing should preserve both"}
```

## 容易弄错的

冻结不会降低音质，它只是提前算好。渲染之后工程也不是不能改，原工程还在，只是成品文件不再回写。
:::

::: en
Freezing renders a track to audio and temporarily disables its plug-ins; rendering exports sound for good. Both trade disk for CPU, but one is reversible and the other is not.

## Where it gets hard

Large sample libraries and long effect chains make a project stutter, especially while recording or adding parts. Freezing stops the real-time calculation for tracks that are already settled, until you need to change them again.

## Principle and practice

Freezing renders the whole track offline, including plug-ins and automation, then bypasses the original chain. Rendering writes a new file, either a finished mix or a set of stems. Freezing must respect side-chain and bus dependencies, so do not freeze a track another track still feeds.

## Settings and trade-offs

Check side-chain sources, automation and sends before freezing. Leave headroom when rendering and do not sit at zero dB. After export, verify length, tail and sample rate. Keep tracks you still expect to revise unfrozen.

## What the ear catches

Compare before and after freezing. The difference should be noise floor and tail, not musicality. If freezing makes a track thin, look for a plug-in that was skipped.

```audiolab
{"type": "instrument", "gm": "Harpsichord", "synth": "plucked", "phrase": ["C4", "E4", "G4", "C5"], "label": "A harpsichord before freezing", "label_en": "A harpsichord before freezing", "hint": "听瞬态与尾音，冻结后应保持一致", "hint_en": "Hear the attack and tail; freezing should preserve both"}
```

## Easy to get wrong

Freezing does not reduce audio quality; it calculates ahead of time. Rendering does not make a project unchangeable either. The project remains, but the exported file no longer writes back.
:::
