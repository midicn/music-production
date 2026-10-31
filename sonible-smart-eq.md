---
id: sonible-smart-eq
site: prod
cat: C
order: 400
title: smart:EQ
title_en: sonible smart:EQ
summary: 按素材类型分析并给出起始曲线，哪些频段该留仍由人决定。
summary_en: It analyses the material and proposes a starting curve; a person still decides which bands should stay.
level: standard
tags: [插件, 均衡, 智能均衡, 混音]
tags_en: [plugin, EQ, smart EQ, mixing]
alias: [smart:EQ, sonible smart EQ, 智能均衡, smart EQ]
links:
  - "[[glossary:eq]]"
  - "[[glossary:dynamic-eq]]"
  - "[[glossary:plugin]]"
  - "[[glossary:mixdown]]"
instances:
  - groove-001086 | 86 BPM 嘻哈鼓循环，低频与踩镲的比例适合检验自动曲线（C1）
  - atepp-001115 | 肖邦第一叙事曲，钢琴低音区厚，自动衰减容易削掉琴体（C1）
  - musicnet-000067 | 弦乐四重奏四件乐器挤在中频，最适合看 group 怎么分空间（C1）
  - groove-000000 | 138 BPM 放克鼓组，军鼓与踩镲的瞬态不能被抹平（C1）
sources:
  - sonible 官方 smart:EQ 4 产品页与用户手册，profile、smart:filter 与 group 说明（产品文档）
  - sonible 官方教程，smart:EQ 在混音与母带中的用法（厂商资料）
  - Sound on Sound 对 sonible smart 系列的公开评测（行业媒体）
updated: 2026-10-31
tool_kind: plugin
tool_vendor: sonible
tool_form: 插件（VST3 / AU / AAX）
tool_platforms: [macOS, Windows]
tool_price: 买断（单插件与套装分档，以官方为准）
tool_jobs: [混音, 母带, 现场]
tool_verified: 2026-10-31
---

::: zh
## 它先给一条曲线

把 smart:EQ 挂上轨道，选一个 profile，播几秒素材，它会分析频谱并给出一条起始曲线。这条曲线解决的是“从哪开始”，不是“最终该是什么样”。直接接受，通常得到一个没有明显毛病、也没有特点的声音。

## 三块功能各管什么

| 功能 | 做什么 | 适合 | 注意 |
|---|---|---|---|
| profile 分析 | 按素材类型给出起始曲线 | 陌生素材、快速起步 | 类型选错，曲线方向就错 |
| smart:filter | 让频段随信号强弱动作 | 随段落变化的堆积 | 范围过大像两套 EQ |
| group | 多条轨道一起比较、分配频段 | 鼓组、人声与伴奏 | 轨道角色要先分清楚 |

profile 的选项按人声、鼓、贝斯、钢琴、弦乐等类型划分；选错类型比不选更糟，曲线会朝错误方向修。group 模式把几条轨道放在同一张频谱上，按重要性互相让位，前提是每条轨道的角色已经明确。

## 放在工作流的哪个位置

混音前段用它做清理：修掉录音里固定的共振，给陌生素材一个可用的起点。中段用它做 group 平衡：鼓组内部、人声与伴奏之间，让掩蔽关系先成立。母带前不建议再叠一层自动曲线，除非清楚它要解决什么；母带阶段的每一次宽频提升，都会改变整张专辑的平衡。

## 上手先学什么

先学 profile 与素材类型的对应，再学 smart:filter 的阈值与范围，最后学 group 里谁让谁。配合“均衡器”“动态均衡”“插件格式”三篇读；需要手动精修时，仍要回到参量均衡。

## 哪些判断不能交给它

- 自动曲线不知道歌曲风格，也不知道这一段该不该亮
- 对白、样本与电子音色的 profile 判断常失准，先试听再决定
- group 的分配基于分析时的那几秒，段落一变就要重看
- 动态频段开得太宽，弱奏与强奏会像两版混音
- 它不替代声源与话筒位置，录音里的问题仍要回到录音解决

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","G3","C4","E4","G4"],"label":"低音区偏厚的和弦","label_en":"A chord with a thick low end","hint":"先听低音区的堆积，再想自动曲线会先削哪一段、你又想留下哪一段","hint_en":"Hear the low-mid build-up, then guess which band the auto curve cuts first and which you would keep"}
```
:::

::: en
## It starts with a curve

Load smart:EQ on a track, choose a profile and play a few seconds. The plug-in analyses the spectrum and proposes a starting curve. That curve answers "where do I begin", not "what should this become". Accept it untouched and you usually get a sound with no obvious faults and no character.

## Three parts, three jobs

| Part | What it does | Good for | Watch out |
|---|---|---|---|
| Profile analysis | Proposes a start curve by material type | Unknown material, quick setup | A wrong type sends the curve the wrong way |
| smart:filter | Moves a band with signal level | Build-up that changes by section | Too wide a range sounds like two EQs |
| Group | Compares tracks and shares out bands | Drums, vocal against backing | Roles must be clear before grouping |

Profiles are organised by material: voice, drums, bass, piano, strings and so on. A wrong profile is worse than none, because the curve corrects in the wrong direction. Group mode places several tracks on one spectrum and makes them yield to one another by importance, which only works once each track's role is settled.

## Where it belongs in the chain

Use it early in a mix to clean up: remove a fixed resonance from a recording, or give unfamiliar material a usable starting point. Use it mid-chain for group balance, inside a drum kit or between vocal and backing, so masking is addressed before fader moves. Do not stack another automatic curve just before mastering unless you know what it is meant to solve; every broad boost at that stage changes the balance of the whole album.

## What to learn first

Learn how profiles map to material types, then the threshold and range of smart:filter, then who yields to whom inside a group. Read it alongside the pages on EQ, dynamic EQ and plug-in formats; when a fix needs precision, return to a parametric EQ.

## Judgements not to hand over

- The curve does not know the genre or whether this section should be bright
- Profiles misread dialogue, samples and electronic timbres; audition first
- Group decisions come from the seconds analysed, and change when the arrangement does
- A dynamic band set too wide makes quiet and loud passages sound like two mixes
- It cannot replace source and microphone placement; recording faults go back to recording
:::
