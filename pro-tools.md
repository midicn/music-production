---
id: pro-tools
site: prod
cat: C
order: 6
title: Pro Tools
title_en: Pro Tools
summary: 录音棚与影视后期共用的工程标准，长于剪辑、缩混与工程交换。
summary_en: The shared session standard in recording studios and post, strongest at editing, mixing and interchange.
level: standard
tags: [DAW, 录音, 影视后期]
tags_en: [DAW, recording, post-production]
alias: [Pro Tools, PT, Avid, 普洛工具]
links:
  - "[[glossary:daw]]"
  - "[[glossary:stems]]"
  - "[[glossary:mixdown]]"
instances:
  - mutopia-000690 | 人声加钢琴的艺术歌曲，适合对照多次录音的 comping 与剪辑
  - musicnet-000235 | 弦乐六重奏的末乐章，用来对照多话筒录音的编辑与缩混
  - oga-000006 | 一分多钟的战斗配乐，可对照影视配乐的对齐与交付
  - mutopia-000493 | 二十一分钟的小提琴协奏曲，用来对照长工程的分段与归档
sources:
  - 厂商公开的产品说明、授权方式与插件格式（2026-10 复核）。
  - 播放列表、总线与工程交换的功能范围——依据来自官方文档与录音工程教材。
  - AAF 与 OMF 的交换范围，对照后期流程文档整理。
updated: 2026-10-30
tool_kind: daw
tool_vendor: Avid
tool_form: 桌面应用
tool_platforms: [macOS, Windows]
tool_price: 订阅
tool_jobs: [录音, 剪辑, 混音, 工程交换, 影视后期]
tool_verified: 2026-10-30
---

::: zh
## 能替你做完什么

录一整支乐队或一条人声，做多轨 comping，剪掉噪音，缩混到交付标准。给影视做对白、音乐与音效的编辑和混音，走环绕或全景声流程。接收 AAF 或 OMF，把别的部门的工程接进来，按时间码对齐。导出分轨、立体声或环绕混音，以及各平台要的响度版本。把工程按版本归档，交给下一位混音师；给同一场戏做多个混音版本，并把现场多轨与棚内补录拼成一场完整演出。

## 它怎么工作

播放列表与剪辑是核心：一条轨可以存多个 take，comping 是在播放列表上拼出来的。音频走固定的输入输出与总线路径，硬件插入把外部设备接进通道。工程交换靠 AAF 与 OMF，素材、位置与时间码一起走。效果以 AAX 格式运行，DSP 硬件承担计算。自动化可以写到很细的层级，剪辑点也能跟着画面走。除了 AAF，工程本身也能整体交出去，但对方要有同样的插件。关键词是播放列表、总线、AAX、AAF、时间码。

## 哪里会坑你

- MIDI 与作曲工具弱，写歌、编程与配器不如 Cubase、FL Studio。
- 只认 AAX，VST 与 AU 插件不能直接用，同一插件要另买 AAX 版。
- 授权以订阅为主，也有永久版；版本与授权管理是额外负担。
- 工程跨大版本不兼容，新旧版本协作要先统一，否则只能交分轨。
- 对音频接口与输入输出设置敏感，换机器要重建路由。
- 环绕与全景声流程复杂，房间、校准与监听数量都要配套。
- 插件与硬件的组合成本高，个人工作室容易为用不到的功能付费。
- 快捷键与工作流偏硬件思维，从消费级 DAW 过来需要一段适应期。
- 虚拟乐器与采样要跟工程一起归档，否则换机器打开时音色会被替换。

## 换成什么

以作曲与编程为主，Logic 或 Cubase 更顺；预算有限又要全能，REAPER 与 Studio One 更轻；现场电子，Ableton Live 更直接。搭配修复工具、母带工具与 Avid 硬件；与视频剪辑软件交换靠 AAF。

## 先学三件事

先学三件事：播放列表与 comping、输入输出与总线、AAF 的导入导出。配合「多轨录音」「切片与对齐」「协作与工程交付」读。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q q q q","bpm":120,"label":"录音棚的参考点击","label_en":"A studio reference click at 120 BPM","hint":"先听四拍是否稳，再想乐手跟着它进棚时该听到什么","hint_en":"Hear whether the four beats hold, then imagine what a player needs in the phones"}
```
:::

::: en
## What it finishes for you

Track a full band or a single voice, comp multiple takes, remove noise and mix to a delivery standard. Edit and mix dialogue, music and effects for picture, in surround or immersive formats. Import an AAF or OMF from another department and align it against timecode. Export stems, stereo or surround mixes, and loudness versions for each platform. Archive the session by version so the next mixer can continue, and deliver several mixes of one scene for different platforms; hand over the whole session when the receiving room shares the same plug-ins.

## How it works

Playlists and editing are the core: a track holds several takes, and comping means assembling them on a playlist. Audio follows fixed input, output and bus paths, and hardware inserts bring outboard gear into a channel. Interchange runs on AAF and OMF, carrying media, positions and timecode together. Processing runs as AAX, with DSP hardware taking the load. Automation can be written at a fine level of detail, and edit points can follow picture. Vocabulary: playlist, bus, AAX, AAF, timecode.

## Where it bites

- MIDI and composition tools are weak; writing, programming and orchestration go further in Cubase or FL Studio.
- AAX only. VST and AU plug-ins do not load, so the same processor must be bought again in AAX form.
- Licensing is mainly subscription, with perpetual options; version and licence management is extra overhead.
- Sessions are not compatible across major versions, so collaborators must agree on a version or exchange stems.
- The app is sensitive to interface and I/O settings; moving machines means rebuilding the routing.
- Surround and immersive work is complex: room, calibration and speaker count all have to match.
- Plug-ins plus hardware add up, and a personal studio can end up paying for capacity it never uses.

## What to swap in

If writing and programming dominate, Logic or Cubase is smoother. For a tight budget and broad needs, REAPER and Studio One are lighter. For live electronic work, Ableton Live is more direct. Pair Pro Tools with restoration and mastering tools and Avid hardware; exchange with video editing through AAF.

## First three things

Learn three things first: playlists and comping, I/O and bus routing, and AAF import and export. Read the entries on multitrack recording, comping and alignment, and collaboration and handoff.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q q q q","bpm":120,"label":"A studio reference click at 120 BPM","label_en":"A studio reference click at 120 BPM","hint":"Hear whether the four beats hold, then imagine what a player needs in the phones","hint_en":"Hear whether the four beats hold, then imagine what a player needs in the phones"}
```
:::
