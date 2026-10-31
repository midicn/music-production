---
id: garageband
site: prod
cat: C
order: 10
title: GarageBand
title_en: GarageBand
summary: 苹果平台的免费入门 DAW，从循环拼接到简单编曲都够用。
summary_en: Apple's free starter DAW, enough for loop-based sketches and simple arrangements.
level: standard
tags: [DAW, 入门, macOS]
tags_en: [DAW, beginner, macOS]
alias: [GarageBand, GB, 车库乐队, 苹果入门宿主]
links:
  - "[[glossary:daw]]"
  - "[[instrument:drum-kit]]"
  - "[[glossary:mastering]]"
instances:
  - mutopia-000001 | 人声加钢琴的短歌，适合对照入门工程的录音与混音层次
  - abcmisc-000433 | 一分半的传统圆舞曲，用来对照循环与简单编曲的搭法
  - groove-000007 | 不到半分钟的摇滚鼓循环，可对照鼓手轨道的复杂度设置
  - oga-000020 | 一分钟的城堡场景配乐，用来对照游戏或短片配乐的入门做法
sources:
  - 厂商公开的产品说明、平台与免费方式（2026-10 复核）。
  - 循环、鼓手与智能乐器的功能范围，参考官方文档。
  - 与 Logic 的工程兼容关系；官方支持文档是主要依据。
updated: 2026-10-30
tool_kind: daw
tool_vendor: Apple
tool_form: 桌面应用
tool_platforms: [macOS, iOS, iPadOS]
tool_price: 免费
tool_jobs: [编曲, 录音, 配乐]
tool_verified: 2026-10-30
---

::: zh
## 适用工作

用循环与鼓手快速做出一段可用的背景音乐。用智能乐器弹和弦与贝斯，接麦克风录人声，做一个 demo。在手机或平板上记录动机，回到 Mac 继续。导出成品，或把工程用 Logic Pro 打开继续做，升级后仍能改音符与音色。给视频与播客做一段片头音乐，用循环拼出练习伴奏并改速度与调性配合演唱。把课堂或乐队小样录成立体声文件发给别人；用自带的吉他放大器与踏板录电吉他，再把循环与真人演奏混在一起。

## 原理

轨道加循环浏览器加智能乐器，是它的全部骨架。鼓手按风格生成鼓，可改复杂度与摆动。工程格式与 Logic 同源，可以升级打开。效果以预设为主，可调参数有限。Mac 版能用 AU 插件，移动版只支持适配的插件格式。智能乐器把和弦选择收在一个手势里，按对了就出声。循环可以整段拖进时间线，也可以只取其中一层，速度自动跟随工程。轨道越多，界面与机器的压力越明显，编曲要做取舍。关键词是循环、鼓手、智能乐器、预设。

## 边界

- 混音与路由浅：总线与发送只有固定的几条，没有灵活的侧链。
- 没有 AAF 或 OMF，工程交换只能导出音频。
- Logic 能打开 GarageBand 工程，反向不成立，升级是单行道。
- 移动版功能更少，文件管理与云同步容易出错。
- 不适合大编制、影视配乐与专业交付。
- 插件参数暴露少，学不到完整的混音思路。
- 自动化的颗粒度粗，复杂变化要回 Logic 做。
- 导出选项有限，交付前要确认格式与响度是否够用。
- 多人协作没有版本管理，文件只能靠手动起名区分。

## 替代

要继续深入，Logic Pro 是同源升级；要跨平台，Studio One 或 REAPER 更自由；只想快速出背景音乐，循环库加简单的剪辑工具就够。搭配音频接口、MIDI 键盘与 iPad 遥控。

## 上手

先学三件事：循环与鼓手、智能乐器与录音、导出与升级到 Logic。配合「数字音频工作站」「编曲与作曲的分界」「响度表」读。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q e q e q e q e","bpm":100,"label":"100 BPM 的入门节拍","label_en":"A beginner pulse at 100 BPM","hint":"先跟着拍手，再想循环里的哪一层该省掉","hint_en":"Clap along first, then decide which layer the loop can lose"}
```
:::

::: en
## Jobs it covers

Make a usable background cue quickly with loops and a drummer. Play chords and bass on the smart instruments, plug in a microphone and record a vocal demo. Capture an idea on a phone or tablet and continue on the Mac. Export a finished file, or open the project in Logic Pro and keep going. Write a signature tune for a video or podcast, and assemble a practice backing from loops, changing tempo and key to suit a singer. Record a class or band sketch as a stereo file and send it to someone; record electric guitar through the built-in amps and pedals without extra gear.

## How it works

Tracks, a loop browser and smart instruments are the whole skeleton. The drummer generates parts by style, with complexity and swing adjustable. The project format shares its roots with Logic and can be opened there. Effects are preset-driven, with limited parameters exposed. The Mac version hosts AU plug-ins, while the mobile version only accepts compatible formats. Smart instruments fold chord choice into a single gesture, so the right touch produces a chord. Vocabulary: loop, drummer, smart instrument, preset.

## Limits

- Mixing and routing are shallow: only a few fixed buses and sends, and no flexible sidechain.
- There is no AAF or OMF, so project exchange means exporting audio.
- Logic opens GarageBand projects, but not the other way round; the upgrade is one-way.
- The mobile version has fewer features, and file management and cloud sync break easily.
- It is not suited to large ensembles, picture scoring or professional delivery.
- Plug-in parameters are barely exposed, so the full picture of mixing is hard to learn here.
- Automation is coarse, and complex moves have to wait for Logic.

## Alternatives

To go deeper, Logic Pro is the same-family upgrade. For cross-platform work, Studio One or REAPER is freer. For a fast background cue, a loop library plus a simple editor is enough. Pair it with an audio interface, a MIDI keyboard and an iPad remote.

## First three things

Learn three things first: loops with the drummer, smart instruments and recording, and exporting or moving up to Logic. Read the entries on the DAW, the line between arranging and composing, and loudness metering.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q e q e q e q e","bpm":100,"label":"A beginner pulse at 100 BPM","label_en":"A beginner pulse at 100 BPM","hint":"Clap along first, then decide which layer the loop can lose","hint_en":"Clap along first, then decide which layer the loop can lose"}
```
:::
