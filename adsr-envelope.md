---
id: adsr-envelope
site: prod
cat: B3
title: 包络 ADSR
title_en: The ADSR Envelope
summary: 四个时间段，决定音头、持续与余音的形状。
summary_en: Four stages shape the attack, the sustain and the tail of every note.
level: standard
tags: [合成, 包络, ADSR, 动态]
tags_en: [synthesis, envelope, ADSR, dynamics]
alias: [ADSR, 包络, 起音衰减持续释放, envelope, attack decay sustain release]
links:
  - "[[glossary:timbre]]"
  - "[[glossary:velocity]]"
  - "[[instrument:organ]]"
  - "[[period:modern]]"
instances:
  - oga-000163 | 锯齿主音短句与长铺底并存，起音与释放的差别一耳可辨
  - oga-000143 | 管钟与拉杆风琴同曲，击发后的长衰减和持续音形成对照
  - oga-000195 | 尼龙弦吉他与闷音吉他交替，拨弦的起音与衰减长短不同
sources:
  - Gordon Reid, Sound On Sound Synth Secrets.
  - Curtis Roads, The Computer Music Tutorial.
updated: 2026-10-28
---

::: zh
## 难在哪

同样的振荡器和滤波器，为什么一个像拨弦，一个像弦乐铺底？差别往往不在波形，而在包络的四个时间段。

## 它怎么工作

起音从零升到峰值，衰减从峰值落到持续电平，持续段在按键期间保持，释放从持续电平回到零。起音与衰减是时间，持续是电平，三者常被混为一谈。包络不只控制音量，也可以控制滤波器截止、音高或脉冲宽度；力度常被映射到包络量，于是弹得越重，音头越亮。真实乐器很少是直线变化，指数形状通常更自然。

## 旋钮与耳朵

起音几毫秒像拨弦与打击，几十到几百毫秒像弓弦与气声；衰减短则音头独立，长则与持续段连成一片；持续高像风琴，持续低像拨弦；释放长会让相邻音符叠在一起，释放短则收得干净。释放还会被复音数截断，尾音可能突然消失。

## 耳朵要抓的点

先听锯齿主音与长铺底，注意前者起音快、释放短，后者两头都慢。再听管钟与风琴，前者一击之后一路衰减，后者按住多久就响多久。最后对比尼龙弦与闷音吉他，起音相同而衰减长度不同。

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"长起音与长释放的铺底","label_en":"A pad with a long attack and release","hint":"先听它的软起音，再想象起音 400 毫秒、释放 1.5 秒时，音符会怎样连成一片","hint_en":"Hear the soft attack, then imagine 400 ms of attack and 1.5 s of release blending the notes into one surface"}
```

## 容易弄错的

把持续当成一段时间，其实它是电平；把释放当成混响，其实它属于音符本身；以为起音越短越清楚，过短会让音头变成咔哒声。
:::

::: en
## Where it gets hard

With the same oscillator and filter, why does one patch read as a pluck and another as a pad? Often it is not the waveform but the four envelope stages.

## How it works

Attack rises to peak, decay falls to sustain, sustain holds while the key is down, and release returns to zero when it lifts. Attack and decay are times, sustain is a level. It can also shape cutoff, pitch or pulse width. Velocity often maps to envelope amount, so a harder note opens brighter. Exponential shapes usually sound more natural than straight lines.

## Knobs and ears

An attack of a few milliseconds reads as a pluck or a hit; tens to hundreds of milliseconds read as a bow or breath. A short decay separates the attack, a long one joins it to sustain. High sustain reads as an organ, low as a pluck. A long release overlaps notes, a short one closes cleanly.

## What the ear should catch

Hear the saw lead and the long pad, noting the fast attack and short release of the first against the slow ends of the second. Then hear the tubular bells and the organ; one decays after a strike, the other sounds while held. Finally compare nylon and muted guitar, same attack, different decay length.

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"A pad with a long attack and release","label_en":"A pad with a long attack and release","hint":"Hear the soft attack, then imagine 400 ms of attack and 1.5 s of release blending the notes into one surface","hint_en":"Hear the soft attack, then imagine 400 ms of attack and 1.5 s of release blending the notes into one surface"}
```

## Easy to get wrong

That sustain is a length of time, when it is a level; that release is reverb, when it belongs to the note itself; that a shorter attack is always clearer, when too short clicks.
:::
