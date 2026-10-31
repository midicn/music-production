---
id: mixing-introduction
site: prod
cat: A6
title: 混音导论
title_en: Introduction to Mixing
summary: 混音要解决谁在何时被听见，而不是把每件乐器都做好听。
summary_en: Mixing decides who is heard and when, not how good each track sounds on its own.
level: standard
tags: [混音, 工作流, 判断, 入门]
tags_en: [mixing, workflow, judgement, beginner]
alias: [混音, 混音入门, 混音流程, mixing, mixdown]
links:
  - "[[glossary:bus]]"
  - "[[glossary:automation]]"
  - "[[instrument:drum-kit]]"
  - "[[period:contemporary]]"
instances:
  - oga-000002 | 游戏场景编制多、层次杂，适合练从整体到局部的听法
  - pdmx-000450 | 勃拉姆斯《德意志安魂曲》动态跨度大，合唱与乐队的关系清楚
  - groove-000000 | 放克鼓循环材料单一，适合先建立音量与频段的基线
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook, balance and monitoring chapters.
  - Huber and Runstein, Modern Recording Techniques, mixdown chapter.
updated: 2026-10-28
---

::: zh
## 问题

多轨工程里每件乐器单独听都成立，合在一起却像一堵墙。混音要处理的不是音色好不好，而是谁在什么时候被听见。

## 目标与判断

三个目标按顺序排：清楚、平衡、情绪。清楚指主要信息不被遮住；平衡指各频段与左右位置没有长期缺口或堆积；情绪指副歌比主歌更有推力。判断靠对比，不靠单轨独奏。先问这首歌最重要的一条线是什么，再决定其他声部让出多少空间。

## 做法

先关掉所有处理，只推推子做静态平衡；用总线压缩与均衡只修整体；再回到单轨处理频段冲突；最后加空间与自动化。每一步都留一版，隔一天回听。参考曲目只用来校准响度与频段，不照搬音色。

## 听什么

从副歌最满的八小节开始，听主唱或主奏是否始终在前；切到主歌，听是否突然空掉；再把总音量降得很低，听平衡是否还在。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","G3","E4","G4"],"label":"钢琴四音","label_en":"Four piano notes","hint":"先听整体轮廓，再分辨每个音的位置","hint_en":"Hear the overall shape first, then locate each note"}
```

## 常见误解

以为混音就是加效果；以为独奏好听就等于混音成立；以为响度越大越专业。
:::

::: en
## The problem

Every track sounds fine alone; together they form a wall. Mixing is not about making each sound pretty. It decides who is heard, when, and at what distance.

## Goal and judgement

Three goals in order: clarity, balance, emotion. Clarity means the main message is never buried. Balance means no band or side is permanently empty or crowded. Emotion means the chorus pushes harder than the verse. Judge by comparison, never by solo. Ask which single line carries the song, then decide how much room everything else gives it.

## Method

Turn off processing and set static faders first. Fix the whole picture with bus EQ and compression. Return to tracks for masking. Add space and automation last. Keep a version at each step and listen again the next day. Use a reference only to calibrate level and spectrum, not to copy timbre.

## What to listen for

Start at the fullest eight bars of the chorus and check that the lead stays in front. Drop to the verse and hear whether the arrangement collapses. Then lower the whole mix and see if the balance survives.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C3", "G3", "E4", "G4"], "label": "Four piano notes", "label_en": "Four piano notes", "hint": "先听整体轮廓，再分辨每个音的位置", "hint_en": "Hear the overall shape first, then locate each note"}
```

## Common misconceptions

That mixing means adding effects; that a good solo means a good mix; that louder is more professional.
:::
