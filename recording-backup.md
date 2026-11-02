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
  - giantmidi-004397 | 长篇钢琴 MIDI 文件，可作为文件清单与恢复练习的材料 | A long piano MIDI file for file-inventory and restoration exercises
  - mutopia-000180 | 器乐 MIDI 文件，文件时长不证明一次性现场录制 | An instrumental MIDI file; its duration does not establish a one-take recording
  - atepp-000841 | 奏鸣曲音符文件，可与项目说明一起练习归档 | Sonata-note data that can be archived with project notes
sources:
  - IASA TC-04, Guidelines in the Production and Preservation of Digital Audio Objects
  - AES Convention paper on audio archive redundancy and checksums
updated: 2026-11-02
---

::: zh
## 问题

一次录音只存在一块盘上，等于没有录。硬盘会坏，工程会误删，备份必须能在主盘消失后独立还原，而不是同一块盘上的另一个文件夹。

## 信号链

录音机写入工作盘，收工后复制到第二块盘，再留一份异地或云端。工程文件、音频、插件预设与录音日志要一起走，缺一项都可能还原不出来。

## 摆位与参数

采用三份副本、两种介质、一份异地。每份带日期与工程名，只增不改。当天收工前完成复制，并抽查一条轨能否播放；每月做一次完整还原演练。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","D4","E4","G4"],"label":"短句文件参照","label_en":"Short-phrase file reference","hint":"音符不能证明备份可靠。下载或导出后核对文件清单，并从独立副本实际打开，才是恢复测试。","hint_en":"Notes cannot establish backup reliability. Verify a file inventory after export and open an independent copy for a restoration test."}
```

## 听什么

恢复演练要从另一块盘或新目录开始，把原工作盘暂时移出搜索路径，确认工程不会悄悄引用原文件。核对 take 数量、起点、时长与离线媒体提示，再抽查播放。插件授权或旧版本无法恢复时，干声、分轨与最终参考混音能保留作品，但不能替代原始工程的编辑能力。

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
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","D4","E4","G4"],"label":"Short-phrase file reference","label_en":"Short-phrase file reference","hint":"Notes cannot establish backup reliability. Verify a file inventory after export and open an independent copy for a restoration test.","hint_en":"Notes cannot establish backup reliability. Verify a file inventory after export and open an independent copy for a restoration test."}
```

## What to listen for

Restore to another drive or a new directory, temporarily keeping the working drive outside the search path so the session cannot silently reference originals. Check take count, start positions, durations and missing-media warnings before spot playback. If plug-in licences or old versions cannot be restored, dry tracks, stems and a reference mix preserve sound, but not every editing capability of the original session.

## Common misconceptions

- **A backup is a copied folder** → without a restore test it is only a guess.
- **RAID replaces backup** → it survives a failed drive, not a deletion.
- **Cloud sync is enough** → sync also copies the mistake.
:::
