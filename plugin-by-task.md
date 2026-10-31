---
id: plugin-by-task
site: prod
cat: C
order: 50
title: 按任务选插件
title_en: Choosing Plug-ins by Task
summary: 先按任务分工，再补原厂做不到的一件，避免囤插件。
summary_en: Split plug-ins by task, then add only what the stock set cannot do, instead of collecting them.
level: standard
tags: [插件, 选型, EQ, 混响]
tags_en: [plug-ins, selection, EQ, reverb]
alias: [按任务选插件, 插件怎么选, 混音插件, plug-ins by task]
links:
  - "[[glossary:eq]]"
  - "[[glossary:compressor]]"
  - "[[glossary:reverb]]"
instances:
  - pdmx-000007 | 编制完整的交响曲，声部多、频段挤，是 EQ 取舍的参照
  - openscore-000005 | 人声随钢琴起伏，动态大，是压缩控制的参照
  - cyberhymnal-000000 | 管风琴长音，尾音与空间分不开，是混响处理的参照
  - atepp-001116 | 标注为转制的钢琴录音，嘶声与踏板噪声分层，是修复插件的参照
sources:
  - 均衡、压缩与混响的参数分工；音频工程教材是主要依据。
  - 插件的授权、格式与过采样做法——依据来自厂商公开文档。
tool_kind: guide
tool_vendor: —
tool_form: 流程
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [选型, 混音]
tool_verified: 2026-10-30
updated: 2026-10-30
---

::: zh
插件不是越多越好。先按任务列清单：修频率、控动态、造空间、救素材。原厂能做的先用原厂，第三方只在原厂做不到的那一处补。

## 要判断什么

看三件事。这件事原厂能不能做，能就不买。它吃多少 CPU 与延迟，实时监听时能不能开。授权与格式是否匹配你的宿主，AAX、AU 与 VST3 不通用。

## 选择表

EQ 用宿主原厂做削减，共振用 Pro-Q 的动态均衡，母带用线性相位；压缩用原厂做控制，染色压缩按素材挑，总线用慢启动；混响保留一个算法混响与一个卷积，Valhalla 混响适合做板式与长尾；饱和与延迟用 Soundtoys 一类；修复用 RX 的频谱工具或 Audition 的频谱显示；母带用 Ozone 的线性相位与限幅。

## 三种情形

播客对白：Audition 做降噪与响度，RX 补单点修复，压缩只做温和控制。流行混音：原厂 EQ 与压缩打底，一套染色压缩加一个板式混响，总线限幅最后。影视音乐：卷积混响匹配画面空间，动态 EQ 处理与对白的频段冲突。

## 边界与坑

- 插件囤积比缺插件更常见，同一任务三个插件只会让判断变慢。
- 订阅套装停订后工程打不开，重要工程要并轨或冻结。
- 授权管理器换机麻烦，出门前确认离线授权。
- 高采样与过采样吃 CPU，实时监听时先关。
- 预设不携带你的房间与素材，照抄只会更远。
- 格式锁定，AAX、AU 与 VST3 不能互换。

## 怎么开始

先只用原厂插件做完一首，再按最痛的一处补一个。每加一个插件，做一次 A/B 并记录它解决了什么。读这里的均衡器的三种形态、压缩器的五个参数、混响的空间感三页。

```audiolab
{"type":"instrument","gm":"Cello","synth":"bowed","phrase":["C3","G3","D4","A4"],"label":"先听这段的中低频","label_en":"Hear the low mids first","hint":"听哪个音最浑，再想 EQ 要削的是音高还是共振","hint_en":"Hear which note muddies the line, then decide whether EQ should cut level or resonance"}
```
:::

::: en
More plug-ins is not better. List tasks first: fix frequency, control dynamics, create space, rescue material. Use the stock set where it works, and add a third-party tool only where it does not.

## What you are deciding

Three questions. Can the stock plug-in do this job, and if so, do not buy. What CPU and latency does it cost, and can it run while monitoring? Does its licence and format match your host, since AAX, AU and VST3 do not interchange?

## The decision table

Cut with the host EQ; fix resonances with the dynamic EQ in Pro-Q; use linear phase for mastering. Control with the stock compressor, choose a coloured compressor by material, and use slow attack on the bus. Keep one algorithmic reverb and one convolution, with Valhalla for plates and long tails. Use something like Soundtoys for saturation and delay. Repair with the spectral tools in RX or the spectral display in Audition. Master with the linear-phase and limiting tools in Ozone.

## Three cases

Podcast dialogue: Audition for noise reduction and loudness, RX for single-event repair, and gentle compression only. A pop mix: stock EQ and compression as the base, one coloured compressor, one plate, and bus limiting last. Film music: convolution reverb to match the scene, and dynamic EQ where music fights dialogue.

## Limits and traps

- Hoarding is more common than shortage; three plug-ins for one task slow the decision down.
- Stop a subscription bundle and projects stop opening; bounce or freeze what matters.
- Licence managers make machine changes painful; confirm offline authorisation before travelling.
- High sample rates and oversampling are CPU-heavy; switch them off while monitoring.
- Presets do not carry your room or your material; copying them moves you further away.
- Formats are locked: AAX, AU and VST3 are not interchangeable.

## How to start

Finish one track with stock plug-ins only, then add one tool at the sorest point. With every addition, run an A/B and write down what it solved; six months later that note is the only honest review of the purchase. Read Three Shapes of EQ, Five Compressor Settings, and Space and Reverb alongside.

```audiolab
{"type":"instrument","gm":"Cello","synth":"bowed","phrase":["C3","G3","D4","A4"],"label":"Hear the low mids first","label_en":"Hear the low mids first","hint":"Hear which note muddies the line, then decide whether EQ should cut level or resonance","hint_en":"Hear which note muddies the line, then decide whether EQ should cut level or resonance"}
```
:::
