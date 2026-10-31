---
id: reaper
site: prod
cat: C
order: 7
title: REAPER
title_en: REAPER
summary: 安装包小、几乎每个环节都可改的 DAW，适合愿意自己搭工作流的人。
summary_en: A small, deeply customisable DAW for people who would rather build their own workflow.
level: standard
tags: [DAW, 轻量, 可定制]
tags_en: [DAW, lightweight, customisable]
alias: [REAPER, Reaper, Cockos, 收割机]
links:
  - "[[glossary:daw]]"
  - "[[glossary:buffer-size]]"
  - "[[instrument:virtual-instruments]]"
instances:
  - musicnet-000243 | 弦乐六重奏的末乐章，适合对照多轨编辑与图层 comping
  - oga-000049 | 四分多钟的游戏配乐，用来对照长工程的结构与导出
  - groove-000036 | 三分半的爵士放克鼓循环，可对照 take 与循环编辑
  - mutopia-000622 | 四十多秒的人声小曲，用来对照小工程的轻量开工
sources:
  - 厂商公开的产品说明、平台与授权方式（2026-10 复核）。
  - 路由、take 与动作系统的功能范围，参考官方文档与用户手册。
  - 工程交换与插件兼容的限制；DAW 文档是主要依据。
updated: 2026-10-30
tool_kind: daw
tool_vendor: Cockos
tool_form: 桌面应用
tool_platforms: [Windows, macOS, Linux]
tool_price: 买断
tool_jobs: [录音, 剪辑, 混音, 现场录音]
tool_verified: 2026-10-30
---

::: zh
## 它能完成什么

在一台旧机器上录十几轨乐队，剪完、混完、导出，现场录完当天就能交粗混。把整场演出或整张专辑当一条长时间线处理，批量渲染。用自定义动作把重复操作变成一键，做自己的编辑流程。给视频挂参考音轨做简单的画面同步，再用内置的可编程效果搭自己的处理链。把常用的轨道、路由与效果存成模板，开工时一次调出；用批处理把几十个文件的格式与响度统一。

## 它怎么工作

每条轨都能当总线，路由矩阵可以任意连，不需要先建辅助轨。片段上可以叠多个 take 与图层，comping 直接在时间线上拼。动作系统把几乎任何操作变成可绑定命令，脚本可以再往下扩展。安装包小、启动快，主题与菜单都能改。内置的可编程效果不占额外授权。批量渲染把同一套处理套到很多文件上。关键词是路由矩阵、take、动作、脚本、JSFX。

## 边界与坑

- 自带音源与采样库薄，管弦与流行制作要另配，开箱不等于能开工。
- 没有原生 AAF 或 OMF，影视后期交换靠分轨或第三方脚本。
- 高度可定制意味着别人的模板与快捷键在你这里不通用，出问题要自己查。
- 记谱、和弦轨与配乐打点偏弱，通常另配工具。
- 默认界面与工作流不现代，新手容易被密集的选项劝退。
- 社区教程分散，冷门问题往往只能读文档与论坛。
- 自定义过深会让工程难以交给别人，协作前要约定一套最小设置。

## 替代与搭配

想要开箱即用的音源与流程，Logic 或 Studio One 更省事；影视配乐深度，Cubase 更完整；录音棚交换，Pro Tools 是共同语言。搭配脚本包、任何 VST 插件与轻量音频接口；工程小、依赖少，适合长期保存与迁移。工程要交给别人时，先导分轨并附一份说明，老机器上它常常是唯一跑得动的选择。

## 上手路径

先学三件事：路由与轨道模板、take 与图层 comping、动作与快捷键。配合「缓冲区大小」「总线的处理」「冻结与渲染」读。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"e e e e e e e e","bpm":140,"label":"140 BPM 的连续八分","label_en":"A run of eighths at 140 BPM","hint":"先听它是否均匀，再想旧机器上加大缓冲会先牺牲什么","hint_en":"Hear whether it stays even, then ask what a larger buffer costs on an old machine"}
```
:::

::: en
## What it lets you finish

Track a dozen channels of a band on an old machine, edit, mix and export. Treat a whole concert or album as one long timeline and render in batches. Turn repeated operations into one-key actions and build your own editing workflow. Put a reference audio track against picture for simple sync, and build a processing chain from the built-in programmable effects. Save tracks, routing and effects as a template, and batch-process dozens of files to one format and loudness without opening each.

## How it works

Every track can act as a bus, and the routing matrix connects anything to anything without first creating auxiliaries. Items stack several takes and lanes, so comping happens directly on the timeline. The action system turns almost any operation into a bindable command, and scripts extend it further. The installer is small, startup is fast, and themes and menus are editable. Built-in programmable effects need no extra licence. Batch rendering applies one chain to many files. Vocabulary: routing matrix, take, action, script, JSFX.

## Limits and traps

- Stock instruments and sample libraries are thin, so orchestral and pop production needs outside purchases.
- There is no native AAF or OMF, so post exchanges rely on stems or third-party scripts.
- Deep customisation means somebody else's template and shortcuts do not apply; troubleshooting is on you.
- Notation, chord tracks and picture hit-points are weak, so those usually mean another tool.
- The default interface and workflow look dated, and the dense options can put beginners off.
- Community tutorials are scattered, and unusual problems often end at the manual and forums.
- Over-customised setups are hard to hand over, so agree on a minimal configuration before collaborating.

## Alternatives and pairings

For stock sounds and a ready-made workflow, Logic or Studio One saves time. For picture-scoring depth, Cubase is more complete. For studio interchange, Pro Tools is the shared language. Pair REAPER with a script pack, any VST plug-in and a light interface; on an old machine it is often the only option that keeps up.

## First three things to learn

Learn three things first: routing with track templates, take and lane comping, and actions with shortcuts. Read the entries on buffer size, bus processing and freezing and rendering.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"e e e e e e e e","bpm":140,"label":"A run of eighths at 140 BPM","label_en":"A run of eighths at 140 BPM","hint":"Hear whether it stays even, then ask what a larger buffer costs on an old machine","hint_en":"Hear whether it stays even, then ask what a larger buffer costs on an old machine"}
```
:::
