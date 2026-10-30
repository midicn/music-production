---
id: pianoteq
site: prod
cat: C
title: Pianoteq 物理建模钢琴
title_en: Pianoteq
summary: 用模型算出来的钢琴，几十 MB、加载几乎瞬时，代价是 CPU 与近场真实感。
summary_en: A modelled piano that installs in tens of megabytes and loads instantly, paid for in CPU and close-mic realism.
level: standard
tags: [钢琴, 物理建模, 虚拟乐器, 采样库]
tags_en: [piano, physical modelling, virtual instrument, sample library]
alias: [Pianoteq, Modartt, 建模钢琴, 物理建模钢琴]
order: 28
tool_kind: instrument
tool_vendor: Modartt
tool_form: 插件
tool_platforms: [macOS, Windows, Linux]
tool_price: 买断
tool_jobs: [编曲, 现场演出, 录音]
tool_verified: 2026-10-30
links:
  - "[[instrument:piano]]"
  - "[[instrument:digital-piano]]"
  - "[[glossary:velocity]]"
instances:
  - atepp-001114 | 肖邦叙事曲的 rubato 与大幅力度变化，是这类建模钢琴最常被拿来对照的独奏素材；这是该工具常见产出的参照（C1，参照不是该库的演示）
  - atepp-000195 | 德彪西《月光》的弱奏与踏板层次，用来检验模型的低力度响应；这是该工具常见产出的参照（C1，参照不是该库的演示）
  - atepp-000369 | 格里格夜曲的长句与半踏板，是判断共鸣与衰减是否自然的参照；这是该工具常见产出的参照（C1，参照不是该库的演示）
  - giantmidi-003263 | 萨蒂《裸体歌舞》的极弱与长持续音，最容易暴露模型在高频上的干净感；这是该工具常见产出的参照（C1，参照不是该库的演示）
sources:
  - 建模方式、版本分层与扩展乐器，依厂商公开页面核查，未抄文本
  - 授权与系统要求，依厂商文档核查，未抄文本
updated: 2026-10-30
---

::: zh
## 它能完成什么

给古典钢琴录音做替换或补录，不必找采样库。用 MIDI 重新演一遍旧录音，保留原来的速度与分句。给独奏钢琴 demo 做出可判断的演奏层次。给教学或排练做慢速版本，不改音高。用电钢、竖琴、钢片琴扩展音色做配器色彩。它也能给作曲者当练琴与试奏工具，录音前用它定速度与分句。它也常被用来给视频配乐里的钢琴做快速草稿。在低配笔记本上跑钢琴，不占采样盘。现场用独立版当轻量钢琴。

## 它怎么工作

物理建模：琴弦、琴槌、共鸣板、踏板各自是模型，按键时实时算出声，不读采样。模型按琴槌击弦的位置与速度计算，弱奏不会像采样那样跳层；不同琴型是同一引擎换参数与脉冲响应。参数改动随预设保存。参数可调琴槌硬度、弦长、共鸣、麦克风位置；踏板支持半踩。独立版与插件都能用，MIDI 响应细。

## 边界与坑

第一，CPU：复音多、共鸣与半踏板开启时负载高，缓冲设小容易爆。第二，音色偏干净：近场细节与录音室采样钢琴不同，独奏对比会听出模型味。第三，房间里没有真实厅堂，要自己加混响；想要现成的近、中、远麦克风，得上 Standard 或 Pro。第四，扩展乐器另购，型号多，按项目挑。第五，授权绑定账户，转售与转让受限。第六，大版本升级收费，旧工程的参数要重调。第七，快速重复音与极端强奏的瞬态不如顶级采样库自然。第八，独立版的工程管理与 DAW 不同，现场要提前存好预设。

## 替代与搭配

要采样钢琴的质感，换 Kontakt 钢琴库或 Keyscape；要舞台电钢，换 Nord 类硬件或 Arturia 的采样电钢；只要轻量运行，Stage 版够用。它常与混响、EQ 搭配，补空间与亮度。

## 上手路径

先学麦克风与琴槌参数、半踏板、CPU 与缓冲设置。先在一段 8 小节的古典片段里对比，再读本站的钢琴、数码钢琴、力度三篇。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","B4","C5"],"label":"模型钢琴的一条短句","label_en":"A short line on the modelled piano","hint":"先听弱到强的过渡是否连续，再想采样库会在哪里断层","hint_en":"Hear whether the soft-to-loud transition is continuous, then ask where samples would step"}
```
:::

::: en
## What it lets you finish

Replace or patch a classical piano recording without hunting for a sample library. Give a solo piano demo playing levels that can be judged. Add electric piano, harp or celesta models as orchestral colour. It also works as a practice and audition instrument, setting tempo and phrasing before a recording. Run a piano on a modest laptop without a sample drive. Use the standalone build as a light live piano.

## How it works

Physical modelling: strings, hammers, soundboard and pedals are each a model, and sound is computed as keys are pressed rather than read from samples. The model calculates hammer position and velocity, so soft playing does not step between layers, and different piano models are the same engine with new parameters and impulse responses. Changes are saved with the preset. Hammer hardness, string length, resonance and microphone position are adjustable, and the pedal supports half-pedalling. Both standalone and plugin builds work, with fine MIDI response.

## Limits and traps

CPU comes first: high polyphony with resonance and half-pedalling is expensive, and small buffers crackle. The tone is clean, and close detail differs from a studio sample piano, so a solo comparison reveals the model. There is no real hall in the box, so reverb must be added; ready-made close, mid and far microphones require Standard or Pro. Additional instruments are sold separately, and a full set is a large collection to manage. Licences are account-bound with restricted resale and transfer. Major upgrades are paid, and old project settings need re-dialling. Fast repeated notes and extreme fortissimos are less natural than a mature sample library. The standalone build manages sessions differently from a DAW, so live presets must be saved in advance.

## Alternatives and pairings

For sample-piano texture, use a Kontakt piano library or Keyscape; for a stage electric piano, a Nord-style instrument; for a light setup, the Stage edition is enough. It pairs with reverb and EQ to add space and brightness.

## First three things to learn

Learn microphone and hammer settings, half-pedalling, and CPU with buffer size. Then read the site's piano, digital piano, and velocity entries.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","B4","C5"],"label":"模型钢琴的一条短句","label_en":"A short line on the modelled piano","hint":"先听弱到强的过渡是否连续，再想采样库会在哪里断层","hint_en":"Hear whether the soft-to-loud transition is continuous, then ask where samples would step"}
```
:::
