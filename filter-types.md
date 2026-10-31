---
id: filter-types
site: prod
cat: A7
title: 滤波器的四种响应
title_en: Four Filter Responses
summary: 低通、高通、带通与陷波各让哪一段通过，斜率与 Q 如何改变听感。
summary_en: What low-pass, high-pass, band-pass and notch filters pass, and how slope and Q change what you hear.
level: standard
tags: [效果器, 滤波器, 频率, 合成]
tags_en: [effects, filter, frequency, synthesis]
alias: [滤波器, 低通, 高通, 带通, 陷波, filter, low-pass, high-pass]
links:
  - "[[glossary:eq]]"
  - "[[instrument:organ]]"
  - "[[glossary:automation]]"
instances:
  - oga-000009 | 游戏场景音乐以持续铺底为主，扫低通时共振峰最容易辨认
  - mutopia-001412 | 钢琴与弦乐的混合织体，高通逐级上移时能听出哪一层先退
  - groove-000010 | 鼓组循环含明显低频与镲片，适合比较高通与带通对两端的取舍
sources:
  - Udo Zölzer, DAFX — Digital Audio Effects, filters chapter — background checked, not quoted
  - Sound On Sound, synthesizer filter primer — slopes and resonance checked, not quoted
updated: 2026-10-28
---

::: zh
## 这件事难在哪

低通、高通、带通、陷波常被当成 EQ 的四种曲线，其实它们回答的是另一个问题，让哪一段通过。斜率与共振才是听感的主要来源。

## 工作方式

低通保留截止频率以下，高通保留以上；带通只留中间一段，陷波只挖掉一条窄缝。每增加一阶，斜率约增加 6 dB/倍频程，常见的是 12 与 24 dB。截止点定在 −3 dB 处，Q 抬高会在那里形成共振峰，Q 很高时甚至自激。

## 旋钮与耳朵

24 dB 低通扫到 200 Hz 以下，鼓会失去敲击的实体；12 dB 更自然，但漏掉的高频更多。高通放在 80–120 Hz 能清掉隆隆声，再往上男声开始变薄。带通 Q 在 2–6 时像电话，陷波 Q 过 10 只咬住一条线，适合削掉共振或啸叫。

## 耳朵要抓的点

用持续和弦扫截止频率，注意共振峰先出现再消失。换一段噪声音色切高通，嘶声会一层层退掉。

```audiolab
{"type":"instrument","gm":"Synth Strings 1","synth":"bowed","phrase":["A3","C4","E4","A4"],"label":"持续和弦","label_en":"Sustained chord","hint":"先听干声，再用低通从 8 kHz 往下扫","hint_en":"Hear it dry, then sweep a low-pass down from 8 kHz"}
```

## 容易弄错的

把滤波器等同于 EQ；以为斜率越陡越干净，其实相位与瞬态要付代价；把共振当成温暖。
:::

::: en
## What makes it hard

Low-pass, high-pass, band-pass and notch are often treated as four EQ curves. They answer a different question, which part is allowed through, and slope and resonance shape the result.

## The working principle

A low-pass keeps content below the cutoff and a high-pass keeps content above. A band-pass leaves a middle slice; a notch removes a narrow strip. Each additional order adds about 6 dB per octave of slope, with 12 and 24 dB the common choices. The cutoff sits at the minus 3 dB point, and raising Q builds a resonant peak there, high enough at extreme settings to self-oscillate.

## Knobs and ears

Sweep a 24 dB low-pass below 200 Hz and a drum loses its body; 12 dB sounds more natural but leaks more highs. A high-pass at 80 to 120 Hz clears rumble, and higher up it thins a male voice. A band-pass around Q 2 to 6 sounds like a telephone; a notch above Q 10 bites one narrow line, useful on a resonance or a squeal.

## What the ear should catch

Sweep the cutoff on a sustained chord and notice the resonant peak arrive before it disappears. On a noisy timbre, raise the high-pass and hear the hiss retreat layer by layer.

```audiolab
{"type": "instrument", "gm": "Synth Strings 1", "synth": "bowed", "phrase": ["A3", "C4", "E4", "A4"], "label": "Sustained chord", "label_en": "Sustained chord", "hint": "先听干声，再用低通从 8 kHz 往下扫", "hint_en": "Hear it dry, then sweep a low-pass down from 8 kHz"}
```

## Easy to get wrong

That a filter is just an EQ; that steeper is always cleaner, though phase and transients pay for it; that resonance equals warmth.
:::
