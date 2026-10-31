---
id: wwise
site: prod
cat: C
order: 44
title: Wwise（游戏音频中间件）
title_en: Wwise
summary: 面向游戏与交互媒体的音频中间件，把素材接成状态、事件与可调的混音。
summary_en: Game audio middleware that turns finished assets into events, states and a mix that responds to play.
level: standard
tags: [游戏音频, 中间件, 交互音乐, 实现]
tags_en: [game audio, middleware, interactive music, implementation]
alias: [Wwise, Audiokinetic Wwise, 游戏音频中间件, Wwise 集成]
links:
  - "[[glossary:sound-design]]"
  - "[[glossary:stems]]"
  - "[[instrument:drum-kit]]"
instances:
  - oga-000004 | 分层战斗曲，节奏密度高，是状态切换与循环点的参照，不是该工具的演示
  - oga-000009 | 短循环的海滩环境曲，适合对照探索状态的淡入淡出，是场景循环的参照，不是该工具的演示
  - oga-000011 | Boss 战音乐，段落清楚，可对照分段与转场的写法，是 Boss 音乐的参照，不是该工具的演示
  - oga-000053 | 不到两秒的 fanfare，是奖励提示与 stinger 的参照，不是该工具的演示
  - oga-000045 | 两分多钟的管弦片段，可对照叙事段落怎样被切成可触发的小节，是长段配乐的参照，不是该工具的演示
sources:
  - Wwise 的 Event、Actor-Mixer 与 Interactive Music 结构——依据来自Audiokinetic 公开文档。
  - 状态、开关与 RTPC 的分工，对照游戏音频实现资料整理。
tool_kind: middleware
tool_vendor: Audiokinetic
tool_form: 桌面应用
tool_platforms: [macOS, Windows]
tool_price: 按量
tool_jobs: [游戏音频, 交互音乐, 声音设计, 实现]
tool_verified: 2026-10-30
updated: 2026-10-30
---

::: zh
Wwise 不是用来写音乐的，它解决的是另一件事：同一批素材，怎样随玩家的位置、血量与选择，变成不同的音乐与音效。作曲在 DAW 完成，Wwise 负责它们何时响、怎样叠、怎样收。

## 适用工作

把探索与战斗两条循环接成随状态切换的系统，切换点落在小节线上。为 Boss 战做分段音乐，血量变化时转场而不打断节拍。把脚步声的随机容器接到材质开关上，草地与石板各有一套。给对白设优先级与并发上限，避免三个人同时说话。在真机上跑 Profiler，找出爆音、声部超限与 CPU 峰值。

## 原理

Event 是最小触发单位，内部挂容器与音源。Actor-Mixer 组织总线、衰减与效果；State、Switch 与 RTPC 分别处理离散状态、分类切换与连续参数。Interactive Music 用 segment、stinger 与 transition 拼出可变的音乐结构。集成到 Unity 或 Unreal 由官方插件与代码完成，运行时加载 SoundBank。

## 边界

- 不是作曲工具，音乐与音效仍在 DAW 里做完再导入，循环点也要在 DAW 里定。
- 必须有人写集成与事件调用，纯音频人无法独立上线，和程序员的接口要提前约定。
- Wwise 版本与引擎插件版本要锁死，升级一方就要做一轮回归。
- 授权按项目规模分档，条款要按当前官方页面核对，不能沿用旧项目的理解。
- 素材本身不好，中间件不会补救；混音问题在总线里调，不要在容器里堆效果。

## 替代

FMOD 在中小项目上更快，学习曲线更短；Unity 内置音频与 MetaSounds 在原型阶段够用。与 DAW 的分工是固定的：DAW 出素材、循环点与初始混音，Wwise 负责触发、混合与真机验证。

## 上手

先学 Event 与容器、State 与 Switch 与 RTPC 的区别、Profiler 真机连接。读这里的游戏音频导论、交互音乐与自适应音频、游戏循环与交互层，用一个两层循环走完导入到真机。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"e e e e e e e e","bpm":140,"label":"战斗状态的密度","label_en":"The density of a combat state","hint":"先听八分脉冲，再想它怎样从探索段的稀疏淡入","hint_en":"Hear the eighth-note pulse, then imagine it fading in from a sparser exploration state"}
```
:::

::: en
Wwise is not for writing music. It answers a different question: how one set of assets becomes different music and sound as the player moves, loses health or chooses. Composition stays in the DAW; Wwise decides when it sounds, how it layers and how it ends.

## Jobs it covers

Join exploration and combat loops into a system that switches on state, with the switch landing on a bar line. Build segmented boss music that transitions on health without breaking the beat. Route footstep random containers through a material switch, with separate sets for grass and stone. Give dialogue a priority and a concurrency limit so three characters do not talk at once. Run the profiler on device to find clipping, voice limits and CPU peaks.

## How it works

An Event is the smallest trigger and holds containers and sources. The Actor-Mixer organises buses, attenuation and effects. State, Switch and RTPC handle discrete states, category changes and continuous parameters. Interactive Music assembles segments, stingers and transitions into a structure that can change. Integration into Unity or Unreal runs through official plug-ins and code, and the runtime loads SoundBanks. Authoring runs on Windows and macOS; on-device checks come back through the profiler.

## Limits

- It is not a composition tool. Music and sound are finished in a DAW and imported, and loop points are set there.
- Someone must write the integration and event calls; an audio person cannot ship alone, and the interface with programmers has to be agreed early.
- The Wwise version and the engine plug-in version must be locked; upgrading one forces a regression pass.
- Projects are made of binary work units, so multi-person work needs rules for check-out, naming and merging.
- Licensing is tiered by project scale, and the terms must be read on the current official page rather than carried over from an old project.
- Middleware does not rescue weak assets, and mix problems belong in the bus structure.

## Alternatives

FMOD is faster on small and mid-size projects and has a shorter learning curve. Unity's built-in audio and MetaSounds are enough for a prototype. The split with a DAW is fixed: the DAW supplies assets, loop points and a first mix; Wwise handles triggering, blending and device checks. For the music itself, finish the score in Dorico or Sibelius and cut it into segments here.

## First three things

Events and containers, the difference between State, Switch and RTPC, and connecting the profiler to a device. Then read Introduction to Game Audio, Interactive and Adaptive Music, and Game Loops and Interactive Layers, and take one two-layer loop from import to device.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"e e e e e e e e","bpm":140,"label":"The density of a combat state","label_en":"The density of a combat state","hint":"Hear the eighth-note pulse, then imagine it fading in from a sparser exploration state","hint_en":"Hear the eighth-note pulse, then imagine it fading in from a sparser exploration state"}
```
:::
