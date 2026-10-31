---
id: spitfire-labs
site: prod
cat: C
title: Spitfire Audio 系列
title_en: Spitfire Audio Libraries
summary: 用大厅录制的成套管弦与织体库，把草稿做到能进混音。
summary_en: Hall-recorded orchestral and texture libraries that carry a sketch far enough to mix.
level: standard
tags: [采样库, 管弦, 配乐, 弦乐]
tags_en: [sample library, orchestral, scoring, strings]
alias: [Spitfire, BBCSO, Albion, LABS, 喷火, 管弦采样]
order: 23
tool_kind: instrument
tool_vendor: Spitfire Audio
tool_form: 插件
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [编曲, 配乐, 声音设计]
tool_verified: 2026-10-30
links:
  - "[[glossary:sampler]]"
  - "[[instrument:violin]]"
  - "[[instrument:cello]]"
instances:
  - musicnet-000090 | 弦乐四重奏的力度与连断变化多，是这类库最常被要求还原的写法；这是该工具常见产出的参照，不是该工具的演示（C1，参照不是该库的演示）。
  - mutopia-000498 | 完整管弦乐的声部层次与长句，用来对照成套音源能否撑住配器；这是该工具常见产出的参照，不是该工具的演示（C1，参照不是该库的演示）。
  - atepp-000369 | 弱奏钢琴的近距离质感，用来检查织体类音色会不会把细腻动态压平；这是该工具常见产出的参照，不是该工具的演示（C1，参照不是该库的演示）。
  - oga-000001 | 游戏配乐式的管弦加合成层，正是这类库被叠进 hybrid 音色的典型用法；这是该工具常见产出的参照，不是该工具的演示（C1，参照不是该库的演示）。
sources:
  - 产品线、播放器与录音场地，对照厂商公开页面整理。
  - 采样库容量与授权条款（厂商授权说明）。
updated: 2026-10-30
---

::: zh
## 适用工作

给一支短片铺出可信的管弦底色，做到能进混音的 demo。用 BBCSO 把一段总谱写成完整配器，再用 Albion 的弦乐与织体补厚度。用 LABS 的免费音色补钢琴、人声切片或噪音层。把分轨交给混音，或在模板里换成更细的独奏库重做旋律。它也能把旧工程里过时的音色整体替换掉，保留原有演奏数据。草稿阶段就能判断配器成不成立。它最常被用来交「像真的」草稿，而不是终混。

## 原理

核心是采样加自家播放器：每个音记下多个力度层与轮替，按键触发对应录音。力度层之间按演奏力度交叉淡化，轮替避免重复音机械。BBCSO 在 AIR Lyndhurst 大厅录制，声音自带厅堂；麦克风混音决定近场与空间的比例。演奏法用 keyswitch 或 UACC 切换，长音靠 CC1 推表情。旧库仍在 Kontakt 里，加载方式与 Spitfire 播放器不同。

## 边界

第一是湿。大厅是产品的性格，想做成贴耳的流行或电子，减掉混响仍留着空间；Core 版只给固定混音，要拆麦克风得买 Pro。第二是体积与加载：Core 三十 GB 级，Pro 的全麦克风版本数百 GB，必须 SSD，整套模板加载要等，Kontakt 旧库更慢。第三是演奏法：keyswitch 要背键位，legato 只覆盖录过的音程，快速跳进、重复音与大幅滑音会露馅；独奏弦乐不如专门的独奏库，solo 段落常要换库。第四是许可：买断、绑定账户、不可转售，采样不能单独再分发。第五是资源：多麦克风与全套模板吃内存，16 GB 的机器很快见底，CPU 反而不是主要瓶颈。

## 替代

要更干、更可控的厅，换 Orchestral Tools；要一次拿到整套影视管弦并接受订阅，换 EastWest；只做织体与氛围，Heavyocity 的纹理库更轻。它常与 Omnisphere 叠 hybrid 层，用混响补空间，用 EQ 削掉 200–400 Hz 的厅堂堆积。

## 上手

先学三件事：keyswitch 与 UACC 的演奏法切换、麦克风混音的比例、CC1 与 CC11 的表情。先在空工程里跑通一条弦乐，再读这里的管弦乐配器、采样库整理、round-robin 与演奏法三篇，最后建自己的小模板。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["D3","A3","D4","F4","A4"],"label":"一段大厅弦乐的长音","label_en":"A hall string line","hint":"先听厅堂尾巴有多长，再想它适不适合贴耳的编曲","hint_en":"Hear how long the hall tail runs, then ask whether it suits an intimate arrangement"}
```
:::

::: en
## Jobs it covers

A short film can get a credible orchestral bed that survives to the mix. BBCSO covers a full score draft; Albion adds weight with strings and textures. LABS fills gaps with free pianos, vocal slices and noise layers. Stems can go to a mixer, or the melodic lines can be replaced with a dedicated solo library. It can also swap dated sounds across an old project while keeping the performance data. This is sketching that sounds finished enough to judge, not a final orchestral recording.

## How it works

Samples plus a proprietary player. Each note stores several dynamic layers and round robins, triggered from the keyboard. Layers crossfade with playing strength, and round robins keep repeated notes from sounding mechanical. BBCSO was recorded in the AIR Lyndhurst hall, so the room is part of the sound; microphone mixes set the balance of close and far. Articulations switch by keyswitch or UACC, and long notes take expression from CC1. Older libraries still run in Kontakt, with different loading behaviour.

## Limits

The hall is the point and also the problem. Pull the reverb down and space remains, which fights tight pop or electronic arrangements; Core offers a fixed mix, and separating microphones means buying Pro. Size and load times follow: Core is around thirty gigabytes, the full-mic Pro runs to hundreds, an SSD is mandatory, and a large template takes time to load, with Kontakt libraries slower still. Articulation switching has limits. Keyswitches must be memorised, legato only covers recorded intervals, and fast leaps, repeated notes and wide slides expose the joins. Solo strings are weaker than dedicated solo libraries, so exposed lines often need a swap. Licences are perpetual, account-bound and non-transferable, and samples cannot be redistributed on their own. Multi-mic templates are also memory-hungry, and a 16 GB machine runs out quickly; CPU is not the usual bottleneck.

## Alternatives

Orchestral Tools gives a drier, more controllable room; EastWest bundles a film orchestra on subscription; for texture work alone, Heavyocity's libraries are lighter. It pairs well with Omnisphere for hybrid layers, a reverb for extra space, and EQ to cut the 200–400 Hz build-up from the hall.

## First three things

Learn keyswitch and UACC articulation switching, how microphone mixes change the image, and CC1 with CC11 for expression. Then read the site's orchestration, sample library organisation, and round-robin and articulation entries, and build a small template of your own.

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["D3","A3","D4","F4","A4"],"label":"一段大厅弦乐的长音","label_en":"A hall string line","hint":"先听厅堂尾巴有多长，再想它适不适合贴耳的编曲","hint_en":"Hear how long the hall tail runs, then ask whether it suits an intimate arrangement"}
```
:::
