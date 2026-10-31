---
id: high-pass-routine
site: prod
cat: A6
title: 高通滤波的日常用法
title_en: High-Pass in Daily Practice
summary: 按声部真正有用的最低频定切点，而不是每轨机械切到一百赫兹。
summary_en: Set the corner from the lowest useful note of each part instead of cutting every track at 100 Hz.
level: standard
tags: [混音, 均衡, 高通, 低频]
tags_en: [mixing, eq, high-pass, low-end]
alias: [高通滤波, 低切, HPF, high-pass, low cut]
links:
  - "[[glossary:eq]]"
  - "[[glossary:bus]]"
  - "[[instrument:voice]]"
  - "[[instrument:drum-kit]]"
instances:
  - openscore-000008 | 旋律与钢琴低音同处中低频，切得太高会抽走支撑
  - groove-000006 | 流行鼓组各件切点不同，镲片与底鼓要分开判断
  - essen-000000 | 单声部民歌曲调，切点过高会削掉旋律厚度
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook, EQ chapter — background checked, not quoted
  - Udo Zölzer, DAFX — Digital Audio Effects, filter section — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

高通常被当成每条轨必切的机械动作。切点选错，男声会变薄，钢琴会失去底座，鼓组会变得只剩敲击。

## 目标与判断

先找该声部真正有用的最低频，再把无用的低频与隆隆声切掉。判断靠扫频与电平匹配对比，不靠预设。人声通常从七十到一百二十赫兹起切，吉他八十到一百二十赫兹，镲片两百到四百赫兹，但都要按编曲让位。

## 做法

用每倍频程十二分贝的斜率，先把切点升到明显变薄，再退回二三十赫兹；Q 保持在零点七附近；切完与未切做电平匹配。总线高通要谨慎，除非整首有直流或次声。与贝斯冲突时，先切伴奏而不是切贝斯。切完再听整段，确认低频乐器进入时不会突然变空。

## 听什么

听切点升高时胸腔感何时消失；听低频乐器进入时是否变浑；把高通旁通，听整体是否只是变小。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C2","G2","C3","G3"],"label":"低频钢琴","label_en":"Low piano","hint":"先听低音，再把高通从 20 Hz 推到 120 Hz","hint_en":"Hear the low notes, then move the high-pass from 20 Hz to 120 Hz"}
```

## 常见误解

以为所有轨都要切；以为切得越高越干净；以为高通只影响低频。
:::

::: en
## The problem

High-pass filtering has become a reflex: cut every track at 100 Hz. The wrong corner thins a male vocal, removes the floor from a piano, and leaves drums with nothing but clicks.

## Goal and judgement

Find the lowest frequency the part actually uses, then remove rumble and unused lows below it. Judge by sweeping and matching level, not by preset. Vocals often start between 70 and 120 Hz, guitars between 80 and 120 Hz, cymbals between 200 and 400 Hz, but arrangement decides.

## Method

With a 12 dB per octave slope, raise the corner until the sound clearly thins, then back off 20 to 30 Hz. Keep Q near 0.7 and match level before comparing filtered and bypassed. Be careful with a master high-pass unless the whole mix has DC or subsonic content. When fighting bass, filter the accompaniment before filtering the bass. After filtering, hear the full section to ensure the low end does not drop out when bass enters.

## What to listen for

When chest weight disappears as the corner rises; whether the mix turns muddy when the bass enters; whether bypassing the filter only makes things louder.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C2", "G2", "C3", "G3"], "label": "Low piano", "label_en": "Low piano", "hint": "先听低音，再把高通从 20 Hz 推到 120 Hz", "hint_en": "Hear the low notes, then move the high-pass from 20 Hz to 120 Hz"}
```

## Common misconceptions

That every track needs a high-pass; that a higher corner is cleaner; that the filter only affects low frequencies.
:::
