---
id: job-live-set
site: prod
cat: D
order: 7
title: 电子现场
title_en: An Electronic Live Set
summary: 把电子现场的准备、冗余与响度做成可执行的清单。
summary_en: Prepare an electronic live set with printed audio, tested redundancy and a loudness plan that survives the room.
level: standard
tags: [流程, 现场, 电子, 冗余]
tags_en: [workflow, live, electronic, redundancy]
alias: [电子现场, live set, 现场演出, 演出准备]
links:
  - "[[glossary:headroom]]"
  - "[[instrument:polysynth]]"
instances:
  - groove-000010 | 两分多钟的放克鼓型，可听一段律动怎样靠细微变化维持长度，是现场素材的参照，不是本页演示
  - groove-000011 | 三分半的同速律动，适合练长段落的能量管理，不是本页演示
  - oga-000089 | 一分多钟的循环曲，结构稳定，可参考现场如何留出切换空间，不是本页演示
  - giantmidi-008518 | 五十秒的电子音乐练习，音色与织体偏电子，可对照现场音色的层次，不是本页演示
sources:
  - 现场演出的工程准备、备份与试场做法；现场演出惯例是主要依据。
  - 主输出余量、真峰值与限制器的用法——依据来自现场扩声惯例。
tool_kind: guide
tool_vendor: 本站
tool_form: 流程
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [流程]
tool_verified: 2026-10-30
updated: 2026-10-30
---

::: zh
## 你要交的是什么

一场 30–45 分钟的电子现场：一套能在场地里跑完的工程、可独立播放的备份，以及一份给场地方的输出清单。场地方要的是能直接进调音台的信号，不是你的工程文件。交立体声主输出与分轨备份，48 kHz、24 bit；所有素材提前打印成音频，不依赖只装在你这台电脑上的插件。另附节目单、每首的起始场景、调性与响度目标。

## 三步走

先搭模板：主输出链、限制器、提示轨、节拍器与备用通道，固定采样率与缓冲区。第二步把每首整理成场景：前奏、主段、breakdown、回到主段，标好切换点；能打印的打印，不能打印的写清插件与预设；每首的结尾写成可循环的尾段，超时也能自然收。第三步试场：在场地的系统上放一遍，检查低频、相位与响度，留 6 dB 余量，再演练一次断电与换机。

## 用到的工具与页面

DAW 或现场宿主、控制器与限制器就够；这里的工程模板与响度表两页先读。别把限制器当音色，它只防削波。备份用另一台电脑加一个装满 WAV 的 U 盘，U 盘里的版本不依赖任何插件。带一副熟悉的耳机，场地监听不可信时用它核对。演出前把电脑的睡眠、通知与自动更新全部关掉，再把输出电平表调到能一眼看见的位置。

## 验收标准

整套节目能连续播放 30 分钟以上，没有空白；限制器前留 6 dB 余量，主输出峰值不超过 -1 dBTP；每首的切换点在节拍上；备份设备能在五分钟内接管；场地系统上低频不糊、相位不空；节目单与实际播放顺序一致；从第一首到最后一首，手不用离开控制器超过十秒；断电后能从头恢复。

```audiolab
{"type":"rhythm","sig":"4/4","bpm":128,"pattern":"q q q q","cycles":2,"label":"四拍循环能不能一直推","label_en":"Can a four-on-the-floor loop keep pushing","hint":"听第二遍，若没有新的层进来，现场就会平","hint_en":"Hear the second pass; without a new layer entering, the room goes flat"}
```

## 常见返工原因

工程依赖没装的插件，到场打开是静音；只带一台电脑，没有备份；限制器拉得太狠，鼓点没有起伏；采样率设错，速度整体偏；没有试场，低频在俱乐部里翻倍；节目单与工程不一致，台上找不到下一首；没给场地方输出清单，调音台找不到你的通道；把笔记本的自动更新留在演出时段。
:::

::: en
## What you have to hand over

A thirty-to-forty-five-minute electronic live set: a session that runs in the venue, an independent playback backup, and an output list for the venue. Deliver a stereo master output and stem backups at 48 kHz and 24 bit. Print every part to audio in advance; do not depend on plug-ins installed only on your laptop. Add a setlist, the opening scene of each track, keys and loudness targets.

## Three steps

Build a template first: master chain, limiter, cue track, click and a spare channel, with fixed sample rate and buffer. Second, turn each track into scenes: intro, main, breakdown, return, with switch points marked. Print what can be printed; for what cannot, write down the plug-in and preset. Third, test in the room: play the set through the venue system, check low end, phase and loudness, leave 6 dB of headroom, then rehearse a power cut and a machine swap.

## Tools and pages

A DAW or live host, a controller and a limiter are enough. Read the site pages Session Templates and Loudness Metering first. Do not treat the limiter as a sound; it only prevents clipping. Back up on a second computer plus a USB drive full of WAV files, and make the USB version free of plug-ins. Before doors, disable sleep, notifications and automatic updates, and place the output meter where you can see it at a glance.

## Acceptance checks

The set plays continuously for at least thirty minutes with no silence. Leave 6 dB before the limiter; master peaks stay below -1 dBTP. Every switch lands on a beat. The backup can take over within five minutes. Low end is not muddy and phase is not hollow in the venue. The setlist matches the running order. After a power cut, the set can restart from the top.

```audiolab
{"type":"rhythm","sig":"4/4","bpm":128,"pattern":"q q q q","cycles":2,"label":"四拍循环能不能一直推","label_en":"Can a four-on-the-floor loop keep pushing","hint":"听第二遍，若没有新的层进来，现场就会平","hint_en":"Hear the second pass; without a new layer entering, the room goes flat"}
```

## Why work gets sent back

The session needs a plug-in that is not installed and opens silent. Only one laptop is brought, with no backup. The limiter is pushed so hard that the drums lose their shape. The sample rate is wrong and the whole set runs at the wrong speed. Nobody tested in the room and the bass doubles in the club. The setlist and the session disagree and the next track cannot be found. Automatic updates are left scheduled during the show.
:::
