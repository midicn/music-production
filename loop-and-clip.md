---
id: loop-and-clip
site: prod
cat: B2
title: 循环与片段
title_en: Loops and Clips
summary: 循环决定重复哪一段，片段决定这段装什么。
summary_en: A loop decides which range repeats, while a clip decides what that range contains.
level: standard
tags: [音序, 循环, 片段, 编排]
tags_en: [sequencing, loop, clip, arrangement]
alias: [循环, 片段, 循环区间, loop, clip, loop region]
links:
  - "[[glossary:sequence]]"
  - "[[glossary:daw]]"
  - "[[glossary:tempo]]"
instances:
  - oga-000009 | 半分钟的海滩场景配乐，短到能整段反复
  - groove-000035 | 三十秒的爵士放克过门，接缝处最容易听出问题
  - groove-001103 | 迪斯科循环，四拍结构适合按小节回卷
sources:
  - 工程循环与片段循环的差别——依据来自 DAW 文档。
  - 循环接缝的尾音与渲染处理，对照数字音频工作流惯例整理。
updated: 2026-10-28
---

::: zh
循环决定重复哪一段，片段决定这一段里装什么，两者常被混为一谈。

## 难在哪

八小节副歌要重复十六遍，逐段复制既费事又容易漏改。循环与片段让重复成为结构，而不是体力活。

## 背后的机制

循环是时间线上的一个区间，播放头到终点就跳回起点；片段是容器，装着音符或音频，可以独立复制、裁剪与再循环。片段内的循环点与工程循环点是两套设置，前者跟着片段走，后者跟着播放头走。

## 旋钮与做法

循环起止落在小节线上，长度取四或八的倍数；片段复制用共享副本，改一处即全改；循环接缝处留出释放尾音，混响与延迟不设零；导出前把循环渲染成完整长度，避免接缝被裁掉。

## 耳朵要抓的点

听接缝有没有咔哒声，尾音是否被切断，律动是否在回卷时断一拍。把循环点前后各留一小节，更容易听出问题。

## 容易弄错的

循环不等于精确复制，带尾音的片段回卷时会重叠。片段循环也不会真的生成新事件，导出前要确认渲染范围。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5"],"label":"可循环的短句","label_en":"A phrase made to loop","hint":"听结尾能否直接接回开头","hint_en":"Hear whether the end returns to the start"}
```
:::

::: en
A loop decides which passage repeats, while a clip decides what that passage contains, and the two are often confused.

## Where it gets hard

An eight-bar chorus must repeat sixteen times, and copying it section by section is slow and easily inconsistent. Loops and clips make repetition a structure rather than labour.

## The mechanism

A loop is a range on the timeline; playback jumps back at its end. A clip is a container holding notes or audio that can be copied, trimmed and looped on its own. Clip loop points and project loop points are separate: one travels with the clip, the other with the playhead.

## Settings and practice

Place loop boundaries on bar lines and use lengths of four or eight bars. Copy clips as shared instances so one edit changes all. Leave release tails at the seam and never set reverb or delay to zero. Render the loop to full length before export so the seam survives.

## What the ear catches

Check for a click at the seam, a cut tail, or a lost beat when playback wraps. One bar on each side of the loop makes faults easier to hear.

## Common misunderstandings

A loop is not an exact copy; clips with tails overlap when they wrap. Clip looping does not create new events either, so confirm the render range before export.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "C5"], "label": "A phrase made to loop", "label_en": "A phrase made to loop", "hint": "听结尾能否直接接回开头", "hint_en": "Hear whether the end returns to the start"}
```
:::
