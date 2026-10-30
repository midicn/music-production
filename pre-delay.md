---
id: pre-delay
site: prod
cat: A7
title: 预延迟
title_en: Pre-Delay
summary: 直达声与混响之间那段等待，如何改变距离感与字音清晰度。
summary_en: The wait between direct sound and reverb, and how it changes distance and the clarity of words.
level: standard
tags: [效果器, 混响, 时间, 听感]
tags_en: [effects, reverb, timing, listening]
alias: [预延迟, 预延时, pre-delay, predelay]
links:
  - "[[glossary:reverb]]"
  - "[[glossary:delay]]"
  - "[[instrument:voice]]"
instances:
  - pdmx-000070 | 弦乐长音没有辅音遮挡，预延迟改变时空间远近最明显
  - pdmx-000450 | 合唱与乐队层次多，预延迟太短会让歌词与尾音糊在一起
  - mutopia-001411 | 萨蒂《裸体歌舞》第一首音符稀疏，能听清直达声与反射的分界
sources:
  - Välimäki, Parker and Savioja, Fifty Years of Artificial Reverberation, IEEE TASLP 2012 — pre-delay and early reflections checked, not quoted
  - Huber and Runstein, Modern Recording Techniques, reverberation chapter — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

预延迟常被当成「混响开始前的一点空隙」，于是随手设 20 ms。它其实决定了直达声与空间是否被听成同一件事，也决定了人声还清不清楚。

## 原理

预延迟是混响开始输出前的等待。20 ms 以内，延迟声与直达声在听觉上融合，只增加响度与厚度；30–60 ms 之后，耳朵开始把两者分开，空间显得更大，字音也不再被尾音糊住。它不改变混响的衰减，只改变时间关系。

## 参数与听感

人声常用 10–30 ms，既保住辅音又拉开距离；给鼓加 40–80 ms 会让房间明显变大，太短却会与直达声产生梳状滤波，太长则像两个独立的声音。按歌曲速度换算成音符时值，还能得到有节奏的反射。

## 听什么

同一句人声，分别用 0、30、60 ms 的预延迟，注意「s」与「t」是否还被尾音盖住。在军鼓上拉长预延迟，房间会从贴身移到身后。

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["C4","E4","G4"],"label":"合唱长音","label_en":"Sustained choir","hint":"先听干声，再用 0 与 40 ms 预延迟对比","hint_en":"Hear it dry, then compare 0 and 40 ms of pre-delay"}
```

## 常见误解

把预延迟当成延迟效果器；以为越长空间越大；认为混响应当紧贴直达声开始。
:::

::: en
## The question

Pre-delay is often treated as a small gap before the reverb starts, so 20 ms gets dialled in without thought. It actually decides whether direct sound and space are heard as one event, and whether a vocal stays clear.

## How it works

Pre-delay is the wait before a reverb begins to output. Within about 20 ms the reflection fuses with the direct sound, adding loudness and body. From roughly 30 to 60 ms the ear starts to separate them, the space seems larger and consonants stop being smeared by the tail. It does not change decay, only the timing relationship.

## Settings and what you hear

Vocals often take 10 to 30 ms, keeping consonants while adding distance. On drums, 40 to 80 ms makes a room noticeably larger, but too short causes comb filtering with the direct sound and too long sounds like a separate event. Converting the value to a note length can produce rhythmic reflections.

## What to listen for

Take one vocal line with pre-delay at 0, 30 and 60 ms and hear whether the s and t sounds are still covered by the tail. Stretch pre-delay on a snare and the room moves from close to behind.

```audiolab
{"type": "instrument", "gm": "Choir Aahs", "synth": "vocal", "phrase": ["C4", "E4", "G4"], "label": "Sustained choir", "label_en": "Sustained choir", "hint": "先听干声，再用 0 与 40 ms 预延迟对比", "hint_en": "Hear it dry, then compare 0 and 40 ms of pre-delay"}
```

## Common misconceptions

That pre-delay is a delay effect; that longer always means bigger; that reverb should begin right against the direct sound.
:::
