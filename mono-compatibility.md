---
id: mono-compatibility
site: prod
cat: A6
title: 单声道兼容检查
title_en: Mono Compatibility Check
summary: 折叠到单声道后主唱、底鼓、贝斯仍要在，宽度才算成立。
summary_en: If the lead, kick and bass survive the mono fold, the width is trustworthy.
level: standard
tags: [混音, 单声道, 相位, 检查]
tags_en: [mixing, mono, phase, check]
alias: [单声道兼容, 单声道检查, 相位检查, mono compatibility, mono check]
links:
  - "[[glossary:bus]]"
  - "[[glossary:stems]]"
  - "[[instrument:drum-kit]]"
  - "[[period:contemporary]]"
instances:
  - oga-000004 | 多声部铺开后折成单声道，掩蔽与相位问题会暴露
  - pdmx-000087 | 钢琴宽织体，单声道下低音与和弦的平衡更容易判断
  - groove-000000 | 鼓组展宽后折成单声道，镲片与军鼓是否变薄一听便知
sources:
  - Huber and Runstein, Modern Recording Techniques, mono compatibility — background checked, not quoted
  - David Gibson, The Art of Mixing, phase and mono chapter — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

在耳机上很宽的混音，折成单声道可能变薄、变闷，甚至丢掉一条声部。问题不总在展宽器，也可能在相位。

## 目标与判断

单声道检查不是复古，而是验证相关性。左右相同的内容会相加，反相的内容会抵消。判断标准是折叠后主唱、底鼓与贝斯仍在，且没有元素明显消失。宽度可以保留，但中心必须成立。

## 做法

在总线上放单声道开关，或把左右声道相加；逐个旁通立体声展宽、哈斯延迟与乒乓延迟；发现某轨消失时，先检查相位，而不是继续加宽。给侧向元素留一点中心成分。最后在手机外放与单只音箱上复核。单声道下降三分贝以内属正常，骤降才需要查相位。

## 听什么

听主唱是否变远；听镲片与和弦是否变薄；听贝斯是否有空洞；切换单声道时总电平是否大幅下降。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"立体声弦乐","label_en":"Stereo strings","hint":"先听立体声，再按单声道监听","hint_en":"Hear it in stereo, then listen in mono"}
```

## 常见误解

以为单声道只适合俱乐部；以为宽度越大越专业；以为相位问题只能靠耳朵猜。
:::

::: en
## The problem

A mix that feels wide on headphones can thin out, turn dull, or lose a part when folded to mono. The cause is not always the widener; it may be phase.

## Goal and judgement

A mono check tests correlation, not nostalgia. Identical left and right add; opposite phase cancels. The lead, kick and bass must survive the fold, and no element should vanish. Width is allowed, but the centre must hold.

## Method

Use a mono switch on the master, or sum left and right. Bypass stereo wideners, Haas delays and ping-pong delays one at a time. If a track disappears, check phase before adding width. Leave some centre content in side elements. Finish on a phone speaker and a single cabinet. A drop of up to 3 dB in mono is normal; a sudden collapse calls for a phase check.

## What to listen for

Whether the lead moves away; whether cymbals and chords thin out; whether the bass develops a hole; whether the overall level drops sharply in mono.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C4", "E4", "G4", "C5"], "label": "Stereo strings", "label_en": "Stereo strings", "hint": "先听立体声，再按单声道监听", "hint_en": "Hear it in stereo, then listen in mono"}
```

## Common misconceptions

That mono is only for clubs; that more width is more professional; that phase problems can only be guessed by ear.
:::
