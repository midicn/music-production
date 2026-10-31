---
id: cubase
site: prod
cat: C
order: 3
title: Cubase
title_en: Cubase
summary: 以 MIDI 编辑深度与影视配乐流程见长的 DAW，管弦与打点工作常用。
summary_en: A DAW known for deep MIDI editing and picture-scoring workflow, common in orchestral mockups and cues.
level: standard
tags: [DAW, MIDI, 影视配乐]
tags_en: [DAW, MIDI, film scoring]
alias: [Cubase, Cubase Pro, 斯坦伯格, Steinberg]
links:
  - "[[glossary:daw]]"
  - "[[glossary:incidental-music]]"
  - "[[glossary:automation]]"
instances:
  - oga-000002 | 一分半的动作游戏配乐，适合对照打点、段落切换与配器密度；这是该工具常见产出的参照，不是该工具的演示
  - oga-000008 | 两分钟的战斗配乐，用来对照长 cue 的结构与力度层次；这是该工具常见产出的参照，不是该工具的演示
  - mutopia-000511 | 贝多芬《埃格蒙特》序曲，可对照管弦 mockup 的声部与动态；这是该工具常见产出的参照，不是该工具的演示
  - musicnet-000111 | 小提琴奏鸣曲乐章，用来对照演奏法与表情映射的处理；这是该工具常见产出的参照，不是该工具的演示
sources:
  - 厂商公开的产品说明、平台与插件格式要求，参考2026-10 复核。
  - MIDI 编辑、演奏法映射与时间码功能；官方文档与配乐流程教材是主要依据。
  - AAF 与 OMF 的交换范围——依据来自后期文档。
updated: 2026-10-30
tool_kind: daw
tool_vendor: Steinberg
tool_form: 桌面应用
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [编曲, 影视配乐, 录音, 混音]
tool_verified: 2026-10-30
---

::: zh
## 它能完成什么

写一段三十秒的影视 cue：打点、配器、导视频参考，按时间码交付。深度编辑 MIDI，做力度、时值与演奏法，把采样库做成接近实录的管弦 mockup。录乐队与人声，做 comping，缩混并导出分轨。用和弦轨试和声走向，用编曲轨重排曲式，不动音频。接收 AAF 或 OMF，把别的部门的工程接进来继续做。给同一段音乐做长短两个版本，靠段落顺序切换而不是重写；配乐之外的流行编曲与缩混也能做，只是工作流要自己搭。

## 它怎么工作

MIDI 编辑分三层：键编辑器改音符，列表编辑器改数值，逻辑编辑器按条件批量改。演奏法映射把弓法、连奏与强弱接到采样库的键位与控制器上，换音色不必重画。和弦轨记录和声，编曲轨记录段落顺序。视频轨与时间码是配乐流程的骨架。采样库的键位因厂商而异，映射做好后可以反复用。关键词是演奏法映射、逻辑编辑器、和弦轨、时间码、AAF。

## 边界与坑

- 学习曲线陡：菜单深、概念多，第一周很容易只学会一小部分，然后靠习惯硬撑。
- 只支持 VST 系插件，AU 不能直接用；换到 Mac 上的 Logic 要另找插件。
- 工程跨大版本不兼容，新版本存的工程旧版本打不开，协作前要统一版本。
- AAF 与 OMF 只带素材、位置与基本电平，插件、自动化与演奏法映射不跟随。
- 大模板加采样库吃内存，配乐工程对机器要求高，冻结与多机是常用手段。
- 自带音源够用但不全面，管弦与鼓通常还要另配采样库。
- 键编辑器里的逻辑操作很强，但不会用时会拖慢简单编辑。

## 替代与搭配

Mac 上要一体化，Logic Pro 更省心；现场与电子，Ableton Live 更直接；轻量可定制，REAPER 的授权更宽松、改动空间更大。搭配采样库、多机采样主机与后期软件；出谱可以交给专门的记谱软件。

## 上手路径

先学三件事：模板与音频连接、键编辑器加演奏法映射、视频轨与时间码。配合「配乐工作流程」「轮替采样与奏法切换」「参数自动化」读。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"e s s e s s e s s e s s","bpm":120,"label":"120 BPM 的十六分驱动","label_en":"A driving sixteenth pattern at 120 BPM","hint":"先听重音如何推动段落，再想配乐里哪一层该承担这个推力","hint_en":"Hear how the accents push the bar, then decide which layer carries that push"}
```
:::

::: en
## What it lets you finish

Write a thirty-second cue: hit the marks, orchestrate, lay in a video reference and deliver against timecode. Edit MIDI in depth — velocity, timing and articulation — until a sample library behaves like a recorded orchestra. Track a band and vocals, comp the takes, mix and export stems. Test harmony on a chord track and reorder sections on an arranger track without touching the audio. Import an AAF or OMF from another department and keep working. Produce long and short versions of one cue by changing section order.

## How it works

MIDI editing comes in layers: a key editor for notes, a list editor for values, and a logical editor for conditional batch changes. Articulation maps connect bowings, legato and dynamics to a library's keyswitches and controllers, so swapping sounds does not mean redrawing. A chord track records harmony and an arranger track records section order. A video track and timecode form the spine of scoring work. Library key layouts differ by vendor, so a good map pays off repeatedly. Vocabulary: articulation map, logical editor, chord track, timecode, AAF.

## Limits and traps

- The learning curve is steep: menus are deep and concepts are many, so the first week covers only a slice.
- VST only. AU plug-ins do not load, and moving to Logic on a Mac means finding new versions.
- Projects are not compatible across major versions; a newer file will not open in an older install, so agree on a version before collaborating.
- AAF and OMF carry material, positions and basic levels only — no plug-ins, automation or articulation maps.
- Large templates plus sample libraries eat memory; scoring sessions demand a strong machine, and freezing only partly helps.
- Stock sounds are serviceable but not complete; orchestras and drums usually mean buying libraries.

## Alternatives and pairings

On a Mac, Logic Pro is the lower-friction all-in-one. For live and electronic work, Ableton Live is more direct. For a light, customisable setup, REAPER is freer in licensing. Pair Cubase with sample libraries, a multi-machine sample host and post-production software; send notation to a dedicated scoring app.

## First three things to learn

Learn three things first: templates and audio connections, the key editor with articulation maps, and the video track with timecode. Read the entries on the scoring workflow, articulation switching and parameter automation.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"e s s e s s e s s e s s","bpm":120,"label":"A driving sixteenth pattern at 120 BPM","label_en":"A driving sixteenth pattern at 120 BPM","hint":"Hear how the accents push the bar, then decide which layer carries that push","hint_en":"Hear how the accents push the bar, then decide which layer carries that push"}
```
:::
