---
id: compressor-parameters
site: prod
cat: A7
title: 压缩器的五个参数
title_en: Five Compressor Settings
summary: 阈值、比率、启动、释放与拐点各自改变什么，怎么听出来。
summary_en: What threshold, ratio, attack, release and knee each change, and how to hear the difference on one loop.
level: standard
tags: [效果器, 动态, 压缩, 听感]
tags_en: [effects, dynamics, compression, listening]
alias: [压缩器, 压缩参数, 阈值, 比率, 启动, 释放, compressor, threshold, ratio]
links:
  - "[[glossary:compressor]]"
  - "[[glossary:sidechain]]"
  - "[[glossary:bus]]"
  - "[[instrument:drum-kit]]"
instances:
  - groove-000000 | 鼓组音头的源素材；启动时间差别须另做压缩渲染 | Drum attacks as source material; attack-time differences need separately compressed renders
  - groove-000011 | 节奏与声部交替参照，不包含释放时间的处理对照 | Alternating rhythmic parts, without a release-time processing comparison
  - pdmx-000450 | 强弱层次的谱面参照，不证明压缩器保留了动态 | A reference for scored dynamics, not evidence of compressor behaviour
sources:
  - Giannoulis, Massberg and Reiss, Digital Dynamic Range Compressor Design, JAES 2012.
  - Huber and Runstein, Modern Recording Techniques, dynamics chapter.
updated: 2026-11-02
---

::: zh
## 这件事难在哪

「压一下」这句话里至少藏着五个参数。只动阈值，声音会忽然变扁；把启动与释放配好，压缩才像在托住演奏，而不是把它按平。

## 它怎么工作

检测器读输入电平，超过阈值后按比率缩小增益。2:1 表示超出 10 dB 只留下 5 dB；拐点决定压缩是突然开始还是渐变；启动与释放是增益变化的速度，不是声音的快慢。补偿增益把整体抬回，否则只会觉得变小。

## 旋钮与耳朵

阈值必须跟随输入电平，不能把某个 dB 数字当成人声通用处方。可先用 3:1、较慢启动和中等释放，调阈值让目标强句出现约几 dB 衰减，再听弱句是否仍完整。例如输入高于阈值 9 dB，在硬拐点的静态 3:1 曲线上只超出 3 dB，即衰减约 6 dB；真实启动阶段还受检测与时间常数影响。

## 耳朵要抓的点

放鼓组循环，先听军鼓的敲击边缘，再把启动从 30 ms 收到 1 ms。然后让贝斯与鼓同时出现，听整体是否随低音一压一放。

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E2","E2","G2","A2"],"label":"贝斯短句参照","label_en":"Bass phrase reference","hint":"听每个音的起音与持续部分。此演示不改变压缩器启动时间，快慢启动须在同一音频上做处理对照。","hint_en":"Hear each note’s onset and body. This block does not vary compressor attack; compare attack settings on the same audio."}
```

## 容易弄错的

把压缩当音量旋钮；以为比率越高越响；认为启动越快越安全。
:::

::: en
## What makes it hard

The instruction to compress it hides at least five settings. Move only the threshold and the sound turns flat; match attack and release and compression starts to hold the performance instead of pressing it down.

## How it works

A detector reads the input level and, above the threshold, scales gain by the ratio. At 2 to 1, 10 dB over the threshold leaves 5 dB. The knee decides whether gain reduction begins abruptly or gradually. Attack and release are speeds of gain change, not speeds of the sound. Makeup gain restores the overall level, without which compression only seems quieter.

## Knobs and ears

Threshold must follow input level rather than a universal vocal setting. Try 3:1, a slower attack and moderate release, then set threshold for a few dB of reduction on the intended loud phrases. A steady signal 9 dB above a hard-knee threshold emerges 3 dB above it at 3:1, giving about 6 dB reduction. Detection and timing also affect the attack.

## What the ear should catch

Play a drum loop and listen to the edge of the snare, then pull attack from 30 ms to 1 ms. Next, with bass and drums together, hear whether the whole picture dips and recovers with every bass note.

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E2","E2","G2","A2"],"label":"Bass phrase reference","label_en":"Bass phrase reference","hint":"Hear each note’s onset and body. This block does not vary compressor attack; compare attack settings on the same audio.","hint_en":"Hear each note’s onset and body. This block does not vary compressor attack; compare attack settings on the same audio."}
```

## Easy to get wrong

That compression is a volume knob; that a higher ratio means louder; that the fastest attack is always safest.
:::
