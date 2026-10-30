---
id: native-instruments-komplete
site: prod
cat: C
title: Komplete 综合音源包
title_en: Native Instruments Komplete
summary: 一套买断的综合音源包，用广度覆盖 demo，深度要另找专库。
summary_en: A perpetual bundle that covers a demo through breadth, while depth still comes from dedicated libraries.
level: standard
tags: [采样库, 综合音源, Kontakt, 合成器]
tags_en: [sample library, bundle, Kontakt, synths]
alias: [Komplete, NI, Native Instruments, Kontakt, Massive X, Battery]
order: 26
tool_kind: instrument
tool_vendor: Native Instruments
tool_form: 插件
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [编曲, 声音设计, 配乐]
tool_verified: 2026-10-30
links:
  - "[[glossary:sampler]]"
  - "[[instrument:software-synth]]"
  - "[[instrument:drum-kit]]"
instances:
  - atepp-000195 | 弱奏钢琴的层次与踏板，用来检验综合包里的钢琴能否撑住独奏段；这是该工具常见产出的参照，不是该工具的演示（C1，参照不是该库的演示）。
  - musicnet-000296 | 弦乐四重奏的连奏与力度，对照综合包里的室内乐音色能达到什么程度；这是该工具常见产出的参照，不是该工具的演示（C1，参照不是该库的演示）。
  - groove-000014 | 爵士放克的鼓组律动，是 Battery 与 Studio Drummer 最常被要求的写法；这是该工具常见产出的参照，不是该工具的演示（C1，参照不是该库的演示）。
  - oga-000163 | 锯齿合成器与鼓的叠加，对应 Massive X 与 Reaktor 在游戏配乐里的用法；这是该工具常见产出的参照，不是该工具的演示（C1，参照不是该库的演示）。
sources:
  - 捆绑包版本分层与所含产品，依厂商公开页面核查，未抄文本
  - Native Access 授权与升级方式，依厂商文档核查，未抄文本
updated: 2026-10-30
---

::: zh
## 它能完成什么

用一套授权覆盖 demo 需要的大部分音色：钢琴、鼓、贝斯、合成器、弦乐。用 Session Strings 与 Session Horns 快速铺流行编曲的弦乐与铜管。用 Kontakt 加载第三方音色库，把不同厂商的库放进同一模板。用 Battery 做鼓组与切片。用 Massive X 或 FM8 做电子音色。用 Damage 与 Rise & Hit 做预告片冲击。它也能当作 Kontakt 的入口，之后只补需要的第三方库，也常被用来给视频配乐做第一版。它适合从零开始做完整的编曲草稿。

## 它怎么工作

核心是 Kontakt 采样器，加上合成器与鼓机；Native Access 负责安装、授权与更新。Kontakt 的库可以放在外置 SSD，按需 purge 释放内存；Battery 的每个鼓格可单独输出。音色以 patch 为单位，可多输出到 DAW 分轨；NKS 键盘能直接浏览与调参。捆绑包按版本分层，买得越高，包含的库越多。

## 边界与坑

第一，广而不深：管弦乐不如专门的管弦库，原声钢琴不如 Pianoteq 或采样钢琴专库，独奏弦乐更明显。第二，体积：Standard 过百 GB，Ultimate 以 TB 计，装完要留出系统盘与备份空间。第三，大版本升级要再付费，旧工程的 patch 可能在新版里改名或消失，Kontakt 大版本对旧库的兼容要看厂商。第四，授权走 Native Access，转售需厂商同意，第三方 Kontakt 库各有自己的条款。第五，捆绑包容易买多：真正每天用的可能只有三五个音色。第六，Reaktor 与 Massive X 的 CPU 占用高于采样库。第七，安装与授权依赖网络，离线机器要先完成离线授权。第八，部分钢琴与鼓的预混很重，进混音时反而要拆。买之前先列清单，别按打包的惯性下单。

## 替代与搭配

只要管弦，买 Spitfire 或 Orchestral Tools 更对路；只要合成器，Serum 与 Pigments 更专注；只要钢琴，Pianoteq 更轻；已有 Kontakt 时，只买缺的库比升级整套更省。它常作为底座，把专库当作 Kontakt 里的补充，而不是替代，这是折中。

## 上手路径

先学 Kontakt 的库管理与多输出、Battery 的分轨、Native Access 的安装。先在模板里固定三条总线，再读本站的采样库整理、合成器导论、微时序与律动三篇。

```audiolab
{"type":"instrument","gm":"Electric Piano 1","synth":"struck","phrase":["C3","E3","G3","B3","D4"],"label":"综合包里的一架电钢","label_en":"An electric piano from the bundle","hint":"先听音头与衰减，再想它该被当成钢琴还是当成音色层","hint_en":"Hear the attack and decay, then decide whether it is a piano or a layer"}
```
:::

::: en
## What it lets you finish

One licence covers most of a demo: piano, drums, bass, synths, strings. Session Strings and Session Horns lay down pop string and brass parts quickly. Kontakt loads third-party libraries, putting several vendors in one template. Battery handles drum kits and slices. Massive X or FM8 supplies electronic tones. Damage and Rise & Hit provide trailer impacts. It also serves as an entry into Kontakt, and as a first pass for video scoring. It is built for finishing a full arrangement sketch from an empty project.

## How it works

Kontakt is the sampler at the centre, joined by synths and drum machines; Native Access handles installation, authorisation and updates. Libraries can live on an external SSD, purge frees memory on demand, and Battery sends each pad to its own output. Sounds are patches that can output to separate DAW channels, and NKS keyboards browse and edit them directly. The bundle is tiered, and higher tiers add more libraries.

## Limits and traps

Breadth is not depth: orchestral sounds fall short of a dedicated orchestra, acoustic pianos fall short of Pianoteq or a sampled piano library, and solo strings show it most. Size is the second issue: Standard passes a hundred gigabytes and Ultimate reaches terabytes, so system and backup space must be planned. Major upgrades cost again, and patches can be renamed or dropped, while Kontakt's compatibility with older libraries depends on the vendor. Authorisation runs through Native Access, resale needs vendor approval, and third-party Kontakt libraries carry their own terms. Bundles also invite over-buying, when three or five sounds do the daily work. Reaktor and Massive X cost more CPU than sample libraries. Installation needs a network, so offline machines must be authorised offline first, and some pianos and drums arrive heavily processed, which means undoing a mix before mixing.

## Alternatives and pairings

For orchestral work only, Spitfire or Orchestral Tools is the better route; for synths only, Serum and Pigments are more focused; for piano only, Pianoteq is lighter; if Kontakt is already owned, buying the missing libraries beats a full upgrade. Komplete serves as a base, with dedicated libraries added inside Kontakt rather than replaced.

## First three things to learn

Learn Kontakt library management and multiple outputs, Battery's separate channels, and how Native Access installs libraries. Set three fixed buses in a template first, then read the site's sample library organisation, synthesis introduction, and microtiming and groove entries.

```audiolab
{"type":"instrument","gm":"Electric Piano 1","synth":"struck","phrase":["C3","E3","G3","B3","D4"],"label":"综合包里的一架电钢","label_en":"An electric piano from the bundle","hint":"先听音头与衰减，再想它该被当成钢琴还是当成音色层","hint_en":"Hear the attack and decay, then decide whether it is a piano or a layer"}
```
:::
