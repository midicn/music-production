---
id: platform-loudness-targets
site: prod
cat: A8
title: 各平台响度目标
title_en: Platform Loudness Targets
summary: 不同平台回放目标不同，母带响度要按发布场景取舍。
summary_en: Streaming, broadcast and club playback normalise or expect different levels, so a master's loudness should follow its release context.
level: standard
tags: [母带, 响度, 流媒体]
tags_en: [mastering, loudness, streaming]
alias: [平台响度, 流媒体响度, platform loudness]
links:
  - "[[glossary:lufs]]"
  - "[[glossary:loudness-normalization]]"
  - "[[glossary:true-peak-limiter]]"
instances:
  - pdmx-000995 | 德沃夏克第九的段落对比大，适合观察平台归一后动态是否还在
  - mutopia-001411 | 萨蒂《裸体歌舞》很安静，适合检查归一后底噪与尾音
  - essen-000024 | 短小的民歌录音，适合练习按发布场景选择保守的响度目标
sources:
  - Spotify、Apple Music 与 YouTube 的响度归一目标，依平台公开帮助文档核查，未抄文本
  - 流媒体与广播响度目标的差异，依交付与母带通识核查，未抄文本
updated: 2026-10-28
---

::: zh
平台会按自己的目标调整回放音量。母带做得过响，不一定在平台上更响，反而可能被压小。

## 问题

同一首歌在不同平台音量不同，听众一换平台就要拧旋钮。有人为追响度把单曲推到 -8 LUFS，上传后却被归一，只剩更扁的瞬态。

## 目标与标准

流媒体常见归一目标在 -14 LUFS 左右，Apple Music 偏向 -16 LUFS，广播按 EBU R128 常用 -23 LUFS，真峰值都留 -1 dBTP 左右。目标应跟发布场景走：单曲流媒体取 -14 上下，动态大的作品可更保守；俱乐部或实体可更响，但要另做版本。

## 做法

先确定主发布渠道，再定母带目标。同一张 EP 的所有曲目用同一个 integrated 目标，避免歌与歌之间跳。上传前用平台预览或手机外放试听，确认归一后没有变薄。保留一版动态更大的母带，供视频、广播或实体使用。

## 听什么

把参考曲与自己的母带调到同一响度再比较，听低频是否还在、人声是否还稳。归一后若只剩高频刺耳，说明原母带压得太狠。下面这段长笛可听弱奏的呼吸与尾音。

```audiolab
{"type":"instrument","gm":"Flute","synth":"blown","phrase":["C5","E5","G5","E5","C5"],"label":"弱奏的呼吸","label_en":"Breath in a soft line","hint":"归一之后，先听气声与尾音是否还被保留","hint_en":"After normalisation, listen for the breath and tail first"}
```

## 常见误解

平台会归一，不代表母带可以随便做响，音色与动态仍由母带决定。-14 LUFS 不是所有平台的统一值，各家算法与目标并不相同。归一也不会让压坏的瞬态恢复。
:::

::: en
Platforms adjust playback level to their own target. A very loud master may simply be turned down, its dynamics gone.

## The problem

The same song plays at different levels on different services, so listeners reach for the volume knob. Pushing a single to -8 LUFS only invites normalisation and flatter transients.

## Goals and standards

Streaming normalisation commonly sits near -14 LUFS, Apple Music leans toward -16 LUFS, and broadcast under EBU R128 often uses -23 LUFS, with true peak near -1 dBTP. Use about -14 for streaming, more conservative settings for dynamic music, and a louder separate version for club or physical use.

## Practice

Choose the release channel first, then set the target. Use one integrated target for every track on an EP. Before upload, check a platform preview or phone speaker and keep a more dynamic master for video or physical use.

## What to listen for

Match a reference and your master to the same loudness, then hear whether low end and vocal survive. If only harsh highs remain, the master was overpressed.

```audiolab
{"type": "instrument", "gm": "Flute", "synth": "blown", "phrase": ["C5", "E5", "G5", "E5", "C5"], "label": "Breath in a soft line", "label_en": "Breath in a soft line", "hint": "归一之后，先听气声与尾音是否还被保留", "hint_en": "After normalisation, listen for the breath and tail first"}
```

## Common misunderstandings

Normalisation does not mean any loudness will do, because tone and dynamics still come from the master. Nor is -14 LUFS universal; services differ. Normalisation is not quality control, since crushed transients do not return.
:::
