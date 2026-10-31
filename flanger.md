---
id: flanger
site: prod
cat: A7
title: 镶边
title_en: Flanging
summary: 短延迟与反馈如何扫出一排梳状陷波，听感像喷气机掠过。
summary_en: How a short delay and feedback sweep a comb of notches, heard as a jet passing overhead.
level: standard
tags: [效果器, 调制, 镶边, 梳状滤波]
tags_en: [effects, modulation, flanger, comb filtering]
alias: [镶边, 法兰, 梳状滤波, flanger, flange]
links:
  - "[[glossary:comb-filtering]]"
  - "[[glossary:modulation]]"
  - "[[instrument:electric-guitar]]"
instances:
  - groove-000000 | 放克鼓循环的闭镲短促，镶边扫过时金属色最容易被抓住
  - oga-000057 | 太空题材的铺底长音多，缓慢扫动会形成连续的呼啸
  - mutopia-000005 | 古典吉他分解和弦颗粒清楚，梳状陷波经过时音色会变空
sources:
  - Udo Zölzer, DAFX — Digital Audio Effects, modulation chapter — background checked, not quoted
  - Curtis Roads, The Computer Music Tutorial, delay and comb filtering sections — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 要解决的事

镶边听起来像一束声音在中频扫过，带一点喷气机的呼啸。它来自一个很短的延迟，而不是混响或合唱。

## 声音是怎么来的

输入与延迟 0.5–10 ms 的信号相加，产生梳状滤波，陷波间隔等于延迟时间的倒数。LFO 让延迟时间缓慢变化，陷波就上下扫动。反馈把输出送回延迟线，让陷波更深、更尖；有的电路让左右声道反向扫动，宽度更大。延迟长到 20 ms 以上、且不加深反馈时，听感更接近合唱。

## 旋钮与耳朵

rate 0.1–2 Hz 适合缓慢扫过整段；depth 决定扫动范围；feedback 超过 60% 会明显啸叫。干湿各半最容易听出梳状结构。放在鼓组上，镲片会先出现金属色的扫动；放在持续和弦上，扫动更连贯。

## 耳朵要抓的点

先听放克鼓循环的闭镲，打开镶边后注意每一击的尾音是否被拉出一条移动的金属带。再把反馈从 20% 推到 70%，听陷波变尖。最后做单声道检查，左右反相设置可能让中央声部变薄。

```audiolab
{"type":"instrument","gm":"Electric Guitar (clean)","synth":"plucked","phrase":["E3","B3","E4","G4","B4","G4","E4"],"label":"清音吉他的和弦","label_en":"Clean guitar chords","hint":"先听干声，再想象短延迟扫过时那一排移动的陷波","hint_en":"Hear it dry, then picture the moving notches of a short delay sweep"}
```

## 容易弄错的

把镶边与合唱混为一谈；以为反馈越大越好；在总线上加镶边却不检查单声道兼容。
:::

::: en
## The problem to solve

Flanging sounds like a band of tone sweeping through the midrange with a jet-like whistle. It comes from a very short delay, not from reverb or chorus.

## Where the sound comes from

The input is summed with a copy delayed by 0.5 to 10 ms, creating comb filtering. Notch spacing equals the reciprocal of the delay time. An LFO moves the delay slowly, so the notches sweep. Feedback deepens and sharpens them; some circuits sweep the channels in opposite directions for width. Past about 20 ms with low feedback, the effect leans toward chorus.

## Knobs and ears

A rate of 0.1 to 2 Hz suits a slow sweep across a section. Depth sets its range, and feedback above 60 percent whistles. An equal blend makes the comb clearest. On drums, cymbals take on a metallic sweep first; on sustained chords the motion is smoother.

## What the ear should catch

Play the closed hats of a funk loop, engage the flanger and hear whether each tail is pulled into a moving metallic band. Push feedback from 20 to 70 percent and listen to the notches sharpen. Then check in mono, because an inverted stereo setting can thin the centre.

```audiolab
{"type": "instrument", "gm": "Electric Guitar (clean)", "synth": "plucked", "phrase": ["E3", "B3", "E4", "G4", "B4", "G4", "E4"], "label": "Clean guitar chords", "label_en": "Clean guitar chords", "hint": "先听干声，再想象短延迟扫过时那一排移动的陷波", "hint_en": "Hear it dry, then picture the moving notches of a short delay sweep"}
```

## Easy to get wrong

That flanging and chorus are the same effect; that more feedback is always better; that a flanged bus needs no mono check.
:::
