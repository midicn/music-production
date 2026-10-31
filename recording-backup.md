---
id: recording-backup
site: prod
cat: A4
title: 录音备份
title_en: Recording Backup
summary: 只存在一块盘上的录音等于没录，备份要能独立还原
summary_en: A take that lives on one drive is not recorded. A backup must restore on its own.
level: standard
tags: [录音, 备份, 数据]
tags_en: [recording, backup, data]
alias: [备份, 多份备份, 数据安全, backup, redundancy, archive]
links:
  - "[[glossary:daw]]"
  - "[[glossary:stems]]"
instances:
  - giantmidi-004397 | 六十多分钟的连续录音，重录成本最高
  - mutopia-000180 | 十二分钟一次成型，没有补录的机会
  - atepp-000841 | 多乐章奏鸣曲工程，音频与工程文件要一起备份
sources:
  - IASA TC-04, Guidelines in the Production and Preservation of Digital Audio Objects
  - AES Convention paper on audio archive redundancy and checksums
updated: 2026-10-28
---

::: zh
## 问题

一次录音只存在一块盘上，等于没有录。硬盘会坏，工程会误删，备份必须能在主盘消失后独立还原，而不是同一块盘上的另一个文件夹。

## 信号链

录音机写入工作盘，收工后复制到第二块盘，再留一份异地或云端。工程文件、音频、插件预设与录音日志要一起走，缺一项都可能还原不出来。

## 摆位与参数

采用三份副本、两种介质、一份异地。每份带日期与工程名，只增不改。当天收工前完成复制，并抽查一条轨能否播放；每月做一次完整还原演练。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","D4","E4","G4"],"label":"一条无法重来的轨","label_en":"A take that cannot be redone","hint":"听这四个音，想象它只留在一块盘上","hint_en":"Hear these four notes and picture them living on a single drive"}
```

## 听什么

备份本身听不见，但可以验证：从备份盘打开工程，随机播三段，确认不缺文件、不错位。再对照原始轨的电平与时长，确认复制完整。

## 常见误解

- **备份就是复制文件夹** → 没做还原演练的备份只是猜测。
- **RAID 可以代替备份** → 它防盘坏，不防误删。
- **云端自动同步就够了** → 同步也会把误删同步过去。
:::

::: en
## The problem

A take that exists on one drive is not recorded. Drives fail and projects get deleted, so a backup has to restore on its own after the main copy is gone, not sit in another folder on the same disk.

## Signal chain

The recorder writes to the working drive; after the session the files are copied to a second drive and one copy goes off-site or to the cloud. Project files, audio, plug-in presets and the session log travel together, because missing one of them can block the restore.

## Placement and settings

Use three copies, two kinds of media and one off-site. Label every copy with the date and project name, and only add, never overwrite. Finish the copy before leaving, spot-check that one track plays, and run a full restore test once a month.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "D4", "E4", "G4"], "label": "A take that cannot be redone", "label_en": "A take that cannot be redone", "hint": "听这四个音，想象它只留在一块盘上", "hint_en": "Hear these four notes and picture them living on a single drive"}
```

## What to listen for

Backups are silent, so verify them: open the project from the backup drive, play three random sections and confirm nothing is missing or shifted. Compare level and duration with the original tracks to prove the copy is complete.

## Common misconceptions

- **A backup is a copied folder** → without a restore test it is only a guess.
- **RAID replaces backup** → it survives a failed drive, not a deletion.
- **Cloud sync is enough** → sync also copies the mistake.
:::
