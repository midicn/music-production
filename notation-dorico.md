---
id: notation-dorico
site: prod
cat: B6
order: 500
title: Dorico 工作流
title_en: A Dorico Workflow
summary: 先建编制与 Flow，再录音符；分谱与缩编是派生物，顺序反了返工最久。
summary_en: Set the ensemble and flows before entering notes; parts and condensing are derived, and the wrong order costs the most rework.
level: standard
tags: [Dorico, 制谱, 工作流, 分谱]
tags_en: [Dorico, notation, workflow, parts]
alias: [Dorico 工作流, Dorico 制谱流程, Dorico 分谱, Dorico workflow]
links:
  - "[[glossary:score]]"
  - "[[glossary:full-score]]"
  - "[[glossary:clef]]"
instances:
  - m21-000001 | 四声部众赞歌，声部进行规矩，适合走完编制、录入、分谱的全程
  - musicnet-000248 | 木管五重奏，五件乐器各有分谱，缩编与分谱的先后最容易在这里出错
  - openscore-000008 | 舒伯特《魔王》，人声与钢琴两个谱表，歌词落位与伴奏间距一起考验版面
  - mutopia-000498 | 贝多芬第五交响曲第二乐章，声部多、系统长，适合检查缩编后的总谱
sources:
  - Steinberg Dorico 操作手册，Setup、Write、Engrave 与 Condensing 章节（官方文档）。
  - Elaine Gould, Behind Bars, Faber，总谱与分谱的版面规则。
  - MusicXML 4.0 规范，谱面交换的字段定义。
updated: 2026-10-31
---

::: zh
打开 Dorico 先点音符，是返工的起点。编制、Flow 与版面还没定，后面每加一件乐器都要重排一次。

## 先建编制，别急着打音符

Setup 里把演奏者、乐器与人数定下来，再决定这份工程分几个 Flow。一个乐章一个 Flow，或一套配乐一段一个 Flow，速度、调号与排练号各自独立。编制写错，Condensing 会把不该合并的声部并到一行，分谱也跟着错。模板里先选纸张与谱表大小，页面定得越早，后面手动避让越少。

## 六个阶段

| 阶段 | 在哪做 | 做完检查 |
|---|---|---|
| 建编制 | Setup | 乐器、人数、移调是否正确 |
| 录音符 | Write | 时值、连音线、歌词是否成句 |
| 加表情 | Write | 力度、奏法、分句是否落到音符 |
| 排版 | Engrave | 系统断点、翻页、避让是否可读 |
| 缩编与分谱 | Setup / Engrave | 合并声部是否正确，分谱是否同步 |
| 导出 | File | PDF 字体、MusicXML、音频是否完整 |

阶段之间会来回走，但每次回到前面的阶段，都要把后面的结果重新看一遍。尤其是编制变动，它会让缩编与分谱一起重算。

## 分谱是派生物，不是副本

Dorico 的分谱由总谱派生，改总谱后分谱跟着变。分谱里手动挪过的力度、换页与提示会作为局部覆盖保留；改编制时这些覆盖可能失效，需要回头看。给每份分谱单独设版面，别在总谱里替演奏者决定翻页。排练号与提示也要在分谱上检查，总谱整齐不代表分谱好读。

## 改完总谱回头查三处

一查 Condensing：加人、减人、换移调乐器后，合并行是否还成立。二查提示谱：删掉源声部后，提示可能变成空白。三查版面覆盖：总谱里拉过的间距不会自动传给分谱，分谱可能挤在一起。每次大改后导出 PDF 逐页翻，不要只看屏幕。

## 顺序错在哪

先排版后改编制，所有手动断行都要重来；先导分谱后改总谱，分谱里的旧覆盖会和新音符打架；用 MusicXML 从别处导入，音符与多数记号能带过来，手动调过的版面带不过来。Dorico 的强项是结构，结构没建对，强项就变成返工。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["D4","E4","F4","G4","A4"],"label":"总谱上的一行，分谱上的一个乐句","label_en":"One staff in the score, one phrase in the part","hint":"听五个音的呼吸，再想它在总谱与分谱上各要占几行","hint_en":"Hear the breath across five notes, then picture the space it needs in score and part"}
```
:::

::: en
Opening Dorico and typing notes first is how rework begins. Until the ensemble, the flows and the page are set, every added instrument forces another layout pass.

## Build the ensemble first

In Setup, fix the players, instruments and section sizes, then decide how many flows the project needs. One flow per movement, or one per cue, keeps tempo, key and rehearsal marks separate. A wrong ensemble makes Condensing merge voices that should stay apart, and the parts inherit the mistake. Choose paper and staff size in the template; the earlier the page is fixed, the less manual collision work later.

## Six stages

| Stage | Where | Check before moving on |
|---|---|---|
| Ensemble | Setup | Instruments, player counts and transpositions |
| Notes | Write | Durations, slurs and lyrics form a phrase |
| Expression | Write | Dynamics, articulations and phrasing sit on notes |
| Layout | Engrave | System breaks, page turns and collisions read clearly |
| Condensing and parts | Setup / Engrave | Merged staves are correct and parts follow |
| Export | File | PDF fonts, MusicXML and audio are complete |

You will move back and forth, but every return to an earlier stage means rechecking what came after. An ensemble change, in particular, recalculates condensing and parts together.

## Parts are derived

Dorico derives parts from the score, so a score edit reaches the part. Manual moves of dynamics, page turns and cues stay as local overrides; change the ensemble and those overrides may no longer apply. Give each part its own layout instead of deciding page turns for the player from the score. Check rehearsal marks and cues in the part as well; a tidy score says little about a readable part.

## Three checks after a score edit

First, condensing: after adding, removing or transposing an instrument, do the merged staves still hold? Second, cues: delete the source voice and a cue may turn blank. Third, layout overrides: spacing pulled in the score does not travel to the part, which may now be cramped. After any large edit, export a PDF and turn every page rather than trusting the screen.

## Where the order breaks

Lay out before changing the ensemble and every manual break is lost. Export parts before the score is final and old overrides fight the new notes. Import through MusicXML and notes plus most markings survive, but hand-adjusted layout does not. Dorico is strong on structure; get the structure wrong and that strength becomes the rework.

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["D4","E4","F4","G4","A4"],"label":"One staff in the score, one phrase in the part","label_en":"One staff in the score, one phrase in the part","hint":"Hear the breath across five notes, then picture the space it needs in score and part","hint_en":"Hear the breath across five notes, then picture the space it needs in score and part"}
```
:::
