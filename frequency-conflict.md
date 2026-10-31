---
id: frequency-conflict
site: prod
cat: A6
title: 频率冲突与避让
title_en: Frequency Conflict and Carving
summary: 冲突不能靠两边提升解决，要让每个频段在每一刻只有一个主人。
summary_en: Conflict is not solved by boosting both sides, but by giving each band a single owner at any moment.
level: standard
tags: [混音, 频段, 掩蔽, 避让]
tags_en: [mixing, frequency, masking, carving]
alias: [频率打架, 频段避让, frequency masking]
links:
  - "[[glossary:eq]]"
  - "[[glossary:sidechain]]"
  - "[[instrument:piano]]"
  - "[[period:classical]]"
instances:
  - musicnet-000097 | 弦乐四重奏四个声部音区接近，掩蔽关系一听就明白（C1）
  - oga-000004 | 游戏战斗段层数多，适合找谁在抢同一块中低频（C1）
  - musicnet-000119 | 木管六重奏音色接近，和弦排列稍密就会互相遮盖（C1）
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook, frequency masking and EQ chapters.
  - David Gibson, The Art of Mixing, frequency range ownership.
updated: 2026-10-28
---

::: zh
## 问题

底鼓与贝斯抢六十到一百赫兹，吉他与键盘挤在两百到五百赫兹，人声与军鼓又在二到四千赫兹相遇。听不清时最容易做的事是两边都提升，结果掩蔽更重，音量也越来越大。

## 目标与判断

同一时刻，每个频段只留一个主人。判断冲突要看整段，不看单轨：把疑似抢频的声部静音，主信息是否立刻回来。若回来，问题在编曲与音区；若不回来，才轮到均衡处理。频谱上的坑不必填平，听感上的主次才要守住。

## 做法

先改编曲，换八度、改节奏、挪声像，让两个声部不在同一刻占同一块。再做静态均衡，在次要声部衰减一到三 dB，而不是提升主角。需要持续避让时，用侧链或动态均衡，触发要慢、量要小。每一步都回到整段确认。

## 听什么

先听低频是否紧，底鼓起音后贝斯是否还清楚；再听主唱字头有没有被军鼓盖住。下面四个低音依次响起，注意尾音如何叠成一块。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","E3","G3","B3"],"label":"低音区挤在一起","label_en":"A crowded low register","hint":"先听整体厚度，再分辨每个音还剩下多少轮廓","hint_en":"Hear the thickness first, then how much outline each note keeps"}
```

## 常见误解

以为每个声部都必须厚；以为提升被遮住的频段就能听清；以为频谱越平越好。
:::

::: en
## The problem

Kick and bass fight over sixty to one hundred hertz, guitar and keys crowd two hundred to five hundred, and vocal and snare meet again between two and four thousand. When something is hard to hear, the easy move is to boost both sides. Masking gets worse and the level keeps climbing.

## Goal and judgement

At any moment, each band should have one owner. Judge conflict across a full section, not in solo. Mute the suspected competitor and see whether the main information returns at once. If it does, the problem lives in arrangement and register. If it does not, EQ may help. Gaps in a spectrum display do not need filling; the audible hierarchy does.

## Method

Change the arrangement first: move an octave, alter the rhythm, shift the pan, so two parts no longer occupy the same band at the same time. Then apply static EQ, cutting one to three dB on the supporting part rather than boosting the lead. For constant overlap, use sidechain or dynamic EQ with a slow trigger and a small amount. Return to the full section after every move.

## What to listen for

Hear whether the low end stays tight and the bass remains clear after each kick. Then check that the vocal's consonants are not covered by the snare. The four low notes below follow in turn; notice how their tails overlap.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C3", "E3", "G3", "B3"], "label": "A crowded low register", "label_en": "A crowded low register", "hint": "先听整体厚度，再分辨每个音还剩下多少轮廓", "hint_en": "Hear the thickness first, then how much outline each note keeps"}
```

## Common misconceptions

That every part must sound thick; that boosting a masked band restores clarity; that a flat spectrum is the goal.
:::
