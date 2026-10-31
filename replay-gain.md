---
id: replay-gain
site: prod
cat: B5
title: 回放增益
title_en: ReplayGain
summary: 按测量响度给每首加增益标签，随机播放不再忽大忽小。
summary_en: Measured gain tags even out playback so shuffled tracks no longer jump in level.
level: standard
tags: [响度, 归一, 回放, 随机播放]
tags_en: [loudness, normalization, playback, shuffle]
alias: [回放增益, ReplayGain, 响度归一, replay gain]
links:
  - "[[glossary:loudness-normalization]]"
  - "[[glossary:lufs]]"
  - "[[glossary:loudness-war]]"
instances:
  - cyberhymnal-000785 | 管风琴圣诗音量饱满，随机播放时会把前后曲目压下去（C1）
  - giantmidi-009128 | 鲁特琴独奏音量很小，回放增益把它提到与合奏同一电平（C1）
  - oga-000001 | 游戏管弦编制响度大，与独奏相邻时落差要靠增益抹平（C1）
sources:
  - ReplayGain 的测量与标签机制（公开规范与播放器文档）。
  - EBU R128 响度测量的通识，参考公开标准资料。
updated: 2026-10-28
---

::: zh
## 问题

不同录音的电平差得很远，随机播放时一首震耳、下一首几乎听不见。回放增益按测量值写一个增益标签，播放时自动把电平拉齐。

## 原理

工具先测曲目响度，早期用加权 RMS，现在多用 EBU R128 的 LUFS，再与参考值比较得出增益。也可以写专辑增益，保留专辑内部的强弱关系。播放器读到标签后在输出前施加增益，必要时加限幅防止削波。它不改音频数据，只改回放电平。

## 参数与做法

随机播放用单曲模式，整张专辑用专辑模式。目标常用负 18 LUFS 左右。开启防削波，防止峰值过满刻度。改过标签后要重新扫描。流媒体平台用自己的归一，不读本地标签。

## 听什么

让管风琴圣诗与鲁特琴独奏相邻播放，听开启前后的落差。注意弱奏细节是否还在，峰值是否被限幅压平。再听专辑内部，强奏与弱奏的相对关系是否保留。

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"reed","phrase":["C3","G3","C4","E4","G4"],"label":"饱满的管风琴和弦","label_en":"A full organ chord","hint":"听完它再换一首独奏，比较开启回放增益前后的落差","hint_en":"Then play a quiet solo and compare the jump with and without gain"}
```

## 常见误解

回放增益会改写文件，它只写标签。它会压缩动态，单曲模式只改整体电平，不改变曲内起伏。开了就都一样响，测量误差与限幅仍会留下差别。它也不等于母带响度标准。
:::

::: en
## The question

Recordings differ widely in level, so shuffle jumps from deafening to silent. ReplayGain measures each track and writes a gain tag that playback applies automatically.

## How it works

The tool measures loudness, historically with weighted RMS, now usually with EBU R128 LUFS, then compares it with a reference to derive a gain. Album gain can preserve relative levels inside an album. The player reads the tag and applies gain before output, limiting if needed. No audio data changes, only playback level.

## Settings and practice

Use track mode for shuffle and album mode for whole albums. The target commonly sits near -18 LUFS. Enable clipping protection so gain cannot push peaks past full scale. Rescan after editing tags. Streaming services normalise on their own and ignore local tags.

## What to listen for

Play an organ hymn beside a lute solo and hear the jump with gain on and off. With it on, check whether quiet detail survives and peaks flatten under limiting. Then listen inside one album, where loud and soft movements should keep their relationship.

```audiolab
{"type": "instrument", "gm": "Church Organ", "synth": "reed", "phrase": ["C3", "G3", "C4", "E4", "G4"], "label": "A full organ chord", "label_en": "A full organ chord", "hint": "听完它再换一首独奏，比较开启回放增益前后的落差", "hint_en": "Then play a quiet solo and compare the jump with and without gain"}
```

## Common misconceptions

ReplayGain does not rewrite files, only tags. It does not compress dynamics; track mode changes overall level, not the shape within a track. It does not make everything equally loud, since measurement error and limiting leave differences. It is not a mastering loudness standard.
:::
