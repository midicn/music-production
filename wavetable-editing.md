---
id: wavetable-editing
site: prod
cat: B3
title: 波表编辑
title_en: Editing a Wavetable
summary: 帧的顺序、插值与变形方式决定音色走向，先定起点与终点。
summary_en: Frame order, interpolation and warp decide where a wavetable can travel; fix the endpoints before touching modulation.
level: standard
tags: [波表, 音色设计, 扫描, 变形, 限带]
tags_en: [wavetable, sound design, scanning, warp, band-limiting]
alias: [波表编辑, 波表制作, 帧编辑, wavetable editing, warp mode]
order: 410
links:
  - "[[glossary:timbre]]"
  - "[[instrument:wavetable-synthesis]]"
  - "[[instrument:software-synth]]"
  - "[[glossary:modulation]]"
instances:
  - oga-000163 | 曲中锯齿主音与扫频铺底并存，能听出同一张表在不同位置上的两种性格（C1）
  - oga-000142 | 场景音乐里主音多次换色，像手工挑了中间帧再排顺序（C1）
  - oga-000116 | 洞穴场景的金属铺底明暗渐变，适合判断帧之间是否连续（C1）
  - oga-000286 | 锯齿主音与合成贝斯同场，可对照扫描幅度大小对音色的影响（C1）
sources:
  - Curtis Roads, The Computer Music Tutorial — 波表合成与插值
  - Udo Zölzer，DAFX — Digital Audio Effects — 波表振荡器与限带
  - Xfer Records，Serum 用户指南（厂商文档）— 波表编辑与变形模式
updated: 2026-10-31
---

::: zh
随手扫一张现成的表，音色只是在明暗之间晃，扫到底也不知道自己去了哪。波表编辑真正要决定的是三件事：表里放哪些帧、帧按什么顺序排、位置怎么被推动。

## 帧从哪来

帧可以是手绘的谐波叠加，可以从采样里提取单周期，也可以用频谱分析再合成。手绘适合做明确的起点与终点；采样提取保留真实乐器的细节，但要去掉直流与噪声。每一帧都要归一化到同一峰值，否则扫描会变成音量起伏。帧数不必多，八到十六帧足以撑起一段连续变化。

## 扫描与变形不是一回事

| 控制 | 作用对象 | 听感 | 常见用法 | 设置要点 |
|---|---|---|---|---|
| 扫描位置 | 选哪一帧 | 从暗到亮 | 长音铺底呼吸 | 与速度同步 |
| 扫描速率 | 移动快慢 | 慢如呼吸，快如摆动 | 节奏型音色 | 与 LFO 分权 |
| 变形 | 单帧内部形状 | 同一帧变宽变窄 | 持续音微调 | 注意电平 |
| 相位对齐 | 帧与帧之间 | 减少抵消与毛刺 | 谐波类波表 | 起始相位一致 |

## 一张表的工作流

先定起点与终点：一个接近正弦的柔和帧，一个谐波丰富的亮帧。中间帧按听感补，不要按数学等分；哪一段变化太快，就在那里加帧。检查每一帧的限带情况，把音高试到最高音区，听有没有混叠的沙沙声。最后把表存成带名字与版本的文件，附一段固定音高的试听。

## 哪里会坏

帧之间相位不一致，扫描时会出现抵消，音量忽大忽小；帧电平不统一，扫描听起来像颤音；表没有限带，高音区会混叠；扫描同时被包络与 LFO 推动，两者打架，音色走到一半被拉回。把波表当采样用也会出问题：单周期表长度固定，拉伸不会换来更长的音。

```audiolab
{"type":"instrument","gm":"Lead 2 (sawtooth)","synth":"bowed","phrase":["C3","G3","C4"],"label":"同一张表的两个位置","label_en":"Two positions on one table","hint":"先听和弦现在的亮度，再把扫描位置推到表尾；音高不动，只有谐波在换。","hint_en":"Hear the chord where it sits now, then push the scan to the far end of the table; pitch stays, only the harmonics move."}
```
:::

::: en

Scan a stock table at random and the timbre merely brightens and darkens; reach the end and you cannot say where you went. Editing a wavetable is really three decisions: which frames go in, what order they sit in, and what pushes the position.

## Where frames come from

A frame can be drawn as a stack of harmonics, extracted as a single cycle from a recording, or resynthesised from a spectrum. Drawing suits clear endpoints; extraction keeps the detail of a real instrument but needs DC and noise removed. Normalise every frame to the same peak, or scanning turns into a volume ride. Eight to sixteen frames carry a continuous morph comfortably.

## Scanning and warping are different jobs

| Control | What it acts on | What you hear | Typical use | Setting to watch |
|---|---|---|---|---|
| Scan position | Which frame plays | Dark to bright | Breathing pads | Sync to tempo |
| Scan rate | How fast it moves | Slow breath, fast sway | Rhythmic timbres | Share with the LFO |
| Warp | Shape inside one frame | Same frame, wider or narrower | Fine sustain shaping | Level changes |
| Phase alignment | Frame to frame | Less cancellation, fewer clicks | Harmonic tables | Common start phase |

## A working method for one table

Set the endpoints first: a soft frame close to a sine, and a bright frame rich in harmonics. Fill the middle by ear rather than by arithmetic, adding frames wherever the change happens too fast. Check band-limiting frame by frame, playing up to the top of the range for aliasing hiss. Save the table with a name and a version, plus a fixed-pitch audio example.

## Where it breaks

If frames disagree in phase, scanning cancels and the level jumps; if frames disagree in level, the scan sounds like tremolo; an unlimited table aliases in the high register; an envelope and an LFO both driving position fight each other and pull the timbre back halfway. Treating a wavetable like a sample also fails: a single-cycle table has a fixed length, and stretching it does not produce a longer note.

```audiolab
{"type":"instrument","gm":"Lead 2 (sawtooth)","synth":"bowed","phrase":["C3","G3","C4"],"label":"Two positions on one table","label_en":"Two positions on one table","hint":"Hear the chord where it sits now, then push the scan to the far end of the table; pitch stays, only the harmonics move.","hint_en":"Hear the chord where it sits now, then push the scan to the far end of the table; pitch stays, only the harmonics move."}
```
:::
