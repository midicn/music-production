---
id: kontakt
site: prod
cat: C
order: 19
title: Kontakt（采样器）
title_en: Kontakt (Sampler)
summary: 采样库的通用宿主，音色真假取决于库与演奏法。
summary_en: A common host for sample libraries, where realism depends on the library and its articulations.
level: standard
tags: [插件, 采样器, 采样库, 配器]
tags_en: [plugin, sampler, sample library, orchestration]
alias: [Kontakt, Native Instruments Kontakt, 采样器, Kontakt Player]
tool_kind: plugin
tool_vendor: Native Instruments
tool_form: 插件
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [编曲, 影视配乐, 游戏音频]
tool_verified: 2026-10-30
links:
  - "[[instrument:samplers]]"
  - "[[glossary:sampler]]"
  - "[[glossary:midi-protocol]]"
instances:
  - musicnet-000020 | 巴赫第三无伴奏大提琴组曲前奏，单声部弓法变化细，采样库的连奏与换弓一测就露（C1，参照不是该插件的演示）。
  - atepp-001202 | 肖邦《船歌》，弱奏层次与踏板共鸣都很细，是钢琴采样库最难装像的部分（C1，参照不是该插件的演示）。
  - mutopia-000053 | 普雷托里乌斯《一支玫瑰》，早期乐器与声部写法朴素，音色选择比技巧更关键（C1，参照不是该插件的演示）。
  - atepp-000195 | 德彪西《月光》，钢琴采样库的踏板共鸣与弱奏层次很难同时顾到（C1，参照不是该插件的演示）。
  - musicnet-000067 | 贝多芬弦乐四重奏，四件独奏乐器各自换弓，采样库的独立声部能力受考验（C1，参照不是该插件的演示）。
sources:
  - Native Instruments 官方产品页的采样引擎、脚本与授权说明，依公开资料核对，未抄原文
  - 采样库的演奏法、键位切换与磁盘流式读取，依采样通识核对，未抄文本
updated: 2026-10-30
---

::: zh
## 它能完成什么

- 用采样库把一段管弦乐谱弹成可听的 mockup。
- 给流行与影视配乐铺真实乐器：弦乐、铜管、木管、打击乐。
- 用键位切换演奏法，在同一条轨上做连奏、断奏与颤音。
- 把多个音色组成一个 multi，一次加载整套编制。
- 给写好的 MIDI 换音色，比较不同库对同一段落的适配。
- 用脚本做自定义的演奏逻辑，并把一套编制的键位与力度习惯固定下来，换曲目时少调一遍。

## 它怎么工作

采样器把录音切成音区与力度层，按键时按音高与力度选样本，再用包络、滤波与调制把衔接补平。Kontakt 的核心是库格式与脚本引擎：库作者把样本、映射、演奏法与界面打包，用户加载后通过键位或控制器切换。磁盘流式读取让大库不必全进内存，代价是首次发声的延迟与硬盘占用。多个音色可存成 multi，随工程一起调用。脚本能改响应曲线与演奏法逻辑，但脚本随库走，不通用。

## 边界与坑

- 免费 Player 只能跑厂商授权的库，第三方库通常要完整版，买库前先确认兼容。
- 大库占硬盘与内存，流式读取依赖 SSD；机械盘上换音色会明显等待。
- 演奏法靠键位切换，写 MIDI 时要留出切换键，否则段落之间会串音。
- 各厂商的键位切换不同，同一编制里统一键位要额外花时间。
- 它是采样器不是合成器，做不出现有库之外的声音；要新音色得另找合成器。
- 库与宿主有版本要求，工程交给别人前要核对 Kontakt 版本与库授权。

## 替代与搭配

Decent Sampler 免费且轻，适合小库；UVI Falcon 的合成与采样混合更灵活；HALion 在 Steinberg 生态里更顺。它常与 Superior Drummer 这类专用鼓采样器分工：Kontakt 管管弦与键盘，鼓组交给专用工具。轻量工程可先试免费采样器，确认音色方向再换大库。

## 上手路径

先学音区与力度层的概念，再学演奏法切换，最后学 multi 与内存管理。配合本站「采样器」「MIDI 协议」「配器」三篇读。

```audiolab
{"type":"instrument","gm":"Cello","synth":"bowed","phrase":["C3","G3","D4","A4","D4","G3"],"label":"一条待分句的大提琴线","label_en":"A cello line to phrase","hint":"先听换弓的缝隙，再想采样库的连奏要补哪一段","hint_en":"Hear the gaps between bow changes first, then imagine what a sampled legato has to fill"}
```
:::

::: en
## What it lets you finish

- Play an orchestral score into an audible mockup with sampled instruments.
- Put real-sounding strings, brass, woodwind and percussion under pop and film cues.
- Switch articulations by key so one track can play legato, staccato and tremolo.
- Load a whole ensemble as a multi and recall it with the session.
- Write custom performance logic in script, and keep one set of key switches and velocity habits across a template so each new cue needs less setup.

## How it works

A sampler cuts recordings into key ranges and velocity layers, chooses a sample from pitch and velocity, and smooths the joins with envelopes, filters and modulation. Kontakt's centre is its library format and script engine: a library author packages samples, mappings, articulations and an interface, and the player switches between them by key or controller. Disk streaming keeps large libraries out of RAM, at the cost of first-note latency and drive space. Several instruments can be stored as a multi and recalled with the project. Scripts can change response curves and articulation logic, but a script belongs to its library and does not travel.

## Limits and traps

- The free Player runs only vendor-authorised libraries; third-party libraries usually need the full version, so check compatibility before buying a library.
- Large libraries consume drive space and RAM, and streaming needs an SSD; on a mechanical drive, patch changes wait.
- Articulations are switched by keys, so MIDI must leave room for those keys or passages bleed into each other.
- It is a sampler, not a synthesizer; it cannot invent sounds outside its libraries, and new timbres require a synth.
- Key switches differ between vendors, so unifying them across one ensemble takes extra time.
- Libraries and hosts have version requirements, so confirm both before handing a session over.

## Alternatives and pairings

Decent Sampler is free and light for small libraries. UVI Falcon mixes sampling and synthesis more flexibly. HALion sits more naturally in a Steinberg workflow. Kontakt usually divides work with a dedicated drum sampler such as Superior Drummer: Kontakt covers orchestra and keys, the drum tool covers the kit. A light project can start with a free sampler to confirm the sound direction before moving to a large library.

## First three things to learn

Learn key ranges and velocity layers, then articulation switching, then multis and memory management. Read the site's pages on samplers, the MIDI protocol and orchestration alongside it.

```audiolab
{"type":"instrument","gm":"Cello","synth":"bowed","phrase":["C3","G3","D4","A4","D4","G3"],"label":"一条待分句的大提琴线","label_en":"A cello line to phrase","hint":"先听换弓的缝隙，再想采样库的连奏要补哪一段","hint_en":"Hear the gaps between bow changes first, then imagine what a sampled legato has to fill"}
```
:::
