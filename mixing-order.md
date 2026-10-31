---
id: mixing-order
site: prod
cat: A6
title: 混音顺序
title_en: The Order of Mixing
summary: 先地基后主次，先平衡后处理，顺序对了每一步都更省力。
summary_en: Foundation before hierarchy, balance before processing; a sound order makes every later step easier.
level: standard
tags: [混音, 工作流, 顺序, 平衡]
tags_en: [mixing, workflow, order, balance]
alias: [混音流程, 处理顺序, mixing order]
links:
  - "[[glossary:bus]]"
  - "[[glossary:automation]]"
  - "[[instrument:drum-kit]]"
  - "[[period:contemporary]]"
instances:
  - oga-000002 | 游戏场景层数多，按地基到主次的顺序最容易搭起来（C1）
  - musicnet-000097 | 弦乐四重奏只有四层，顺序错了会立刻听出来（C1）
  - openscore-000008 | 人声与钢琴关系清楚，适合先定主唱再铺伴奏（C1）
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook, mix preparation and workflow.
  - David Gibson, The Art of Mixing, building a mix from foundation upward.
updated: 2026-10-28
---

::: zh
## 问题

打开工程就从第一轨开始加均衡，推到哪算哪；遇到问题就独奏，越修越碎；混了三小时，主唱还没进过整段。顺序混乱时，每个决定都在和上一个决定打架。

## 目标与判断

先地基，再主次，再细节。鼓与贝斯给出节奏与低频的底，主唱或主奏确定前景，和声与键盘填中景，效果与加花放最后。判断标准是每一步都能在整段里站住，而不是单轨好听。若后一步推翻了前一步，就回到上一步，不要在错误的地基上继续装修。

## 做法

先清理工程、统一增益、标好段落。用推子做静态平衡，再从鼓与贝斯开始处理，接着是人声，最后是吉他、键盘与效果。总线处理放在单轨之后，自动化放在最后。每完成一段存一版，隔一天回听再决定下一步。

## 听什么

听副歌进入时层次是否自然，主唱是否一开口就在前，低频是否从头到尾稳定。下面四个音按顺序出现，注意先建立的是哪一层。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","G3","E4","C5"],"label":"一层一层搭起来","label_en":"Built one layer at a time","hint":"听低音、和声、旋律加入的先后","hint_en":"Hear the order in which bass, harmony and melody arrive"}
```

## 常见误解

以为存在唯一正确的顺序；以为先加均衡更专业；以为独奏好听就能拼成好混音。
:::

::: en
## The problem

Open the session and start EQing the first track, pushing faders wherever the ear leads. Every problem is solved in solo, so the work fragments. Three hours later the lead vocal has never been heard in context. With no order, each decision fights the one before it.

## Goal and judgement

Foundation first, hierarchy second, detail last. Drums and bass establish rhythm and low end, the lead vocal or instrument defines the foreground, harmony and keys fill the middle, and effects and ornaments come at the end. The test is whether each step holds across a full section, not whether a solo sounds good. If a later step overturns an earlier one, go back rather than decorating a bad foundation.

## Method

Clean the session, set consistent gain and mark the sections. Build a static balance with faders, then process drums and bass, followed by the vocal, then guitar, keys and effects. Bus processing comes after the tracks, and automation comes last. Save a version at each stage and listen again the next day before deciding the next move.

## What to listen for

Hear whether the chorus enters with a natural hierarchy, whether the lead is in front from its first word, and whether the low end stays steady throughout. The four notes below arrive in order; notice which layer is established first.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C3", "G3", "E4", "C5"], "label": "Built one layer at a time", "label_en": "Built one layer at a time", "hint": "听低音、和声、旋律加入的先后", "hint_en": "Hear the order in which bass, harmony and melody arrive"}
```

## Common misconceptions

That one correct order exists; that starting with EQ is more professional; that good solos automatically add up to a good mix.
:::
