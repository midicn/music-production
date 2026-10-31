---
id: output-arcade
site: prod
cat: C
title: Arcade 循环音源
title_en: Output Arcade
summary: 以订阅更新的循环音源，Kit 与行按风格成组，按键触发即可铺底。
summary_en: A subscription loop instrument whose kits of tempo-locked loops are fired from the keyboard.
level: standard
tags: [循环, 采样库, 电子, 编曲]
tags_en: [loops, sample library, electronic, arranging]
alias: [Arcade, Output, Output Arcade, 循环音源]
order: 30
tool_kind: instrument
tool_vendor: Output
tool_form: 插件
tool_platforms: [macOS, Windows]
tool_price: 订阅
tool_jobs: [编曲, 声音设计, 配乐]
tool_verified: 2026-10-30
links:
  - "[[glossary:sampler]]"
  - "[[glossary:tempo]]"
  - "[[instrument:samplers]]"
instances:
  - groove-000037 | 116 BPM 的拉丁桑巴一小节鼓循环，正好用来试循环起点与叠行；这是该工具常见产出的参照（C1）
  - groove-000012 | 80 BPM 的放克鼓底，短到能听清按键切换与循环接缝；这是该工具常见产出的参照（C1）
  - oga-000076 | 四小节鼓循环，适合对照同一个 Kit 里鼓行的变体与长度；这是该工具常见产出的参照（C1）
  - oga-000267 | 近两分钟的电子织体，用来对照旋律行在结构里怎么进出；这是该工具常见产出的参照（C1）
sources:
  - 产品定位、Kit 与行结构与订阅方式——依据来自厂商公开页面。
  - 循环的使用与再分发限制，对照厂商许可说明整理。
updated: 2026-10-30
---

::: zh
## 适用工作

给广告或短视频在半小时内铺好鼓、贝斯与和声，交出一份能直接混的草稿。给播客或游戏关卡做循环背景，按段落切换 Kit 与行。用现成循环搭 demo，再让乐手把关键声部换成真录音。给电子流行加一层切片人声或质感，保留原来的律动。给现场做可触发的循环层，跟着宿主速度走。把同一条底做成长短两个版本，改结构不必重录。

## 原理

内容以 Kit 为单位：一个 Kit 是一包同风格的循环，分成鼓、贝斯、旋律、人声几行，每行有多个变体，由按键触发。循环跟随宿主速度，可以锁调；每行能改起点与长度，再叠滤波与音量。宏把常用参数收在一处，参数可以写自动化。内容随订阅更新、按需下载，已下载的 Kit 离线可用。它的本质是音频循环播放器，不是采样器：不读你自己的采样，也不改循环内部的音符。

## 边界

- 订阅：停止续费后，工程里的声音会失效；交付前要把用到的行导成分轨。
- 闭库：不能导入自己的采样，也不能改循环内部音符，只能在触发、起点、滤波这一层做文章。
- 原创性：同一批循环别人也买得到，成品容易撞；素材可用于成品，但不能单独再分发。
- 速度与调性：循环速度固定，工程速度大幅偏移会听出拉伸；调性锁不住时叠层会打架。
- 需要账户与联网验证，协作者没有同一订阅就打不开工程。
- 预混很满，多层叠起来容易糊，要主动让出频段。
- 长工程里大量触发会吃 CPU 与磁盘读取，冻结或导成分轨更稳。

## 替代

要完全可控，用采样器自己切循环，或用 Serum 一类合成器从零做；要更自由但得自己编，用 Splice 或 Loopcloud 的采样订阅；要可玩性与声音设计更深，看 Native Instruments 的 Play 系列。它常与侧链、滤波自动化、总线压缩搭配，把空间让出来；关键鼓点可以用一次性采样或真鼓替换。

## 上手

先学 Kit 与行的触发、循环起点与长度、跟随宿主速度与锁调。先在空工程里把一条鼓循环和一条旋律循环对齐，再读这里的采样器、速度、循环与片段三篇。

```audiolab
{"type":"instrument","gm":"Synth Bass 1","synth":"plucked","phrase":["C2","C2","G2","A2","C3"],"label":"一条可循环的低音动机","label_en":"A loopable bass motif","hint":"先听重复两遍是否接得住，再想这一行该让出多少频段","hint_en":"Hear whether the repeat joins cleanly, then decide how much low end this row should leave"}
```
:::

::: en
## Jobs it covers

Lay a drum, bass and harmony bed under an ad or short video and hand over a mixable draft. Build a looping background for a podcast or game level, switching kits and rows by section. Sketch a demo from loops, then have players replace key parts with real recordings. Add a sliced vocal or texture layer to electronic pop while keeping the groove. Run a triggerable loop layer live that follows tempo. Cut long and short versions of one bed without re-recording.

## How it works

Content comes as kits: loops in one style, split into rows for drums, bass, melody and vocals. Each row holds several variations fired from the keyboard. Loops follow host tempo and can be locked to a key; rows have a start point, length, filter and level. Macros gather parameters worth automating. Kits arrive through the subscription and download on demand, and downloaded kits work offline. At heart it is a loop player, not a sampler: it reads no user samples and cannot edit notes inside a loop.

## Limits

- Subscription: if it lapses, project sounds stop loading; export used rows as stems before delivery.
- Closed library: no user samples and no note-level editing, only triggering, start points and filtering.
- Originality: the same loops go to every subscriber and will collide; they may be used in finished work but not redistributed as loops.
- Tempo and key: loops have a fixed tempo, so a large tempo move exposes stretching, and stacked rows fight when keys disagree.
- It needs an account and online checks; collaborators without the subscription cannot open the project.
- Presets arrive mixed, so rows blur together and frequency space must be cleared.
- Dense triggering costs CPU and disk reads; freezing or exporting stems is steadier.

## Alternatives

For full control, chop loops in a sampler or build parts in a synth such as Serum; for a freer but more manual workflow, a Splice or Loopcloud subscription; for deeper sound design, the Play series from Native Instruments. Pair it with sidechain, filter automation and bus compression, and replace key hits with one-shots or a real kit.

## First three things

Learn kit and row triggering, loop start and length, and tempo following with key lock. Line up a drum loop and a melodic loop in an empty project, then read the site's sampler, tempo, and loops entries.

```audiolab
{"type":"instrument","gm":"Synth Bass 1","synth":"plucked","phrase":["C2","C2","G2","A2","C3"],"label":"一条可循环的低音动机","label_en":"A loopable bass motif","hint":"先听重复两遍是否接得住，再想这一行该让出多少频段","hint_en":"Hear whether the repeat joins cleanly, then decide how much low end this row should leave"}
```
:::
