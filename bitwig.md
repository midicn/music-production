---
id: bitwig
site: prod
cat: C
order: 8
title: Bitwig Studio
title_en: Bitwig Studio
summary: 以调制系统与模块化环境为核心的 DAW，声音设计与现场电子常用。
summary_en: A DAW built around modulation and a modular environment, common in sound design and live electronics.
level: standard
tags: [DAW, 声音设计, 模块化]
tags_en: [DAW, sound design, modular]
alias: [Bitwig, Bitwig Studio, 比特维格]
links:
  - "[[glossary:daw]]"
  - "[[glossary:sound-design]]"
  - "[[instrument:eurorack]]"
instances:
  - oga-000022 | 近一分钟的环境游戏配乐，适合对照调制下的音色变化；这是该工具常见产出的参照，不是该工具的演示
  - oga-000056 | 半分钟的神秘循环，用来对照片段触发与声音设计；这是该工具常见产出的参照，不是该工具的演示
  - groove-000014 | 两分多钟的爵士放克律动，可对照节奏层的调制与编排；这是该工具常见产出的参照，不是该工具的演示
  - oga-000037 | 两分半的荒废场景配乐，用来对照长音与滤波的运动；这是该工具常见产出的参照，不是该工具的演示
sources:
  - 厂商公开的产品说明、平台与升级方式，对照2026-10 复核整理。
  - 调制、逐音控制与模块化环境的功能范围（官方文档）。
  - 工程交换与插件格式的限制，参考DAW 文档。
updated: 2026-10-30
tool_kind: daw
tool_vendor: Bitwig
tool_form: 桌面应用
tool_platforms: [Windows, macOS, Linux]
tool_price: 买断
tool_jobs: [声音设计, 编曲, 现场演出]
tool_verified: 2026-10-30
---

::: zh
## 它能完成什么

用片段启动器搭 loop，再把即兴触发录成线性编曲。给任何设备加调制器，做出会呼吸的音色与节奏。在模块化环境里从零搭合成器或效果器，存成可复用设备。用复音表情与逐音调制写表情丰富的合成器声部。用同一套素材做现场版与发行版，编曲与片段共用一个工程，导出成品与分轨或交给别人继续；给影像做氛围底噪与脉冲，虽然不做专业打点。把现场演出录回工程，再在同一份文件里剪成发行版本。

## 它怎么工作

双视图：片段触发与线性编曲，每条轨可以在两者间切换。调制是核心，调制器能指向设备上的任何参数，逐音调制把表情写到单个音。模块化环境把振荡器、滤波器与逻辑模块连成信号链，自己决定走法。内置合成器覆盖减法、相位失真与采样。调制器可以串联、相乘或按条件触发，复杂运动不必逐段画自动化。工程的速度与调制也能被外部控制器推动。关键词是片段启动器、调制器、模块化环境、复音表情。

## 边界与坑

- 自带采样库与管弦音源少，传统制作要另配。
- 没有记谱与视频配乐流程，长片配乐要换工具。
- 没有 AAF 或 OMF，跨 DAW 只能交分轨。
- 调制与模块化学习成本高，容易做出能动但不好听的声音。
- 生态与教程规模小于 Ableton、Cubase，遇到问题可查的资料少。
- 升级采用按年计划，停更后仍能用，但新功能要续计划。
- 模块化补丁难读，别人接手你的工程要先花时间理解信号链。
- 快捷键与操作习惯自成一套，换宿主后要重建肌肉记忆。

## 替代与搭配

现场与电子但想要更大生态，Ableton Live 更稳；想要硬件模块化，Eurorack 与配套接口是另一条路；传统编曲与录音，Logic 或 Cubase 更完整。搭配复音表情控制器、模块化硬件与任何 VST3 插件。

## 上手路径

先学三件事：片段与编曲的录制、调制器、模块化环境里的最小信号链。配合「减法合成」「采样器的结构」「参数自动化」读。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"t t t t t t t t t t t t","bpm":120,"label":"120 BPM 的三连音网格","label_en":"A triplet grid at 120 BPM","hint":"先听三连音的流动，再想调制怎样让它不呆板","hint_en":"Hear the triplet flow, then imagine modulation keeping it alive"}
```
:::

::: en
## What it lets you finish

Build loops in the clip launcher, then record a performance into a linear arrangement. Add modulators to any device and make timbres and rhythms that breathe. Build a synth or effect from scratch in the modular environment and save it as a reusable device. Write expressive synth parts with polyphonic expression and per-note modulation. Keep a live version and a release version of one set of material, with clips and arrangement in one project, and export a master or stems. Make atmospheric beds and pulses for picture, though not professional hit-points; record a live performance back into the project and cut a release version from it.

## How it works

Two views: clip launching and linear arrangement, and each track can switch between them. Modulation is the core; modulators can target any parameter on a device, and per-note modulation writes expression into a single note. The modular environment wires oscillators, filters and logic modules into a signal chain you define. Built-in synths cover subtractive, phase-distortion and sampling. Tempo and modulation can be driven from external controllers. Vocabulary: clip launcher, modulator, modular environment, polyphonic expression.

## Limits and traps

- Stock sample libraries and orchestral sounds are few, so traditional production needs outside material.
- There is no notation and no video-scoring workflow, so long-form scoring means another tool.
- There is no AAF or OMF, so moving between DAWs means stems.
- Modulation and modular patching take time to learn, and it is easy to make sounds that move without sounding good.
- The ecosystem and tutorial base are smaller than Ableton's or Cubase's, so unusual questions find fewer answers.
- Upgrades follow a yearly plan; the app keeps working when it lapses, but new features require renewing.
- Modular patches are hard to read, so whoever inherits your project must first trace the signal chain.

## Alternatives and pairings

For live electronics with a larger ecosystem, Ableton Live is steadier. For hardware modular, Eurorack with a suitable interface is another route. For traditional arranging and recording, Logic or Cubase is more complete. Pair Bitwig with an expressive controller, modular hardware and any VST3 plug-in.

## First three things to learn

Learn three things first: recording clips into the arrangement, modulators, and the smallest useful signal chain in the modular environment. Read the entries on subtractive synthesis, sampler architecture and parameter automation.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"t t t t t t t t t t t t","bpm":120,"label":"A triplet grid at 120 BPM","label_en":"A triplet grid at 120 BPM","hint":"Hear the triplet flow, then imagine modulation keeping it alive","hint_en":"Hear the triplet flow, then imagine modulation keeping it alive"}
```
:::
