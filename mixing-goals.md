---
id: mixing-goals
site: prod
cat: A6
title: 混音的目标
title_en: The Goals of Mixing
summary: 先写清谁该被听见，再决定每件乐器让出多少空间。
summary_en: Decide who should be heard first, then let every other part give up the space it does not need.
level: standard
tags: [混音, 目标, 判断, 层次]
tags_en: [mixing, goals, judgement, hierarchy]
alias: [混音目标, 清楚平衡情绪, mixing goals]
links:
  - "[[glossary:bus]]"
  - "[[glossary:panning]]"
  - "[[instrument:drum-kit]]"
  - "[[period:contemporary]]"
instances:
  - oga-000002 | 游戏场景层次多，适合检查主旋律是否始终站在最前（C1）
  - groove-000000 | 放克鼓组材料单一，适合先建立音量与频段的基线（C1）
  - openscore-000008 | 叙事歌曲角色与钢琴互相让位，能听出目标是否清楚（C1）
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook, balance and monitoring chapters — background checked, not quoted
  - David Gibson, The Art of Mixing, visual mapping of clarity and balance — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

每件乐器单独听都成立，合起来却没有主次：主唱被吉他盖住，副歌与主歌一样响，最后只能靠总线限制器硬推。问题不在音色，而在没有说清这首歌要让人先听见什么。

## 目标与判断

把目标写成一句话，按清楚、平衡、情绪排序。清楚是主信息始终可辨；平衡是频段与左右没有长期空缺或堆积；情绪是段落之间有真实的强弱差。判断用整段对比，不用独奏。先问三件事，谁领唱，谁支撑，谁只在缝隙里出现。

## 做法

先关掉所有处理，用推子排出静态平衡，让主唱或主奏在副歌最满处仍在前。再给支撑声部让出中频与声像位置，最后才加压缩、空间与自动化。每改一轮只解决一个目标，并保留上一版。

## 听什么

从副歌最满的八小节开始，确认主唱字字清楚；切到主歌，听是否突然塌掉；把总音量降到很小，听层次是否还在。下面四个音先听谁最突出。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["G3","B3","D4","G4"],"label":"四个音里谁最突出","label_en":"Which of the four notes stands out","hint":"先听整体，再追问哪个音最先抓住注意力","hint_en":"Hear the whole first, then ask which note grabs attention first"}
```

## 常见误解

以为目标是每件乐器都清楚；以为更响就是更有情绪；以为加效果器能让混乱变整齐。
:::

::: en
## The problem

Every instrument sounds fine alone, yet together they have no hierarchy. The vocal sits behind the guitar, the chorus is as loud as the verse, and the mix bus limiter is asked to create excitement. The problem is not timbre but an unstated answer to what should be heard first.

## Goal and judgement

Write the goal in one sentence and rank it as clarity, balance, emotion. Clarity means the main message stays legible. Balance means no band or side is permanently empty or crowded. Emotion means the sections differ in real intensity. Judge whole sections, never solos. Ask three questions: who leads, who supports, who appears only in the gaps.

## Method

Bypass all processing and set static faders so the lead still sits in front at the fullest chorus. Then make room for supporting parts in the midrange and stereo field. Add compression, space and automation last. Each pass should solve one goal, and keep the previous version.

## What to listen for

Start with the fullest eight bars of the chorus and check that every word of the lead is clear. Drop to the verse and hear whether the arrangement collapses. Lower the whole mix and see if the hierarchy survives. In the four notes below, notice which one stands out first.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["G3", "B3", "D4", "G4"], "label": "Which of the four notes stands out", "label_en": "Which of the four notes stands out", "hint": "先听整体，再追问哪个音最先抓住注意力", "hint_en": "Hear the whole first, then ask which note grabs attention first"}
```

## Common misconceptions

That the goal is to make every instrument clear; that louder means more emotion; that effects can organize a confused arrangement.
:::
