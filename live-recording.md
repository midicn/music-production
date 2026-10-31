---
id: live-recording
site: prod
cat: A4
title: 现场录音
title_en: Live Recording
summary: 没有第二次机会，换来一次成形的呼吸与真实房间
summary_en: No second chance, but a single take that keeps its breath and the real room.
level: standard
tags: [录音, 现场, 演出]
tags_en: [recording, live, concert]
alias: [现场, 实况录音, 现场收音, live, live session, concert recording]
links:
  - "[[glossary:room-treatment]]"
  - "[[glossary:monitoring]]"
  - "[[instrument:voice]]"
instances:
  - mutopia-001319 | 长音连绵的合唱，一次成形时空间就是乐器
  - openscore-000667 | 人声与钢琴同处一室，踏板与演唱互相渗入
  - m21-000576 | 牧歌多声部，声部间不齐的呼吸正是现场要保留的
sources:
  - Bartlett and Bartlett, Practical Recording Techniques, remote recording chapters
  - AES Convention paper on live concert recording practice and audience miking
updated: 2026-10-28
---

::: zh
## 问题

现场录音没有第二次机会，也不能把人声拆出来重录。它换来的是一次成形的呼吸、真实的房间与观众；代价是错音、串音与无法完全掌控的平衡。

## 信号链

舞台话筒先经舞台接口箱，再到监听位的话放与录音机；同时取调音台主输出作为参照。观众话筒单独成轨，后期用来补空间。录音机另开一份备份录制。

## 摆位与参数

主话筒架在观众席后方，高度接近人耳。舞台话筒按乐器分组，用不到的通道先关掉以减少串音。峰值留 10 dB 余量，宁可录低一点；备份机与主机各用独立存储。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"一次成形的长音","label_en":"Sustained notes formed in one pass","hint":"听四个音怎样连成一句，想象中间没有补录的机会","hint_en":"Hear the four notes become one phrase, with no chance to patch later"}
```

## 听什么

先听掌声与房间的比例，再听人声是否被乐器盖住。对比参照轨与主话筒，注意低频是否在现场堆积、串音是否让声像变宽。

## 常见误解

- **调音台直录就是现场录音** → 那只是参照，缺了空间。
- **话筒越多越好** → 串音与相位更难收拾。
- **现场不能后期** → 可以修，但不能重录。
:::

::: en
## The problem

A live recording has no second chance and no way to redo a part. What it gives back is a single take with real breath, a real room and an audience; what it costs is wrong notes, bleed and a balance you cannot control.

## Signal chain

Stage microphones run through a stage box to the preamps and recorder, while the console's main output is captured as a reference. Audience microphones get their own tracks for room, and a second recorder runs as backup.

## Placement and settings

Place the main pair behind the audience, at about ear height. Group the stage microphones by instrument and mute unused channels to reduce bleed. Leave 10 dB of headroom at the peaks; lower is safer than clipped, and the backup recorder uses separate storage.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C4", "E4", "G4", "C5"], "label": "Sustained notes formed in one pass", "label_en": "Sustained notes formed in one pass", "hint": "听四个音怎样连成一句，想象中间没有补录的机会", "hint_en": "Hear the four notes become one phrase, with no chance to patch later"}
```

## What to listen for

Start with the ratio of applause to room, then hear whether the voice is covered by the band. Compare the reference with the main pair and notice whether the low end piles up and whether bleed widens the image.

## Common misconceptions

- **A board feed is a live recording** → it is a reference without the room.
- **More microphones is better** → bleed and phase get harder to manage.
- **Live means no post-production** → you can fix things, but you cannot retake them.
:::
