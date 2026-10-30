---
id: fmod
site: prod
cat: C
order: 45
title: FMOD（游戏音频中间件）
title_en: FMOD
summary: 以事件与参数驱动的游戏音频中间件，小团队上手快，集成直接。
summary_en: Event-driven game audio middleware with a short path from asset to running game, especially for small teams.
level: standard
tags: [游戏音频, 中间件, 交互音乐, 实现]
tags_en: [game audio, middleware, interactive music, implementation]
alias: [FMOD, FMOD Studio, Firelight FMOD, 游戏音频中间件]
links:
  - "[[glossary:sound-design]]"
  - "[[glossary:automation]]"
  - "[[instrument:drum-kit]]"
instances:
  - oga-000018 | 场景循环曲，长度与配器适合做区域音乐，是场景音乐的参照，不是该工具的演示
  - oga-000021 | 洞穴环境曲，动态平缓，适合对照参数驱动的环境层，是环境音乐的参照，不是该工具的演示
  - oga-000002 | 行动段配乐，节奏密集，可对照快节奏事件的切换，是行动段配乐的参照，不是该工具的演示
  - oga-000024 | 追逐曲，段落推进明显，适合对照强度参数，是追逐段落的参照，不是该工具的演示
  - oga-000088 | 二十多秒的循环，是循环点与过渡的参照，不是该工具的演示
sources:
  - FMOD Studio 的 Event、参数、Snapshot 与 Live Update，依 Firelight 公开文档核查，未抄文本
  - 运行时的 bank 加载与引擎集成，依官方集成文档核查，未抄文本
tool_kind: middleware
tool_vendor: Firelight Technologies
tool_form: 桌面应用
tool_platforms: [macOS, Windows]
tool_price: 按量
tool_jobs: [游戏音频, 交互音乐, 声音设计, 实现]
tool_verified: 2026-10-30
updated: 2026-10-30
---

::: zh
FMOD 的路线是把复杂度压到能在一周内跑通：素材导入、事件搭好、参数一挂，游戏里就能听见。对独立团队，这比功能表上的深度更重要。

## 它能完成什么

一周内把三层战斗音乐接进 Unity 原型，开战、受伤与胜利各有层次。用参数控制城市昼夜的配器，白天加弦乐，夜里换合成铺底。给载具做随速度变化的引擎声，音高与滤波一起走。用 snapshot 做水下与室内的整体滤波与混响。在编辑器里连上运行中的游戏，边玩边调混音。

## 它怎么工作

Event 里放音轨与乐器，参数驱动音高、音量、效果与音轨的启停。Snapshot 叠加全局的总线状态，进出水下时一次切换。Live Update 让编辑器回连运行中的游戏，改完立刻能听。运行时由 API 加载 bank，再按事件路径播放；内置效果、3D 衰减与声部管理都在中间件里完成。

## 边界与坑

- 大型项目的状态与总线治理不如 Wwise 细，需要自建命名、分层与文档。
- bank 与引擎插件版本要锁，升级一方就要回归测试。
- 编辑器只跑 Windows 与 macOS，Linux 只作为运行时目标。
- 授权按项目规模分档，免费档有条件，条款要按当前官方页面核对。
- 不是 DAW，长时间线与复杂编曲仍要回宿主完成。
- 调试依赖游戏端日志，编辑器里看不到全部运行时问题。

## 替代与搭配

Wwise 适合复杂状态与多平台大团队；Unity 内置音频够原型与小型项目；MetaSounds 是 Unreal 的原生路线。与 DAW 的分工同 Wwise：宿主出素材与循环点，FMOD 做事件、混合与真机验证。音乐需要出谱时，交给 Dorico 或 Sibelius 定稿，再按段落切进事件。

## 上手路径

先学 Event 与参数、Snapshot、bank 构建与 Live Update。读本站的游戏音频导论、交互音乐与自适应音频、游戏循环与交互层，用一个昼夜切换的场景走完导进到真机。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q e e q e e q q","bpm":110,"label":"随强度参数变化的脉冲","label_en":"A pulse that follows an intensity parameter","hint":"先听这个节奏型，再想参数升高时哪一层先加进来","hint_en":"Hear the pattern, then decide which layer enters first as the parameter rises"}
```
:::

::: en
The FMOD route compresses complexity into something that runs within a week: import assets, build an event, attach a parameter, hear it in the game. For an independent team that matters more than depth on a feature chart.

## What it lets you finish

Get three layers of combat music into a Unity prototype in a week, with separate layers for engagement, damage and victory. Drive the orchestration of a town by time of day, adding strings by day and a synth bed at night. Build a vehicle engine that follows speed, with pitch and filtering moving together. Use snapshots for the overall filtering and reverb underwater and indoors. Connect the editor to a running build and mix while playing.

## How it works

Events hold tracks and instruments; parameters drive pitch, level, effects and whether a track plays. Snapshots stack global bus states, so entering water is one switch. Live Update reconnects the editor to a running game, and changes are audible immediately. At runtime the API loads banks and plays events by path; built-in effects, 3D attenuation and voice management happen inside the middleware.

## Limits and traps

- State and bus governance for very large projects is less detailed than Wwise, so naming, layering and documentation must be invented locally.
- Bank and engine plug-in versions must be locked; upgrading one side requires a regression pass.
- The editor runs only on Windows and macOS; Linux is a runtime target, not an authoring host.
- Licensing is tiered by project scale, the free tier has conditions, and the terms must be read on the current official page.
- It is not a DAW; long-form editing and complex arrangement still happen in a host.
- Debugging leans on game-side logs; the editor does not show every runtime problem.

## Alternatives and pairings

Wwise suits complex state logic and large multiplatform teams. Unity's built-in audio is enough for prototypes and small titles. MetaSounds is the native route in Unreal. The split with a DAW is the same as with Wwise: the host supplies assets and loop points, FMOD handles events, blending and device checks. When the music needs a score, finish it in Dorico or Sibelius and cut it into events by section.

## First three things to learn

Events and parameters, snapshots, and bank builds with Live Update. Then read Introduction to Game Audio, Interactive and Adaptive Music, and Game Loops and Interactive Layers, and take one day-night scene from import to device.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q e e q e e q q","bpm":110,"label":"A pulse that follows an intensity parameter","label_en":"A pulse that follows an intensity parameter","hint":"Hear the pattern, then decide which layer enters first as the parameter rises","hint_en":"Hear the pattern, then decide which layer enters first as the parameter rises"}
```
:::
