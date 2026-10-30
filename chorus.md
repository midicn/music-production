---
id: chorus
site: prod
cat: A7
title: 合唱效果
title_en: Chorus
summary: 几毫秒的延迟摆动如何造出宽度，速率与深度又该怎么听。
summary_en: How a few milliseconds of modulated delay create width, and how rate and depth change what you hear.
level: standard
tags: [效果器, 调制, 宽度, 听感]
tags_en: [effects, modulation, width, listening]
alias: [合唱, 合唱效果, 合声, chorus]
links:
  - "[[glossary:delay]]"
  - "[[glossary:bus]]"
  - "[[instrument:electric-guitar]]"
instances:
  - pdmx-000070 | 弦乐长音持续稳定，合唱的轻微音高摆动与加宽最容易听出
  - oga-000009 | 游戏场景铺底音色本来就宽，加合唱后能判断宽度是否过头
  - mutopia-001412 | 钢琴与弦乐混合，低音区加合唱后是否失焦一听便知
sources:
  - Udo Zölzer, DAFX — Digital Audio Effects, modulation chapter — background checked, not quoted
  - Sound On Sound, chorus and vibrato explained — typical rates and depths checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

合唱效果听起来像「变宽了」，于是常被当成空间效果。它其实靠的是几毫秒级的时间摆动，让同一条信号与自己错开，产生音高与相位的微小差别。

## 原理

输入分成两路，一路干燥，一路经过 15–35 ms 的延迟，延迟时间被 0.1–3 Hz 的 LFO 缓慢调制。延迟变短时音高略升，变长时略降，两路相加产生梳状滤波；多声部合唱用几个相位不同的 LFO，让摆动不整齐。湿声越多，直达声被削弱得越明显。

## 参数与听感

速率低、深度浅时像双轨录音，适合人声与弦乐；速率快、深度大就接近颤音，钢琴会显得走音。立体声模式把两路分到左右，宽度立刻增加；低频不做单声道处理会散开。

## 听什么

用清音电吉他弹一个长音，先听干声，再加合唱，注意音高轻微起伏与两侧差异。换到低音区，听它是否开始失焦。

```audiolab
{"type":"instrument","gm":"Electric Guitar (clean)","synth":"plucked","phrase":["E3","B3","E4","G4"],"label":"清音吉他","label_en":"Clean guitar","hint":"先听干声，再加浅速合唱","hint_en":"Hear it dry, then add a slow, shallow chorus"}
```

## 常见误解

把合唱当混响；以为声部越多越厚；在低频上大量使用却不检查单声道。
:::

::: en
## The question

Chorus sounds like width, so it is often filed as a space effect. It really works through a few milliseconds of time wobble, running a signal against a delayed copy and creating tiny differences in pitch and phase.

## How it works

The input splits into a dry path and a copy delayed by 15 to 35 ms, with the delay time modulated by a 0.1 to 3 Hz LFO. A shorter delay raises pitch slightly and a longer one lowers it, and summing the two paths creates comb filtering. Multi-voice chorus uses several LFOs at different phases so the wobble is not uniform. More wet signal weakens the direct sound.

## Settings and what you hear

Slow and shallow reads as double tracking, good on vocals and strings. Fast and deep approaches vibrato, and a piano starts to sound out of tune. Stereo mode splits the paths left and right for instant width; low frequencies spread apart unless they are kept mono.

## What to listen for

Hold a long note on a clean electric guitar, first dry, then with chorus, and notice the slight pitch movement and the difference between sides. Move down to the low register and hear whether it starts to lose focus.

```audiolab
{"type": "instrument", "gm": "Electric Guitar (clean)", "synth": "plucked", "phrase": ["E3", "B3", "E4", "G4"], "label": "Clean guitar", "label_en": "Clean guitar", "hint": "先听干声，再加浅速合唱", "hint_en": "Hear it dry, then add a slow, shallow chorus"}
```

## Common misconceptions

That chorus is reverb; that more voices mean more thickness; that heavy use on bass is safe without a mono check.
:::
