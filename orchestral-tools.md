---
id: orchestral-tools
site: prod
cat: C
title: Orchestral Tools
title_en: Orchestral Tools
summary: 按声部单件售卖的柏林管弦，厅堂比 AIR 干，模块可以慢慢补齐。
summary_en: Berlin orchestral modules sold by section, with a tighter room than AIR and room to grow.
level: standard
tags: [采样库, 管弦, 配乐, 柏林]
tags_en: [sample library, orchestral, scoring, Berlin]
alias: [OT, 柏林管弦, SINE, Metropolis Ark, Berlin Strings]
order: 24
tool_kind: instrument
tool_vendor: Orchestral Tools
tool_form: 插件
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [编曲, 配乐]
tool_verified: 2026-10-30
links:
  - "[[glossary:legato]]"
  - "[[instrument:cello]]"
  - "[[instrument:timpani]]"
instances:
  - musicnet-000308 | 弦乐五重的慢乐章，声部独立、连奏多，是这类库最常被要求还原的室内乐写法；这是该工具常见产出的参照，不是该工具的演示（C1，参照不是该库的演示）。
  - musicnet-000090 | 四重奏的强奏与快速经过句，用来检验连奏音程与交替弓法的边界；这是该工具常见产出的参照，不是该工具的演示（C1，参照不是该库的演示）。
  - mutopia-000498 | 完整管弦乐的动力层次，对照成套模块能否撑住大编制；这是该工具常见产出的参照，不是该工具的演示（C1，参照不是该库的演示）。
  - oga-000002 | 游戏配乐的管弦加电子层，是柏林模块被叠进 hybrid 模板的典型场景；这是该工具常见产出的参照，不是该工具的演示（C1，参照不是该库的演示）。
sources:
  - 产品线、单件售卖方式与录音场地，依厂商公开页面核查，未抄文本
  - SINE 播放器的功能范围与授权条款，依厂商文档核查，未抄文本
updated: 2026-10-30
---

::: zh
## 它能完成什么

按声部搭出一套柏林管弦，写传统配器而不是拼预制。用 Metropolis Ark 做预告片式的厚铜管与合唱冲击。单件买齐缺的声部，例如低音提琴或低音长号。用 Layers 做当代配乐的持续音与织体。在同一工程里把柏林弦乐与 Metropolis Ark 的铜管并置，也是常见做法。缺一支独奏乐器时，买对应的独奏模块即可。把分轨交出去，或在模板里只加载当前 cue 用到的模块。

## 它怎么工作

采样按声部与演奏法分模块，SINE 播放器统一读取。Teldex 录音棚的厅堂比 AIR 干，但仍有明显房间；每件乐器提供近场、AB、树麦等位置，可按 cue 调比例。演奏法用 keyswitch 或 SINE 的 articulation set 切换，常用键位可以跨库统一，连奏只覆盖录过的音程。多麦克风按需流式读取，purge 能释放不用的采样。模块按件售卖，可以先买一件再补。

## 边界与坑

第一，SINE 播放器比 Kontakt 浅：没有深层采样编辑与脚本，复杂映射要靠 DAW 侧完成。第二，厅堂声仍在，close 麦偏薄，想要完全干声的流行编曲要另找。第三，连奏音程有限，快速音阶与重复音要靠交替弓法或直接切 staccato；独奏弦乐的表现力仍不如专门的独奏库。第四，体积：单件模块几 GB 到几十 GB，整套柏林百 GB 级，必须 SSD，全模板加载慢。第五，许可：买断、账户绑定、不可转售，模块不能拆开二手卖。第六，学习成本：单件售卖意味着先想清缺什么，买错模块的钱省不回来。这套库的强项是厚，不是细。

## 替代与搭配

要更湿、更成套的影视感，换 Spitfire；要一次订阅拿到多套管弦与合唱，换 EastWest；要更干、更学院派的室内乐，换 Vienna Symphonic Library；只做史诗预告片，Metropolis Ark 本身就够，不必上柏林全套。它常与 Omnisphere 的脉冲层、Valhalla 的混响搭配，补足电子与空间。

## 上手路径

先学 articulation set 的键位组织、麦克风位置的比例、按 cue 只加载需要的模块。先在一首短曲里跑通，再读本站的管弦乐配器、采样库整理、legato 与 round-robin 三篇。

```audiolab
{"type":"instrument","gm":"String Ensemble 2","synth":"bowed","phrase":["C3","G3","C4","E4","G4"],"label":"柏林弦乐的中低音区","label_en":"Berlin strings in the lower middle","hint":"先听房间与近场的比例，再想这一句该用哪支麦克风","hint_en":"Hear the room against the close mic, then choose which signal the line needs"}
```
:::

::: en
## What it lets you finish

A Berlin orchestra can be assembled section by section for traditional orchestration rather than preset collage. Metropolis Ark supplies the thick brass and choir hits a trailer needs. Missing sections, such as double bass or bass trombone, can be bought one at a time. Layers covers the sustained tones and textures of contemporary scoring. Placing Berlin strings beside Metropolis Ark brass in one cue is standard practice. Stems can be delivered, or the template can load only the modules the current cue uses.

## How it works

Samples are split into modules by section and articulation, all read by the SINE player. The Teldex room is tighter than AIR but still audible, and each instrument offers close, AB and tree positions that can be balanced per cue. Articulations switch by keyswitch or a SINE articulation set, key layouts can be kept consistent across libraries, and legato covers only recorded intervals. Microphones stream on demand, and purge frees samples not in use. Modules are sold individually, so the library can grow one purchase at a time.

## Limits and traps

SINE is shallower than Kontakt: there is no deep sample editing or scripting, so complex mapping moves into the DAW. The room is still present, and close mics can sound thin, so a fully dry pop arrangement needs another library. Legato intervals are limited, and fast scales and repeated notes depend on alternate bowings or a switch to staccato; solo strings remain less expressive than a dedicated solo library. Size grows quickly: a module runs from a few gigabytes to tens, a full Berlin setup into the hundreds, an SSD is required, and a complete template loads slowly. Licences are perpetual, account-bound and non-transferable, and modules cannot be resold separately. Buying by module also means knowing what is missing up front; a wrong purchase cannot be recovered.

## Alternatives and pairings

Spitfire offers a wetter, more complete film sound; EastWest puts several orchestras and choirs on one subscription; Vienna Symphonic Library is drier and more academic for chamber work; for epic trailers alone, Metropolis Ark is enough without the full Berlin set. It pairs with Omnisphere pulses and a Valhalla reverb to add electronic edge and space.

## First three things to learn

Learn how an articulation set is keyed, how microphone positions change the image, and how to load only the modules a cue needs. Then read the site's orchestration, sample library organisation, legato, and round-robin entries.

```audiolab
{"type":"instrument","gm":"String Ensemble 2","synth":"bowed","phrase":["C3","G3","C4","E4","G4"],"label":"柏林弦乐的中低音区","label_en":"Berlin strings in the lower middle","hint":"先听房间与近场的比例，再想这一句该用哪支麦克风","hint_en":"Hear the room against the close mic, then choose which signal the line needs"}
```
:::
