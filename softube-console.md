---
id: softube-console
site: prod
cat: C
order: 40
title: Softube Console
title_en: Softube Console
summary: 硬件控制器加通道条建模，把调音台的手感搬进电脑，但只给你一种台子的味道。
summary_en: A hardware controller plus channel-strip models that bring console feel into the box — with one console's flavour at a time.
level: standard
tags: [混音, 通道条, 控制器, 插件]
tags_en: [mixing, channel strip, controller, plug-in]
alias: [Softube, Console 1, 通道条, 调音台建模, SSL 4000]
tool_kind: hardware
tool_vendor: Softube
tool_form: 硬件
tool_platforms: [macOS, Windows]
tool_price: 硬件
tool_jobs: [混音, 录音, 母带]
links:
  - "[[glossary:compressor]]"
  - "[[glossary:mix-bus]]"
  - "[[glossary:gain-staging]]"
instances:
  - groove-000014 | 一一六拍的爵士放克鼓组，多个话筒要压成一套鼓，通道条的顺序最见功力；这是该工具常见产出的参照，不是该工具的演示
  - nottingham-000001 | 民间舞曲的三件乐器，声部少、动态真，适合检验通道条会不会把声音压死；这是该工具常见产出的参照，不是该工具的演示
  - musicnet-000001 | 无伴奏小提琴，单轨上的均衡与压缩决定琴腔是否自然；这是该工具常见产出的参照，不是该工具的演示
  - wikifonia-000255 | 一首慢歌的旋律，人声与伴奏的比例靠总线上的胶水感；这是该工具常见产出的参照，不是该工具的演示
sources:
  - 厂商公开的控制器功能、随附通道条与宿主支持说明，对照官方页面整理。
  - 通道条顺序与增益结构的通识（混音惯例）。
tool_verified: 2026-10-30
updated: 2026-10-30
---

::: zh
## 能替你做完什么

在每条轨上得到一套统一的均衡、压缩与饱和，混音时不必逐个插件拼。用硬件旋钮与推子操作，手感接近台子，长时间混音不容易烦。把鼓组压成一套，把贝斯与底鼓扣在一起。给总线加一点胶水感，让分轨听起来像一个整体。现场或录音时用它快速给出可听的粗混。把人声从干声修到能进混音的状态，一条通道条就够。

## 它怎么工作

控制器本身不处理声音，它通过插件与宿主通信，把旋钮动作映射到当前轨道上的通道条。通道条按经典台子的模块顺序排列：输入增益、高通、均衡、压缩、饱和与输出。轨道跟随让你选中哪条轨，控制器就切到哪条，不必手动翻页。不同型号的台子作为扩展包提供，音色取向与增益结构各不相同。面板上的表头显示增益衰减，压缩多少一眼能看出来。

## 哪里会坑你

- 它只给你一种台子的味道。做惯了会发现所有歌都往同一个方向走。
- 每个实例都吃处理器，几十条轨的工程要算清楚，必要时冻结。
- 轨道跟随只支持部分宿主，冷门 DAW 里会退化成手动映射。
- 控制器与插件版本绑定，升级不同步时会出现旋钮无响应。
- 它不是真实求和。总线上的宽度与深度，仍然来自编曲与混音决定。
- 扩展台子要另买，算总价时别只算控制器。
- 通道条不教你判断，参数都在你手上，抄别人的数字没有用。

## 换成什么

不想买控制器，UAD 与 SSL 自家的通道条插件能给出类似的声音；要更中性的选择，Waves 的通道条更便宜。搭配一台总线压缩与一首参照曲，能把它的染色控制在合适范围。

## 先学三件事

先学三件事：一条通道从输入到输出的顺序、增益结构、轨道跟随的设置。再拿一套鼓练手。配合读压缩器、混音总线、增益结构三条。

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E1","E2","G2","B2","A2","G2","E2","B1"],"label":"通道条上的一条贝斯","label_en":"A bass through one channel strip","hint":"听压缩与饱和之后低频是否还跟得住，过头就只剩一团","hint_en":"Listen for whether the low end still tracks after compression and drive; push too far and it becomes one lump"}
```
:::

::: en
## What it finishes for you

Put one consistent EQ, compressor and saturation on every track instead of assembling plug-ins by hand. Work with hardware knobs and faders so long mixing sessions feel like a desk rather than a mouse. Glue a multi-mic kit into one drum sound and lock the bass to the kick. Add a little cohesion on the bus so the stems sound like one record. Print a listenable rough mix quickly during tracking or a live date.

## How it works

The controller makes no sound. It talks to the plug-in through the host and maps its knobs to the channel strip on the selected track. The strip follows a classic console order: input gain, high-pass, EQ, compression, drive and output. The meter shows gain reduction, so compression depth is visible at a glance. Track-follow switches the controller to whichever track you select, so there is no paging. Different console models arrive as add-on strips, each with its own voicing and gain structure.

## Where it bites

- It gives you one console's flavour at a time. Mix enough records and everything drifts the same way.
- Every instance costs processing. On a fifty-track session do the arithmetic and freeze where needed.
- Track-follow works only in supported hosts; an unusual DAW falls back to manual mapping.
- Controller and plug-in versions are tied together. Upgrade one without the other and knobs stop responding.
- It is not real summing. Width and depth on the bus still come from arrangement and mixing decisions.
- Extra consoles cost extra, so price the whole set rather than the controller alone.

## What to swap in

If the controller is not the point, channel strips from UAD and SSL itself give a similar sound; for something more neutral, Waves strips cost less. A bus compressor and one reference track keep the colour inside a sensible range.

## First three things

Learn the order of one channel from input to output, the gain structure, and how to set up track-follow. Then practise on a drum kit. Read the compressor, mix bus and gain staging entries alongside this one.

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E1","E2","G2","B2","A2","G2","E2","B1"],"label":"通道条上的一条贝斯","label_en":"A bass through one channel strip","hint":"听压缩与饱和之后低频是否还跟得住，过头就只剩一团","hint_en":"Listen for whether the low end still tracks after compression and drive; push too far and it becomes one lump"}
```
:::
