---
id: logic-pro
site: prod
cat: C
order: 2
title: Logic Pro
title_en: Logic Pro
summary: 苹果平台的一体化 DAW，作曲、录音、混音与母带都在同一个工程里。
summary_en: Apple's all-in-one DAW, taking a project from writing and recording through mixing to a master.
level: standard
tags: [DAW, macOS, 一体化]
tags_en: [DAW, macOS, all-in-one]
alias: [Logic, 逻辑, Logic Pro X, 苹果宿主]
links:
  - "[[glossary:daw]]"
  - "[[glossary:mastering]]"
  - "[[instrument:piano]]"
instances:
  - mutopia-000546 | 人声加钢琴的完整歌曲，适合对照录音轨、音色轨与混音的层次；这是该工具常见产出的参照，不是该工具的演示
  - musicnet-000240 | 弦乐六重奏的完整乐章，用来对照多轨编制的编辑与平衡；这是该工具常见产出的参照，不是该工具的演示
  - atepp-000184 | 德彪西钢琴曲，可对照软音源的表情与踏板处理；这是该工具常见产出的参照，不是该工具的演示
  - mutopia-000514 | 近十五分钟的交响乐章，用来对照大模板与长工程的资源占用；这是该工具常见产出的参照，不是该工具的演示
sources:
  - 厂商公开的产品说明、平台与版本要求，2026-10 核对，未抄文本
  - 轨道、区域与工程结构的功能范围，依官方文档与音频工程教材核查
  - 插件格式与工程交换的限制，依通行 DAW 文档核查
updated: 2026-10-30
tool_kind: daw
tool_vendor: Apple
tool_form: 桌面应用
tool_platforms: [macOS, iPadOS]
tool_price: 买断
tool_jobs: [编曲, 录音, 混音, 母带, 影视配乐]
tool_verified: 2026-10-30
---

::: zh
## 它能完成什么

从钢琴或吉他写歌，编到鼓、贝斯与弦乐，录人声，混完导出成品。用鼓手轨道生成可编辑的鼓，用 take 文件夹把多次录音拼成一条。给影像配乐，按时间码对齐，并用乐谱编辑器出谱。做 5.1 或 7.1 环绕混音，导出分轨与不同响度版本。用内置的母带助手起一版草稿，再自己判断改哪里。把工程存成模板，下一首歌直接套用；把现场录的多轨整理成一张专辑，曲目之间统一电平与间隔。

## 它怎么工作

单窗口，以轨道与区域为中心；工程由轨道、区域、插件与自动化组成。内置音源与效果覆盖大部分常用声音，第三方插件走 AU 格式。时间伸缩在区域上做，节奏与音高可以分开改；堆栈把多轨并成一条可整体处理的子混音。视频轨与时间码让配乐跟着画面剪。插件可以按轨道、按总线或按发送插入，处理顺序在信号链上看得见。关键词是区域、take 文件夹、伸缩、堆栈、AU。

## 边界与坑

- macOS 独占，iPad 版是另一条产品线；换平台等于换工程，Windows 协作方打不开。
- 只认 AU；只有 VST 版的插件用不了，跨平台插件要另找 AU 版。
- 与 Pro Tools 交换没有原生 AAF，通常交分轨，插件与自动化不跟随。
- 大编制模板与采样库吃内存，工程越大启动越慢，机器要留余量。
- 系统与版本绑定紧，旧机器停在旧系统就只能停在旧版本。
- 自动保存省心，但工程引用的第三方采样仍要自己归档。
- 大工程在不同机器上表现不同，交付前要在目标机器上完整打开一次。
- 从 Logic 回 GarageBand 不可行，教学或交接时两边的功能对不上。

## 替代与搭配

需要跨平台，Cubase 或 Studio One 更稳；需要录音棚工程交换，Pro Tools 是共同语言；只想快速起步，GarageBand 的工程可以直接打开继续做。搭配 iPad 遥控、外部合成器与音频接口；出谱交给专门的记谱软件。

## 上手路径

先学三件事：区域编辑与 take 文件夹、鼓手轨道与伸缩、导出分轨与响度。配合本站「数字音频工作站」「切片与对齐」「母带与混音的分工」读。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"h q q h q q","bpm":96,"label":"96 BPM 的二分与四分交替","label_en":"Alternating halves and quarters at 96 BPM","hint":"先听重音落在哪里，再想编曲里哪一层该跟着这个落点","hint_en":"Hear where the accents fall, then decide which layer should follow them"}
```
:::

::: en
## What it lets you finish

Write from piano or guitar, arrange drums, bass and strings, record vocals, and mix to a finished file. Generate an editable drum part with Drummer and comp several takes into one performance. Score to picture, align to timecode, and print parts from the notation editor. Mix in 5.1 or 7.1 and export stems at different loudness targets. Start a master with the built-in assistant, then decide what to change yourself. Save the session as a template for the next song.

## How it works

One window, organised around tracks and regions; a project is tracks, regions, plug-ins and automation. Built-in instruments and effects cover most everyday sounds, and third-party plug-ins run as AU only. Time stretching happens on regions, with rhythm and pitch handled separately; stacks fold several tracks into one submix. A video track and timecode let a cue follow the cut. The vocabulary is region, take folder, flex, stack, AU.

## Limits and traps

- macOS only, and the iPad edition is a separate product line; changing platform means changing projects, and Windows collaborators cannot open them.
- AU only: plug-ins sold as VST alone will not load.
- There is no native AAF for Pro Tools exchange, so stems are the usual handoff, without plug-ins or automation.
- Large orchestral templates and sample libraries eat memory; bigger projects start slower, so leave headroom on the machine.
- OS and app versions are tied together; an old Mac on an old system stays on an old Logic.
- Autosave is reliable, but third-party samples referenced by the project still need archiving.

## Alternatives and pairings

For cross-platform work, Cubase or Studio One is steadier. For studio interchange, Pro Tools is the shared language. For a quick start, a GarageBand project opens here and keeps going. Pair it with an iPad remote, external synths and an interface; send notation work to a dedicated scoring app.

## First three things to learn

Learn three things first: region editing and take folders, Drummer with flex, and exporting stems at a target loudness. Read the entries on the DAW, comping and alignment, and the split between mixing and mastering.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"h q q h q q","bpm":96,"label":"Alternating halves and quarters at 96 BPM","label_en":"Alternating halves and quarters at 96 BPM","hint":"Hear where the accents fall, then decide which layer should follow them","hint_en":"Hear where the accents fall, then decide which layer should follow them"}
```
:::
