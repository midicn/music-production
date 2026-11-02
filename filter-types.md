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
  - oga-000009 | 持续铺底的音符素材，可另渲染后施加实际滤波 | Sustained-note material for separate rendering and actual filtering
  - mutopia-001412 | 钢琴与弦乐的声部参照，没有扫动高通的对照版本 | Piano-and-string parts without a high-pass sweep comparison
  - groove-000010 | 鼓组编制参照，不能用原始 MIDI 代替滤波频响测量 | Drum instrumentation reference, not a substitute for filter-response measurement
sources:
  - "https://docs.scipy.org/doc/scipy/reference/signal.html"
  - Udo Zölzer, DAFX.
  - Sound On Sound, synthesizer filter primer.
updated: 2026-11-02
---

::: zh
## 这件事难在哪

低通、高通、带通、陷波常被当成 EQ 的四种曲线，其实它们回答的是另一个问题，让哪一段通过。斜率与共振才是听感的主要来源。

## 工作方式

低通、高通、带通和陷波分别保留低频、高频、中间频带或削弱一段频带。常见滤波器每增加一阶，远离过渡带的渐近斜率约增加 6 dB/倍频程；具体截止点定义和响应依类型而定，不能一律当作 −3 dB。Q 可表示共振或带宽的关系，但高 Q 是否自激取决于滤波器的电路或算法设计。

## 旋钮与耳朵

24 dB 低通扫到 200 Hz 以下，鼓会失去敲击的实体；12 dB 更自然，但漏掉的高频更多。高通放在 80–120 Hz 能清掉隆隆声，再往上男声开始变薄。带通 Q 在 2–6 时像电话，陷波 Q 过 10 只咬住一条线，适合削掉共振或啸叫。

## 耳朵要抓的点

用含宽频能量的声音扫动截止频率：提高高通截止会先削掉低频，降低低通截止会先削掉高频。想处理高频嘶声，应试低通或有针对性的高频衰减，而不是把高通截止不断抬高。原有音符演示可听滤波音色变化，但不能代替显示频响曲线的测量。

```audiolab
{"type":"instrument","gm":"Synth Strings 1","synth":"bowed","phrase":["A3","C4","E4","A4"],"label":"持续音色参照","label_en":"Sustained timbre reference","hint":"先熟悉这段持续音的频谱感受；此播放器没有低通扫频控件，滤波对照应在实际滤波器上完成。","hint_en":"Become familiar with this sustained sound. This player has no low-pass sweep control; perform filtering comparisons with an actual filter."}
```

## 容易弄错的

把滤波器等同于 EQ；以为斜率越陡越干净，其实相位与瞬态要付代价；把共振当成温暖。
:::

::: en
## What makes it hard

Low-pass, high-pass, band-pass and notch are often treated as four EQ curves. They answer a different question, which part is allowed through, and slope and resonance shape the result.

## The working principle

Low-pass, high-pass, band-pass and notch filters retain lows, highs, a middle band, or attenuate a band respectively. For common designs, each order adds roughly 6 dB per octave of asymptotic slope away from the transition band. Cutoff definition and response depend on design and are not universally −3 dB. Q relates to resonance or bandwidth; high Q causes self-oscillation only in designs that support it.

## Knobs and ears

Sweep a 24 dB low-pass below 200 Hz and a drum loses its body; 12 dB sounds more natural but leaks more highs. A high-pass at 80 to 120 Hz clears rumble, and higher up it thins a male voice. A band-pass around Q 2 to 6 sounds like a telephone; a notch above Q 10 bites one narrow line, useful on a resonance or a squeal.

## What the ear should catch

Sweep a broadband sound: raising a high-pass cutoff removes low frequencies first, while lowering a low-pass cutoff removes highs first. To address high-frequency hiss, try a low-pass or targeted high-frequency attenuation rather than continually raising a high-pass cutoff. Note-based examples can illustrate a tonal change but do not replace a measured response curve.

```audiolab
{"type":"instrument","gm":"Synth Strings 1","synth":"bowed","phrase":["A3","C4","E4","A4"],"label":"Sustained timbre reference","label_en":"Sustained timbre reference","hint":"Become familiar with this sustained sound. This player has no low-pass sweep control; perform filtering comparisons with an actual filter.","hint_en":"Become familiar with this sustained sound. This player has no low-pass sweep control; perform filtering comparisons with an actual filter."}
```

## Easy to get wrong

That a filter is just an EQ; that steeper is always cleaner, though phase and transients pay for it; that resonance equals warmth.
:::
