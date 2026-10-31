---
id: notation-musescore
site: prod
cat: B6
order: 504
title: MuseScore 工作流
title_en: A MuseScore Workflow
summary: 免费方案也能交付：先把模板、分谱与导出格式定好，再谈排版细节。
summary_en: A free tool can still deliver: settle the template, parts and export format before polishing the layout.
level: standard
tags: [MuseScore, 制谱, 开源, 教学]
tags_en: [MuseScore, notation, open source, teaching]
alias: [MuseScore 工作流, MuseScore 制谱流程, MuseScore 分谱, MuseScore workflow]
links:
  - "[[glossary:tablature]]"
  - "[[glossary:lead-sheet]]"
  - "[[instrument:classical-guitar]]"
instances:
  - thesession-000000 | 单声部舞曲，调号与反复清楚，适合课堂或社区乐团的短谱
  - nottingham-000001 | 单声部舞曲旋律短小，导入后改动少，适合检查模板与分谱
  - mutopia-000005 | 阿瓜多吉他练习曲，六线谱与标准谱并排，最考验谱表类型设置
  - pdmx-000013 | 《绿袖子》的简易改编，声部少，适合走完导出与分享
sources:
  - MuseScore Studio Handbook，音符输入、分谱与导出章节（官方文档）。
  - Elaine Gould, Behind Bars, Faber，基础版面规则。
  - MusicXML 4.0 规范，跨软件交换的字段定义。
updated: 2026-10-31
---

::: zh
给学校乐队、社区合唱团或一节吉他课做谱，MuseScore 通常够用。够用的前提是先把模板与交付格式定下来，而不是打到一半再换纸张。

## 先问这份谱给谁

给演奏者读，还是给课堂投影，决定谱表大小、纸张与是否要六线谱。给业余乐团，分谱的翻页与排练号比总谱的缩编更重要。给自己改，MusicXML 与可编辑源文件比 PDF 更重要。先答这个问题，后面的模板选择才有依据。

## 模板与谱表

New Score 里选模板，再逐件加乐器；模板缺的声部手动补，别用复制谱表硬凑。吉他用标准谱加六线谱，两条谱表链接同一份音符，改一处两边同步。合唱用歌词行，不要用文字框逐字摆。页面设置先定 A4 或 Letter 与谱表毫米数，后面再调会牵动所有断行。

## 输入与排版

步进输入最适合有明确节奏的谱，先放时值再改音高；实时输入适合即兴素材，但量化会把连奏改成格子。力度、奏法与反复从面板拖到音符上，拖到小节上不会跟着音符走。排版先调风格里的间距与字体，再手动断行；手动断行会被下一次重排覆盖，能少用就少用。

## 任务对照表

| 任务 | 在哪做 | 容易错的地方 |
|---|---|---|
| 建谱 | New Score / 模板 | 模板缺声部，后面加乐器会改版面 |
| 分谱 | Parts | 改总谱后忘了看分谱换页 |
| 吉他谱 | 链接谱表 | 两条谱表没有链接，改一处漏一处 |
| 排版 | Style / 页面设置 | 先手动断行，再改纸张，全部重来 |
| 交付 | Export | 只交 PDF，对方无法改；只交 MusicXML，版面丢失 |

## 免费方案的边界

复杂管弦乐的总谱，MuseScore 的自动间距不如商业软件稳，声部多时手动避让会变多。内置音源适合校对，不适合当成品音频；要听真实音色，仍要导 MIDI 或 MusicXML 到 DAW。MuseScore.com 的分享与下载依赖账号与订阅档位，公开谱面的授权也要自己确认。免费省下的是授权成本，不是校对时间。

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (nylon)","synth":"plucked","phrase":["E3","G3","B3","E4"],"label":"吉他谱上的两个声部","label_en":"Two voices on a guitar staff","hint":"听低音与旋律是否分得开，再想它们在六线谱与标准谱上怎样并排","hint_en":"Hear whether bass and melody stay apart, then picture them side by side in tab and staff notation"}
```
:::

::: en
For a school band, a community choir or a guitar class, MuseScore is usually enough. It is enough when the template and the delivery format are settled first, not when the paper changes halfway through.

## Who reads this score

A player reading at a stand, a class reading a projection and a guitarist reading tab need different staff sizes, paper and staves. For an amateur ensemble, page turns and rehearsal marks in the parts matter more than a condensed score. For your own edits, MusicXML and an editable source matter more than a PDF. Answer that question before choosing a template.

## Templates and staves

Pick a template in New Score, then add instruments one by one; add missing sections by hand instead of duplicating staves to fake them. For guitar, put standard notation and tablature on linked staves so both follow the same notes. Use a lyric line for a choir, not text boxes placed syllable by syllable. Set A4 or Letter and the staff size in millimetres early; changing it later moves every line break.

## Entry and layout

Step-time entry suits music with a clear rhythm: choose the duration, then the pitch. Real-time entry suits improvised material, but quantisation turns a legato line into a grid. Drag dynamics, articulations and repeats from the palette onto notes; drop them on a bar and they will not follow the note. Set spacing and fonts in Style before breaking lines by hand, because manual breaks are lost at the next reflow.

## Task table

| Task | Where | Common mistake |
|---|---|---|
| Create the score | New Score / template | A missing section changes layout when added later |
| Parts | Parts | Score edits made without checking part page turns |
| Guitar notation | Linked staves | Staves are not linked, so one edit misses the other |
| Layout | Style / page settings | Manual breaks first, paper change later, all redone |
| Delivery | Export | PDF only cannot be edited; MusicXML only loses layout |

## Limits of the free route

In a dense orchestral score, automatic spacing is less settled than in commercial software, and manual collision work grows with the number of staves. The built-in sounds are for proofing, not for a finished mix; real tone still means MIDI or MusicXML into a DAW. Sharing and downloading on MuseScore.com depend on an account and a subscription tier, and the licence of a public score is still yours to confirm. The free route saves licence cost, not proofreading time.

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (nylon)","synth":"plucked","phrase":["E3","G3","B3","E4"],"label":"Two voices on a guitar staff","label_en":"Two voices on a guitar staff","hint":"Hear whether bass and melody stay apart, then picture them side by side in tab and staff notation","hint_en":"Hear whether bass and melody stay apart, then picture them side by side in tab and staff notation"}
```
:::
