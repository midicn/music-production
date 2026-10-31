---
id: file-naming-convention
site: prod
cat: B5
order: 384
title: 文件命名规范
title_en: File Naming Conventions
summary: 文件名是唯一跟到底的元数据，字段顺序决定它能不能排序。
summary_en: A filename is the metadata that survives every transfer; field order decides whether it sorts.
level: standard
tags: [命名, 交付, 版本, 工程整理]
tags_en: [naming, delivery, versioning, organisation]
alias: [文件命名, 命名规范, 交付命名, file naming]
links:
  - "[[glossary:stems]]"
  - "[[glossary:bus]]"
  - "[[glossary:isrc]]"
  - "[[glossary:daw]]"
instances:
  - pdmx-000600 | 《拉德茨基进行曲》声部多，导出后最容易出现同名不同版本（C1）
  - mutopia-000514 | 交响曲乐章多，按乐章与声部编号才不会错配（C1）
  - oga-000001 | 分层配乐音色多，按功能命名比按音源命名更容易找（C1）
  - pdmx-000407 | 《春》的合奏编制整齐，适合练同一套字段贯穿分轨（C1）
sources:
  - Avid Pro Tools Reference Guide，片段、文件与导出命名规则（产品文档）
  - DDEX ERN 标准，电子发行元数据字段与版本（标准）
  - EBU Tech 3293 EBUCore，音视频元数据与标识（标准）
updated: 2026-10-31
---

::: zh
## 交付之后只剩文件名

工程里的轨道名、总线名、备注，到对方手里多半看不见；能跟着文件走完整个流程的，只有文件名。命名规范的目的不是整齐，而是让陌生人在不打开工程的情况下，知道这是哪首、哪段、哪一版、哪一组。

## 字段顺序就是排序规则

| 顺序 | 字段 | 写法 | 例子 |
|---|---|---|---|
| 1 | 项目或曲目代码 | 短、唯一、无空格 | PRJ07 |
| 2 | 内容 | 段落或乐器组 | CH02_DRUMS |
| 3 | 版本 | v01 起，两位补零 | v03 |
| 4 | 日期 | YYYYMMDD | 20261031 |
| 5 | 状态 | MIX、STM、MST、REF | MIX |
| 6 | 处理标记 | 可选，采样率与位深 | 48k24b |

把版本放在日期前面，同一段落的所有版本会排在一起；把日期放前面，则按时间排。两种都能用，关键是整批一致。空格、中文、括号与井号在跨系统传输时会被替换或截断，用下划线或连字符，ASCII 字母数字最稳。

## 版本号与状态分开写

v01、v02 是修改次数，MIX、STM、MST 是文件性质，两者不能互相代替。final 不是版本号，三个月后会出现 final2 与 final_final；用 v 加数字，旧版保留，交给对方的压缩包里只放当前版和一份变更说明。客户回稿用 REF 标记，避免与正式混音混在一起。

## 交接前的检查

- 同一批文件的字段顺序、分隔符、大小写一致
- 版本号连续，没有跳号或重号
- 日期是导出日，不是工程创建日
- 采样率、位深、声道数写在名字里或随附清单里
- 压缩包内没有系统缓存文件、缩略图与旧版混入
- 名字长度在对方系统限制内，路径不要太深

## 命名救不了的事

命名不能补上缺失的元数据，也不能替代交付清单；ISRC、版权归属、联系人仍要单独给。对方若有固定模板，先按对方模板，再谈统一。最危险的是看起来一样的文件：同名不同内容，或同内容不同名，都会让后期在错误版本上做决定。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q q q q q q q q","bpm":100,"label":"八下一样的落点","label_en":"Eight identical hits","hint":"先听这串重复，再想每一版都叫 final 时，怎么找回第三版","hint_en":"Hear the repeat, then imagine every version named final and how you would find take three"}
```
:::

::: en
## After delivery, only the filename remains

Track names, bus names and notes inside the session rarely reach the other studio. The filename is what travels through the whole chain. A convention is not about tidiness; it lets a stranger tell which song, section, version and group a file belongs to without opening anything.

## Field order is sort order

| Order | Field | Form | Example |
|---|---|---|---|
| 1 | Project or song code | Short, unique, no spaces | PRJ07 |
| 2 | Content | Section or instrument group | CH02_DRUMS |
| 3 | Version | From v01, two digits | v03 |
| 4 | Date | YYYYMMDD | 20261031 |
| 5 | Status | MIX, STM, MST, REF | MIX |
| 6 | Technical tag | Optional rate and depth | 48k24b |

Put the version before the date and every version of one section sorts together; put the date first and the batch sorts by time. Either works if the whole batch agrees. Spaces, Chinese characters, brackets and hash marks get replaced or truncated across systems, so use underscores or hyphens and plain ASCII letters and digits.

## Version numbers and status are different things

v01 and v02 count revisions; MIX, STM and MST describe what the file is. One cannot stand in for the other. "Final" is not a version, and within three months there will be final2 and final_final. Number with v, keep the old versions, and put only the current one plus a change note in the package you send. Mark client reference bounces as REF so they never sit beside a real mix.

## Checks before handoff

- Field order, separators and capitalisation agree across the batch
- Version numbers run without gaps or repeats
- The date is the export date, not the session creation date
- Sample rate, bit depth and channel count appear in the name or the accompanying list
- No system cache files, thumbnails or old versions inside the archive
- Names fit the receiver's length limit and paths stay shallow

## What naming cannot fix

A filename does not supply missing metadata or replace a delivery sheet; ISRCs, rights and contacts still travel separately. If the receiver has a fixed template, follow it first and argue about standardisation later. The dangerous case is files that look alike: same name with different content, or the same content under different names, either of which lets post make decisions on the wrong version.
:::
