---
id: expander-and-gate
site: prod
cat: A7
title: 扩展器与噪声门
title_en: Expanders and Gates
summary: 阈值以下如何按比率压低，保持与迟滞又解决了什么问题。
summary_en: How downward expansion and gating reduce level below a threshold, and why hold and hysteresis exist.
level: standard
tags: [效果器, 动态, 噪声门, 听感]
tags_en: [effects, dynamics, gate, listening]
alias: [扩展器, 噪声门, 门限, 保持时间, expander, gate, noise gate]
links:
  - "[[glossary:compressor]]"
  - "[[glossary:sidechain]]"
  - "[[instrument:drum-kit]]"
instances:
  - groove-000007 | 摇滚鼓循环速度慢，门在镲片尾音上的切断更容易听清
  - groove-000000 | 放克鼓循环间隙短，适合观察保持时间如何防止门抖动
  - groove-000011 | 鼓与贝斯在同一循环里交替，门跟随底鼓开合时对比明显
sources:
  - Giannoulis, Massberg and Reiss, Digital Dynamic Range Compressor Design, JAES 2012.
  - Udo Zölzer, DAFX.
updated: 2026-10-28
---

::: zh
## 为什么会用到它

噪声门不是简单的静音开关。它和扩展器做的是同一件事，在阈值以下把增益压低，压多少、多快，决定了它是在修噪还是毁掉尾音。

## 工作方式

向下扩展按比率继续降低阈值以下的电平，2:1 表示每低 1 dB 再降 2 dB；噪声门把比率推到极限，变成开与关两态。保持时间让门在短促间隙里不关闭，迟滞给开启与关闭设不同阈值，避免抖动。侧链高通可以让低频不反复推开门。

## 旋钮与耳朵

Range 设到 −40 dB 已接近静音；阈值贴着噪声底上方，启动 1–5 ms、释放 100–500 ms、保持 50–100 ms。门开得太快会有咔哒声，释放太短会把鼓的余音整段切掉。

## 耳朵要抓的点

在鼓房间麦克风上听门，先听到镲片尾音被整段收掉，再把保持加长，尾音会恢复一点自然。贝斯与鼓同录时，门会跟着底鼓开合。

```audiolab
{"type":"instrument","gm":"Synth Bass 1","synth":"plucked","phrase":["E2","G2","A2","E3"],"label":"带尾音的贝斯","label_en":"Bass with tails","hint":"先听干声，再想门会在哪个位置切断","hint_en":"Hear it dry, then decide where a gate would cut"}
```

## 容易弄错的

以为门能无痕去噪，其实间隙里的环境声会突然消失；把门与压缩器当成相反的两件事，方向相反，却可能共用同一个检测器；忽略保持时间。
:::

::: en
## Why reach for it

A gate is not a mute switch. It and the expander do one job, lowering gain below a threshold, and how far and how fast decide whether it cleans noise or ruins tails.

## The working principle

Downward expansion keeps reducing level below the threshold by a ratio; at 2 to 1 every 1 dB lower becomes 2 dB lower. A gate pushes the ratio to its limit and becomes a two-state switch. Hold keeps it open through short gaps, and hysteresis sets different open and close thresholds to stop chatter. A high-pass in the sidechain keeps bass from reopening it.

## Knobs and ears

A range of minus 40 dB is already near silence. Put the threshold just above the noise floor, with attack 1 to 5 ms, release 100 to 500 ms and hold 50 to 100 ms. Too fast an attack clicks; too short a release chops the decay of a drum.

## What the ear should catch

Gate a drum room microphone and hear the cymbal tail vanish all at once, then lengthen hold and hear some of it return. With bass and drums recorded together, the gate opens and closes with the kick.

```audiolab
{"type": "instrument", "gm": "Synth Bass 1", "synth": "plucked", "phrase": ["E2", "G2", "A2", "E3"], "label": "Bass with tails", "label_en": "Bass with tails", "hint": "先听干声，再想门会在哪个位置切断", "hint_en": "Hear it dry, then decide where a gate would cut"}
```

## Easy to get wrong

That a gate removes noise without a trace, when room tone vanishes in the gaps; that gate and compressor are opposites, though both can share one detector; that hold is optional.
:::
