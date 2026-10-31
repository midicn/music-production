---
id: sibelius
site: prod
cat: C
order: 42
title: Sibelius（记谱与院校生态）
title_en: Sibelius
summary: 老牌制谱软件，强在院校教学、分谱与既有出版流程的衔接。
summary_en: A long-established notation program whose strength is teaching workflows, parts and the publishing chain around it.
level: standard
tags: [记谱, 制谱, 分谱, 教学]
tags_en: [notation, engraving, parts, education]
alias: [Sibelius, 西贝柳斯制谱, Avid Sibelius, Sibelius Ultimate]
links:
  - "[[glossary:score]]"
  - "[[glossary:full-score]]"
  - "[[instrument:voice]]"
instances:
  - musicnet-000248 | 木管五重奏乐章，五份分谱的声部独立，是院校合奏交付的参照，不是该工具的演示
  - pdmx-000600 | 进行曲短小、反复多，适合学校乐队的排练谱，是院校排练交付的参照，不是该工具的演示
  - cyberhymnal-000005 | 四声部赞美诗加管风琴，歌词与和声都规矩，是教学用谱的参照，不是该工具的演示
  - pdmx-000007 | 交响曲的钢琴缩编，是教材与排练用缩编谱的参照，不是该工具的演示
sources:
  - Sibelius 的 Dynamic Parts、Magnetic Layout 与 Review 模式；Avid 公开文档是主要依据。
  - 分谱与教学用谱的版面惯例——依据来自制谱与音乐教育资料。
tool_kind: notation
tool_vendor: Avid
tool_form: 桌面应用
tool_platforms: [macOS, Windows]
tool_price: 订阅
tool_jobs: [制谱, 分谱, 教学, 管弦乐]
tool_verified: 2026-10-30
updated: 2026-10-30
---

::: zh
Sibelius 的价值不只在软件本身，还在它周围那一整套流程：院校的课程、出版社的模板、抄谱员的习惯与指挥手里的分谱。选它，多半是为了接上这套流程。

## 适用工作

为管乐团写总谱并抽出分谱，排练前改一次调号也不用重排整份。给合唱队做带钢琴伴奏的谱，歌词、呼吸记号与钢琴缩编在同一份文件里。把配乐总谱交给抄谱员，保留批注与修改记录。让指挥在平板上看动态分谱。为教材做带指法、弓法与歌词的练习谱，并按班级复制。

## 原理

单窗口工作，Keypad 用小键盘选时值与临时记号，输入以键盘为主。Magnetic Layout 在排版时自动避让谱号、临时记号与连线。Dynamic Parts 让每份分谱独立成页，并随总谱改动同步。Review 模式加批注，云共享把分谱发给演奏者。回放走内置音源或 NotePerformer，导出 PDF、MusicXML、音频与图形。

## 边界

- 订阅制，停止续费就无法启动，旧工程也打不开。
- Magnetic Layout 解决常见碰撞，不替代排版判断，密集谱面仍要逐页看。
- 大型总谱在旧机器上滚动与重排会卡，分谱多时更明显。
- MusicXML 往返会丢手动版面与部分记号，跨软件交接要留出返工时间。
- 云共享依赖网络与 Avid 账号；教育授权绑定机构，离校后要重新授权。
- 回放音色偏旧，试听效果不代表最终音频。

## 替代

Dorico 在自动分谱与弹性间距上更强，新项目值得比较；MuseScore 免费且能跑 Linux，适合预算为零的班级；LilyPond 适合模板化批量出谱。与 Pro Tools 的配合是老流程：Sibelius 出谱，Pro Tools 录音与混音。配器阶段可以在 DAW 里试听，定稿再回 Sibelius 排版。

## 上手

先学 Keypad 输入、Dynamic Parts、Magnetic Layout 的开关。读这里的打谱与排版规范、记谱软件导论、乐谱交换格式，用一首赞美诗走完总谱到分谱。

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["C4","E4","G4","C5"],"label":"四个声部同唱一个和弦","label_en":"Four voices on one chord","hint":"听四个音是否齐，再想它们在分谱上要各自成页","hint_en":"Hear whether the four notes align, then picture each voice on its own part"}
```
:::

::: en
Sibelius matters less as a program than as a chain: courses, publisher templates, copyist habits and the parts in a conductor's hands. Most people choose it to join that chain.

## Jobs it covers

Write a wind band score and extract the parts, then change a key signature before rehearsal without redoing the layout. Set a choral piece with piano accompaniment, lyrics and breath marks in one file. Hand a score to a copyist and keep comments and revisions attached. Let a conductor read dynamic parts on a tablet. Build teaching scores with fingering, bowing and lyrics, and duplicate them for a class.

## How it works

Work happens in one window. The Keypad selects durations and accidentals, and entry is keyboard-first. Magnetic Layout moves clefs, accidentals and slurs out of each other's way during layout. Dynamic Parts give each part its own pages and keep them in step with the score. Review mode adds comments, and cloud sharing sends parts to players. Playback uses the built-in sounds or NotePerformer; export goes to PDF, MusicXML, audio and graphics.

## Limits

- It is subscription software. Stop paying and it will not start, so old projects stop opening too.
- Magnetic Layout prevents common collisions; it does not make layout decisions, and dense pages still need a human pass.
- Large scores scroll and reflow slowly on older machines, especially with many parts.
- MusicXML round trips lose manual layout and some markings; cross-program handoff needs slack in the schedule.
- Cloud sharing depends on the network and an Avid account; education licences are tied to an institution and must be replaced after leaving.
- Playback sounds are dated, and what you hear is not the finished audio.

## Alternatives

Dorico is stronger on automatic part generation and elastic spacing, and new projects deserve a comparison. MuseScore is free and runs on Linux, which suits a class with no budget. LilyPond handles templated batch output. The pairing with Pro Tools is an old workflow: Sibelius makes the score, Pro Tools records and mixes. Sketch in a DAW if you like, then return to Sibelius to engrave.

## First three things

Keypad entry, Dynamic Parts, and when to switch Magnetic Layout off. Then read Engraving and Layout Rules, Introduction to Notation Software, and Score Exchange Formats, and take one hymn from score to parts.

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["C4","E4","G4","C5"],"label":"Four voices on one chord","label_en":"Four voices on one chord","hint":"Hear whether the four notes align, then picture each voice on its own part","hint_en":"Hear whether the four notes align, then picture each voice on its own part"}
```
:::
