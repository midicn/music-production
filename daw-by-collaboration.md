---
id: daw-by-collaboration
site: prod
cat: C
order: 49
title: 按协作与工程交换选
title_en: Choosing a DAW by Collaboration and Exchange
summary: 先定哪些东西必须可改，再选交换格式与宿主，而不是先买软件。
summary_en: Decide what must stay editable first, then pick the interchange format and the host that supports it.
level: standard
tags: [协作, 交换, AAF, 交付]
tags_en: [collaboration, interchange, AAF, delivery]
alias: [按协作选 DAW, 工程交换, AAF 交付, 协作选型]
links:
  - "[[glossary:daw]]"
  - "[[glossary:stems]]"
  - "[[glossary:automation]]"
instances:
  - openscore-000001 | 人声与钢琴的艺术歌曲，谱面与音频都要交给别人，是乐谱交换的参照，不是本页演示
  - oga-000004 | 分层战斗曲，层与层要分开交，是分轨交换的参照，不是本页演示
  - musicnet-000248 | 木管五重奏，五份分谱各自独立，是多方交付的参照，不是本页演示
  - mutopia-000789 | 人声与钢琴的叙事小品，速度与力度变化多，是交换后要不要重建的参照，不是本页演示
sources:
  - AAF、OMF 与 MusicXML 能携带的内容，依通行 DAW 与制谱文档核查，未抄文本
  - 声像法则、采样率与时间码对交换的影响，依后期流程资料核查，未抄文本
tool_kind: guide
tool_vendor: 本站
tool_form: 流程
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [选型, 协作]
tool_verified: 2026-10-30
updated: 2026-10-30
---

::: zh
协作选型的第一步不是选软件，而是问对方拿到工程要改什么。只改平衡，给分轨；要挪片段，给交换格式；要改音符，给乐谱文件。答案不同，宿主也不同。

## 要判断什么

先问对方要改到哪一层：平衡、时值、音符还是触发逻辑。再问版本与插件：有没有同款宿主、同大版本、同插件。最后问交付介质：文件多大、能否嵌入媒体、用什么盘传。

## 选择表

交影视后期，用 Pro Tools 的 AAF 导出，保留片段位置、音量与淡变；与编曲或作曲交换，用 MusicXML，Dorico、Sibelius 与 MuseScore 都读得动；与远程混音师交换，用分轨加时间码，统一 48 kHz、24 bit，并从 0:00 开始；与游戏团队交换，用 Wwise 或 FMOD 的工程与 bank 版本，附事件表；现场交接，用工程副本、场景列表与备份机。

## 三种情形

短片交声音后期：在 Cubase 或 Logic Pro 里把音乐并轨，导出 AAF 加参考视频，确认起始时间码与帧率，附一份音乐提示表。跨国编曲：主旋律用 MusicXML 交给 Dorico 或 Sibelius 出谱，音频走分轨，别传整个工程。游戏更新：Wwise 工程与 Unity 插件版本一起锁，事件改名要同步表。

## 边界与坑

- 插件与自动化基本带不走，AAF 只保留基础音量与淡变。
- 声像法则不同，导入后平衡会变，要重新对一遍。
- OMF 是旧格式，长工程与嵌入媒体容易出问题，优先 AAF。
- 采样率与时间码不一致，整条会偏移，交付前双方确认。
- 工程版本不同，打开会提示缺失或静默替换。
- 云盘同步工程时，二进制文件冲突会损坏工程。

## 怎么开始

先做一次空工程交换测试：一段音乐、一条对白、一个淡变，走完导出与导入再正式交付。读本站的工程交换格式、协作与工程交付、Stems 交付三页。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","B4","A4","G4","E4","D4"],"label":"一段要被别人接着改的素材","label_en":"Material someone else has to keep editing","hint":"听句尾有没有留出余地，再想交换后哪一处最难重建","hint_en":"Hear whether the phrase leaves room, then judge what would be hardest to rebuild after the handoff"}
```
:::

::: en
The first step in choosing for collaboration is not choosing software. It is asking what the other person must change. Balance only, send stems. Move clips, send an interchange file. Change notes, send a score. Each answer points to a different host.

## What you are deciding

Ask how deep the other side must edit: balance, timing, notes or trigger logic. Ask about versions and plug-ins: same host, same major version, same plug-ins. Ask about delivery media: file size, embedded or referenced audio, and which drive carries it.

## The decision table

For picture post, export AAF from Pro Tools, keeping clip positions, levels and fades. For arranging and composition, use MusicXML, which Dorico, Sibelius and MuseScore all read. For a remote mixer, send stems with timecode, all at 48 kHz and 24 bit, starting at 0:00. For a game team, exchange Wwise or FMOD projects and bank versions with an event list. For a stage handoff, supply a project copy, a scene list and a spare machine.

## Three cases

A short film to sound post: bounce the music in Cubase or Logic Pro, export AAF plus a reference video, confirm start timecode and frame rate, and attach a music cue sheet. A co-arranger abroad: send the melody as MusicXML for Dorico or Sibelius to engrave, send audio as stems, and never send the whole project. A game update: lock the Wwise project and the Unity plug-in version together, and update the event table when names change.

## Limits and traps

- Plug-ins and automation rarely travel; AAF keeps basic level and fades only.
- Pan law differs, so the balance shifts on import and must be checked again.
- OMF is an old format; long sessions and embedded media break easily, so prefer AAF.
- A sample-rate or timecode mismatch shifts everything; both sides confirm before delivery.
- Different project versions produce missing items or silent substitutions on open.
- Cloud sync of a live project can corrupt binary files on a conflict.

## How to start

Run an empty-session exchange first: one music cue, one dialogue line, one fade, exported and imported before the real delivery. Read Session Interchange Formats, Collaboration and Handoff, and Delivering Stems alongside.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","B4","A4","G4","E4","D4"],"label":"Material someone else has to keep editing","label_en":"Material someone else has to keep editing","hint":"Hear whether the phrase leaves room, then judge what would be hardest to rebuild after the handoff","hint_en":"Hear whether the phrase leaves room, then judge what would be hardest to rebuild after the handoff"}
```
:::
