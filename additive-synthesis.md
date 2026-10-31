---
id: additive-synthesis
site: prod
cat: B3
title: 加法合成
title_en: Additive Synthesis
summary: 把正弦一层层叠起来，直接写出谐波结构。
summary_en: Stack sine waves one by one and write the harmonic structure directly.
level: standard
tags: [合成, 加法, 泛音, 风琴]
tags_en: [synthesis, additive, partials, organ]
alias: [加法合成, 泛音合成, 拉杆风琴, additive synthesis, additive]
links:
  - "[[glossary:timbre]]"
  - "[[glossary:eq]]"
  - "[[instrument:organ]]"
  - "[[period:modern]]"
instances:
  - oga-000143 | 拉杆风琴由各次谐波推子叠加，推子组合改变音色厚度
  - oga-000309 | 铃音与空灵铺底叠置，高频分音一层层加上去
  - oga-000233 | 教堂管风琴以整倍数泛音叠加，低音区厚、高音区亮
sources:
  - Curtis Roads, The Computer Music Tutorial.
  - Jean-Baptiste Fourier, Théorie analytique de la chaleur.
updated: 2026-10-28
---

::: zh
## 要解决的事

既然任何音色都能拆成正弦波，为什么不直接叠起来，而要绕道滤波器和 FM？加法合成给的正是这条直路。

## 它怎么工作

一个周期波可以写成基频与各次谐波的叠加。每个分音有自己的频率、幅度与相位；放在整数倍上得到有音高的音色，放在非整数倍上得到钟与金属。拉杆风琴最直观，每根拉杆对应一组谐波，推子位置就是各分音的幅度。加法重合成先分析声音的分音，再用振荡器把它重建出来。分音越多，谱越细，计算也越重。

## 旋钮与耳朵

各分音的电平决定明暗与厚薄，奇次分音突出时有空洞的木管感，偶次分音补进来会更饱满。高次分音衰减快，音头亮而尾巴暗；分音一起长鸣，音色就像风琴。轻微失谐会让分音拍频，声音变宽。相位会改变瞬态形状，但对稳定段音色影响较小。

## 耳朵要抓的点

先听拉杆风琴，注意音色厚度随分音组合变化，而不是靠滤波扫出来的。再听铃音，高次分音多而衰减快，所以一击之后迅速变暗。最后听教堂管风琴，低音区分音密，高音区反而更透。

```audiolab
{"type":"instrument","gm":"Drawbar Organ","synth":"blown","phrase":["C4","E4","G4","C5"],"label":"拉杆风琴的泛音叠加","label_en":"Partials stacked into a drawbar organ","hint":"先听整体的厚，再想象只留下奇次分音，音色会立刻变空；加法就是在这组推子上做加减","hint_en":"Hear the full body, then imagine keeping only odd partials; the tone turns hollow at once, and additive synthesis is that set of drawbars"}
```

## 容易弄错的

以为加法只能做风琴，它也能做钟与金属；以为分音越多越好，过多的高次分音会刺耳；以为相位完全无所谓，相位会改变起音的形状。
:::

::: en
## The problem to solve

If every timbre splits into sines, why not stack them instead of filtering or FM? Additive synthesis is that direct route.

## How it works

A periodic wave can be written as a fundamental plus its harmonics. Each partial has its own frequency, amplitude and phase. Place partials on integer multiples and the result has pitch; place them between multiples and it reads as a bell or metal. The drawbar organ is clearest, where each drawbar sets one harmonic group. Additive resynthesis analyses a sound into partials and rebuilds it. More partials mean a finer spectrum and more computation.

## Knobs and ears

Partial levels set brightness and weight. Strong odd partials give a hollow, woody tone; adding even partials fills it out. High partials that decay fast make a bright head, dark tail; partials that ring together sound like an organ. Slight detuning makes partials beat and widens the tone. Phase shapes the transient but matters less when steady.

## What the ear should catch

Hear the drawbar organ and notice that thickness comes from the partial mix, not from a filter sweep. Then hear the bell, where many high partials decay quickly and the strike darkens at once. Finally hear the church organ, dense in the low register and clearer up top.

```audiolab
{"type":"instrument","gm":"Drawbar Organ","synth":"blown","phrase":["C4","E4","G4","C5"],"label":"Partials stacked into a drawbar organ","label_en":"Partials stacked into a drawbar organ","hint":"Hear the full body, then imagine keeping only odd partials; the tone turns hollow at once, and additive synthesis is that set of drawbars","hint_en":"Hear the full body, then imagine keeping only odd partials; the tone turns hollow at once, and additive synthesis is that set of drawbars"}
```

## Easy to get wrong

That additive only makes organs, when it also makes bells and metal; that more partials are better, when too many turn harsh; that phase does not matter, when it shapes the attack.
:::
