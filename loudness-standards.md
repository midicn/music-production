---
id: loudness-standards
site: prod
cat: A8
title: 响度标准与真峰值
title_en: Loudness Standards and True Peak
summary: 用 LUFS 与真峰值衡量响度，让作品既够响又不削波。
summary_en: Measuring loudness with LUFS and true peak so a master can be loud enough without clipping after encoding.
level: standard
tags: [母带, 响度, LUFS, 真峰值]
tags_en: [mastering, loudness, LUFS, true peak]
alias: [LUFS, 真峰值, 响度标准, loudness standards]
links:
  - "[[glossary:lufs]]"
  - "[[glossary:true-peak-limiter]]"
  - "[[glossary:loudness-normalization]]"
  - "[[glossary:limiter]]"
instances:
  - pdmx-000585 | 贝多芬第七的节奏重音密，适合检查限制器是否把峰值压成一堵墙
  - mutopia-000037 | 阿莱格里的《求主怜悯》篇幅长而安静，适合测整首的积分响度
  - pdmx-001017 | 莫扎特第四十的交响织体，适合对照短时响度与真峰值
sources:
  - ITU-R BS.1770 与 EBU R128 的响度与真峰值定义（公开标准文本）。
  - 有损编码前留真峰值余量的做法，参考母带交付惯例。
updated: 2026-10-28
---

::: zh
响度不是峰值。一个波形看起来很满的母带，听感可能并不响；一个峰值不高的母带，整首却更有压迫感。把两者分开看，母带才有判断依据。

## 问题

只用峰值表做母带，容易把每一首推到接近 0 dBFS，转成 MP3 或 AAC 后却出现削波。也有人按 RMS 比较，结果安静段落被忽略，整首的响度仍然忽大忽小。不同平台回放时，音量一跳，作品就吃亏。

## 目标与标准

用 integrated LUFS 测整首，用 short-term LUFS 看段落，用 LRA 看动态跨度，再用 true peak 表看采样点之间的峰值。单曲母带常见目标是 -14 到 -9 LUFS，真峰值不超过 -1 dBTP；广播按 EBU R128 常以 -23 LUFS 为准。数字是起点，不是奖杯。

## 做法

先测未处理混音的整首响度，找出最响与最静段落。限制器 ceiling 设在 -1.0 dBTP，逐步加增益，每次只动 1 dB 左右。处理后再测一遍，并导出有损版本试听。若真峰值超限，先降 ceiling 或减少限制量，不要只把输出拉低。

## 听什么

听前奏、副歌与尾奏的响度差是否自然，限制器工作时低频是否抽吸，镲片是否变硬。下面这段钢琴有强弱变化，适合对照表头数字与听感。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5","G4","E4"],"label":"强弱与峰值","label_en":"Dynamics and peaks","hint":"注意渐强时是更有力，还是只剩更响","hint_en":"At the crescendo, ask whether it gains force or only volume"}
```

## 常见误解

LUFS 不是峰值表，读数相同不代表波形一样。-14 LUFS 也不是法律，不同平台、不同风格各有取舍。真峰值贴着 0 dBTP 并不专业，留 1 dB 余量才不会在转码后出事。
:::

::: en
Loudness is not peak level. A waveform that looks full may not sound loud, while lower peaks can feel more forceful.

## The problem

Mastering with a peak meter alone pushes every track toward 0 dBFS, only for MP3 or AAC encoding to clip. Comparing RMS can ignore quiet passages while the overall level still jumps.

## Goals and standards

Measure integrated LUFS for the whole track, short-term LUFS for sections, LRA for dynamic span, and true peak between samples. A common target is -14 to -9 LUFS with true peak no higher than -1 dBTP; broadcast under EBU R128 often uses -23 LUFS.

## Practice

Measure the unprocessed mix and find its loudest and quietest sections. Set the limiter ceiling to -1.0 dBTP and add gain in steps of about 1 dB. Measure again and audition a lossy encode. If true peak exceeds the limit, lower the ceiling or limit less.

## What to listen for

Hear whether intro, chorus and outro relate naturally, whether the low end pumps when the limiter works, and whether cymbals harden. The piano phrase below has dynamic contrast.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "C5", "G4", "E4"], "label": "Dynamics and peaks", "label_en": "Dynamics and peaks", "hint": "注意渐强时是更有力，还是只剩更响", "hint_en": "At the crescendo, ask whether it gains force or only volume"}
```

## Common misunderstandings

LUFS is not a peak meter; equal readings do not mean equal waveforms. Nor is -14 LUFS a law, since platforms and genres differ. Sitting at 0 dBTP is not professional either; about 1 dB of margin keeps encoding clean.
:::
