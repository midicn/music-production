---
id: adobe-audition
site: prod
cat: C
order: 46
title: Audition（播客与对白后期）
title_en: Audition
summary: 以波形与频谱为核心的后期工具，擅长播客、对白清理与老录音修复。
summary_en: A waveform and spectrogram editor for podcast post, dialogue cleanup and restoration rather than music production.
level: standard
tags: [后期, 播客, 对白, 修复]
tags_en: [post-production, podcast, dialogue, restoration]
alias: [Audition, Adobe Audition, 播客后期, 对白修复]
links:
  - "[[glossary:de-esser]]"
  - "[[glossary:noise-floor]]"
  - "[[glossary:signal-to-noise]]"
instances:
  - atepp-001111 | 钢琴演奏转写为MIDI的音符，不包含原录音嘶声 | Piano-performance notes transcribed to MIDI without original recording hiss
  - cyberhymnal-000003 | 管风琴旋律参照，不保留原乐器机械噪声 | Organ-melody reference without original mechanical noise
  - mutopia-000001 | 人声与钢琴的谱面声部，不是真实口播录音 | Scored voice-and-piano parts rather than recorded speech
  - openscore-000005 | 声部强弱的音乐参照，压缩比较须另制音频 | A musical reference for part dynamics; compression comparison needs separate audio renders
sources:
  - "https://helpx.adobe.com/premiere/desktop/use-premiere-with-other-apps/working-with-other-adobe-applications/edit-premiere-sequences-in-audition.html"
  - Audition 的波形、频谱显示与 Match Loudness（Adobe 公开文档）。
  - 播客与对白的降噪、去齿音与响度做法，参考后期制作惯例。
tool_kind: plugin
tool_vendor: Adobe
tool_form: 桌面应用
tool_platforms: [macOS, Windows]
tool_price: 订阅
tool_jobs: [播客, 对白后期, 修复, 音频编辑]
tool_verified: 2026-10-30
updated: 2026-11-02
---

::: zh
Adobe Audition 提供波形编辑、多轨混音、频谱处理和音频后期。它可用于对白、播客、音乐编辑与交付；若任务主要依赖MIDI编曲和虚拟乐器，应先检查它是否满足该工作流，而不是把所有音乐制作都排除在外。

## 能替你做完什么

把一段四十分钟的双人对谈修到可发布，响度对齐平台要求。去掉空调嗡声、键盘敲击与椅子吱呀，同时保住说话的瞬态。把采访里的口水音与过长停顿修顺，剪掉口误而不留接缝。给视频做对白替换与音效铺底，再按场景导出。批量把三十条口播统一响度并导出 MP3。

## 它怎么工作

波形编辑适合处理单个文件，多轨会话组织对白、音乐和效果。Premiere 的序列可发送到 Audition 多轨会话，视频可通过 Dynamic Link 引用；音频修改如何返回，要按所选导出或链接混音流程确认，不能理解为两边所有剪辑与插件都双向实时同步。响度匹配也应先选定交付规范，再核对测量结果。

## 哪里会坑你

- 先验证所需的MIDI、乐器与工程交换方式
- 保存原始素材、会话和可独立打开的音频输出
- 频谱与降噪处理应逐段检查伪影
- 与其他软件交换时核对通道、起点和插件依赖
- 批处理前先试一份，并检查异常素材

## 换成什么

选工具时比较实际任务：单文件修复、对白剪辑、多轨混音还是工程协作。把同一小段素材走完导入、处理、导出和重新打开，核对格式与交接成本，比直接按品牌判断谁更专业更可靠。

## 先学三件事

先学频谱显示与降噪、Match Loudness、多轨会话的总线。读这里的音频修复、播客片头、响度标准与真峰值，用一段带空调噪声的对白走完修复到导出。

```audiolab
{"type":"instrument","gm":"Voice Oohs","synth":"vocal","phrase":["C4","D4","E4","G4"],"label":"旋律与衰减素材","label_en":"Melody-and-decay material","hint":"合成音色没有原录音的气口、磁带嘶声或机械噪声。修复演示需要真实且获授权的带噪音频。","hint_en":"The synthesized timbre contains no original-recording breaths, tape hiss or mechanical noise. Restoration examples need real, authorised noisy audio."}
```
:::

::: en
Adobe Audition provides waveform editing, multitrack mixing, spectral tools and audio post-production. It can support dialogue, podcasts, music editing and delivery. For MIDI sequencing and virtual instruments, check workflow support rather than assuming all music production is outside its role.

## What it finishes for you

Clean a forty-minute two-person interview until it is publishable, with loudness matched to the platform. Remove air-conditioning hum, keyboard clicks and chair creaks while keeping speech transients. Smooth mouth noise and long pauses, and cut fluffs without audible seams. Replace dialogue and lay sound effects under picture, then export per scene. Batch thirty voice spots to one loudness target and export MP3.

## How it works

Waveform editing handles individual files; multitrack sessions organise dialogue, music and effects. Premiere sequences can be sent to Audition, with video referenced through Dynamic Link. Confirm how audio returns through the selected export or linked-mix workflow rather than assuming all edits and plug-ins synchronise bidirectionally. Choose a delivery specification before loudness matching and verify the measurements.

## Where it bites

- Verify required MIDI, instrument and session-exchange workflows first
- Preserve source media, sessions and independently readable audio exports
- Check spectral and denoising artifacts section by section
- Confirm channels, time origin and plug-in dependencies when exchanging
- Test one file before batch processing and inspect outliers

## What to swap in

Compare tools for the actual task: file restoration, dialogue editing, multitrack mixing or collaboration. Run one small asset through import, processing, export and reopening, checking format and handoff cost rather than ranking professionalism by brand.

## First three things

The spectral display and noise reduction, Match Loudness, and bus structure in a multitrack session. Then read Audio Restoration, A Podcast Intro, and Loudness Standards and True Peak, and take one dialogue clip with air-conditioning noise from repair to export.

```audiolab
{"type":"instrument","gm":"Voice Oohs","synth":"vocal","phrase":["C4","D4","E4","G4"],"label":"Melody-and-decay material","label_en":"Melody-and-decay material","hint":"The synthesized timbre contains no original-recording breaths, tape hiss or mechanical noise. Restoration examples need real, authorised noisy audio.","hint_en":"The synthesized timbre contains no original-recording breaths, tape hiss or mechanical noise. Restoration examples need real, authorised noisy audio."}
```
:::
