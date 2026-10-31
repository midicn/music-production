---
id: scoring-workflow
site: prod
cat: A9
title: 配乐工作流程
title_en: The Scoring Workflow
summary: 读本、spotting、写 cue、录音与混录，配乐靠流程管理而不是等灵感。
summary_en: Script, spotting, cues, sessions and the mix: scoring runs on process rather than waiting for inspiration.
level: standard
tags: [配乐流程, 读本, 时码, 录音, 交付]
tags_en: [scoring workflow, spotting, timecode, recording, delivery]
alias: [配乐流程, 配乐工作流, scoring workflow, spotting]
links:
  - "[[glossary:cue]]"
  - "[[glossary:score]]"
  - "[[glossary:daw]]"
instances:
  - pdmx-000027 | 柴可夫斯基《胡桃夹子》全剧，按场次编号的舞曲可看作一套完整 cue 表
  - pdmx-001192 | 格里格《培尔·金特》戏剧配乐，前奏、间奏与舞曲各有明确功能
  - pdmx-000092 | 门德尔松《仲夏夜之梦》配乐，序曲与场景曲的次序对应戏剧结构
sources:
  - Davis, Richard，Complete Guide to Film Scoring（Berklee Press）— 从 spotting 到录音的流程核对，未引用
  - Kalinak, Kathryn，Film Music — A Very Short Introduction（Oxford University Press）— 配乐制作环节核对，未引用
updated: 2026-10-28
---

::: zh
配乐看起来是作曲，实际更像一条生产线：读本、定 spot、写 cue、做 mockup、录音、混录，每一步都有交付物。

## 问题

导演不会等你慢慢找灵感。片子锁剪之后，配乐要在固定窗口内完成，还要通过试映修改。没有流程，改动会层层返工，最后连主题都被改散。

## 流程

先读本并与导演过一遍 spotting，标出需要音乐与需要安静的位置。每个 spot 写成一条 cue，注明起止时码、情绪、配器与参考。写完先做 mockup 给剪辑试用，确认后再进录音棚。录音按 cue 分批，混录时把音乐压到对白之下，最后交付分轨与不同版本。

## 做法与判断

每条 cue 只解决一个问题，长度跟着画面而不是跟着乐段。给修改留出版本号与备用段落。判断一条 cue 是否完成，看它进入与退出是否自然，而不是看它单独播放时是否完整。

## 听什么

听《胡桃夹子》里各段舞曲如何按场次切换，听《培尔·金特》前奏怎样在几小节内建立地点，听《仲夏夜之梦》序曲怎样把全剧材料先摆出来。演示用钢琴弹一条八小节的短 cue，注意它如何起、如何收。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","B4","A4","G4","E4","C4"],"label":"一条八小节的短 cue","label_en":"A short eight-bar cue","hint":"听它怎样在最后一小节收住，为下一场留出进入点","hint_en":"Hear it close in the last bar and leave room for the next scene"}
```

## 常见误解

流程不是创作的对立面，它把时间留给真正需要判断的地方。demo 通过也不等于配乐完成，录音与混录会改变平衡。另一点，导演要改的常常不是音符，而是进入点与长度。
:::

::: en
Scoring looks like composing but behaves like a production line: read the script, spot the film, write cues, make mockups, record, mix. Each stage has a deliverable.

## The problem

A director will not wait while you look for inspiration. Once the cut is locked, the score must be finished inside a fixed window and revised after test screenings. Without a process, each change causes another round of rework until the themes come apart.

## The workflow

Read the script and go through spotting with the director, marking where music is needed and where silence is. Turn each spot into a cue with start and end timecode, mood, instrumentation and references. Build a mockup, confirm it, then book the session. Record cue by cue, mix under dialogue, and deliver stems and alternates.

## Practice and judgement

One cue should solve one problem, and its length follows the picture, not a musical form. Keep version numbers and alternates for revisions. A cue is finished when its entrance and exit feel natural, not when it sounds complete alone.

## What to listen for

Hear The Nutcracker's dances change scene by scene, the Peer Gynt prelude establish a place in a few bars, and the Midsummer overture lay out the play's material. The demo is an eight-bar piano cue; notice how it starts and closes.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "B4", "A4", "G4", "E4", "C4"], "label": "A short eight-bar cue", "label_en": "A short eight-bar cue", "hint": "听它怎样在最后一小节收住，为下一场留出进入点", "hint_en": "Hear it close in the last bar and leave room for the next scene"}
```

## Common misunderstandings

Process is not the enemy of creation; it protects time for judgement. A passed demo is not a finished score, since recording and mixing change the balance. Directors usually want the entrance and length changed, not notes.
:::
