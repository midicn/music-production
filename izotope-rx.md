---
id: izotope-rx
site: prod
cat: C
order: 16
title: RX（修复）
title_en: RX (Restoration)
summary: 频谱里直接改，噪声、嗡声与咔嗒各有对应工具。
summary_en: Edit inside the spectrogram, with a dedicated tool for noise, hum and clicks.
level: standard
tags: [插件, 修复, 降噪, 频谱编辑]
tags_en: [plugin, restoration, noise reduction, spectral editing]
alias: [RX, iZotope RX, 音频修复, spectral repair, 降噪插件]
tool_kind: plugin
tool_vendor: iZotope
tool_form: 插件
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [修复, 影视配乐, 母带]
tool_verified: 2026-10-30
links:
  - "[[glossary:noise-floor]]"
  - "[[glossary:transient-shaper]]"
  - "[[glossary:phase]]"
instances:
  - thesession-022200 | 传统曲调的音符参照，不记录原演奏的弓弦摩擦（C1） | Traditional-tune notes without recorded bow friction (C1)
  - mutopia-000001 | 声乐与钢琴的谱面声部，不是待分离的混合录音（C1） | Scored voice-and-piano parts rather than a mixed recording for separation (C1)
  - essen-000009 | 民歌旋律的符号记录，不包含田野录音的环境声音（C1） | Symbolic folk-melody data without field-recording ambience (C1)
sources:
  - "https://www.izotope.com/community/blog/audio-artifacts"
  - iZotope 官方产品页的模块与独立应用说明（公开资料）。
  - 谱减降噪、去嗡与去咔嗒的常见做法，参考修复惯例。
updated: 2026-11-02
---

::: zh
## 能替你做完什么

RX用于分析和处理录音中的噪声、点击、失真或其他局部问题。能修到什么程度取决于原始信息和问题的重叠，不能保证把任何手机铃声、混响或缺失片段无痕去掉。先保留原件，再用代表片段验证需要的模块。

## 它怎么工作

不同模块可能使用检测、滤波、插值或学习模型，不宜都解释为从频谱中做减法。频谱选区可定位特定时频事件，但选区范围与周围可用素材影响结果。修复助手给的是处理起点，仍需核对节目类型、保留目标和实际伪影。

## 哪里会坑你

- 对同一片段保留原始、处理和差分监听版本
- 检查瞬态、语音可懂度和低电平细节
- 批处理前验证多种代表片段与异常文件
- 保存处理设置及可独立打开的最终音频
- 交接前核对使用版本、模块与许可条件

## 换成什么

用相同的困难片段比较可选工具，关注修复效果、处理时间、可撤销性与工程交接。对白、音乐母带和档案转录的保留目标不同，不应把某一品牌或固定串联方案当作所有项目的标准。

## 先学三件事

先学噪声采样与降噪量的临界点，再学频谱修复的选区，最后学去嗡与去咔嗒的顺序。配合「音频修复」「本底噪声」「瞬态」三篇读。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G4","A4","B4","D5","B4","A4","G4"],"label":"弦乐音符参照","label_en":"String-note reference","hint":"这里没有带噪录音或RX处理。应使用获授权的实际录音，检查修复前后被保留和被损伤的细节。","hint_en":"There is no noisy recording or RX processing here. Use authorised actual recordings to assess detail retained or damaged by restoration."}
```
:::

::: en
## What it finishes for you

RX analyses and processes noise, clicks, distortion and other recording problems. Recovery depends on overlap with wanted information; it cannot guarantee transparent removal of every ringtone, reverb or missing section. Preserve the original and test required modules on a representative excerpt.

## How it works

Modules may use detection, filtering, interpolation or learned models rather than one spectral-subtraction principle. Spectral selection locates time-frequency events, but selection extent and available neighbouring material affect reconstruction. Assistant suggestions are starting points; check programme type, preservation goals and artifacts.

## Where it bites

- Retain original, processed and difference-audition versions of an excerpt
- Check attacks, speech intelligibility and low-level detail
- Test representative passages and outlier files before batching
- Preserve settings and independently readable final audio
- Confirm versions, modules and licence conditions before handoff

## What to swap in

Compare candidate tools on the same difficult excerpt for result, time, reversibility and handoff. Dialogue, music mastering and archival transfer have different preservation goals; one brand or fixed chain is not a universal standard.

## First three things

Learn noise sampling and the point where reduction starts to damage, then how to make a spectral selection, then the order of de-hum and de-click. Read the site's pages on audio restoration, noise floor and transients alongside it.

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G4","A4","B4","D5","B4","A4","G4"],"label":"String-note reference","label_en":"String-note reference","hint":"There is no noisy recording or RX processing here. Use authorised actual recordings to assess detail retained or damaged by restoration.","hint_en":"There is no noisy recording or RX processing here. Use authorised actual recordings to assess detail retained or damaged by restoration."}
```
:::
