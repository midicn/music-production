---
id: dynamic-contrast
site: prod
cat: A2
title: 动态对比
title_en: Dynamic Contrast
summary: 对比来自前后参照，先用配器做出落差，再动推子。
summary_en: Contrast needs a reference. Build the drop with orchestration first, then move faders.
level: standard
tags: [编曲, 动态, 力度]
tags_en: [arranging, dynamics, contrast]
alias: [动态对比, 力度对比, dynamic contrast, terraced dynamics]
links:
  - "[[glossary:dynamics]]"
  - "[[glossary:crescendo]]"
  - "[[instrument:timpani]]"
  - "[[period:classical]]"
instances:
  - mutopia-000497 | 贝多芬第五交响曲首乐章，主题在弱与强之间反复换挡
  - mutopia-000514 | 贝多芬第七交响曲首乐章，长段渐强靠重复与配器累积
  - atepp-004908 | 贝多芬 Op.110 第二乐章，突强、停顿与尾声的力度落差清楚
sources:
  - The New Grove Dictionary of Music and Musicians, 2nd ed., entry Dynamics（Oxford University Press），用于核对力度层级与配器关系
  - Walter Piston, Orchestration（W. W. Norton, 1955），用于核对强弱对比在乐队中的实现方式
updated: 2026-10-28
---

::: zh
动态对比靠参照。全曲都强，强就不再是强。先有弱，才有大。编曲可以用配器做出落差，撤一层比推推子更自然，也更容易在回放设备上成立。

## 问题
从头到尾一个力度，高潮会消失。只靠自动化推音量，弱段往往糊，强段又挤。

## 织体或频段
弱奏时减层数与高频，强奏时加宽低音，加入铜管或鼓。低频的增减比整体响度更能制造大小。旋律音区要保住，否则强奏只剩厚度，没有方向。

## 做法
先画一条力度曲线，标出三个必须听见的落差。用配器实现，先决定撤哪层、加哪层，再动推子。突强前留一拍空，长渐强至少预留八小节，否则听起来像突然变响。

## 听什么
听贝多芬第五交响曲首乐章主题的弱强交替。听第七交响曲首乐章的长渐强怎样靠重复累积。再听 Op.110 第二乐章的突强与停顿。

## 常见误解
动态不等于音量自动化，换织体往往更有效。强弱记号也不是绝对值，取决于前后文与演奏空间。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C2","C2","C5","C5","G2","G2","E5","E5"],"label":"低音与高音交替","label_en":"Low and high in alternation","hint":"听音区与厚度的变化怎样制造大小，不要只比较响度","hint_en":"Hear how register and weight create size, not just loudness"}
```
:::

::: en
Dynamic contrast depends on a reference. If everything is loud, loud stops being loud. The quiet has to exist first. Arrangement can build the drop with orchestration, and removing a layer usually sounds more natural than pushing a fader.

## The problem
One level from start to finish erases the climax. Rely on volume automation alone and quiet passages turn muddy while loud ones crowd.

## Texture or frequency band
In soft passages, reduce layers and high frequencies. In loud ones, widen the bass and add brass or drums. Adding and removing low end creates more size than overall level. Keep the melody's register intact, or the loud passage becomes weight without direction.

## Approach
Draw a dynamic curve and mark three drops that must be heard. Realise them through orchestration first, deciding which layer leaves and which enters, then move faders. Leave one beat of silence before a sudden accent, and allow at least eight bars for a long crescendo, or it will sound like a sudden jump.

## What to listen for
Hear the alternation of soft and strong in the first movement of Beethoven's Fifth. Hear how repetition accumulates in the long crescendo of the Seventh. Then hear the sudden accents and pauses in the second movement of Op. 110.

## Common misunderstandings
Dynamics are not volume automation, and changing texture is often more effective. A dynamic mark is not an absolute value either, since it depends on context and the performance space.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C2", "C2", "C5", "C5", "G2", "G2", "E5", "E5"], "label": "Low and high in alternation", "label_en": "Low and high in alternation", "hint": "听音区与厚度的变化怎样制造大小，不要只比较响度", "hint_en": "Hear how register and weight create size, not just loudness"}
```
:::
