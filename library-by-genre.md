---
id: library-by-genre
site: prod
cat: C
order: 51
title: 按体裁选采样库
title_en: Choosing Sample Libraries by Genre
summary: 先定写作方式与演奏法需求，再挑采样库的录音、体量与授权。
summary_en: Match a sample library to how you write and which articulations you need before comparing its sound.
level: standard
tags: [采样库, 选型, 管弦, 音源]
tags_en: [sample libraries, selection, orchestral, instruments]
alias: [按体裁选采样库, 采样库怎么选, 音源选择, sample libraries by genre]
links:
  - "[[instrument:violin]]"
  - "[[instrument:drum-kit]]"
  - "[[instrument:erhu]]"
instances:
  - mutopia-000498 | 交响曲慢乐章，编制完整，是管弦库要还原的参照，不是本页演示
  - pdmx-000021 | 当代敬拜歌曲的钢琴改编，句法与流行歌相近，是流行制作的参照，不是本页演示
  - oga-000020 | 场景循环曲，段落短、可重复，是游戏配乐的参照，不是本页演示
  - nottingham-000003 | 单声部民间舞曲，装饰音与呼吸都在，是民族与民间库的参照，不是本页演示
sources:
  - 管弦、流行、游戏与民族采样库的录音方式与授权范围，依厂商公开资料核查，未抄文本
  - 演奏法、麦克风位与流式读取的取舍，依采样制作通识核查，未抄文本
tool_kind: guide
tool_vendor: 本站
tool_form: 流程
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [选型, 音源]
tool_verified: 2026-10-30
updated: 2026-10-30
---

::: zh
采样库的差别不只在音色，还在它假设你怎么写：写总谱、写 loop、写歌，还是写氛围。先定写法，再看演奏法与录音。

## 要判断什么

先定写作方式。再看演奏法：需要多少连奏、跳音与力度层，切换是否顺手。再看录音：录在多大的厅、有几支麦克风、近场与远场能否分开。最后看机器与授权：内存、硬盘、能否商用、能否用于游戏。

## 选择表

管弦用 Spitfire Audio 系列、Orchestral Tools、EastWest 影视管弦，差别在厅、编制与麦克风位；流行用 Superior Drummer 的鼓、Komplete 的综合包、Omnisphere 的合成音色；游戏用可分层、可循环、起音短的库，用 Kontakt 承载，Heavyocity 与 Soundiron 常被提起；民族用 Kong Audio、三体科技这类中国乐器库，或 Best Service 的民族系列。

## 三种情形

短片配乐：一套中型管弦库加一架钢琴，先解决连奏与力度切换，够写完三分钟。流行制作：鼓与键盘优先，贝斯用合成或采样，别一次买整套。游戏：选能拆层、能循环、尾音可切的库，先与 Wwise 或 FMOD 的容器对齐。

## 边界与坑

- 试听曲是混过的，干声进来往往差一截。
- 麦克风位越多，硬盘与内存压力越大，小机器先关远场。
- 授权按用途分，游戏、影视、再分发各有限制。
- 民族库的音准、律制与演奏法差异大，写之前先确认。
- 大而全的套装容易只用其中一成。
- 采样库不能替代配器判断，声部打架时换库也没用。

## 怎么开始

先写八小节，再决定买什么：写不出来是配器问题，音色不对才是库的问题。用同一段旋律试三套库的连奏与强弱。读本站的素材与循环库整理、轮替采样与奏法切换、配器导论三页。

```audiolab
{"type":"instrument","gm":"Trumpet","synth":"brass","phrase":["C4","E4","G4","C5"],"label":"同一支小号，三套库的连奏不同","label_en":"One trumpet line, three libraries, three legatos","hint":"听音与音之间有没有气息，再想试听曲里藏掉了什么","hint_en":"Hear the air between notes, then ask what the demo mix concealed"}
```
:::

::: en
Sample libraries differ less in tone than in how they assume you write: a score, a loop, a song or an atmosphere. Settle the writing first, then look at articulation and recording.

## What you are deciding

Decide how you write. Then count articulations: how many legato, staccato and dynamic layers you need, and whether switching feels natural. Then read the recording: how large the hall, how many microphones, and whether close and far can be separated. Finally check the machine and the licence: memory, drive, commercial use, game use.

## The decision table

For orchestral work, Spitfire Audio, Orchestral Tools and EastWest differ in hall, section size and microphone positions. For pop, Superior Drummer for drums, Komplete for the broad package, Omnisphere for synth textures. For games, choose libraries that split into layers, loop cleanly and start short, hosted in Kontakt, with Heavyocity and Soundiron often mentioned. For regional instruments, Chinese libraries such as Kong Audio and Three Body Technology, or the ethnic series from Best Service.

## Three cases

A short film: one mid-size orchestral library plus a piano, with legato and dynamic switching solved first, is enough for three minutes. Pop production: drums and keys first, bass from synth or samples, and no all-in-one bundle on day one. A game: pick libraries that split, loop and cut tails, and align them with Wwise or FMOD containers first.

## Limits and traps

- Demo tracks are mixed; the dry samples usually land a step behind.
- More microphone positions mean more drive and memory pressure; small machines should mute the far mics.
- Licences split by use, with separate limits for games, film and redistribution.
- Regional libraries differ in tuning, temperament and playing technique; confirm before writing.
- Large bundles tend to use one tenth of their content.
- A library cannot replace orchestration judgement; swapping libraries will not fix clashing parts.

## How to start

Write eight bars before buying anything: if it will not come, the problem is orchestration; if the tone is wrong, it is the library. Play one melody through three libraries and compare legato and dynamics. Read Organizing Samples and Loops, Round Robin and Articulation Switching, and Introduction to Orchestration alongside.

```audiolab
{"type":"instrument","gm":"Trumpet","synth":"brass","phrase":["C4","E4","G4","C5"],"label":"One trumpet line, three libraries, three legatos","label_en":"One trumpet line, three libraries, three legatos","hint":"Hear the air between notes, then ask what the demo mix concealed","hint_en":"Hear the air between notes, then ask what the demo mix concealed"}
```
:::
