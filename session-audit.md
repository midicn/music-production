---
id: session-audit
site: prod
cat: A1
order: 300
title: 工程体检
title_en: Auditing a Session
summary: 在别人打开工程之前，把命名、路由、增益、插件与备份查一遍。
summary_en: Check names, routing, gain, plug-ins and backups before anyone else opens the session.
level: standard
tags: [工程, 检查, 工作流, 备份]
tags_en: [session, audit, workflow, backup]
alias: [工程体检, 工程自检, 工程检查, session audit, session check]
links:
  - "[[glossary:gain-staging]]"
  - "[[glossary:bus]]"
  - "[[glossary:plugin]]"
  - "[[glossary:patchbay]]"
instances:
  - oga-000077 | 32 条轨只落在 15 个通道，通道与轨道的对应必须先查清（GPL-3.0）
  - musicnet-000265 | 弗雷钢琴四重奏，12 条轨共用 5 个通道，弦乐与钢琴的路由容易错位（CC BY 4.0）
  - pdmx-000922 | 《春》的七条轨各走独立通道，适合核对声部与总线是否一一对应（CC0）
sources:
  - AES（Audio Engineering Society）关于工程交换、会话文档与归档的会议文献
  - Avid Pro Tools 与 Apple Logic Pro 官方用户指南中关于 I/O 设置、冻结与工程备份的章节
  - Bob Katz, Mastering Audio（Focal Press）关于增益结构与电平表的章节
updated: 2026-10-31
---

::: zh
工程在自己机器上干净，换一台电脑却少两条声部、多出 6 dB 底噪，交付当天才发现就晚了。体检查的是那些只在别处才现形的东西。

## 轨道与通道先对齐

轨道名、颜色和顺序是给人看的，通道与端口是给机器看的。两者错位时声音还在，只是去错了地方。一条 32 轨的工程只落在 15 个通道上，说明若干声部共用通道，改一个音量会连带另一个。先按声部组命名，弦乐、铜管、打击、合成各成一组，再核对每个通道的输入输出与总线归属，最后统一颜色和编号。名称不必漂亮，但要能让接手的人在十秒内找到大提琴。

## 增益要看得见

推子位置不代表电平。逐轨看峰值与 RMS，找出异常高或异常低的那几条，多半是录音增益、采样归一化或残留自动化造成的。再看总线上的插件顺序与旁通状态，尤其是限制器：前一个人为了试听挂上的限制器，会让整份工程动态失真，而推子看起来一切正常。判断方法是把总线插件全部旁通，听动态是否回来。

## 插件缺失与备份

缺插件时不要让对方随手替换。先冻结或并轨，把音色钉住，再写清用了哪个厂商、哪个版本、哪个预设。备份也不是复制一份到移动硬盘：至少三份、两种介质、一份离线，并且真的做过一次还原演练。备份要包含音频文件、采样库路径、插件预设与导出设置；只拷工程文件，换机器后仍会满屏报错。在另一台机器上打开、播放、导出，与参考逐段对比，做不出来就等于没有备份。

## 一张体检表

| 项目 | 症状 | 处理 |
|---|---|---|
| 轨道命名 | 出现 Audio 12 这类默认名 | 按声部组重命名并统一编号 |
| 通道与端口 | 两轨同通道，改一轨动两轨 | 拆通道或改输出 |
| 增益 | 单轨峰值贴顶、总线却很低 | 从源头修正，不靠推子补 |
| 插件 | 打开时提示缺失 | 冻结或并轨，记录版本与预设 |
| 备份 | 只有一份工程文件 | 补音频、预设，并做还原演练 |

## 查过头的地方

体检也会查过头。把时间花在颜色和图标上，不如先确认通道与备份。工程体检只能发现结构问题，修不了编曲：声部打架、低频过多、段落没有起伏，这些要回到编曲与混音解决。终点不是一份完美清单，而是另一个人能打开、能播放、能继续做。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["D3","A3","D4","F4","A4","F4","D4","A3"],"label":"三条弦乐轨，还是一条","label_en":"Three string tracks or one","hint":"听内声部有没有被盖住，再决定合并还是让路","hint_en":"Listen for a buried inner line before merging or clearing space"}
```
:::

::: en
A session that plays cleanly on your machine can open elsewhere with two parts missing and six decibels of extra noise. Find that on delivery day and it is already too late. An audit happens before anyone else opens the file, and it looks for what only shows up somewhere else.

## Tracks and channels first

Track names, colours and order are for people. Channels and ports are for the machine. When the two disagree, sound still plays, just in the wrong place. Thirty-two tracks landing on fifteen channels means several parts share a channel, so moving one fader moves another. Name by section first, strings, brass, percussion and synths each in a group, then verify every channel's input, output and bus assignment, and only then unify colours and numbers. Names need not be elegant, but a stranger should find the cello within ten seconds.

## Gain you can see

Fader position is not level. Read peak and RMS track by track and look for the outliers, usually caused by recording gain, sample normalisation or leftover automation. Then inspect plug-in order and bypass state on the buses, especially limiters. A limiter left on from a listening test flattens the whole session while every fader looks reasonable. Bypass the bus chain and hear whether the dynamics return.

## Missing plug-ins and backups

When a plug-in is missing, do not let the recipient substitute something similar. Freeze or print the track, pin the sound, and write down the maker, version and preset. A backup is not a copy on an external drive either: three copies, two media, one offline, and a restore you have actually performed. A session backup includes audio files, sample library paths, plug-in presets and export settings. Copy only the project file and the next machine greets you with a wall of errors. To test, open on another machine, play, export, and compare section by section with the reference. If you cannot, you have no backup.

## One audit sheet

| Item | Symptom | Action |
|---|---|---|
| Track names | Defaults such as Audio 12 | Rename by section, number consistently |
| Channels and ports | Two tracks share one channel | Split the channel or change outputs |
| Gain | One track pinned, bus very low | Fix at the source, not with faders |
| Plug-ins | Missing on open | Freeze or print, log version and preset |
| Backup | A single project file | Add audio, presets, and a restore test |

## Where the audit goes too far

An audit can also waste a day. Time spent on colours and icons is better spent on channels and backups, and re-normalising every track destroys the dynamics that were already right. An audit finds structural faults; it cannot fix arrangement. Parts that fight, too much low end, sections without contrast, all belong to arranging and mixing. The point is not a perfect checklist but a session another person can open, play and continue.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["D3", "A3", "D4", "F4", "A4", "F4", "D4", "A3"], "label": "Three string tracks or one", "label_en": "Three string tracks or one", "hint": "Listen for a buried inner line before merging or clearing space", "hint_en": "Listen for a buried inner line before merging or clearing space"}
```
:::
