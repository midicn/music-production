---
id: automation-curves
site: prod
cat: A1
title: 参数自动化
title_en: Parameter Automation
summary: 让音量、声像与插件参数随时间变化，而不是靠手一直推。
summary_en: Recording fader and plug-in moves as curves, so a mix can breathe without a hand on the control at every moment.
level: standard
tags: [DAW, 自动化, 工作流]
tags_en: [DAW, automation, workflow]
alias: [自动化, 参数自动化, 包络线, automation]
links:
  - "[[glossary:automation]]"
  - "[[glossary:daw]]"
  - "[[glossary:compressor]]"
instances:
  - pdmx-000031 | 拉威尔《波莱罗》的钢琴改编，长段渐强适合画音量曲线
  - mutopia-001630 | 圆舞曲的乐句起伏明显，适合练呼吸式的推子动作
  - pdmx-000269 | 管弦组曲的强弱层次多，可对照自动化与压缩的分工
sources:
  - 自动化曲线、写入与读取模式的用法——依据来自DAW 文档。
  - 音量、发送与插件参数在信号链中的位置，对照音频工程教材整理。
updated: 2026-10-28
---

::: zh
自动化是把推子、旋钮与开关的动作录下来，让参数随时间自己走。它解决的是静态设置管不了整首曲子的起伏。

## 难在哪

一首歌从主歌到副歌，音量、声像与混响都要变。靠手推只能应付一次，而且难以复现。自动化让这些动作成为工程的一部分，可以反复播放与修改。

## 它怎么工作

每个可自动化参数都有一条曲线，横轴是时间，纵轴是参数值。节点之间可以线性、曲线或阶梯连接。写入模式记录你的动作，读取模式回放，锁定模式防止误改。音量自动化通常在推子之后，插件自动化发生在链路内部。

## 参数与取舍

先画大局，再修细节。节点少而平滑，避免听得出阶梯。确认曲线是跟着片段还是跟着绝对时间。写完切回读取，再听一遍有没有突然的跳变。

## 耳朵要抓的点

听《波莱罗》的渐强，听《蓝色多瑙河》的乐句呼吸。短句演示本身没有自动化，但可以把它当素材，想象推子从弱到强推过去。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","A4"],"label":"可供画曲线的素材","label_en":"Material for a volume curve","hint":"听长音的余量，想象它在八小节里渐强","hint_en":"Hear the headroom, then imagine it rising over eight bars"}
```

## 容易弄错的

自动化不等于压缩，压缩跟着信号走，自动化跟着你的决定走。曲线也不是越密越好，密到失去整体形状就难改。
:::

::: en
Automation records the moves of faders, knobs and switches so parameters change over time. It handles the ups and downs that a static setting cannot.

## Where it gets hard

From verse to chorus, level, pan and reverb all need to change. A hand on the fader works once and is hard to repeat. Automation makes those moves part of the project, playable and editable again and again.

## How it works

Every automatable parameter has a curve, with time across and value up. Nodes join linearly, in curves or in steps. Write mode records your moves, read mode plays them back, and lock mode prevents accidental changes. Volume automation usually sits after the fader; plug-in automation happens inside the chain.

## Settings and trade-offs

Draw the large shape first, then detail. Use few, smooth nodes and avoid audible steps. Decide whether the curve follows the clip or absolute time. Return to read mode and listen for sudden jumps.

## What the ear catches

Hear the build in Bolero and the phrase breathing in the Blue Danube. The short demo has no automation of its own, but you can treat it as material and imagine the fader rising.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C4", "E4", "G4", "A4"], "label": "Material for a volume curve", "label_en": "Material for a volume curve", "hint": "听长音的余量，想象它在八小节里渐强", "hint_en": "Hear the headroom, then imagine it rising over eight bars"}
```

## Easy to get wrong

Automation is not compression. A compressor follows the signal, automation follows your decision. Denser curves are not better either; if the overall shape is lost, the part becomes hard to revise.
:::
