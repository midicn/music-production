---
id: studio-one
site: prod
cat: C
order: 4
title: Studio One
title_en: Studio One
summary: 以拖拽与单窗口为核心的 DAW，母带页把成品收在同一个工程体系里。
summary_en: A drag-and-drop, single-window DAW whose Project page keeps mastering inside the same workflow.
level: standard
tags: [DAW, 工作流, 母带]
tags_en: [DAW, workflow, mastering]
alias: [Studio One, S1, PreSonus, 普瑞声纳]
links:
  - "[[glossary:daw]]"
  - "[[glossary:mastering]]"
  - "[[instrument:software-synth]]"
instances:
  - groove-000006 | 138 BPM 的流行鼓循环，适合对照拖拽搭骨架与段落铺排；这是该工具常见产出的参照，不是该工具的演示
  - mutopia-000001 | 人声加钢琴的短歌，用来对照录音、comping 与混音的层次；这是该工具常见产出的参照，不是该工具的演示
  - oga-000001 | 三分钟的管弦游戏配乐，可对照编曲轨重排与多轨平衡；这是该工具常见产出的参照，不是该工具的演示
  - groove-000010 | 两分钟的放克鼓循环，用来对照长时间线的编辑与导出；这是该工具常见产出的参照，不是该工具的演示
sources:
  - 厂商公开的产品说明、版本分层与插件格式——依据来自2026-10 复核。
  - 事件、图层与母带页的功能范围，对照官方文档与音频工程教材整理。
  - 工程交换与版本兼容的限制（DAW 文档）。
updated: 2026-10-30
tool_kind: daw
tool_vendor: PreSonus
tool_form: 桌面应用
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [编曲, 录音, 混音, 母带]
tool_verified: 2026-10-30
---

::: zh
## 它能完成什么

从浏览器把循环、插件与预设拖进工程，快速搭出一首歌的骨架。录人声与乐队，用图层做 comping，用集成的修音工具改音高与节奏。用编曲轨重排段落，用草稿板试另一种编曲而不弄乱主工程。在母带页把几首混音排成一张 EP，处理曲间间隔与整体响度。导出成品、分轨与给视频的参考；把常用轨道存成模板，下一次开工不用从零搭。把现场录音的多轨拖进同一个工程，按曲目分批整理与导出；用和弦轨试转调，再把结果写回 MIDI 声部。

## 它怎么工作

单窗口加拖拽是核心：浏览器里的音频、MIDI 与预设都能直接落到时间线或轨道。事件与图层承担 comping，和弦轨与编曲轨承担结构。母带页是独立于歌曲工程的另一份工程，读的是各首歌导出的混音。插件走 AU 与 VST3。拖拽不只搬文件，也能把效果器拖到总线上，路由跟着处理意图走。工程可以把外部素材收进一处，换机器时不会缺件。关键词是事件、图层、编曲轨、草稿板、母带页。

## 边界与坑

- 第三方模板与硬件控制脚本比 Cubase、Logic 少，冷门设备常常没有专门的控制脚本。
- 没有通用的工程交换格式，交给影视后期通常只能导分轨，插件与自动化不跟随。
- 版本分层明显，入门版缺总线与母带页等功能，教程经常对不上你的版本。
- 母带页面向立体声成品，环绕与全景声不是它的战场。
- 记谱与配乐打点弱，写谱或做长片配乐要换工具。
- 大型工程与多插件链吃 CPU，缓冲与冻结要提前规划。
- 自动保存与版本历史省心，但大工程的历史文件会占不少空间。

## 替代与搭配

要影视配乐深度，Cubase 更合适；Mac 上一体化，Logic Pro 更省心；录音棚交换，Pro Tools 是共同语言。搭配修音工具、母带插件与任何 AU 或 VST3 效果器；循环素材来自哪个库都可以，关键在挑选与编辑。

## 上手路径

先学三件事：浏览器拖拽与事件编辑、图层 comping、母带页导出。配合「编组与总线」「母带与混音的分工」「响度表」读。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q q e e q q e e","bpm":100,"label":"100 BPM 的流行骨架","label_en":"A pop skeleton at 100 BPM","hint":"先听四拍落点，再想哪一层该留白让主唱进来","hint_en":"Hear the four-beat pulse, then leave room for the vocal"}
```
:::

::: en
## What it lets you finish

Drag loops, plug-ins and presets from the browser and assemble the skeleton of a song in minutes. Record vocals and a band, comp with layers and fix pitch and timing with the integrated tuning tools. Reorder sections on an arranger track, or try a different arrangement on a scratch pad without disturbing the main song. Lay several mixes out as an EP on the Project page, setting gaps and overall loudness. Export a master, stems and a reference for picture, and save the tracks you reuse as a template so the next session does not start from zero. Batch-organise and export a live multitrack session in the same project.

## How it works

One window plus drag-and-drop is the core: audio, MIDI and presets in the browser land directly on the timeline or a track. Events and layers handle comping, while chord and arranger tracks handle structure. The Project page is a separate document from the song, reading the exported mixes of each song. Plug-ins run as AU and VST3. Vocabulary: event, layer, arranger track, scratch pad, Project page.

## Limits and traps

- There are fewer third-party templates and hardware control scripts than for Cubase or Logic, so an obscure device may have no dedicated support.
- There is no universal project interchange format; picture-post handoffs are usually stems, without plug-ins or automation.
- Editions differ sharply, and the entry tier lacks buses and the Project page, so tutorials often describe functions you do not have.
- The Project page is built for stereo masters; surround and immersive formats are not its ground.
- Notation and picture hit-points are weak, so scores and long-form scoring belong in another tool.
- Large sessions with many plug-in chains are CPU-hungry, so buffer size and freezing need planning.

## Alternatives and pairings

For picture-scoring depth, Cubase is the better fit. On a Mac, Logic Pro is the lower-friction all-in-one. For studio interchange, Pro Tools is the shared language. Pair it with tuning tools, mastering plug-ins and any AU or VST3 processor; the loop library matters less than how carefully you choose and edit.

## First three things to learn

Learn three things first: dragging from the browser into events, comping with layers, and exporting from the Project page. Read the entries on groups and buses, the split between mixing and mastering, and loudness metering.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q q e e q q e e","bpm":100,"label":"A pop skeleton at 100 BPM","label_en":"A pop skeleton at 100 BPM","hint":"Hear the four-beat pulse, then leave room for the vocal","hint_en":"Hear the four-beat pulse, then leave room for the vocal"}
```
:::
