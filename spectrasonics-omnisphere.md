---
id: spectrasonics-omnisphere
site: prod
cat: C
title: Omnisphere 合成音源
title_en: Spectrasonics Omnisphere
summary: 采样与合成混合的音源，强在织体与氛围，弱在真实乐器与 CPU。
summary_en: A hybrid sample-and-synthesis instrument strong on texture and atmosphere, weak on realism and CPU.
level: standard
tags: [合成器, 采样库, 声音设计, 配乐]
tags_en: [synth, sample library, sound design, scoring]
alias: [Omnisphere, Spectrasonics, STEAM, 大气合成器]
order: 27
tool_kind: instrument
tool_vendor: Spectrasonics
tool_form: 插件
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [声音设计, 配乐, 编曲]
tool_verified: 2026-10-30
links:
  - "[[glossary:sound-design]]"
  - "[[glossary:texture]]"
  - "[[instrument:polysynth]]"
instances:
  - oga-000033 | 游戏配乐的空灵铺底与铃音层，是这类合成音源最常被要求做出的氛围；这是该工具常见产出的参照（C1）
  - oga-000052 | 多层游戏配乐的空间与持续音，用来对照织体音色的层次控制；这是该工具常见产出的参照（C1）
  - oga-000163 | 锯齿主音与鼓的叠加，对应 Omnisphere 在 hybrid 编曲里的 lead 用法；这是该工具常见产出的参照（C1）
  - oga-000143 | 管钟与持续低音的混合，是采样加合成做音效层的典型参照；这是该工具常见产出的参照（C1）
sources:
  - 引擎结构、双层与调制功能，对照厂商公开页面整理。
  - 授权与安装方式（厂商授权说明）。
updated: 2026-10-30
---

::: zh
## 能替你做完什么

给画面铺一层合成的底，从 pad、脉冲到噪音纹理。用脉冲层给预告片做节奏底，用噪音层做转场。为管弦模板加低频与脉冲，做 hybrid 配乐。给流行或游戏做 lead、bass 与氛围。它也常被用来做游戏的环境音床。用硬件合成器作控制器，把参数映射到宏。做声音设计时，从原厂预设改起比从零搭更快。把同一预设改成自己的版本，存进工程复用。

## 它怎么工作

STEAM 引擎把采样与合成揉在一起：两层音色、滤波器、调制矩阵、8 个宏、琶音器与效果。两层可以各自选采样或合成波形，再经过同一滤波与效果链；宏把常用参数打包，现场只拧几个旋钮。预设量很大，按类别与属性检索；用户音频可以拖进来做颗粒化处理。与 Keyscape、Trilian 共享同一插件壳，键盘与贝斯音色可以并置。

## 哪里会坑你

第一，CPU：多层、unison 与长释放的 pad 很吃 CPU，一台机器开十来个实例就顶。第二，不是真实管弦：独奏小提琴、铜管与合唱都假，别拿它替代采样库。第三，预设太多，找音色比做音色更费时间，要建立自己的收藏。第四，加载时间与体积：核心库数十 GB，SSD 更稳。第五，授权绑定账户、不可转售、没有试用版，买前只能听官方 demo。第六，采样内容不能深度编辑，想拆样本做设计要用别的工具。第七，和弦密集时音色会互相掩蔽，编曲要留频率空位。第八，自定义宏与调制映射跨版本并不保证生效，工程要留原厂预设备份。

## 换成什么

要更强的合成设计，换 Serum 或 Pigments；要真实管弦，换 Spitfire 或 Orchestral Tools；要钢琴与键盘，Keyscape 在同一体系里；想省 CPU，换 u-he Diva 或 Vital。它常与管弦库叠层，用侧链与滤波把低频让出来。

## 先学三件事

先学双层与 8 个宏、调制矩阵、按标签检索预设。别把所有宏都映射满，先在空工程里做一条 8 小节的铺底，再读这里的声音设计、织体、减法合成三篇。

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["C3","G3","C4","E4","G4"],"label":"一层合成铺底","label_en":"A synth pad layer","hint":"先听它的高频在不在动，再想这一层该盖住谁、让开谁","hint_en":"Hear whether the top end moves, then decide what this layer covers and what it leaves"}
```
:::

::: en
## What it finishes for you

A synthetic bed for picture, from pads and pulses to noise textures. Pulses give a trailer rhythmic floor, and noise layers make transitions. Low end and pulses for an orchestral template, which is hybrid scoring. Leads, basses and atmospheres for pop or games, and game ambience. Hardware synths can act as controllers, mapping parameters to macros. For sound design, editing a factory preset is faster than building from zero. A preset can be turned into a personal version and saved into the project.

## How it works

STEAM blends samples and synthesis: two layers, filters, a modulation matrix, eight macros, an arpeggiator and effects. Each layer can choose a sample or a synth waveform and pass through the same filter and effect chain; macros bundle common parameters so a live set needs only a few knobs. The preset library is huge and searchable by category and attribute, and user audio can be dragged in for granular work. It shares a plugin shell with Keyscape and Trilian, so keyboard and bass sounds can sit side by side.

## Where it bites

CPU is the first limit: layered, unison and long-release pads are expensive, and a dozen instances can saturate a machine. It is not a real orchestra; solo violin, brass and choir sound synthetic, so it cannot replace a sample library. Too many presets make finding a sound slower than making one, and a personal collection is necessary. Load times follow, with a core library of tens of gigabytes that behaves better on an SSD. The licence is account-bound, non-transferable and has no demo, so buying means trusting official examples. Sample content cannot be edited deeply, and cutting samples for design needs another tool. Dense chords also mask each other, so arrangements must leave frequency space. Custom macros and mod routings are not guaranteed across versions, so projects should keep a factory preset backup.

## What to swap in

Serum or Pigments is stronger for pure synthesis; Spitfire or Orchestral Tools covers real orchestra; Keyscape covers pianos and keys in the same ecosystem; u-he Diva or Vital is lighter on CPU. It layers well with orchestral libraries, with sidechain and filtering to clear low end.

## First three things

Learn the two layers and eight macros, the modulation matrix, and tag-based preset search. Do not fill every macro; build one eight-bar bed, then read the site's sound design, texture, and subtractive synthesis entries.

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["C3","G3","C4","E4","G4"],"label":"一层合成铺底","label_en":"A synth pad layer","hint":"先听它的高频在不在动，再想这一层该盖住谁、让开谁","hint_en":"Hear whether the top end moves, then decide what this layer covers and what it leaves"}
```
:::
