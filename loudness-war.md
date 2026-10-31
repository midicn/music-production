---
id: loudness-war
site: prod
cat: B5
title: 响度战争
title_en: The Loudness War
summary: 把母带推到极限换来更响，代价是动态与冲击力。
summary_en: Pushing the master to the ceiling buys loudness at the cost of dynamics and impact.
level: standard
tags: [响度战争, 动态范围, 母带, 流媒体]
tags_en: [loudness war, dynamic range, mastering, streaming]
alias: [响度战争, 响度竞赛, loudness war]
links:
  - "[[glossary:lufs]]"
  - "[[glossary:headroom]]"
  - "[[glossary:compressor]]"
instances:
  - mutopia-000497 | 贝多芬第五交响曲第一乐章，强弱的落差本身就是内容（C1）
  - groove-000004 | 84 BPM 放克鼓组，瞬态被压平后律动会变得呆板（C1）
  - atepp-005385 | 拉威尔《绞刑架》，极弱奏在过度压缩的母带里几乎消失（C1）
sources:
  - 响度战争的年代与流媒体响度归一的背景（公开行业报道）。
  - 压缩与限幅对动态范围的影响，参考音频工程惯例。
updated: 2026-10-28
---

::: zh
## 要解决的事

同一副耳机里，更响的那版总显得更好听，于是几十年里唱片越做越响。峰值被限幅器压到天花板，弱奏被推上来，动态范围一点点消失。流媒体开始统一响度以后，这场竞赛的收益变小了，但习惯还在。

## 原理

动态范围是乐曲最强与最弱之间的差距。压缩器缩小这个差距，限幅器把峰值削到上限。持续推高平均电平，会让瞬态失去尖头，鼓的冲击变成一堵墙，弱奏失去呼吸。长时间听高响度还会让人耳暂时疲劳，反而觉得不够刺激。流媒体平台按响度归一播放，过响的曲子被整体衰减，被压掉的动态却回不来。

## 参数与做法

混音阶段就把动态当内容来设计，段落之间留出真实的强弱。母带时限幅只处理个别过冲，不整体推平。按交付平台的目标响度定值，一般流行歌曲整体响度比过去低几 LU，换来更好的瞬态。需要更响时先想编曲与配器，少靠限幅。AB 对比时对齐响度，才听得出压扁带来的损失。

## 耳朵要抓的点

在贝多芬第五的强弱转换处听落差是否还在，在放克鼓组的军鼓上听瞬态有没有被削平，在《绞刑架》的极弱段落里听细节是否还听得见。压得过狠的母带，第一耳更响，第二耳更累。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","C3","C3","C3","G3","G3","C4","C4"],"label":"弱到强的推进","label_en":"From soft to strong","hint":"听每一组音逐步加力，动态被压平后这段推进会变得平直","hint_en":"Each group should push harder; flatten the dynamics and the climb goes limp"}
```
:::

::: en
## The problem to solve

On the same pair of headphones the louder version always seems better, so records grew louder for decades. Limiters pinned peaks to the ceiling, quiet passages were pushed up, and dynamic range quietly disappeared. Streaming loudness normalisation has shrunk the payoff, but the habit remains.

## Principle

Dynamic range is the distance between the loudest and quietest moments. A compressor narrows that distance and a limiter shaves peaks at the ceiling. Raising average level continuously robs transients of their point, turns drum impact into a wall and takes the breath out of quiet passages. Long exposure to high level also tires the ear, so the music stops feeling exciting. Platforms normalise playback loudness, turning down over-hot tracks, but the dynamics that were crushed do not come back.

## Settings and practice

Treat dynamics as content at the mixing stage and leave real contrast between sections. At mastering, let the limiter catch occasional overshoots rather than flattening everything. Set integrated loudness to the delivery target, often a few LU below the loudness of past pop records in exchange for better transients. When something needs to feel louder, look at arrangement and orchestration before reaching for the limiter. Compare versions at matched loudness to hear what squashing actually costs.

## What the ear catches

At the shift from soft to strong in the Beethoven Fifth, hear whether the contrast survives; on the funk kit, whether the snare still has a point; in the quiet stretches of Le gibet, whether detail is still audible. An over-crushed master sounds bigger on first listen and more tiring on the second.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","C3","C3","C3","G3","G3","C4","C4"],"label":"From soft to strong","label_en":"From soft to strong","hint":"Each group should push harder; flatten the dynamics and the climb goes limp","hint_en":"Each group should push harder; flatten the dynamics and the climb goes limp"}
```
:::
