---
id: modulation-effects-in-mix
site: prod
cat: A6
title: 调制类效果
title_en: Modulation Effects in the Mix
summary: 合唱、镶边与相位器让声音变宽，也让瞬态变软。
summary_en: Chorus, flanging and phasing widen a sound and soften its transients at the same time.
level: standard
tags: [混音, 调制, 合唱, 镶边, 相位器]
tags_en: [mixing, modulation, chorus, flanging, phasing]
alias: [调制类效果, 调制效果, 合唱效果, modulation effects, chorus and flanger]
links:
  - "[[glossary:modulation]]"
  - "[[glossary:delay]]"
  - "[[glossary:stereo-technique]]"
instances:
  - oga-000067 | 锯齿主音与合成贝斯持续发声，调制在长音上最容易听出
  - oga-000004 | 弦乐铺底加宽后是否糊掉攻击，这一段可当场判断
  - oga-000002 | 失真吉他与清音吉他同场，相位器的扫频在吉他上最清楚
sources:
  - Zölzer, Udo，DAFX — Digital Audio Effects（Wiley）— 调制延迟与梳状滤波章节核对，未引用
  - Sound On Sound, chorus, flanger and phaser explained — 参数与听感描述核对，未引用
updated: 2026-10-28
---

::: zh
## 卡住的地方
合唱、镶边与相位器都能让声音变宽，但代价常被忽略：瞬态变软、低频摆动、单声道塌陷。混音里要决定的是用在哪一层，而不是用不用。

## 原理与做法
三者都靠被调制的短延迟。延迟在一到十毫秒之间产生梳状滤波，扫动时就是镶边或相位器；十五到三十五毫秒、多路失谐则像几支乐器齐奏，是合唱。立体声两路用反相的低频振荡器推动，宽度来自左右差异，差异越大中间能量越少。速率决定晃动的快慢，深度决定失谐量，干湿比决定原声保留多少。

## 参数与取舍
优先用在持续音，例如铺底、弦乐与背景人声。底鼓与贝斯尽量不经过调制，或给侧链加高通。宽度不要超过原声，干湿比通常低于一半。每次加完做单声道检查，中间的人声与贝斯不能消失。相位器与镶边的区别在延迟级数与反馈，不在名字。

## 耳朵要抓的点
弦乐加合唱后是否变宽而音头是否变糊，吉他和弦经过相位器是否出现缓慢扫频，镶边的喷气声是否盖住拨弦的细节。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C3","G3","C4","E4","G4","C5"],"label":"弦乐长音","label_en":"Sustained strings","hint":"先听干净的齐奏，再想象两路失谐叠加后，宽度与音头各自怎样变化","hint_en":"Hear the clean unison first, then imagine two detuned copies and how width and attack each change"}
```

## 容易弄错的
把调制当成万能加宽器。它加的是差异，不是信息；过度使用会让混音在单声道里塌掉，也会让低频失去重心。
:::

::: en
## Where it snags
Chorus, flanging and phasing all widen a sound, and all charge a price that is easy to ignore: softer transients, wobbling bass and a collapse in mono. The mixing decision is which layer receives them, not whether to use them.

## Principle and practice
All three rely on a modulated short delay. Between one and ten milliseconds the delay forms a comb filter, and sweeping it gives flanging or phasing. Between fifteen and thirty-five milliseconds, several detuned copies resemble several players in unison, which is chorus. In stereo, two paths driven by opposite-phase low-frequency oscillators create width from left-right difference; more difference means less centre. Rate sets the wobble, depth sets the detuning, and the wet control decides how much dry sound survives.

## Settings and trade-offs
Use them on sustained material: pads, strings and backing voices. Keep kick and bass out of the modulation, or high-pass the sidechain. Do not let width exceed the dry signal, and keep the wet level below half. Check mono after every addition; the centre voice and bass must not vanish. Phaser and flanger differ in delay stages and feedback, not in name.

## What the ear catches
Do strings widen without smearing their attack, does a guitar chord sweep slowly through a phaser, does the flanger's jet sound cover the pick detail?

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C3", "G3", "C4", "E4", "G4", "C5"], "label": "Sustained strings", "label_en": "Sustained strings", "hint": "先听干净的齐奏，再想象两路失谐叠加后，宽度与音头各自怎样变化", "hint_en": "Hear the clean unison first, then imagine two detuned copies and how width and attack each change"}
```

## Common misconceptions
Treating modulation as a universal widener. It adds difference, not information; overuse collapses the mix in mono and takes the weight out of the low end.
:::
