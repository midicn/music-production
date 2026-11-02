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
  - mutopia-001319 | 合唱音符与连句的参照，不是现场房间声录音 | Choral notes and connected phrasing, not a recording of live room sound
  - openscore-000667 | 歌声与钢琴的 MIDI 声部，不记录真实话筒串音 | Voice-and-piano MIDI parts that do not record real microphone spill
  - m21-000576 | 多声部进入与停顿的参照，不用于证明现场换气 | Multiple entries and rests as reference, not proof of live breathing
sources:
  - Bartlett and Bartlett, Practical Recording Techniques, remote recording chapters
  - AES Convention paper on live concert recording practice and audience miking
updated: 2026-11-02
---

::: zh
## 问题

现场录音没有第二次机会，也不能把人声拆出来重录。它换来的是一次成形的呼吸、真实的房间与观众；代价是错音、串音与无法完全掌控的平衡。

## 信号链

舞台话筒先经舞台接口箱，再到监听位的话放与录音机；同时取调音台主输出作为参照。观众话筒单独成轨，后期用来补空间。录音机另开一份备份录制。

## 摆位与参数

主话筒位置应按视线、安全、直达/混响比例与扩声系统覆盖决定，不必固定在观众席后排或耳高。观众话筒要避开明显的扬声器直射，检查与舞台近讲轨混合时的时间差。用各自独立存储的主、备录音保留足够峰值余量，开演前确认实际写盘而非只有输入电平。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"连贯乐句","label_en":"Connected phrase","hint":"听音符如何组成乐句。这是合成示例，不是现场录音，不能据此判断舞台串音、观众声或话筒距离。","hint_en":"Hear how notes form a phrase. This is synthesis, not a live recording, and cannot establish stage spill, audience sound or microphone distance."}
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

Place the main array for sight lines, safety, direct/reverberant balance and PA coverage, not automatically at the rear or ear height. Keep audience microphones away from strong direct loudspeaker spill and check their timing against close stage tracks. Main and backup recorders should use independent storage with suitable peak headroom; confirm actual recorded files before the show.

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"Connected phrase","label_en":"Connected phrase","hint":"Hear how notes form a phrase. This is synthesis, not a live recording, and cannot establish stage spill, audience sound or microphone distance.","hint_en":"Hear how notes form a phrase. This is synthesis, not a live recording, and cannot establish stage spill, audience sound or microphone distance."}
```

## What to listen for

Start with the ratio of applause to room, then hear whether the voice is covered by the band. Compare the reference with the main pair and notice whether the low end piles up and whether bleed widens the image.

## Common misconceptions

- **A board feed is a live recording** → it is a reference without the room.
- **More microphones is better** → bleed and phase get harder to manage.
- **Live means no post-production** → you can fix things, but you cannot retake them.
:::
