---
id: superior-drummer
site: prod
cat: C
order: 20
title: 鼓采样器（Superior Drummer 一类）
title_en: Drum Samplers (Superior Drummer and Peers)
summary: 用 MIDI 指挥一套录好的鼓，房间与串音都在混音台里。
summary_en: Conduct a recorded kit from MIDI, with room mics and bleed on its own mixer.
level: standard
tags: [插件, 鼓组, 采样器, 编曲]
tags_en: [plugin, drums, sampler, arranging]
alias: [Superior Drummer, Toontrack, SD3, 鼓采样器, 虚拟鼓]
tool_kind: plugin
tool_vendor: Toontrack
tool_form: 插件
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [编曲, 录音, 混音]
tool_verified: 2026-10-30
links:
  - "[[instrument:drum-kit]]"
  - "[[glossary:drum-machine]]"
  - "[[glossary:phase]]"
instances:
  - groove-000007 | 65 BPM 摇滚鼓组，速度慢，房间尾音与串音有时间展开（C1）。
  - groove-000000 | 138 BPM 放克鼓组，踩镲密集，适合看采样鼓在高频是否发假（C1）。
  - groove-000005 | 87 BPM 嘻哈鼓组，底鼓与军鼓留白多，房间麦的比例一听就变（C1）。
  - groove-000002 | 86 BPM 灵魂乐鼓组，律动偏后，适合检验 MIDI  groove 的人性化程度（C1）。
sources:
  - Toontrack 官方产品页的鼓组、混音台与 MIDI 库说明（公开资料）。
  - 多麦鼓录音与串音的常见处理，参考录音惯例。
updated: 2026-10-30
---

::: zh
## 适用工作

- 给一首 demo 配上像真鼓手打的鼓，不必进棚。
- 用 MIDI 改节奏与过门，比重新录一遍鼓快得多。
- 在插件内部调每支麦克风的电平与串音，做出房间感。
- 拿它替换或叠加真鼓录音，补军鼓与底鼓的力度。
- 给广告与短视频快速换风格，同一段 MIDI 换一套鼓。
- 用自带 groove 库找风格合适的律动，再改成自己的句子。

## 原理

每个鼓件按力度与演奏法录了多层样本，MIDI 音符触发对应层，力度与演奏法决定音色与音量。混音台里每支麦克风是独立通道：近场、头顶、房间与串音都能单独调，串音不是缺陷而是空间感的来源。鼓组可以整体换库，房间与麦克风配置跟着库走。内置的 groove 库给的是演奏数据，不是音频，所以速度、力度与编排都能继续改。鼓件位置与力度映射固定，电鼓触发要按映射表设。库越大，首次加载越慢，换一套库要留出加载时间。

## 边界

- 采样鼓的弱点在镲片与密集军鼓，快速连击容易听出重复，需要力度与人性化处理。
- 库很大，装几个 SDX 就占数百 GB；流式读取依赖 SSD，内存不足会爆音。
- 每个扩展库单独授权，换电脑要重新登记；工程交接要说明用了哪些库。
- 房间与串音的比例在不同库之间不通用，换库要重新调。
- 它是采样器，不能像合成鼓那样做出库外的新音色；要怪声得另加合成器。
- 插件的内部延迟与电子鼓触发有关，现场监听要算进去。

## 替代

EZdrummer 更轻、上手更快，同厂跨级可升级；BFD3 的鼓件与混音台更细；Steven Slate Drums 偏成品音色。它常与 Kontakt 分工：Kontakt 管管弦与键盘，鼓组留在鼓采样器里，混音时统一房间感。

## 上手

先学力度层与击打位置的差别，再学混音台里的麦克风比例，最后学 groove 的人性化。配合「鼓组」「鼓机」「相位」三篇读。

```audiolab
{"type":"instrument","drum":"36","phrase":["36","38","42","38","36","42","38"],"label":"一组基本鼓点","label_en":"A basic kit pattern","hint":"先听底鼓与军鼓的力度差，再想房间麦加多少会改变前后距离","hint_en":"Hear the level difference between kick and snare first, then imagine how much room mic changes the front-to-back distance"}
```
:::

::: en
## Jobs it covers

- Give a demo drums that sound played rather than programmed, without a room.
- Edit grooves and fills in MIDI far faster than re-recording.
- Balance each microphone and its bleed inside the plugin to shape the room.
- Replace or reinforce a real kit, adding weight to snare and kick.
- Swap the whole kit under one MIDI part to change style quickly for an advert or a short video.
- Find a feel in the built-in groove library and rewrite it into your own part.

## How it works

Each piece is sampled in multiple velocity layers and articulations; a MIDI note triggers the matching layer, and velocity and articulation set tone and level. On the mixer, every microphone is a separate channel: close mics, overheads, room and bleed can be balanced independently, and bleed is the source of space, not a fault. A kit can be swapped wholesale, with rooms and microphone setups following the library. The built-in grooves are performance data, not audio, so tempo, dynamics and arrangement stay editable. Piece positions and velocity mappings are fixed, so electronic drum triggering follows the map. Larger libraries load slowly, so allow time when swapping kits.

## Limits

- Sampled drums are weakest on cymbals and dense snare work, where fast repeats expose repetition and need velocity and humanising.
- Libraries are large, and a few SDX packs run to hundreds of gigabytes; streaming needs an SSD, and insufficient RAM causes dropouts.
- Each expansion is licensed separately and must be registered again on a new machine; a session handover must list the libraries used.
- Room and bleed proportions do not carry between libraries, so a kit swap needs the mix rebuilt.
- It is a sampler and cannot invent sounds outside its libraries the way a synth can; unusual drums need another instrument.
- The plugin has latency that matters with electronic drums, so count it in live.

## Alternatives

EZdrummer is lighter and quicker to learn, with a crossgrade path from the same vendor. BFD3 goes deeper on kit pieces and mixer routing. Steven Slate Drums leans toward finished tones. The drum sampler usually divides work with Kontakt: Kontakt covers orchestra and keys, the kit stays here, and the mix unifies the room.

## First three things

Learn velocity layers and hit positions, then microphone balance on the mixer, then humanising a groove. Read the site's pages on the drum kit, drum machines and phase alongside it.

```audiolab
{"type":"instrument","drum":"36","phrase":["36","38","42","38","36","42","38"],"label":"一组基本鼓点","label_en":"A basic kit pattern","hint":"先听底鼓与军鼓的力度差，再想房间麦加多少会改变前后距离","hint_en":"Hear the level difference between kick and snare first, then imagine how much room mic changes the front-to-back distance"}
```
:::
