---
id: spectral-synthesis
site: prod
cat: B3
title: 频谱合成
title_en: Spectral Synthesis
summary: 把声音拆成频率与时间的二维图，再逐格重建。
summary_en: Split sound into a frequency-time map, then rebuild it cell by cell.
level: standard
tags: [合成, 频谱, 分音, 数字合成]
tags_en: [synthesis, spectral, partials, digital]
alias: [频谱合成, 谱合成, 频谱重塑, spectral synthesis]
links:
  - "[[glossary:harmonics]]"
  - "[[glossary:timbre]]"
  - "[[instrument:software-synth]]"
  - "[[period:contemporary]]"
instances:
  - oga-000150 | 长音铺底与西塔琴、音效层叠置，频谱密集且持续
  - oga-000033 | 钟琴与管钟占据高音区，高频分音一层层堆叠
  - oga-000079 | 弦乐与金属音效交叠，宽带成分让频谱边界变模糊
sources:
  - Miller Puckette, The Theory and Technique of Electronic Music.
  - Udo Zölzer, DAFX.
updated: 2026-10-28
---

::: zh
## 要解决的事

如果声音只是一张「频率随时间变化的图」，能不能直接在图上改，再把它变回声音？频谱合成把音色当成一张可编辑的图像。

## 工作方式

短时傅里叶变换把声音切成短帧，每帧得到一组频率与幅度。所有帧排起来就是频谱图。合成时反过来，把每帧的幅度与相位送进逆变换，重叠相加得到波形。在图上涂改，等于直接改分音：抹掉一条线就少一个泛音，拉长一条线就让某个分音持续。相位必须连贯，否则帧与帧之间会出现咔嗒。计算量比减法大，但编辑的自由度也大。

## 数值怎么变成声音

帧长决定时间与频率的分辨率：帧长则频率细、时间糊，帧短则相反。窗口形状影响旁瓣，旁瓣高会让相邻分音互相污染。改幅度最直观，改相位则常带来金属或空洞的音色。冻结一段频谱再让它慢慢演化，会得到拖长的、没有起音的声音。

## 耳朵要抓的点

先听持续的长音铺底，注意它的高频不是慢慢衰减，而是一直挂着。再听钟琴，每个分音像一条独立的线。最后听音效层，宽带噪声在频谱上是一片雾，而不是一条线。

```audiolab
{"type":"instrument","gm":"Pad 6 (metallic)","synth":"metal","phrase":["C4","G4","C5","G5"],"label":"分音被当作可编辑的线","label_en":"Partials treated as editable lines","hint":"先听金属铺底，再想象只留下几条分音线；线越少，声音越像被冻结的钟，而不是完整的铺底","hint_en":"Hear the metallic pad, then imagine keeping only a few partial lines; fewer lines make it read as a frozen bell rather than a full pad"}
```

## 容易弄错的

以为频谱合成等于加法合成；以为图上改了什么就一定能听见，相位与窗口也会改变结果；忽略计算与延迟成本。
:::

::: en
## The problem to solve

If a sound is a map of frequency against time, could you edit the map and turn it back into audio? Spectral synthesis treats timbre as a redrawable image.

## The working principle

A short-time Fourier transform cuts the sound into frames, each yielding frequencies and magnitudes. Stacking the frames produces a spectrogram. Synthesis runs the reverse: magnitudes and phases go through an inverse transform, and frames overlap-add into a waveform. Painting the map edits partials directly; erase a line and a harmonic disappears, stretch one and it rings longer. Phase must stay coherent, or clicks appear between frames. Computation is heavier than subtractive synthesis, but the editing freedom is greater.

## From numbers to sound

Frame length trades time against frequency resolution: long frames give fine frequency detail but smear time; short frames do the opposite. Window shape controls sidelobes, and strong ones let neighbouring partials contaminate each other. Changing magnitude is intuitive; changing phase often adds a metallic or hollow colour. Freeze a spectrum and let it evolve and the result is stretched, with no real attack.

## What the ear should catch

Hear a pad and notice that its highs do not decay but hang in place. Then hear a glockenspiel, where each partial reads as a separate line. Finally hear an effects layer, where broadband noise looks like fog rather than a line.

```audiolab
{"type": "instrument", "gm": "Pad 6 (metallic)", "synth": "metal", "phrase": ["C4", "G4", "C5", "G5"], "label": "Partials treated as editable lines", "label_en": "Partials treated as editable lines", "hint": "先听金属铺底，再想象只留下几条分音线；线越少，声音越像被冻结的钟，而不是完整的铺底", "hint_en": "Hear the metallic pad, then imagine keeping only a few partial lines; fewer lines make it read as a frozen bell rather than a full pad"}
```

## Easy to get wrong

That spectral synthesis is just additive synthesis; that any map edit must be audible, when phase and windowing shape the result; that computing and latency costs can be ignored.
:::
