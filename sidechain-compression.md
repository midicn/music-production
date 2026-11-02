---
id: sidechain-compression
site: prod
cat: A6
title: 侧链压缩
title_en: Sidechain Compression
summary: 让一条声部在另一条出现时自动后退，关键在于时机与幅度。
summary_en: One part steps back when another appears, and timing plus amount matter more than the ratio.
level: standard
tags: [混音, 侧链, 压缩, 律动]
tags_en: [mixing, sidechain, compression, groove]
alias: [侧链, 侧链压缩, 泵感, sidechain, pumping]
links:
  - "[[glossary:sidechain]]"
  - "[[glossary:compressor]]"
  - "[[glossary:bus]]"
  - "[[instrument:drum-kit]]"
instances:
  - groove-001103 | 规律底鼓可用作外部触发；需另设被压轨道并接好侧链路由 | Regular kicks can trigger a sidechain; supply a separate processed track and verify routing
  - oga-000002 | 可将鼓与贝斯分轨渲染，在 DAW 中接外部侧链，比较有无让位 | Render drums and bass separately, route an external sidechain in a DAW and compare ducking on and off
  - groove-000006 | 密集鼓点可测试侧链释放是否及时恢复，需查看增益衰减并听合奏 | Dense hits test recovery between triggers; watch gain reduction and listen in the mix
sources:
  - Giannoulis, Massberg and Reiss, Digital Dynamic Range Compressor Design, JAES 2012.
  - Bobby Owsinski, The Mixing Engineer's Handbook, sidechain section.
updated: 2026-11-02
---

::: zh
## 问题

侧链是处理器用来判断何时动作的检测路径。检测信号可来自被处理声音本身，也可来自另一条轨道；它不一定直接混入可听输出。外部底鼓触发贝斯衰减，是其中一种用途。

## 目标与判断

先确定谁触发、谁让位及让位的时间段。底鼓可触发贝斯衰减，人声也可触发伴奏让位。所需持续时间依音符长度与编曲而变；观察增益衰减曲线，听释放是否衔接下一音。过快动作可能引入调制失真，长释放也可能是有意的包络设计。

## 做法

先把贝斯送入压缩器的音频输入，把底鼓送入其侧链输入，并确认路由和检测监听。调阈值让目标击打触发，再设置最大需要的让位量。听贝斯是否在下一音前恢复，按节奏调整释放；如果只有某一频带冲突，可比较动态EQ或自动化，不必让整条贝斯都下降。

## 听什么

保持同一段鼓与贝斯，比较侧链关闭与开启，记录触发位置和恢复时间，再匹配总体响度判断让位是否有效。若没有实际外部触发路由，单独播放一个音色并不能展示侧链动作。

```audiolab
{"type":"instrument","gm":"Synth Bass 1","synth":"plucked","phrase":["E1","E1","G1","E1"],"label":"侧链练习的贝斯短句","label_en":"Bass material for sidechain practice","hint":"在 DAW 录下贝斯，另用底鼓送入压缩器外部侧链；观察每次触发的衰减与两次触发间的恢复。","hint_en":"Record the bass in a DAW and feed a separate kick into the compressor’s external sidechain. Observe reduction per trigger and recovery between triggers."}
```

## 常见误解

以为侧链只属于舞曲；以为释放越短越紧；以为侧链能替代编曲上的让位。
:::

::: en
## The problem

A sidechain is the detector path that decides when a processor acts. It can use the processed signal or another track and need not be audible in the output. Ducking bass from an external kick is one application.

## Goal and judgement

Choose the trigger, the reduced part and the intended ducking interval. A kick may duck bass, or a vocal may duck accompaniment. Duration depends on notes and arrangement; observe gain reduction and listen through recovery into the next note. Very fast action can introduce modulation distortion, while long release can be an intentional envelope choice.

## Method

Feed bass to the audio input and kick to the sidechain, verifying routing and detector audition. Set threshold for intended hits, then choose the required ducking. Adjust release so bass recovers at the needed point. If only one band conflicts, compare dynamic EQ or automation rather than ducking the whole bass.

## What to listen for

Keep the same kick-and-bass passage, compare sidechain off and on, and note triggering and recovery before matching overall loudness. A single preset sound without the external-trigger route does not demonstrate sidechain behaviour.

```audiolab
{"type":"instrument","gm":"Synth Bass 1","synth":"plucked","phrase":["E1","E1","G1","E1"],"label":"Bass material for sidechain practice","label_en":"Bass material for sidechain practice","hint":"Record the bass in a DAW and feed a separate kick into the compressor’s external sidechain. Observe reduction per trigger and recovery between triggers.","hint_en":"Record the bass in a DAW and feed a separate kick into the compressor’s external sidechain. Observe reduction per trigger and recovery between triggers."}
```

## Common misconceptions

That sidechain belongs only to dance music; that a shorter release is tighter; that sidechain replaces arrangement.
:::
