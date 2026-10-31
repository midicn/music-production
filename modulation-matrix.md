---
id: modulation-matrix
site: prod
cat: B3
title: 调制矩阵
title_en: The Modulation Matrix
summary: 把 LFO、包络与力度指派给任意目标，声音才会自己动。
summary_en: Route LFOs, envelopes and velocity to any destination, and a static patch starts to move.
level: standard
tags: [合成, 调制, LFO, 包络]
tags_en: [synthesis, modulation, lfo, envelope]
alias: [调制矩阵, 调制路由, mod matrix, modulation routing]
links:
  - "[[glossary:synthesizer]]"
  - "[[instrument:moog-modular]]"
  - "[[instrument:prophet-5]]"
  - "[[period:modern]]"
instances:
  - oga-000329 | 合成铜管单独写入两百余个 CC1，调制轮只作用于这一层
  - oga-000327 | 弯音事件密集，音高作为调制目标被反复推动
  - oga-000270 | 多条通道各自写入 CC91 与 CC93，混响与合唱深度分开控制
sources:
  - Gordon Reid, Sound On Sound Synth Secrets.
  - Curtis Roads, The Computer Music Tutorial.
updated: 2026-10-28
---

::: zh
## 起点：一个问题

一个音色为什么会在按住不放时慢慢变亮、变宽或颤动？如果每个旋钮只能固定一个值，声音就是死的。调制矩阵解决的正是「让谁去推谁」。

## 一层层看原理

矩阵把调制源与调制目标两两相连，交点上的量就是深度。常见源有 LFO、ADSR 包络、力度、键位、调制轮与触后；常见目标有音高、截止、音量、声像、脉宽与效果发送。深度可正可负，负值让方向反过来。一个源可以同时推多个目标，一个目标也可以被多个源叠加。模块化合成器用线缆完成这件事，软件合成器把它做成一张表格或一串下拉菜单。

## 旋钮与耳朵

颤音是 LFO 推音高，深度小、速度快；滤波摆动是 LFO 推截止，速度慢时像呼吸。包络推音高会得到打击乐式的下滑音；力度推截止会让重音更亮。深度过大时目标会撞到边界，产生卡住或失真。多个源叠加时要留余量，否则一个占满，另一个就听不见。

## 耳朵要抓的点

先听长音上的颤音，判断它是音高在动还是音量在动；再听铺底的明暗是否周期性起伏；最后听重音与轻音的音色差，判断力度是否被指派到截止。能说出「哪个源在推哪个目标」，就听懂了矩阵。

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["A3","E4","A4","E5"],"label":"一个 LFO 推两个目标","label_en":"One LFO pushing two destinations","hint":"先听长音，再想象 LFO 同时推音高与截止；颤音很浅，明暗起伏很慢，两者速度可以分开","hint_en":"Hear the held note, then imagine one LFO pushing pitch and cutoff at once; the vibrato is shallow and the brightness moves slowly, so the two depths stay separate"}
```

## 容易弄错的

以为调制就是加效果器；以为源越多越好；忽略负深度与叠加，结果调不出想要的方向。
:::

::: en
## Starting point: a problem

Why does a held note grow brighter, wider or unsteady? If every knob held one value, the sound would sit still. The modulation matrix answers one question: what pushes what?

## Inside the mechanism

A matrix connects sources to destinations, and the amount at each crossing is the depth. Common sources are LFOs, ADSR envelopes, velocity, key position, the mod wheel and aftertouch. Common destinations are pitch, cutoff, level, pan, pulse width and effect send. Depth can be positive or negative. One source may push several destinations, and one destination may sum several sources. Modular synths use patch cables; software synths reduce it to a table.

## Knobs and ears

Vibrato is an LFO on pitch, with small depth and fast rate. A filter wobble is an LFO on cutoff, and slowly it reads as breathing. An envelope on pitch gives a percussion-like fall; velocity on cutoff makes accents brighter. Too much depth drives a destination into its limit, where it sticks. When sources sum, leave headroom, or one will hide the other.

## What the ear should catch

On a long note, decide whether vibrato moves pitch or level. Then hear whether the pad's brightness rises and falls in a cycle. Finally compare accent and soft notes and judge whether velocity is routed to cutoff. Naming the source and the destination is the point.

```audiolab
{"type": "instrument", "gm": "Pad 2 (warm)", "synth": "bowed", "phrase": ["A3", "E4", "A4", "E5"], "label": "One LFO pushing two destinations", "label_en": "One LFO pushing two destinations", "hint": "先听长音，再想象 LFO 同时推音高与截止；颤音很浅，明暗起伏很慢，两者速度可以分开", "hint_en": "Hear the held note, then imagine one LFO pushing pitch and cutoff at once; the vibrato is shallow and the brightness moves slowly, so the two depths stay separate"}
```

## Easy to get wrong

That modulation means adding an effect; that more sources always improve a patch; that negative depth and summed routes can be ignored, when they decide the final direction and amount.
:::
